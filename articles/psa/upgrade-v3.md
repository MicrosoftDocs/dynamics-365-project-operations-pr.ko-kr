---
title: 업그레이드 고려 사항 - Microsoft Dynamics 365 Project Service Automation 버전 2.x or 1.x에서 버전 3
description: 이 항목은 Project Service Automation 버전 2.x 또는 1.x에서 버전 3으로 업그레이드할 때 고려해야 할 사항에 대한 정보를 제공합니다.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121721"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a><span data-ttu-id="8cecb-103">업그레이드 고려 사항 - PSA 버전 2.x 또는 1.x에서 버전 3</span><span class="sxs-lookup"><span data-stu-id="8cecb-103">Upgrade considerations - PSA version 2.x or 1.x to version 3</span></span>
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a><span data-ttu-id="8cecb-104">Project Service Automation 및 Field Service</span><span class="sxs-lookup"><span data-stu-id="8cecb-104">Project Service Automation and Field Service</span></span>
<span data-ttu-id="8cecb-105">Dynamics 365 Project Service Automation과 Dynamics 365 Field Service 모두 리소스 스케줄링에 URS(Universal Resourcing Scheduling) 솔루션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-105">Both Dynamics 365 Project Service Automation and Dynamics 365 Field Service use the Universal Resourcing Scheduling (URS) solution for resource scheduling.</span></span> <span data-ttu-id="8cecb-106">인스턴스에 Project Service Automation과 Field Service가 모두 있는 경우 두 솔루션을 모두 최신 버전(Project Service Automation의 경우 버전 3.x, Field Service의 경우 버전 8.x)으로 업그레이드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-106">If you have both Project Service Automation and Field Service in your instance, you should plan on upgrading both solutions to the latest version (version 3.x for Project Service Automation, version 8.x for Field Service).</span></span> <span data-ttu-id="8cecb-107">Project Service Automation 또는 Field Service를 업그레이드하면 최신 버전의 URS가 설치되므로 동일한 인스턴스의 Project Service Automation 및 Field Service 솔루션이 모두 최신 버전으로 업그레이드되지 않으면 일관성 없는 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-107">Upgrading Project Service Automation or Field Service will install the latest version of URS, which means that inconsistent behavior is possible if both Project Service Automation and Field Service solutions in the same instance aren’t upgraded to the latest version.</span></span>

## <a name="resource-assignments"></a><span data-ttu-id="8cecb-108">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="8cecb-108">Resource assignments</span></span>
<span data-ttu-id="8cecb-109">Project Service Automation 버전 2 및 버전 1에서 작업 할당은 **작업 엔터티** 의 하위 작업(라인 작업이라고도 함)으로 저장되고 **리소스 할당** 엔터티와 간접적으로 관련되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-109">In Project Service Automation version 2 and version 1, task assignments were stored as child tasks (also called line tasks) in the **Task entity**, and indirectly related to the **Resource Assignment** entity.</span></span> <span data-ttu-id="8cecb-110">WBS(작업 분할 구조)의 할당 팝업 창에서 라인 작업이 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-110">The line task was visible in the assignment pop-up window on the Work Breakdown Structure (WBS).</span></span>

![Project Service Automation 버전 2 및 버전 1의 WBS에서 라인 작업](media/upgrade-line-task-01.png)

<span data-ttu-id="8cecb-112">Project Service Automation 버전 3에서는 예약 가능한 리소스를 작업에 할당하는 기본 스키마가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-112">In version 3 of Project Service Automation, the underlying schema of assigning bookable resources to tasks has changed.</span></span> <span data-ttu-id="8cecb-113">라인 작업이 더 이상 사용되지 않았으며 **작업 엔터티** 의 작업과 **리소스 할당** 엔터티의 팀 구성원 간에 직접 1:1 관계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-113">The line task has been deprecated and there is a direct 1:1 relationship between the task in the **Task entity** and the team member in the **Resource Assignment** entity.</span></span> <span data-ttu-id="8cecb-114">이제 프로젝트 팀 구성원에게 할당된 작업이 리소스 할당 엔터티에 직접 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-114">Tasks that are assigned to a project team member are now stored directly in the Resource Assignment entity.</span></span>  

