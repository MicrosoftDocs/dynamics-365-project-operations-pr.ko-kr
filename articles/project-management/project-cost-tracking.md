---
title: 프로젝트 비용 추적
description: 이 항목은 Project Operations가 프로젝트의 인건비 및 지출에 대한 진행 상황을 추적하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711064"
---
# <a name="labor-cost-tracking-on-projects"></a><span data-ttu-id="9a516-103">프로젝트에 대한 인건비 추적</span><span class="sxs-lookup"><span data-stu-id="9a516-103">Labor cost tracking on projects</span></span>

<span data-ttu-id="9a516-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="9a516-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a516-105">Dynamics 365 Project Operations는 프로젝트 계획에서 필요한 가장 낮은 단위로 노동 추정치 및 지출을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-105">Dynamics 365 Project Operations tracks labor estimates and spend at the lowest required granularity on the project plan.</span></span> <span data-ttu-id="9a516-106">인건비의 재무 추정은 계획된 작업량과 프로젝트 계획의 각 리프 노드 작업에 할당된 일반 또는 명명된 리소스를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-106">The financial estimate of labor cost is based on the planned effort and the generic or named resources that are assigned to each leaf-node task in the project plan.</span></span> <span data-ttu-id="9a516-107">프로젝트가 시작되고 사람들이 다양한 프로젝트 작업에 대한 시간을 보고하기 시작하면 실제 노동 지출이 요약되어 예상 계산이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-107">When the project begins and people start to report time on various project tasks, the actual spend on labor is summarized which starts a calculation of the projections.</span></span>

## <a name="labor-cost-tracking-view"></a><span data-ttu-id="9a516-108">인건비 추적 보기</span><span class="sxs-lookup"><span data-stu-id="9a516-108">Labor Cost Tracking view</span></span>

<span data-ttu-id="9a516-109">**프로젝트** 페이지의 **추적** 탭에서 **추적** > **비용** 을 선택하여 **비용 추적** 보기를 열고 프로젝트 계획의 각 작업에 대한 인건비 지출의 진행 상황을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-109">On the **Projects** page, on the **Tracking** tab, you can select **Tracking** > **Cost** to open the **Cost Tracking** view and see the progress of labor spend on each task in the project plan.</span></span> <span data-ttu-id="9a516-110">이 보기는 또한 작업에 소비된 실제 인건비를 작업의 계획된 인건비와 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-110">This view also compares the actual labor cost spent on a task to the task's planned labor cost.</span></span> <span data-ttu-id="9a516-111">Project Operations는 다음 공식을 사용하여 인건비 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-111">Project Operations uses the following formulas to calculate labor cost metrics:</span></span>

- <span data-ttu-id="9a516-112">**예정 비용**: 각 리프 노드 작업에 대한 모든 리소스 할당의 예상 비용</span><span class="sxs-lookup"><span data-stu-id="9a516-112">**Planned cost**: Estimated cost of all resource assignments on each leaf node task</span></span>
- <span data-ttu-id="9a516-113">**실제 비용**: 작업에 기록된 시간 동안 모든 비용의 합계</span><span class="sxs-lookup"><span data-stu-id="9a516-113">**Actual Cost**: Sum of all cost actuals for time recorded on the task</span></span>
- <span data-ttu-id="9a516-114">**비용 소비 비율**: 실제 비용 ÷ 완료시 예상 비용</span><span class="sxs-lookup"><span data-stu-id="9a516-114">**Cost consumption percentage**: Actual cost ÷ Cost estimate at complete</span></span>
- <span data-ttu-id="9a516-115">**남은 비용**: 완료시 예상 비용 - 실제 비용</span><span class="sxs-lookup"><span data-stu-id="9a516-115">**Remaining Cost**: Cost estimate at complete  – Actual cost</span></span>
- <span data-ttu-id="9a516-116">**완료 시 비용**: 남은 비용 + 실제 비용</span><span class="sxs-lookup"><span data-stu-id="9a516-116">**Cost at Complete**: Remaining cost + Actual cost</span></span>
- <span data-ttu-id="9a516-117">**비용 차이**: 예상 비용 - 완료시 예상 비용</span><span class="sxs-lookup"><span data-stu-id="9a516-117">**Cost variance**: Planned cost – Cost estimate at complete</span></span>

