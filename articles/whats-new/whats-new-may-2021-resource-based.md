---
title: 2021년 5월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 5월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930418"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 5월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dynamics 365 Dataverse 환경 버전 4.10.0.186의 Project Operations
- 금융 및 운영 앱 환경 버전 10.0.18의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- [예약 모드](../project-management/scheduling-modes.md): 프로젝트 관리자는 프로젝트를 고정 기간, 고정 작업 또는 고정 단위 스케줄링 모드를 사용하여 관리해야 하는지 정의할 수 있습니다.
- [마일리지 비율 계층을 사용하여 마일리지 설정](../expense/set-up-mileage.md): 직원 경비 보고서의 마일리지 비율 계층을 업데이트합니다.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

다음 목록은 Project Operations 2021년 5월 릴리스에서 수정되거나 추가된 이중 쓰기 맵을 보여줍니다.

| 엔터티 맵 | 업데이트된 버전 | 댓글 |
| --- | --- | --- |
| 프로젝트 자금 출처(msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | 프로젝트 계약 고객 결제 조건을 동기화합니다. |
| 프로젝트 송장 제안서 V2(송장) | 1.0.0.3 | 견적 송장 결제 조건을 동기화합니다. |
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn\_projectvendorinvoicelines) | 1.0.0.1 | 품질 업데이트 |
| 프로젝트 V2 (msdyn\_projects) | 1.0.0.2 | 품질 업데이트 |

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 금융 및 운영 앱 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작할 때 문제가 발생하면 이중 쓰기 문제 해결 가이드의 [맵에서 표 열 누락 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2227635 | **단위 그룹** 및 **단위** 필드의 값은 **재료 추정** 그리드의 제품에서 기본값입니다. |
| 청구 및 가격 책정 | 2234127 | 공급업체 송장이 전기될 때 **작업 ID** 필드가 이제 Dataverse 프로젝트 실제 값에 올바르게 통합됩니다. |
| 청구 및 가격 책정 | 2235564 | 분개장 항목을 저장하면 분개장 항목에 표시된 통화가 저장 후 라인에 대한 기본 통화와 일치합니다. |
| 청구 및 가격 책정 | 2246671 | 송장 발행 중에 트랜잭션을 청구 불가능하게 설정하면 원래의 청구되지 않은 판매 레코드가 취소되고 청구되지 않은 새 판매 레코드가 청구 불가능으로 생성됩니다. |
| 청구 및 가격 책정 | 2264042 | 환경에서 유효하지 않은 송장 수정 세부 정보가 있는 경우 유효한 송장 수정을 차단해서는 안됩니다. |
| 청구 및 가격 책정 | 2146367 | 프로젝트 송장 헤더 이중 쓰기 매핑이 지불 조건을 포함하도록 확장되었습니다. |
|  영업 기회 관리 | 2086888 | 견적을 새로 복사된 견적의 유료 역할 및 범주에 복사하기 전에 비활성화 된 역할 및 범주를 추가하지 마십시오. |
|  영업 기회 관리 | 2234376 | 읽기 전용 필드는 **재료 추정** 그리드에서 회색으로 표시됩니다. |
|  영업 기회 관리 | 2238337 | 연락처를 기반으로 한 견적은 프로젝트 가격표와 연결되지 않은 경우에도 저장할 수 있습니다. |
|  영업 기회 관리 | 2239810 | 견적을 분실로 마감하면 관련 프로젝트도 마감되고 모든 예약이 취소됩니다. |
| 프로젝트 계획 및 추적 | 2099559 | **프로젝트 작업** 그리드가 열리기 전에 시스템 상태에 대한 추가 유효성 검사를 추가했습니다. |
| 프로젝트 계획 및 추적 | 2178987 | **프로젝트** 페이지에서 **다음 단계** 를 선택할 때 발생하는 일시적인 오류를 수정했습니다. |
| 리소스 관리 | 2224817 | 예약을 확장하는 기능은 기본적으로 올바른 예약 상태로 설정됩니다. |
| 시간 항목 | 2202476 | **시간 항목** 페이지는 이제 반응 그리드 제어를 사용하고 그리드 정렬 불량과 같은 문제를 수정합니다. |
| 시간 항목 | 2223377 | 사용성과의 혼동을 피하기 위해 **예약 가능한 리소스** 페이지의 **관련 항목** 섹션에서 시간 항목이 숨겨집니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 프로젝트 관리 및 회계 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 리소스 기반 시나리오의 Project Operations: 통합 오류로 인해 견적을 성공으로 변환할 수 없습니다. |
| 프로젝트 관리 및 회계 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: 겹치는 계약 내용 및 트랜잭션 유형을 확인하기 때문에 계약 내용을 프로젝트 ID에 연관시키려고 하면 오류가 발생합니다. |
| 프로젝트 관리 및 회계 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 는 다른 고객의 자금 출처 송장 주소를 설정합니다. |
| 이동 및 경비 | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 마일리지 설정과 관련된 게시 오류가 발생할 수 있습니다. |
| 이동 및 경비 | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **개인으로 분할** 기능이 외화 경비 트랜잭션에 대해 작동하지 않습니다. |
| 이동 및 경비 | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 경비 범주 드롭 다운 값이 대리인이 리소스인 경우 잘못된 범주를 표시합니다. |
| 이동 및 경비 | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | **리소스/범주 검증** 오류로 인해 회사 간 경비 보고서를 저장할 수 없습니다. |
| 이동 및 경비 | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 경비 보고서 전기의 잘못된 마일리지 계산에 분할 라인이 있습니다. |
| 이동 및 경비 | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 판매세가 포함되어 있고 결제 방법의 오프셋 계정 유형이 **작업자** 와 같은 경우 회사 간 경비 보고서를 전기할 수 없습니다. |
| 이동 및 경비 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** 데이터 엔터티 및 관련 고유 인덱스 롤백이 연결되어 있습니다. |
| 이동 및 경비 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 경비 보고서는 소스 문서 라인 생성 및 업데이트를 지원합니다. |
| 이동 및 경비 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 판매세가 대상 법인에 전기되는 경우 본지사 시나리오에 잘못된 보조 원장 분개가 표시됩니다. |
| 이동 및 경비 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: 지출 추정치는 재무에서 삭제될 때 Dataverse에서 삭제되지 않습니다. |
| 이동 및 경비 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 경비 범주가 비 프로젝트 범주인 경우 **경비** 페이지에 선택된 재무 차원은 경비 보고서에 복사되지 않습니다. |
