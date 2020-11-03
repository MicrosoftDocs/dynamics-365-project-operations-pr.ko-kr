---
title: 견적 - 주요 개념
description: 이 항목은 Project Operations에서 사용할 수 있는 프로젝트 견적 및 판매 견적에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42ea1eb71b3285159b3fdf79ba34a562f948fd6e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080218"
---
# <a name="quotes---key-concepts"></a>견적 - 주요 개념

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations에는 두 가지 유형의 견적, 프로젝트 및 판매가 있습니다. 두 가지 유형의 견적은 다음과 같은 방식으로 다릅니다.

- **라인 항목에 대한 그리드** : 영업 견적에는 라인 항목에 대한 그리드가 하나만 있습니다. 프로젝트 견적에는 라인 항목에 대한 두 개의 그리드가 있습니다. 한 그리드는 프로젝트 라인용이고 다른 그리드는 제품 라인용입니다.
- **활성화 및 수정** : 판매 견적은 활성화 및 수정을 지원합니다. 이러한 프로세스는 프로젝트 견적에서 지원되지 않습니다.
- **첨부된 주문** : 영업 견적에 여러 주문을 첨부할 수 있습니다. 프로젝트 견적에는 하나의 프로젝트 계약만 첨부할 수 있습니다.
- **견적 받기** : 판매 견적을 받으면 관련 영업 기회가 열려 있을 수 있습니다. 프로젝트 견적을 따낸 후에 관련 영업 기회가 닫힙니다.
- **필드 및 개념** : 영업 견적에는 프로젝트 견적에 포함된 일부 필드 및 개념을 포함하지 않습니다. 필드에는 **계약 단위** , **거래처 관리자** 및 **청구할 연락처 이름** 이 포함됩니다.  
- **유형** : 영업 견적 및 프로젝트 견적은 **유형** 이라는 옵션 집합 기반 필드로 식별됩니다. 영업 견적의 경우, 이 필드에는 **항목 기반** 값이 있습니다. 프로젝트 견적의 경우, **작업 기반** 값이 있습니다.

이 항목은 프로젝트 견적의 세부 정보에 초점을 맞춥니다.

Project Operations의 프로젝트 견적에는 여러 라인 항목 또는 견적 라인이 있을 수 있습니다. 실제로 프로젝트 견적에는 라인 항목에 대한 두 개의 그리드가 있습니다. 하나의 그리드는 상세한 예상을 허용하는 프로젝트 기반 라인입니다. 다른 그리드는 간단한 단가 및 수량 기반 접근 방식을 사용하는 제품 기반 라인에 대한 것입니다.

- **프로젝트 기반** : 필요한 작업량을 예상한 후 견적 금액 값이 결정됩니다. 프로젝트 및 프로젝트 계획을 사용하여 각 견적 라인 아래의 라인 세부 사항으로 직접 또는 기초 견적을 기반으로 높은 수준에서 작업을 추정할 수 있습니다. 프로젝트 기반 견적 라인은 Project Operations를 사용하여 만든 프로젝트 기반 견적에서만 찾을 수 있습니다. 이러한 유형의 견적 라인은 Microsoft Dynamics 365 Sales에서 사용할 수 있는 직접 입력 견적 라인의 사용자 지정 양식입니다.

- **제품 기반** : 판매 단위와 단위 영업 가격을 기준으로 견적 금액 값이 결정됩니다. 제품 기반 라인의 제품은 영업의 제품 카탈로그에서 제공되거나 정의한 제품일 수 있습니다. 이러한 유형의 견적 라인은 Project Operations를 사용하여 만든 프로젝트 기반 견적에서도 사용할 수 있습니다.

견적의 금액은 제품 기반 라인과 프로젝트 기반 라인의 합계입니다.

> [!NOTE]
> Project Operations에서는 견적과 견적 라인이 필요하지 않습니다. 프로젝트 계약(판매된 프로젝트)으로 프로젝트 프로세스를 시작할 수 있습니다. 그러나 견적 또는 프로젝트 계약으로 시작하든 관계없이 항상 영업 기회가 필요합니다.

## <a name="project-based-quote-lines"></a>프로젝트 기반 견적 라인

Project Operations의 프로젝트 기반 견적 라인에는 다음과 같은 청구 방법이 있습니다.

- 시간 및 재료
- 고정 가격

### <a name="time-and-material"></a>시간 및 재료