<span data-ttu-id="9a516-118">각 작업은 작업에 대한 비용 차이의 예측을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-118">Each task shows a projection of the cost variance on the task.</span></span> <span data-ttu-id="9a516-119">완료시 예상 비용이 계획된 비용보다 많으면 작업이 예산을 초과할 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-119">If the cost estimate at complete is more than the planned cost, the task is projected to go over budget.</span></span> <span data-ttu-id="9a516-120">완료시 예상 비용이 계획된 비용보다 적으면 작업이 예산 내에서 완료될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-120">If the cost estimate at complete is less than the planned cost, the task is projected to finish under budget.</span></span>

>[!NOTE]
> <span data-ttu-id="9a516-121">Project Operations **추적** 탭의 **프로젝트** 페이지에서만 인건비를 표시합니다. 재료 및 경비를 추정하고 소비를 추적할 수 있지만 이러한 비용은 **추적** 탭에 표시된 비용에 포함되지 않습니다. 이 탭은 작업량을 재추정하여 인건비를 재추정하는 경우에만 작동하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-121">Project Operations only shows labor costs on the **Project** page on the **Tracking** tab. While materials and expenses can be estimated and tracked for consumption, these costs are not included in the costs shown on the **Tracking** tab. This tab is designed to work only for reprojecting labor costs by reprojecting effort.</span></span>
<span data-ttu-id="9a516-122">표시된 모든 비용 금액은 비용 요금을 결정하는 데 사용된 프로젝트의 비용 가격 통화에서 프로젝트의 비용 통화로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-122">All cost amounts shown are converted to the project's cost currency from the project's cost price currency used to determine the cost rate.</span></span> <span data-ttu-id="9a516-123">프로젝트의 원가 통화는 프로젝트 계약 단위의 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-123">The cost currency of the project is the currency of the contracting unit on the project.</span></span> <span data-ttu-id="9a516-124">**프로젝트** 페이지의 **추정** 탭에 표시된 시간에 대한 추정 비용 값은 **추적** 탭의 계획 비용에 합산되지 않을 수 있습니다. 이러한 불일치의 이유는 예상 비용이 **추정** 그리드에 요약되는 방식과 **추적** 그리드에서 계획된 비용이 계산되는 방식의 차이 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-124">The estimated cost values for time that are shown on the **Estimates** tab on the **Project** page might not add up to the planned cost on the **Tracking** tab. The reason for this discrepancy is because of the differences in how estimated cost is summarized on the **Estimates** grid and how planned cost is calculated on the **Tracking** grid.</span></span> 
>
> - <span data-ttu-id="9a516-125">**추정 탭** 은 가격표에 있는 비용 요금과 동일한 통화를 사용하여 추정 비용을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-125">The **Estimates tab** calculates the estimated cost by using the same currency of the cost rate in the price list.</span></span> <span data-ttu-id="9a516-126">그런 다음 가격표 통화의 예상 비용이 프로젝트 비용 통화의 예상 비용으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-126">Then, the estimated cost in the price list currency is converted to the estimated cost in the project's cost currency.</span></span> <span data-ttu-id="9a516-127">프로젝트 통화의 추정 비용은 소수점 둘째 자리로 반올림하여 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-127">The estimated cost in the project currency is shown rounded to 2 decimal places.</span></span> <span data-ttu-id="9a516-128">이 변환 중에는 통화 정밀도가 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-128">At no point during this conversion is currency precision applied.</span></span> 
> - <span data-ttu-id="9a516-129">**추적** 탭에서 계획 비용 계산은 두 단계로 적용되는 통화 정밀도를 포함하는 약간 다른 계산 순서를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-129">On the **Tracking** tab, the planned cost calculation follows a slightly different calculation order that involves currency precision being applied in two stages:</span></span> 
   ><ol>
   ><li><span data-ttu-id="9a516-130">가격표 통화의 추정 비용이 기준 통화로 변환됩니다(변환 1).</span><span class="sxs-lookup"><span data-stu-id="9a516-130">The estimated cost amount in the price list currency is converted to the base currency (conversion 1).</span></span></li>
   ><li><span data-ttu-id="9a516-131">기준 통화의 추정 비용이 프로젝트 비용 통화로 변환됩니다(변환 2).</span><span class="sxs-lookup"><span data-stu-id="9a516-131">The estimated cost amount in the base currency is converted to the project cost currency (conversion 2).</span></span> </li>
   ></ol>
   ><span data-ttu-id="9a516-132">통화 정밀도는 두 단계 모두에 적용되어 추정 비용(**추정** 탭의 **시간 - 단계별** 보기)에서 약간 벗어나는 계획된 비용 (**추적** 탭)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-132">Currency precision is applied in both steps to get a planned cost (on the **Tracking** tab) that deviates slightly from the estimated cost (on the **Time - phased** view on the **Estimates** tab).</span></span> 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a><span data-ttu-id="9a516-133">리프 노드 작업에 대한 비용 재추정</span><span class="sxs-lookup"><span data-stu-id="9a516-133">Reprojecting costs on leaf node tasks</span></span>

