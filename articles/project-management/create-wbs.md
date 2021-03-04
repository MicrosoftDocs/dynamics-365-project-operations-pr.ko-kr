---
title: 작업 분할 구조 만들기
description: 이 토픽은 새 스케줄링 인터페이스의 기본 제어를 포함하는 WBS(작업 분할 구조)를 작성하는 방법을 설명합니다.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841367"
---
# <a name="create-a-work-breakdown-structure-wbs"></a><span data-ttu-id="581b8-103">작업 분할 구조(WBS) 만들기</span><span class="sxs-lookup"><span data-stu-id="581b8-103">Create a work breakdown structure (WBS)</span></span>

<span data-ttu-id="581b8-104">프로젝트 일정은 완료해야 할 작업, 그 작업을 수행할 리소스, 해당 작업 완료에 필요한 시간을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe in which the work must be completed.</span></span> <span data-ttu-id="581b8-105">일정은 제 때 납품하는 것에 관련된 모든 작업을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-105">The schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="581b8-106">Dynamics 365 Project Operations에서 다음과 같은 방법으로 프로젝트 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-106">In Dynamics 365 Project Operations, you create a project schedule by:</span></span>

  - <span data-ttu-id="581b8-107">작업을 관리할 수 있는 업무로 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-107">Breaking the work down into manageable tasks.</span></span>
  - <span data-ttu-id="581b8-108">각 작업을 수행하는 데 필요한 시간을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-108">Estimating the time that is required to do each task.</span></span>
  - <span data-ttu-id="581b8-109">작업 종속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-109">Setting task dependencies.</span></span>
  - <span data-ttu-id="581b8-110">작업 기간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-110">Setting task durations.</span></span>
  - <span data-ttu-id="581b8-111">작업을 수행할 일반 리소스를 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-111">Estimating the generic resources that will do the tasks.</span></span> 

<span data-ttu-id="581b8-112">프로젝트 일정은 **프로젝트** 페이지의 **일정** 탭에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-112">The project schedule is created on the **Schedule** tab on the **Project** page.</span></span>

## <a name="tasks"></a><span data-ttu-id="581b8-113">작업</span><span class="sxs-lookup"><span data-stu-id="581b8-113">Tasks</span></span>

<span data-ttu-id="581b8-114">프로젝트 일정을 만드는 첫 번째 단계는 작업을 관리 가능한 부분으로 나누는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-114">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="581b8-115">Project Operations의 일정은 다음과 같은 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-115">The schedule in Project Operations supports the following features:</span></span>

- <span data-ttu-id="581b8-116">요약 또는 컨테이너 업무</span><span class="sxs-lookup"><span data-stu-id="581b8-116">Summary or container tasks</span></span>
- <span data-ttu-id="581b8-117">리프 노드 업무</span><span class="sxs-lookup"><span data-stu-id="581b8-117">Leaf node tasks</span></span>

### <a name="summary-tasks"></a><span data-ttu-id="581b8-118">요약 작업</span><span class="sxs-lookup"><span data-stu-id="581b8-118">Summary tasks</span></span>

<span data-ttu-id="581b8-119">요약 작업은 다른 요약 작업이나 리프 노드 작업을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-119">Summary tasks can store other summary tasks or leaf node tasks.</span></span> <span data-ttu-id="581b8-120">자체적인 작업량이나 비용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-120">They have no work effort or cost of their own.</span></span> <span data-ttu-id="581b8-121">대신, 작업량과 비용은 컨테이너 작업의 작업 노력과 비용의 롤업입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-121">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="581b8-122">요약 작업의 시작 날짜는 컨테이너 작업의 시작 날짜이며 종료 날짜는 컨테이너 작업의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-122">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="581b8-123">요약 작업의 이름은 편집할 수 있지만 일정 속성(작업량, 날짜 및 기간 포함)은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-123">The name of a summary task can be edited, but scheduling properties, including effort, dates, and duration, can't be edited.</span></span> <span data-ttu-id="581b8-124">요약 작업을 삭제하면 모든 컨테이너 작업도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-124">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="581b8-125">리프 노드 업무</span><span class="sxs-lookup"><span data-stu-id="581b8-125">Leaf node tasks</span></span>

<span data-ttu-id="581b8-126">리프 노드 작업은 프로젝트에서 가장 세분화된 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-126">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="581b8-127">예상된 작업량, 리소스 수, 계획된 시작일과 종료일, 기간이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-127">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>

