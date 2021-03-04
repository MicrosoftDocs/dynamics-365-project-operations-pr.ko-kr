---
title: 리소스 관리 변경 (Project Service Automation 3.x)
description: 이 항목은 리소스 관리 영역의 변경에 대한 정보를 제공합니다.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148651"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="5cb47-103">리소스 관리 변경 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="5cb47-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="5cb47-104">이 주제의 섹션들은 Dynamics 365 Project Service Automation 버전 3.x의 리소스 관리 영역에 대한 변경에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="5cb47-105">프로젝트 추산</span><span class="sxs-lookup"><span data-stu-id="5cb47-105">Project estimates</span></span>

<span data-ttu-id="5cb47-106">프로젝트 추산은 **msdyn\_projecttask** 엔터티(**프로젝트 과업**)을 기반으로 하는 대신, **msdyn\_resourceassignment** 엔터티(**리소스 할당**)에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="5cb47-107">리소스 할당은 과업 스케줄링 및 가격 책정을 위한 "진실의 원천"이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="5cb47-108">행 과업</span><span class="sxs-lookup"><span data-stu-id="5cb47-108">Line tasks</span></span>

<span data-ttu-id="5cb47-109">PSA 3.x에서는 행 과업이 더 이상 사용되지 않습니다(단종됨).</span><span class="sxs-lookup"><span data-stu-id="5cb47-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="5cb47-110">이제 할당이 행 과업 대신 전체 과업을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="5cb47-111">다음 예는 이전 버전의 PSA 및 PSA 3.x에서 "테스트 과업"이라는 명칭의 과업이 팀원 A와 B에게 할당되는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="5cb47-112">**PSA 3.x 이전:**</span><span class="sxs-lookup"><span data-stu-id="5cb47-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="5cb47-113">테스트 과업</span><span class="sxs-lookup"><span data-stu-id="5cb47-113">Test task</span></span>

        - <span data-ttu-id="5cb47-114">테스트 과업 – 행 과업 1</span><span class="sxs-lookup"><span data-stu-id="5cb47-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="5cb47-115">A에게 할당</span><span class="sxs-lookup"><span data-stu-id="5cb47-115">Assignment to A</span></span>

        - <span data-ttu-id="5cb47-116">테스트 과업 – 행 과업 2</span><span class="sxs-lookup"><span data-stu-id="5cb47-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="5cb47-117">B에게 할당</span><span class="sxs-lookup"><span data-stu-id="5cb47-117">Assignment to B</span></span>

- <span data-ttu-id="5cb47-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="5cb47-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="5cb47-119">테스트 과업</span><span class="sxs-lookup"><span data-stu-id="5cb47-119">Test task</span></span>

        - <span data-ttu-id="5cb47-120">A에게 할당</span><span class="sxs-lookup"><span data-stu-id="5cb47-120">Assignment to A</span></span>
        - <span data-ttu-id="5cb47-121">B에게 할당</span><span class="sxs-lookup"><span data-stu-id="5cb47-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="5cb47-122">할당되지 않은 과제</span><span class="sxs-lookup"><span data-stu-id="5cb47-122">Unassigned assignment</span></span>

<span data-ttu-id="5cb47-123">PSA 3.x에서 할당되지 않은 과제는 **NULL** 팀원과 **NULL** 리소스에 할당된 과제입니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="5cb47-124">할당되지 않은 과제는 다음과 같은 몇 가지 시나리오에서 발생할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="5cb47-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="5cb47-125">과업이 만들어졌지만 아직 팀원에게 할당되지 않은 경우 할당되지 않은 과제가 항상 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="5cb47-126">과업의 모든 피지정인이 제거되면 해당 과업에 대해 할당되지 않은 과제가 다시 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="5cb47-127">프로젝트 과업 엔터티에서의 스케줄링 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="5cb47-128">**msdyn\_projecttask** 엔터티의 필드가 더 이상 사용되지 않거나 **msdyn\_resourceassignment** 엔터티로 이동되었거나, 이제는 **msdyn\_projectteam** 엔터티(**프로젝트 팀원**)에서 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="5cb47-129">msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="5cb47-130">msdyn\_resourceassignment(리소스 할당)에서의 새 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="5cb47-131">설명</span><span class="sxs-lookup"><span data-stu-id="5cb47-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="5cb47-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="5cb47-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="5cb47-133">없음</span><span class="sxs-lookup"><span data-stu-id="5cb47-133">None</span></span> | |
| <span data-ttu-id="5cb47-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="5cb47-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="5cb47-135">없음</span><span class="sxs-lookup"><span data-stu-id="5cb47-135">None</span></span> | |
| <span data-ttu-id="5cb47-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="5cb47-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="5cb47-137">없음</span><span class="sxs-lookup"><span data-stu-id="5cb47-137">None</span></span> | |
| <span data-ttu-id="5cb47-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="5cb47-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="5cb47-139">없음</span><span class="sxs-lookup"><span data-stu-id="5cb47-139">None</span></span> | |
| <span data-ttu-id="5cb47-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="5cb47-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="5cb47-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="5cb47-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="5cb47-142">필드에 저장된 JSON(JavaScript 개체 표기형) 데이터 구조의 형식이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="5cb47-143">스케줄 등고선</span><span class="sxs-lookup"><span data-stu-id="5cb47-143">Schedule contour</span></span>

<span data-ttu-id="5cb47-144">스케줄 등고선은 각 **리소스 할당** 엔터티(**msdyn\_resourceassignment**)의 **계획된 작업** 필드(**msdyn\_plannedwork**)에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="5cb47-145">구조</span><span class="sxs-lookup"><span data-stu-id="5cb47-145">Structure</span></span>

