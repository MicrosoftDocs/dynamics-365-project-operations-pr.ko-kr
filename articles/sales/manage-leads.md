---
title: 잠재 고객 관리
description: 이 항목은 프로젝트 기반 잠재 고객 관리 설정에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898629"
---
# <a name="manage-leads"></a>잠재 고객 관리

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

프로젝트 기반 잠재 고객은 Project Operations에서 관리하고 검증할 수 있습니다. 잠재 고객 관리 프로세스에는 작업 기반 잠재 고객을 생성하고 해당 잠재 고객을 검증하는 것이 포함됩니다. 

## <a name="project-sales-leads"></a>프로젝트 잠재 고객

**영업** 섹션의 왼쪽 탐색 창에서 **잠재 고객** 목록 페이지를 열어 시스템의 모든 잠재 고객 레코드 목록을 봅니다. 표시된 잠재 고객 목록은 Dynamics 365 Sales 또는 Dynamics 365 Field Service 응용 프로그램도 있는 경우 생성할 수 있는 작업 기반 및 기타 유형의 잠재 고객입니다.

**유형** 값에 필터를 만들어 프로젝트 기반 잠재 고객만 표시하도록 필터링된 보기를 만들 수 있습니다. 예를 들어 작업 기반 잠재 고객만 표시하도록 선택할 수 있습니다.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>프로젝트 기반 거래를 위한 새로운 잠재 고객 생성

프로젝트 기반 잠재 고객이 자격을 갖추면 영업 기회와 거래처가 생성됩니다. 프로젝트 기반 영업 기회는 영업 기회 단계에서 영업 추구 활동의 시작점입니다. 프로젝트 기반 영업 기회에는 프로젝트 작업을 판매하는 데 필요한 고유한 기능이 있습니다. 이러한 기능은 다음과 같습니다.

- 시간 및 재료 및 고정 가격 청구 방법
- 프로젝트에서 발생한 인적 자원, 경비 및 자재에 대한 여러 날짜 유효 가격 목록

적격 잠재 고객이 자동으로 영업 기회를 생성하려면 잠재 고객을 만들 때 **유형** 특성을 **작업 기반**으로 설정합니다. 다른 유형을 선택하는 경우 잠재 고객은 자격이 있으면 프로젝트 기반 영업 기회를 생성하지 않습니다. 프로젝트 기반 영업 기회가 생성되지 않으면 프로젝트별 기능을 다운스트림 판매 프로세스에서 사용할 수 없습니다.

다음 표에는 잠재 고객에 대한 중요한 필드 정보와 해당 필드의 다운스트림 영향이 포함되어 있습니다.
 
| **필드** | **위치** | **관련성, 목적 및 지침** | **다운스트림 영향** |
| --- | --- | --- | --- |
| 주제 | 일반 탭 | 이 텍스트 필드에는 거래에 대한 간단한 설명이 포함되어야 합니다. | 잠재 고객 토픽은 기본적으로 영업 기회의 토픽, 견적 및 프로젝트 계약의 이름으로 지정됩니다. |
| 종류 | 일반 탭 | 이 옵션 집합 필드에는 다음 옵션이 있습니다.</br>- 작업 기반(Project Operations가 설치된 경우에만 사용 가능)</br>- 항목 기반(Project Operations 및 Sales가 설치된 경우에만 사용 가능)</br>- 서비스 유지 보수 기반(Field Service가 설치된 경우 사용 가능) | 이 필드의 값이 잠재 고객에서 **업무 기반**으로 설정된 경우 잠재 고객은 프로젝트 기반 영업 기회를 생성할 자격이 있습니다. 이 거래에 대한 다운스트림 판매 프로세스에서 모든 프로젝트별 확장 및 기능을 활성화하려면 프로젝트 기반 영업 기회가 필요합니다. |
| 이름 | 일반 탭 | 잠재 기부자 연락처의 이름 | 잠재 고객이 자격을 갖추면 거래처, 연락처 및 영업 기회가 생성됩니다. 연락처의 이름이 여기에 설정된 값입니다. |
| 성 | 일반 탭 | 잠재 기부자 연락처의 성 | 잠재 고객이 자격을 갖추면 거래처, 연락처 및 영업 기회가 생성됩니다. 연락처의 성이 여기에 설정된 값입니다. |
| 회사 | 일반 탭 | 잠재 기부자 고객의 회사 이름 | 잠재 고객이 자격을 갖추면 거래처, 연락처 및 영업 기회가 생성됩니다. 생성된 거래처의 이름이 여기에 설정된 값입니다. |
| 통화 | Details 탭 | 잠재 기부자 고객의 통화 | 잠재 고객이 자격을 갖추면 거래처, 연락처 및 영업 기회가 생성됩니다. 생성된 거래처의 통화가 여기에 설정된 값입니다. |

