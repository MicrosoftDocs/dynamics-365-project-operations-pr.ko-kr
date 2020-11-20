---
title: 작업 세분화 구조를 위한 업그레이드 고려 사항
description: 이 항목은 작업 세분화 구조를 Project Service Automation 2.x에서 3.x로 업그레이드하는 방법을 설명합니다.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121811"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="99c13-103">작업 세분화 구조를 위한 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="99c13-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="99c13-104">이 항목은 작업 세분화 구조를 Project Service Automation 2.x에서 3.x로 업그레이드하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="99c13-105">이 항목은 Project Service Automation(PSA)에서 성공적인 업그레이드를 위해 요구되는 건전한 프로젝트의 상태를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="99c13-106">업그레이드를 실패하게 만드는 일반적인 차단 조건에 대한 정보도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="99c13-107">프로젝트 스케줄 내에서 프로젝트 과업 및 그 기능을 정의하는 데 대한 자세한 설명은 [프로젝트 스케줄](project-creating.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="99c13-108">주요 엔터티</span><span class="sxs-lookup"><span data-stu-id="99c13-108">Key entities</span></span>
<span data-ttu-id="99c13-109">리소스가 이미 로드된 정확한 작업 세분화 구조의 경우 다음 엔터티가 요구됩니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="99c13-110">프로젝트</span><span class="sxs-lookup"><span data-stu-id="99c13-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="99c13-111">프로젝트 팀</span><span class="sxs-lookup"><span data-stu-id="99c13-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="99c13-112">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="99c13-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="99c13-113">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="99c13-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="99c13-114">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="99c13-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="99c13-115">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="99c13-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="99c13-116">리소스가 로드한 작업 세분화 구조를 정의하려면 다음 단계를 완료해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="99c13-117">새 프로젝트 만들기.</span><span class="sxs-lookup"><span data-stu-id="99c13-117">Create a new project.</span></span> <span data-ttu-id="99c13-118">새 프로젝트를 만드는 방법에 대한 자세한 설명은 [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="99c13-119">하나 이상의 과업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-119">Create one or more tasks.</span></span> <span data-ttu-id="99c13-120">과업을 만드는 방법에 대한 자세한 설명은 [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="99c13-121">과업 종속성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-121">Define the task dependencies.</span></span> <span data-ttu-id="99c13-122">자세한 내용은 [프로젝트 작업 종속성](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99c13-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="99c13-123">프로젝트에 프로젝트 팀원을 배정합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-123">Assign project team members to the project.</span></span> <span data-ttu-id="99c13-124">자세한 설명은 [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="99c13-125">과업에 프로젝트 팀원을 배정합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="99c13-126">자세한 설명은 [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="99c13-127">프로젝트 팀 관계</span><span class="sxs-lookup"><span data-stu-id="99c13-127">Project team relationships</span></span>

<span data-ttu-id="99c13-128">성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="99c13-129">모든 프로젝트 팀원이 예약 가능한 리소스와 연계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="99c13-130">모든 프로젝트 팀원이 같은 프로젝트와 연계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="99c13-131">프로젝트 과업 관계</span><span class="sxs-lookup"><span data-stu-id="99c13-131">Project task relationships</span></span>
<span data-ttu-id="99c13-132">성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="99c13-133">관련 과업은 동일한 프로젝트와 연계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="99c13-134">모든 행 과업에는 상위 과업이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="99c13-135">모든 과업에는 상위 프로젝트가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="99c13-136">유효한 조건</span><span class="sxs-lookup"><span data-stu-id="99c13-136">Valid conditions</span></span>

- <span data-ttu-id="99c13-137">모든 과업 기간은 1시간보다 크거나 같아야 하며(>=) 1,800,000분(1,250일)보다 작아야 합니다.\*</span><span class="sxs-lookup"><span data-stu-id="99c13-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="99c13-138">모든 과업은 시작 날짜가 2000/01/01 이후여야 합니다.\*</span><span class="sxs-lookup"><span data-stu-id="99c13-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="99c13-139">모든 과업은 현재 날짜로부터 17년 이내의 시작 날짜가 있어야 합니다.\*</span><span class="sxs-lookup"><span data-stu-id="99c13-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="99c13-140">모든 과업은 시작 날짜가 완료 날짜보다 일찍 또는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="99c13-141">분류에 대한 모든 처리 타입(경비, 자재, 세금 및 시간)에는 **기본 단위** 및 **단위 그룹** 에 대한 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="99c13-142">문자가 있는 날짜 형식은 피해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="99c13-143">잠재적인 완화 단계</span><span class="sxs-lookup"><span data-stu-id="99c13-143">Potential mitigation steps</span></span>
- <span data-ttu-id="99c13-144">상세하게 찾기를 사용하여 프로젝트 ID가없는 프로젝트 작업을 식별하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="99c13-145">예약된 기간이 1,800,000보다 큰 프로젝트 작업을 식별하려면 상세하게 찾기를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="99c13-146">데이터를 변경하기 전에 데이터를 불량 상태로 만드는 엔터티와 관련된 사용자 지정 내용을 조사해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="99c13-147">이러한 사용자 지정은 데이터 관련 업데이트를 진행하기 전에 해결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="99c13-148">연결된 프로젝트가 없는 것으로 식별된 작업이 필요하지 않거나 올바른 상위 프로젝트와 연관되어야 하는 경우 해당 작업을 삭제하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="99c13-149">기간이 1,250일을 초과하는 작업의 경우 가능하다면 전체 기간을 나타내는 여러 작업을 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="99c13-150">별표(\*)로 표시된 항목에는 고객 관계 관리(CRM) 시스템이 7,320번의 되풀이 확장만 지원함으로 인한 한도가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="99c13-151">이 한도 밑으로 유지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="99c13-152">리소스 할당 관계</span><span class="sxs-lookup"><span data-stu-id="99c13-152">Resource Assignment relationships</span></span>
<span data-ttu-id="99c13-153">성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="99c13-154">작업 분할 구조의 모든 리소스 할당은 동일한 프로젝트에 관련되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="99c13-155">작업 분할 구조의 모든 리소스 할당은 동일한 프로젝트의 프로젝트 팀원들과 연계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="99c13-156">잠재적인 완화 단계</span><span class="sxs-lookup"><span data-stu-id="99c13-156">Potential mitigation steps</span></span>
- <span data-ttu-id="99c13-157">위에서 설명한 조건을 벗어나는 모든 작업을 식별하십시오.</span><span class="sxs-lookup"><span data-stu-id="99c13-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="99c13-158">더 이상 유효하지 않은 리소스 할당은 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="99c13-159">프로젝트 과업 종속성 관계</span><span class="sxs-lookup"><span data-stu-id="99c13-159">Project task dependency relationships</span></span>
<span data-ttu-id="99c13-160">성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="99c13-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="99c13-161">모든 프로젝트 과업 종속성은 동일한 프로젝트에 관련되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="99c13-162">과업은 두 번 이상 참조된 동일한 종속성을 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="99c13-162">A task can't have the same dependency referenced more than once.</span></span>
