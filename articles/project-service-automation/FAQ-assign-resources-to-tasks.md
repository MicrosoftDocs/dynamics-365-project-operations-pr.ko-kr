---
title: 과업에 리소스를 배정
description: 이 항목은 과업에 리소스를 배정하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753377"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="f856a-103">과업에 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="f856a-103">Assign a resource to a task</span></span>

<span data-ttu-id="f856a-104">Microsoft Dynamics 365 Project Service Automation에서 과업에 리소스를 배정하는 방법에는 세 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="f856a-105">리소스를 팀원으로 예약한 다음 과업에 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="f856a-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="f856a-106">프로젝트 팀에 리소스를 추가한 다음, 프로젝트 스케줄에서 과업에 리소스를 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="f856a-107">**팀원** 탭에서 **신규**를 선택하여 새 팀원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="f856a-108">**팀원 빠른 생성** 패널이 열리면 예약 가능한 리소스 이름을 선택하고 역할을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="f856a-109">다음 할당 방법 중 하나를 선택하여 리소스를 예약합니다:</span><span class="sxs-lookup"><span data-stu-id="f856a-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="f856a-110">**전체 생산 능력**은 지정한 종료 날짜에서 시작 날짜까지 리소스의 전체 생산 능력을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f856a-111">**백분율 생산 능력**은 지정한 종료 날짜에서 시작 날짜까지 리소스 생산 능력의 백분율로 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f856a-112">**시간별 균등 분배**는 지정된 시간 동안 리소스를 예약하여 지정된 시작 날짜부터 종료 날짜까지 매일 균등하게 분배합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="f856a-113">**시간별 초기 단계 이익 배분**은 지정된 시간 동안 리소스를 예약하여 지정된 시작 날짜부터 종료 날짜까지 일일 시간 단위로 초기 단계 이익 배분을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="f856a-114">**없음**은 리소스를 팀에 추가하지만 해당 리소스의 생산 능력을 흡수하는 예약은 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="f856a-115">과업의 **스케줄** 그리드에서 리소스 셀의 **리소스** 아이콘을 선택한 다음 **팀원** 항목에서 방금 추가한 팀원을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="f856a-116">**팀원** 및 **조정** 탭에서 리소스는 예약 시간 및 할당된 시간을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="f856a-117">시간 수는 동일해야 하지만, 예약과 할당이 긴밀하게 결합되지 않으므로 같을 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="f856a-118">**조정** 탭을 사용하면 예약한 것보다 더 많은 시간 동안 리소스를 할당할 때와 같이 다른 경우에 대한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="f856a-119">필요한 경우, 리소스의 예약을 확장하거나 할당을 변경함으로써 정보를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="f856a-120">작업 할당을 통한 일반 팀원 생성</span><span class="sxs-lookup"><span data-stu-id="f856a-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="f856a-121">과업 할당을 통해 일반 팀원을 생성할 때 귀하가 궁극적으로 과업을 수행하려는 명명된 리소스의 특성을 설명하는 자리 표시자 또는 일반 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="f856a-122">그런 다음 명명된 리소스를 검색하고 예약하는 데 사용되는 요건을 생성하거나 요건을 사용하여 요청을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="f856a-123">과업의 **스케줄** 그리드에서 리소스 셀에 있는 **리소스** 아이콘을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="f856a-124">자리 표시자 리소스 이름으로 사용할 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="f856a-125">예: 프로그램 관리자.</span><span class="sxs-lookup"><span data-stu-id="f856a-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="f856a-126">**생성**을 선택하고 **프로젝트 팀원 빠른 생성** 필드에서 일반 리소스에 대한 역할을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="f856a-127">작업에 대한 **리소스 선택기**에서 리소스를 선택하여 이 자리 표시자 리소스에 작업을 계속 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="f856a-128">이들은 **팀원** 아래에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="f856a-129">일반 리소스 할당을 마쳤으면 **팀** 탭에서 일반 리소스를 선택하고 **요건 생성**을 선택하여 일반 리소스에 대한 리소스 요건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="f856a-130">일반 리소스에 대한 **예약**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="f856a-131">그런 다음 스케줄 게시판을 사용하여 실제 리소스를 찾고 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="f856a-132">리소스 관리자가 이행 요구 사항을 제출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="f856a-133">명명된 리소스로 일반 리소스가 이행되면 일반 리소스가 팀에서 제거되고 일반 리소스에 대한 작업 할당이 일반 리소스의 리소스 요구 사항을 충족하는 명명된 리소스에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="f856a-134">예약 가능한 모든 리소스 목록에서 명명된 리소스 할당</span><span class="sxs-lookup"><span data-stu-id="f856a-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="f856a-135">**리소스 선택기**의 검색 상자를 사용하여 예약 가능한 모든 리소스를 검색하고 작업에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="f856a-136">이 방법으로 할당된 리소스는 예약 없이 팀에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="f856a-137">이는 팀원을 추가하고 없음을 할당 방법으로 선택하는 것과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="f856a-138">리소스는 **팀** 탭과 **조정** 탭에 할당 및 예약 부족만 있는 리소스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="f856a-139">가용성을 사용하려면 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="f856a-140">과업의 **스케줄** 그리드에서 리소스 셀에 있는 **리소스** 아이콘을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="f856a-141">이름을 입력하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-141">Start typing a name.</span></span> <span data-ttu-id="f856a-142">이름에 대한 검색 결과는 **리소스 선택기**의 **기타 리소스**에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="f856a-143">과업에 배정하기 원하는 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f856a-143">Select the resource that you want to assign to the task.</span></span>