## <a name="qualify-a-new-project-based-lead"></a>새로운 프로젝트 기반 잠재 고객을 우량으로 선별

**유형** 값이 **작업 기반**으로 설정된 잠재 고객을 프로젝트 기반 잠재 고객이라고 합니다. 프로젝트 기반 잠재 고객이 검증되면 다음이 생성됩니다.

- 잠재 고객의 **회사** 필드를 사용하는 거래처.
- 잠조 고객의 **이름**과 **성**의 값을 기반으로 거래처에 연결된 연락처 레코드.
- **유형** 필드가 &quot;**작업 기반**으로 설정된 프로젝트 기반 영업 기회.

적격 잠재 고객에 대한 자세한 내용은 [잠재 고객을 우량으로 선별 또는 전환](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales)을 참조하십시오.

## <a name="lead-qualification-and-legal-entity-information"></a>잠재 고객 선별 및 법인 정보 

배포 모드를 사용하여 Project Operations를 실행하는 경우 리소스/비 재고 기반 시나리오에 대한 Project Operations, 각 고객 및 영업 기회는 **담당 회사** 필드 집합이 있어야 합니다. 담당 회사는 프로젝트 제공을 담당하는 조직의 법인입니다. 각 고객 또는 고객 관계 유형이 있는 거래처는 이 고객과 계약하고 협상하는 법인으로 설정된 **담당 회사** 필드 값이 있어야 합니다. 고객은 하나의 법인에만 속할 수 있습니다.

잠재 고객이 우량으로 선별되면 생성된 고객 및 영업 기회 레코드에 **담당 회사** 필드가 현재 사용자의 예약 가능한 리소스 레코드 회사로 설정됩니다.

현재 사용자의 예약 가능한 리소스 레코드가 비어 있으면 사용자 레코드의 **담당 회사** 필드 값은 고객 및 영업 기회 레코드를 기본값으로 설정하는 데 사용됩니다.

## <a name="business-process-flow-for-project-based-deals"></a>프로젝트 기반 거래의 경우 비즈니스 프로세스 흐름

Project Operations의 프로젝트 기반 거래에 대해 다음 비즈니스 프로세스 흐름이 지원됩니다.

- 잠재 고객 - 영업 기회 비즈니스 프로세스
- 영업 기회 영업 프로세스

잠재 고객 - 영업 기회 비즈니스 프로세스는 다음 스테이지를 지원합니다.

| 스테이지 이름 | 매핑된 엔티티 | 기능 |
| --- | --- | --- |
| 우량으로 선별 | 잠재 고객 | 잠재 고객을 우량으로 선별하여 거래처, 연락처 및 영업 기회를 만듭니다. |
| 전개 | 영업 기회 | 관련된 작업, 주요 이해 관계자 및 경쟁에 대한 더 많은 정보를 추가할 수 있는 영업 기회를 개발하십시오. |
| 제안 | 영업 기회 | 제안서를 개발하고 내부 검토 팀의 승인을 받으십시오. |
| 종료 | 영업 기회 | 거래를 성사시킬 수 있는 영업 기회를 얻으십시오. |
