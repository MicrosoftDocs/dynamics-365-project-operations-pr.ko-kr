---
title: 일정 엔터티로 일정 API를 사용하여 작업 수행
description: 이 항목은 일정 API 사용에 대한 정보와 샘플을 제공합니다.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950812"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="889eb-103">일정 엔터티로 일정 API를 사용하여 작업 수행</span><span class="sxs-lookup"><span data-stu-id="889eb-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="889eb-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="889eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="889eb-105">이 항목에 언급된 일부 또는 모든 기능은 미리 보기 릴리스의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="889eb-106">내용과 기능은 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="889eb-107">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="889eb-107">Scheduling entities</span></span>

<span data-ttu-id="889eb-108">일정 API는 **예약 엔터티** 를 통해 생성, 업데이트 및 삭제 작업을 수행할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="889eb-109">이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="889eb-110">**예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="889eb-111">다음 표는 **예약 엔터티** 전체 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="889eb-112">엔터티 이름</span><span class="sxs-lookup"><span data-stu-id="889eb-112">Entity name</span></span>  | <span data-ttu-id="889eb-113">엔터티 논리적 이름</span><span class="sxs-lookup"><span data-stu-id="889eb-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="889eb-114">Project</span><span class="sxs-lookup"><span data-stu-id="889eb-114">Project</span></span> | <span data-ttu-id="889eb-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="889eb-115">msdyn_project</span></span> |
| <span data-ttu-id="889eb-116">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="889eb-116">Project Task</span></span>  | <span data-ttu-id="889eb-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="889eb-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="889eb-118">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="889eb-118">Project Task Dependency</span></span>  | <span data-ttu-id="889eb-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="889eb-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="889eb-120">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="889eb-120">Resource Assignment</span></span> | <span data-ttu-id="889eb-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="889eb-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="889eb-122">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="889eb-122">Project Bucket</span></span>  | <span data-ttu-id="889eb-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="889eb-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="889eb-124">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="889eb-124">Project Team Member</span></span> | <span data-ttu-id="889eb-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="889eb-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="889eb-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="889eb-126">OperationSet</span></span>

<span data-ttu-id="889eb-127">OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="889eb-128">일정 API</span><span class="sxs-lookup"><span data-stu-id="889eb-128">Schedule APIs</span></span>

<span data-ttu-id="889eb-129">다음은 현재 일정 API 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="889eb-130">**msdyn_CreateProjectV1**: 이 API를 사용하여 프로젝트를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="889eb-131">프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="889eb-132">**msdyn_CreateTeamMemberV1**: 이 API를 사용하여 프로젝트 팀 구성원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="889eb-133">팀 구성원 레코드가 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="889eb-134">**msdyn_CreateOperationSetV1**: 이 API는 트랜잭션 내에서 수행해야 하는 여러 요청을 예약하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="889eb-135">**msdyn_PSSCreateV1**: 이 API는 엔터티를 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="889eb-136">엔터티는 만들기 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="889eb-137">**msdyn_PSSUpdateV1**: 이 API는 엔터티를 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="889eb-138">엔터티는 업데이트 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="889eb-139">**msdyn_PSSDeleteV1**: 이 API는 엔터티를 삭제하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="889eb-140">엔터티는 삭제 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="889eb-141">**msdyn_ExecuteOperationSetV1**: 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="889eb-142">OperationSet과 함께 일정 API 사용</span><span class="sxs-lookup"><span data-stu-id="889eb-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="889eb-143">**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="889eb-144">그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="889eb-145">지원되는 작업</span><span class="sxs-lookup"><span data-stu-id="889eb-145">Supported operations</span></span>