<span data-ttu-id="5cb47-146">스케줄 등고선의 새 구조는 스케줄의 각 일에 대해 정의된 유연한 시간 조각으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="5cb47-147">각 시간 조각은 다음 속성들을 갖습니다:</span><span class="sxs-lookup"><span data-stu-id="5cb47-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="5cb47-148">**시작** – 프로젝트 캘린더에 따른 그 날 작업 시간의 시작입니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="5cb47-149">**끝** – 프로젝트 캘린더에 따른 그 날 작업 시간의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="5cb47-150">**시간 수** – 당일 할당된 시간 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="5cb47-151">**예제**</span><span class="sxs-lookup"><span data-stu-id="5cb47-151">**Example**</span></span>

<span data-ttu-id="5cb47-152">이 예는 작업일이 UTC-8 표준 시간대에서 오전 9시부터 오후 5시까지인 프로젝트 캘린더를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="5cb47-153">자동 스케줄링 및 수동 스케줄링</span><span class="sxs-lookup"><span data-stu-id="5cb47-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="5cb47-154">과업이 자동으로 스케줄링된 경우 시간이 미리 로드되고 과업 기간이 단축될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="5cb47-155">**예제**</span><span class="sxs-lookup"><span data-stu-id="5cb47-155">**Example**</span></span>

<span data-ttu-id="5cb47-156">다음 과업은 3일(2018년 12월 3일~ 2018년 12월 5일)에 걸친 18시간을 위해 자동으로 스케줄링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="5cb47-157">과업이 수동으로 스케줄링된 경우 시간 수는 모든 날짜에 균등하게 분배됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="5cb47-158">**예제**</span><span class="sxs-lookup"><span data-stu-id="5cb47-158">**Example**</span></span>

<span data-ttu-id="5cb47-159">다음 과업은 3일(2018년 12월 3일~ 2018년 12월 5일)에 걸친 18시간을 위해 수동으로 스케줄링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="5cb47-160">할당 단위</span><span class="sxs-lookup"><span data-stu-id="5cb47-160">Assignment unit</span></span>

<span data-ttu-id="5cb47-161">할당 단위는 PSA 3.x에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="5cb47-162">이제 과업 노력 시간 수는 할당된 모든 리소스들 사이에 일당으로 균등하게 나뉩니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="5cb47-163">**예**</span><span class="sxs-lookup"><span data-stu-id="5cb47-163">**Example**</span></span>

<span data-ttu-id="5cb47-164">이 예에서는 과업이 두 리소스에게 할당되고 3일에 걸친 36시간을 위해 자동 스케줄링됩니다(2018년 12월 3일~ 2018년 12월 5일).</span><span class="sxs-lookup"><span data-stu-id="5cb47-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="5cb47-165">할당 1:</span><span class="sxs-lookup"><span data-stu-id="5cb47-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="5cb47-166">할당 2:</span><span class="sxs-lookup"><span data-stu-id="5cb47-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="5cb47-167">가격 차원</span><span class="sxs-lookup"><span data-stu-id="5cb47-167">Pricing dimensions</span></span>

<span data-ttu-id="5cb47-168">PSA 3.x에서 리소스별 가격 책정 차원 필드(예: **역할** 및 **조직 단위**)가 **msdyn\_projecttask** 엔터티에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="5cb47-169">이제 프로젝트 추산이 생성될 때 리소스 할당(**msdyn\_resourceassignment**)의 해당 프로젝트 팀원(**msdyn\_projectteam**)에서 이러한 필드를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="5cb47-170">**msdyn\_organizationalunit** 라는 새 필드가 **msdyn\_projectteam** 엔터티에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="5cb47-171">msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="5cb47-172">대신 사용되는 msdyn\_projectteam(프로젝트 팀원)의 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="5cb47-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5cb47-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="5cb47-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5cb47-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="5cb47-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="5cb47-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="5cb47-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="5cb47-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="5cb47-177">등고선</span><span class="sxs-lookup"><span data-stu-id="5cb47-177">Contours</span></span>

<span data-ttu-id="5cb47-178">가격 책정 및 추산 등고선 필드는 **msdyn\_projecttask** 엔터티에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="5cb47-179">그들은 **msdyn\_resourceassignment** 엔터티로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5cb47-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="5cb47-180">msdyn\_projecttask(프로젝트 과업)에서 더 이상 사용되지 않는 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="5cb47-181">msdyn\_resourceassignment(리소스 할당)에서의 새 필드</span><span class="sxs-lookup"><span data-stu-id="5cb47-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="5cb47-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="5cb47-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="5cb47-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="5cb47-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="5cb47-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="5cb47-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="5cb47-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="5cb47-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="5cb47-186">다음 필드들이 **msdyn\_resourceassignment** 엔터티에 추가되었습니다:</span><span class="sxs-lookup"><span data-stu-id="5cb47-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="5cb47-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5cb47-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="5cb47-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5cb47-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="5cb47-189">**msdyn\_projecttask** 엔터티에서 계획된, 실제값 및 남은 비용 및 매출액에 대한 다음 필드들은 변경되지 않았습니다:</span><span class="sxs-lookup"><span data-stu-id="5cb47-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="5cb47-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5cb47-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="5cb47-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5cb47-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="5cb47-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="5cb47-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="5cb47-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="5cb47-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="5cb47-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5cb47-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="5cb47-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5cb47-195">msdyn\_remainingsales</span></span>
