---
title: 새로운 기능 2022년 7월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비재고 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 7월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403960"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>새로운 기능 2022년 7월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.44.0.22의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.28의 프로젝트 관리 및 회계

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 배포 및 구성 | 2761472 | Project Operations 설치 오류가 처리됩니다. |
| 청구 및 가격 책정 | 2746940 | 하도급 계약 내용 이름은 최대 100자여야 합니다. |
| 청구 및 가격 책정 | 2739162 | 고객은 실제 그리드 보기에서 리본 단추를 볼 수 있어야 합니다. |
| 프로젝트 계획 및 추적 | 2730318 | 프로젝트 제목에서 지원되지 않는 문자에 대한 유효성 검사가 업데이트되었습니다. |
| 청구 및 가격 책정 | 2705361 | 마일스톤 청구 매출액 실제는 프로젝트 추적 필드에 포함되어야 합니다. |
| 청구 및 가격 책정 | 2675880 | 프로젝트가 작업 기반이 아닌 계약 내용에 연결되지 않도록 합니다. |
| 청구 및 가격 책정 | 2664396 | 견적 가격표가 견적 없이 저장되는 경우 견적을 비워 둘 수 없다는 오류가 있어야 합니다. |
| 청구 및 가격 책정 | 2184019 | 지원 계약 또는 견적이 없는 프로젝트의 경우 **작업 기반 청구** 탭이 표시되지 않아야 합니다. |
| 시간 및 경비 | 2754459 | 반복 예약 클라우드 흐름이 비활성화되면 배너를 표시하고 비동기 처리를 우회합니다. |
| 청구 및 가격 책정 | 2724391 | 프로젝트 계약 분할 청구 규칙에 고객 값이 누락된 경우 잘못된 예외가 발생합니다. |
| 청구 및 가격 책정 | 2708638 | 자재 사용량 및 자재 사용 승인에서 그리드 검색을 사용하여 검색하는 동안 레코드를 찾을 수 없습니다.|
| 청구 및 가격 책정 | 2686977 | 송장 생성 중 송장 라인에 대한 유효성 검사를 방지합니다. |
| 청구 및 가격 책정 | 2683032 | 청구 가능한 역할 및 범주 복사는 5000개 레코드를 초과하지 않습니다.|
| 청구 및 가격 책정 | 2673363 | 프로젝트의 비용 소비 %는 프로젝트에 대한 노력 및 비용 추정치와 실제 수치가 모두 있는 경우 손상됩니다. |

### <a name="project-management-and-accounting-in-finance"></a>Finance의 프로젝트 관리 및 회계

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics LCS(Lifecycle Services)에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)를 보십시오.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>향후 릴리스에서 기본적으로 켜져 있는 기능

다음 표에는 버전 10.0.29에서 기본적으로 켜져 있는 기능이 나열되어 있습니다. 자동으로 켜진 대부분의 기능은 [기능 관리](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)에서 끌 수 있습니다. 앞으로는 자동으로 켜진 일부 기능이 기능 관리에서 제거되어 필수가 될 수 있습니다. 이 변경 사항은 고객이 현재 기능을 사용하도록 하여 추가된 현재 기능을 기반으로 개선 사항을 구축할 수 있도록 합니다. 기능은 필수라고 판단되지 않는 한 1년 이내에 자동으로 활성화되지 않습니다.

| 기능 이름 | 활성화 날짜 | 기능을 추가한 날짜 | 기능 상태 | 모듈 |
| --- | --- | --- |--- |--- |
| 자금 조달 규칙 할당 변경에 따른 시간 트랜잭션 조정 가능 | 2022년 9월 16일 | 2020년 10월 7일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트 구매 주문 선불 송장 취소 기능 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 자원 기반/비 재고 시나리오에 대해 Project Operations를 사용할 때 송장 제안 라인 삭제 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 게시된 프로젝트 트랜잭션에 대한 회계 조정 | 2022년 9월 16일 | 2020년 5월 10일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트에 대한 기본 회계 설정 활성화 | 2022년 9월 16일 | 2020년 2월 19일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트에 대해 여러 계약 내용 활성화 | 2022년 9월 16일 | 2020년 6월 29일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 현재 승인 상태가 편집을 허용하지 않는 경우 프로젝트 시간 분개장을 읽기 전용으로 설정 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 구매 라인이 업데이트되고 구매 주문 변경 관리 매개 변수가 켜져 있을 때 구매 라인에서 판매 라인 동기화 활성화 | 2022년 9월 16일 | 2020년 10월 7일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| Dynamics 365 Customer Engagement에서 Project Operations 활성화 | 2022년 9월 16일 | 2020년 6월 29일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트 트랜잭션 취소 수정 기능 | 2022년 9월 16일 | 2020년 7월 13일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>향후 릴리스에서 필수가 되는 기능

다음 표에는 버전 10.0.29 이후에 필수가 되는 기능이 나열되어 있습니다.

| 기능 이름 | 활성화 날짜 | 기능을 추가한 날짜 | 기능 상태 | 모듈 |
| --- | --- | --- | --- | --- |
| 환율을 반올림하지 않고 자금 출처의 약정 가치를 계산합니다. | 2022년 9월 16일 | 2020년 6월 14일 | 필수 | 프로젝트 관리 및 회계 |
| 원래 거래와 동일한 원장 계정으로 프로젝트 조정 전기 활성화 | 2022년 9월 16일 | 2020년 6월 14일 | 필수 | 프로젝트 관리 및 회계 |
| 프로젝트 계약 약정 금액 세부 정보 | 2022년 9월 16일 | 2019년 8월 31일 | 필수 | 프로젝트 관리 및 회계 |
| 프로젝트 송장 제안 생성 중 리소스별 정렬 활성화 | 2022년 9월 16일 | 2019년 8월 31일 | 필수 | 프로젝트 관리 및 회계 |