| <span data-ttu-id="889eb-146">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="889eb-146">Scheduling entity</span></span> | <span data-ttu-id="889eb-147">만들기</span><span class="sxs-lookup"><span data-stu-id="889eb-147">Create</span></span> | <span data-ttu-id="889eb-148">엽데이트</span><span class="sxs-lookup"><span data-stu-id="889eb-148">Update</span></span> | <span data-ttu-id="889eb-149">Delete</span><span class="sxs-lookup"><span data-stu-id="889eb-149">Delete</span></span> | <span data-ttu-id="889eb-150">중요 사항</span><span class="sxs-lookup"><span data-stu-id="889eb-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="889eb-151">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="889eb-151">Project task</span></span> | <span data-ttu-id="889eb-152">네</span><span class="sxs-lookup"><span data-stu-id="889eb-152">Yes</span></span> | <span data-ttu-id="889eb-153">네</span><span class="sxs-lookup"><span data-stu-id="889eb-153">Yes</span></span> | <span data-ttu-id="889eb-154">네</span><span class="sxs-lookup"><span data-stu-id="889eb-154">Yes</span></span> | <span data-ttu-id="889eb-155">없음</span><span class="sxs-lookup"><span data-stu-id="889eb-155">None</span></span> |
| <span data-ttu-id="889eb-156">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="889eb-156">Project task dependency</span></span> | <span data-ttu-id="889eb-157">네</span><span class="sxs-lookup"><span data-stu-id="889eb-157">Yes</span></span> | <span data-ttu-id="889eb-158">네</span><span class="sxs-lookup"><span data-stu-id="889eb-158">Yes</span></span> | | <span data-ttu-id="889eb-159">프로젝트 작업 종속성 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="889eb-160">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="889eb-161">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="889eb-161">Resource assignment</span></span> | <span data-ttu-id="889eb-162">네</span><span class="sxs-lookup"><span data-stu-id="889eb-162">Yes</span></span> | <span data-ttu-id="889eb-163">네</span><span class="sxs-lookup"><span data-stu-id="889eb-163">Yes</span></span> | | <span data-ttu-id="889eb-164">**BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="889eb-165">리소스 할당 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="889eb-166">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="889eb-167">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="889eb-167">Project bucket</span></span> | <span data-ttu-id="889eb-168">해당 없음</span><span class="sxs-lookup"><span data-stu-id="889eb-168">N/A</span></span> | <span data-ttu-id="889eb-169">해당 없음</span><span class="sxs-lookup"><span data-stu-id="889eb-169">N/A</span></span> | <span data-ttu-id="889eb-170">해당 없음</span><span class="sxs-lookup"><span data-stu-id="889eb-170">N/A</span></span> | <span data-ttu-id="889eb-171">기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="889eb-172">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="889eb-172">Project team member</span></span> | <span data-ttu-id="889eb-173">네</span><span class="sxs-lookup"><span data-stu-id="889eb-173">Yes</span></span> | <span data-ttu-id="889eb-174">네</span><span class="sxs-lookup"><span data-stu-id="889eb-174">Yes</span></span> | <span data-ttu-id="889eb-175">네</span><span class="sxs-lookup"><span data-stu-id="889eb-175">Yes</span></span> | <span data-ttu-id="889eb-176">생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="889eb-177">Project</span><span class="sxs-lookup"><span data-stu-id="889eb-177">Project</span></span> | <span data-ttu-id="889eb-178">네</span><span class="sxs-lookup"><span data-stu-id="889eb-178">Yes</span></span> | <span data-ttu-id="889eb-179">네</span><span class="sxs-lookup"><span data-stu-id="889eb-179">Yes</span></span> | <span data-ttu-id="889eb-180">해당 없음</span><span class="sxs-lookup"><span data-stu-id="889eb-180">N/A</span></span> | <span data-ttu-id="889eb-181">**StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="889eb-182">이러한 API는 사용자 지정 필드를 포함하는 엔터티 개체를 사용하여 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="889eb-183">ID 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-183">The ID property is optional.</span></span> <span data-ttu-id="889eb-184">제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="889eb-185">제공되지 않으면 시스템에서 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="889eb-186">제한된 필드</span><span class="sxs-lookup"><span data-stu-id="889eb-186">Restricted fields</span></span>

<span data-ttu-id="889eb-187">다음 표는 **생성** 및 **편집** 에서 제한되는 필드를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="889eb-188">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="889eb-188">Project task</span></span>