## <a name="create-a-task-hierarchy"></a><span data-ttu-id="581b8-128">작업 계층 구조 만들기</span><span class="sxs-lookup"><span data-stu-id="581b8-128">Create a task hierarchy</span></span>

### <a name="add-a-task"></a><span data-ttu-id="581b8-129">작업 추가</span><span class="sxs-lookup"><span data-stu-id="581b8-129">Add a task</span></span>

<span data-ttu-id="581b8-130">하나 이상의 작업을 추가하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-130">Complete the following steps to add one or more tasks.</span></span>

1. <span data-ttu-id="581b8-131">**프로젝트** 로 이동하고 일정을 만들 프로젝트 레코드를 선택하고 엽니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-131">Go to **Projects** and select and open the project record for which you want to create a schedule.</span></span> 
2. <span data-ttu-id="581b8-132">**작업** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-132">Select the **Tasks** tab.</span></span> 
3. <span data-ttu-id="581b8-133">**새 작업 추가** 를 선택하고 작업 이름을 입력한 다음 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-133">Select **Add new task**, enter a name for the task, and then press Enter.</span></span>
2. <span data-ttu-id="581b8-134">다른 작업 이름을 입력하고 전체 작업 목록이 표시될 때까지 Enter 키를 다시 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-134">Enter another task name and press Enter again until you have a full list of tasks.</span></span>

### <a name="manage-hierarchy-of-a-task"></a><span data-ttu-id="581b8-135">작업 계층 구조 관리</span><span class="sxs-lookup"><span data-stu-id="581b8-135">Manage hierarchy of a task</span></span>

<span data-ttu-id="581b8-136">작업이 들여쓰기되면 바로 위에 있는 작업의 하위가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-136">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="581b8-137">그런 다음 작업의 일정 ID가 다시 계산되어 새 사위의 일정 ID를 기반으로 하고 개요 번호 매기기 체계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-137">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="581b8-138">이제 상위 작업이 요약 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-138">The parent task is now a summary task.</span></span> <span data-ttu-id="581b8-139">따라서 하위 작업의 롤업이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-139">Therefore, it becomes a rollup of its child tasks.</span></span> <span data-ttu-id="581b8-140">작업 수준이 올라가면 더 이상 해당 상위였던 작업의 하위가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-140">When a task is promoted, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="581b8-141">그런 다음 작업 ID가 다시 계산되어 계층 구조에서 작업의 업데이트된 깊이와 위치를 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-141">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="581b8-142">이전 상위 작업의 작업량, 비용 및 날짜가 다시 계산되어 이 작업을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-142">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

<span data-ttu-id="581b8-143">작업을 들여쓰거나 수준을 올리려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-143">Complete the following steps to indent or promote a task.</span></span>

1. <span data-ttu-id="581b8-144">**프로젝트** 페이지의 **작업** 탭에 있는 **요약 작업** 에서 작업 이름 옆에 있는 세 개의 수직 점을 선택한 다음 **하위 작업 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-144">On the **Project** page, on the **Tasks** tab, under **Summary tasks**, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 
2. <span data-ttu-id="581b8-145">들여쓰거나 수준을 올리려는 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-145">Select the task to indent or promote.</span></span> <span data-ttu-id="581b8-146">둘 이상의 작업을 선택하려면 작업을 선택하고 Ctrl 키를 누른 상태에서 추가 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-146">To select more than one task, select a task, press and hold Ctrl, and then select additional tasks.</span></span>
2. <span data-ttu-id="581b8-147">**들여쓰기** 또는 **하위 작업 수준 올리기** 를 선택하여 요약 작업 아래로 이동하거나 작업을 꺼냅니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-147">Select **Indent** or **Promote subtask**  to move tasks under or out from under summary tasks.</span></span>

### <a name="move-tasks-up-and-down"></a><span data-ttu-id="581b8-148">작업을 위로 및 아래로 이동</span><span class="sxs-lookup"><span data-stu-id="581b8-148">Move tasks up and down</span></span>

<span data-ttu-id="581b8-149">작업은 다음 두 가지 방법 중 하나로 작업 분할 구조의 모든 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-149">Tasks can me moved to any level in the work breakdown structure in one of two ways:</span></span>