<span data-ttu-id="8cecb-115">이러한 변경 사항은 프로젝트 팀의 명명된 예약 가능 리소스 및 일반 리소스에 대한 리소스 할당이 있는 기존 프로젝트의 업그레이드에 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-115">These changes impact the upgrade of any existing projects that have resource assignments for named bookable resources and generic resources on a project team.</span></span> <span data-ttu-id="8cecb-116">이 주제는 버전 3으로 업그레이드할 때 프로젝트에 대해 고려해야 할 사항을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-116">This topic provides the considerations that you will need to take into account for your projects when you upgrade to version 3.</span></span> 

### <a name="tasks-assigned-to-named-resources"></a><span data-ttu-id="8cecb-117">명명된 리소스에 할당된 작업</span><span class="sxs-lookup"><span data-stu-id="8cecb-117">Tasks assigned to named resources</span></span>
<span data-ttu-id="8cecb-118">기본 작업 엔터티를 사용하여 버전 2 및 버전 1의 작업을 통해 팀 구성원은 기본 정의된 역할 이외의 역할을 묘사할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-118">Using the underlying task entity, tasks in version 2 and version 1 allowed team members to portray a role other than their default defined role.</span></span> <span data-ttu-id="8cecb-119">예를 들어 기본적으로 프로그램 관리자의 역할을 할당 받은 박지민 씨는 개발자 역할을 수행하는 작업에 할당될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-119">For example, Gracie George, who’s by default assigned the role of Program Manager, could be assigned to a task with the role of Developer.</span></span> <span data-ttu-id="8cecb-120">버전 3에서 명명된 팀 멤버의 역할은 항상 기본값이므로 박지민 씨가 할당된 모든 작업은 프로그램 관리자의 기본 역할을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-120">In version 3, the role of a named team member is always the default, so any task that Gracie George is assigned to uses her default role of Program Manager.</span></span>

<span data-ttu-id="8cecb-121">버전 2 및 버전 1의 기본 역할 이외의 작업에 리소스를 할당한 경우 업그레이드할 때 명명된 리소스는 버전 2의 역할 할당에 관계없이 모든 작업 할당에 대한 기본 역할이 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-121">If you have assigned a resource to a task outside of their default role in version 2 and version 1, when you upgrade, the named resource will be assigned the default role for all task assignments, regardless of role assignment in version 2.</span></span> <span data-ttu-id="8cecb-122">이렇게 하면 라인 작업 할당이 아닌 리소스의 역할에 따라 예측이 계산되므로 버전 2 또는 버전 1에서 버전 3까지 계산된 예상이 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-122">This will result in differences in the calculated estimates from version 2 or version 1 to version 3 because estimates are calculated based on the role of the resource and not the line task assignment.</span></span> <span data-ttu-id="8cecb-123">예를 들어 버전 2에서는 김은주 씨에게 두 가지 작업이 할당되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-123">For example, in version 2, two tasks have been assigned to Ashley Chinn.</span></span> <span data-ttu-id="8cecb-124">작업 1의 라인 작업에 대한 역할은 개발자이며 작업 2의 경우 프로그램 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-124">The role on the line task for task 1 is Developer and for task 2, Program Manager.</span></span> <span data-ttu-id="8cecb-125">김은주 씨는 프로그램 관리자의 기본 역할이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-125">Ashley Chinn has the default role of Program Manager.</span></span>

![하나의 리소스에 할당된 여러 역할](media/upgrade-multiple-roles-02.png)

<span data-ttu-id="8cecb-127">개발자 및 프로그램 관리자의 역할이 다르기 때문에 비용 및 영업 예상은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-127">Because the roles of Developer and Program Manager differ, the cost and sales estimates are as follows:</span></span>

![리소스 역할에 대한 비용 예상](media/upggrade-cost-estimates-03.png)