| <span data-ttu-id="889eb-189">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="889eb-189">**Logical name**</span></span>                       | <span data-ttu-id="889eb-190">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-190">**Can create**</span></span> | <span data-ttu-id="889eb-191">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="889eb-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="889eb-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="889eb-193">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-193">no</span></span>             | <span data-ttu-id="889eb-194">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-194">no</span></span>               |
| <span data-ttu-id="889eb-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="889eb-196">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-196">no</span></span>             | <span data-ttu-id="889eb-197">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-197">no</span></span>               |
| <span data-ttu-id="889eb-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="889eb-198">msdyn_actualend</span></span>                        | <span data-ttu-id="889eb-199">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-199">no</span></span>             | <span data-ttu-id="889eb-200">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-200">no</span></span>               |
| <span data-ttu-id="889eb-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="889eb-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="889eb-202">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-202">no</span></span>             | <span data-ttu-id="889eb-203">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-203">no</span></span>               |
| <span data-ttu-id="889eb-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="889eb-205">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-205">no</span></span>             | <span data-ttu-id="889eb-206">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-206">no</span></span>               |
| <span data-ttu-id="889eb-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="889eb-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="889eb-208">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-208">no</span></span>             | <span data-ttu-id="889eb-209">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-209">no</span></span>               |
| <span data-ttu-id="889eb-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="889eb-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="889eb-211">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-211">no</span></span>             | <span data-ttu-id="889eb-212">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-212">no</span></span>               |
| <span data-ttu-id="889eb-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="889eb-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="889eb-214">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-214">no</span></span>             | <span data-ttu-id="889eb-215">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-215">no</span></span>               |
| <span data-ttu-id="889eb-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="889eb-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="889eb-217">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-217">no</span></span>             | <span data-ttu-id="889eb-218">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-218">no</span></span>               |
| <span data-ttu-id="889eb-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="889eb-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="889eb-220">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-220">no</span></span>             | <span data-ttu-id="889eb-221">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-221">no</span></span>               |
| <span data-ttu-id="889eb-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="889eb-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="889eb-223">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-223">no</span></span>             | <span data-ttu-id="889eb-224">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-224">no</span></span>               |
| <span data-ttu-id="889eb-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="889eb-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="889eb-226">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-226">no</span></span>             | <span data-ttu-id="889eb-227">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-227">no</span></span>               |
| <span data-ttu-id="889eb-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="889eb-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="889eb-229">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-229">no</span></span>             | <span data-ttu-id="889eb-230">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-230">no</span></span>               |
| <span data-ttu-id="889eb-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="889eb-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="889eb-232">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-232">no</span></span>             | <span data-ttu-id="889eb-233">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-233">no</span></span>               |
| <span data-ttu-id="889eb-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="889eb-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="889eb-235">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-235">no</span></span>             | <span data-ttu-id="889eb-236">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-236">no</span></span>               |
| <span data-ttu-id="889eb-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="889eb-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="889eb-238">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-238">no</span></span>             | <span data-ttu-id="889eb-239">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-239">no</span></span>               |
| <span data-ttu-id="889eb-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="889eb-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="889eb-241">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-241">no</span></span>             | <span data-ttu-id="889eb-242">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-242">no</span></span>               |
| <span data-ttu-id="889eb-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="889eb-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="889eb-244">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-244">no</span></span>             | <span data-ttu-id="889eb-245">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-245">no</span></span>               |
| <span data-ttu-id="889eb-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="889eb-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="889eb-247">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-247">no</span></span>             | <span data-ttu-id="889eb-248">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-248">no</span></span>               |
| <span data-ttu-id="889eb-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="889eb-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="889eb-250">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-250">no</span></span>             | <span data-ttu-id="889eb-251">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-251">no</span></span>               |
| <span data-ttu-id="889eb-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="889eb-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="889eb-253">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-253">no</span></span>             | <span data-ttu-id="889eb-254">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-254">no</span></span>               |
| <span data-ttu-id="889eb-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="889eb-256">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-256">no</span></span>             | <span data-ttu-id="889eb-257">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-257">no</span></span>               |
| <span data-ttu-id="889eb-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="889eb-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="889eb-259">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-259">no</span></span>             | <span data-ttu-id="889eb-260">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-260">no</span></span>               |
| <span data-ttu-id="889eb-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="889eb-262">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-262">no</span></span>             | <span data-ttu-id="889eb-263">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-263">no</span></span>               |
| <span data-ttu-id="889eb-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="889eb-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="889eb-265">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-265">no</span></span>             | <span data-ttu-id="889eb-266">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-266">no</span></span>               |
| <span data-ttu-id="889eb-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="889eb-267">msdyn_progress</span></span>                         | <span data-ttu-id="889eb-268">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-268">no</span></span>             | <span data-ttu-id="889eb-269">아니요(P4W의 경우 예)</span><span class="sxs-lookup"><span data-stu-id="889eb-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="889eb-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="889eb-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="889eb-271">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-271">no</span></span>             | <span data-ttu-id="889eb-272">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-272">no</span></span>               |
| <span data-ttu-id="889eb-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="889eb-274">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-274">no</span></span>             | <span data-ttu-id="889eb-275">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-275">no</span></span>               |
| <span data-ttu-id="889eb-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="889eb-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="889eb-277">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-277">no</span></span>             | <span data-ttu-id="889eb-278">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-278">no</span></span>               |
| <span data-ttu-id="889eb-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="889eb-280">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-280">no</span></span>             | <span data-ttu-id="889eb-281">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-281">no</span></span>               |
| <span data-ttu-id="889eb-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="889eb-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="889eb-283">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-283">no</span></span>             | <span data-ttu-id="889eb-284">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-284">no</span></span>               |
| <span data-ttu-id="889eb-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="889eb-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="889eb-286">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-286">no</span></span>             | <span data-ttu-id="889eb-287">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-287">no</span></span>               |
| <span data-ttu-id="889eb-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="889eb-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="889eb-289">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-289">no</span></span>             | <span data-ttu-id="889eb-290">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-290">no</span></span>               |
| <span data-ttu-id="889eb-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="889eb-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="889eb-292">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-292">no</span></span>             | <span data-ttu-id="889eb-293">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-293">no</span></span>               |
| <span data-ttu-id="889eb-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="889eb-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="889eb-295">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-295">no</span></span>             | <span data-ttu-id="889eb-296">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-296">no</span></span>               |
| <span data-ttu-id="889eb-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="889eb-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="889eb-298">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-298">no</span></span>             | <span data-ttu-id="889eb-299">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-299">no</span></span>               |
| <span data-ttu-id="889eb-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="889eb-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="889eb-301">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-301">no</span></span>             | <span data-ttu-id="889eb-302">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-302">no</span></span>               |
| <span data-ttu-id="889eb-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="889eb-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="889eb-304">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-304">no</span></span>             | <span data-ttu-id="889eb-305">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-305">no</span></span>               |
| <span data-ttu-id="889eb-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="889eb-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="889eb-307">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-307">no</span></span>             | <span data-ttu-id="889eb-308">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-308">no</span></span>               |
| <span data-ttu-id="889eb-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="889eb-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="889eb-310">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-310">no</span></span>             | <span data-ttu-id="889eb-311">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-311">no</span></span>               |
| <span data-ttu-id="889eb-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="889eb-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="889eb-313">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-313">no</span></span>             | <span data-ttu-id="889eb-314">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-314">no</span></span>               |
| <span data-ttu-id="889eb-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="889eb-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="889eb-316">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-316">no</span></span>             | <span data-ttu-id="889eb-317">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-317">no</span></span>               |
| <span data-ttu-id="889eb-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="889eb-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="889eb-319">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-319">no</span></span>             | <span data-ttu-id="889eb-320">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-320">no</span></span>               |
| <span data-ttu-id="889eb-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="889eb-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="889eb-322">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-322">no</span></span>             | <span data-ttu-id="889eb-323">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-323">no</span></span>               |
| <span data-ttu-id="889eb-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="889eb-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="889eb-325">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-325">no</span></span>             | <span data-ttu-id="889eb-326">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-326">no</span></span>               |
| <span data-ttu-id="889eb-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="889eb-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="889eb-328">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-328">no</span></span>             | <span data-ttu-id="889eb-329">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-329">no</span></span>               |
| <span data-ttu-id="889eb-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="889eb-330">msdyn_summary</span></span>                          | <span data-ttu-id="889eb-331">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-331">no</span></span>             | <span data-ttu-id="889eb-332">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-332">no</span></span>               |
| <span data-ttu-id="889eb-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="889eb-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="889eb-334">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-334">no</span></span>             | <span data-ttu-id="889eb-335">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-335">no</span></span>               |
| <span data-ttu-id="889eb-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="889eb-337">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-337">no</span></span>             | <span data-ttu-id="889eb-338">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="889eb-339">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="889eb-339">Project task dependency</span></span>

