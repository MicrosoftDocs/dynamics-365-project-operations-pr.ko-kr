---
title: Project Service Automation에서 Finance and Operations로 직접 프로젝트 추정치 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 시간 견적 및 프로젝트 경비 추정치를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753264"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ad5d0-103">Project Service Automation에서 Finance and Operations로 직접 프로젝트 추정치 동기화</span><span class="sxs-lookup"><span data-stu-id="ad5d0-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ad5d0-104">이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 시간 견적 및 프로젝트 경비 추정치를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ad5d0-105">프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="ad5d0-106">실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="ad5d0-107">Project Service Automation에서 Finance까지의 데이터 흐름</span><span class="sxs-lookup"><span data-stu-id="ad5d0-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="ad5d0-108">Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ad5d0-109">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 시간 추정 및 프로젝트 경비 추정에 대한 데이터 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ad5d0-110">다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ad5d0-111">[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="ad5d0-112">프로젝트 시간 추청치</span><span class="sxs-lookup"><span data-stu-id="ad5d0-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ad5d0-113">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="ad5d0-113">Template and tasks</span></span>

<span data-ttu-id="ad5d0-114">사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트**를 선택한 다음 오른쪽 상단에서 **새 프로젝트**를 선택하여 공개 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ad5d0-115">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 시간 추정치를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ad5d0-116">**데이터 통합의 템플릿 이름:** 프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ad5d0-117">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ad5d0-118">트랜잭션 관계</span><span class="sxs-lookup"><span data-stu-id="ad5d0-118">Transaction relationships</span></span>
    - <span data-ttu-id="ad5d0-119">경비 추정</span><span class="sxs-lookup"><span data-stu-id="ad5d0-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ad5d0-120">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="ad5d0-120">Entity set</span></span>

| <span data-ttu-id="ad5d0-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad5d0-121">Project Service Automation</span></span> | <span data-ttu-id="ad5d0-122">재무</span><span class="sxs-lookup"><span data-stu-id="ad5d0-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="ad5d0-123">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="ad5d0-123">Project tasks</span></span>              | <span data-ttu-id="ad5d0-124">프로젝트 시간 추정을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="ad5d0-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ad5d0-125">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="ad5d0-125">Entity flow</span></span>

<span data-ttu-id="ad5d0-126">프로젝트 시간 추정치는 Project Service Automation에서 관리되며 프로젝트 시간 예측으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ad5d0-127">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ad5d0-127">Prerequisites</span></span>

<span data-ttu-id="ad5d0-128">프로젝트 시간 추정치를 동기화하기 전에 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ad5d0-129">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="ad5d0-129">Power Query</span></span>

<span data-ttu-id="ad5d0-130">프로젝트 시간 예상 템플릿에서 Microsoft Excel용 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="ad5d0-131">통합이 새 시간 예측을 생성할 때 사용할 기본 예측 모델 ID를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ad5d0-132">시간 예측으로의 통합에 실패할 작업에서 리소스 별 레코드를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="ad5d0-133">빈 트랜잭션 범주 행을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="ad5d0-134">이 작업을 완료하지 못하면 시간 예측이 잘못될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ad5d0-135">기본 예측 모델 ID 설정</span><span class="sxs-lookup"><span data-stu-id="ad5d0-135">Set the default forecast model ID</span></span>

