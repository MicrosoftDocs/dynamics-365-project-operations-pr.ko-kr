---
title: Project Service Automation에서 Finance and Operations로 직접 프로젝트 작업 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 작업을 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009984"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a3da9-103">Project Service Automation에서 Finance and Operations로 직접 프로젝트 작업 동기화</span><span class="sxs-lookup"><span data-stu-id="a3da9-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3da9-104">이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 작업을 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3da9-105">프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="a3da9-106">KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a3da9-107">회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="a3da9-108">실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a3da9-109">Project Service Automation에서 Finance까지의 데이터 흐름</span><span class="sxs-lookup"><span data-stu-id="a3da9-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a3da9-110">Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a3da9-111">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 작업에 대한 데이터 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a3da9-112">다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a3da9-113">[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a3da9-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a3da9-114">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="a3da9-114">Template and task</span></span>

<span data-ttu-id="a3da9-115">템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a3da9-116">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 작업을 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a3da9-117">**데이터 통합의 템플릿 이름:** 프로젝트 작업(PSA에서 Fin 및 Ops까지)</span><span class="sxs-lookup"><span data-stu-id="a3da9-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a3da9-118">**프로젝트에서 작업의 이름:** 프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="a3da9-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="a3da9-119">프로젝트 작업의 동기화가 발생하기 전에 프로젝트 계약 및 프로젝트를 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a3da9-120">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="a3da9-120">Entity set</span></span>

| <span data-ttu-id="a3da9-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3da9-121">Project Service Automation</span></span> | <span data-ttu-id="a3da9-122">재무</span><span class="sxs-lookup"><span data-stu-id="a3da9-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="a3da9-123">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="a3da9-123">Project Tasks</span></span>              | <span data-ttu-id="a3da9-124">프로젝트 작업을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="a3da9-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a3da9-125">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="a3da9-125">Entity flow</span></span>

<span data-ttu-id="a3da9-126">프로젝트 작업은 Project Service Automation에서 관리되며 프로젝트 활동으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a3da9-127">필수 조건 및 매핑 설정</span><span class="sxs-lookup"><span data-stu-id="a3da9-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="a3da9-128">프로젝트 작업의 동기화가 발생하기 전에 프로젝트 계약 및 프로젝트를 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="a3da9-129">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="a3da9-129">Power Query</span></span>

<span data-ttu-id="a3da9-130">이 조건이 충족되는 경우 데이터를 필터링하려면 Microsoft Excel용 파워 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="a3da9-131">프로젝트 작업에 리소스별 레코드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="a3da9-132">파워 쿼리를 사용해야 하는 경우 다음 지침을 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="a3da9-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="a3da9-133">프로젝트 작업(PSA에서 Fin 및 Ops로) 템플릿에는  **IsLineTask** 의 필터를 **False** 로 설정하여 프로젝트 작업에서 리소스 별 레코드를 제외하는 기본 필터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="a3da9-134">고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a3da9-135">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="a3da9-135">Template mapping in Data integration</span></span>

<span data-ttu-id="a3da9-136">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="a3da9-137">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3da9-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a3da9-138">[![템플릿 매핑](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="a3da9-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]