| <span data-ttu-id="889eb-340">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="889eb-340">**Logical name**</span></span>              | <span data-ttu-id="889eb-341">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-341">**Can create**</span></span> | <span data-ttu-id="889eb-342">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="889eb-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="889eb-343">msdyn_linktype</span></span>                | <span data-ttu-id="889eb-344">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-344">no</span></span>             | <span data-ttu-id="889eb-345">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-345">no</span></span>           |
| <span data-ttu-id="889eb-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="889eb-346">msdyn_linktypename</span></span>            | <span data-ttu-id="889eb-347">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-347">no</span></span>             | <span data-ttu-id="889eb-348">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-348">no</span></span>           |
| <span data-ttu-id="889eb-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="889eb-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="889eb-350">예</span><span class="sxs-lookup"><span data-stu-id="889eb-350">yes</span></span>            | <span data-ttu-id="889eb-351">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-351">no</span></span>           |
| <span data-ttu-id="889eb-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="889eb-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="889eb-353">예</span><span class="sxs-lookup"><span data-stu-id="889eb-353">yes</span></span>            | <span data-ttu-id="889eb-354">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-354">no</span></span>           |
| <span data-ttu-id="889eb-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="889eb-355">msdyn_project</span></span>                 | <span data-ttu-id="889eb-356">예</span><span class="sxs-lookup"><span data-stu-id="889eb-356">yes</span></span>            | <span data-ttu-id="889eb-357">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-357">no</span></span>           |
| <span data-ttu-id="889eb-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="889eb-358">msdyn_projectname</span></span>             | <span data-ttu-id="889eb-359">예</span><span class="sxs-lookup"><span data-stu-id="889eb-359">yes</span></span>            | <span data-ttu-id="889eb-360">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-360">no</span></span>           |
| <span data-ttu-id="889eb-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="889eb-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="889eb-362">예</span><span class="sxs-lookup"><span data-stu-id="889eb-362">yes</span></span>            | <span data-ttu-id="889eb-363">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-363">no</span></span>           |
| <span data-ttu-id="889eb-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="889eb-364">msdyn_successortask</span></span>           | <span data-ttu-id="889eb-365">예</span><span class="sxs-lookup"><span data-stu-id="889eb-365">yes</span></span>            | <span data-ttu-id="889eb-366">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-366">no</span></span>           |
| <span data-ttu-id="889eb-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="889eb-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="889eb-368">예</span><span class="sxs-lookup"><span data-stu-id="889eb-368">yes</span></span>            | <span data-ttu-id="889eb-369">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="889eb-370">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="889eb-370">Resource assignment</span></span>

