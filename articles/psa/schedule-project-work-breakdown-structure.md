---
title: 작업 분할 구조로 프로젝트 일정 짜기
description: 작업 분할 구조로 프로젝트 일정을 짜는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127886"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="91b64-103">작업 분할 구조로 프로젝트 일정 짜기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="91b64-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="91b64-104">프로젝트 일정은 수행해야 할 작업, 그 작업을 수행할 리소스, 해당 작업 완료에 필요한 시간을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="91b64-105">프로젝트 일정은 제 때 납품하는 것에 관련된 모든 작업을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="91b64-106">프로젝트 시작 단계에서 처음 수행할 일 중 하나는 바로 프로젝트 일정을 짜는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="91b64-107">프로젝트 일정을 수립하려면, 작업 분할 구조를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="91b64-108">작업 분할 구조로 프로젝트 구조를 만들면 다음과 같은 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="91b64-109">작업을 관리할 수 있는 업무로 분할</span><span class="sxs-lookup"><span data-stu-id="91b64-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="91b64-110">업무를 완료하는 데 필요한 시간 예측</span><span class="sxs-lookup"><span data-stu-id="91b64-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="91b64-111">업무 기간 및 업무 의존도 설정</span><span class="sxs-lookup"><span data-stu-id="91b64-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="91b64-112">각 업무를 완료하는 데 필요한 역할 결정</span><span class="sxs-lookup"><span data-stu-id="91b64-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="91b64-113">작업 분할 구조의 프로젝트 일정은 대화식 Gantt 차트로 만들어 형태나 사용 면에서 익숙합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="91b64-114">프로젝트에 대한 작업 분할 구조 만들기</span><span class="sxs-lookup"><span data-stu-id="91b64-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="91b64-115">프로젝트에서 업무 순서를 나타낼 작업 분할 구조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="91b64-116">작업 분할 구조에는 업무, 각 업부에 대한 요구 사항, 수익 및 비용 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="91b64-117">작업 분할 구조에 다음을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="91b64-118">계층 구조에서의 업무 순서</span><span class="sxs-lookup"><span data-stu-id="91b64-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="91b64-119">시작 전에 완료해야 하는 다른 업무(있을 경우)</span><span class="sxs-lookup"><span data-stu-id="91b64-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="91b64-120">시작 날짜, 종료 날짜 및 업무 기간</span><span class="sxs-lookup"><span data-stu-id="91b64-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="91b64-121">업무에 필요한 시간</span><span class="sxs-lookup"><span data-stu-id="91b64-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="91b64-122">필요한 작업자 기술 및 교육</span><span class="sxs-lookup"><span data-stu-id="91b64-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="91b64-123">업무에 할당된 작업자</span><span class="sxs-lookup"><span data-stu-id="91b64-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="91b64-124">예상 수익 및 비용</span><span class="sxs-lookup"><span data-stu-id="91b64-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="91b64-125">작업 유형</span><span class="sxs-lookup"><span data-stu-id="91b64-125">Task types</span></span>  
<span data-ttu-id="91b64-126">작업 분할 구조 생성 시 다음 유형의 업무를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="91b64-127">**프로젝트의 루트 노드**</span><span class="sxs-lookup"><span data-stu-id="91b64-127">**Project root node**</span></span> | <span data-ttu-id="91b64-128">프로젝트에 대한 최상위 요약 업무</span><span class="sxs-lookup"><span data-stu-id="91b64-128">The top-level summary task for the project.</span></span> <span data-ttu-id="91b64-129">다른 모든 프로젝트 업무가 그 아래 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-129">All other project tasks are created under it.</span></span> <span data-ttu-id="91b64-130">루트 작업의 이름은 프로젝트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-130">The name of the root task is the project name.</span></span> <span data-ttu-id="91b64-131">루트 노드의 업무량, 날짜, 기간은 그 아래 계층의 값을 바탕으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="91b64-132">루트 노드를 삭제하거나 루트 노드의 속성을 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="91b64-133">**요약 또는 컨테이너 업무**</span><span class="sxs-lookup"><span data-stu-id="91b64-133">**Summary or container tasks**</span></span> | <span data-ttu-id="91b64-134">요약 업무는 그 아래에 하위 작업이 있는 업무입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="91b64-135">요약 업무는 작업량 또는 비용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="91b64-136">작업량과 비용은 하위 업무의 롤업입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="91b64-137">요약 업무의 이름을 변경할 수 있지만 업무량, 날짜, 기간은 자동으로 계산되므로 바꿀 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="91b64-138">요약 업무를 삭제하면 해당 업무와 하위 업무가 모두 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="91b64-139">**리프 노드 업무**</span><span class="sxs-lookup"><span data-stu-id="91b64-139">**Leaf node tasks**</span></span> | <span data-ttu-id="91b64-140">리프 노드 업무는 프로젝트에서 가장 분화된 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="91b64-141">예상된 작업량, 계획된 리소스 수, 계획된 시작일과 종료일, 기간이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="91b64-142">업무 계층 구조</span><span class="sxs-lookup"><span data-stu-id="91b64-142">Task hierarchy</span></span>  
 <span data-ttu-id="91b64-143">업무 계층 구조 생성에는 다음 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="91b64-144">**업무 추가**</span><span class="sxs-lookup"><span data-stu-id="91b64-144">**Add task**.</span></span>   <span data-ttu-id="91b64-145">업무 계층 구조에서 선택한 위치에 업무를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="91b64-146">위치를 선택하지 않으면 새 업무가 마지막에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="91b64-147">**업무 들여쓰기**</span><span class="sxs-lookup"><span data-stu-id="91b64-147">**Indent task**.</span></span>   <span data-ttu-id="91b64-148">바로 위에 있는 업무의 하위 업무를 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="91b64-149">**업무 내어쓰기**</span><span class="sxs-lookup"><span data-stu-id="91b64-149">**Outdent task**.</span></span>   <span data-ttu-id="91b64-150">업무를 내어쓰면 더 이상 원래 상위 업무의 하위 업무가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="91b64-151">**위로 이동 및 아래로 이동**</span><span class="sxs-lookup"><span data-stu-id="91b64-151">**Move up and Move down**.</span></span>   <span data-ttu-id="91b64-152">업무를 상위 업무의 계층 구조에서 아래로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="91b64-153">업무를 위나 아래로 이동해도 작업량, 비용, 날짜, 기간에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="91b64-154">업무 특성</span><span class="sxs-lookup"><span data-stu-id="91b64-154">Task attributes</span></span>  
 <span data-ttu-id="91b64-155">업무 이름이 완료되어야 하는 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="91b64-156">다양한 업무 특성을 사용하여 업무에 대한 일정 및 직원 구성 요구 사항을 설명할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="91b64-157">일정 특성</span><span class="sxs-lookup"><span data-stu-id="91b64-157">Schedule attributes</span></span>

 - <span data-ttu-id="91b64-158">**작업량(시간)**, **리소스 수**, **시작 날짜**, **종료 날짜**, **기간** 에 값을 할당하여 업무에 대한 일정을 정합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="91b64-159">**작업량** 은 업무 완료에 걸리는 시간의 추정치입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="91b64-160">**리소스 수** 는 프로젝트 관리자가 업무에 투입할 리소스의 추정치로 가능한 최상의 일정을 만드는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="91b64-161">**기간**(일별)은 업무 완료에 걸리는 작업일 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="91b64-162">직원 구성 특성</span><span class="sxs-lookup"><span data-stu-id="91b64-162">Staffing attributes</span></span>

 - <span data-ttu-id="91b64-163">**역할**, **리소스 조직 단위**, **리소스 수** 및 **리소스** 는 업무에 필요한 직원 구성을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="91b64-164">**역할** 은 업무 수행에 필요한 리소스 유형을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="91b64-165">**리소스 조직 단위** 는 해당 업무에 구성할 리소스의 조직 단위를 나타내며, 리소스에 대한 단위 판매 가격을 결정할 때 고려하는 사항이므로 업무의 비용 및 판매 추정치에 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="91b64-166">**리소스** 에는 포괄적 리소스 또는 명명된 리소스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="91b64-167">업무 종속성</span><span class="sxs-lookup"><span data-stu-id="91b64-167">Task dependencies</span></span>  
 <span data-ttu-id="91b64-168">작업 분할 구조에서 하나 이상의 업무 선행 관계를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="91b64-169">업무에 대한 선행자 필드에 대한 하나 이상의 값을 설정하여 종속될 업무를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="91b64-170">선행 값을 업무에 배정할 때 모든 선행 업무가 완료되어야 후속 업무를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="91b64-171">업무에 대한 종속성을 설정하면 모든 선행 업무의 최신 종료 시점으로 업무에 계획된 시작 날짜를 다시 계산하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="91b64-172">선행 업무가 일정에 미치는 영향은 업무에서 정의된 업무 모드로 제한되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="91b64-173">업무 모드</span><span class="sxs-lookup"><span data-stu-id="91b64-173">Task mode</span></span>  
 <span data-ttu-id="91b64-174">업무 모드는 리프 노드 업무 일정을 결정하는 중요한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="91b64-175">모든 업무에는 자동 일정 모드와 수동 일정 모드의 두 가지 업무 모드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="91b64-176">**자동 예약**.</span><span class="sxs-lookup"><span data-stu-id="91b64-176">**Auto scheduling**.</span></span>   <span data-ttu-id="91b64-177">업무 모드를 자동으로 예약으로 설정할 경우, 업무 일정 엔진이 다음 업무 특성에 대한 일정 규칙을 사용하여 업무에 대한 일정을 정합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="91b64-178">선행 업무</span><span class="sxs-lookup"><span data-stu-id="91b64-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="91b64-179">작업량</span><span class="sxs-lookup"><span data-stu-id="91b64-179">Effort</span></span>  
  
    -   <span data-ttu-id="91b64-180">리소스 수</span><span class="sxs-lookup"><span data-stu-id="91b64-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="91b64-181">시작 및 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="91b64-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="91b64-182">**내 예약 규칙**.</span><span class="sxs-lookup"><span data-stu-id="91b64-182">**Scheduling rules**.</span></span>   <span data-ttu-id="91b64-183">프로젝트의 일정 시작일에 대한 선행 업무가 없는 리프 노드 업무의 시작 날짜.</span><span class="sxs-lookup"><span data-stu-id="91b64-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="91b64-184">리프 노드 업무 기간은 항상 시작 및 종료 날짜 간의 작업일 수로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="91b64-185">업무 일정이 자동으로 설정되는 경우, 일정 엔진은 아래 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="91b64-186">업무 시작 및 종료 날짜는 반드시 프로젝트의 일정 관리 일정에 따른 작업일 수여야 함</span><span class="sxs-lookup"><span data-stu-id="91b64-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="91b64-187">선행 업무가 있는 경우, 선행 업무의 최종 날짜가 업무 시작 날짜</span><span class="sxs-lookup"><span data-stu-id="91b64-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="91b64-188">작업량 = 사용자 수 \* 기간 \* 프로젝트 일정의 표준 작업일의 시간</span><span class="sxs-lookup"><span data-stu-id="91b64-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="91b64-189">**일정 관리자**.</span><span class="sxs-lookup"><span data-stu-id="91b64-189">**Manual scheduling**.</span></span>   <span data-ttu-id="91b64-190">경우에 따라, 이러한 규칙을 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="91b64-191">이 경우 업무에 대한 업무 모드를 수동으로 일정을 수립하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="91b64-192">그러면 일정 엔진이 다른 일정 특성에 대한 값 계산을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="91b64-193">업무의 선행 업무 설정은 항상 종속 업무의 시작 날짜에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="91b64-194">작업 분할 구조 만들기</span><span class="sxs-lookup"><span data-stu-id="91b64-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="91b64-195">**Project Service > 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="91b64-196">작업을 원하는 프로젝트를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="91b64-197">화면 상단 표시줄에서 프로젝트 이름 옆의 아래로 향하는 화살표를 선택한 다음 작업 분할 구조를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="91b64-198">업무를 추가하려면 **업무 추가** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="91b64-199">업무에 대한 필드를 입력한 후 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="91b64-200">작업 분할 구조가 완성될 때까지 업무를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="91b64-201">작업 분할 구조를 생성하는 동안 다음을 수행하여 업무를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="91b64-202">업무를 선택하고 **들여쓰기** 를 클릭하여 다른 업무 아래로 이동하거나 내어쓰기를 클릭하여 내어 씁니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="91b64-203">업무를 선택하고 **위로 이동** 또는 **아래로 이동** 을 클릭하여 목록에서 위나 아래로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="91b64-204">**Gantt 숨기기** 를 클릭하여 Gantt 차트를 숨기고 다시 표시하려면 **Gantt 표시** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="91b64-205">**시간 조정** 의 Gantt 차트에 대한 기간을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="91b64-206">프로젝트의 팀 구성원에게 작업 분할 구조에서 지정한 역할을 추가하려면 **프로젝트 팀 생성** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="91b64-207">변경을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="91b64-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="91b64-208">참고 항목</span><span class="sxs-lookup"><span data-stu-id="91b64-208">See Also</span></span>  
 [<span data-ttu-id="91b64-209">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="91b64-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
