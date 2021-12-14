---
title: 2021년 11월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 11월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827334"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 11월 새로운 내용 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.26.0.145, 4.26.0.148 또는 4.26.0.150의 Project Operations.
- Dynamics 365 Finance 환경 버전 10.0.22의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- 프로젝트 일정 API(응용 프로그래밍 인터페이스)는 이제 프로젝트 버킷 생성 및 삭제 기능을 지원합니다.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](/dynamics365/project-operations/environment/resource-dual-write-maps)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-in-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2240080 | **지불 조건** 필드는 견적 송장에서 중복되지 않아야 합니다. |
| 청구 및 가격 책정 | 2358236 | 송장 수정은 영(0) 가격 라인이 있는 수정을 허용해야 합니다. |
| 리소스 관리 | 2410072 | 프로젝트 관리자로 작업에 할당된 리소스 설정을 허용합니다. |
| 청구 및 가격 책정 | 2430234 | 비용 성과 계산 문제를 해결합니다. |
| 시간 및 경비 | 2436978 | 시간을 hh:mm 형식으로 입력할 수 있습니다. |
| 청구 및 가격 책정 | 2448623 | 가격표가 조직 구성 단위와 연결된 후 업데이트되도록 허용합니다. |
| 시간 및 경비 | 2460396 | 셀을 지워서 시간 항목을 삭제할 수 있습니다. |
| 청구 및 가격 책정 | 2467386 | 작업이 낙찰된 견적과 연결된 경우에도 작업이 있는 프로젝트를 삭제할 수 있습니다. |
| 시간 및 경비 | 2461744 | **내 승인 실패** 보기에는 **제출됨** 스테이지의 프로젝트 승인만 포함됩니다. |
| 시간 및 경비 | 2464082 | 대상 상태가 일치하면 프로젝트 승인에서 승인 집합으로의 링크를 제거합니다. |
| 시간 및 경비 | 2468108 | 일정 작업은 승인 집합에 대한 **처리 중** 상태를 설정해서는 안 됩니다. |
| 시간 및 경비 | 2471503 | 7일이 지난 승인 집합을 삭제합니다. |
| 청구 및 가격 책정 | 2480687 | 견적 라인 이정표가 생성될 때 견적 라인 참조를 제거하면 안 됩니다. |

### <a name="project-management-and-accounting-in-finance"></a>Finance의 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 프로젝트 경비 트랜잭션에서 유지된 공급업체 금액은 트랜잭션 목록에 표시되지 않습니다. |
| 프로젝트 관리 및 회계 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 공급업체 송장 통합이 켜져 있으면 회사 간 공급업체 송상이 손상됩니다. |
| 프로젝트 관리 및 회계 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 프로젝트 송장의 지불 조건이 예상대로 작동하지 않습니다. |
| 프로젝트 관리 및 회계 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 공급업체 보유가 해제되면 전표 전기에 잘못된 추가 행이 있습니다. |
| 프로젝트 관리 및 회계 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations 통합 저널이 게시될 때 게시되지 않는 계정에 대한 차원이 누락되어 실패합니다. |
| 프로젝트 관리 및 회계 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 조달 범주가 항목에 할당된 경우 보류 중인 공급업체 송장에서 **프로젝트** 탭을 편집할 수 없습니다. |
| 프로젝트 관리 및 회계 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse에 로그인하지 않은 경우 탐색 창이 없습니다. |
| 프로젝트 관리 및 회계 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 적용된 유지 사례의 프로젝트 송장에서 수익을 전기할 때 바우처의 트랜잭션이 균형을 이루지 않기 때문에 문제가 발생합니다. |
| 프로젝트 관리 및 회계 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 송장 제안을 게시한 후 견적을 생성하면 수정 라인 가져오기가 차단됩니다. |
| 프로젝트 관리 및 회계 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 완전히 청구된 마일스톤 레코드의 수정은 불가능해야 합니다. |
| 이동 및 경비 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 모든 경비 보고서는 경비 모바일 앱에서 범주를 검색할 때 볼 수 있습니다. |
| 이동 및 경비 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 신용 카드 트랜잭션에서 생성된 비용으로 전기된 공급업체 트랜잭션 및 판매세 거래 금액이 올바르지 않습니다. |
| 이동 및 경비 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | **경비 보고서** 페이지를 새로 고칠 때 관련 없는 경고가 발생합니다. |
| 이동 및 경비 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 임시 승인자를 삭제한 후 워크플로를 통해 경비 보고서를 다시 제출하면 잘못된 임시 승인자가 사용됩니다. |
| 이동 및 경비 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 마일리지 설정과 관련된 게시 오류가 발생합니다. |
