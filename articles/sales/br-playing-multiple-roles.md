---
title: 예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다.
description: 이 토픽에서는 가격 책정 측정 기준을 사용하여 프로젝트에서 여러 역할을 수행하는 리소스의 가격 책정 및 예상 비용을 지원하는 방법을 설명합니다.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531487"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a><span data-ttu-id="e80eb-103">예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-103">Estimate project sales and costs when a bookable resource fills multiple roles on a project</span></span> 

<span data-ttu-id="e80eb-104">_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 처리 및 재고/생산 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e80eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_</span></span> 

<span data-ttu-id="e80eb-105">프로젝트 기반 회사는 종종 프로젝트에서 여러 역할을 수행하기 위해 하나의 리소스가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-105">Project-based companies often have the need for one resource to fill multiple roles on a project.</span></span> <span data-ttu-id="e80eb-106">각 역할은 가격과 비용이 다르게 책정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-106">Each role can be priced and costed differently.</span></span> <span data-ttu-id="e80eb-107">즉, 프로젝트에서 동일한 리소스의 시간이 각 역할의 청구서 및 비용 요율에 따라 다른 재정적 추정치를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-107">This means that the same resource's time on a project could get a different financial estimate depending on the bill and cost rates for each role.</span></span> <span data-ttu-id="e80eb-108">팀 구성원이 할당된 각 작업에 대해 다른 재정의를 사용하여 명명된 리소스에 대한 팀 구성원 레코드의 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-108">You can set up the values on the team member record for the named resource with different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="e80eb-109">다음 예제는 값의 단순한 재정의를 통해 리소스가 비용 및 청구 비율이 다른 프로젝트에서 여러 역할을 가질 수 있도록 하는 방법을 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-109">The following example walks you through how the simple override of a value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="e80eb-110">작업 만들기</span><span class="sxs-lookup"><span data-stu-id="e80eb-110">Create tasks</span></span>
<span data-ttu-id="e80eb-111">작업을 만들려면 작업과 요약 작업을 추가해야 하며 그 후에 작업 기간을 추가하기 전에 작업을 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-111">To create tasks, you need to add tasks, as well as summary tasks, after which you need to assign the task before you add task duration.</span></span> 

### <a name="add-tasks-and-summary-tasks"></a><span data-ttu-id="e80eb-112">작업 및 요약 작업 추가</span><span class="sxs-lookup"><span data-stu-id="e80eb-112">Add tasks and summary tasks</span></span>
<span data-ttu-id="e80eb-113">작업을 추가하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-113">To add a task, complete the following steps.</span></span>

1. <span data-ttu-id="e80eb-114">**프로젝트** 로 이동하고 작업을 추가할 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-114">Go to **Projects** and open the project to which you want to add tasks.</span></span>
2. <span data-ttu-id="e80eb-115">**새 작업 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-115">Select **Add new task**.</span></span> <span data-ttu-id="e80eb-116">작업 이름을 지정한 다음 **Enter** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-116">Name the task, and then press **Enter**.</span></span>
3. <span data-ttu-id="e80eb-117">다른 작업 이름을 입력한 다음 **Enter** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-117">Enter another task name and press **Enter**.</span></span> <span data-ttu-id="e80eb-118">전체 작업 목록이 나올 때까지 이 작업을 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-118">Repeat this until you have a full list of tasks.</span></span>
3. <span data-ttu-id="e80eb-119">**요약** 작업 아래에 작업을 들여 쓰려면 이름 옆에 있는 세 개의 수직 점을 선택한 다음 **하위 작업 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-119">To indent tasks under **Summary** tasks, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 

  > [!TIP]
  > <span data-ttu-id="e80eb-120">둘 이상의 작업을 선택하려면 작업을 선택하고 **Ctrl** 키를 누른 상태에서 다른 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-120">To select more than one task, select a task, press and hold **Ctrl**, and then select another task.</span></span>
  >
  > <span data-ttu-id="e80eb-121">또한 **하위 작업 수준 올리기** 를 선택하여 **요약** 작업 아래에서 작업을 꺼낼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-121">You can also choose **Promote subtask** to move tasks out from under **Summary** tasks.</span></span>

### <a name="assign-tasks"></a><span data-ttu-id="e80eb-122">작업 할당</span><span class="sxs-lookup"><span data-stu-id="e80eb-122">Assign tasks</span></span>

<span data-ttu-id="e80eb-123">작업을 할당하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-123">Complete the following steps to assign tasks.</span></span>

1. <span data-ttu-id="e80eb-124">작업의 **할당 대상** 열에서 사람 아이콘을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-124">In the  **Assigned to**  column for a task, select the person icon.</span></span>
2. <span data-ttu-id="e80eb-125">목록에서 팀 구성원을 선택하거나 텍스트를 입력하여 이름을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-125">Choose a team member from the list or enter text to search for a name.</span></span>

### <a name="add-task-duration-and-columns"></a><span data-ttu-id="e80eb-126">작업 기간 및 열 추가</span><span class="sxs-lookup"><span data-stu-id="e80eb-126">Add task duration and columns</span></span>