![리소스 역할에 대한 영업 예상](media/upgrade-sales-estimates-04.png)

<span data-ttu-id="8cecb-130">버전 3으로 업그레이드하면 라인 작업이 예약 가능한 리소스 팀 구성원의 작업에 대한 리소스 할당으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-130">When you upgrade to version 3, line tasks are replaced with resource assignments on the task of the bookable resource team member.</span></span> <span data-ttu-id="8cecb-131">할당은 예약 가능한 리소스의 기본 역할을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-131">The assignment will use the default role of the bookable resource.</span></span> <span data-ttu-id="8cecb-132">다음 그래픽에서 프로그램 관리자 역할을 맡고 있는 김은주 씨가 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-132">In the following graphic, Ashley Chinn who has a role of Program Manager, is the resource.</span></span>

![리소스 할당](media/resource-assignment-v2-05.png)

<span data-ttu-id="8cecb-134">예상은 리소스의 기본 역할을 기반으로 하므로 영업 및 비용 예상이 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-134">Because the estimates are based on the default role for the resource, the sales and cost estimates may change.</span></span> <span data-ttu-id="8cecb-135">다음 그래픽에서는 이제 예약 가능한 리소스의 기본 역할에서 역할이 수행되었으므로 **개발자** 역할이 더 이상 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-135">Note that in the following graphic, you no longer see the **Developer** role as the role is now taken from the bookable resource’s default role.</span></span>

<span data-ttu-id="8cecb-136">![기본 역할에 대한 비용 예상](media/resource-assignment-cost-estimate-06.png)
![기본 역할에 대한 영업 예상](media/resource-assignment-sales-estimate-07.png)</span><span class="sxs-lookup"><span data-stu-id="8cecb-136">![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Sales estimate for default roles](media/resource-assignment-sales-estimate-07.png)</span></span>

<span data-ttu-id="8cecb-137">업그레이드가 완료된 후에 팀 구성원의 역할을 할당된 기본값이 아닌 다른 역할로 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-137">After upgrade is complete, you can edit a team member's role to be something other than the assigned default.</span></span> <span data-ttu-id="8cecb-138">그러나 팀 구성원 역할을 변경하면 팀 구성원이 버전 3에서 여러 역할을 더 이상 할당할 수 없기 때문에 할당된 모든 작업에서 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-138">However, if you change a team members role, it will be changed on all of their assigned tasks because team members are no longer allowed to be assigned multiple roles in version 3.</span></span>

![리소스 역할 업데이트](media/resource-role-assignment-08.png)

<span data-ttu-id="8cecb-140">리소스의 조직 구성 단위를 기본값에서 다른 조직 구성 단위로 변경할 때 명명된 리소스에 할당된 라인 작업에도 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-140">This is also true for line tasks that were assigned to named resources when you change the resource’s organization unit from the default to another organization unit.</span></span> <span data-ttu-id="8cecb-141">버전 3 업그레이드가 완료되면 할당은 라인 작업에 설정된 대신 리소스의 기본 조직 구성 단위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-141">After the version 3 upgrade is complete, the assignment will use the resource’s default organization unit instead of the one set on the line task.</span></span>

### <a name="tasks-assigned-to-generic-resources"></a><span data-ttu-id="8cecb-142">일반 리소스에 할당된 작업</span><span class="sxs-lookup"><span data-stu-id="8cecb-142">Tasks assigned to generic resources</span></span>
<span data-ttu-id="8cecb-143">버전 2 및 버전 1에서는 작업에서 역할 및 조직 단위를 설정한 다음 **팀 생성** 기능을 사용하여 작업에 설정된 특성에 따라 일반 리소스를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-143">In version 2 and version 1, you can set the role and org unit on a task and then use the **Generate team** feature to generate generic resources based on the attributes set on the task.</span></span> <span data-ttu-id="8cecb-144">버전 3에서는 역할 및 조직 단위를 사용하여 일반 팀 구성원을 만든 다음 팀 구성원을 작업에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-144">In version 3, you create the generic team members with role and org unit, and then assign the team members to tasks.</span></span>