| <span data-ttu-id="889eb-371">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="889eb-371">**Logical name**</span></span>             | <span data-ttu-id="889eb-372">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-372">**Can create**</span></span> | <span data-ttu-id="889eb-373">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="889eb-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="889eb-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="889eb-375">예</span><span class="sxs-lookup"><span data-stu-id="889eb-375">yes</span></span>            | <span data-ttu-id="889eb-376">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-376">no</span></span>           |
| <span data-ttu-id="889eb-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="889eb-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="889eb-378">예</span><span class="sxs-lookup"><span data-stu-id="889eb-378">yes</span></span>            | <span data-ttu-id="889eb-379">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-379">no</span></span>           |
| <span data-ttu-id="889eb-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="889eb-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="889eb-381">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-381">no</span></span>             | <span data-ttu-id="889eb-382">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-382">no</span></span>           |
| <span data-ttu-id="889eb-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="889eb-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="889eb-384">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-384">no</span></span>             | <span data-ttu-id="889eb-385">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-385">no</span></span>           |
| <span data-ttu-id="889eb-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="889eb-386">msdyn_committype</span></span>             | <span data-ttu-id="889eb-387">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-387">no</span></span>             | <span data-ttu-id="889eb-388">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-388">no</span></span>           |
| <span data-ttu-id="889eb-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="889eb-389">msdyn_committypename</span></span>         | <span data-ttu-id="889eb-390">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-390">no</span></span>             | <span data-ttu-id="889eb-391">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-391">no</span></span>           |
| <span data-ttu-id="889eb-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="889eb-392">msdyn_effort</span></span>                 | <span data-ttu-id="889eb-393">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-393">no</span></span>             | <span data-ttu-id="889eb-394">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-394">no</span></span>           |
| <span data-ttu-id="889eb-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="889eb-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="889eb-396">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-396">no</span></span>             | <span data-ttu-id="889eb-397">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-397">no</span></span>           |
| <span data-ttu-id="889eb-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="889eb-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="889eb-399">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-399">no</span></span>             | <span data-ttu-id="889eb-400">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-400">no</span></span>           |
| <span data-ttu-id="889eb-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="889eb-401">msdyn_finish</span></span>                 | <span data-ttu-id="889eb-402">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-402">no</span></span>             | <span data-ttu-id="889eb-403">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-403">no</span></span>           |
| <span data-ttu-id="889eb-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="889eb-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="889eb-405">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-405">no</span></span>             | <span data-ttu-id="889eb-406">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-406">no</span></span>           |
| <span data-ttu-id="889eb-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="889eb-408">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-408">no</span></span>             | <span data-ttu-id="889eb-409">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-409">no</span></span>           |
| <span data-ttu-id="889eb-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="889eb-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="889eb-411">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-411">no</span></span>             | <span data-ttu-id="889eb-412">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-412">no</span></span>           |
| <span data-ttu-id="889eb-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="889eb-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="889eb-414">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-414">no</span></span>             | <span data-ttu-id="889eb-415">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-415">no</span></span>           |
| <span data-ttu-id="889eb-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="889eb-417">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-417">no</span></span>             | <span data-ttu-id="889eb-418">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-418">no</span></span>           |
| <span data-ttu-id="889eb-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="889eb-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="889eb-420">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-420">no</span></span>             | <span data-ttu-id="889eb-421">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-421">no</span></span>           |
| <span data-ttu-id="889eb-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="889eb-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="889eb-423">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-423">no</span></span>             | <span data-ttu-id="889eb-424">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-424">no</span></span>           |
| <span data-ttu-id="889eb-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="889eb-425">msdyn_projectid</span></span>              | <span data-ttu-id="889eb-426">예</span><span class="sxs-lookup"><span data-stu-id="889eb-426">yes</span></span>            | <span data-ttu-id="889eb-427">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-427">no</span></span>           |
| <span data-ttu-id="889eb-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="889eb-428">msdyn_projectidname</span></span>          | <span data-ttu-id="889eb-429">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-429">no</span></span>             | <span data-ttu-id="889eb-430">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-430">no</span></span>           |
| <span data-ttu-id="889eb-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="889eb-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="889eb-432">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-432">no</span></span>             | <span data-ttu-id="889eb-433">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-433">no</span></span>           |
| <span data-ttu-id="889eb-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="889eb-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="889eb-435">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-435">no</span></span>             | <span data-ttu-id="889eb-436">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-436">no</span></span>           |
| <span data-ttu-id="889eb-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="889eb-437">msdyn_start</span></span>                  | <span data-ttu-id="889eb-438">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-438">no</span></span>             | <span data-ttu-id="889eb-439">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-439">no</span></span>           |
| <span data-ttu-id="889eb-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="889eb-440">msdyn_taskid</span></span>                 | <span data-ttu-id="889eb-441">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-441">no</span></span>             | <span data-ttu-id="889eb-442">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-442">no</span></span>           |
| <span data-ttu-id="889eb-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="889eb-443">msdyn_taskidname</span></span>             | <span data-ttu-id="889eb-444">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-444">no</span></span>             | <span data-ttu-id="889eb-445">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-445">no</span></span>           |
| <span data-ttu-id="889eb-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="889eb-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="889eb-447">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-447">no</span></span>             | <span data-ttu-id="889eb-448">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="889eb-449">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="889eb-449">Project team member</span></span>

