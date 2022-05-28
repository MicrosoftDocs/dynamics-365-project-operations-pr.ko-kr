---
title: 프로젝트 일정 API 성능
description: 이 항목은 프로젝트 일정 API의 성능 벤치마크에 대한 정보를 제공하고 최적의 사용을 위한 모범 사례를 식별합니다.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593850"
---
# <a name="project-schedule-api-performance"></a>프로젝트 일정 API 성능

_**적용 대상:** 리소스/비재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 발행 처리, Project for the Web_

이 항목에서는 프로젝트 일정 API(응용 프로그래밍 인터페이스)의 성능 벤치마크에 대한 정보를 제공하고 사용 최적화를 위한 모범 사례를 식별합니다.

## <a name="project-scheduling-service"></a>프로젝트 일정 서비스
프로젝트 일정 서비스는 Microsoft Azure에서 실행되는 다중 테넌트 서비스입니다. 사용자가 프로젝트에서 작업할 때 빠르고 유연한 경험을 제공하여 상호 작용을 개선하도록 설계되었습니다. 이러한 개선은 변경 요청을 수락하고 처리한 다음 즉시 결과를 반환함으로써 달성됩니다. 서비스는 Dataverse에 비동기적으로 지속되며 사용자가 다른 작업을 수행하는 것을 차단하지 않습니다.

프로젝트 일정 API는 프로젝트 일정 서비스에 의존하여 이 토픽 뒷부분에 자세히 설명된 요청을 실행합니다.

프로젝트 일정 API는 다음 WBS(작업 분할 구조) 엔터티와 함께 작동하도록 설계되었습니다.

  - Project
  - 프로젝트 작업
  - 프로젝트 작업 종속성
  - 프로젝트 팀 구성원
  - 리소스 할당
  
기본 필드와 사용자 정의 필드가 모두 지원됩니다. 달리 명시되지 않는 한 생성, 업데이트 및 삭제와 같은 모든 일반 작업이 지원됩니다. 자세한 내용은 [프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행](schedule-api-preview.md)을 참조하십시오.

프로젝트 일정 API의 일부로 작업 단위 패턴이 추가되었습니다. 이 패턴을 OperationSet이라고 하며 하나의 트랜잭션에서 여러 요청을 처리해야 할 때 사용할 수 있습니다.

다음 그림은 이 기능을 사용할 때 파트너가 경험하게 될 흐름을 보여줍니다.

![Dataverse 및 프로젝트 일정 서비스 흐름.](./media/dataverse-project-scheduling-service-flow.png)

**1단계**: 클라이언트가 Dataverse에서 OData(Open Data Protocol) 끝점에 대한 API 호출을 수행하여 OperationSet을 생성합니다.

**2단계**: 새로운 OperationSet이 생성된 후, **OperationSetId** 값이 반환됩니다.

**3단계**: 클라이언트가 **OperationSetId** 값을 사용하여 다른 프로젝트 일정 API 요청을 만듭니다. 결과는 일정 엔터티에 대한 생성, 업데이트 또는 삭제 요청입니다. 이 요청이 수행되면 메타데이터 유효성 검사가 수행됩니다. 유효성 검사가 실패하면 요청이 종료되고 오류가 반환됩니다.

**4a-4c 단계**: 이 단계는 ACCEPT 단계를 나타냅니다. 클라이언트는 **ExecuteOperationSetV1** API를 호출하여 모든 변경 사항을 프로젝트 일정 서비스에 일괄적으로 보냅니다. 프로젝트 일정 서비스는 일괄 처리의 요청에 대해 자체 유효성 검사를 실행합니다. 모든 유효성 검사 실패는 일괄 처리를 실행 취소하고 호출자에게 예외를 반환합니다. 프로젝트 일정 서비스에서 배치를 성공적으로 수락하면 OperationSet 상태가 업데이트되어 OperationSet이 프로젝트 일정 서비스에서 처리되고 있다는 사실을 반영합니다.

**5단계**: 이 단계는 PERSIST 단계를 나타냅니다. 프로젝트 일정 서비스는 트랜잭션에서 Dataverse에 일괄 처리를 비동기적으로 씁니다. 쓰기 작업이 성공하면 OperationSet이 **완료됨** 으로 표시됩니다. 모든 오류는 트랜잭션과 배치를 롤백하고 OperationSet은 **실패** 로 표시됩니다.