- <span data-ttu-id="581b8-150">작업을 하나 더 선택하고 원하는 위치로 끕니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-150">Select one more tasks and drag them to the desired location.</span></span>
- <span data-ttu-id="581b8-151">하나 이상의 작업을 선택하고 마우스 오른쪽 단추를 클릭한 다음 **잘라내기** 를 선택하고 일정에서 대상 셀을 선택한 다음 마우스 오른쪽 단추를 클릭하고 **붙여넣기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-151">Select one or more tasks, right-click and select **Cut**, select the destination cell in the schedule, and then right-click and select **Paste**.</span></span>

## <a name="task-attributes"></a><span data-ttu-id="581b8-152">업무 특성</span><span class="sxs-lookup"><span data-stu-id="581b8-152">Task attributes</span></span>

<span data-ttu-id="581b8-153">작업의 이름이 완료되어야 하는 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-153">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="581b8-154">Project Operations에서 작업과 연관된 특성은 작업의 일정과 인력 배치 요구 사항을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-154">In Project Operations, the attributes associated with a task describe the schedule of the task and its staffing requirements.</span></span>

## <a name="schedule-attributes"></a><span data-ttu-id="581b8-155">일정 특성</span><span class="sxs-lookup"><span data-stu-id="581b8-155">Schedule attributes</span></span>

<span data-ttu-id="581b8-156">**작업량**, **시작 날짜**, **종료 날짜** 및 **기간** 특성은 작업에 대한 일정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-156">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="581b8-157">다음 표는 추가 일정 특성을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-157">The following table shows additional schedule attributes.</span></span>

