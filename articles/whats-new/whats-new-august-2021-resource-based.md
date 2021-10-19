---
title: 새로운 기능 2021년 8월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 2021년 8월 Project Operations에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501379"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>새로운 기능 2021년 8월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

   - Microsoft Dataverse 환경 버전 4.13.0.152의 Project Operations.
   - Dynamics 365 Finance 환경 버전 10.0.20의 프로젝트 관리 및 회계

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- **승인 집합**: 승인은 그룹 시간, 경비 또는 자재 사용 승인 요청을 더 작은 작업 하위 집합으로 함께 설정합니다. 이 그룹화를 통해 프로젝트별로 특정 순서로 승인을 처리하고 재시도 및 순서를 지정할 수 있습니다. 요청을 그룹화하면 대량 승인에 대한 승인 처리의 안정성과 추적 가능성이 향상됩니다. 자세한 내용은 [승인 집합](../approvals/approval-sets.md)을 참조하십시오.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다.

Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다. **버전** 열의 **이중 쓰기** 페이지에서 활성 버전의 맵을 볼 수 있습니다. **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장하여 맵의 새 버전을 활성화합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

지도를 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 [지도에서 테이블 열 누락 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2295625 | 마일스톤 이름은 송장 일정에서 송장 라인 상세내역으로 복사해야 합니다. |
| 청구 및 가격 책정 | 2316323 | 리소스 기반 시나리오에 대한 Project Operations의 견적 송장에서 할인을 편집할 수 없어야 합니다. |
|  영업 기회 관리 | 2338619 | **영업 기회** 및 **견적** 비즈니스 규칙은 페이지에서만 호출해야 합니다. |
| 리소스 관리 | 2316523 | 역할이 연결된 리소스 요구 사항에서 **요청 보내기** 를 사용하면 오류가 표시되지 않습니다. |
| 리소스 관리 | 2326885 | 프로젝트를 통해 리소스 요구 사항을 생성하면 오류가 표시되지 않습니다. |
| 시간 및 경비 | 2335584 | 시간 항목에서 더 이상 사용되지 않는 작업 흐름입니다. |
| 시간 및 경비 | 2336884 | **주 복사** 시간 입력 버튼은 현재 사용자뿐만 아니라 다른 사용자에게도 작동해야 합니다. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 이동 및 경비 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 잘못된 판매자 거래 및 판매세 거래 금액은 신용 카드 거래에서 비용이 생성될 때 전기됩니다. |
| 이동 및 경비 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 잘못된 정산은 지급 분개가 생성될 때 생성되는 라인입니다. |
| 이동 및 경비 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 잘못된 판매세 거래 금액은 신용 카드 거래에서 비용이 생성될 때 전기됩니다. |
| 이동 및 경비 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 경비 라인을 삭제하는 데 시간이 오래 걸릴 수 있습니다. |
| 프로젝트 회계 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | 시스템은 KB 4619395를 적용한 후 추정치를 게시할 때 연속 번호 시퀀싱 설정을 지원하지 않습니다. |
| 프로젝트 회계 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 공급업체 송장 게시가 "2021년 5월 17일 기준으로 바우처의 거래 잔액이 일치하지 않습니다."라는 오류 메시지와 함께 실패할 수 있습니다. (회계 통화: 0.00 - 보고 통화: 0.01)" |
