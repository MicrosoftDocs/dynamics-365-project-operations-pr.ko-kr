---
title: Finance and Operations 및 Project Service Automation 간에 프로젝트 비용 범주 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Finance 및 Dynamics 365 Project Service Automation 간에 프로젝트 경비 범주를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999859"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="9b216-103">Finance and Operations 및 Project Service Automation 간에 프로젝트 비용 범주 동기화</span><span class="sxs-lookup"><span data-stu-id="9b216-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9b216-104">이 항목에서는 Dynamics 365 Finance 및 Dynamics 365 Project Service Automation 간에 프로젝트 경비 범주를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="9b216-105">프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="9b216-106">실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="9b216-107">KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="9b216-108">회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="9b216-109">Project Service Automation 및 Finance를 위한 데이터 흐름</span><span class="sxs-lookup"><span data-stu-id="9b216-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="9b216-110">Project Service Automation 및 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="9b216-111">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Finance와 Project Service Automation 간에 프로젝트 경비 트랜잭션 범주에 대한 데이터 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="9b216-112">프로젝트 경비 범주가 Finance에서 마스터되는 경우 통합 흐름은 먼저 Finance에서 Project Service Automation으로 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="9b216-113">그런 다음 Project Service Automation에서 Finance 로의 동기화를 통해 프로젝트 경비 범주의 통합 ID가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="9b216-114">프로젝트 경비 범주가 Project Service Automation에서 마스터되는 경우 통합 흐름은 먼저 Project Service Automation에서 Finance로 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="9b216-115">프로젝트 범주는 Project Service Automation에서 동기화하기 전에 Finance에 이미 구성되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="9b216-116">그런 다음 Finance에서 Project Service Automation으로 다시 동기화한 다음 Project Service Automation에서 Finance로 다시 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="9b216-117">이러한 방식으로 범주가 연결되고 중복이 생성되지 않도록 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="9b216-118">일반적으로 프로젝트 경비 범주는 Finance에서 마스터됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="9b216-119">그러나 그렇지 않거나 Project Service Automation에서 경비 범주가 이미 생성된 경우 먼저 프로젝트 경비 트랜잭션 범주(PSA에서 Fin 및 Ops로) 템플릿을 사용하여 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="9b216-120">그런 다음 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿을 사용하여 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="9b216-121">그런 다음 Project Service Automation에서 Finance로 동기화를 한 번 더 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="9b216-122">Project Service Automation에서 먼저 동기화하는 경우 동기화를 실행하기 전에 Finance에서 다음 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="9b216-123">Project Service Automation에서 설정된 프로젝트 범주와 일치하는 공유 범주가 있어야 하며 **프로젝트** 와 **경비** 두 범주 모두에 대해 활성화되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="9b216-124">통합해야 하는 각 Finance 법인에 대해 다음 프로젝트 범주가 존재해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="9b216-125">**프로젝트 범주** 가 존재합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="9b216-126">**경비에 사용** 이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="9b216-127">**저널에서 활성화** 가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="9b216-128">**트랜잭션 유형** 이 **경비** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="9b216-129">다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="9b216-130">[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="9b216-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="9b216-131">Finance에서 Project Service Automation으로의 프로젝트 경비 범주 동기화</span><span class="sxs-lookup"><span data-stu-id="9b216-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="9b216-132">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="9b216-132">Template and task</span></span>

<span data-ttu-id="9b216-133">템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9b216-134">다음 템플릿 및 기본 작업은 Finance에서 Project Service Automation으로 프로젝트 경비 범주를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="9b216-135">**데이터 통합의 템플릿 이름:** 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로)</span><span class="sxs-lookup"><span data-stu-id="9b216-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="9b216-136">**프로젝트의 작업 이름:** 범주를 PSA에 동기화</span><span class="sxs-lookup"><span data-stu-id="9b216-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="9b216-137">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="9b216-137">Entity set</span></span>

| <span data-ttu-id="9b216-138">재무</span><span class="sxs-lookup"><span data-stu-id="9b216-138">Finance</span></span>                           | <span data-ttu-id="9b216-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9b216-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="9b216-140">범주를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="9b216-140">Integration entity for categories</span></span> | <span data-ttu-id="9b216-141">트랜잭션 범주</span><span class="sxs-lookup"><span data-stu-id="9b216-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="9b216-142">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="9b216-142">Entity flow</span></span>

<span data-ttu-id="9b216-143">프로젝트 경비 범주는 Finance에서 관리되며 트랜잭션 범주로 Project Service Automation에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="9b216-144">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="9b216-144">Power Query</span></span>

<span data-ttu-id="9b216-145">Project Service Automation에 동기화할 때 Microsoft Excel용 파워 쿼리를 사용하여 트랜잭션 범주에 대한 청구 유형을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="9b216-146">프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿은 기본 열 및 매핑을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="9b216-147">고유한 템플릿을 만드는 경우 파워 쿼리에서 이 조건부 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="9b216-148">다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-148">Follow these steps.</span></span>

1. <span data-ttu-id="9b216-149">화살표를 클릭하여 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿에서 프로젝트 경비 범주 작업의 매핑을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="9b216-150">**고급 쿼리 및 필터링** 링크를 클릭하여 파워 쿼리를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="9b216-151">**조건부 열 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="9b216-152">새 열의 이름(**BillingType**)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="9b216-153">다음 조건을 입력합니다. **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="9b216-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="9b216-154">열에서 **확인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="9b216-155">매핑 페이지에서 이 새 열을 매핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="9b216-156">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="9b216-157">매핑은 Finance에서 Project Service Automation으로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="9b216-158">[![프로젝트 경비와 Project Service Automation 템플릿 매핑](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="9b216-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="9b216-159">Project Service Automation에서 Finance로의 프로젝트 경비 범주 동기화</span><span class="sxs-lookup"><span data-stu-id="9b216-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="9b216-160">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="9b216-160">Template and task</span></span>

<span data-ttu-id="9b216-161">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 경비 범주를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="9b216-162">**데이터 통합의 템플릿 이름:** 프로젝트 경비 트랜잭션 범주(PSA에서 Fin 및 Ops로)</span><span class="sxs-lookup"><span data-stu-id="9b216-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="9b216-163">**프로젝트의 작업 이름:** 범주를 Fin Ops에 동기화</span><span class="sxs-lookup"><span data-stu-id="9b216-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="9b216-164">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="9b216-164">Entity set</span></span>

| <span data-ttu-id="9b216-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9b216-165">Project Service Automation</span></span> | <span data-ttu-id="9b216-166">재무</span><span class="sxs-lookup"><span data-stu-id="9b216-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="9b216-167">트랜잭션 범주</span><span class="sxs-lookup"><span data-stu-id="9b216-167">Transaction categories</span></span>     | <span data-ttu-id="9b216-168">범주를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="9b216-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="9b216-169">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="9b216-169">Entity flow</span></span>

<span data-ttu-id="9b216-170">프로젝트 경비 범주는 Finance에서 관리되며 트랜잭션 범주로 Project Service Automation에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="9b216-171">Project Service Automation의 통합 ID를 사용하여 Finance로의 동기화가 다시 Finance에서 프로젝트 범주를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9b216-172">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="9b216-172">Template mapping in Data integration</span></span>

<span data-ttu-id="9b216-173">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="9b216-174">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b216-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="9b216-175">[![Project Service Automation과 Finance 템플릿 매핑](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="9b216-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]