---
title: 프로젝트 작업량 추적
description: 이 항목은 프로젝트 노력 및 작업 진행 상황을 추적하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 6fe381470326fc4000a9ed096b91fde56c045c38
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369204"
---
# <a name="project-effort-tracking"></a><span data-ttu-id="55fee-103">프로젝트 작업량 추적</span><span class="sxs-lookup"><span data-stu-id="55fee-103">Project effort tracking</span></span>

<span data-ttu-id="55fee-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="55fee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55fee-105">일정에 대한 진행 상황을 추적할 필요성은 업계에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="55fee-106">일부 산업은 세분화된 수준에서 추적하는 반면 다른 산업은 더 높은 수준에서 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="55fee-107">이 주제는 조직의 요구 사항을 충족하기 위해 예약하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="55fee-108">작업량 추적 보기</span><span class="sxs-lookup"><span data-stu-id="55fee-108">Effort tracking view</span></span>

<span data-ttu-id="55fee-109">**작업량 추적** 보기는 작업에 소요된 실제 작업 시간을 작업의 계획된 작업 시간과 비교하여 일정의 작업 진행 상황을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="55fee-110">Dynamics 365 Project Operations는 다음 수식을 사용하여 추적 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="55fee-111">**진행률 비율**: 현재까지 사용된 실제 작업량 ÷ 작업 완료 시 추정 비용(EAC)</span><span class="sxs-lookup"><span data-stu-id="55fee-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="55fee-112">**남은 작업량**: 완료 시 추정 작업량 - 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="55fee-112">**Remaining Effort**: Estimated effort at complete – Actual effort spent to date</span></span> 
- <span data-ttu-id="55fee-113">**EAC**: 남은 작업량 + 현재까지 사용된 실제 작업량</span><span class="sxs-lookup"><span data-stu-id="55fee-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="55fee-114">**예상 노력 분산**: 계획된 작업량 – EAC</span><span class="sxs-lookup"><span data-stu-id="55fee-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="55fee-115">Project Operations는 작업에 대한 작업량 차이를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="55fee-116">EAC가 계획된 작업량보다 더 많은 경우 작업이 원래 계획한 것보다 더 많은 시간이 소요되고 일정이 늦어질 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="55fee-117">EAC가 계획된 작업량보다 더 적은 경우 작업이 원래 계획한 것보다 더 적은 시간이 소요되고 일정이 앞당겨질 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort-on-leaf-node-tasks"></a><span data-ttu-id="55fee-118">리프 노드 작업에 대한 작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="55fee-118">Reprojecting effort on leaf node tasks</span></span>

<span data-ttu-id="55fee-119">프로젝트 관리자는 종종 작업에 대한 원래 예상을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="55fee-120">프로젝트 재추정은 프로젝트의 현재 상태를 고려할 때 프로젝트 관리자의 예상에 대한 인식입니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="55fee-121">그러나 프로젝트 관리자가 계획된 작업량을 변경하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-121">However, we don't recommend that project managers change the planned effort numbers.</span></span> <span data-ttu-id="55fee-122">이는 프로젝트 계획된 작업량이 프로젝트 일정 및 비용 추정에 대해 확립된 진실의 출처를 나타내며 모든 프로젝트 이해 관계자가 이에 동의했기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-122">This is because the project planned effort represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="55fee-123">프로젝트 관리자는 기본값 **남은 작업량** 을 작업에 대한 새로운 추정으로 업데이트하여 작업에 대한 작업량을 다시 추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-123">A project manager can reproject effort on tasks by updating the default **Remaining Effort** with a new estimate on the task.</span></span> <span data-ttu-id="55fee-124">이 업데이트로 인해 작업의 EAC(완료 시 추정), 진행률 및 작업에 대한 예상 작업량 차이가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-124">This update causes a recalculation of the task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="55fee-125">요약 작업에 대한 EAC, ETC 및 진행률 비율도 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-125">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="55fee-126">요약 작업에 대한 작업량 재추정</span><span class="sxs-lookup"><span data-stu-id="55fee-126">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="55fee-127">요약 작업 또는 컨테이너 작업에 대한 작업량을 재추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-127">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="55fee-128">프로젝트 관리자는 요약 작업에 대한 나머지 작업량을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-128">Project managers can update remaining effort on the summary tasks.</span></span> <span data-ttu-id="55fee-129">나머지 작업량을 업데이트하면 애플리케이션에서 다음과 같은 계산 세트가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-129">Updating the remaining effort triggers the following set of calculations in the application:</span></span>

- <span data-ttu-id="55fee-130">EAC 및 작업의 진행률이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-130">The EAC and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="55fee-131">새 EAC는 원래 EAC가 작업에 있던 것과 동일한 비율로 하위 작업에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-131">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="55fee-132">리프 노드 작업에 이르기까지 각 개별 작업에 대한 새 EAC가 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-132">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="55fee-133">리프 노드까지 영향을 받는 하위 작업에는 EAC 값에 따라 남은 작업량 및 진행률이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-133">The affected child tasks down to the leaf nodes have their remaining effort and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="55fee-134">이렇게 하면 작업의 작업량 차이에 대해 새 추정이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-134">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="55fee-135">루트 노드까지의 요약 작업의 EAC가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-135">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>


## <a name="project-status-summary"></a><span data-ttu-id="55fee-136">프로젝트 상태 요약</span><span class="sxs-lookup"><span data-stu-id="55fee-136">Project status summary</span></span>

<span data-ttu-id="55fee-137">**작업량 추적** 및 **비용 추적** 보기의 데이터를 추적하면 프로젝트 루트 노드, 요약 작업 및 리프 노드 작업 수준에서 진행률 및 비용 소비가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-137">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="55fee-138">**프로젝트 엔터티** 페이지의 **상태** 섹션에는 프로젝트 수준 상태 요약이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-138">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="55fee-139">상태 요약 필드</span><span class="sxs-lookup"><span data-stu-id="55fee-139">Status summary fields</span></span>

<span data-ttu-id="55fee-140">**전체 프로젝트 상태** 필드는 프로젝트의 전체 상태를 표시하는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-140">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="55fee-141">녹색, 노란색 및 빨간색과 같은 색상 코딩을 사용하여 위험 증가를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-141">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="55fee-142">**주석** 필드를 사용하면 프로젝트 관리자가 상태에 대한 특정 주석을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-142">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="55fee-143">**필드에 업데이트된 상태** 는 편집할 수 없으며 값은 상태가 마지막으로 업데이트된 시기를 나타내는 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-143">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="55fee-144">**일정 성능** 및 **비용 성능** 필드는 추적 날짜부터 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-144">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="55fee-145">**작업량 추적** 보기에서 루트 노드의 일정 및 비용 차이가 양수인 경우 이러한 필드를 **선행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-145">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="55fee-146">루트 노드의 일정 및 비용 차이가 음수인 경우 **후행** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55fee-146">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
