---
title: 2021년 9월의 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 9월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582902"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 9월의 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

*적용 대상: 리소스/비 재고 기반 시나리오에 대한 Project Operations*

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

   - Microsoft Dataverse 환경 버전 4.14.0.99의 Project Operations.
   - Dynamics 365 Finance 환경 버전 10.0.20의 프로젝트 관리 및 회계.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다. **버전** 열의 **이중 쓰기** 페이지에서 활성 버전의 맵을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 시간 및 경비 | 1811407 | 경비 입력 승인을 위해 프로젝트 승인자 보안 역할을 조정했습니다. |
| 시간 및 경비 | 1811438 | 시간 입력 승인 취소에 대한 프로젝트 승인자 보안 역할을 조정했습니다. |
| 시간 및 경비 | 2370126 | **시간 입력** 엔터티의 **프로젝트 작업** 및 **역할** 아이콘을 업데이트했습니다. |
| 시간 및 경비 | 2379879 | 전화기용 Dynamics 365를 사용할 때 시간 입력에서 **주 복사** 기능을 수정했습니다. |
| 청구 및 가격 책정 | 2371906 | 견적 송장 총액은 리소스 기반 배포에 대한 Project Operations에서 조정할 수 없습니다. |
| 청구 및 가격 책정 | 2385802 | 프로젝트 합계를 새로 고칠 때 음수 실제 시간으로 발생하는 오류가 수정되었습니다. |
| 청구 및 가격 책정 | 2389675 | 견적 송장 확인 동작이 개선되었습니다. 장기 실행 작업 엔터티는 회계 확인 결과를 작성하는 데 필요한 활동을 고려해야 합니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 이동 및 경비 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 신용 카드 트랜잭션에서 생성된 비용으로 전기된 공급업체 및 판매세 거래 금액이 올바르지 않습니다. |
| 이동 및 경비 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 지급 분개가 생성될 때 잘못된 정산 라인이 생성됩니다. |
| 이동 및 경비 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 신용 카드 트랜잭션에서 생성된 비용으로 전기된 판매세 거래 금액이 올바르지 않습니다. |
| 이동 및 경비 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 경비 라인을 삭제하는 데 시간이 오래 걸릴 수 있습니다. |
| 프로젝트 회계 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | KB 4619395를 적용한 후 숫자 시퀀스를 연속으로 변경하는 것은 지원되지 않으며 추정치를 게시할 때 "시스템이 숫자 시퀀스 Proj_X의 **연속** 설정을 지원하지 않습니다."라는 오류가 발생합니다. |
| 프로젝트 회계 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 다음 오류 메시지와 함께 공급업체 송장 게시가 실패할 수 있습니다. ""바우처에 대한 트랜잭션은 2021년 5월 17일 기준으로 균형이 맞지 않습니다. (회계 통화: 0.00 - 보고 통화: 0.01)." |
