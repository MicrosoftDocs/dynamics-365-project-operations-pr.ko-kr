---
title: Project Service Automation 개요
description: 이 항목은 Dynamics 365 Project Service Automation과 Dynamics 365 Finance 통합 솔루션에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080193"
---
# <a name="project-service-automation-overview"></a>Project Service Automation 개요

[!include[banner](../includes/banner.md)]

Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Common Data Service를 통해 Dynamics 365 Finance 및 Dynamics 365 Project Service Automation의 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 프로젝트, 프로젝트 계약, 프로젝트 계약 내용, 프로젝트 계약 내용 중요 시점, 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정치 및 Project Service Automation에서 Finance에 이르는 경비 추정치의 흐름을 사용할 수 있습니다.

> [!NOTE]
> - 버전 7.3.0을 사용하는 경우 KB 4074835를 설치해야 합니다. 그런 다음 고정 가격 프로젝트를 통합할 수 있습니다.
> - 버전 7.3.0을 사용 중이고 Project Service Automation에서 수수료 거래를 가져오는 경우 프로젝트 송장에 해당 수수료를 포함하려면 KB 4345320를 설치해야 합니다.
> - 버전 8.0을 사용하는 경우 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정치, 비용 추정치 및 기능 잠금을 사용할 수 있습니다.
> - 버전 8.0.1 이상을 사용하는 경우 실제 데이터를 동기화할 수 있습니다.

Project Service Automation Finance를 통합하려면 먼저 Project Service Automation 통합 매개 변수를 구성해야 합니다. 자세한 내용은 [Project Service Automation 통합 매개 변수](PSA-parameters.md)를 참조하십시오.

이 통합 솔루션은 다음 시나리오에서 직접 동기화를 가능하게 합니다.

- Project Service Automation에서 프로젝트 계약을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 계약 내용을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 계약 내용 중요 시점을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 작업을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Finance에서 경비 트랜잭션 범주를 유지하고 Finance에서 Project Service Automation으로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 시간 추정치를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 경비 추정치를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.
- Project Service Automation에서 프로젝트 시간, 경비 및 수수료 실제를 만들고 Finance에 게시할 수 있도록 Project Service Automation 통합 저널에 프로젝트 트랜잭션을 만듭니다.

## <a name="data-synchronization"></a>데이터 동기화

다음 그림은 Project Service Automation과 Finance 간에 통합의 일부로 데이터가 동기화되는 방식을 보여줍니다.

> [!NOTE]
> 현재 모든 템플릿을 사용할 수 있는 것은 아닙니다. 템플릿이 완성되면 릴리스됩니다.

[![Project Service Automation과 Finance 통합](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance 시스템 요구 사항

Project Service Automation와 Finance 통합 솔루션을 사용하려면 플랫폼 업데이트 12 이상이 포함된 Enterprise 버전 7.3을 설치해야 합니다.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation 시스템 요구 사항

Project Service Automation과 Finance 통합 솔루션을 사용하려면 다음 구성 요소를 설치해야 합니다.

- Dynamics 365 Project Service Automation 버전 9.0.0.0 이상
- Dynamics 365 Sales, 버전 1.14.0.0(v14) 이상을 위한 현금 잠재 기부자 솔루션
- Dynamics 365 Project Service Automation 버전 1.0.0.0 이상용 Project Service Automation to Finance 솔루션

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation 인스턴스에 Project Service Automation to Finance 통합 솔루션 설치

[Microsoft 다운로드 센터](https://www.microsoft.com/download/details.aspx?id=57016)에서 Project Service Automation to Finance 통합 솔루션을 다운로드하고 솔루션에 포함된 지침을 따릅니다.
