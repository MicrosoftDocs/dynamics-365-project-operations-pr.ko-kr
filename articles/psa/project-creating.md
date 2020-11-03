---
title: 프로젝트 일정
description: 이 주제는 일정을 만드는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080087"
---
# <a name="project-schedules"></a><span data-ttu-id="be839-103">프로젝트 일정</span><span class="sxs-lookup"><span data-stu-id="be839-103">Project schedules</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="be839-104">프로젝트 일정은 완료해야 할 작업, 그 작업을 수행할 리소스, 해당 작업 완료에 필요한 시간을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="be839-105">제 때 납품하는 것에 관련된 모든 작업을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="be839-106">Dynamics 365 Project Service Automation에서 작업을 관리 가능한 작업으로 나누고, 각 작업을 수행하는 데 필요한 시간을 예측하고, 작업 종속성을 설정하고, 작업 기간을 설정하고, 작업을 수행할 일반 리소스를 예측하여 프로젝트 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be839-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="be839-107">프로젝트 일정은 프로젝트 페이지의 **일정** 탭에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="be839-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="be839-108">작업</span><span class="sxs-lookup"><span data-stu-id="be839-108">Tasks</span></span>

<span data-ttu-id="be839-109">프로젝트 일정을 만드는 첫 번째 단계는 작업을 관리 가능한 부분으로 나누는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="be839-110">PSA의 일정은 다음과 같은 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="be839-111">프로젝트의 루트 노드</span><span class="sxs-lookup"><span data-stu-id="be839-111">Project root node</span></span>
- <span data-ttu-id="be839-112">요약 또는 컨테이너 업무</span><span class="sxs-lookup"><span data-stu-id="be839-112">Summary or container tasks</span></span>
- <span data-ttu-id="be839-113">리프 노드 업무</span><span class="sxs-lookup"><span data-stu-id="be839-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="be839-114">프로젝트의 루트 노드</span><span class="sxs-lookup"><span data-stu-id="be839-114">Project root node</span></span>

<span data-ttu-id="be839-115">프로젝트 루트 노드는 프로젝트의 최상위 요약 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="be839-116">다른 모든 프로젝트 업무가 그 아래 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-116">All other project tasks are created under it.</span></span> <span data-ttu-id="be839-117">루트 노드의 이름은 항상 프로젝트 이름으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="be839-118">루트 노드의 업무량, 날짜, 기간은 그 아래 계층의 값을 바탕으로 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="be839-119">다음과 같은 루트 노드 속성들을 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="be839-120">루트 노드도 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="be839-121">요약 또는 컨테이너 업무</span><span class="sxs-lookup"><span data-stu-id="be839-121">Summary or container tasks</span></span> 

<span data-ttu-id="be839-122">요약 작업에는 하위 작업 또는 컨테이너 작업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="be839-123">자체적인 작업량이나 비용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="be839-124">대신, 작업량과 비용은 컨테이너 작업의 작업 노력과 비용의 롤업입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="be839-125">요약 작업의 시작 날짜는 컨테이너 작업의 시작 날짜이며 종료 날짜는 컨테이너 작업의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="be839-126">요약 작업의 이름은 편집할 수 있지만 일정 속성(작업량, 날짜 및 기간)은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="be839-127">요약 작업을 삭제하면 모든 컨테이너 작업도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="be839-128">리프 노드 업무</span><span class="sxs-lookup"><span data-stu-id="be839-128">Leaf node tasks</span></span>

<span data-ttu-id="be839-129">리프 노드 작업은 프로젝트에서 가장 세분화된 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be839-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="be839-130">예상된 작업량, 리소스 수, 계획된 시작일과 종료일, 기간이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="be839-131">작업 계층 구조 만들기</span><span class="sxs-lookup"><span data-stu-id="be839-131">Creating a task hierarchy</span></span>

<span data-ttu-id="be839-132">작업 계층 구조 생성에는 다음 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="be839-133">**작업 추가** 단추</span><span class="sxs-lookup"><span data-stu-id="be839-133">**Add task** button</span></span>
- <span data-ttu-id="be839-134">**들여쓰기 작업** 단추</span><span class="sxs-lookup"><span data-stu-id="be839-134">**Indent task** button</span></span>
- <span data-ttu-id="be839-135">**내어쓰기 작업** 단추</span><span class="sxs-lookup"><span data-stu-id="be839-135">**Outdent task** button</span></span>
- <span data-ttu-id="be839-136">**위로 이동** 및 **아래로 이동** 단추</span><span class="sxs-lookup"><span data-stu-id="be839-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="be839-137">내게 필요한 옵션 및 바로 가기 키</span><span class="sxs-lookup"><span data-stu-id="be839-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="be839-138">작업 추가</span><span class="sxs-lookup"><span data-stu-id="be839-138">Add task</span></span>