시간 및 재료 청구 방법은 소비를 기반으로 합니다. 이 청구 방법을 선택하면 프로젝트에 비용이 발생하면 고객에게 송장이 발부됩니다. 송장은 날짜 기반 주기적 빈도로 작성됩니다. 영업 프로세스 중에 시간 및 재료 구성 요소의 견적 값은 고객에게 최종 비용을 예상할 뿐입니다. 공급업체는 정확히 인용된 값으로 프로젝트를 완료하는 데 커밋하지 않습니다. 시간 및 재료 구성 요소는 고객의 위험을 증가시킵니다. 고객은 위험을 최소화하기 위해 추가 미초과 조항을 협상할 수 있습니다. Project Operations는 미초과 조항 설정을 지원하지 않습니다.

### <a name="fixed-price"></a>고정 가격

고정 가격 청구 방법에서 공급업체는 고객에게 고정된 비용으로 프로젝트를 제공하기 위해 자체적으로 커밋합니다. 고객은 공급업체가 해당 견적 라인을 제공하기 위해 발생하는 비용에 관계없이 고정 가격 견적 라인의 견적 값으로 청구됩니다. 고정 가격 견적 라인 값은 다음 방법 중 하나로 청구됩니다. 

- 프로젝트의 시작 또는 끝에 일괄 금액으로 또는 프로젝트 이정표에 도달할 때. 
- 견적 라인에 고정된 값의 동일한 할부의 날짜 기반 빈도로. 이러한 할부는 주기적인 이정표라고 합니다.
- 작업 진행 또는 프로젝트에서 달성된 특정 이정표와 일치하는 금전적 가치가 있는 할부. 이 경우 각 할부의 값은 다를 수 있지만 모두 견적 라인의 고정 값까지 합산해야 합니다.

Project Operations는 고정 가격 견적 라인에 대한 세 가지 유형의 송장 일정을 모두 지원합니다.

## <a name="transaction-classification"></a>거래 분류

전문 서비스 조직은 일반적으로 비용 분류별로 고객에게 견적과 송장을 발부합니다. 비용은 다음 거래 분류로 표시됩니다.

- **시간** : 이 분류는 프로젝트에 대한 인건비 또는 인적 자원의 시간을 나타냅니다.
- **경비** : 이 분류는 프로젝트에 대한 다른 모든 종류의 경비를 나타냅니다. 경비는 광범위하게 분류될 수 있으므로 대부분의 조직에서는 여행, 렌터카, 호텔 또는 사무용품과 같은 하위 범주를 만듭니다.
- **수수료** : 이 분류는 기타 간접비, 위약금 및 고객에게 청구되는 기타 항목을 나타냅니다. 
- **세금** - 이 분류는 사용자가 비용을 입력하는 동안 추가하는 세금 금액을 나타냅니다.
- **재료 거래** : 이 분류는 확인된 프로젝트 송장의 제품 라인의 실제를 나타냅니다.
- **이정표** : 이 분류는 고정 가격 청구 논리에서 사용됩니다.

이러한 거래 분류는 하나 이상 각 견적 라인과 연결될 수 있습니다. 견적을 따낸 후, 거래 분류와 견적 라인 간의 매핑이 계약 내용으로 전송됩니다.
  
예를 들어, 견적에는 다음 두 개의 견적 라인이 포함될 수 있습니다. 

- 시간 및 수수료 거래 분류가 적용되는 시간 및 재료 청구 방법을 사용하는 컨설팅 작업입니다. 예를 들어, **Dynamics AX 구현** 예제 프로젝트의 모든 시간 및 수수료 거래는 사용된 시간과 재료에 따라 고객에게 청구됩니다. 
- 고정 가격 청구 방법을 사용하는 관련 출장 경비. 예를 들어, **Dynamics AX 구현** 예제 프로젝트의 모든 출장 경비는 고정 금액으로 송장이 발부됩니다.

> [!NOTE]
> 견적 라인 또는 계약 내용과 연결된 **시간** , **경비** 및 **수수료** 의 프로젝트 및 거래 분류의 조합은 고유해야 합니다. 프로젝트 및 거래 클래스의 동일한 조합이 두 개 이상의 계약 내용 또는 견적 라인과 연결되어 있으면 Project Operations가 제대로 작동하지 않습니다.

## <a name="billing-types"></a>청구 유형