## <a name="performance-methodology"></a>성능 방법론
실행 시간은 **ExecuteOperationSetV1** API 호출부터 프로젝트 일정 서비스가 Dataverse에 쓰기를 마칠 때까지의 시간으로 정의됩니다. 모든 작업은 총 2,200회 실행되며 P99 실행 시간 측정값이 보고됩니다. 단일 레코드 및 대량 작업이 측정됩니다.

단일 레코드 작업의 경우 OperationSet에는 하나의 요청이 포함됩니다. 대량 작업의 경우 20, 50 또는 100개의 요청이 포함됩니다. 각 벌크 크기는 별도로 보고됩니다.

이러한 작업은 북미의 UR 15 Project Operations Lite 배포에서 실행됩니다.

## <a name="results"></a>결과
### <a name="create-operations"></a>작업 만들기
#### <a name="single-record-create-operations"></a>단일 레코드 만들기 작업
다음 표는 단일 레코드 만들기에 대한 실행 시간을 보여줍니다. 시간은 초 단위입니다.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">레코드&nbsp;&nbsp;&nbsp;유형</th>
    <th class="tg-0lax" colspan="2">시간</th>
  </tr>
  <tr>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">작업</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">할당</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">팀 구성원</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">종속성</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>대량 만들기 작업
다음 표는 많은 레코드 만들에 대한 실행 시간을 보여줍니다. 특히 Microsoft는 단일 OperationSet에서 20, 50, 100개의 레코드를 만들기 위한 실행 시간을 측정했습니다. 시간은 초 단위입니다.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">레코드&nbsp;&nbsp;&nbsp;유형</th>
    <th class="tg-0lax" colspan="6">시간</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20개 레코드</th>
    <th class="tg-0lax" colspan="2">50개 레코드</th>
    <th class="tg-0lax" colspan="2">100개 레코드</th>
  </tr>
  <tr>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">작업</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">할당</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">종속성</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> **프로젝트** 및 **팀 구성원** 엔터티의 대량 작성 작업은 이 표에 포함되지 않습니다. 단일 레코드를 만들기 위한 API가 여러 번 호출될 때 해당 작업의 런타임이 런타임과 유사하기 때문입니다. 이러한 API는 Dataverse에서 즉시 실행됩니다.

다음 그림에서는 20, 50 및 100개의 레코드가 생성되고 지원되는 모든 필드가 사용되는 경우 **작업**, **할당** 및 **종속성** 엔터티에 대한 실행 시간 플롯을 보여줍니다.

