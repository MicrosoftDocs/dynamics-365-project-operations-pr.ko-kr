---
title: 2022년 9월의 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비재고 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 9월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621286"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022년 9월의 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.46.0.60의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.29의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

| 기능 영역 | 기능 이름 | 자세한 정보 |
| --- | --- | --- |
| 영업 기회 관리 | **견적의 수정 및 활성화**<br>Project Operations는 영업 프로세스를 완벽하게 지원합니다. 프로젝트 견적을 활성화하여 견적이 읽기 전용이고 검토 중인 상태를 나타낼 수 있습니다. 활성화된 견적을 수정하여 개정 번호가 증가된 새 견적을 생성할 수 있습니다. 활성화된 프로젝트 견적 또는 견적 개정은 성공 또는 실패로 종료될 수 있습니다. | [프로젝트 견적 활성화 및 수정](/dynamics365/project-operations/sales/activation-and-revision) |
| 청구 및 가격 책정 | **표준 시간대에 구애 받지 않는 가격 기본값 설정**<br>Project Operations는 모든 프로젝트 실제에 대한 표준 시간대에 구애 받지 않는 날짜 개념을 도입했습니다. 새로운 필드인 **거래 날짜** 는 이제 분개장 항목과 실제에서 사용할 수 있으며 거래가 발생한 날짜를 저장하는 데 사용되지만 해당 날짜를 협정 세계시로 변환하지 않습니다. 이 날짜는 가격 기본값 설정 및 송장 생성과 같은 다운스트림 프로세스에 사용됩니다. | <p>[프로젝트 기반 추정 및 실제 원가율 결정](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[프로젝트 기반 추정 및 실제에 대한 판매 가격 결정](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| 청구 및 가격 책정 | **Project Operations에서 가격 조정 적용 날짜 재정의**<br>가격 조정 적용 날짜는 가격표의 특정 가격을 무시하거나 변경할 수 있는 방법을 제공합니다. | [가격 조정 적용 날짜](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 하도급 계약 | **하도급 계약 및 공급업체 송장 조정**<br>이 기능을 통해 고객은 프로젝트 작업에 사용되는 리소스 시간, 비용 범주 및 자재를 구매하기 위한 하도급 계약을 생성할 수 있습니다. 또한 고객은 금융 및 운영 앱에서 Dataverse의 프로젝트 관리자가 확인을 위해 사용할 수 있는 공급업체 송장을 기록할 수 있습니다. | <p>[하도급 계약 관리](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[공급업체 송장 만들기](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| 시간 및 경비 | **전역 승인자**<br>이 기능을 사용하면 프로젝트 또는 프로젝트의 팀 구성원 상태에 관계없이 ISV(독립 소프트웨어 공급업체) 및 중앙 집중식 승인이 가능합니다. | [보안 및 승인](/dynamics365/project-operations/approvals/approvals-security) |
| 경비 관리 | **공급업체 통화로 경비 부채를 전기할 수 있는 기능**<br>이 기능을 사용하면 현금 결제 방법에 대한 공급업체 통화로 경비 보고서를 전기할 수 있습니다. | [공급업체 통화로 경비 부채를 전기할 수 있는 기능](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| 프로젝트 조달 | **공급업체 지불시 결제**<br>이 기능을 사용하면 PWP(지불시 결제) 기능을 Project Operations 비 재고 환경에서 사용할 수 있습니다. 이를 통해 고객으로부터 결제를 받을 때까지 보유 기간에 따라 공급업체 결제를 차단/유보할 수 있습니다. | [공급업체 지불시 결제](/dynamics365/project-operations/procurement/pay-when-paid) |
| 프로젝트 조달 | **프로젝트 구매 요청**<br>이 기능을 사용하면 Dynamics 365 Customer Engagement 통합의 Project Operations가 활성화된 법인에서 프로젝트 관련 구매 주문을 생성할 수 있습니다. 프로젝트 구매 주문을 사용하여 조달 부서 가상 사용자별로 프로젝트에 대해 재고가 없는 자재 조달을 기록할 수 있습니다. 프로젝트 구매 주문은 Dataverse에 동기화되지 않습니다. 그러나 가상 엔터티를 사용하여 프로젝트 관리자 정보에 대한 Dataverse의 프로젝트 구매 주문 라인을 표시할 수 있습니다. 프로젝트 관련 공급업체 송장 비용은 Dataverse의 실제 프로젝트 엔터티와 통합됩니다. 프로젝트 비용은 Project Operations 통합 분개장을 사용하여 프로젝트 보조원장에 기록됩니다. | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 표는 Project Operations 2022년 9월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| 엔터티 맵 | 업데이트된 버전 | 댓글 |
| -------------- | ------------------- | ------------|
| Project Operations 통합 실제(msdyn_actuals) | 1.0.0.15 | 이 맵은 리소스 기반 시나리오에 대한 Project Operations을 통한 하도급 실제 처리를 지원합니다. |
| Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn_projectvendorinvoices) | 1.0.0.2 | 이 맵은 리소스 기반 시나리오에 대한 Project Operations을 통한 하도급 실제 처리를 지원합니다. |
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn_projectvendorinvoicelines) | 1.0.0.5 | 이 맵은 리소스 기반 시나리오에 대한 Project Operations을 통한 하도급 실제 처리를 지원합니다. |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2754422 | 프로젝트가 Dataverse에 복사될 때 재료 및 비용 견적은 재무로 흐르지 않습니다. |
| 시간 및 경비 | 2787409 | 유효하지 않은 승인자는 비프로젝트 시간 입력을 승인할 수 있습니다. |
| 영업 기회 관리 | 2788907 | 플래그가 포함된 주문 라인의 고유성 검증에 대한 오류 메시지가 업데이트되었습니다. |
| 시간 및 경비 | 2842253 | 시간 승인을 위한 Null 예외 처리. |
| 청구 및 가격 책정 | 2844181 | 상관 관계 ID를 가져오지 못하면 송장 생성이 차단됩니다. |
| 청구 및 가격 책정 | 2876628 | QLD, CLD - 추정 가격표 해결은 가격표의 기존 날짜 범위 필드를 사용해야 합니다. |
| 하도급 계약 | 2893222 | 하도급 계약 내용에 대해 역할이 지정되지 않은 경우 모든 역할에 대해 팀 구성원에서 해당 내용을 선택할 수 있어야 합니다. |

### <a name="project-management-and-accounting-in-finance"></a>Finance의 프로젝트 관리 및 회계

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics Lifecycle Services에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559)를 보십시오.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>향후 릴리스에서 기본적으로 켜져 있는 기능

다음 표에는 버전 10.0.30에서 기본적으로 켜져 있는 기능이 나열되어 있습니다. 자동으로 켜진 대부분의 기능은 [기능 관리](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)에서 끌 수 있습니다. 앞으로는 자동으로 켜진 일부 기능이 기능 관리에서 제거되어 필수가 될 수 있습니다. 이 변경 사항은 고객이 현재 기능을 사용하도록 하여 추가된 현재 기능을 기반으로 개선 사항을 구축할 수 있도록 합니다. 기능은 필수라고 판단되지 않는 한 1년 이내에 자동으로 활성화되지 않습니다.

| 기능 이름 | 활성화 날짜 | 기능을 추가한 날짜 | 기능 상태 | 모듈 |
| --- | --- | --- |--- |--- |
| 사용자가 동기화 작업과 비동기 작업 간에 전환해야 할 때 비동기 작업 활성화 | 2022년 10월 21일 | 2021년 4월 9일 | 기본적으로 켜짐 | 경비 관리 |
| 영수증에 대한 경비 정책 평가 필요 | 2022년 10월 21일 | 2021년 12월 20일 | 기본적으로 켜짐 | 경비 관리 |
| 위임 작업자가 작성한 경비 보고서 목록 보기 | 2022년 10월 21일 | 2020년 2월 19일 | 기본적으로 켜짐 | 경비 관리 |
| 회계 연도 기준 총 마일리지 계산 | 2022년 10월 21일 | 2022년 5월 10일 | 기본적으로 켜짐 | 경비 관리 |