**청구 유형** 필드는 청구 가능성 개념을 정의합니다. 다음과 같은 가능한 값이 있는 옵션 집합입니다.

- **청구 가능** : 이 역할/범주에 의해 발생하는 비용은 프로젝트 실행을 유도하는 직접 비용이며 고객은 이 작업에 대해 비용을 지불하게 됩니다. 지불은 시간 및 재료 또는 고정 가격 배열로 관리될 수 있습니다. 그러나 이 시간을 사용하는 직원은 청구 가능한 사용률에 해당하는 크레딧을 받게 됩니다.
- **청구 불가능** : 이 역할/범주에 의해 발생하는 비용은 프로젝트 실행을 유도하는 직접 비용으로 고려되며, 고객이 이 팩트를 인식하지 않더라도 이 작업에 대해 비용을 지불하지 않게 됩니다. 이 시간을 사용하는 직원은 청구 가능한 사용률로 적립되지 않습니다.
- **무료** : 이 역할/범주에 의해 발생하는 비용은 프로젝트 실행을 유도하는 직접 비용으로 고려되며, 고객은 이 팩트를 인식합니다. 이 시간을 사용하는 직원은 청구 가능한 사용률로 적립됩니다. 그러나 이 비용은 고객에게 청구되지 않습니다.
- **사용할 수 없음** : 수익 추적이 필요하지 않은 내부 프로젝트에서 발생하는 비용은 이 옵션을 사용하여 추적됩니다.

## <a name="invoice-schedule"></a>송장 일정

송장 일정은 프로젝트에 대한 송장이 발생할 때 일련의 날짜입니다. 선택적으로 견적 라인에 송장 일정을 만들 수 있습니다. 각 견적 라인에는 자체 송장 일정이 있을 수 있습니다. 송장 일정을 만들려면 다음 특성 값을 제공해야 합니다.

- 청구 시작 날짜 
- 프로젝트의 청구 종료 날짜를 나타내는 배달 날짜
- 송장 빈도

이러한 세 가지 특성 값을 사용하여 잠정 날짜 집합을 생성하여 송장을 설정합니다.

## <a name="invoice-frequency"></a>송장 빈도

송장 빈도는 송장 생성 빈도를 표현하는 데 도움이 되는 특성 값을 저장하는 엔터티입니다. 다음 특성은 송장 빈도 엔터티를 표현하거나 정의합니다.

- **기간** : 월간, 격주 및 주간 기간이 지원됩니다. 
- **기간별 실행** : 주간 및 격주 기간에 대해 기간당 하나의 실행만 정의할 수 있습니다. 월별 기간의 경우, 기간당 1~4개의 실행을 정의할 수 있습니다. 
- **실행 일 수** : 송장을 실행해야 하는 날입니다. 이 특성을 두 가지 방법으로 구성할 수 있습니다.
  - **평일** : 매주 월요일 또는 두 번째 월요일에 송장이 실행되도록 지정할 수 있습니다. 근무일에 실행하도록 송장을 설정해야 하는 고객은 이러한 종류의 구성을 선호할 수 있습니다. 
  - **일정 일** : 예를 들어, 매월 7일과 21일에 송장이 실행되도록 지정할 수 있습니다. 일부 조직에서는 매달 고정된 일정에 따라 송장을 실행하는 것을 보장하는 데 도움이 되므로 이러한 종류의 구성을 선호할 수 있습니다.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>고정 가격 견적 라인에 대한 송장 일정

고정 가격 견적 라인의 경우 **송장 일정** 그리드를 사용하여 견적 라인의 값과 동일한 청구 이정표를 만들 수 있습니다.

- 동등하게 분할된 청구 이정표를 만들려면 송장 빈도를 선택하고 견적 줄에 청구 시작 날짜를 입력하고 견적 헤더의 **요약** 섹션에서 견적에 대해 **요청된 완료 날짜** 를 선택합니다. . 그런 다음 **주기적인 이정표 생성** 을 선택하여 선택한 송장 빈도에 따라 균등하게 분할된 이정표를 만듭니다. 
- 일괄 청구 이정표를 만들려면 이정표를 만든 다음 견적 라인 값을 이정표 금액으로 입력합니다.
- 프로젝트 계획의 특정 작업을 기반으로 하는 청구 이정표를 만들려면 이정표를 만들고 청구 이정표 UI에서 프로젝트의 일정 요소에 매핑합니다.