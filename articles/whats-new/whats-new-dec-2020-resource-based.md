---
title: 2020년 12월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2020년 12월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3889402ab991e307bc3fe5463098dfab383a53b4
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727888"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020년 12월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dataverse 환경 버전 4.5.0.134의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.15의 프로젝트 관리 및 회계

이 릴리스로 업데이트하는 방법에 대한 정보는 [재무 환경에서 Project Operations 업데이트](ur5-nonstocked-installation.md)를 참조하십시오

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능
이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

  - [회사 간 송장](../project-accounting/intercompany-invoicing-overview.md) 
  - [고객 선불금 및 보유자](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>리소스/비 재고 기반 시나리오에 대한 Project Operations로 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역                    | 참조 번호 | 품질 업데이트                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 청구 및 가격 책정             | 1986009          | 프로젝트가 계약 내용에 연결되거나 연결 해제되기 전에 확인된 경우 수동으로 생성된 분개장 항목의 성과가 일치하지 않습니다.                     |
| 청구 및 가격 책정             | 2028174          | 송장 라인 상세 내역에 대한 업데이트는 수정 분개장 로직을 따라야 합니다.                                                                                  |
| 청구 및 가격 책정             | 2028315          | 편집 가능한 중첩 그리드 동작 수정                                                                                                                        |
| 청구 및 가격 책정             | 2031070          | 수정 송장 라인 세부 사항 조정은 수정 분개장 로직을 따라야 합니다.                                                                              |
| 청구 및 가격 책정             | 2034186          | 계약 내용에서 프로젝트를 업데이트할 수 있어야 합니다.                                                                                                        |
| 청구 및 가격 책정             | 2034206          | 계약 내용에서 프로젝트 연결을 해제하는 동안 조정 상태는 실제 취소 중에 설정되어야 합니다.                                                        |
| 청구 및 가격 책정             | 2040871          | 비용 추정 그리드에서 단위 및 단위 그룹 셀 업데이트 허용                                                                                       |
| 청구 및 가격 책정             | 2053754          | 송장 편집에서 생성된 실제는 조정 상태 및 청구 상태로 표시되지 않습니다.                                                                |
| 청구 및 가격 책정             | 2057874          | 송장 라인 상세 편집 중에 생성된 올바른 트랜잭션 연결                                                                                     |
| 청구 및 가격 책정             | 2057875          | 송장 라인 상세 편집 중에 생성된 올바른 트랜잭션 원본                                                                                        |
| 청구 및 가격 책정           | 2057944          | 송장 수정에서 송장을 발행할 준비가 되지 않은 실제 항목에 대해 커밋됨으로 설정된 초과하지 않음 상태                                             |
| 청구 및 가격 책정           | 2066169          | 이중 쓰기를 사용하여 통합할 때 청구되지 않은 음수 판매 기록에 대한 회계 날짜 업데이트                                                            |
| 청구 및 가격 책정           | 2067622          | 중요 시점을 생성하는 동안 처리 아이콘이 표시되어야 함                                                                                                |
| 청구 및 가격 책정           | 2067624          | 중요 시점을 생성할 때 계약 금액을 비즈니스 권장으로 표시해야 함                                                                      |
| 청구 및 가격 책정           | 2086880          | 프로젝트 기반 견적 라인용 리본의 **제안** 단추 숨기기                                                                                                |
| 청구 및 가격 책정           | 2098140          | 통합 환경을 위한 **올바른 송장** 단추 표시                                                                                             |
| 배포 및 구성  | 2101152          | Power Platform 관리 센터에서 Project Operations 템플릿을 사용하여 만든 새 환경은 모든 설치 후 작업이 수행되어야 함               |
| 영업 기회 관리        | 2086601          | 비활성화된 역할 및 범주는 견적 라인 및 계약 내용의 청구 가능 역할 및 청구 가능 범주 목록에 복사하면 안됨 |
| 프로젝트 계획 및 추적 | 1949065          | 데이터 가시성은 200% 확대시 올바르게 작동                                                                                                                   |
| 프로젝트 계획 및 추적 | 2046317          | Project Operations에서 프로젝트 엔터티의 이름을 바꾸는 기능                                                                                   |
| 프로젝트 계획 및 추적 | 2057171          | **프로젝트** 페이지에서 **프로젝트 시작 날짜** 필드가 비어 있을 때 오류 메시지 업데이트됨                                                           |
| 프로젝트 계획 및 추적 | 2057197          | 작업 참조가 포함된 예상 라인 복사는 지원되지 않음                                                                                                     |
| 프로젝트 계획 및 추적 | 2060687          | 이제 특정 기간이 지나면 시간대 경고가 사라짐                                                                                                      |
| 리소스 관리           | 1832887          | Dataverse 및 Finance 환경에 대해 반복 가능한 데이터 로드를 보장하려면 기본 리소스 범주 ID가 정적이어야 함                                                 |
| 시간 및 경비              | 2081793          | **경비 범주 이름** 은 Finance and Operations 앱의 **경비 범주 설명** 필드에 매핑되어야 함                                                  |
| 시간 및 경비              | 2034882          | Dynamics 365 Field Service가 설치되면 **새로 만들기** 단추가 시간 항목에 대해 명령 모음에 두 번 표시됨                                          |
| 시간 및 경비              | 2056028          | 타임 라인을 포함하도록 **시간 편집** 페이지 업데이트                                                                                                              |
| 시간 및 경비              | 1983747          | 추가 데이터를 보여주는 시간 항목 차트                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계 개요

| 기능 영역                        | 참조 번호 | 품질 업데이트                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 프로젝트 관리 및 회계 | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | 품목 요구 사항 반품에 대해 보류된 조정                                                                                                                                                                                                        |
| 프로젝트 관리 및 회계 | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | 서식이 지정된 프로젝트 송장에 나타나지 않는 양식 메모                                                                                                                                                                                                          |
| 프로젝트 관리 및 회계 | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | 프로젝트 송장에 대한 MEXICO CFDI 33은 송장 제안에서 결제 방법을 업데이트할 수 없음                                                                                                                                                           |
| 프로젝트 관리 및 회계 | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | 회계 날짜를 개설 기간으로 자동 설정하는 매개 변수는 **통합** 분개장에 적용되지 않음                                                                                                                                                             |
| 프로젝트 관리 및 회계 | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | 예측 메뉴 항목을 **프로젝트** 목록 페이지에서 볼 수 없음                                                                                                                                                                                                      |
| 프로젝트 관리 및 회계 | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **프로젝트 명세서** > **트랜잭션 및 예측** 을 열 수 없음                                                                                                                                                                                                      |
| 프로젝트 관리 및 회계 | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 리소스 할당을 제거하고 읽으면 Finance에서 프로젝트 예측 항목이 두 배가 됨                                                                                                                                                                   |
| 프로젝트 관리 및 회계 | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | 프로젝트에 계약 내용없이 Dataverse에서 프로젝트 견적을 생성할 수 없음                                                                                                                                                                 |
| 프로젝트 관리 및 회계 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 회사 통화와 트랜잭션 통화가 다른 경우 바우처 불균형 오류로 인해 제거가 실패함                                                                                                                                            |
| 프로젝트 관리 및 회계 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | 고정 가격 프로젝트에 대해 게시된 프로젝트 트랜잭션의 송장 상태에 대한 필터가 작동하지 않음                                                                                                                                                            |
| 프로젝트 관리 및 회계 | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Dataverse에서 작업의 시작 날짜를 업데이트할 수 없음                                                                                                                                                                                                                    |
| 프로젝트 관리 및 회계 | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Project Operations 통합 시나리오에서 송장 제안 라인 삭제 가능                                                                                                                                                                                    |
| 프로젝트 관리 및 회계 | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Project Operations 통합 시나리오에서 송장 제안 라인 삭제 가능                                                                                                                                                                                    |
| 프로젝트 관리 및 회계 | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Dataverse 통합 없이 여러 계약 내용 기능 활성화 방지                                                                                                                                                                                        |
| 프로젝트 관리 및 회계 | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | 계정 송장 = 이익 및 손실일 때 화면 송장 수익이 영(0)이라고 추정                                                                                                                                                                          |
| 프로젝트 관리 및 회계 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | WIP - 회사 간 프로젝트 송장 발행의 판매 가치 전기가 예상치 못한 계정을 선택함                                                                                                                                                                           |
| 프로젝트 관리 및 회계 | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | Project Operations가 활성화된 상태에서 추정/수익 인식을 수행할 수 없음                                                                                                                                                                         |
| 이동 및 경비                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | 대리인이 입력한 비용은 대리인이 아닌 비용 사용자에게 반환됨                                                                                                                                                                                           |
| 이동 및 경비                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | 워크플로를 제출하는 경비 보고서 워크플로 대리인 사용자가 워크플로 작성자로 식별되지 않음                                                                                                                                                             |
| 이동 및 경비                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | 법인 재정의의 기본 차원이 회사 간 경비 보고서에서 작동하지 않음                                                                                                                                                                    |
| 이동 및 경비                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | 일비 경비 범주에 대한 마지막 날 식사 감소 계산 문제                                                                                                                                                                                    |
| 이동 및 경비                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | 여행 요청에 연결된 경비 보고서에서 경비 라인 항목이 삭제된 후 **여행 요청** 페이지의 **조정할 금액** 필드가 업데이트되지 않음                                                                                                       |
| 이동 및 경비                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | 경비 보고서는 워크플로에 제출한 후 정책을 검증했음                                                                                                                                                                                           |
| 이동 및 경비                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | 항목 대리인에 대한 여행 경비 영수증이 올바르게 표시되지 않음                                                                                                                                                                                            |
| 이동 및 경비                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | 사용자 언어가 es-MX로 설정된 경우 직원당 경비 유형에 항목별 비용이 표시되지 않음                                                                                                                         |
| 이동 및 경비                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | 경비 보고서를 사용하면 경비 범주에 대해 잘못된 하위 범주를 입력할 수 있음                                                                                                                                                                                       |
| 이동 및 경비                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | 경비 보고서 금액이 현금 서비스 금액보다 많은 경우 경비 보고서와의 현금 서비스 조정이 예상대로 작동하지 않음                                                                                                           |
| 이동 및 경비                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | ProjProjectLookup과 관련된 쿼리의 성능 문제. 쿼리를 실행하는 데 시간이 오래 걸리므로 고객이 차단됩니다.                                                                                                                     |
| 이동 및 경비                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | **상쇄 지급 계정을 기준으로 거래 그룹화 허용** 및 **전기시 회계 날짜 수정** 이 설정된 상태로 게시된 경비 보고서는 회계 날짜가 **회계 분배 테이블** 에 그룹화되지 않았으며 이는 판매세 기록에 영향을 미칩니다. |
| 이동 및 경비                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | 외화로 가져온 신용 카드 트랜잭션은 경비 보고서 라인에서 **요금 VAT 취소** 가 사용되는 경우 잘못된 공급업체 트랜잭션을 생성합니다.                                                                                                                     |
| 이동 및 경비                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | 프로젝트 ID가 헤더 수준에 추가된 경우 회사 간 경비 보고서를 생성할 수 없음                                                                                                                                                                 |
| 이동 및 경비                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | 경비 금액이 현금 서비스 금액보다 많을 때 경비 지급 문제                                                                                                                                                                          |
| 이동 및 경비                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | 사용자 역할이 특정 조직에 할당된 경우 회사 간 경비 보고서의 프로젝트 ID 정보가 비어 있음                                                                                                                                           |
| 이동 및 경비                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | 경비 보고서 자동 전기 워크플로우가 완료되었지만 송장이 전기되지 않음                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>규제 업데이트
Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]