<span data-ttu-id="8cecb-145">버전 2 및 버전 1에서는 일반 리소스가 있는 프로젝트가 두 상태이거나 작업 수준에서 둘 다를 혼합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-145">In version 2 and version 1, projects with generic resources can be in two states, or a mix of both at the task level.</span></span> <span data-ttu-id="8cecb-146">예를 들어 다음과 같은 데이터를 가지고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-146">For example, you can have the following scenarios:</span></span>

- <span data-ttu-id="8cecb-147">작업에 역할 및 조직 구성 단위가 설정되었지만, 관련 리소스 할당이 생성되지는 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-147">Tasks with roles and org units set, but no affiliated resource assignment has been generated.</span></span>
- <span data-ttu-id="8cecb-148">**팀 생성** 기능을 사용하여 일반 리소스를 만들어 할당된 일반 팀 구성원 리소스 할당이 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-148">Tasks with generic team member resource assignments that were assigned by creating generic resource using the **Generate team** feature.</span></span>

<span data-ttu-id="8cecb-149">업그레이드를 시작하기 전에 일반 리소스에 할당된 작업이 있거나 아직 팀 생성 프로세스가 실행되지 않은 각 프로젝트에 대해 팀을 다시 생성하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-149">Before you begin your upgrade, we recommend that you re-generate the team for each project that has tasks assigned to generic resources or has yet to have the generate team process run on them.</span></span>

<span data-ttu-id="8cecb-150">**팀 생성** 으로 생성된 일반 팀 구성원에게 할당된 작업의 경우 업그레이드는 팀의 일반 리소스를 떠나 해당 일반 팀 구성원에게 할당을 남깁니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-150">For tasks that are assigned to generic team members that were generated with **Generate Team**, the upgrade will leave the generic resource on the team and leave the assignment to that generic team member.</span></span> <span data-ttu-id="8cecb-151">업그레이드 후 리소스 요청을 예약하거나 제출하기 전에 일반 팀 구성원에 대한 리소스 요구 사항을 생성하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-151">We recommend that you generate the resource requirement for the generic team member after the upgrade but before you book or submit a resource request.</span></span> <span data-ttu-id="8cecb-152">이렇게 하면 프로젝트의 계약 조직 구성 단위와 다른 일반 팀 구성원의 조직 구성 단위 할당이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-152">This will preserve any org unit assignments on the generic team members that are different than the project’s contracting org unit.</span></span>

<span data-ttu-id="8cecb-153">예를 들어 프로젝트 Z 프로젝트에서 계약 조직 구성 단위는 Contoso US입니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-153">For example, in the Project Z project, the contracting org unit is Contoso US.</span></span> <span data-ttu-id="8cecb-154">프로젝트 계획에서 구현 단계 내의 테스트 작업은 기술 컨설턴트 역할을 할당받았으며 할당된 조직 구성 단위는 Contoso India입니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-154">In the project plan, testing tasks within the Implementation phase have been assigned the role Technical Consultant and the assigned org unit is Contoso India.</span></span>

![구현 단계 조직 할당](media/org-unit-assignment-09.png)

<span data-ttu-id="8cecb-156">구현 단계 후 통합 테스트 작업은 기술 컨설턴트 역할에 할당되지만 조직은 Contoso US로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-156">After the implementation phase, the integration test task is assigned to the role Technical consultant, but the org is set to Contoso US.</span></span>  

![통합 테스트 작업 조직 할당](media/org-unit-generate-team-10.png)

<span data-ttu-id="8cecb-158">프로젝트에 대한 팀을 생성할 때 작업의 다른 조직 구성 단위로 인해 두 개의 일반 팀 구성원이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-158">When you generate a team for the project, two generic team members are created due to the different org units on the tasks.</span></span> <span data-ttu-id="8cecb-159">기술 컨설턴트 1은 Contoso India 작업을 할당하고 기술 컨설턴트 2는 Contoso US 작업을 해야합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-159">Technical consultant 1 will be assigned the Contoso India tasks and Technical consultant 2 will have the Contoso US tasks.</span></span>  

