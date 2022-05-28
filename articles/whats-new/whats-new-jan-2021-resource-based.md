---
title: 2021년 1월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 1월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 50874d771afe03b08bd95b670f7095bc2d61509d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599554"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 1월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_


이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

  - Dataverse 환경 버전 4.6.0.154의 Project Operations
  - Dynamics 365 Finance 환경 버전 10.0.16의 프로젝트 관리 및 회계

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| **배포 및 구성** | 2106818 | 페이지 사용자 지정과 관련된 문제를 일으키는 웹 리소스 이름 변경을 수정했습니다. |
| **청구 및 가격 책정** | 2091908 | Project Operations가 Dynamics 365 Field Service와 함께 설치될 때 **송장** 페이지에서 **가격 산정 잠금** 및 **현재 가격 산정 사용** 옵션의 가시성을 수정했습니다. |
| **청구 및 가격 책정** | 2103058 | 작업의 실제 비용에 대한 null 값을 처리하도록 **프로젝트 합계** 를 새로 고쳤습니다. |
| **청구 및 가격 책정** | 2116100 | **실제에 대한 정확한 입력** 기능과 함께 사용되는 오류 메시지를 개선했습니다. |
| **청구 및 가격 책정** | 2116129 | **프로젝트** 페이지의 **추정** 탭에서 경비 추정 가시성이 향상되었습니다. |
| **청구 및 가격 책정** | 2119112 | 다른 환율이 사용될 때 실제 판매 및 실제 비용의 집계가 수정되었습니다. |
| **청구 및 가격 책정** | 2134705 | **송장** 페이지가 열리고 Field Service가 설치될 때 "정의되지 않은 **getResourceString** 속성을 읽을 수 없습니다" 오류가 수정되었습니다. |
| **영업 기회 관리** | 2022195 | **프로젝트** 페이지의 작업 기반 청구 그리드에는 해당 작업에 연결된 계약 또는 견적 라인이 있음을 나타내는 아이콘이 있습니다. |
| **영업 기회 관리** | 2029135 | 사용자가 선불금이 송장 청구된 확인된 송장에서 송장 라인을 열려고 할 때 발생하는 비즈니스 프로세스 오류가 수정되었습니다. |
| **영업 기회 관리** | 2040713 | 계약에서 송장을 생성하고 Field Service가 설치된 경우 발생하는 스크립트 오류가 수정되었습니다. |
| **프로젝트 계획 및 추적** | 2090202 | 더 이상 사용되지 않는 비즈니스 규칙을 **더 이상 사용되지 않음** 으로 표시했습니다. |
| **시간 및 경비** | 2091249 | 사용자가 제출되거나 승인된 시간 항목에 대한 작업을 변경할 수 없도록 제어가 강화되었습니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| **프로젝트 관리 및 회계** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 여러 자금 출처가 있는 고정 가격 프로젝트의 **계정** 페이지에 잘못된 계약 금액이 있습니다. |
| **프로젝트 관리 및 회계** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** 자리 표시자가 워크플로 **프로젝트 송장 제안서 검토** 의 프로젝트 ID를 표시하지 않습니다. |
| **프로젝트 관리 및 회계** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | 프로젝트 송장 제안서를 전기할 때 잘못된 현금 할인 날짜가 사용됩니다. |
| **프로젝트 관리 및 회계** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Project Operations에서 리소스 할당을 제거하고 읽으면 Finance에서 프로젝트 예측 항목이 두 배로 늘어납니다. |
| **프로젝트 관리 및 회계** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Project Operations에서는 프로젝트에 계약 내용이 없으면 Dataverse에서 프로젝트 추정을 생성할 수 없습니다. |
| **프로젝트 관리 및 회계** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | 프로젝트 경비 트랜잭션의 재무 차원은 비용이 잔액에 전기될 때 관련 바우처 및 경비 보고서의 회계 분포와 동기화되지 않습니다. |
| **프로젝트 관리 및 회계** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 고정 가격 프로젝트에 대해 게시된 프로젝트 트랜잭션의 **송장 상태** 필터가 작동하지 않습니다. |
| **프로젝트 관리 및 회계** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | **주기적** 섹션에서 역 추정 제거가 작동하지 않습니다. |
| **프로젝트 관리 및 회계** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | 송장 제안서 라인은 Dataverse와 통합될 때 Project Operations에서 삭제할 수 있습니다. |
| **프로젝트 관리 및 회계** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Dataverse 통합 없이 여러 계약 내용 기능 활성화를 방지합니다. |
| **프로젝트 관리 및 회계** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | 계정 송장 발행이 손익과 같을 때 송장 발행 수익은 추정 페이지에서 0으로 나열됩니다. |
| **프로젝트 관리 및 회계** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | 통합 환경에서는 송장 수정이 작동하지 않습니다. |
| **프로젝트 관리 및 회계** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 회사 간 프로젝트 송장 발행에 WIP - 판매 금액을 전기할 때 잘못된 계정이 선택됩니다. |
| **프로젝트 관리 및 회계** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Project Operations의 Dataverse에서 추정 작업에 대한 종속성을 업데이트할 수 없습니다. |
| **프로젝트 관리 및 회계** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Finance에서 Project Operations 통합 분개장을 반복적으로 삭제하면 데이터가 손실됩니다. |
| **프로젝트 관리 및 회계** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 프로젝트 송장 제안서를 전기할 때 다음 오류가 발생합니다. "공제된 선불 송장이 추가되면 트랜잭션이 보고 통화로 균형을 맞출 수 없습니다." |
| **프로젝트 관리 및 회계** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations에서 기본 프로젝트 계약이 업데이트된 후 잘못된 프로젝트 ID가 공제에 포함됩니다. |
| **프로젝트 관리 및 회계** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Project Operations가 활성화된 경우 견적 및 수익 인식을 완료할 수 없습니다. |
| **프로젝트 관리 및 회계** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations에서는 계약에서 프로젝트를 제거해도 계약의 기본 프로젝트가 재설정되지 않습니다. |
| **프로젝트 관리 및 회계** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations에서 회사 간 송장에서 잘못된 경비 라인이 **줄 추가** 목록에 표시됩니다. |
| **이동 및 경비** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | 계약 내용에 시간 설정이 누락되어 경비 라인을 전기할 수 없습니다. |
| **이동 및 경비** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | 프로젝트/범주 유효성 검사가 필수인 경우 프로젝트와 관련된 경비 범주가 경비 보고서에 표시되지 않습니다. |
| **이동 및 경비** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 경비 보고서가 라인별로 전기될 때 현금 서비스 잔액이 업데이트되지 않습니다. |
| **이동 및 경비** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | 결제 트랜잭션이 둘 이상인 송장이 정산된 경우 정산을 취소한 후 **결제 정보 업데이트** 작업이 실패합니다. |
| **이동 및 경비** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | 일비 경비 범주에 대한 마지막 날 식사 감소 계산에 문제가 있습니다. |
| **이동 및 경비** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | 사용자의 첫 번째 연결이 es-MX 언어인 경우 **직원당 경비 유형** 보고서에 항목별 경비가 표시되지 않습니다. |
| **이동 및 경비** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | 경비 보고서 송장에 대한 공급업체 결제가 정산 전기에 잘못된 요약 계정을 사용하고 있습니다. |
| **이동 및 경비** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | **상쇄 지급 계정을 기준으로 거래 그룹화 허용** 및 **전기시 회계 날짜 수정** 이 활성화된 상태로 경비 보고서가 게시되면 회계 날짜가 **회계 분배 테이블** 에 그룹화되지 않았으며 이는 판매세 기록에 영향을 미칩니다. |
| **이동 및 경비** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | 경비에 사용 확인란을 선택 취소한 다음 다시 선택하면 경비 하위 범주 매핑이 제거됩니다. |
| **이동 및 경비** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | 프로젝트 ID가 헤더 수준에 추가된 경우 회사 간 경비 보고서를 생성할 수 없습니다. |
| **이동 및 경비** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | 경비 금액이 현금 서비스 금액보다 많을 때 경비 지급에 문제가 있습니다. |
| **이동 및 경비** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | 사용자 역할이 특정 조직에 할당된 경우 회사 간 경비 보고서의 **프로젝트 ID** 필드가 비어 있습니다. |
| **이동 및 경비** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 새 경비 라인을 추가하면 경비 범주가 잠깁니다. |
| **이동 및 경비** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 이미 분할된 경비 보고서 라인을 항목화하면 미지급금\총계정 원장 바우처가 불완전하게 전기됩니다. **TRVEXPTRANS.SOURCEDOCUMENTLINE** 의 중복으로 인해 회계 소스 탐색기도 손상됩니다. |
| **이동 및 경비** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | 고객에게 중복된 테이블이 있는 **TRVREQUISITIONLINE** 테이블에 추가된 색인이 업그레이드 중에 오류가 발생합니다. |
| **이동 및 경비** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations의 Dataverse에서 회사 간 작업이 있는 시간을 만들거나 승인할 수 없습니다. |

## <a name="regulatory-updates"></a>규제 업데이트

금융 및 운영 앱의 규정 업데이트에 대한 자세한 내용은 [규정 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 볼 수도 있습니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]