| <span data-ttu-id="889eb-450">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="889eb-450">**Logical name**</span></span>                                 | <span data-ttu-id="889eb-451">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-451">**Can create**</span></span> | <span data-ttu-id="889eb-452">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="889eb-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="889eb-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="889eb-454">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-454">no</span></span>             | <span data-ttu-id="889eb-455">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-455">no</span></span>           |
| <span data-ttu-id="889eb-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="889eb-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="889eb-457">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-457">no</span></span>             | <span data-ttu-id="889eb-458">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-458">no</span></span>           |
| <span data-ttu-id="889eb-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="889eb-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="889eb-460">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-460">no</span></span>             | <span data-ttu-id="889eb-461">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-461">no</span></span>           |
| <span data-ttu-id="889eb-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="889eb-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="889eb-463">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-463">no</span></span>             | <span data-ttu-id="889eb-464">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-464">no</span></span>           |
| <span data-ttu-id="889eb-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="889eb-465">msdyn_effort</span></span>                                     | <span data-ttu-id="889eb-466">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-466">no</span></span>             | <span data-ttu-id="889eb-467">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-467">no</span></span>           |
| <span data-ttu-id="889eb-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="889eb-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="889eb-469">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-469">no</span></span>             | <span data-ttu-id="889eb-470">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-470">no</span></span>           |
| <span data-ttu-id="889eb-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="889eb-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="889eb-472">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-472">no</span></span>             | <span data-ttu-id="889eb-473">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-473">no</span></span>           |
| <span data-ttu-id="889eb-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="889eb-474">msdyn_finish</span></span>                                     | <span data-ttu-id="889eb-475">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-475">no</span></span>             | <span data-ttu-id="889eb-476">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-476">no</span></span>           |
| <span data-ttu-id="889eb-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="889eb-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="889eb-478">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-478">no</span></span>             | <span data-ttu-id="889eb-479">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-479">no</span></span>           |
| <span data-ttu-id="889eb-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="889eb-480">msdyn_hours</span></span>                                      | <span data-ttu-id="889eb-481">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-481">no</span></span>             | <span data-ttu-id="889eb-482">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-482">no</span></span>           |
| <span data-ttu-id="889eb-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="889eb-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="889eb-484">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-484">no</span></span>             | <span data-ttu-id="889eb-485">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-485">no</span></span>           |
| <span data-ttu-id="889eb-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="889eb-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="889eb-487">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-487">no</span></span>             | <span data-ttu-id="889eb-488">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-488">no</span></span>           |
| <span data-ttu-id="889eb-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="889eb-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="889eb-490">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-490">no</span></span>             | <span data-ttu-id="889eb-491">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-491">no</span></span>           |
| <span data-ttu-id="889eb-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="889eb-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="889eb-493">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-493">no</span></span>             | <span data-ttu-id="889eb-494">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-494">no</span></span>           |
| <span data-ttu-id="889eb-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="889eb-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="889eb-496">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-496">no</span></span>             | <span data-ttu-id="889eb-497">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-497">no</span></span>           |
| <span data-ttu-id="889eb-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="889eb-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="889eb-499">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-499">no</span></span>             | <span data-ttu-id="889eb-500">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-500">no</span></span>           |
| <span data-ttu-id="889eb-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="889eb-501">msdyn_start</span></span>                                      | <span data-ttu-id="889eb-502">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-502">no</span></span>             | <span data-ttu-id="889eb-503">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="889eb-504">Project</span><span class="sxs-lookup"><span data-stu-id="889eb-504">Project</span></span>

