---
title: 새로운 기능 2022년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비재고 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 6월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031339"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>새로운 기능 2022년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.43.0.77 또는 4.43.0.119의 Project Operations.
- Dynamics 365 Finance 환경 버전 10.0.27의 프로젝트 관리 및 회계

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 표는 Project Operations 2022년 6월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| 엔터티 맵 | 업데이트된 버전 | 댓글 |
| --- | --- | --- |
| Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn_projectvendorinvoices) | 1.0.0.1 | 공급업체 송장 상태 추적을 위해 레거시 필드를 더 이상 사용하지 않고 새 필드에 매핑했습니다. |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 하도급 계약 | 2708885 | 사용자가 예약 가능한 리소스가 채워지지 않은 예약 가능한 리소스 예약 헤더 레코드를 생성할 때 나타나는 오류 메시지를 수정했습니다. |
| 프로젝트 계획 및 추적 | 2629441 | 프로젝트 작업이 업데이트될 때 무한 루프를 방지하는 데 도움이 되도록 워크플로 트리거 논리를 수정했습니다. |
| 시간 및 경비 | 2641209 | 할당/예약에서 시간 입력 가져오기는 예약 가능한 리소스 참조를 유지해야 합니다. |
| 프로젝트 계획 및 추적 | 2651148 | 프로젝트 문서 헤더는 보호되어야 합니다.|
| 프로젝트 계획 및 추적 | 2653145 | 이름에 유효하지 않은 문자가 포함된 프로젝트 레코드를 생성할 수 없도록 하는 유효성 검사가 추가되었습니다. |
| 시간 및 경비 | 2654710 | **승인** 페이지에서 필터링을 수정했습니다. |
| 청구 및 가격 책정 | 2667805 | 미청구 판매 실적을 뒷받침하지 않는 경우 청구 판매 실적이 생성되지 않도록 하는 유효성 검사가 추가되었습니다. |
| 청구 및 가격 책정 | 2668378 | 논리적 이름과 필드 이름이 채워지지 않는 한 사용자 정의 가격 차원이 추가되는 것을 방지하는 데 도움이 되는 유효성 검사가 추가되었습니다. |
| 하도급 계약 | 2677485 | 공급업체 송장 라인 이중 쓰기 맵의 대상 버전을 업데이트했습니다. |
| 시간 및 경비 | 2700428 | 승인 세트 중 하나가 시스템 작업에 걸린 경우에도 프로젝트에 대한 다른 승인 세트를 처리할 수 있도록 승인 논리를 개선했습니다. |

### <a name="project-management-and-accounting-in-finance"></a>Finance의 프로젝트 관리 및 회계

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics LCS(Lifecycle Services)에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271)를 보십시오.
