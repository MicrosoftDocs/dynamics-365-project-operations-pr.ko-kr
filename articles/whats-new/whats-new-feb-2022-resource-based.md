---
title: 2022년 2월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2022년 2월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932994"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022년 2월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.28.0.120의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.24의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

- 이 릴리스부터 단일 프로젝트에 최대 300명의 팀 구성원을 추가할 수 있습니다. 이전에는 팀원 수 제한이 150명이었습니다. 자세한 내용은 [프로젝트 제한](../project-management/create-wbs.md#project-limitations)을 참조하십시오.

## <a name="project-operations-dual-write-map-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 목록은 Project Operations 2022년 2월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| 엔터티 맵 | 업데이트된 버전 | 댓글 |
| --- | --- | --- |
| Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn\_expenses) | 1.0.0.3 | 프로젝트 활동 동기화가 Dataverse로 확장되었습니다. |

Project Operations 이중 쓰기 맵의 최신 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하십시오.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2415109 | **작업 지불 조건** 필드의 기본값은 프로젝트 계약 고객 레코드 및 견적 송장 레코드여야 합니다. |
| 청구 및 가격 책정 | 2497369 | 재료 수정은 **보정** 매개 변수의 날짜 값을 따라야 합니다. |
| 청구 및 가격 책정 | 2498697 | **시간 입력 회수** 에 대한 보안 구성을 개선했습니다. |
| 청구 및 가격 책정 | 2513824 | 리소스 기반 시나리오의 경우 Project Operations에서 트랜잭션 범주 ID는 28자를 초과할 수 없습니다. |
| 청구 및 가격 책정 | 2517455 | **송장 라인 트랜잭션 새로 고침** 작업은 동일한 송장에 대해 작업이 동시에 여러 번 실행되도록 허용해서는 안 됩니다. |
| 청구 및 가격 책정 | 2517465 | **송장 라인 상세내역 비활성화** 작업은 지원되지 않기 때문에 작업이 차단되었습니다. |
| 청구 및 가격 책정 | 2556660 | 프로젝트 매개변수 레코드에 첨부된 가격표에서 수행되는 날짜 유효성 검사를 수정했습니다. |
| 영업 기회 관리 | 2369202 | 유효 날짜가 겹치는 가격표를 동일한 프로젝트 계약에 첨부할 수 있는지 확인하는 비즈니스 로직을 수정했습니다. |
| 영업 기회 관리 | 2385965 | **저장 후 닫기** 를 선택할 때 **프로젝트 계약** 페이지의 **고객** 탭에서 동작을 수정했습니다. |
| 시간 및 경비 | 2538503 | 경비 보고서가 게시된 후 **프로젝트 실제 값** 엔터티에서 프로젝트 작업을 사용할 수 있어야 합니다. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | 공급업체 신용 메모 가져오기 중 오류가 발생합니다. 오류 메시지는 "유보금 금액은 잔여 순 금액보다 클 수 없습니다."입니다. |
| 프로젝트 관리 및 회계 | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | 송장 제안서에 실제 청구되지 않은 판매 금액이 0인 수수료 거래가 포함되어 있으면 송장을 발행할 수 없습니다. |
| 프로젝트 관리 및 회계 | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | 구매 가격이 업데이트되고 **변경 관리 활성화** 가 활성화된 후 게시된 비용이 올바르지 않습니다.|
| 프로젝트 관리 및 회계 | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | 고정 가격 프로젝트에 대한 전기 견적은 **예상 계산을 위해 프로젝트 계약 통화 활성화** 기능이 활성화된 경우에도 견적 바우처의 잘못된 통화 및 금액을 사용합니다. |
| 프로젝트 관리 및 회계 | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** 은 활성화되지 않은 구성 키가 있는 엔터티에 대한 예외를 포착하지 않고 변경 추적을 활성화하기 위해 호출해서는 안 됩니다. |
| 프로젝트 관리 및 회계 | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | 고급 분개장이 여러 개 전기되고 오류가 발생하면 일괄 작업이 수정됩니다. |
| 이동 및 경비 | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | 경비 보고서의 현금 서비스와 관련된 결제 문제로 인해 세액은 현금 서비스의 일부로 포함되지 않습니다. |
| 이동 및 경비 | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | 판매세 정보는 **경비 - 전기된 트랜잭션** 보고서에 포함되지 않습니다. |
| 이동 및 경비 | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | **영수증 필요** 경비 정책 위반은 경비 보고서에 경고를 잘못 표시합니다. |
| 이동 및 경비 | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | 프로젝트 트랜잭션은 트랜잭션이 마일리지 비용의 결과인 경우 총 판매액에 회수 불가능한 판매세가 포함되지 않습니다. |
| 이동 및 경비 | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | 항목별 라인에 세금이 있는 경우 항목별 라인 날짜를 변경할 수 없으며 출처 문서 상태 오류가 발생합니다. |

## <a name="removed-and-deprecated-features"></a>제거되었고 사용되지 않는 기능

[Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](removed-depreciated-features-project.md) 문서에서는 Dynamics 365 Project Operations의 제거되었거나 더 이상 사용되지 않는 기능을 설명합니다.

- 제거된 기능은 더 이상 제품에서 사용할 수 없습니다.
- 더 이상 사용되지 않는 기능은 현재 개발 중이 아니며 향후 업데이트에서 제거될 수 있습니다.

사용 중단 발표는 제품에서 기능이 제거되기 12개월 전에 [Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](removed-depreciated-features-project.md) 문서에 표시됩니다.

컴파일 시간에만 영향을 미치지만 샌드박스 및 프로덕션 환경과 바이너리 호환되는 주요 변경 사항의 경우 사용 중단 시간은 12개월 미만입니다. 일반적으로 이러한 변경 사항은 컴파일러에 대해 수행해야 하는 기능 업데이트입니다.
