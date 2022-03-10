---
title: 실제
description: 이 토픽은 Microsoft Dynamics 365 Project Operations에서 실제 값으로 작업하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a086fe0be67c21ed73793b6f3b58b47ad08eaa4e8a4c98870b4b2264562e3dce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991809"
---
# <a name="actuals"></a>실제 값 

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

실제는 프로젝트에 대한 검토 및 승인된 재무 및 일정 진행 상황을 나타냅니다. 시간, 경비, 재료 사용 항목, 분개장 항목 및 송장의 승인 결과로 생성됩니다.

## <a name="journal-lines-and-time-submission"></a>분개장 항목 및 시간 제출

시간 항목에 대한 자세한 내용은 [시간 항목 개요](../time/time-entry-overview.md)를 참조하십시오.

### <a name="time-and-materials"></a>시간 및 자재

제출된 시간 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.

### <a name="fixed-price"></a>고정 가격

제출된 시간 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 생성합니다.

### <a name="default-pricing"></a>기본 가격

기본 가격을 작성하는 논리는 분개장 항목에 들어있습니다. 시간 항목의 필드 값이 분개장 항목에 복사됩니다. 이러한 값에는 트랜잭션 날짜, 프로젝트가 매핑된 계약 내용 및 해당 가격표의 통화 결과가 포함됩니다.

기본 가격에 영향을 주는 **역할** 및 **리소싱 단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다. 시간 항목에 사용자 지정 필드를 추가할 수 있습니다. 필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다. 사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다. 트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.

## <a name="journal-lines-and-basic-expense-submission"></a>분개장 항목 및 기본 경비 제출

경비 항목에 대한 자세한 내용은 [경비 개요](../expense/expense-overview.md)를 참조하십시오.

### <a name="time-and-materials"></a>시간 및 자재

제출된 기본 경비 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.

### <a name="fixed-price"></a>고정 가격

제출된 기본 경비 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 만듭니다.

### <a name="default-pricing"></a>기본 가격

경비에 대한 기본 가격을 입력하는 논리는 경비 범주를 기반으로 합니다. 해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다. 기본 가격에 영향을 주는 **트랜잭션 범주** 및 **단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다. 그러나 이것은 가격표의 가격 책정 방법이 **단가** 인 경우에만 작동합니다. 가격 책정 방법이 **원가** 또는 **비용 초과 가격 인상액** 인 경우 경비 항목이 생성될 때 입력된 가격이 비용에 사용되며 판매 분개장 항목의 가격은 가격 책정 방법을 기준으로 계산됩니다. 

경비 항목에 사용자 정의 필드를 추가할 수 있습니다. 필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다. 사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다. 트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.

## <a name="journal-lines-and-material-usage-log-submission"></a>분개장 항목 및 재료 사용량 로그 제출

경비 항목에 대한 자세한 내용은 [재료 사용량 로그](../material/material-usage-log.md)를 참조하십시오.

### <a name="time-and-materials"></a>시간 및 자재

제출된 재료 사용량 로그 항목이 시간 및 재료 계약 내용에 매핑된 프로젝트에 링크되면 시스템은 비용 및 미청구 판매에 대한 두 개의 분개장 항목을 생성합니다.

### <a name="fixed-price"></a>고정 가격

제출된 재료 사용량 로그 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 만듭니다.

### <a name="default-pricing"></a>기본 가격

재료의 기본 가격을 입력하는 논리는 제품 및 단위 조합을 기반으로 합니다. 해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다. 기본 가격에 영향을 주는 **제품 ID** 및 **단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다. 그러나 이것은 카탈로그 제품에만 적용됩니다. 직접 입력 제품의 경우 재료 사용량 로그 항목 생성시 입력한 가격이 분개장 항목의 원가 및 판매 가격에 사용됩니다. 

**재료 사용량 로그** 항목에 사용자 정의 필드를 추가할 수 있습니다. 필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다. 사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다. 트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.

## <a name="use-entry-journals-to-record-costs"></a>항목 분개장을 사용하여 비용 기록

항목 분개장을 사용하여 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다. 분개장은 다음과 같은 목적으로 사용할 수 있습니다.

- 다른 시스템의 트랜잭션 실제를 Microsoft Dynamics 365 Project Operations로 이동합니다.
- 다른 시스템에서 발생한 비용을 기록합니다. 이러한 비용에는 조달 또는 하도급 비용이 포함될 수 있습니다.

> [!IMPORTANT]
> 애플리케이션은 분개장 항목 유형 또는 분개장 항목에 입력된 관련 가격을 검증하지 않습니다. 따라서 실제 값이 프로젝트에 미치는 회계 영향을 완전히 알고 있는 사용자만 항목 분개장을 사용하여 실제 값을 만들어야 합니다. 이 분개장 유형의 영향으로 인해 항목 분개장을 만들 수 있는 액세스 권한이 있는 사람을 신중하게 선택해야 합니다.

## <a name="record-actuals-based-on-project-events"></a>프로젝트 이벤트에 근거한 실제값 기록

Project Operations는 프로젝트 중에 발생하는 재무 트랜잭션을 기록합니다. 이러한 처리는 실제값으로 기록됩니다. 다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다

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

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다

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