| <span data-ttu-id="581b8-158">**최종 표시 이름**</span><span class="sxs-lookup"><span data-stu-id="581b8-158">**Final display name**</span></span> | <span data-ttu-id="581b8-159">**최종 설명**</span><span class="sxs-lookup"><span data-stu-id="581b8-159">**Final description**</span></span> |
| --- | --- |
| <span data-ttu-id="581b8-160">완료된 작업량(시간)</span><span class="sxs-lookup"><span data-stu-id="581b8-160">Effort Completed (Hours)</span></span> | <span data-ttu-id="581b8-161">작업의 완료된 작업량(시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-161">Completed work for the task in hours.</span></span> |
| <span data-ttu-id="581b8-162">기간</span><span class="sxs-lookup"><span data-stu-id="581b8-162">Duration</span></span> | <span data-ttu-id="581b8-163">작업의 기간(일)을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-163">Displays the duration in days for the task.</span></span> |
| <span data-ttu-id="581b8-164">총 작업량</span><span class="sxs-lookup"><span data-stu-id="581b8-164">Total Effort</span></span> | <span data-ttu-id="581b8-165">작업의 총 작업량(시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-165">Total work for the task in hours.</span></span> |
| <span data-ttu-id="581b8-166">완료</span><span class="sxs-lookup"><span data-stu-id="581b8-166">Finish</span></span> | <span data-ttu-id="581b8-167">완료 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-167">Finish date and time.</span></span> |
| <span data-ttu-id="581b8-168">% 완료</span><span class="sxs-lookup"><span data-stu-id="581b8-168">% Complete</span></span> | <span data-ttu-id="581b8-169">작업의 완료율입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-169">The percentage of the task that is complete.</span></span> |
| <span data-ttu-id="581b8-170">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="581b8-170">Project Bucket</span></span> | <span data-ttu-id="581b8-171">버킷에 따라 작업 게시판을 그룹화할 수 있으므로 각 버킷마다 고유한 열이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-171">The task board can be grouped by bucket so each bucket has its own column.</span></span> |
| <span data-ttu-id="581b8-172">남은 작업량(시간)</span><span class="sxs-lookup"><span data-stu-id="581b8-172">Effort Remaining (Hours)</span></span> | <span data-ttu-id="581b8-173">작업의 남은 작업량(시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-173">The remaining work for the task in hours.</span></span> |
| <span data-ttu-id="581b8-174">시작</span><span class="sxs-lookup"><span data-stu-id="581b8-174">Start</span></span> | <span data-ttu-id="581b8-175">시작 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-175">Start date and time.</span></span> |
| <span data-ttu-id="581b8-176">이름</span><span class="sxs-lookup"><span data-stu-id="581b8-176">Name</span></span> | <span data-ttu-id="581b8-177">프로젝트 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-177">The name of the task.</span></span> |
| <span data-ttu-id="581b8-178">ID</span><span class="sxs-lookup"><span data-stu-id="581b8-178">ID</span></span> | <span data-ttu-id="581b8-179">작업 분할 구조에서 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-179">The ID of the task in the work breakdown structure.</span></span> |

## <a name="staffing-attributes"></a><span data-ttu-id="581b8-180">직원 구성 특성</span><span class="sxs-lookup"><span data-stu-id="581b8-180">Staffing attributes</span></span>

<span data-ttu-id="581b8-181">인력 배치 특성은 일정의 **리소스** 필드를 통해 액세스됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-181">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="581b8-182">기존 리소스를 검색하거나 **만들기** 를 선택하고 **빠른 만들기** 창에서 프로젝트 팀 구성원을 새 리소스로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-182">You can either search for an existing resource, or select **Create**, and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="581b8-183">**역할**, **리소스 단위** 및 **위치 이름** 필드는 작업에 대한 인력 지정 요구 사항을 설명하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-183">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="581b8-184">작업 일정과 함께 이러한 인력 특성은 이 작업을 수행하는 데 사용할 수 있는 리소스를 찾는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-184">These staffing attributes, together with the task schedule are used to find available resources to do this task.</span></span>

   - <span data-ttu-id="581b8-185">**역할**: 작업을 수행하는 데 필요한 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-185">**Role**: Specify the type of resource that is required to do the task.</span></span>
   - <span data-ttu-id="581b8-186">**리소스 단위**: 작업에 대한 리소스를 할당할 단위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-186">**Resourcing unit**: Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="581b8-187">이 특성은 리소스의 비용 및 청구 요금이 리소스 단위를 기반으로 설정된 경우 작업에 대한 비용 및 판매 예상값에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-187">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>
   - <span data-ttu-id="581b8-188">**위치 이름**: 궁극적으로 작업을 수행할 리소스의 자리 표시자 역할을 하는 일반 리소스에 대해 친숙한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-188">**Position name**: Enter a name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="581b8-189">**리소스** 필드에는 일반 리소스의 위치 이름이 있거나 리소스가 발견될 때 명명된 리소스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-189">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="581b8-190">**범주** 필드에는 작업을 그룹화할 수 있는 광범위한 작업 유형을 나타내는 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-190">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="581b8-191">이 필드는 일정이나 인력 배치에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-191">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="581b8-192">대신 이 필드는 보고용으로만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-192">Instead, the field is used only for reporting.</span></span>

## <a name="task-dependencies"></a><span data-ttu-id="581b8-193">업무 종속성</span><span class="sxs-lookup"><span data-stu-id="581b8-193">Task dependencies</span></span>

<span data-ttu-id="581b8-194">Project Operations에서 일정을 사용하여 작업 간에 선행 관계를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-194">You can use the schedule in Project Operations to create predecessor relationships between tasks.</span></span> <span data-ttu-id="581b8-195">**선행자** 필드는 작업이 종속된 작업을 나타내기 위해 하나 이상의 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-195">The **Predecessor** field uses one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="581b8-196">선행 값이 작업에 할당될 때 모든 선행 작업이 완료되어야 해당 작업을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-196">When predecessor values are assigned to a task, the task can start only after all of the predecessor tasks have been completed.</span></span> <span data-ttu-id="581b8-197">종속성으로 인해 작업의 계획된 시작 날짜는 선행 작업 완료 날짜로 재설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-197">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="581b8-198">작업 모드는 선행/종속 작업의 시작 및 종료 날짜에 대한 업데이트에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-198">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="581b8-199">내게 필요한 옵션 및 바로 가기 키</span><span class="sxs-lookup"><span data-stu-id="581b8-199">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="581b8-200">**일정** 표는 완전히 액세스할 수 있으며 내레이터, JAWS 또는 NVDA와 같은 화면 판독기에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-200">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="581b8-201">화살표 키(Microsoft Excel에서와 같이)를 사용하여 표 영역을 이동할 수 있으며 탭 키를 사용하여 대화형 사용자 인터페이스 요소를 진행할 수 있으며 아래쪽 화살표 키, Enter 키 또는 스페이스바를 사용하여 드롭다운 메뉴를 선택하고 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="581b8-201">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive user interface elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and open the drop-down menus.</span></span>