![레코드 실행 시간 그래프를 생성합니다.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>작업 업데이트
#### <a name="single-record-update-operations"></a>단일 레코드 업데이트 작업
다음 표는 단일 레코드 업데이트에 대한 실행 시간을 보여줍니다. 시간은 초 단위입니다.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">레코드&nbsp;&nbsp;&nbsp;유형</th>
    <th class="tg-0lax" colspan="2">시간</th>
  </tr>
  <tr>
    <th class="tg-0lax">필수 필드 </th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">작업</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">팀 구성원</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **리소스 할당** 및 **프로젝트 작업 종속성** 엔터티에 대한 업데이트 작업은 지원되지 않습니다.

#### <a name="bulk-update-operations"></a>대량 업데이트 작업
다음 표는 많은 레코드 업데이트에 대한 실행 시간을 보여줍니다. 특히 Microsoft는 단일 OperationSet에서 20, 50, 100개의 레코드를 업데이트하기 위한 실행 시간을 측정했습니다. 시간은 초 단위입니다.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">레코드&nbsp;&nbsp;&nbsp;유형</th>
    <th class="tg-0lax" colspan="6">시간</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20개 레코드</th>
    <th class="tg-0lax" colspan="2">50개 레코드</th>
    <th class="tg-0lax" colspan="2">100개 레코드</th>
  </tr>
  <tr>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
    <th class="tg-0lax">필수 필드</th>
    <th class="tg-0lax">지원되지 않는 모든 필드</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">작업</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">팀 구성원</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **리소스 할당** 및 **프로젝트 작업 종속성** 엔터티에 대한 업데이트 작업은 지원되지 않습니다.

다음 그림은 20, 50 및 100개의 레코드가 업데이트되고 지원되는 모든 필드가 사용될 때 작업 및 팀 구성원 엔티티의 실행 시간 플롯을 보여줍니다.

![레코드 실행 시간 그래프를 업데이트합니다.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>삭제 작업
#### <a name="single-record-delete-operations"></a>단일 레코드 삭제 작업
다음 표는 단일 레코드 삭제에 대한 실행 시간을 보여줍니다. 시간은 초 단위입니다.

| 레코드 종류 | 시간  |
|-------------|-------|
| 작업        | 20.12 |
| 할당  | 10.86 |
| 팀 구성원 | 12.52 |
| 종속성  | 20.89 |

> [!NOTE]
> **프로젝트** 엔터티에 대한 삭제 작업은 지원되지 않습니다.

#### <a name="bulk-delete-operations"></a>대량 삭제 작업 
다음 표는 많은 레코드 삭제에 대한 실행 시간을 보여줍니다. 특히 Microsoft는 단일 OperationSet에서 20, 50, 100개의 레코드를 삭제하기 위한 실행 시간을 측정했습니다. 시간은 초 단위입니다.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">레코드&nbsp;&nbsp;&nbsp;유형</th>
    <th class="tg-0lax" colspan="3">시간</th>
  </tr>
  <tr>
    <th class="tg-0lax">20개 레코드</th>
    <th class="tg-0lax">50개 레코드</th>
    <th class="tg-0lax">100개 레코드</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">작업</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">할당</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">팀 구성원</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">종속성</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **프로젝트** 엔터티에 대한 삭제 작업은 지원되지 않습니다.

다음 그림은 20개, 50개 및 100개의 레코드가 삭제될 때 **작업**, **할당**, **팀 구성원** 및 **종속성** 엔터티에 대한 실행 시간의 플롯을 보여줍니다.

![레코드 실행 시간 그래프를 삭제합니다.](./media/delete-record-execution-time.png)

## <a name="observations"></a>관찰
각 레코드 작업에 대해 **ExecuteOperationSet** API가 프로젝트 일정 서비스에 요청을 보내는 데 약 800밀리초가 걸립니다. 그런 다음 프로젝트 일정 서비스는 페이로드를 처리하고 Dataverse를 호출하는 데 약 5초가 걸립니다. 나머지 실행 시간은 비즈니스 로직을 실행하고 Dataverse에서 데이터베이스에 데이터를 쓰는 데 사용됩니다.

100개의 레코드가 생성, 업데이트 또는 삭제되면 **ExecuteOperationSet** API가 프로젝트 일정 서비스에 요청을 보내는 데 약 3초가 걸립니다. 그런 다음 프로젝트 일정 서비스는 요청을 처리하고 Dataverse를 호출하는 데 약 5초가 걸립니다. 대량 작업은 OperationSet의 모든 레코드에 대해 **프로젝트 일정 서비스 세금** 을 한 번만 지불해야 합니다. 따라서 대량 작업은 단일 레코드 작업보다 평균 실행 시간이 훨씬 짧습니다.

## <a name="scenarios"></a>시나리오
다음 표는 특정 시나리오를 수행하기 위해 프로젝트 일정 API를 사용하는 경우의 실행 시간을 보여줍니다. 시간은 초 단위입니다.

| 시나리오                                                                   | 시간  |
|----------------------------------------------------------------------------|-------|
| 40개의 작업이 있는 프로젝트를 만듭니다.                                      | 36.01 |
| 40개 작업과 20개 종속성이 있는 프로젝트를 만듭니다.                  | 38.11 |
| 40개 작업과 30개 할당이 있는 프로젝트를 만듭니다.                   | 60.17 |
| 40개 작업, 20개 종속성 및 30개 할당이 있는 프로젝트를 만듭니다. | 60.27 |

## <a name="best-practices"></a>모범 사례
앞의 시나리오 결과에 따르면 API는 다음 조건에서 더 잘 수행됩니다.

  - 가능한 한 많은 작업을 그룹화하십시오. 대량 작업의 평균 런타임은 단일 레코드 작업의 평균 런타임보다 낫습니다. 사용 중인 OperationSet 수가 적을수록 평균 실행 시간이 빨라집니다.
  - 시나리오를 수행하는 데 필요한 최소 속성만 설정하십시오. OperationSet 요청에 포함된 비필수 필드 유형을 선택하십시오. 외래 키 또는 롤업 필드가 포함된 필드는 성능에 부정적인 영향을 미칩니다.
