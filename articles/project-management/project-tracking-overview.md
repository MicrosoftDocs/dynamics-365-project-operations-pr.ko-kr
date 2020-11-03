---
title: 프로젝트 추적 개요
description: 이 주제는 프로젝트 진행 상황과 비용 소비를 추적하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079903"
---
# <a name="project-tracking-overview"></a><span data-ttu-id="cf20b-103">프로젝트 추적 개요</span><span class="sxs-lookup"><span data-stu-id="cf20b-103">Project tracking overview</span></span>

<span data-ttu-id="cf20b-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="cf20b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf20b-105">일정에 대한 진행 상황을 추적할 필요성은 업계에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="cf20b-106">일부 산업은 세분화된 수준에서 추적하는 반면 다른 산업은 더 높은 수준에서 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="cf20b-107">이 주제는 조직의 요구 사항을 충족하기 위해 예약하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="cf20b-108">작업량 추적 보기</span><span class="sxs-lookup"><span data-stu-id="cf20b-108">Effort tracking view</span></span>

<span data-ttu-id="cf20b-109">**작업량 추적** 보기는 작업에 소요된 실제 작업 시간을 작업의 계획된 작업 시간과 비교하여 일정의 작업 진행 상황을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="cf20b-110">Dynamics 365 Project Operations는 다음 수식을 사용하여 추적 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="cf20b-111">**진행률 비율** : 현재까지 사용된 실제 작업량 ÷ 작업 완료 시 추정 비용(EAC)</span><span class="sxs-lookup"><span data-stu-id="cf20b-111">**Progress percentage** : Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="cf20b-112">**완료 예상(ETC)** : 계획된 작업량 – 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="cf20b-112">**Estimate to complete (ETC)** : Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="cf20b-113">**EAC** : 남은 작업량 + 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="cf20b-113">**EAC** : Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="cf20b-114">**예상 노력 분산** : 계획된 작업량 – EAC</span><span class="sxs-lookup"><span data-stu-id="cf20b-114">**Projected effort variance** : Planned effort – EAC</span></span>

<span data-ttu-id="cf20b-115">Project Operations는 작업에 대한 작업량 차이를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="cf20b-116">EAC가 계획된 작업량보다 더 많은 경우 작업이 원래 계획한 것보다 더 많은 시간이 소요되고 일정이 늦어질 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="cf20b-117">EAC가 계획된 작업량보다 더 적은 경우 작업이 원래 계획한 것보다 더 적은 시간이 소요되고 일정이 앞당겨질 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="cf20b-118">작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="cf20b-118">Reprojecting effort</span></span>

<span data-ttu-id="cf20b-119">프로젝트 관리자는 종종 작업에 대한 원래 예상을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="cf20b-120">프로젝트 재추정은 프로젝트의 현재 상태를 고려할 때 프로젝트 관리자의 예상에 대한 인식입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="cf20b-121">하지만, 프로젝트 관리자가 기본 수치를 변경하는 것은 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-121">However, we don't recommend that project managers change the baseline numbers.</span></span> <span data-ttu-id="cf20b-122">그 이유는 프로젝트 기본 수치는 프로젝트의 일정 및 비용에 대해 구비된 실제 자원이며, 모든 프로젝트 이해 관계자가 동의했기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-122">This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="cf20b-123">프로젝트 관리자가 작업에 대한 작업량을 다시 프로젝트할 수 있는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-123">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="cf20b-124">작업에 실제 남은 작업량의 새 예상값으로 기본 ETC를 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-124">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="cf20b-125">작업의 실제 진행률의 새 예상값으로 기본 진행률을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-125">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="cf20b-126">각 접근 방식은 작업의 ETC, EAC 및 진행률을 다시 계산하고 작업에 추정된 작업량 차이를 발생하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-126">Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="cf20b-127">요약 작업에 대한 EAC, ETC 및 진행률 비율도 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-127">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="cf20b-128">요약 작업에 대한 작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="cf20b-128">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="cf20b-129">요약 작업 또는 컨테이너 작업에 대한 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-129">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="cf20b-130">사용자가 나머지 작업또는 요약 작업의 진행률을 사용하여 다시 프로젝트를 수행하든 관계없이 다음 계산 집합이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-130">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="cf20b-131">EAC, ETC 및 작업의 진행률이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-131">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="cf20b-132">새 EAC는 원래 EAC가 작업에 있던 것과 동일한 비율로 하위 작업에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-132">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="cf20b-133">리프 노드 작업에 이르기까지 각 개별 작업에 대한 새 EAC가 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-133">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="cf20b-134">리프 노드까지 영향을 받는 하위 작업에는 EAC 값에 따라 ETC 및 진행률이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-134">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="cf20b-135">이렇게 하면 작업의 작업량 차이에 대해 새 추정이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-135">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="cf20b-136">루트 노드까지의 요약 작업의 EAC가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-136">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="cf20b-137">비용 추적 보기</span><span class="sxs-lookup"><span data-stu-id="cf20b-137">Cost tracking view</span></span> 

