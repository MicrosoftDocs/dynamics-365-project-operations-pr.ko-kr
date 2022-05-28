---
title: 2022년 4월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목에서는 리소스/비재고 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 4월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613282"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022년 4월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.41.0.45의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.26의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

조달 범주는 프로젝트 구매 주문 및 보류 중인 공급업체 송장에 사용할 수 있습니다. 자세한 내용은 [프로젝트 구매 주문 및 보류 중인 공급업체 송장에 조달 범주 사용](configure-procurement-categories.md)을 참조하십시오.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 표는 Project Operations 2022년 3월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| 엔터티 맵 | 업데이트된 버전 | 댓글 |
| -------------- | ------------------- | ------------|
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn\_projectvendorinvoicelines) | 1.0.0.4 | 이 맵은 구매 주문 및 보류 중인 공급업체 송장과 함께 조달 범주 사용을 지원합니다. |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| ------------ | ---------------- | -------------- |
| 시간 및 경비 | 2573900 | **최신 승인** 기능은 기본적으로 활성화되어야 합니다. |
| 청구 및 가격 책정 | 2603313 | 제품이 있는 견적 및 계약 내용이 추가되지 않는 중복 레코드 오류를 수정했습니다. |
| 배포 및 구성 | 2611368 | 고객은 최신 앱 디자이너를 사용하여 솔루션에 최대 5개의 사용자 지정 엔터티를 추가할 수 있어야 합니다. |
| 시간 및 경비 | 2628285 | 시간 항목을 가져오는 동안 올바른 리소스 범주를 설정하는 기능에 영향을 주는 문제를 수정했습니다. |
| 영업 기회 관리| 2628815 | 제목이 100자를 초과하는 작업에 대해 가져오기가 성공하도록 작업 제목의 문자 제한과 일치하도록 견적 라인 세부 정보 설명의 문자 제한을 업데이트합니다. |
| 시간 및 경비| 2629547 | **제출자** 프로젝트 승인 필드는 레코드를 제출한 사용자를 가리켜야 합니다. |
| 시간 및 경비| 2629865 | 프로젝트를 복사할 때 작업의 **범주 복사** 필드입니다. |
| 시간 및 경비| 2636463 | 최신 승인 양식의 승인에 대한 필터를 수정했습니다. |
| 프로젝트 계획 및 추적 | 2648300 | 프로젝트 소유자가 변경되지 않는 문제가 수정되었습니다. |
| 청구 및 가격 책정 | 2563000 | 통화가 계약 통화와 다른 미청구 판매에 대한 분개장 항목은 허용되지 않아야 합니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics LCS(Lifecycle Services)에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)를 보십시오.