<span data-ttu-id="9a516-134">리프 노드 작업에 대한 인건비는 **프로젝트** 페이지의 **추적** 탭에서 직접 재추정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-134">Labor costs on a leaf node task can't be directly reprojected on the **Tracking** tab on the **Project page**.</span></span> <span data-ttu-id="9a516-135">그러나 **작업량 추적** 보기를 사용하여 작업에 대한 나머지 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-135">However, you can use the **Effort Tracking** view to reproject the remaining effort on a task.</span></span> <span data-ttu-id="9a516-136">이로 인해 작업에 대한 나머지 비용이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-136">This causes a recalculation of the remaining cost on the task.</span></span> <span data-ttu-id="9a516-137">다음은 이것이 작동하는 방법에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-137">The following is a description of how this works.</span></span>

1. <span data-ttu-id="9a516-138">프로젝트 관리자는 **남은 작업량** 필드의 기본값을 작업에 대한 남은 작업량의 새로운 추정치로 업데이트하여 작업에 대한 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-138">A project manager can reproject effort on tasks by updating the default value in the **Remaining Effort** field with a new estimate of the remaining effort on the task.</span></span> <span data-ttu-id="9a516-139">재추정으로 인해 작업의 EAC(완료 시 추정 작업량), 진행률 및 작업에 대한 예상 작업량 차이가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-139">Reprojecting causes a recalculation of the task's effort estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="9a516-140">요약 작업에 대한 EAC, ETC(완료 시 추정) 및 진행률 비율도 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-140">The EAC, estimate to complete (ETC), and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="9a516-141">작업의 남은 작업량에 대한 새 값을 기반으로 시스템은 **비용 추적** 보기에서 남은 비용을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-141">Based on the new value for the remaining effort on the task, the system calculates the remaining cost on the **Cost Tracking** view.</span></span> <span data-ttu-id="9a516-142">남은 작업량을 기준으로 나머지 비용을 계산하기 위해 시스템은 먼저 작업에 대한 1시간 작업의 평균 비용을 예상 비용 또는 예상 작업량으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-142">To calculate the remaining cost based on the remaining effort, the system first calculates the average cost of one hour of effort on the task as planned cost or planned effort.</span></span> <span data-ttu-id="9a516-143">예상 비용은 작업에 대한 모든 리소스 할당 비용의 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-143">The planned cost is the sum of the cost of all resource assignments on the task.</span></span> <span data-ttu-id="9a516-144">시간당 평균 비용은 작업에 대한 새로 예상되는 나머지 작업량에 대한 나머지 비용을 계산하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-144">The average cost per hour is used to compute the remaining cost for the newly projected remaining effort on the task.</span></span>
3. <span data-ttu-id="9a516-145">완료시 비용과 리프 노드 작업에 대한 비용 소비 비율이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-145">The cost at complete and cost consumption percentage on the leaf-node task are re-calculated.</span></span>
4. <span data-ttu-id="9a516-146">요약 작업의 전체 값에서 루트 노드까지의 비용이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-146">The cost at complete value of the summary tasks all the way to the root node are recalculated.</span></span>

## <a name="reprojecting-costs-on-summary-tasks"></a><span data-ttu-id="9a516-147">요약 작업에 대한 비용 재추정</span><span class="sxs-lookup"><span data-stu-id="9a516-147">Reprojecting costs on summary tasks</span></span>