<span data-ttu-id="e80eb-127">기간을 두고 프로젝트 구성을 시작하는 것이 가장 쉬운 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-127">It's often easiest to begin constructing your project with duration.</span></span> <span data-ttu-id="e80eb-128">작업 기간을 추가하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-128">Complete the following steps to add a task duration.</span></span>

1. <span data-ttu-id="e80eb-129">작업의 **기간** 열에 작업을 완료하는 데 걸리는 일 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-129">In the **Duration** column for a task, type the number of days you think it will take to accomplish the task.</span></span> <span data-ttu-id="e80eb-130">다른 시간 단위를 사용하려면 숫자와 단어 **시간**,**주** 또는 **개월** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-130">If you want to use a different unit of time, enter a number plus the word **hours**, **weeks**, or **months**.</span></span>
2. <span data-ttu-id="e80eb-131">작업이 다이아몬드 모양의 중요 시점으로 표시되도록 하려면 **타임라인** 보기의 **기간** 열에 **0일** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-131">If you want your task to appear as a diamond-shaped milestone in the **Timeline** view, in the **Duration** column, enter **0 days** .</span></span>
3. <span data-ttu-id="e80eb-132">**Enter** 키를 눌러 다음 작업의 **기간** 필드로 이동하고 기간을 계속 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-132">Press **Enter**  to go to the next task's **Duration** field and continue entering durations.</span></span>

  > [!NOTE]
  > <span data-ttu-id="e80eb-133">요약 작업 기간은 입력할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-133">You can't enter a duration for summary tasks.</span></span>

<span data-ttu-id="e80eb-134">프로젝트에 열을 추가하여 더 자세한 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-134">You can add columns to your project to provide more details.</span></span> <span data-ttu-id="e80eb-135">이를 위해 **열 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-135">To do this, select **Add column**.</span></span> 