![생성된 일반 팀 구성원](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> <span data-ttu-id="8cecb-161">Project Service Automation 버전 2 및 버전 1에서 팀 구성원은 라인 작업에서 유지되는 조직 구성 단위를 보유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-161">In Project Service Automation version 2 and version 1, the team member does not hold the organization unit, that is maintained on the line task.</span></span>

![Project Service Automation의 버전 2 및 버전 1 라인 작업](media/line-tasks-12.png)

<span data-ttu-id="8cecb-163">예상 보기에서 조직 구성 단위를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-163">You can see the organization unit on the estimates view.</span></span> 

![조직 구성 단위 예상](media/org-unit-estimates-view-13.png)
 
<span data-ttu-id="8cecb-165">업그레이드가 완료되면 일반 팀 구성원에 해당하는 라인 작업의 조직 구성 단위가 일반 팀 구성원에 추가되고 라인 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-165">When the upgrade is complete, the organization unit on the line task that corresponds to the generic team member is added to the generic team member and the line task is removed.</span></span> <span data-ttu-id="8cecb-166">따라서 업그레이드하기 전에 일반 리소스가 포함된 각 프로젝트에서 팀을 생성하거나 다시 생성하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-166">Because of this, we recommend that before you upgrade, you generate or re-generate the team on each project that contains generic resources.</span></span>

<span data-ttu-id="8cecb-167">계약 프로젝트의 조직 구성 단위와 다른 조직 구성 단위가 있는 역할에 할당되고, 팀이 생성되지 않은 작업의 경우 업그레이드는 역할에 대한 일반 팀 구성원을 만들지만, 팀 구성원의 조직 구성 단위 프로젝트에 프로젝트의 계약 단위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-167">For tasks that are assigned to a role with an org unit that differs from the org unit of the contracting project, and a team has not been generated, upgrade will create a generic team member for the role, but will use the contracting unit of the project for the team member's org unit.</span></span> <span data-ttu-id="8cecb-168">프로젝트 Z의 예제를 다시 참조하면 계약 조직 단위 Contoso US와 구현 단계 내의 프로젝트 계획 테스트 작업이 Contoso India에 할당된 조직 단위의 기술 컨설턴트 역할을 할당되었음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-168">Referring back to the example with Project Z, this means that the contracting org unit Contoso US, and the project plan testing tasks within the Implementation phase have been assigned the role Technical Consultant with the org unit assigned to Contoso India.</span></span> <span data-ttu-id="8cecb-169">구현 단계 후에 완료된 구현 테스트 작업은 기술 컨설턴트 역할에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-169">The Integration test task that is completed after the Implementation phase has been assigned to the role Technical consultant.</span></span> <span data-ttu-id="8cecb-170">조직 구성 단위는 Contoso US이며 팀이 생성되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-170">The org unit is Contoso US and a team has not been generated.</span></span> <span data-ttu-id="8cecb-171">업그레이드는 하나의 일반 팀 구성원, 세 가지 작업의 할당된 시간을 포함하는 기술 컨설턴트 및 프로젝트의 계약 조직 구성 단위인 Contoso US의 조직 구성 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-171">Upgrade will create one generic team member, a Technical consultant that has the assigned hours of all three tasks, and an org unit of Contoso US, the project’s contracting org unit.</span></span>   
 
<span data-ttu-id="8cecb-172">생성되지 않은 팀 구성원에 대한 다른 소싱 조직 단위의 기본값을 변경하는 이유는 조직 구성 단위 할당이 수행되지 않도록 업그레이드 전에 일반 리소스가 포함된 각 프로젝트에서 팀을 생성하거나 다시 생성하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8cecb-172">Changing the default of the different resourcing org units on un-generated team members is the reason we recommend that you generate or re-generate the team on each project that contains generic resources prior to the upgrade so that the org unit assignments are not lost.</span></span>

