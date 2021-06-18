---
title: 2021년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dcf11d770082308d77b369c6f50aabb1ec7c1c86
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995674"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dataverse 환경 버전 4.8.0.91의 Project Operations 
- Dynamics 365 Finance 환경 버전 10.0.16의 프로젝트 관리 및 회계 

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations


| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2133873 | **경비 추정** 그리드의 **단위 판매 가격** 통화 기호의 표시가 수정되었습니다. |
| 청구 및 가격 책정 | 2174616 | 견적이 성공되면 견적에서 복사된 계약 내용 세부 사항에서 계약 사용자 정의 가격표가 참조됩니다. |
| 영업 기회 관리 | 2167475 | 청구되지 않은 실제 입력이 발생한 수정 송장의 세액이 수정되었습니다. |
| 영업 기회 관리 | 2176285 | 판매 계약/견적 라인 상세 내역에서 원가 계약/견적 라인 상세 내역으로 세액을 복사할 수 없습니다. |
| 영업 기회 관리 | 2188079 | 작업 기반이 아닌 계약에 대해서는 분할 청구 규칙을 생성하면 안됩니다. |
| 계획 및 추적 | 2125274 | **프로젝트 시작 날짜 매핑** 의 **프로젝트 이중 쓰기 맵** 특성이 **msdyn\_taskearlieststart** 에서 **msdyn\_actualstart** 로 업데이트되었습니다. |
| 계획 및 추적 | 2138853 | 참조 작업이 대상 프로젝트에 복사되는 경비 추정 라인을 보장하기 위해 프로젝트 복사 기능이 업데이트되었습니다. |
| 계획 및 추적 | 2154306 | Project Operations에서 리소스 기반 시나리오에 대한 경비 추정을 삭제하는 문제를 수정했습니다. |
| 계획 및 추적 | 2173259 | 특정 시나리오에서 **WBS 복사** 오류 메시지를 표시하지 않도록 프로젝트 복사 기능이 업데이트되었습니다. |
| 시간 및 경비 | 2148910 | **시간 항목** 그리드에서 **항목 편집** 페이지의 표시 문제가 수정되었습니다. |
| 시간 및 경비 | 2159798 | 승인된 경비 항목을 편집할 수 없도록 제어를 강화했습니다. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance에서 프로젝트 관리 및 회계

자세한 내용은 [2021년 1월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations](whats-new-jan-2021-resource-based.md)를 참조하십시오.

## <a name="regulatory-updates"></a>규제 업데이트

Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. 규제 업데이트에 대해 배우는 또 다른 방법은 LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 보는 것입니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]