---
title: 리소스 관리
description: 이 항목은 리소스를 관리할 수 있는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080253"
---
# <a name="manage-resources"></a><span data-ttu-id="d7c31-103">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="d7c31-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7c31-104">Dynamics 365 Project Service Automation에는 조직 전체의 리소스 수요 및 사용률에 대한 시각적 개요를 제공하는 리소스 관리자 대시보드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="d7c31-105">이 대시보드의 차트를 사용하여 다음 정보를 시각화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="d7c31-106">**리소스 요구** - **활성 리소스 요청** 차트에 제출된 리소스가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="d7c31-107">리소스는 역할 또는 프로젝트별로 집계됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="d7c31-108">**제출되지 않은 리소스 수요** - **할당되지 않은 리소스 수요** 차트에는 제출되지 않은 모든 리소스 요구 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="d7c31-109">리소스 관리자가 확고하지 않고 리소스 요청을 통해 제출할 수 있는 수요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="d7c31-110">**지난 주에 대한 청구 가능 사용률** – **역할별 사용률** 차트는 역할별 대상 청구 가능 사용률에 대해 역할별 조직의 실제 청구 가능 사용률의 백분율을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d7c31-111">**역할별 사용률** 차트를 사용할 수 있도록 하려면 UpdateRoleUtilization 워크플로를 실행하는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="d7c31-112">이 되풀이 작업은 7일마다 실행되어 이전 7일 동안의 청구 가능 사용률을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="d7c31-113">결과는 역할별로 집계됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="d7c31-114">프로젝트 팀 구성원 관리</span><span class="sxs-lookup"><span data-stu-id="d7c31-114">Manage project team members</span></span>

<span data-ttu-id="d7c31-115">프로젝트 관리자는 리소스 관리자 대시보드를 사용하여 프로젝트의 리소스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="d7c31-116">예를 들어 프로젝트에 팀 구성원을 직접 추가하고 팀 구성원을 예약하여 일반 리소스에 의해 캡처된 리소스 요구 사항을 충족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="d7c31-117">프로젝트에 직접 팀 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="d7c31-117">Add a team member directly to a project</span></span>

<span data-ttu-id="d7c31-118">프로젝트에 팀 구성원을 직접 추가하려면 **팀** 탭의 **프로젝트** 페이지에서 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="d7c31-119">**빠른 만들기:프로젝트 팀 구성원** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="d7c31-120">이 대화 상자에서 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="d7c31-121">**명명된 리소스 예약** – **예약 가능한 리소스** 필드에서 리소스 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="d7c31-122">그런 다음 역할을 선택하고 기간을 설정하고 할당 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="d7c31-123">선택한 지정된 리소스가 선택한 할당 메서드와 리소스 일정을 사용하여 프로젝트에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="d7c31-124">**일반 리소스 추가** – **예약 가능한 리소스** 필드를 비워 두었다가 역할을 선택하고 기간을 설정하고 기본 할당 메서드를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="d7c31-125">일반 리소스가 팀에 자리 표시자로 추가되어 팀에서 명명된 리소스를 예약하는 데 사용되는 요구 패턴을 보유합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="d7c31-126">요구 사항은 프로젝트 일정에 따라 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="d7c31-127">**리소스 생산 능력을 소모하지 않고 명명된 리소스를 팀에 추가** - **예약 가능한 리소스** 필드에서 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="d7c31-128">그런 다음 기간을 선택하고 **없음** 을 할당 메서드로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="d7c31-129">리소스가 팀에 추가되지만 리소스의 생산 능력은 예약을 통해 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="d7c31-130">일반 리소스에 대한 리소스 요구 사항을 충족하기 위해 팀 구성원을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="d7c31-131">PSA에서는 프로젝트 팀에서 일반 리소스를 예약할 수 있으며 역할, 필요한 생산 능력 및 해당 생산 능력이 배포되는 방법을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="d7c31-132">리소스 요구 사항에 따라 일반 리소스와 연결된 특성을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="d7c31-133">이러한 특성에는 필수 기술, 선호 조직 구성 단위 및 선호 리소스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="d7c31-134">다음 단계에 따라 개발자의 일반 리소스에 필요한 기술을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="d7c31-135">**팀** 탭의 **프로젝트** 페이지에서 **신규** 를 선택하여 일반 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![팀에 예약한 일반 리소스](media/Resource-Management-image9.png)