<span data-ttu-id="be839-139">**작업 추가** 단추를 사용하면 계층 구조에서 새 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="be839-140">위치를 선택하지 않으면 작업이 마지막에 삽입됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="be839-141">일정 ID는 모든 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="be839-142">일정 ID는 계층 구조에서 작업의 깊이와 위치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be839-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="be839-143">윤곽선 번호 매기기를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-143">It uses outline numbering.</span></span> <span data-ttu-id="be839-144">프로젝트 루트 노드 아래의 첫 번째 수준의 작업의 경우 1, 2, 3 등의 번호 매기기 방식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="be839-145">첫 번째 수준 아래 작업의 경우 1.1, 1.2, 1.3 등의 번호 매기기 방식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="be839-146">들여쓰기 작업</span><span class="sxs-lookup"><span data-stu-id="be839-146">Indent task</span></span>

<span data-ttu-id="be839-147">작업이 들여쓰기되면 바로 위에 있는 작업의 하위가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="be839-148">그런 다음 작업의 일정 ID가 다시 계산되어 새 사위의 일정 ID를 기반으로 하고 개요 번호 매기기 체계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="be839-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="be839-149">상위 작업은 이제 요약 작업 또는 컨테이너 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="be839-150">따라서 하위 작업의 롤업이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="be839-151">내어쓰기 작업</span><span class="sxs-lookup"><span data-stu-id="be839-151">Outdent task</span></span> 

<span data-ttu-id="be839-152">작업이 내어쓰기되면 더 이상 해당 상위였던 작업의 하위가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="be839-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="be839-153">그런 다음 작업 ID가 다시 계산되어 계층 구조에서 작업의 업데이트된 깊이와 위치를 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="be839-154">이전 상위 작업의 작업량, 비용 및 날짜가 다시 계산되어 이 작업을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="be839-155">위로 이동 및 아래로 이동</span><span class="sxs-lookup"><span data-stu-id="be839-155">Move up and Move down</span></span> 

<span data-ttu-id="be839-156">**위로 이동** 및 **아래로 이동** 단추는 상위 계층 구조 내에서 작업의 위치를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="be839-157">이 유형의 변경은 작업량, 비용, 날짜 또는 기간에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="be839-158">작업의 일정 ID만 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="be839-159">작업 ID가 다시 계산되어 하위 작업의 상위 목록에서 작업의 새 위치를 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="be839-160">내게 필요한 옵션 및 바로 가기 키</span><span class="sxs-lookup"><span data-stu-id="be839-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="be839-161">**일정** 표는 완전히 액세스할 수 있으며 내레이터, JAWS 또는 NVDA와 같은 화면 판독기에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="be839-162">화살표 키(Microsoft Excel에서와 같이)를 사용하여 표 영역을 이동할 수 있으며 탭 키를 사용하여 대화형 UI 요소를 진행할 수 있으며 아래쪽 화살표 키, Enter 키 또는 스페이스바를 사용하여 드롭다운 메뉴를 선택하고 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="be839-163">열 헤더도 대화형입니다.</span><span class="sxs-lookup"><span data-stu-id="be839-163">The column headers are also interactive.</span></span> <span data-ttu-id="be839-164">열을 숨기고 표시하고, 탭 키와 화살표 키를 사용하여 열 머리글을 이동하고, 도구 모음의 작업 단추를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="be839-165">또한, 다음 바로 가기 키를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="be839-166">**새로 고침** : ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="be839-166">**Refresh** : ALT+SHIFT+F5</span></span>
- <span data-ttu-id="be839-167">**추가** : ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="be839-167">**Add** : ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="be839-168">**삭제** : ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="be839-168">**Delete** : ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="be839-169">**위/아래로 이동** : ALT+SHIFT+위/아래 화살표</span><span class="sxs-lookup"><span data-stu-id="be839-169">**Move up/down** : ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="be839-170">**들여쓰기/내어쓰기** : ALT_SHIFT+왼쪽/오른쪽 화살표</span><span class="sxs-lookup"><span data-stu-id="be839-170">**Indent/Outdent** : ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="be839-171">**계층 확장/축소** : ALT+SHIFT+더하기/빼기 키</span><span class="sxs-lookup"><span data-stu-id="be839-171">**Expand/Collapse Hierarchies** : ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="be839-172">업무 특성</span><span class="sxs-lookup"><span data-stu-id="be839-172">Task attributes</span></span>

