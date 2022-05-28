---
title: 2021년 4월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 4월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 07622ed798fd8d70e0ce5cc42297bd5056402474
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589112"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 4월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dataverse 환경 버전 4.9.0.221의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.17의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- 프로젝트를 위한 비 재고 재료. 주요 기능은 다음과 같습니다.
  - 프로젝트 판매 주기 동안 비재고 재료를 추정하고 가격을 책정합니다. 자세한 내용은 [카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md)를 참조하십시오.
  - 프로젝트를 제공하는 동안 비재고 재료의 사용을 추적합니다. 자세한 내용은 [프로젝트 및 프로젝트 작업에 대한 재료 사용량 기록](../material/material-usage-log.md)을 참조하십시오.
  - 송장은 비재고 재료 비용을 사용했습니다. 자세한 내용은 [청구 백로그 관리](../proforma-invoicing/manage-billing-backlog.md)를 참조하십시오.
  - 이 기능을 구성하는 방법에 대한 자세한 내용은 [비 재고 재료 및 보류 중인 공급업체 송장 구성](../procurement/configure-materials-nonstocked.md)을 참조하십시오.
- 작업 기반 청구: 프로젝트 작업을 프로젝트 계약 내용과 연관시키는 기능이 추가되어 계약 내용에 있는 것과 동일한 청구 방법, 송장 빈도 및 고객이 적용됩니다. 이 연결은 프로젝트 작업에 대한 이 설정에 따라 작동하도록 정확한 송장 발행, 회계, 수익 추정 및 인식을 보장합니다.
- Dynamics 365 Dataverse의 의 새로운 API를 사용하면 **일정 엔터티** 로 작업을 생성, 업데이트 및 삭제할 수 있습니다. 자세한 내용은 [일정 엔터티로 일정 API를 사용하여 작업 수행](../project-management/schedule-api-preview.md)을 참조하십시오.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 목록은 Project Operations 2021년 4월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| **엔터티 맵** | **업데이트된 버전** | **댓글** |
| --- | --- | --- |
| Project Operations 통합 실제(msdyn\_actuals) | 1.0.0.14 | 재료 프로젝트 실제 데이터를 동기화하도록 맵이 수정되었습니다. |
| 경비 추정용 Project Operations 통합 엔터티(msdyn\_estimateslines) | 1.0.0.2 | 작업 기반 청구 지원을 위해 금융 및 운영 앱에 프로젝트 계약 내용 동기화를 추가했습니다. |
| 시간 추정용 Project Operations 통합 엔터티(msdyn\_resourceassignments) | 1.0.0.5 | 작업 기반 청구 지원을 위해 금융 및 운영 앱에 프로젝트 계약 내용 동기화를 추가했습니다. |
| 재료 추정을 위한 Project Operations 통합 테이블(msdyn\_estimatelines) | 1.0.0.0 | Dataverse에서 금융 및 운영 앱으로 자재 견적을 동기화하는 새로운 테이블 맵. |
| Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn\_projectvendorinvoices) | 1.0.0.0 | 금융 및 운영 앱의 공급업체 송장 헤더를 Dataverse로 동기화하는 새로운 테이블 맵입니다. |
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn\_projectvendorinvoicelines) | 1.0.0.0 | 금융 및 운영 앱의 공급업체 송장 라인을 Dataverse로 동기화하는 새로운 테이블 맵입니다. |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance and Operations 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화해야 합니다. 맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장하여 새 버전의 맵을 활성화할 수 있습니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작할 때 문제가 발생하면 이중 쓰기 문제 해결 가이드의 [맵에서 표 열 누락 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-in-dynamics-365-dataverse"></a>Dynamics 365 Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2124532 | 보유자 금액 또는 적용된 보유자 금액이 원래 송장에 있는 경우 **송장 수정** 버튼이 견적 송장에 표시됩니다. 이 버튼은 Finance 버전 10.0.19 이상의 환경에서만 표시됩니다. |
| 청구 및 가격 책정 | 2224568 | 송장 확인 플러그인을 호출하는 것과 관련된 사용자 지정을 활성화하는 논리가 추가되었습니다. |
| 청구 및 가격 책정 | 2101098 | 견적 송장에 대한 기본 필드의 논리가 개선되었습니다. **청구지 주소**, **청구지 이름** 및 **결제 조건** 이 이제 해당 프로젝트 계약 고객 레코드에서 기본값으로 설정됩니다. |
| 청구 및 가격 책정 | 2021413 | 작업에서 미청구 및 청구 경비의 판매 값을 포함하도록 **작업** 엔터티에서 **실제 비용** 과 **판매** 필드가 업데이트되었습니다. |
| 청구 및 가격 책정 | 2182110 | 프로젝트 계약을 복사할 때 계약 항목 ID가 대상 프로젝트 계약에서 다시 생성되어 고유한지 확인합니다. |
| 영업 기회 관리 | 2186741 | **원본** 필드 및 **트랜잭션 유형** 이 기존 견적 항목 세부 정보에서 업데이트될 수 없도록 유효성 검사를 추가했습니다. |
| 영업 기회 관리 | 2191353 | 이정표는 시간 및 재료 계약 내용에 생성되어서는 안됩니다. |
| 영업 기회 관리 | 2216956 | **가격 업데이트** 문제가 해결되었습니다. |
| 계획 및 추적 | 2182979 | 경비 추정 라인이 원래 프로젝트에서 복사되도록 프로젝트 복사 기능이 개선되었습니다. |
| 계획 및 추적 | 2184144 | 리소스 위치 이름이 원래 프로젝트에서 복사되도록 프로젝트 복사 기능이 개선되었습니다. |
| 계획 및 추적 | 2184799 | 프로젝트 복사: 복사가 진행되는 동안 예상 시작 날짜를 변경할 수 없도록 제어가 강화되었습니다. |
| 계획 및 추적 | 2185134 | 프로젝트 복사: 대상 프로젝트 예상 시작일이 오늘 날짜로 설정됩니다. |
| 계획 및 추적 | 2196373 | 프로젝트 복사: 프로젝트 관리자 및 팀 구성원 레코드가 프로젝트 팀에서 중복되지 않도록 합니다. |
| 계획 및 추적 | 2211833 | 프로젝트 복사: 리소스 할당이 소스 프로젝트 작업에서 대상 프로젝트로 복사됩니다. |
| 계획 및 추적 | 2186541 | 리소스별로 그룹화할 때 **추정** 그리드의 문제가 해결되었습니다. |
| 계획 및 추적 | 2166906 | 작업의 트랜잭션 범주를 **리소스 할당** 엔터티로 복사해야 합니다. |
| 리소스 관리 | 2125362 | 시간 기반 할당 방법을 사용하여 일반 팀 구성원을 만들 때 발생하는 문제를 해결했습니다. |
| 시간 및 경비 | 2113603 | **시간 입력** 페이지에서 특성 제거와 관련된 사용자 지정 관련 문제를 해결했습니다. 이제 시스템은 스크립트를 사용하여 특성에 액세스하기 전에 페이지에 특성이 있는지 확인합니다. |
| 시간 및 경비 | 2204377 | 시간 입력 중 **주 복사** 를 선택하면 복사된 작업표가 자동으로 표시되어야 합니다. |
| 시간 및 경비 | 2209059 | Dynamics 365 Field Service 시간 항목에 대한 **상태** 필드를 편집할 수 있습니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | **주기적** 섹션에서 역 추정 제거가 작동하지 않습니다.  |
| 프로젝트 관리 및 회계 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **회계 조정** 기능은 **수동 입력 허용 안함** 이 선택된 원장 계정에 문제가 일으킵니다. |
| 프로젝트 관리 및 회계 | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | 보유자 금액 또는 적용된 보유자 금액을 포함한 수정 송장을 처리하는 비즈니스 논리가 추가되었습니다. |
| 프로젝트 관리 및 회계 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - 회사 간 프로젝트 송장 발행의 판매 가치 전기가 예상치 못한 계정을 선택함. |
| 프로젝트 관리 및 회계 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations에서 보유자와 함께 작업할 때 선급금이 청구된 후 계약의 기본 프로젝트를 변경하면 차감에 문제가 발생합니다. |
| 프로젝트 관리 및 회계 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations에서 계약에서 프로젝트를 제거하면 필요한 경우 계약의 기본 프로젝트가 재설정되어야 합니다. |
| 프로젝트 관리 및 회계 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations에서 회사 간 송장의 **라인 추가** 목록에 잘못된 비용 라인이 표시됩니다. |
| 프로젝트 관리 및 회계 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations에서 **구매 계약** 페이지는 Project Operations와 통합된 금융 법인에 표시되지 않습니다. |
| 프로젝트 관리 및 회계 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse 통합 오류로 인해 Project Operations에서 견적을 성공으로 변환할 수 없습니다. |
| 프로젝트 관리 및 회계 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 는 다른 고객의 자금 출처 송장 주소를 설정할 수 있습니다.  |
| 프로젝트 관리 및 회계 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Project Operations에서는 트랜잭션에 대한 전기 송장을 생성할 때 차원이 선택되지 않습니다. |
| 이동 및 경비 | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 현금 서비스 잔액이 승인되고 행별로 게시된 경우 경비 보고서에 대해 업데이트되지 않습니다. |
| 이동 및 경비 | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | 항목별 회사 간 경비 보고서에 대한 세금이 올바르게 계산되지 않습니다. |
| 이동 및 경비 | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | 프로젝트와 관련된 추가 필드가 재구성된 **회사간 경비 보고서** 페이지에 표시됩니다. |
| 이동 및 경비 | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | 경비 보고서의 헤더 영수증에 잘못된 오류 메시지가 발생합니다. |
| 이동 및 경비 | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | 판매세가 대상 법인에 전기되는 경우 본지사 시나리오에서 경비 보고서가 잘못 전기됩니다. |
| 이동 및 경비 | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | 보고서 제출 날짜는 승인된 경비 보고서에 인쇄되지 않습니다. |
| 이동 및 경비 | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | **승인된 날짜** 및 **거부된 날짜** 비용이 승인된 후에는 필드가 채워지지 않습니다. |
| 이동 및 경비 | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | 한 근로자에 대해 생성된 출장 요청을 다른 근로자의 경비 보고서에 사용할 수 있습니다. |
| 이동 및 경비 | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 새 경비 라인을 추가할 때 경비 범주가 잠깁니다. |
| 이동 및 경비 | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 이미 분할 된 경비 보고서 라인을 항목화하면 **TRVEXPTRANS.SOURCEDOCUMENTLINE** 이 중복되므로 AP\총계정 원장 전표가 불완전하게 전기되고 회계 소스 탐색기가 중단됩니다. |
| 이동 및 경비 | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | 여행 요청 정책이 예상대로 작동하지 않습니다. |
| 이동 및 경비 | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | 경비 보고서를 위해 게시된 프로젝트 트랜잭션에 공급업체 계정 이름이 표시되지 않습니다. |
| 이동 및 경비 | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations에서 회사 간 프로젝트에 대한 작업으로 시간을 승인할 수 없습니다. |
| 이동 및 경비 | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | 현금 서비스 반환 범주는 전기될 때 현금 서비스 잔액을 업데이트하지 않습니다. |
| 이동 및 경비 | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | 수입 신용 카드 트랜잭션을 사용하여 외화로 생성되고 프로젝트와 연결된 경비 보고서에서 판매 가격이 잘못 계산됩니다. |
| 이동 및 경비 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** 데이터 엔터티 및 관련 고유 인덱스를 롤백했습니다. |
| 이동 및 경비 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | **SOURCEDOCUMENTLINE** 세대에 계측을 추가했습니다. |
| 이동 및 경비 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 판매세가 대상 법인에 전기되는 경우 본지사 시나리오에 잘못된 보조 원장 분개가 표시됩니다. |
| 이동 및 경비 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations에서 지출 추정치는 재무에서 삭제될 때 Dataverse에서 삭제되지 않습니다. |
| 이동 및 경비 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 경비 범주가 비 프로젝트 범주인 경우 **경비** 페이지에 선택된 재무 차원은 경비 보고서에 복사되지 않습니다. |