<span data-ttu-id="ad5d0-136">템플릿에서 기본 예측 모델 ID를 업데이트하려면 **매핑** 화살표를 클릭하여 매핑을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ad5d0-137">그런 다음 **고급 쿼리 및 필터링** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ad5d0-138">기본 프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 **적용 단계** 목록에서 **삽입된 조건**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="ad5d0-139">**함수** 항목에서 **O\_forecast**를 통합과 함께 사용해야 하는 예측 모델 ID의 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ad5d0-140">기본 템플릿에는 데모 데이터의 예측 모델 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ad5d0-141">새 템플릿을 만드는 경우 이 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ad5d0-142">파워 쿼리에서 **조건 열 추가**를 클릭하고 새 열의 이름(예: **ModelID**)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ad5d0-143">열에 대한 조건을 입력합니다. 여기서 프로젝트 작업이 null이 아닌 경우 \<예측 모델 ID를 입력하세요.\>, 그렇지 않으면 null입니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="ad5d0-144">리소스별 레코드 필터링</span><span class="sxs-lookup"><span data-stu-id="ad5d0-144">Filter out resource-specific records</span></span>

<span data-ttu-id="ad5d0-145">프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 리소스별 레코드를 제거하는 기본 필터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="ad5d0-146">고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ad5d0-147">**False**인 레코드만 포함되도록 **msdyn\_islinetask** 열에서 필터링할 **고급 쿼리 및 필터링** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="ad5d0-148">빈 트랜잭션 범주 행을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="ad5d0-149">트랜잭션 범주가 비어있는 행을 제거하려면 필터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="ad5d0-150">이 작업은 기본 템플릿을 사용하는지 또는 고유한 템플릿을 생성하는지에 관계없이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="ad5d0-151">이 필터는 Finance의 시간 예측이 잘못될 수 있는 모든 요약 행을 Project Service Automation에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="ad5d0-152">**고급 쿼리 및 필터링** 링크를 선택하여 **msdyn\_transactioncategory\_value** 열에서 null 레코드를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ad5d0-153">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="ad5d0-153">Template mapping in Data integration</span></span>

