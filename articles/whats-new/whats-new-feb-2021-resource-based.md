---
title: 2021년 2월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 문서에서는 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 2월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029630"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021년 2월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 문서는 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

- Dataverse 환경 4.7.0.95의 Project Operations
- Dynamics 365 Finance 환경 버전 10.0.16의 프로젝트 관리 및 회계 

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| **청구 및 가격 책정** | 2053736 | 이제 **송장** > **관련 정보** 로 이동하여 송장 라인 세부 정보에 액세스할 수 있습니다. |
| **청구 및 가격 책정** | 2122613 | **활성화** 및 **비활성화** 작업이 **가격표** 연결 엔터티에서 제거되었습니다. |
| **청구 및 가격 책정** | 2128606 | **GetEstimatesForProject** 플러그인에서 **ullReferenceException** 관련 문제가 해결되었습니다. |
| **배포 및 구성** | 2139346 | 관리되지 않는 **Dynamics365ProjectOperationsDualWrite** 솔루션 가져오기 관련 문제가 해결되었습니다. |
| **배포 및 구성** | 2140569 | 프로젝트 솔루션은 Dataverse Teams 환경에 설치되어서는 안됩니다. |
| **배포 및 구성** | 2086991 | 웹 리소스의 지역화 사용자 지정이 제한되었습니다. |
| **영업 기회 관리** | 2136794 | **송장 확인** 또는 **지불됨으로 송장 표시** 프로세스가 실패하면 올바른 오류 메시지를 표시합니다. |
| **영업 기회 관리** | 2139330 | 프로젝트에서 프로젝트 관리자를 변경하면 담당 회사가 기본값으로 다시 설정되지 않아야 합니다. |
| **영업 기회 관리** | 2146376 | 청구 불가능한 실제의 정정된 세액은 송장 확인에서 생성됩니다. |
| **프로젝트 계획 및 추적** | 2099879 | Dataverse 환경 배포는 정적 ID로 기본 트랜잭션 범주를 만들어야 하며 환경 당 하나를 임의로 생성하지 않아야 합니다. |
| **프로젝트 계획 및 추적** | 2128577 | 리소스 할당에서 트랜잭션 범주를 업데이트하도록 Project Service 사용자 권한을 수정했습니다. |
| **프로젝트 계획 및 추적** | 2164035 | **프로젝트 복사** 함수 관련 문제가 수정되었습니다. |
| **시간 항목** | 2129161 | 사용자가 제출 또는 승인된 시간 항목을 변경 및 업데이트할 수 없도록 더 엄격한 제한이 적용됩니다. |
| **시간 항목** | 2103572 | 비 프로젝트 시간 항목에 대한 시간 승인은 프로젝트 승인자 역할을 찾지 않아야 합니다. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance의 프로젝트 관리 및 회계 

Dynamics 365 Finance의 프로젝트 관리 및 회계에 대한 자세한 내용은 [2021년 1월의 새로운 기능 - 리소스/비재고 기반 시나리오에 대한 Project Operations](whats-new-jan-2021-resource-based.md)를 참조하십시오.


## <a name="regulatory-updates"></a>규제 업데이트

금융 및 운영 앱의 규정 업데이트에 대한 자세한 내용은 [규정 업데이트](/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오. 규제 업데이트에 대해 배우는 또 다른 방법은 LCS(Lifecycle Services)에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 보는 것입니다. 문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]