<span data-ttu-id="be839-173">작업의 이름이 완료되어야 하는 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="be839-174">PSA에서 작업과 연관된 특성은 작업의 일정과 인력 배치 요구 사항을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![업무 특성](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="be839-176">일정 특성</span><span class="sxs-lookup"><span data-stu-id="be839-176">Schedule attributes</span></span>

<span data-ttu-id="be839-177">**작업량** , **시작 날짜** , **종료 날짜** 및 **기간** 특성은 작업에 대한 일정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-177">The **Effort** , **Start date** , **End date** , and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="be839-178">추가 일정 특성은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="be839-179">**작업 시간** : 작업을 완료하는 데 필요한 예상 시간을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-179">**Effort hours** : Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="be839-180">**기간** : 작업을 완료하는 데 필요한 근무일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-180">**Duration** : Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="be839-181">**일정 ID** : 이 자동으로 생성된 ID는 계층 구조에서 작업을 주문하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-181">**Schedule ID** : This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="be839-182">작업 간의 종속성은 작업이 수행되는 실제 순서를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="be839-183">직원 구성 특성</span><span class="sxs-lookup"><span data-stu-id="be839-183">Staffing attributes</span></span>

<span data-ttu-id="be839-184">인력 배치 특성은 일정의 **리소스** 필드를 통해 액세스됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="be839-185">기존 리소스를 검색하거나 **만들기** 를 클릭하고 **빠른 만들기** 창에서 프로젝트 팀 구성원을 새 리소스로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="be839-186">**역할** , **리소스 단위** 및 **위치 이름** 필드는 작업에 대한 인력 지정 요구 사항을 설명하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-186">The **Role** , **Resourcing Unit** , and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="be839-187">작업 일정과 함께 이러한 인력 특성은 이 작업을 수행하는 데 사용할 수 있는 리소스를 찾는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="be839-188">**역할** - 작업을 수행하는 데 필요한 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="be839-189">**리소스 단위** - 작업에 대한 리소스를 할당할 단위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="be839-190">이 특성은 리소스의 비용 및 청구 요금이 리소스 단위를 기반으로 설정된 경우 작업에 대한 비용 및 판매 예상값에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be839-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="be839-191">**위치 이름** - 궁극적으로 작업을 수행할 리소스의 자리 표시자 역할을 하는 일반 리소스에 대해 친숙한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="be839-192">**리소스** 필드에는 일반 리소스의 위치 이름이 있거나 리소스가 발견될 때 명명된 리소스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="be839-193">**범주** 필드에는 작업을 그룹화할 수 있는 광범위한 작업 유형을 나타내는 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="be839-194">이 필드는 일정이나 인력 배치에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="be839-195">보고용으로만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="be839-196">업무 종속성</span><span class="sxs-lookup"><span data-stu-id="be839-196">Task dependencies</span></span> 

<span data-ttu-id="be839-197">PSA에서 일정을 사용하여 작업 간에 선행 관계를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="be839-198">**작업** 아래의 **선행자** 필드는 작업이 종속된 작업을 나타내기 위해 하나 이상의 값을 취합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="be839-199">선행 값이 작업에 할당될 때 모든 선행 작업이 완료되어야 해당 작업을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="be839-200">종속성으로 인해 작업의 계획된 시작 날짜는 선행 작업 완료 날짜로 재설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="be839-201">작업 모드는 선행/종속 작업의 시작 및 종료 날짜에 대한 업데이트에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="be839-202">업무 모드</span><span class="sxs-lookup"><span data-stu-id="be839-202">Task mode</span></span> 

<span data-ttu-id="be839-203">작업 모드는 리프 노드 작업의 일정을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="be839-204">PSA는 모든 업무에 자동 일정 모드와 수동 일정 모드의 두 가지 작업 모드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="be839-205">자동 일정</span><span class="sxs-lookup"><span data-stu-id="be839-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="be839-206">작업 모드를 **자동 예약** 으로 설정할 경우, 작업 일정 엔진이 다음 업무 특성에 대한 일정 규칙을 사용하여 업무에 대한 일정을 정합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="be839-207">일정 규칙</span><span class="sxs-lookup"><span data-stu-id="be839-207">Scheduling rules</span></span>

<span data-ttu-id="be839-208">기본적으로 리프 노드 작업에는 선행 업무가 없으며, 시작 날짜는 프로젝트의 일정 시작 날짜로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="be839-209">리프 노드 업무 기간은 항상 시작 및 종료 날짜 간의 작업일 수로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="be839-210">작업이 자동으로 설정되는 경우, 일정 엔진은 다음 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="be839-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="be839-211">작업 시작 및 종료 날짜는 반드시 프로젝트의 일정 관리 일정에 따른 작업일 수여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="be839-212">선행 작업이 있는 작업의 경우, 해당 시작 날짜는 선행 업무의 최종 날짜로 자동으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="be839-213">작업량은 사람 수 × 기간 × 프로젝트 달력의 표준 근무일 시간 수식을 사용하여 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="be839-214">수동 예약</span><span class="sxs-lookup"><span data-stu-id="be839-214">Manual scheduling</span></span>

<span data-ttu-id="be839-215">자동 예약의 규칙이 요구 사항을 충족하지 않는 경우 해당 작업의 작업 모드를 **수동으로 예약됨** 으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be839-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="be839-216">이 설정은 일정 엔진이 다른 일정 특성에 대한 값 계산을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="be839-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="be839-217">작업 모드에 관계없이 이전 작업을 작업에 설정하면 종속 작업의 시작 날짜에 항상 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="be839-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>
