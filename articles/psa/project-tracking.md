---
title: 프로젝트 진행률 및 비용 소비율
description: 이 주제는 프로젝트 진행 상황과 비용 소비 추적에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283646"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="a71db-103">프로젝트 진행률 및 비용 소비율</span><span class="sxs-lookup"><span data-stu-id="a71db-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a71db-104">일정에 대한 진행 상황을 추적할 필요성은 업계에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="a71db-105">일부 산업은 세분화된 수준에서 추적하는 반면 다른 산업은 더 높은 수준에서 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="a71db-106">이 주제는 조직의 요구 사항을 충족하기 위해 예약하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="a71db-107">작업량 추적 보기</span><span class="sxs-lookup"><span data-stu-id="a71db-107">Effort tracking view</span></span>

<span data-ttu-id="a71db-108">**작업량 추적** 보기는 일정의 작업 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="a71db-109">작업에 들인 실제 작업 시간을 작업의 계획된 작업 시간과 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="a71db-110">Project Service Automation은 다음 수식을 사용하여 추적 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="a71db-111">작업 생성 초기: 계획된 비용은 완료시 예상 비용으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="a71db-112">작업에 실제가 기록되면 작업량에 대한 추적 보기에서 다음이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="a71db-113">진행률 비율 = 현재까지 사용된 실제 작업량 ÷ 작업 완료 시 추정 비용(EAC)</span><span class="sxs-lookup"><span data-stu-id="a71db-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="a71db-114">완료 예상(ETC) = 작업 완료 시 추정 비용(EAC) – 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="a71db-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="a71db-115">EAC = 남은 작업량 + 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="a71db-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="a71db-116">예상 노력 분산 = 계획된 작업량 – EAC</span><span class="sxs-lookup"><span data-stu-id="a71db-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="a71db-117">Project Service Automation은 작업에 대한 작업량 차이를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="a71db-118">EAC가 계획된 작업량보다 더 많은 경우 작업이 원래 계획한 것보다 더 많은 시간이 소요될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="a71db-119">따라서 일정이 늦어진 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="a71db-120">EAC가 계획된 작업량보다 더 적은 경우 작업이 원래 계획한 것보다 더 적은 시간이 소요될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="a71db-121">따라서 일정이 앞당겨진 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="a71db-122">작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="a71db-122">Reprojecting effort</span></span>

<span data-ttu-id="a71db-123">프로젝트 관리자는 작업에 대한 원래 예상을 수정하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="a71db-124">프로젝트 재추정은 프로젝트의 현재 상태를 고려할 때 프로젝트 관리자의 예상에 대한 인식입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="a71db-125">하지만, 프로젝트 관리자가 기본 수치를 변경하는 것은 권장하지 않습니다. 프로젝트 기본 수치는 프로젝트의 일정 및 비용에 대해 구비된 실제 자원이며, 모든 프로젝트 이해 관계자가 동의했기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="a71db-126">프로젝트 관리자가 작업에 대한 작업량을 다시 프로젝트할 수 있는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="a71db-127">작업에 실제 남은 작업량의 새 예상값으로 기본 ETC를 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="a71db-128">작업의 실제 진행률의 새 예상값으로 기본 진행률을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="a71db-129">이러한 각 접근 방식은 작업의 ETC, EAC 및 진행률을 다시 계산하고 작업에 추정된 작업량 차이를 발생하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a71db-130">요약 작업에 대한 EAC, ETC 및 진행률 비율도 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="a71db-131">요약 작업에 대한 작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="a71db-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="a71db-132">요약 작업 또는 컨테이너 작업에 대한 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="a71db-133">사용자가 나머지 작업또는 요약 작업의 진행률을 사용하여 다시 프로젝트를 수행하든 관계없이 다음 계산 집합이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="a71db-134">EAC, ETC 및 작업의 진행률이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="a71db-135">새 EAC는 원래 EAC가 작업에 있던 것과 동일한 비율로 하위 작업에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="a71db-136">리프 노드 작업에 이르기까지 각 개별 작업에 대한 새 EAC가 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="a71db-137">리프 노드까지 영향을 받는 하위 작업에는 EAC 값에 따라 ETC 및 진행률이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="a71db-138">이렇게 하면 작업의 작업량 차이에 대해 새 추정이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="a71db-139">루트 노드까지의 요약 작업의 EAC가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="a71db-140">비용 추적 보기</span><span class="sxs-lookup"><span data-stu-id="a71db-140">Cost tracking view</span></span> 