<span data-ttu-id="cf20b-138">**비용 추적** 보기는 작업에 소요된 실제 비용을 작업의 계획된 비용과 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-138">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf20b-139">이 보기는 인건비만 표시하며 경비 예상의 비용은 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-139">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> <span data-ttu-id="cf20b-140">Project Operations는 다음 수식을 사용하여 추적 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-140">Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="cf20b-141">**사용된 비용의 백분율** : 현재까지 사용된 실제 비용 ÷ 완료시 예상 비용</span><span class="sxs-lookup"><span data-stu-id="cf20b-141">**Percentage of cost consumed** : Actual cost spent to date ÷ Estimated cost at completion</span></span>
- <span data-ttu-id="cf20b-142">**완료 비용(CTC)** : 계획된 비용 – 현재까지 사용된 실제 비용</span><span class="sxs-lookup"><span data-stu-id="cf20b-142">**Cost to complete (CTC)** : Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="cf20b-143">**EAC** : 남은 비용 + 현재까지 사용된 실제 비용</span><span class="sxs-lookup"><span data-stu-id="cf20b-143">**EAC** : Remaining cost + Actual cost spent to date</span></span>
- <span data-ttu-id="cf20b-144">**예상 비용 차이** : 계획된 비용 – EAC</span><span class="sxs-lookup"><span data-stu-id="cf20b-144">**Projected cost variance** : Planned cost – EAC</span></span>

<span data-ttu-id="cf20b-145">비용 차이의 추정이 작업에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-145">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="cf20b-146">EAC가 계획된 비용보다 더 많은 경우 작업이 원래 계획한 것보다 더 많이 소요될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-146">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="cf20b-147">따라서 예산을 초과하는 추세입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-147">Therefore, it's trending over budget.</span></span> <span data-ttu-id="cf20b-148">EAC가 계획된 비용보다 더 적은 경우 작업이 원래 계획한 것보다 더 적게 소요될 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-148">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="cf20b-149">따라서 예산을 초과하지 않는 추세입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-149">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="cf20b-150">프로젝트 관리자의 비용 재추정</span><span class="sxs-lookup"><span data-stu-id="cf20b-150">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="cf20b-151">작업량이 재추정되면 CTC, EAC, 소비된 비용의 백분율 및 추정 비용 차이가 모두 **비용 추적** 보기에서 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-151">When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="cf20b-152">프로젝트 상태 요약</span><span class="sxs-lookup"><span data-stu-id="cf20b-152">Project status summary</span></span>

<span data-ttu-id="cf20b-153">**작업량 추적** 및 **비용 추적** 보기의 데이터를 추적하면 프로젝트 루트 노드, 요약 작업 및 리프 노드 작업 수준에서 진행률 및 비용 소비가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-153">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="cf20b-154">**프로젝트 엔터티** 페이지의 **상태** 섹션에는 프로젝트 수준 상태 요약이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-154">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="cf20b-155">상태 요약 필드</span><span class="sxs-lookup"><span data-stu-id="cf20b-155">Status summary fields</span></span>

<span data-ttu-id="cf20b-156">**전체 프로젝트 상태** 필드는 프로젝트의 전체 상태를 표시하는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-156">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="cf20b-157">녹색, 노란색 및 빨간색과 같은 색상 코딩을 사용하여 위험 증가를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-157">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="cf20b-158">**주석** 필드를 사용하면 프로젝트 관리자가 상태에 대한 특정 주석을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-158">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="cf20b-159">**필드에 업데이트된 상태** 는 편집할 수 없으며 값은 상태가 마지막으로 업데이트된 시기를 나타내는 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-159">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="cf20b-160">**일정 성능** 및 **비용 성능** 필드는 추적 날짜부터 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-160">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="cf20b-161">**작업량 추적** 보기에서 루트 노드의 일정 및 비용 차이가 양수인 경우 이러한 필드를 **선행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-161">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="cf20b-162">루트 노드의 일정 및 비용 차이가 음수인 경우 **후행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20b-162">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