<span data-ttu-id="e80eb-136">자세한 내용은 [프로젝트 만들기](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e80eb-136">For more information, see [Create a project](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).</span></span>

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="e80eb-137">일반 프로젝트 팀 구성원의 역할 및 조직 구성 단위 설정</span><span class="sxs-lookup"><span data-stu-id="e80eb-137">Set up the role and organization unit for a generic project team member</span></span>
<span data-ttu-id="e80eb-138">일반 팀 구성원의 역할 및 조직 구성 단위를 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e80eb-138">Complete the following steps to set up a role and organizational unit for a generic team member.</span></span>

1. <span data-ttu-id="e80eb-139">**작업** 페이지에서 **작업 A** 의 **작업** 행을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-139">On the **Tasks** page, select the **Task** row for **Task A**.</span></span> 
2. <span data-ttu-id="e80eb-140">**할당 대상** 에서 **일반 리소스 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-140">In **Assigned To**, select **Add generic resource**.</span></span> <span data-ttu-id="e80eb-141">그러면 **팀 구성원 빨리 만들기** 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-141">This opens the **Team Member Quick Create** page.</span></span>
3. <span data-ttu-id="e80eb-142">**팀 구성원 빨리 만들기** 페이지에서 이 작업을 수행할 수 있는 일반 팀 구성원의 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-142">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="e80eb-143">적절한 역할 및 조직 구성 단위를 선택한 다음 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-143">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="e80eb-144">일반 팀 구성원이 생성되고 이 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-144">A generic team member is created and assigned to this task.</span></span> 
5. <span data-ttu-id="e80eb-145">**작업 B** 에 대해 1-4 단계를 반복합니다. 그러나 **작업 B** 는 일반 팀 구성원에게 할당된 역할과 조직 구성 단위가 **작업 A** 와 달라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-145">Repeat steps 1-4 for **Task B**. However, **Task B** must have a different role and organizational unit assigned for the generic team member than **Task A**.</span></span> 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="e80eb-146">프로젝트 작업의 역할 및 조직 구성 단위 설정</span><span class="sxs-lookup"><span data-stu-id="e80eb-146">Set up the role and organization unit for a project task</span></span>
<span data-ttu-id="e80eb-147">작업의 역할 및 조직 구성 단위를 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e80eb-147">Complete the following steps to set up a role and organizational unit for a task.</span></span>

1. <span data-ttu-id="e80eb-148">**작업 A** 를 만든 후 작업을 선택한 다음 **i** 아이콘을 선택하여 **작업 세부 정보** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-148">After you create **Task A**, select the task, and then select the **i** icon to open the **Task Details** pane.</span></span> 
2. <span data-ttu-id="e80eb-149">**작업 세부 정보** 창에서 아래로 스크롤하여 **세부 정보 보기** 를 선택하여 **작업 세부 정보** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-149">On the **Task Details** pane, scroll to the bottom and select **View Details** to open the **Task Details** page.</span></span>
3. <span data-ttu-id="e80eb-150">**작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 에서 리소스에 대해 이 작업을 수행하는 데 필요한 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-150">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required to perform this task for the resource.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e80eb-151">Project Operations 데모 데이터를 사용하여 이 시나리오를 완료한 경우 역할에 대한 **컨설팅 리드** 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-151">If you complete this scenario using the Project Operations demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

4. <span data-ttu-id="e80eb-152">**작업 B** 를 선택한 다음 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-152">Select **Task B**, and then select the task.</span></span>
5. <span data-ttu-id="e80eb-153">**i** 아이콘을 선택하여 **작업 세부 정보** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-153">Select the **i** icon to open **Task Details** pane.</span></span> 
6. <span data-ttu-id="e80eb-154">**작업 세부 정보** 창에서 아래로 스크롤하여 **세부 정보 보기** 를 선택하여 **작업 세부 정보** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-154">On the **Task Details** pane, scroll to the bottom and select **View details** to open the **Task Details** page.</span></span>
7. <span data-ttu-id="e80eb-155">**작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 에서 이 작업을 수행할 리소스에 필요한 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-155">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="e80eb-156">**작업 B** 에 대한 **역할** 및 **조직 구성 단위** 의 값은 **작업 A** 와 달라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-156">The values in **Role** and **Organizational Unit** for **Task B** must be different than those for **Task A**.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e80eb-157">Project Operations 데모 데이터를 사용하여 이 시나리오를 완료한 경우 역할에 대한 **네트워크 기술자** 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-157">If you complete this scenario using the Project Operations demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

8. <span data-ttu-id="e80eb-158">저장 후 **작업 세부 정보** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-158">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="e80eb-159">팀 구성원 및 추정 행동</span><span class="sxs-lookup"><span data-stu-id="e80eb-159">Team member and estimates behavior</span></span> 
<span data-ttu-id="e80eb-160">**팀 구성원** 그리드 및 추정치의 행동을 이해하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e80eb-160">To understand the behavior on the **Team Member** grid and the estimates, complete the following steps.</span></span>

1. <span data-ttu-id="e80eb-161">**팀 구성원** 그리드에서 두 명의 일반 팀 구성원을 선택한 다음 **요구 사항 생성** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-161">On the **Team Member** grid, select the two generic team members, and then select **Generate Requirements**.</span></span> <span data-ttu-id="e80eb-162">그러면 리소스 요구 사항이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-162">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="e80eb-163">**컨설팅 리드** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-163">Select the team member row for **Consulting Lead**, and then select **Book**.</span></span> <span data-ttu-id="e80eb-164">리소스 목록과 함께 일정 게시판이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-164">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="e80eb-165">리소스를 선택한 다음 **예약** 을 선택하여 해당 요구 사항에 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-165">Select a resource and then select **Book** to book the resource to that requirement.</span></span>
3. <span data-ttu-id="e80eb-166">**네트워크 기술자** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-166">Select the team member row for **Network Technician**, and then select **Book**.</span></span> <span data-ttu-id="e80eb-167">리소스 목록과 함께 일정 게시판이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-167">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="e80eb-168">위와 동일한 리소스를 선택한 다음 **예약** 을 선택하여 해당 요구 사항에 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-168">Select the same resource as above and then select **Book** to book the resource to that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="e80eb-169">팀 구성원 그리드</span><span class="sxs-lookup"><span data-stu-id="e80eb-169">Team Member grid</span></span> 

<span data-ttu-id="e80eb-170">**팀 구성원** 그리드에서 두 개의 일반 팀 구성원 레코드가 삭제되고 하나의 리소스로만 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-170">On the **Team Member** grid, the two generic team member records are deleted and replaced with only one resource.</span></span> <span data-ttu-id="e80eb-171">**역할** 및 **조직 구성 단위** 에 대한 기본값 집합인 해당 리소스에 대해 하나의 값 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-171">There is one set of values for that resource, which are a default set of values for **Role** and **Organizational Unit**.</span></span>

<span data-ttu-id="e80eb-172">해당 팀 구성원 레코드에 대한 행을 확장하면 두 작업에 대한 팀 구성원 레코드에서 고유한 할당을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-172">When you expand the row for that team member record, you can see distinct assignments on the team member record for both tasks.</span></span> <span data-ttu-id="e80eb-173">각 할당 행에는 **역할** 및 **조직 구성 단위** 에 대한 작업별 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-173">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="e80eb-174">추정 그리드</span><span class="sxs-lookup"><span data-stu-id="e80eb-174">Estimates grid</span></span> 

<span data-ttu-id="e80eb-175">**추정** 그리드에서 동일한 리소스에 대한 두 할당은 서로 다른 가격이 책정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-175">On the **Estimates** grid, both assignments for the same resource are priced differently.</span></span> <span data-ttu-id="e80eb-176">**작업 A** 의 리소스 할당은 **컨설팅 리드** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-176">The assignment for the resource on **Task A** is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="e80eb-177">**작업 B** 의 동일한 리소스 할당은 **네트워크 기술자** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e80eb-177">The assignment for the same resource on **Task B** is priced using the **Role** attribute value of **Network Technician**.</span></span>