<span data-ttu-id="9a516-148">요약 작업 또는 컨테이너 작업에 대한 인건비를 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-148">You can reproject labor costs on summary tasks or container tasks.</span></span> <span data-ttu-id="9a516-149">그러나 **프로젝트** 페이지의 **추적** 탭에서 요약 프로젝트 작업에 대한 인건비를 직접 재추정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-149">However, you can't directly reproject labor cost on a summary project task on the **Tracking** tab on the **Project** page.</span></span> <span data-ttu-id="9a516-150">리프 노드 작업과 유사하게 요약 및 컨테이너 작업 재추정은 **작업량 추적** 보기를 사용하여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-150">Similar to leaf node tasks, reprojecting summary and container tasks can be done using the **Effort Tracking** view.</span></span> <span data-ttu-id="9a516-151">이 보기에서 요약 작업에 대한 나머지 수익을 다시 계산하여 요약 작업에 대한 나머지 비용을 재계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-151">In this view, you can reproject the remaining effort on a summary task causing a recalculation of the remaining cost on the summary task.</span></span> <span data-ttu-id="9a516-152">다음은 이것이 작동하는 방법에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-152">The following is a description of how this works.</span></span>

1. <span data-ttu-id="9a516-153">프로젝트 관리자는 남은 작업량의 기본값을 작업에 대한 새 추정값으로 업데이트하여 요약 작업에 대한 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-153">A project manager can reproject effort on summary tasks by updating the default value of the remaining effort with a new estimate on the task.</span></span> <span data-ttu-id="9a516-154">이 업데이트로 인해 요약 작업의 EAC(완료 시 추정), 진행률 및 작업에 대한 예상 작업량 차이가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-154">This update causes a recalculation of the summary task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="9a516-155">요약 작업에 대한 EAC, ETC 및 진행률 비율도 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-155">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="9a516-156">요약 작업의 남은 작업량에 대한 새 값을 기반으로 시스템은 **비용 추적** 보기에서 남은 비용을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-156">Based on the new value for remaining effort on the summary task, the system calculates the remaining cost on the **Cost Tracking** view.</span></span> <span data-ttu-id="9a516-157">남은 작업량을 기준으로 나머지 비용을 계산하기 위해 시스템은 먼저 요약 작업에 대한 1시간 작업의 평균 비용을 예상 비용 또는 예상 작업량으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-157">To calculate the remaining cost based on the remaining effort, the system first calculates the average cost of one hour of effort on the summary task as planned cost or planned effort.</span></span> <span data-ttu-id="9a516-158">시간당 평균 비용은 요약 작업에 대한 새로 예상되는 나머지 작업량에 대한 비용을 계산하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-158">The average cost per hour is used to calculate the cost of the newly projected remaining effort on the summary task.</span></span>
3. <span data-ttu-id="9a516-159">완료시 비용과 요약 작업에 대한 비용 소비 비율이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-159">The cost at complete and cost consumption percentage on the summary task are re-calculated.</span></span>
4. <span data-ttu-id="9a516-160">완료시 새 비용은 원래 예상 비용이 작업에 있었던 것과 동일한 비율로 하위 작업에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-160">The new cost at complete is distributed down to the child tasks in the same proportion as the original planned cost was on the task.</span></span>
5. <span data-ttu-id="9a516-161">리프 노드 작업까지 각 개별 작업에 대한 완료시 새로운 비용 값이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-161">The new cost at complete value on each of the individual tasks down to the leaf node tasks is calculated.</span></span> <span data-ttu-id="9a516-162">이 값을 기반으로 리프 노드까지 영향을 받는 하위 작업은 전체 값의 비용을 기반으로 나머지 비용 및 비용 소비 백분율을 다시 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-162">Based on this value, the affected child tasks down to the leaf nodes will have their remaining cost and cost consumption percentage recalculated based on the cost at complete value.</span></span> <span data-ttu-id="9a516-163">이 값을 사용하면 작업의 비용 차이에 대해 새 추정이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-163">This value results in a new projection for the cost variance of the task.</span></span> 


<span data-ttu-id="9a516-164">**비용 성능** 필드는 추적 데이터에서 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-164">The **Cost performance** field can be set from the tracking data.</span></span> <span data-ttu-id="9a516-165">**비용 추적** 보기에서 루트 노드의 비용 차이가 음수이면 이 필드를 **예산 부족** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-165">When the cost variance for the root node in the **Cost tracking** view is negative, you can set this field to **Under Budget**.</span></span> <span data-ttu-id="9a516-166">루트 노드에 대한 비용 차이가 양수이면 값을 **예산 초과** 로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a516-166">When the cost variance for the root node is positive, you can set the value to **Over Budget**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]