---
title: Project Service Automation에서 Finance and Operations로 직접 프로젝트 작업 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 작업을 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080034"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation에서 Finance and Operations로 직접 프로젝트 작업 동기화

[!include[banner](../includes/banner.md)]

이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 작업을 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.

> [!NOTE]
> - 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.
> - KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다. 회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.
> - 실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation에서 Finance까지의 데이터 흐름

Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 작업에 대한 데이터 흐름을 사용할 수 있습니다.

다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.

[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>템플릿 및 작업

템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 작업을 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 작업(PSA에서 Fin 및 Ops까지)
- **프로젝트에서 작업의 이름:** 프로젝트 작업

프로젝트 작업의 동기화가 발생하기 전에 프로젝트 계약 및 프로젝트를 동기화해야 합니다.

## <a name="entity-set"></a>엔터티 집합

| Project Service Automation | 재무                             |
|----------------------------|-------------------------------------|
| 프로젝트 작업              | 프로젝트 작업을 위한 통합 엔터티 |

## <a name="entity-flow"></a>엔터티 흐름

프로젝트 작업은 Project Service Automation에서 관리되며 프로젝트 활동으로 Finance에 동기화됩니다.

## <a name="prerequisites-and-mapping-setup"></a>필수 조건 및 매핑 설정

프로젝트 작업의 동기화가 발생하기 전에 프로젝트 계약 및 프로젝트를 동기화해야 합니다.

## <a name="power-query"></a>파워 쿼리

이 조건이 충족되는 경우 데이터를 필터링하려면 Microsoft Excel용 파워 쿼리를 사용해야 합니다.

- 프로젝트 작업에 리소스별 레코드가 있습니다.

파워 쿼리를 사용해야 하는 경우 다음 지침을 따르십시오.

- 프로젝트 작업(PSA에서 Fin 및 Ops로) 템플릿에는  **IsLineTask** 의 필터를 **False** 로 설정하여 프로젝트 작업에서 리소스 별 레코드를 제외하는 기본 필터가 있습니다. 고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.

## <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![템플릿 매핑](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
