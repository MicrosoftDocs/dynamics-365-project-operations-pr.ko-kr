---
title: Project Service Automation 개요
description: 이 항목은 Dynamics 365 Project Service Automation과 Dynamics 365 Finance 통합 솔루션에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005889"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="20e18-103">Project Service Automation 개요</span><span class="sxs-lookup"><span data-stu-id="20e18-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="20e18-104">Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Common Data Service를 통해 Dynamics 365 Finance 및 Dynamics 365 Project Service Automation의 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="20e18-105">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 프로젝트, 프로젝트 계약, 프로젝트 계약 내용, 프로젝트 계약 내용 중요 시점, 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정치 및 Project Service Automation에서 Finance에 이르는 경비 추정치의 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="20e18-106">버전 7.3.0을 사용하는 경우 KB 4074835를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="20e18-107">그런 다음 고정 가격 프로젝트를 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="20e18-108">버전 7.3.0을 사용 중이고 Project Service Automation에서 수수료 거래를 가져오는 경우 프로젝트 송장에 해당 수수료를 포함하려면 KB 4345320를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="20e18-109">버전 8.0을 사용하는 경우 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정치, 비용 추정치 및 기능 잠금을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="20e18-110">버전 8.0.1 이상을 사용하는 경우 실제 데이터를 동기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="20e18-111">Project Service Automation Finance를 통합하려면 먼저 Project Service Automation 통합 매개 변수를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="20e18-112">자세한 내용은 [Project Service Automation 통합 매개 변수](PSA-parameters.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="20e18-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="20e18-113">이 통합 솔루션은 다음 시나리오에서 직접 동기화를 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="20e18-114">Project Service Automation에서 프로젝트 계약을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-115">Project Service Automation에서 프로젝트를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-116">Project Service Automation에서 프로젝트 계약 내용을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-117">Project Service Automation에서 프로젝트 계약 내용 중요 시점을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-118">Project Service Automation에서 프로젝트 작업을 유지하고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-119">Finance에서 경비 트랜잭션 범주를 유지하고 Finance에서 Project Service Automation으로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="20e18-120">Project Service Automation에서 프로젝트 시간 추정치를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-121">Project Service Automation에서 프로젝트 경비 추정치를 만들고 Project Service Automation에서 Finance로 직접 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="20e18-122">Project Service Automation에서 프로젝트 시간, 경비 및 수수료 실제를 만들고 Finance에 게시할 수 있도록 Project Service Automation 통합 저널에 프로젝트 트랜잭션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="20e18-123">데이터 동기화</span><span class="sxs-lookup"><span data-stu-id="20e18-123">Data synchronization</span></span>

<span data-ttu-id="20e18-124">다음 그림은 Project Service Automation과 Finance 간에 통합의 일부로 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="20e18-125">현재 모든 템플릿을 사용할 수 있는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-125">Not all templates are currently available.</span></span> <span data-ttu-id="20e18-126">템플릿이 완성되면 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="20e18-127">[![Project Service Automation과 Finance 통합](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="20e18-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="20e18-128">Finance 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="20e18-128">System requirements for Finance</span></span>

<span data-ttu-id="20e18-129">Project Service Automation와 Finance 통합 솔루션을 사용하려면 플랫폼 업데이트 12 이상이 포함된 Enterprise 버전 7.3을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="20e18-130">Project Service Automation 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="20e18-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="20e18-131">Project Service Automation과 Finance 통합 솔루션을 사용하려면 다음 구성 요소를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="20e18-132">Dynamics 365 Project Service Automation 버전 9.0.0.0 이상</span><span class="sxs-lookup"><span data-stu-id="20e18-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="20e18-133">Dynamics 365 Sales, 버전 1.14.0.0(v14) 이상을 위한 현금 잠재 기부자 솔루션</span><span class="sxs-lookup"><span data-stu-id="20e18-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="20e18-134">Dynamics 365 Project Service Automation 버전 1.0.0.0 이상용 Project Service Automation to Finance 솔루션</span><span class="sxs-lookup"><span data-stu-id="20e18-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="20e18-135">Project Service Automation 인스턴스에 Project Service Automation to Finance 통합 솔루션 설치</span><span class="sxs-lookup"><span data-stu-id="20e18-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="20e18-136">[Microsoft 다운로드 센터](https://www.microsoft.com/download/details.aspx?id=57016)에서 Project Service Automation to Finance 통합 솔루션을 다운로드하고 솔루션에 포함된 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="20e18-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]