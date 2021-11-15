---
title: 새로운 기능 2021년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 2021년 6월 Project Operations에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6a40335df89cc6b2bb35e54832140aac6eb9ac6
ms.sourcegitcommit: 03414a74ddf1f2d63043d734ebdee7485f1aadd2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679217"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>새로운 기능 2021년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dynamics 365 Dataverse 환경 버전 4.11.0.156 또는 4.11.0.164의 Project Operations.
- Finance and Operations 앱 환경 버전 10.0.19의 프로젝트 관리 및 회계.

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- [조정 시나리오에 대한 프로젝트 송장 제안 라인](../invoicing/correct-project-invoice-proposals.md) 삭제 기능.
- 항목별 경비 라인은 경비 보고서 [경비 보고서 재구상된 새로운 기능](../expense/expense-reports-reimagined.md#new-features)의 하위 범주 이름을 반영합니다.
- 새 경비를 생성할 때 새 경비 창에서 결제 방법을 사용할 수 있습니다.
- 프로젝트 일정 API의 일반 공급. 이 새로운 기능을 통해 고객은 프로젝트 작업, 리소스 할당, 작업 종속성 및 프로젝트 팀 구성원 레코드에 대한 생성, 업데이트 및 삭제 작업을 프로그래밍 방식으로 수행할 수 있습니다. 자세한 내용은 [프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행](../project-management/schedule-api-preview.md)을 참조하십시오.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. 

Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

Project Operations Dataverse 솔루션 및 Finance and Operations 앱 솔루션 버전을 업데이트할 때 환경에서 맵의 최신 버전을 실행하고 모든 관련 테이블 맵을 활성화합니다. 맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다. **버전** 열의 **이중 쓰기** 페이지에서 활성 버전의 맵을 볼 수 있습니다. **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장하여 맵의 새 버전을 활성화합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

지도를 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 [지도에서 테이블 열 누락 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2281417 | 송장 일정을 통한 송장 자동 생성 동작이 실패하는 현상이 수정되었습니다. |
| 청구 및 가격 책정 | 2287835 | 송장 확인 성능이 향상되었습니다. |
| 영업 기회 관리 | 2222555 | 자재 견적 청구 가능성에서 **프로젝트 견적에서 가져오기** 를 사용할 때 견적 라인 상세내역에 올바르게 복사해야 합니다. |
| 영업 기회 관리 | 2223427 | 이제 **GenerateRetainersFromRetainerScheduleOptions** 작업에 대한 사용자 정의가 허용됩니다. |
| 영업 기회 관리 | 2277528 | 여러 고객이 있는 프로젝트 계약 내용에 대한 고정 청구 중요 시점 값 계산. |
| 프로젝트 계획 및 추적 | 2226110 | **프로젝트 팀** 그리드의 **요구사항 생성** 기능과 관련된 간헐적인 문제를 수정했습니다. |
| 프로젝트 계획 및 추적 | 2208109 | 사용자는 다른 통화의 관련 작업과 함께 한 통화로 프로젝트를 생성할 수 없습니다. |
| 프로젝트 계획 및 추적 | 2258228 | 일정 API를 사용하여 **일정** 항목으로 수정할 수 있는 필드 목록이 업데이트되었습니다. |
| 프로젝트 계획 및 추적 | 2293989 | 올바른 언어 및 지역 설정이 **프로젝트 작업** 그리드에 전달되어야 합니다. |
| 리소스 관리 | 2220493 | 리소스 요청을 완료로 빠르게 표시할 때 **작업** 그리드의 사용자 경험을 수정했습니다. |
| 리소스 관리 | 2330496 | **일정 게시판** 로딩 문제가 해결되었습니다. (품질 업데이트는 4.11.0.164 버전에서 사용 가능) |
| 시간 및 경비 | 2194431 | **시간 항목** 그리드는 **시스템 설정** 에 설정된 그 주의 시작을 표시해야 합니다. |
| 시간 및 경비 | 2277311 | **시간 항목** 그리드의 셀에서 값을 삭제한 후에도 커서는 그리드에 남아 있습니다. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **양식 메모** 및 **양식 설정** 은 Project Operations와 통합된 Finance 법인의 **프로젝트 관리 설정** 아래에 표시되지 않습니다. |
| 프로젝트 관리 및 회계 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | 프로젝트 송장 바우처에 대한 **전기 유형** = **판매세** 인 경우 VAT에 대한 기본 설명은 비어 있습니다. |
| 프로젝트 관리 및 회계 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Project Operations 통합과 함께 Dataverse에서 작업 기반 청구가 사용되는 경우 이중 트랜잭션이 게시됩니다. |
| 프로젝트 관리 및 회계 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Project Operations 통합을 사용하는 동안 수익 인식 완료율이 올바르지 않습니다. |
| 프로젝트 관리 및 회계 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Project Operations 통합 시나리오에서 보류 중인 공급업체 송장에 대해 수익 발생이 두 배가 됩니다. |
| 프로젝트 관리 및 회계 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 수익 프로필 규칙이 **그룹** 설정으로 설정된 경우 통합 저널을 게시할 수 없습니다. |
| 프로젝트 관리 및 회계 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 여러 측정 단위가 있는 라인이 있는 프로젝트 구매 발주에 대해서는 구매 송장을 전기할 수 없습니다. |
| 프로젝트 관리 및 회계 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | 프로젝트의 기본 재무 차원은 프로젝트 **V2** 데이터 항목을 사용하여 업데이트할 수 없습니다. |
| 프로젝트 관리 및 회계 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | 프로젝트 견적을 생성하기 위한 일괄 처리 프로세스를 완료하는 데 너무 오래 걸립니다. |
| 프로젝트 관리 및 회계 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 계약을 삭제하면 고객과 연결된 주소도 삭제됩니다. |
| 이동 및 경비 | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 경비 보고서 승인 워크플로 조건이 올바르게 평가되지 않습니다. |
| 이동 및 경비 | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 경비 보고서 정책이 프로젝트 ID를 올바르게 평가하지 않습니다. |
| 이동 및 경비 | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | **본지사 경비 트랜잭션을 위해 개인으로 분할** 작업이 제대로 작동하지 않습니다. |
| 이동 및 경비 | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 특정 출장 요청이 삭제되면 경비 보고서 라인 근거가 실수로 삭제됩니다. 경비 보고서의 recID와 이동 요청서가 동일한 경우에 발생합니다. |
| 이동 및 경비 | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 경비 보고서 정책에 **프로젝트 ID** 필드가 필요한 경우 경비 모바일 앱에 문제가 있습니다. |
| 이동 및 경비 | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | 프로젝트와 연결된 본지사 비용은 편집할 수 없습니다. 대신 "개체 참조가 개체의 인스턴스로 설정되지 않았습니다."라는 오류 메시지가 표시됩니다. |
| 이동 및 경비 | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 경비 보고서가 전기된 후 은행 보조원장에 잘못된 통화와 금액이 나열됩니다. |
| 이동 및 경비 | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | *신용카드 트랜잭션 삭제* 기능이 개선되었습니다.  |
| 이동 및 경비 | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 경비 보고서에 포함된 판매세는 법인에서 다른 보고 통화가 지정된 경우 일관되게 계산되지 않습니다. |
| 이동 및 경비 | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 새로운 현금 여행 경비를 추가하면 성능이 영향을 받습니다. |
| 이동 및 경비 | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 경비 정책 규칙은 경비 보고서에서 트리거되지 않습니다. |
| 이동 및 경비 | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | 데이터 관리 프레임워크를 사용하여 새 공유 범주를 업로드하면 모든 공유 범주에 대한 모든 하위 범주가 제거됩니다. |
| 이동 및 경비 | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 경비 라인을 생성한 다음 범주를 선택하면 "판매세 그룹 DOM과 품목 판매세 그룹 STD의 조합이 유효하지 않습니다."라는 오류 메시지가 표시됩니다. |
| 이동 및 경비 | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 경비 모바일 애플리케이션에 동기화 문제가 있습니다. |
