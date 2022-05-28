---
title: 리소스 관리 변경 (Project Service Automation 3.x)
description: 이 항목은 리소스 관리 영역의 변경에 대한 정보를 제공합니다.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595506"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>리소스 관리 변경 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

이 주제의 섹션들은 Dynamics 365 Project Service Automation 버전 3.x의 리소스 관리 영역에 대한 변경에 대한 정보를 제공합니다.

## <a name="project-estimates"></a>프로젝트 추산

프로젝트 추산은 **msdyn\_projecttask** 엔터티(**프로젝트 과업**)을 기반으로 하는 대신, **msdyn\_resourceassignment** 엔터티(**리소스 할당**)에 근거합니다. 리소스 할당은 과업 스케줄링 및 가격 책정을 위한 "진실의 원천"이 되었습니다.

## <a name="line-tasks"></a>행 과업

PSA 3.x에서는 행 과업이 더 이상 사용되지 않습니다(단종됨). 이제 할당이 행 과업 대신 전체 과업을 가리킵니다.

다음 예는 이전 버전의 PSA 및 PSA 3.x에서 "테스트 과업"이라는 명칭의 과업이 팀원 A와 B에게 할당되는 방법을 보여줍니다.

- **PSA 3.x 이전:**

    - 테스트 과업

        - 테스트 과업 – 행 과업 1

            - A에게 할당

        - 테스트 과업 – 행 과업 2

            - B에게 할당

- **PSA 3.x:**

    - 테스트 과업

        - A에게 할당
        - B에게 할당

## <a name="unassigned-assignment"></a>할당되지 않은 과제

PSA 3.x에서 할당되지 않은 과제는 **NULL** 팀원과 **NULL** 리소스에 할당된 과제입니다. 할당되지 않은 과제는 다음과 같은 몇 가지 시나리오에서 발생할 수 있습니다:

- 과업이 만들어졌지만 아직 팀원에게 할당되지 않은 경우 할당되지 않은 과제가 항상 만들어집니다. 
- 과업의 모든 피지정인이 제거되면 해당 과업에 대해 할당되지 않은 과제가 다시 만들어집니다.

## <a name="scheduling-fields-on-the-project-task-entity"></a>프로젝트 과업 엔터티에서의 스케줄링 필드

**msdyn\_projecttask** 엔터티의 필드가 더 이상 사용되지 않거나 **msdyn\_resourceassignment** 엔터티로 이동되었거나, 이제는 **msdyn\_projectteam** 엔터티(**프로젝트 팀원**)에서 참조됩니다.

| msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드 | msdyn\_resourceassignment(리소스 할당)에서의 새 필드 | 설명 |
|---|---|---|
| msdyn\_assignedresources | 없음 | |
| msdyn\_assignedteammembers | 없음 | |
| msdyn\_numberofresources | 없음 | |
| msdyn\_scheduledhours | 없음 | |
| msdyn\_effortcontour | msdyn\_plannedwork | 필드에 저장된 JSON(JavaScript 개체 표기형) 데이터 구조의 형식이 변경되었습니다. |

## <a name="schedule-contour"></a>스케줄 등고선

스케줄 등고선은 각 **리소스 할당** 엔터티(**msdyn\_resourceassignment**)의 **계획된 작업** 필드(**msdyn\_plannedwork**)에 저장됩니다.

### <a name="structure"></a>구조

스케줄 등고선의 새 구조는 스케줄의 각 일에 대해 정의된 유연한 시간 조각으로 구성됩니다. 각 시간 조각은 다음 속성들을 갖습니다:

- **시작** – 프로젝트 캘린더에 따른 그 날 작업 시간의 시작입니다.
- **끝** – 프로젝트 캘린더에 따른 그 날 작업 시간의 끝입니다.
- **시간 수** – 당일 할당된 시간 수입니다.

**예제**

이 예는 작업일이 UTC-8 표준 시간대에서 오전 9시부터 오후 5시까지인 프로젝트 캘린더를 사용합니다.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>자동 스케줄링 및 수동 스케줄링

과업이 자동으로 스케줄링된 경우 시간이 미리 로드되고 과업 기간이 단축될 수 있습니다.

**예제**

다음 과업은 3일(2018년 12월 3일~ 2018년 12월 5일)에 걸친 18시간을 위해 자동으로 스케줄링되었습니다.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

과업이 수동으로 스케줄링된 경우 시간 수는 모든 날짜에 균등하게 분배됩니다.

**예제**

다음 과업은 3일(2018년 12월 3일~ 2018년 12월 5일)에 걸친 18시간을 위해 수동으로 스케줄링되었습니다.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>할당 단위

할당 단위는 PSA 3.x에서 더 이상 사용되지 않습니다. 이제 과업 노력 시간 수는 할당된 모든 리소스들 사이에 일당으로 균등하게 나뉩니다.

**예**

이 예에서는 과업이 두 리소스에게 할당되고 3일에 걸친 36시간을 위해 자동 스케줄링됩니다(2018년 12월 3일~ 2018년 12월 5일).

- 할당 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 할당 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>가격 차원

PSA 3.x에서 리소스별 가격 책정 차원 필드(예: **역할** 및 **조직 단위**)가 **msdyn\_projecttask** 엔터티에서 제거되었습니다. 이제 프로젝트 추산이 생성될 때 리소스 할당(**msdyn\_resourceassignment**)의 해당 프로젝트 팀원(**msdyn\_projectteam**)에서 이러한 필드를 검색할 수 있습니다. **msdyn\_organizationalunit** 라는 새 필드가 **msdyn\_projectteam** 엔터티에 추가되었습니다.

| msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드 | 대신 사용되는 msdyn\_projectteam(프로젝트 팀원)의 필드 |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>등고선

가격 책정 및 추산 등고선 필드는 **msdyn\_projecttask** 엔터티에서 더 이상 사용되지 않습니다. 그들은 **msdyn\_resourceassignment** 엔터티로 이동되었습니다.

| msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드 | msdyn\_resourceassignment(리소스 할당)에서의 새 필드 |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

다음 필드들이 **msdyn\_resourceassignment** 엔터티에 추가되었습니다:

* msdyn\_plannedcost
* msdyn\_plannedsales

**msdyn\_projecttask** 엔터티에서 계획된, 실제값 및 남은 비용 및 매출액에 대한 다음 필드들은 변경되지 않았습니다:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