| <span data-ttu-id="889eb-505">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="889eb-505">**Logical name**</span></span>                       | <span data-ttu-id="889eb-506">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-506">**Can create**</span></span> | <span data-ttu-id="889eb-507">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="889eb-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="889eb-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="889eb-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="889eb-509">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-509">no</span></span>             | <span data-ttu-id="889eb-510">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-510">no</span></span>           |
| <span data-ttu-id="889eb-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="889eb-512">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-512">no</span></span>             | <span data-ttu-id="889eb-513">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-513">no</span></span>           |
| <span data-ttu-id="889eb-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="889eb-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="889eb-515">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-515">no</span></span>             | <span data-ttu-id="889eb-516">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-516">no</span></span>           |
| <span data-ttu-id="889eb-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="889eb-518">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-518">no</span></span>             | <span data-ttu-id="889eb-519">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-519">no</span></span>           |
| <span data-ttu-id="889eb-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="889eb-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="889eb-521">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-521">no</span></span>             | <span data-ttu-id="889eb-522">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-522">no</span></span>           |
| <span data-ttu-id="889eb-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="889eb-524">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-524">no</span></span>             | <span data-ttu-id="889eb-525">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-525">no</span></span>           |
| <span data-ttu-id="889eb-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="889eb-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="889eb-527">예</span><span class="sxs-lookup"><span data-stu-id="889eb-527">yes</span></span>            | <span data-ttu-id="889eb-528">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-528">no</span></span>           |
| <span data-ttu-id="889eb-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="889eb-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="889eb-530">예</span><span class="sxs-lookup"><span data-stu-id="889eb-530">yes</span></span>            | <span data-ttu-id="889eb-531">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-531">no</span></span>           |
| <span data-ttu-id="889eb-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="889eb-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="889eb-533">예</span><span class="sxs-lookup"><span data-stu-id="889eb-533">yes</span></span>            | <span data-ttu-id="889eb-534">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-534">no</span></span>           |
| <span data-ttu-id="889eb-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="889eb-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="889eb-536">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-536">no</span></span>             | <span data-ttu-id="889eb-537">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-537">no</span></span>           |
| <span data-ttu-id="889eb-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="889eb-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="889eb-539">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-539">no</span></span>             | <span data-ttu-id="889eb-540">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-540">no</span></span>           |
| <span data-ttu-id="889eb-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="889eb-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="889eb-542">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-542">no</span></span>             | <span data-ttu-id="889eb-543">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-543">no</span></span>           |
| <span data-ttu-id="889eb-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="889eb-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="889eb-545">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-545">no</span></span>             | <span data-ttu-id="889eb-546">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-546">no</span></span>           |
| <span data-ttu-id="889eb-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="889eb-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="889eb-548">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-548">no</span></span>             | <span data-ttu-id="889eb-549">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-549">no</span></span>           |
| <span data-ttu-id="889eb-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="889eb-550">msdyn_duration</span></span>                         | <span data-ttu-id="889eb-551">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-551">no</span></span>             | <span data-ttu-id="889eb-552">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-552">no</span></span>           |
| <span data-ttu-id="889eb-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="889eb-553">msdyn_effort</span></span>                           | <span data-ttu-id="889eb-554">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-554">no</span></span>             | <span data-ttu-id="889eb-555">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-555">no</span></span>           |
| <span data-ttu-id="889eb-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="889eb-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="889eb-557">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-557">no</span></span>             | <span data-ttu-id="889eb-558">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-558">no</span></span>           |
| <span data-ttu-id="889eb-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="889eb-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="889eb-560">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-560">no</span></span>             | <span data-ttu-id="889eb-561">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-561">no</span></span>           |
| <span data-ttu-id="889eb-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="889eb-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="889eb-563">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-563">no</span></span>             | <span data-ttu-id="889eb-564">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-564">no</span></span>           |
| <span data-ttu-id="889eb-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="889eb-565">msdyn_finish</span></span>                           | <span data-ttu-id="889eb-566">예</span><span class="sxs-lookup"><span data-stu-id="889eb-566">yes</span></span>            | <span data-ttu-id="889eb-567">예</span><span class="sxs-lookup"><span data-stu-id="889eb-567">yes</span></span>          |
| <span data-ttu-id="889eb-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="889eb-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="889eb-569">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-569">no</span></span>             | <span data-ttu-id="889eb-570">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-570">no</span></span>           |
| <span data-ttu-id="889eb-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="889eb-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="889eb-572">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-572">no</span></span>             | <span data-ttu-id="889eb-573">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-573">no</span></span>           |
| <span data-ttu-id="889eb-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="889eb-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="889eb-575">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-575">no</span></span>             | <span data-ttu-id="889eb-576">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-576">no</span></span>           |
| <span data-ttu-id="889eb-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="889eb-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="889eb-578">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-578">no</span></span>             | <span data-ttu-id="889eb-579">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-579">no</span></span>           |
| <span data-ttu-id="889eb-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="889eb-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="889eb-581">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-581">no</span></span>             | <span data-ttu-id="889eb-582">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-582">no</span></span>           |
| <span data-ttu-id="889eb-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="889eb-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="889eb-584">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-584">no</span></span>             | <span data-ttu-id="889eb-585">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-585">no</span></span>           |
| <span data-ttu-id="889eb-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="889eb-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="889eb-587">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-587">no</span></span>             | <span data-ttu-id="889eb-588">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-588">no</span></span>           |
| <span data-ttu-id="889eb-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="889eb-590">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-590">no</span></span>             | <span data-ttu-id="889eb-591">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-591">no</span></span>           |
| <span data-ttu-id="889eb-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="889eb-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="889eb-593">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-593">no</span></span>             | <span data-ttu-id="889eb-594">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-594">no</span></span>           |
| <span data-ttu-id="889eb-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="889eb-596">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-596">no</span></span>             | <span data-ttu-id="889eb-597">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-597">no</span></span>           |
| <span data-ttu-id="889eb-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="889eb-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="889eb-599">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-599">no</span></span>             | <span data-ttu-id="889eb-600">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-600">no</span></span>           |
| <span data-ttu-id="889eb-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="889eb-602">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-602">no</span></span>             | <span data-ttu-id="889eb-603">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-603">no</span></span>           |
| <span data-ttu-id="889eb-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="889eb-604">msdyn_progress</span></span>                         | <span data-ttu-id="889eb-605">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-605">no</span></span>             | <span data-ttu-id="889eb-606">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-606">no</span></span>           |
| <span data-ttu-id="889eb-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="889eb-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="889eb-608">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-608">no</span></span>             | <span data-ttu-id="889eb-609">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-609">no</span></span>           |
| <span data-ttu-id="889eb-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="889eb-611">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-611">no</span></span>             | <span data-ttu-id="889eb-612">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-612">no</span></span>           |
| <span data-ttu-id="889eb-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="889eb-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="889eb-614">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-614">no</span></span>             | <span data-ttu-id="889eb-615">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-615">no</span></span>           |
| <span data-ttu-id="889eb-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="889eb-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="889eb-617">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-617">no</span></span>             | <span data-ttu-id="889eb-618">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-618">no</span></span>           |
| <span data-ttu-id="889eb-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="889eb-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="889eb-620">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-620">no</span></span>             | <span data-ttu-id="889eb-621">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-621">no</span></span>           |
| <span data-ttu-id="889eb-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="889eb-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="889eb-623">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-623">no</span></span>             | <span data-ttu-id="889eb-624">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-624">no</span></span>           |
| <span data-ttu-id="889eb-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="889eb-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="889eb-626">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-626">no</span></span>             | <span data-ttu-id="889eb-627">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-627">no</span></span>           |
| <span data-ttu-id="889eb-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="889eb-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="889eb-629">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-629">no</span></span>             | <span data-ttu-id="889eb-630">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-630">no</span></span>           |
| <span data-ttu-id="889eb-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="889eb-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="889eb-632">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-632">no</span></span>             | <span data-ttu-id="889eb-633">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-633">no</span></span>           |
| <span data-ttu-id="889eb-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="889eb-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="889eb-635">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-635">no</span></span>             | <span data-ttu-id="889eb-636">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-636">no</span></span>           |
| <span data-ttu-id="889eb-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="889eb-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="889eb-638">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-638">no</span></span>             | <span data-ttu-id="889eb-639">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-639">no</span></span>           |
| <span data-ttu-id="889eb-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="889eb-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="889eb-641">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-641">no</span></span>             | <span data-ttu-id="889eb-642">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-642">no</span></span>           |
| <span data-ttu-id="889eb-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="889eb-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="889eb-644">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-644">no</span></span>             | <span data-ttu-id="889eb-645">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-645">no</span></span>           |
| <span data-ttu-id="889eb-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="889eb-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="889eb-647">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-647">no</span></span>             | <span data-ttu-id="889eb-648">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-648">no</span></span>           |
| <span data-ttu-id="889eb-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="889eb-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="889eb-650">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-650">no</span></span>             | <span data-ttu-id="889eb-651">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-651">no</span></span>           |
| <span data-ttu-id="889eb-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="889eb-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="889eb-653">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-653">no</span></span>             | <span data-ttu-id="889eb-654">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-654">no</span></span>           |
| <span data-ttu-id="889eb-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="889eb-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="889eb-656">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-656">no</span></span>             | <span data-ttu-id="889eb-657">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-657">no</span></span>           |
| <span data-ttu-id="889eb-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="889eb-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="889eb-659">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-659">no</span></span>             | <span data-ttu-id="889eb-660">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-660">no</span></span>           |
| <span data-ttu-id="889eb-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="889eb-662">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-662">no</span></span>             | <span data-ttu-id="889eb-663">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-663">no</span></span>           |
| <span data-ttu-id="889eb-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="889eb-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="889eb-665">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-665">no</span></span>             | <span data-ttu-id="889eb-666">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-666">no</span></span>           |
| <span data-ttu-id="889eb-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="889eb-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="889eb-668">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-668">no</span></span>             | <span data-ttu-id="889eb-669">아니요</span><span class="sxs-lookup"><span data-stu-id="889eb-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="889eb-670">제한 사항 및 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="889eb-670">Limitations and known issues</span></span>
<span data-ttu-id="889eb-671">다음은 제한 사항 및 알려진 문제 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="889eb-672">일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="889eb-673">다음 사용자는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-673">They can't be used by:</span></span>
    - <span data-ttu-id="889eb-674">응용 프로그램 사용자</span><span class="sxs-lookup"><span data-stu-id="889eb-674">Application users</span></span>
    - <span data-ttu-id="889eb-675">시스템 사용자</span><span class="sxs-lookup"><span data-stu-id="889eb-675">System users</span></span>
    - <span data-ttu-id="889eb-676">통합 사용자</span><span class="sxs-lookup"><span data-stu-id="889eb-676">Integration users</span></span>
    - <span data-ttu-id="889eb-677">필요한 라이선스가 없는 다른 사용자</span><span class="sxs-lookup"><span data-stu-id="889eb-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="889eb-678">각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="889eb-679">각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="889eb-680">Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="889eb-681">**OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="889eb-682">일정 API는 공개 미리 보기입니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="889eb-683">프로덕션 환경에서 이러한 API를 사용하는 것은 Microsoft에서 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="889eb-684">프로젝트 및 작업에 대한 제한 및 경계</span><span class="sxs-lookup"><span data-stu-id="889eb-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="889eb-685">오류 처리</span><span class="sxs-lookup"><span data-stu-id="889eb-685">Error handling</span></span>

   - <span data-ttu-id="889eb-686">작업 세트에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **작업 세트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="889eb-687">Project Scheduling Service에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **PSS 오류 로그** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="889eb-688">샘플 시나리오</span><span class="sxs-lookup"><span data-stu-id="889eb-688">Sample scenario</span></span>

<span data-ttu-id="889eb-689">이 시나리오에서는 프로젝트, 팀 구성원, 4개의 작업 및 2개의 리소스 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="889eb-690">다음으로 하나의 작업을 업데이트하고, 프로젝트를 업데이트하고, 하나의 작업을 삭제하고, 하나의 리소스 할당을 삭제하고, 작업 종속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="889eb-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="889eb-691">추가 샘플</span><span class="sxs-lookup"><span data-stu-id="889eb-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