<span data-ttu-id="a71db-141">**비용 추적** 보기는 작업에 소요된 실제 비용을 계획된 비용과 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="a71db-142">이 보기는 인건비만 표시하며 경비 예상의 비용은 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="a71db-143">Project Service Automation은 다음 수식을 사용하여 추적 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="a71db-144">작업이 생성되면 계획된 비용은 완료시 예상 비용과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="a71db-145">작업에 실제가 기록되면 비용에 대한 **추적** 보기에서 다음이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="a71db-146">사용된 비용의 백분율 = 현재까지 사용된 실제 비용 ÷ 작업에 대한 완료시 예상 비용</span><span class="sxs-lookup"><span data-stu-id="a71db-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="a71db-147">완료 비용(CTC) = 완료시 예상 비용 – 현재까지 사용된 실제 비용</span><span class="sxs-lookup"><span data-stu-id="a71db-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="a71db-148">완료시 예상 비용 = CTC + 현재까지 사용된 실제 비용</span><span class="sxs-lookup"><span data-stu-id="a71db-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="a71db-149">예상 비용 차이 = 계획 비용 – 완료시 예상 비용</span><span class="sxs-lookup"><span data-stu-id="a71db-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="a71db-150">비용 차이의 추정이 작업에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="a71db-151">완료 시 예상 비용이 계획된 비용보다 더 많은 경우 작업이 원래 계획한 것보다 더 많이 소요될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="a71db-152">따라서 예산을 초과하는 추세입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="a71db-153">완료 시 예상 비용이 계획된 비용보다 더 적은 경우 작업이 원래 계획한 것보다 더 적게 소요될 것으로 예상되며 예산을 초과하지 않는 추세입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="a71db-154">프로젝트 관리자의 비용 재추정</span><span class="sxs-lookup"><span data-stu-id="a71db-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="a71db-155">작업량이 재추정되면 CTC, 완료 시 예상 비용, 소비된 비용의 백분율 및 추정 비용 차이가 모두 **비용 추적** 보기에서 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="a71db-156">프로젝트 상태 요약</span><span class="sxs-lookup"><span data-stu-id="a71db-156">Project status summary</span></span>

<span data-ttu-id="a71db-157">**작업량 추적** 및 **비용 추적** 보기의 데이터를 추적하면 프로젝트 루트 노드, 요약 작업 및 리프 노드 작업 수준에서 진행률 및 비용 소비가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="a71db-158">**프로젝트 엔터티** 페이지의 **상태** 섹션에는 프로젝트 수준 상태 요약이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="a71db-159">상태 요약 필드</span><span class="sxs-lookup"><span data-stu-id="a71db-159">Status summary fields</span></span>

<span data-ttu-id="a71db-160">**전체 프로젝트 상태** 필드는 프로젝트의 전체 상태를 표시하는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="a71db-161">녹색, 노란색 및 빨간색과 같은 색상 코딩을 사용하여 위험 증가를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="a71db-162">**주석** 필드를 사용하면 프로젝트 관리자가 상태에 대한 특정 주석을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="a71db-163">**필드에 업데이트된 상태** 는 편집할 수 없으며 값은 상태가 마지막으로 업데이트된 시기를 나타내는 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="a71db-164">**일정 성능** 및 **비용 성능** 필드는 추적 날짜부터 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="a71db-165">**작업량 추적** 보기에서 루트 노드의 일정 및 비용 차이가 양수인 경우 이러한 필드를 **선행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="a71db-166">루트 노드의 일정 및 비용 차이가 음수인 경우 **후행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a71db-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]