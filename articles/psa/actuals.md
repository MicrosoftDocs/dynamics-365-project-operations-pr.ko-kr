---
title: 실제 개요
description: 이 항목은 프로젝트 실제값에 대한 정보를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15c8d26fcf4eb9fda8a4fe4ce085ea3becdc2c76f11525357b75f59e18fd6017
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992484"
---
# <a name="actuals-overview"></a>실제 개요

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

실제값은 프로젝트에서 완료된 작업의 양입니다. 프로젝트 실제값은 소스 문서까지 추적할 수 있습니다. 그러한 소스 문서에는 시간, 비용 및 분개장 항목과 송장도 포함되어 있습니다.

![프로젝트 실제값가 소스 문서까지 추적되는 방법.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>시간 항목 제출

PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 두 개의 분개장 행이 만들어집니다. 한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다. 고정 가격 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다. 

기본 가격을 입력하는 논리는 분개장 행에 들어있습니다. 시간 항목의 모든 필드 값이 분개장 행에 복사됩니다. 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화의 필드들이 사용되어 해당 가격표가 결정됩니다. 

기본 가격에 영향을 주는 **역할** 및 **조직 단위** 같은 필드는 기본적으로 해당 가격이 분개장 행에 입력되도록 합니다. 시간 항목에 맞춤 필드를 추가하고 필드 값을 실제값에 전파하려는 경우, 실제값 엔터티에 필드를 만들고 필드 매핑을 사용하여 시간 항목의 필드를 실제값로 복사합니다.

## <a name="submitting-an-expense-entry"></a>경비 항목 제출

PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 두 개의 분개장 행이 만들어집니다. 한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다. 고정 가격 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다.

경비를 위한 기본 가격을 입력하는 논리는 **경비 입력** 페이지에서 선택하는 경비 카테고리에 근거합니다. 해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다. 그러나 가격 자체의 경우, 사용자가 입력한 금액은 기본적으로 비용 및 매출액을 위한 관련 경비 분개장 행에 직접 설정됩니다.

현재 버전의 PSA에서는 경비 항목에 대한 단위당 기본 가격의 카테고리별 입력은 불가능합니다.

## <a name="using-entry-journals-to-record-costs"></a>항목 분개장을 사용한 비용 기록

PSA에서는 항목 분개장을 사용하면 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다. 분개장에는 표제, 행 및 **확인** 작업이 있습니다. 다음은 분개장을 사용할 수 있는 몇 가지 시나리오입니다:

- 귀하가 프로젝트에 대한 자재 실제값 비용 및 매출액을 기록해야 합니다.
- 다른 시스템의 처리 실제값를 PSA로 이동해야 합니다.
- 다른 시스템에서 발생한, 조달 또는 하청 비용과 같은 비용을 기록해야 합니다.

> [!IMPORTANT]
> 항목 분개장을 사용하여 실제를 생성하는 것은 실제가 프로젝트에 미치는 회계 영향을 완전히 알고 있는 사용자만 수행해야 합니다. 이는 애플리케이션이 분개장 항목 유형 또는 분개장 항목에 입력된 관련 가격을 검증하지 않기 때문입니다. 이 분개장 유형의 영향으로 항목 분개장을 작성할 수 있는 액세스 권한이 부여된 사람에 대해 적절한 주의를 기울여야 합니다.     


## <a name="recording-actuals-based-on-project-events"></a>프로젝트 이벤트에 근거한 실제값 기록

PSA는 프로젝트 중에 발생하는 재무 처리를 기록합니다. 이러한 처리는 **실제값** 으로 기록됩니다. 다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.

**리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다**

<table>
<thead>
<tr>
<th rowspan="3">이벤트</th>
<th colspan="4">청구 가능 또는 판매된 프로젝트</th>
<th rowspan="3">판매전 단계의 프로젝트</th>
<th rowspan="3">내부 프로젝트</th>
</tr>
<tr>
<th colspan="2">시간 및 자재</th>
<th colspan="2">고정 가격</th>
</tr>
<tr>
<th>실제</th>
<th>거래 통화</th>
<th>고정 가격</th>
<th>거래 통화</th>
</tr>
</thead>
<tbody>
<tr>
<td>시간 항목이 만들어졌습니다.</td>
<td colspan="6">실제값 엔터티의 활동 없음</td>
</tr>
<tr>
<td>시간 항목이 제출되었습니다.</td>
<td colspan="6">실제값 엔터티의 활동 없음</td>
</tr>
<tr>
<td rowspan="2">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</td>
<td>비용 실제값</td>
<td>계약 단위 통화</td>
<td rowspan="2">비용 실제값</td>
<td rowspan="2">계약 단위 통화
<td rowspan="2">비용 실제값</td>
<td rowspan="2">비용 실제값</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="3">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</td>
<td>비용 실제값</td>
<td>계약 단위 통화</td>
<td rowspan="3">비용 실제값</td>
<td rowspan="3">계약 단위 통화</td>
<td rowspan="3">비용 실제값</td>
<td rowspan="3">비용 실제값</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="2">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</td>
<td>청구되지 않은 매출액 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="2">이정표를 위한 청구된 매출액</td>
<td rowspan="2">프로젝트 계약 통화</td>
<td rowspan="2">해당 없음</td>
<td rowspan="2">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="3">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</td>
<td>청구되지 않은 매출액 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액 – 새 수량에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>청구된 매출액 – 차이에 대해 청구 불가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="2">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</td>
<td>청구된 매출액 – 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="5">
<ul>
<li>이정표를 위한 청구된 매출액 전환</li>
<li>이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</li>
</ul>
</td>
<td rowspan="5">프로젝트 계약 통화</td>
<td rowspan="5">해당 없음</td>
<td rowspan="5">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="3">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</td>
<td>청구된 매출액 – 전환</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>새 수량에 대한 청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>미청구된 매출액 – 차이에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
</tbody>
</table>

**리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다**

<table>
<thead>
<tr>
<th rowspan="3">이벤트</th>
<th colspan="4">청구 가능 또는 판매된 프로젝트</th>
<th rowspan="3">판매전 단계의 프로젝트</th>
<th rowspan="3">내부 프로젝트</th>
</tr>
<tr>
<th colspan="2">시간 및 자재</th>
<th colspan="2">고정 가격</th>
</tr>
<tr>
<th>실제</th>
<th>거래 통화</th>
<th>고정 가격</th>
<th>거래 통화</th>
</tr>
</thead>
<tbody>
<tr>
<td>시간 항목이 만들어졌습니다.</td>
<td colspan="6">실제값 엔터티의 활동 없음</td>
</tr>
<tr>
<td>시간 항목이 제출되었습니다.</td>
<td colspan="6">실제값 엔터티의 활동 없음</td>
</tr>
<tr>
<td rowspan="4">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</td>
<td>비용 실제값</td>
<td>계약 단위 통화</td>
<td rowspan="4">비용 실제값</td>
<td rowspan="4">계약 단위 통화</td>
<td rowspan="4">비용 실제값</td>
<td rowspan="4">비용 실제값</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>리소스 단위 비용</td>
<td>리소스 단위 통화</td>
</tr>
<tr>
<td>조직간 매출액</td>
<td>계약 단위 통화</td>
</tr>
<tr>
<td rowspan="5">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</td>
<td>비용 실제값</td>
<td>계약 단위 통화</td>
<td rowspan="5">비용 실제값</td>
<td rowspan="5">계약 단위 통화</td>
<td rowspan="5">비용 실제값</td>
<td rowspan="5">비용 실제값</td>
</tr>
<tr>
<td>리소스 단위 비용</td>
<td>리소스 단위 통화</td>
</tr>
<tr>
<td>조직간 매출액</td>
<td>계약 단위 통화</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="2">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</td>
<td>청구되지 않은 매출액 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="2">이정표를 위한 청구된 매출액</td>
<td rowspan="2">프로젝트 계약 통화</td>
<td rowspan="2">해당 없음</td>
<td rowspan="2">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="3">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</td>
<td>청구되지 않은 매출액 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
<td rowspan="3">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액 – 새 수량에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>청구된 매출액 – 차이에 대해 청구 불가능</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="2">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</td>
<td>청구된 매출액 – 전환</td>
<td>프로젝트 계약 통화</td>
<td rowspan="5">
<ul>
<li>이정표를 위한 청구된 매출액 전환</li>
<li>이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</li>
</ul>
</td>
<td rowspan="5">프로젝트 계약 통화</td>
<td rowspan="5">해당 없음</td>
<td rowspan="5">해당 없음</td>
</tr>
<tr>
<td>청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td rowspan="3">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</td>
<td>청구된 매출액 – 전환</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>새 수량에 대한 청구된 매출액</td>
<td>프로젝트 계약 통화</td>
</tr>
<tr>
<td>미청구된 매출액 – 차이에 대해 청구 가능</td>
<td>프로젝트 계약 통화</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]