2. <span data-ttu-id="d7c31-137">**모든 팀 구성원** 보기의 **리소스 요구 사항** 열에서 일반 리소스에 필요한 기술을 추가할 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![요구 사항 링크](media/Resource-Management-image10.png)

3. <span data-ttu-id="d7c31-139">**기술** 표에 나타나는 **리소스 요구 사항** 페이지에서 말줄임표( **...** )를 선택하고 **새 요구 사항 특성 추가** 를 선택하여 개발자에게 필요한 기술을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![신규 요구 사항 특성 명령어 추가](media/Resource-Management-image11.png)

4. <span data-ttu-id="d7c31-141">**특성** 필드에 나타나는 **빠른 만들기: 요구 사항 특성** 대화 상자에서 필요한 기술을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="d7c31-142">그런 다음 **등급 값** 필드에서 해당 기술에 대한 숙련도 수준을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="d7c31-143">마지막으로 **리소스 요구 사항** 필드에서 조직 구성 단위 또는 명명된 리소스에서 리소스를 소스로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="d7c31-144">완료되면 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-144">When you've finished, select **Save**.</span></span>

    ![빠른 만들기: 요구 사항 특성 대화 상자](media/Resource-Management-image12.png)

5. <span data-ttu-id="d7c31-146">**리소스 요구 사항** 페이지에서 리소스 요구 사항을 충족하려면 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![리소스 요구 사항 페이지의 예약 단추](media/Resource-Management-image13.png)

    <span data-ttu-id="d7c31-148">**모든 팀 구성원** 표에서 일반 리소스를 선택한 다음 **예약** 을 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![모든 팀 구성원 표 위의 예약 버튼](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="d7c31-150">이 예제에서는 일반 리소스에 예약이 없기 때문에 40시간이 필요하지만 실제 예약 시간은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="d7c31-151">또한 일반 리소스가 팀에 직접 추가되었기 때문에 할당된 시간이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="d7c31-152">작업 할당을 사용하여 추가되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="d7c31-153">**예약 도우미** 페이지에서 리소스 요구 사항에 지정된 요구 사항에 따라 사용 가능한 리소스를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="d7c31-154">리소스는 일정 게시판에 지정된 정렬 매개 변수에 따라 정렬됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![일정 도우미 페이지](media/Resource-Management-image15.png)

    <span data-ttu-id="d7c31-156">다음은 자주 사용되는 몇 가지 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="d7c31-157">**등급에 따른 특성** – 기술, 인증 및 기타 리소스 품질에 따라 필터링하고 숙련도 등급에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="d7c31-158">**역할** - 예약 가능한 리소스에 할당된 기본 역할별로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="d7c31-159">**조직 구성 단위** – 할당된 조직 단위별로 예약 가능한 리소스를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="d7c31-160">초기 요구 사항 검색 결과에 만족하지 않으면 필터 조건을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="d7c31-161">왼쪽의 **필터 보기** 창을 확장한 다음 **검색** 을 선택하여 추가 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![필터 보기 창](media/Resource-Management-image16.png)

7. <span data-ttu-id="d7c31-163">결과를 정렬하는 방법을 변경하려면 **정렬** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-163">To change how the results are sorted, select **Sort**.</span></span>

    ![정렬 명령](media/Resource-Management-image17.png)

8. <span data-ttu-id="d7c31-165">표 맨 위에 표시된 대로 요구 사항에 지정된 수요에 따라 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="d7c31-166">표에서 셀 선택을 지우고 해당 리소스 생산 능력을 열어 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="d7c31-167">한 번에 하나의 리소스만 예약된 리소스로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="d7c31-168">**예약** 을 선택하여 선택한 리소스를 예약하고 일정 게시판을 열어 두면 추가 리소스를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="d7c31-169">또는 **예약 및 종료** 를 선택하여 선택한 리소스를 예약하고 일정 게시판을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![예약할 리소스](media/Resource-Management-image19.png)

    <span data-ttu-id="d7c31-171">예약된 시간에 대한 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="d7c31-172">수요 지표는 예약 요건이 얼마나 충족되는지, 얼마나 남아 있는지를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="d7c31-173">선택한 리소스의 생산 능력이 얼마나 사용되는지도 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="d7c31-174">리소스 예약에 대한 자세한 내용을 보려면 **확장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="d7c31-175">**모든 팀 구성원** 보기로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="d7c31-176">표에서 일반 리소스가 명명된 리소스로 대체되었으며 40시간이 해당 리소스에 대해 예약된 리소스로 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![업데이트된 모든 팀 구성원 표](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="d7c31-178">팀에서 직접 예약했기 때문에 할당된 시간이 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="d7c31-179">작업 할당을 사용하여 예약되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="d7c31-180">작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성</span><span class="sxs-lookup"><span data-stu-id="d7c31-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="d7c31-181">PSA에서 작업을 만든 다음 일반 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="d7c31-182">이러한 방식으로 일정 및 재무 번호를 예측하는 동안 자리 표시자가 리소스 수요를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="d7c31-183">그런 다음 일반 리소스에 대한 리소스 요구 사항을 생성하고 이를 충족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="d7c31-184">**일정** 탭의 **프로젝트** 페이지에서 **추가** 를 선택하여 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![새 작업 생성됨](media/Resource-Management-image21.png)

2. <span data-ttu-id="d7c31-186">**리소스** 필드에서 **리소스 선택기** 기호를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="d7c31-187">리소스 선택기가 나타나고 프로젝트에 대한 기존 팀 구성원을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![리소스 선택기](media/Resource-Management-image22.png)

3. <span data-ttu-id="d7c31-189">새 일반 리소스의 이름을 입력한 다음 **만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![입력한 새 일반 리소스의 이름](media/Resource-Management-image23.png)

4. <span data-ttu-id="d7c31-191">**역할** 필드에 나타나는 **빠른 만들기: 프로젝트 팀 구성원** 대화 상자에서 일반 리소스의 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="d7c31-192">**리소스 단위** 필드에서 일반 리소스에 대한 조직 구성 단위를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="d7c31-193">그런 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-193">Then select **Save**.</span></span>

    ![빠른 만들기: 프로젝트 팀 구성원 대화 상자](media/Resource-Management-image24.png)

    <span data-ttu-id="d7c31-195">이제 일반 팀 구성원이 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-195">The generic team member is now assigned to the task.</span></span>

    ![작업에 할당된 일반 팀 구성원](media/Resource-Management-image25.png)

    <span data-ttu-id="d7c31-197">**팀** 탭에 새 일반 팀 구성원이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="d7c31-198">할당된 시간만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="d7c31-199">이 시간은 일반 팀 구성원에게 할당된 모든 작업의 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="d7c31-200">일반 팀 구성원은 아직 시간이나 리소스 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![팀 탭의 일반 팀 구성원](media/Resource-Management-image26.png)

5. <span data-ttu-id="d7c31-202">이제 리소스 선택기를 사용하여 일반 팀 구성원을 다른 작업에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![리소스 선택기의 일반 팀 구성원](media/Resource-Management-image27.png)

    <span data-ttu-id="d7c31-204">작업에 일반 리소스 할당을 완료하면 일반 리소스에 대한 리소스 요구 사항을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="d7c31-205">**팀** 탭에서 일반 리소스를 선택한 다음 **요구 사항 생성** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![요구 사항 생성 명령](media/Resource-Management-image28.png)

    <span data-ttu-id="d7c31-207">요구 사항이 생성되면 일반 팀 구성원은 리소스 요구 사항에 대한 필요한 시간과 링크를 갖게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![리소스 요구 사항 링크](media/Resource-Management-image29.png)

    <span data-ttu-id="d7c31-209">명명된 리소스를 예약한 후에 일반 리소스가 팀에서 제거되고 명명된 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![명명된 리소스로 대체된 일반 리소스](media/Resource-Management-image30.png)

    <span data-ttu-id="d7c31-211">**일정** 탭에서 일반 리소스 할당이 제거되고 명명된 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![일정 탭에서 일반 리소스 할당이 명명된 리소스로 대체됩니다.](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="d7c31-213">이 동작은 명명된 리소스가 일반 리소스 요구 사항에 대해 완전히 예약된 경우에만 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="d7c31-214">명명된 리소스가 일반 리소스 요구 사항을 부분적으로 대체하거나 여러 명명된 리소스가 일반 리소스 요구 사항을 대체하면 일반 리소스가 작업에 할당된 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="d7c31-215">다음 그림에서는 5일 기간(5일 동안 하루 16시간)에 대해 80시간의 작업을 계획하고 **기능** 이라는 일반 리소스에 할당했습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![기능 일반 리소스에 할당된 80시간 5일 작업](media/Resource-Management-image32.png)

    <span data-ttu-id="d7c31-217">요구 사항을 생성하면 5일 동안 80시간 동안 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![5일 동안 80시간 동안 생성된 요구 사항](media/Resource-Management-image33.png)

    <span data-ttu-id="d7c31-219">사용 가능한 리소스는 하루에 8시간만 작동하므로 요구 사항을 충족하기 위해 두 개의 리소스가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![두 번째 리소스](media/Resource-Management-image35.png)

    <span data-ttu-id="d7c31-221">이제 **팀** 탭에서 일반 리소스에 필요한 시간이 없음을 알 수 있지만 할당된 시간은 여전히 이행을 구성하는 두 개의 명명된 리소스와 함께 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![팀 탭의 명명된 리소스 두 개](media/Resource-Management-image36.png)

    <span data-ttu-id="d7c31-223">**일정** 탭에서 일반 리소스는 작업에 할당된 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![일정 탭의 일반 리소스](media/Resource-Management-image37.png)

<span data-ttu-id="d7c31-225">PSA는 이 동작으로 인해 예측하기 어려운 일정이 생성되므로 두 리소스를 작업에 할당하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="d7c31-226">이 간단한 예제에서는 시간을 두 리소스 간에 균등하게 나눌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="d7c31-227">그러나 여러 작업과 여러 리소스가 포함된 더 복잡한 시나리오에서 PSA는 여러 작업에서 여러 리소스에 대해 받은 예약을 할당하는 방법을 가정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="d7c31-228">따라서 이러한 시나리오에서 프로젝트 관리자는 여러 예약을 구문 분석하고 필요에 따라 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="d7c31-229">예약을 할당하기 위해 프로젝트 관리자는 일반 리소스에서 명명된 리소스에 작업을 할당한 다음 **조정** 보기를 사용하여 할당이 예약과 함께 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="d7c31-230">리소스 요구 사항 편집</span><span class="sxs-lookup"><span data-stu-id="d7c31-230">Edit a resource requirement</span></span>

<span data-ttu-id="d7c31-231">리소스 요구 사항이 만들어진 후 프로젝트 관리자 또는 리소스 관리자는 일정 게시판을 사용할 때 검색 조건을 구체화하기 위해 세부 정보를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="d7c31-232">리소스 요구 사항을 편집하려면 다음 단계를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="d7c31-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="d7c31-233">**팀** 탭의 **프로젝트** 페이지에서 일반 리소스의 요구 사항에 대한 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="d7c31-234">표시되는 **리소스 요구 사항** 페이지에서 여러 특성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="d7c31-235">다음 몇 가지 예를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d7c31-235">Here are some examples:</span></span>

    - <span data-ttu-id="d7c31-236">이름</span><span class="sxs-lookup"><span data-stu-id="d7c31-236">Name</span></span>
    - <span data-ttu-id="d7c31-237">시작 날짜</span><span class="sxs-lookup"><span data-stu-id="d7c31-237">From Date</span></span>
    - <span data-ttu-id="d7c31-238">종료 날짜</span><span class="sxs-lookup"><span data-stu-id="d7c31-238">To Date</span></span>
    - <span data-ttu-id="d7c31-239">기간</span><span class="sxs-lookup"><span data-stu-id="d7c31-239">Duration</span></span>
    - <span data-ttu-id="d7c31-240">리소스 유형</span><span class="sxs-lookup"><span data-stu-id="d7c31-240">Resource Type</span></span>

<span data-ttu-id="d7c31-241">**리소스 요구 사항** 페이지에서 프로젝트 관리자 또는 리소스 관리자는 다음 정보를 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="d7c31-242">기술</span><span class="sxs-lookup"><span data-stu-id="d7c31-242">Skills</span></span>
- <span data-ttu-id="d7c31-243">Roles</span><span class="sxs-lookup"><span data-stu-id="d7c31-243">Roles</span></span>
- <span data-ttu-id="d7c31-244">리소스 선호 설정</span><span class="sxs-lookup"><span data-stu-id="d7c31-244">Resource preferences</span></span>
- <span data-ttu-id="d7c31-245">선호 조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="d7c31-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="d7c31-246">프로젝트에서 예약한 후 리소스 예약 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7c31-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="d7c31-247">프로젝트 팀에 일반 또는 명명된 리소스를 추가한 후 리소스의 예약을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="d7c31-248">**팀** 탭의 **프로젝트** 페이지에서 팀 구성원을 선택하고 **예약 유지** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![선택한 팀 구성원에 대한 일정 게시판 열림](media/Resource-Management-image40.png)

    <span data-ttu-id="d7c31-250">일정 게시판이 나타나고 프로젝트 팀 구성원의 예약을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="d7c31-251">팀 구성원의 레코드를 확장하여 이 프로젝트및 팀 구성원의 생산 능력을 사용하는 다른 프로젝트에 대해 예약된 시간을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="d7c31-252">예약을 선택하고 드래그하여 연장하거나 단축합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="d7c31-253">예약을 조정할 수 있는 **리소스 예약 만들기** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![리소스 예약 만들기 대화 상자](media/Resource-Management-image41.png)

3. <span data-ttu-id="d7c31-255">예약을 마우스 오른쪽 버튼으로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-255">Right-click the booking.</span></span> <span data-ttu-id="d7c31-256">그런 다음 바로 가기 메뉴를 사용하여 다음 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="d7c31-257">예약 상태를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-257">Change the booking status.</span></span>
    - <span data-ttu-id="d7c31-258">예약 편집</span><span class="sxs-lookup"><span data-stu-id="d7c31-258">Edit the booking.</span></span>
    - <span data-ttu-id="d7c31-259">프로젝트 팀의 리소스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="d7c31-260">예약 상태를 변경합니다</span><span class="sxs-lookup"><span data-stu-id="d7c31-260">Change the booking status</span></span>

<span data-ttu-id="d7c31-261">기본 또는 사용자 지정 예약 상태를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-261">You can change any default or custom booking status.</span></span>

![상태 변경 명령](media/Resource-Management-image42.png)

<span data-ttu-id="d7c31-263">다음과 같은 상태가 PSA에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="d7c31-264">**취소됨** - 이 상태는 리소스의 예약을 취소하고 리소스의 생산 능력을 확보합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="d7c31-265">**확정 예약** - 이 상태는 리소스의 생산 능력을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="d7c31-266">일반적으로 **프로젝트** 페이지의 **모든 팀 구성원** 표에서 **예약 유지** 를 열 때 이 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="d7c31-267">**가예약** - 이 상태는 팀에 리소스를 추가하지만 리소스의 생산 능력을 소비하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="d7c31-268">리소스가 잠재적인 작업에 대해 예약되었지만 다른 작업에 필요한 경우 생산 능력이 여전히 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="d7c31-269">전반적인 리소스 가용성을 고려할 때 가예약은 확정 예약과 다른 상태를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="d7c31-270">**제안됨** - 이 상태는 리소스 관리자 또는 프로젝트 관리자의 리소스 제안을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="d7c31-271">제안은 리소스의 생산 능력을 사용하지 않으며 리소스가 프로젝트 팀에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="d7c31-272">팀에서 리소스를 확정 예약하려면 프로젝트 관리자가 제안을 수락해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="d7c31-273">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="d7c31-273">Submit resource requests</span></span>

<span data-ttu-id="d7c31-274">리소스 요청은 리소스 관리자가 수행해야 하는 요구(리소스 요청 사항)을 수행하기 위해 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="d7c31-275">팀에 이미 있는 일반 리소스의 경우 리소스 요청을 직접 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="d7c31-276">리소스 요청은 다음 두 가지 방법으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="d7c31-277">리소스 관리자는 요청을 직접 이행합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="d7c31-278">이 경우 일반 리소스는 명명된 리소스가 있는 확정 예약으로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="d7c31-279">리소스 관리자는 프로젝트 관리자에게 리소스를 제안하고 프로젝트 관리자는 제안된 리소스를 승인하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="d7c31-280">리소스 요청의 직접 이행</span><span class="sxs-lookup"><span data-stu-id="d7c31-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="d7c31-281">리소스 요구 사항이 생성되면 프로젝트 관리자는 리소스를 선택한 다음 **요청 제출** 을 선택하여 일반 리소스에 대한 리소스 요청을 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![요청 제출 단추](media/Resource-Management-image45.png)

<span data-ttu-id="d7c31-283">리소스에 대한 주석은 요청을 충족하는 리소스 관리자에게 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="d7c31-284">요청이 제출되면 팀 구성원의 **상태** 필드가 **제출됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![선택 사항 주석 입력](media/Resource-Management-image46.png)

<span data-ttu-id="d7c31-286">리소스 관리자가 요청을 이행하면 일반 팀 구성원이 **모든 팀 구성원** 표의 명명된 리소스로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![일반 팀 구성원이 모든 팀 구성원 표의 명명된 리소스로 대체되었습니다.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="d7c31-288">리소스 요청에 리소스 제안 사용</span><span class="sxs-lookup"><span data-stu-id="d7c31-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="d7c31-289">리소스 관리자는 리소스 요청에 대한 리소스를 직접 예약하는 대신 프로젝트 관리자에게 리소스를 제안할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="d7c31-290">리소스 관리자는 요구 사항에 대한 정확한 일치를 사용할 수 없는 경우 이 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="d7c31-291">리소스 관리자가 리소스를 제안하면 프로젝트 관리자는 일반 팀 구성원의 **상태** 필드가 **검토 필요** 로 변경된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![일반 팀 구성원의 상태가 검토 필요로 변경됨](media/Resource-Management-image48.png)

<span data-ttu-id="d7c31-293">제안된 리소스를 제안서 예약의 효과에 대한 시각화와 함께 보려면 **검토 필요** 상태가 있는 팀 구성원을 두 번클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="d7c31-294">그런 다음 **제안된 리소스** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-294">Then select the **Proposed Resources** tab.</span></span>

![제안된 리소스 탭](media/Resource-Management-image49.png)

<span data-ttu-id="d7c31-296">**모든 제안 수락** 을 선택하여 모든 제안된 리소스를 수락하하거나 **모든 제안 거부** 를 눌러서 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="d7c31-297">제안된 리소스를 수락하면 프로젝트에서 팀 구성원으로 확정 예약되고 일반 리소스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="d7c31-298">제안된 모든 리소스를 수락하거나 거부해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="d7c31-299">부분적으로 수락하거나 거부할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="d7c31-300">프로젝트 팀의 리소스를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="d7c31-301">경우에 따라 프로젝트 관리자는 프로젝트에서 예약된 팀 구성원을 대체해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="d7c31-302">**팀** 탭의 **프로젝트** 페이지에서 대체가 필요한 리소스를 선택하고 **예약 유지** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="d7c31-303">리소스를 확장하여 할당된 프로젝트를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![할당된 프로젝트를 표시하도록 확장된 리소스](media/Resource-Management-image50.png)

3. <span data-ttu-id="d7c31-305">프로젝트를 마우스 오른쪽 단추로 클릭한다음 **리소스 대체** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="d7c31-306">현재 리소스를 대체할 리소스를 알고 있는 경우 이름을 선택하거나 입력한 다음 **다시 할당** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![대체 리소스 지정](media/Resource-Management-image51.png)

    <span data-ttu-id="d7c31-308">또는 다음 단계를 수행하여 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="d7c31-309">**대체 찾기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-309">Select **Find Substitution**.</span></span>

        ![대체 리소스 검색](media/Resource-Management-image52.png)

        <span data-ttu-id="d7c31-311">일정 도우미는 사용 가능한 대체의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="d7c31-312">일정 도우미에서 사용 가능한 리소스를 추가로 필터링하여 적절한 대체 리소스를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![사용 가능한 대체 목록](media/Resource-Management-image53.png)

    2. <span data-ttu-id="d7c31-314">리소스를 대체하려면 원하는 리소스를 선택한 다음 **대체** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![대체 리소스 선택됨](media/Resource-Management-image54.png)

    <span data-ttu-id="d7c31-316">예약 및 할당은 새 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![예약 및 할당이 새 리소스로 대체됨](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="d7c31-318">팀 구성원 예약 및 할당 조정</span><span class="sxs-lookup"><span data-stu-id="d7c31-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="d7c31-319">팀 구성원의 경우 예약 및 할당이 느슨하게 결합됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="d7c31-320">즉, 리소스는 할당을 가질 수 있지만 예약은 없을 수도 있고, 예약을 할 수 있지만 할당은 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="d7c31-321">예약과 할당은 정렬되는 것이 좋습니다. 그래야 리소스가 작업 할당을 수행할 수 있는 생산 능력이 이행됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="d7c31-322">그러나 예약은 가용성을 기반으로 할 수 있으며 프로젝트가 계속됨에 따라 작업 타이밍이 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="d7c31-323">따라서 예약과 할당의 느슨한 결합은 유연성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="d7c31-324">PSA에는 프로젝트 관리자가 프로젝트 팀을 위한 팀원 예약과 배정을 조정하게 해주는 **조정** 탭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![조정 탭](media/Resource-Management-image56.png)

<span data-ttu-id="d7c31-326">**조정** 탭은 각 팀 구성원에 대해 개별 작업 할당의 수준으로 내려가는 예약 및 할당을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="d7c31-327">그것은 셀에 수 개월~수 일의 기간을 나타내는 시간을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="d7c31-328">탭에는 총 열과 함께 프로젝트의 전체 순합계도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="d7c31-329">각 리소스에 대해 탭은 팀 구성원의 예약과 해당 팀원의 과업 할당 롤업 사이의 차이를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="d7c31-330">이상적으로는 이 차이가 0(제로)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="d7c31-331">즉, 리소스의 예약과 작업 할당 사이에 차이가 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="d7c31-332">차이점은 두 가지 조건에 주의를 끌기 위한 색상과 그늘입니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="d7c31-333">**예약 부족** – 리소스에 예약보다 많은 작업이 있을 때 예약 부족이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="d7c31-334">이 능력은 예약되지 않았므로 프로젝트 관리자는 부족을 충당하기 위해 리소스 예약을 연장하여 이 조건을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="d7c31-335">**초과 예약** – 리소스가 프로젝트에 예약되었지만 과업에 할당되지 않은 경우 초과 예약이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="d7c31-336">작업 할당이 발생하기 전에 리소스가 프로젝트에 예약된 경우 이 조건을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="d7c31-337">그러나 다른 경우에는 작업에 이 리소스를 할당할 계획이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="d7c31-338">이러한 경우 프로젝트 관리자는 다른 프로젝트에 능력을 사용할 수 있도록 리소스의 예약을 취소하는 것을 고려해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="d7c31-339">경우에 따라 일 수준(예: 월 수준)보다 높은 수준에서 시간을 볼 때 리소스에 대한 순 차이(예: 예약 = 할당)가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="d7c31-340">그러나 주 수준의 시간을 살펴보면 첫 주에 0시간의 할당과 40시간의 예약을 볼 수 있지만, 두 번째 주에 40시간의 할당과 0시간의 예약이 있는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="d7c31-341">전반적으로, 예약 및 할당은 조정되지만 1주일에서 다음 주까지 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="d7c31-342">더 높은 시간 수준을 볼 때 **조정** 탭의 셀은 낮은 수준에 차이가 있음을 알리는 표시등이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="d7c31-343">셀을 두 번 클릭하여 확대하고 차이를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="d7c31-344">그런 다음 마우스 오른쪽 단추로 클릭하여 축소할 수 있습니다. 리소스를 선택한 다음 그리드 도구 모음에서 **다음 차이** 컨트롤을 사용하여 해당 리소스에 대한 예약과 할당 간의 다음 차이로 이동하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="d7c31-345">그런 다음 **이전 차이** 컨트롤을 사용하여 다시 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="d7c31-346">**설정** 에서 차이 표시기 및 탐색 동작을 해제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![차이 표시기](media/Resource-Management-image57.png)

<span data-ttu-id="d7c31-348">리소스에 대한 작업 할당이 있지만 예약이 없는 경우, **조정** 탭의 **프로젝트** 페이지에서 예약 부족을 선택한 다음 **예약 연장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="d7c31-349">**예약 연장** 대화 상자가 나타나고 리소스 부족을 해결하는 데 필요한 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="d7c31-350">또한 모든 프로젝트 또는 기타 예약 가능한 엔터티에서 리소스의 기존 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="d7c31-351">리소스의 가용성에 관계없이 리소스에 대한 예약을 만들려면 **확인** 을 선택하면 초과 예약이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![예약 연장 대화 상자](media/Resource-Management-image58.png)

<span data-ttu-id="d7c31-353">그런 다음 프로젝트 관리자 또는 리소스 관리자는 일정 게시판을 사용해서 리소스가 생산 능력을 초과해서 예약된 모든 상황을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c31-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