<span data-ttu-id="ad5d0-154">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ad5d0-155">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ad5d0-156">[![템플릿 매핑](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="ad5d0-157">프로젝트 경비 추정치</span><span class="sxs-lookup"><span data-stu-id="ad5d0-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ad5d0-158">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="ad5d0-158">Template and tasks</span></span>

<span data-ttu-id="ad5d0-159">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 경비 추정치를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ad5d0-160">**데이터 통합의 템플릿 이름:** 프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ad5d0-161">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ad5d0-162">트랜잭션 관계</span><span class="sxs-lookup"><span data-stu-id="ad5d0-162">Transaction relationships</span></span> 
    - <span data-ttu-id="ad5d0-163">경비 추정</span><span class="sxs-lookup"><span data-stu-id="ad5d0-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ad5d0-164">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="ad5d0-164">Entity set</span></span>

| <span data-ttu-id="ad5d0-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad5d0-165">Project Service Automation</span></span> | <span data-ttu-id="ad5d0-166">재무</span><span class="sxs-lookup"><span data-stu-id="ad5d0-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="ad5d0-167">거래 연결</span><span class="sxs-lookup"><span data-stu-id="ad5d0-167">Transaction Connections</span></span>    | <span data-ttu-id="ad5d0-168">프로젝트 트랜잭션 관계를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="ad5d0-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="ad5d0-169">추정 라인</span><span class="sxs-lookup"><span data-stu-id="ad5d0-169">Estimate Lines</span></span>             | <span data-ttu-id="ad5d0-170">프로젝트 경비 추정을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="ad5d0-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="ad5d0-171">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="ad5d0-171">Entity flow</span></span>

<span data-ttu-id="ad5d0-172">프로젝트 경비 추정치는 Project Service Automation에서 관리되며 프로젝트 경비 예측으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ad5d0-173">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ad5d0-173">Prerequisites</span></span>

<span data-ttu-id="ad5d0-174">프로젝트 경비 추정치를 동기화하기 전에 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ad5d0-175">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="ad5d0-175">Power Query</span></span>

<span data-ttu-id="ad5d0-176">프로젝트 경비 추정치 템플릿에서 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="ad5d0-177">경비 추정 라인 레코드만 포함하도록 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="ad5d0-178">통합이 새 시간 예측을 생성할 때 사용할 기본 예측 모델 ID를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ad5d0-179">청구 유형을 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-179">Transform the billing types.</span></span>
- <span data-ttu-id="ad5d0-180">트랜잭션 유형을 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="ad5d0-181">경비 추정 라인만 포함하도록 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="ad5d0-182">프로젝트 경비 추정(PSA에서 Fin 및 Ops까지) 템플릿에는 통합에 경비 라인만 포함하는 기본 필터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="ad5d0-183">고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ad5d0-184">**트랜잭션 관계** 작업을 선택한 다음 **매핑** 화살표를 클릭하여 매핑을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ad5d0-185">**고급 쿼리 및 필터링** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="ad5d0-186">**msdyn\_estimateline**만 포함하도록 **msdyn\_transactiontype1** 열을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ad5d0-187">기본 예측 모델 ID 설정</span><span class="sxs-lookup"><span data-stu-id="ad5d0-187">Set the default forecast model ID</span></span>

<span data-ttu-id="ad5d0-188">템플릿에서 기본 예측 모델 ID를 업데이트하려면 **경비 추정** 작업을 선택한 다음 **매핑** 화살표를 클릭하여 매핑을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ad5d0-189">**고급 쿼리 및 필터링** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ad5d0-190">기본 프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 파워 쿼리의 **적용 단계** 섹션에서 첫 번째 **삽입된 조건**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="ad5d0-191">**함수** 항목에서 **O\_forecast**를 통합과 함께 사용해야 하는 예측 모델 ID의 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ad5d0-192">기본 템플릿에는 데모 데이터의 예측 모델 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ad5d0-193">새 템플릿을 만드는 경우 이 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ad5d0-194">파워 쿼리에서 **조건 열 추가**를 클릭하고 새 열의 이름(예: **ModelID**)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ad5d0-195">열에 대한 조건을 입력합니다. 여기서 추정 라인 ID가 null이 아닌 경우 \<예측 모델 ID를 입력하세요.\>, 그렇지 않으면 null입니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="ad5d0-196">청구 유형을 변환합니다</span><span class="sxs-lookup"><span data-stu-id="ad5d0-196">Transform the billing types</span></span>

<span data-ttu-id="ad5d0-197">프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 통합 중에 Project Service Automation에서 받은 청구 유형을 변환하는 데 사용되는 조건부 열이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ad5d0-198">고유한 템플릿을 만드는 경우 이 조건부 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ad5d0-199">**고급 쿼리 및 필터링** 링크를 선택한 다음 **조건부 열 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ad5d0-200">새 열의 이름(**BillingType**)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="ad5d0-201">그런 후에, 다음 조건을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-201">Then enter the following condition:</span></span>

<span data-ttu-id="ad5d0-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="ad5d0-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="ad5d0-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="ad5d0-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="ad5d0-206">트랜잭션 유형을 변환합니다</span><span class="sxs-lookup"><span data-stu-id="ad5d0-206">Transform the transaction types</span></span>

<span data-ttu-id="ad5d0-207">프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 통합 중에 Project Service Automation에서 받은 트랜잭션 유형을 변환하는 데 사용되는 조건부 열이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ad5d0-208">고유한 템플릿을 만드는 경우 이 조건부 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ad5d0-209">**고급 쿼리 및 필터링** 링크를 선택한 다음 **조건부 열 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ad5d0-210">새 열의 이름(**TransactionType**)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="ad5d0-211">그런 후에, 다음 조건을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-211">Then enter the following condition:</span></span>

<span data-ttu-id="ad5d0-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="ad5d0-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="ad5d0-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="ad5d0-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ad5d0-215">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="ad5d0-215">Template mapping in Data integration</span></span>

<span data-ttu-id="ad5d0-216">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="ad5d0-217">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad5d0-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ad5d0-218">[![템플릿 매핑](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="ad5d0-219">[![템플릿 매핑](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ad5d0-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
