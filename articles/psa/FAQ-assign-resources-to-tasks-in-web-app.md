---
title: 웹 앱에서 과업에 예약 가능한 리소스를 할당하려면 어떻게 해야 합니까?
description: 예약 가능한 리소스를 할당할 수 있는 방법에 대한 개요입니다.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080240"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="682bb-103">웹 앱(Project Service 앱 v2.x)의 작업에 예약 가능한 리소스를 할당하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="682bb-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="682bb-104">Project Service에서 작업에 리소스를 할당하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="682bb-105">리소스를 팀 구성원으로 예약한 다음 작업에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="682bb-106">또는 작업에 대한 역할 할당을 통해 일반 팀 구성원을 만들고 팀을 생성한 다음 명명된 리소스로 지원 요구 사항을 충족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="682bb-107">작업에 예약 가능한 리소스를 할당하려면 예약 가능한 리소스 팀 구성원이 사용 가능한 예약을 충분히 가지고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="682bb-108">예약 상태는 커밋 유형 확정 예약 및 이행된 상태여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="682bb-109">리소스에 대한 예약이 충분하지 않은 경우 Project Service는 할당을 제거하고 다음 오류 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="682bb-110">*작업에 리소스를 할당할 수 없습니다. 프로젝트에 대해 예약된 시간이 충분하지 않습니다.*</span><span class="sxs-lookup"><span data-stu-id="682bb-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="682bb-111">리소스를 팀 구성원으로 예약한 다음 작업에 리소스를 할당</span><span class="sxs-lookup"><span data-stu-id="682bb-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="682bb-112">이 방법을 사용하면 프로젝트 팀에 리소스를 추가한 다음 프로젝트 일정에서 리소스에 작업을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="682bb-113">이 작업을 수행하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="682bb-114">팀 구성원 표에서 **새로 만들기** 를 선택하여 새로운 팀 구성원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="682bb-115">팀 구성원의 빨리 만들기 화면에서 예약 가능한 리소스 이름을 선택하고 역할을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="682bb-116">**시작** 및 **종료** 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="682bb-117">![팀 구성원 추가 스크린샷](media/FAQ-Resources-to-Tasks2-1.png "팀 구성원 추가 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="682bb-118">다음 할당 방법 중 하나를 선택하여 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="682bb-119">**전체 생산 능력** 은 지정한 종료 날짜에서 시작 날짜까지 리소스의 전체 생산 능력을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="682bb-120">**백분율 생산 능력** 은 지정한 종료 날짜에서 시작 날짜까지 리소스 생산 능력의 백분율로 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="682bb-121">**시간별 균등 분배** 는 지정된 시간 동안 리소스를 예약하여 지정된 시작 날짜부터 종료 날짜까지 매일 균등하게 분배합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="682bb-122">**시간별 초기 단계 이익 배분** 은 지정된 시간 동안 리소스를 예약하여 지정된 시작 날짜부터 종료 날짜까지 일일 시간 단위로 초기 단계 이익 배분을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="682bb-123">이 방법은 리소스를 팀에 추가하지만 리소스의 생산 능력을 흡수하는 예약은 생성하지 않으므로 **없음** 을 선택하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="682bb-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="682bb-124">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-124">Select **Save**.</span></span>

    <span data-ttu-id="682bb-125">예약 시간은 이 리소스를 할당하는 작업의 작업 시간 및 날짜 범위를 충분히 포함할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="682bb-126">정렬되지 않은 경우에는 작업에 리소스를 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="682bb-127">작업에 대한 WBS(작업 분할 구조)에서 리소스 셀 드롭다운을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="682bb-128">다음 작업:</span><span class="sxs-lookup"><span data-stu-id="682bb-128">Then:</span></span> 

    1. <span data-ttu-id="682bb-129">**추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-129">Select **Add**.</span></span>
    2. <span data-ttu-id="682bb-130">**리소스** 에서 드롭다운을 선택하고 위에서 추가한 팀 구성원을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="682bb-131">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-131">Select **OK**.</span></span> <span data-ttu-id="682bb-132">이제 팀 구성원이 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="682bb-133">![WBS로 리소스 추가 스크린샷](media/FAQ-Resources-to-Tasks2-2.png "WBS로 리소스 추가 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="682bb-134">팀 구성원 표에는 지정된 시간 아래 리소스의 할당된 시간 집계가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="682bb-135">이 시간은 리소스의 예약된 시간보다 작거나 같을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="682bb-136">![리소스에 할당된 시간의 스크린샷](media/FAQ-Resources-to-Tasks2-3.png "리소스에 할당된 시간의 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="682bb-137">리소스에 할당하려는 작업이 리소스 예약의 종료 날짜 이후에 시작되는 경우 리소스는 드롭다운에서 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="682bb-138">리소스가 할당되지 않은 남은 용량이 있는 경우에는 예약된 시간보다 더 많은 시간에 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="682bb-139">이 경우 리소스는 해당 예약에만 부분적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="682bb-140">무인 시간 열을 작업 분할 구조에 추가하여 할당되지 않은 남은 작업 시간을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="682bb-141">예약한 시간에 리소스가 할당된 경우(예약된 시간이 할당된 시간과 같음) 추가 작업을 할당하려고 하면 다음과 같은 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="682bb-142">*작업에 리소스를 할당할 수 없습니다. 프로젝트에 대해 예약된 시간이 충분하지 않습니다.*</span><span class="sxs-lookup"><span data-stu-id="682bb-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="682bb-143">또한 프로젝트를 만들 때 팀에 추가되는 기본 프로젝트 관리자 팀 구성원은 예약 없이 추가되며 작업에 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="682bb-144">이러한 구성원은 작업에 대한 리소스 드롭다운에 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="682bb-145">이 리소스를 할당하려면 팀에서 제거하고 없음 이외의 할당 방법으로 다시 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="682bb-146">프로젝트가 만들어질 때 팀에 추가되는 이유는 프로젝트에 기본적으로 프로젝트 승인자가 한 명 이상 있도록 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="682bb-147">작업에 대한 역할 할당을 통해 일반 팀 구성원 만들기</span><span class="sxs-lookup"><span data-stu-id="682bb-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="682bb-148">이 방법은 작업에 충분한 리소스가 예약되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="682bb-149">먼저 작업에 역할을 할당한 후 팀을 생성하여 작업을 수행하려는 명명된 리소스의 특성을 설명하는 자리 표시자 또는 일반 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="682bb-150">이 작업을 수행하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="682bb-151">작업 분할 구조에서 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="682bb-152">리소스 셀에서 **할당된 역할** 드롭다운 아이콘을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="682bb-153">**역할** 드롭다운을 선택하고 일반 리소스에 대한 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="682bb-154">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="682bb-155">![WBS를 사용하여 리소스를 추가하는 스크린샷](media/FAQ-Resources-to-Tasks2-4.png "WBS를 사용하여 리소스를 추가하는 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="682bb-156">WBS에서 작업에 역할 할당을 완료했으면 **프로젝트 팀 생성** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="682bb-157">Project Service는 작업 할당을 집계하여 역할, 조직 단위 리소스 및 프로젝트 달력을 기반으로 최소한의 일반 팀 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="682bb-158">![프로젝트 팀 생성 스크린샷](media/FAQ-Resources-to-Tasks2-5.png "프로젝트 팀 생성 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="682bb-159">팀 구성원 표에는 역할 및 위치 이름이 포함된 일반 리소스 유형의 리소스가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="682bb-160">작업을 완료하는 데 역할에 두 개의 리소스가 필요한 경우 팀 생성 기능을 사용하면 두 명의 팀 구성원이 생성되고 둘을 구분하는 데 위치 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="682bb-161">![두 일반 리소스 추가 스크린샷](media/FAQ-Resources-to-Tasks2-6.png "두 일반 리소스 추가 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="682bb-162">리소스 요구 사항 아래의 링크를 선택하여 일반 팀 구성원에 대한 지원 리소스 요구 사항을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="682bb-163">![지원 리소스 요구 사항을 여는 스크린샷](media/FAQ-Resources-to-Tasks2-7.png "지원 리소스 요구 사항을 여는 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="682bb-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="682bb-164">일반 리소스에 대해 **예약** 을 선택한 다음 일정 게시판을 사용하여 실제 리소스를 찾고 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="682bb-165">**요청 제출** 을 선택하여 리소스 관리자가 이행 요구 사항을 제출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="682bb-166">명명된 리소스로 일반 리소스가 이행되면 일반 리소스가 팀에서 제거되고 일반 리소스에 대한 작업 할당이 일반 리소스의 리소스 요구 사항을 충족하는 명명된 리소스에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="682bb-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

