---
title: Project Operations 이중 쓰기 맵 버전
description: 이 항목은 Dynamics 365 Project Operations에 필요한 이중 쓰기 맵 목록을 제공합니다.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 385893e8ecdb29f4dc411c233b9ae19bb2448dfd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612762"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations 이중 쓰기 맵 버전

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

리소스/비 재고 시나리오에 Dynamics 365 Project Operations를 사용하려면 환경에서 실행 중인 이중 쓰기 맵 집합이 필요합니다. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>전제 조건 맵: 이중 쓰기 오케스트레이션 솔루션

다음 맵은 Project Operations 솔루션의 필수 전제 조건입니다. 다음 표에 나열된 맵과 사용자 환경의 관련 테이블 맵을 실행해야 합니다.

| 테이블 맵 | 초기 동기화 |
| --- | --- |
| 원장(msdyn_ledgers) | 테이블 맵 및 모든 전제 조건에 대한 초기 동기화가 필요합니다. 초기 동기화의 마스터는 금융 및 운영 앱입니다. |
| 법인(cdm_companies) | 필수 아님. 이중 쓰기를 사용하여 환경이 연결될 때 시스템은이 엔터티를 자동으로 채웁니다. |
| 고객 V3(거래처) | 프로비저닝에는 필요하지 않습니다. |
| 공급업체 V2(msdyn_vendors) | 프로비저닝에는 필요하지 않습니다. |

1. 맵 목록에서 모든 필수 구성 요소가 있는 원장 **(msdyn\_ledgers)** 을 선택하고 **초기 동기화** 확인란을 선택합니다. **초기 동기화를 위한 마스터** 필드에서 원장 맵과 모든 전제 조건 맵 모두에 대해 **금융 및 운영 앱** 을 선택합니다. **실행** 을 선택합니다.

![원장 맵 동기화.](media/DW6.png)

2. 위의 표에 나열된 나머지 모든 테이블 맵에 대해 동일한 단계를 따르십시오. 해당 맵을 실행할 때 **초기 동기화** 확인란을 선택하지 마십시오.

## <a name="project-operations-dual-write-maps"></a>Project Operations 이중 쓰기 맵

다음 맵은 Project Operations 솔루션에 필요합니다. Project Operations 2021년 5월 업데이트 버전 4.10.0.186부터 이중 쓰기 맵 버전이 나열됩니다.

| 엔터티 맵 | 최신 버전 | 초기 동기화 | 필요한 Dynamics 365 Finance 버전 |
| --- | --- | --- | --- |
| 프로젝트 트랜잭션 관계를 위한 통합 엔터티(msdyn\_transactionconnections) | 1.0.0.0 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 계약 헤더(판매 주문) | 1.0.0.1 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 계약 내용(salesorderdetails) | 1.0.0.0 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 자금 출처(msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | 프로비저닝에는 필요하지 않습니다. ||
| 재료 추정을 위한 Project Operations 통합 테이블(msdyn\_estimatelines) | 1.0.0.0 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 송장 제안서 V2(송장) | 1.0.0.3 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 실제(msdyn_actuals) | 1.0.0.14 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 계약 내용 이정표(msdyn_contractlinescheduleofvalues) | 1.0.0.4 | 프로비저닝에는 필요하지 않습니다. ||
| 경비 추정을 위한 Project Operations 통합 엔터티(msdyn_estimatelines) | 1.0.0.2 | 프로비저닝에는 필요하지 않습니다. ||
| 시간 추정용 Project Operations 통합 엔터티(msdyn_resourceassignments) | 1.0.0.5 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 프로젝트 경비 범주 내보내기 엔터티(msdyn_expensecategories) | 1.0.0.1 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn_expenses) | 1.0.0.3 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn_projectvendorinvoices) | 1.0.0.0 | 프로비저닝에는 필요하지 않습니다. ||
| Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn_projectvendorinvoicelines) | 1.0.0.4 | 프로비저닝에는 필요하지 않습니다. | 10.0.26 이상 |
| 모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories) | 1.0.0.1 | 프로비저닝 중에 Dynamics 365 Dataverse 환경에 채워진 프로젝트 관리자 및 팀 구성원 리소스 역할을 동기화하려면 테이블 맵에 대한 초기 동기화가 필요합니다. Dataverse는 초기 동기화의 주요 소스입니다. ||
| 프로젝트 작업(msdyn_projecttasks) | 1.0.0.4 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 트랜잭션 범주(msdyn_transactioncategories) | 1.0.0.0 | 프로비저닝에는 필요하지 않습니다. ||
| 프로젝트 V2(msdyn_projects) | 1.0.0.2 | 프로비저닝에는 필요하지 않습니다. ||

나열된 맵을 실행하려면 다음 단계를 완료하십시오.

1. 이 맵에는 초기 동기화가 필요하므로 **모든 회사 (bookableresourcecategories)** 테이블 맵에 대한 프로젝트 리소스 역할을 활성화합니다. **초기 동기화 마스터** 필드에서 **Common Data Service** 를 선택합니다. 

 ![리소스 역할 테이블 맵 동기화.](media/6ResourceInitialSync.jpg)

 다음 단계로 이동하기 전에 맵 상태가 **실행 중** 이 될 때까지 기다리십시오.

2. 나머지 필수 맵을 모두 선택합니다. 오른쪽 상단의 검색에서 키워드 **프로젝트** 를 사용하여 이중 쓰기 맵 목록에서 필터링할 수 있습니다. 모든 맵을 다중 선택하여 실행할 수 있습니다. 자세한 내용은 [여러 테이블 맵 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps)를 참조하십시오. 관련 엔터티 맵도 활성화하고 실행해야 합니다.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations 이중 쓰기 맵 버전

항상 환경에서 최신 버전의 맵을 실행하십시오. 다음 조건 중 하나라도 존재하면 특정 기능이 올바르게 작동하지 않을 수 있습니다.

- 맵이 활성화되지 않았습니다.
- 최신 버전의 맵이 활성화되지 않았습니다. 
- 관련 테이블 맵이 활성화되지 않았습니다.

**이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장하여 새 버전의 맵을 활성화할 수 있습니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용해야 합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.
