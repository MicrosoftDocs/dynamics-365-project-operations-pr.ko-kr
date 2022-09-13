---
title: 새로운 기능 2022년 8월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비재고 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 8월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403865"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>새로운 기능 2022년 8월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.45.0.53의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.28의 프로젝트 관리 및 회계

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 이중 쓰기 맵 업데이트

이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다. Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.

항상 사용자 환경에서 최신 버전의 맵을 실행하고 Project Operations Dataverse 솔루션 및 Finance 솔루션 버전을 업데이트할 때 모든 관련 테이블 맵을 활성화하십시오. 최신 버전의 맵이 활성화되지 않은 경우 일부 기능이 제대로 작동하지 않을 수 있습니다. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. 새 버전의 맵을 활성화하려면 **테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장합니다. 기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다. 자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.

맵을 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 맵에서 [누락된 테이블 열 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 영업 기회 관리 | 2762089 | 조직에서 자동 저장이 비활성화된 경우 계약을 닫는 동안 손실되는 오류 처리.|
|프로젝트 계획 및 추적 | 2767841 | 원격 분석 업데이트 프로젝트 엔터티 시나리오 만들기 또는 업데이트.|
|청구 및 가격 책정 | 2771072 | 견적을 받는 동안 Null 참조 예외 처리.|
|청구 및 가격 책정 | 2844181 |상관 관계 ID를 가져오고 송장 생성을 차단하는 데 실패했습니다.|
|청구 및 가격 책정 | 2852836 | CE에서 생성 및 승인된 본지사 경비에 대한 본지사 실제 경비가 누락되었습니다.|


### <a name="project-management-and-accounting-in-finance"></a>Finance의 프로젝트 관리 및 회계

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics LCS(Lifecycle Services)에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)를 보십시오.
