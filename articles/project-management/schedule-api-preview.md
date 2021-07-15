---
title: 프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행
description: 이 항목은 프로젝트 일정 API를 사용하기 위한 정보 및 샘플을 제공합니다.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293235"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="b0378-103">프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행</span><span class="sxs-lookup"><span data-stu-id="b0378-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="b0378-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="b0378-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b0378-105">이 항목에 언급된 일부 또는 모든 기능은 미리 보기 릴리스의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="b0378-106">내용과 기능은 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="b0378-107">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="b0378-107">Scheduling entities</span></span>

<span data-ttu-id="b0378-108">프로젝트 일정 API는 **일정 엔터티** 를 사용하여 생성, 업데이트 및 삭제 작업을 수행하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="b0378-109">이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="b0378-110">**예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="b0378-111">다음 표는 프로젝트 일정 엔터티의 전체 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="b0378-112">엔터티 이름</span><span class="sxs-lookup"><span data-stu-id="b0378-112">Entity name</span></span>  | <span data-ttu-id="b0378-113">엔터티 논리적 이름</span><span class="sxs-lookup"><span data-stu-id="b0378-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="b0378-114">Project</span><span class="sxs-lookup"><span data-stu-id="b0378-114">Project</span></span> | <span data-ttu-id="b0378-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b0378-115">msdyn_project</span></span> |
| <span data-ttu-id="b0378-116">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="b0378-116">Project Task</span></span>  | <span data-ttu-id="b0378-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="b0378-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="b0378-118">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="b0378-118">Project Task Dependency</span></span>  | <span data-ttu-id="b0378-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="b0378-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="b0378-120">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="b0378-120">Resource Assignment</span></span> | <span data-ttu-id="b0378-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="b0378-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="b0378-122">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="b0378-122">Project Bucket</span></span>  | <span data-ttu-id="b0378-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="b0378-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="b0378-124">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="b0378-124">Project Team Member</span></span> | <span data-ttu-id="b0378-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="b0378-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="b0378-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="b0378-126">OperationSet</span></span>

<span data-ttu-id="b0378-127">OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="b0378-128">프로젝트 일정 API</span><span class="sxs-lookup"><span data-stu-id="b0378-128">Project schedule APIs</span></span>

<span data-ttu-id="b0378-129">다음은 현재 프로젝트 일정 API 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="b0378-130">**msdyn_CreateProjectV1**: 이 API를 사용하여 프로젝트를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="b0378-131">프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="b0378-132">**msdyn_CreateTeamMemberV1**: 이 API를 사용하여 프로젝트 팀 구성원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="b0378-133">팀 구성원 레코드가 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="b0378-134">**msdyn_CreateOperationSetV1**: 이 API는 트랜잭션 내에서 수행해야 하는 여러 요청을 예약하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="b0378-135">**msdyn_PSSCreateV1**: 이 API는 엔터티를 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="b0378-136">엔터티는 만들기 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="b0378-137">**msdyn_PSSUpdateV1**: 이 API는 엔터티를 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="b0378-138">엔터티는 업데이트 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="b0378-139">**msdyn_PSSDeleteV1**: 이 API는 엔터티를 삭제하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="b0378-140">엔터티는 삭제 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="b0378-141">**msdyn_ExecuteOperationSetV1**: 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="b0378-142">OperationSet와 함께 프로젝트 일정 API 사용</span><span class="sxs-lookup"><span data-stu-id="b0378-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="b0378-143">**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="b0378-144">그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="b0378-145">지원되는 작업</span><span class="sxs-lookup"><span data-stu-id="b0378-145">Supported operations</span></span>

| <span data-ttu-id="b0378-146">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="b0378-146">Scheduling entity</span></span> | <span data-ttu-id="b0378-147">만들기</span><span class="sxs-lookup"><span data-stu-id="b0378-147">Create</span></span> | <span data-ttu-id="b0378-148">엽데이트</span><span class="sxs-lookup"><span data-stu-id="b0378-148">Update</span></span> | <span data-ttu-id="b0378-149">Delete</span><span class="sxs-lookup"><span data-stu-id="b0378-149">Delete</span></span> | <span data-ttu-id="b0378-150">중요 사항</span><span class="sxs-lookup"><span data-stu-id="b0378-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="b0378-151">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="b0378-151">Project task</span></span> | <span data-ttu-id="b0378-152">네</span><span class="sxs-lookup"><span data-stu-id="b0378-152">Yes</span></span> | <span data-ttu-id="b0378-153">네</span><span class="sxs-lookup"><span data-stu-id="b0378-153">Yes</span></span> | <span data-ttu-id="b0378-154">네</span><span class="sxs-lookup"><span data-stu-id="b0378-154">Yes</span></span> | <span data-ttu-id="b0378-155">없음</span><span class="sxs-lookup"><span data-stu-id="b0378-155">None</span></span> |
| <span data-ttu-id="b0378-156">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="b0378-156">Project task dependency</span></span> | <span data-ttu-id="b0378-157">네</span><span class="sxs-lookup"><span data-stu-id="b0378-157">Yes</span></span> | <span data-ttu-id="b0378-158">네</span><span class="sxs-lookup"><span data-stu-id="b0378-158">Yes</span></span> | | <span data-ttu-id="b0378-159">프로젝트 작업 종속성 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="b0378-160">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b0378-161">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="b0378-161">Resource assignment</span></span> | <span data-ttu-id="b0378-162">네</span><span class="sxs-lookup"><span data-stu-id="b0378-162">Yes</span></span> | <span data-ttu-id="b0378-163">네</span><span class="sxs-lookup"><span data-stu-id="b0378-163">Yes</span></span> | | <span data-ttu-id="b0378-164">**BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="b0378-165">리소스 할당 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="b0378-166">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b0378-167">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="b0378-167">Project bucket</span></span> | <span data-ttu-id="b0378-168">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b0378-168">N/A</span></span> | <span data-ttu-id="b0378-169">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b0378-169">N/A</span></span> | <span data-ttu-id="b0378-170">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b0378-170">N/A</span></span> | <span data-ttu-id="b0378-171">기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="b0378-172">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="b0378-172">Project team member</span></span> | <span data-ttu-id="b0378-173">네</span><span class="sxs-lookup"><span data-stu-id="b0378-173">Yes</span></span> | <span data-ttu-id="b0378-174">네</span><span class="sxs-lookup"><span data-stu-id="b0378-174">Yes</span></span> | <span data-ttu-id="b0378-175">네</span><span class="sxs-lookup"><span data-stu-id="b0378-175">Yes</span></span> | <span data-ttu-id="b0378-176">생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="b0378-177">Project</span><span class="sxs-lookup"><span data-stu-id="b0378-177">Project</span></span> | <span data-ttu-id="b0378-178">네</span><span class="sxs-lookup"><span data-stu-id="b0378-178">Yes</span></span> | <span data-ttu-id="b0378-179">네</span><span class="sxs-lookup"><span data-stu-id="b0378-179">Yes</span></span> | <span data-ttu-id="b0378-180">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b0378-180">N/A</span></span> | <span data-ttu-id="b0378-181">**StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="b0378-182">이러한 API는 사용자 지정 필드를 포함하는 엔터티 개체를 사용하여 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="b0378-183">ID 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-183">The ID property is optional.</span></span> <span data-ttu-id="b0378-184">제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="b0378-185">제공되지 않으면 시스템에서 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="b0378-186">제한된 필드</span><span class="sxs-lookup"><span data-stu-id="b0378-186">Restricted fields</span></span>

<span data-ttu-id="b0378-187">다음 표는 **생성** 및 **편집** 에서 제한되는 필드를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="b0378-188">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="b0378-188">Project task</span></span>

| <span data-ttu-id="b0378-189">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="b0378-189">**Logical name**</span></span>                       | <span data-ttu-id="b0378-190">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-190">**Can create**</span></span> | <span data-ttu-id="b0378-191">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="b0378-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="b0378-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="b0378-193">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-193">no</span></span>             | <span data-ttu-id="b0378-194">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-194">no</span></span>               |
| <span data-ttu-id="b0378-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="b0378-196">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-196">no</span></span>             | <span data-ttu-id="b0378-197">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-197">no</span></span>               |
| <span data-ttu-id="b0378-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="b0378-198">msdyn_actualend</span></span>                        | <span data-ttu-id="b0378-199">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-199">no</span></span>             | <span data-ttu-id="b0378-200">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-200">no</span></span>               |
| <span data-ttu-id="b0378-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b0378-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="b0378-202">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-202">no</span></span>             | <span data-ttu-id="b0378-203">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-203">no</span></span>               |
| <span data-ttu-id="b0378-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b0378-205">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-205">no</span></span>             | <span data-ttu-id="b0378-206">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-206">no</span></span>               |
| <span data-ttu-id="b0378-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="b0378-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="b0378-208">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-208">no</span></span>             | <span data-ttu-id="b0378-209">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-209">no</span></span>               |
| <span data-ttu-id="b0378-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="b0378-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="b0378-211">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-211">no</span></span>             | <span data-ttu-id="b0378-212">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-212">no</span></span>               |
| <span data-ttu-id="b0378-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="b0378-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="b0378-214">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-214">no</span></span>             | <span data-ttu-id="b0378-215">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-215">no</span></span>               |
| <span data-ttu-id="b0378-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b0378-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="b0378-217">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-217">no</span></span>             | <span data-ttu-id="b0378-218">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-218">no</span></span>               |
| <span data-ttu-id="b0378-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b0378-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b0378-220">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-220">no</span></span>             | <span data-ttu-id="b0378-221">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-221">no</span></span>               |
| <span data-ttu-id="b0378-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b0378-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="b0378-223">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-223">no</span></span>             | <span data-ttu-id="b0378-224">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-224">no</span></span>               |
| <span data-ttu-id="b0378-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="b0378-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="b0378-226">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-226">no</span></span>             | <span data-ttu-id="b0378-227">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-227">no</span></span>               |
| <span data-ttu-id="b0378-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="b0378-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="b0378-229">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-229">no</span></span>             | <span data-ttu-id="b0378-230">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-230">no</span></span>               |
| <span data-ttu-id="b0378-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="b0378-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="b0378-232">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-232">no</span></span>             | <span data-ttu-id="b0378-233">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-233">no</span></span>               |
| <span data-ttu-id="b0378-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="b0378-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="b0378-235">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-235">no</span></span>             | <span data-ttu-id="b0378-236">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-236">no</span></span>               |
| <span data-ttu-id="b0378-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="b0378-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="b0378-238">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-238">no</span></span>             | <span data-ttu-id="b0378-239">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-239">no</span></span>               |
| <span data-ttu-id="b0378-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="b0378-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="b0378-241">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-241">no</span></span>             | <span data-ttu-id="b0378-242">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-242">no</span></span>               |
| <span data-ttu-id="b0378-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="b0378-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="b0378-244">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-244">no</span></span>             | <span data-ttu-id="b0378-245">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-245">no</span></span>               |
| <span data-ttu-id="b0378-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="b0378-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="b0378-247">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-247">no</span></span>             | <span data-ttu-id="b0378-248">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-248">no</span></span>               |
| <span data-ttu-id="b0378-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b0378-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="b0378-250">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-250">no</span></span>             | <span data-ttu-id="b0378-251">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-251">no</span></span>               |
| <span data-ttu-id="b0378-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b0378-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="b0378-253">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-253">no</span></span>             | <span data-ttu-id="b0378-254">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-254">no</span></span>               |
| <span data-ttu-id="b0378-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="b0378-256">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-256">no</span></span>             | <span data-ttu-id="b0378-257">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-257">no</span></span>               |
| <span data-ttu-id="b0378-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b0378-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b0378-259">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-259">no</span></span>             | <span data-ttu-id="b0378-260">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-260">no</span></span>               |
| <span data-ttu-id="b0378-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b0378-262">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-262">no</span></span>             | <span data-ttu-id="b0378-263">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-263">no</span></span>               |
| <span data-ttu-id="b0378-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="b0378-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="b0378-265">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-265">no</span></span>             | <span data-ttu-id="b0378-266">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-266">no</span></span>               |
| <span data-ttu-id="b0378-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b0378-267">msdyn_progress</span></span>                         | <span data-ttu-id="b0378-268">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-268">no</span></span>             | <span data-ttu-id="b0378-269">아니요(P4W의 경우 예)</span><span class="sxs-lookup"><span data-stu-id="b0378-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="b0378-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b0378-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b0378-271">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-271">no</span></span>             | <span data-ttu-id="b0378-272">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-272">no</span></span>               |
| <span data-ttu-id="b0378-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b0378-274">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-274">no</span></span>             | <span data-ttu-id="b0378-275">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-275">no</span></span>               |
| <span data-ttu-id="b0378-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b0378-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b0378-277">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-277">no</span></span>             | <span data-ttu-id="b0378-278">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-278">no</span></span>               |
| <span data-ttu-id="b0378-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b0378-280">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-280">no</span></span>             | <span data-ttu-id="b0378-281">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-281">no</span></span>               |
| <span data-ttu-id="b0378-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="b0378-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="b0378-283">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-283">no</span></span>             | <span data-ttu-id="b0378-284">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-284">no</span></span>               |
| <span data-ttu-id="b0378-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b0378-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="b0378-286">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-286">no</span></span>             | <span data-ttu-id="b0378-287">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-287">no</span></span>               |
| <span data-ttu-id="b0378-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="b0378-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="b0378-289">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-289">no</span></span>             | <span data-ttu-id="b0378-290">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-290">no</span></span>               |
| <span data-ttu-id="b0378-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b0378-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="b0378-292">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-292">no</span></span>             | <span data-ttu-id="b0378-293">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-293">no</span></span>               |
| <span data-ttu-id="b0378-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b0378-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="b0378-295">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-295">no</span></span>             | <span data-ttu-id="b0378-296">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-296">no</span></span>               |
| <span data-ttu-id="b0378-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b0378-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="b0378-298">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-298">no</span></span>             | <span data-ttu-id="b0378-299">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-299">no</span></span>               |
| <span data-ttu-id="b0378-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b0378-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="b0378-301">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-301">no</span></span>             | <span data-ttu-id="b0378-302">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-302">no</span></span>               |
| <span data-ttu-id="b0378-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b0378-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="b0378-304">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-304">no</span></span>             | <span data-ttu-id="b0378-305">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-305">no</span></span>               |
| <span data-ttu-id="b0378-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b0378-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b0378-307">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-307">no</span></span>             | <span data-ttu-id="b0378-308">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-308">no</span></span>               |
| <span data-ttu-id="b0378-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b0378-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b0378-310">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-310">no</span></span>             | <span data-ttu-id="b0378-311">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-311">no</span></span>               |
| <span data-ttu-id="b0378-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="b0378-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="b0378-313">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-313">no</span></span>             | <span data-ttu-id="b0378-314">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-314">no</span></span>               |
| <span data-ttu-id="b0378-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="b0378-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="b0378-316">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-316">no</span></span>             | <span data-ttu-id="b0378-317">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-317">no</span></span>               |
| <span data-ttu-id="b0378-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="b0378-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="b0378-319">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-319">no</span></span>             | <span data-ttu-id="b0378-320">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-320">no</span></span>               |
| <span data-ttu-id="b0378-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b0378-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b0378-322">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-322">no</span></span>             | <span data-ttu-id="b0378-323">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-323">no</span></span>               |
| <span data-ttu-id="b0378-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="b0378-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="b0378-325">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-325">no</span></span>             | <span data-ttu-id="b0378-326">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-326">no</span></span>               |
| <span data-ttu-id="b0378-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="b0378-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="b0378-328">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-328">no</span></span>             | <span data-ttu-id="b0378-329">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-329">no</span></span>               |
| <span data-ttu-id="b0378-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="b0378-330">msdyn_summary</span></span>                          | <span data-ttu-id="b0378-331">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-331">no</span></span>             | <span data-ttu-id="b0378-332">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-332">no</span></span>               |
| <span data-ttu-id="b0378-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="b0378-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="b0378-334">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-334">no</span></span>             | <span data-ttu-id="b0378-335">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-335">no</span></span>               |
| <span data-ttu-id="b0378-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="b0378-337">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-337">no</span></span>             | <span data-ttu-id="b0378-338">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="b0378-339">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="b0378-339">Project task dependency</span></span>

| <span data-ttu-id="b0378-340">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="b0378-340">**Logical name**</span></span>              | <span data-ttu-id="b0378-341">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-341">**Can create**</span></span> | <span data-ttu-id="b0378-342">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="b0378-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="b0378-343">msdyn_linktype</span></span>                | <span data-ttu-id="b0378-344">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-344">no</span></span>             | <span data-ttu-id="b0378-345">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-345">no</span></span>           |
| <span data-ttu-id="b0378-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="b0378-346">msdyn_linktypename</span></span>            | <span data-ttu-id="b0378-347">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-347">no</span></span>             | <span data-ttu-id="b0378-348">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-348">no</span></span>           |
| <span data-ttu-id="b0378-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="b0378-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="b0378-350">예</span><span class="sxs-lookup"><span data-stu-id="b0378-350">yes</span></span>            | <span data-ttu-id="b0378-351">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-351">no</span></span>           |
| <span data-ttu-id="b0378-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="b0378-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="b0378-353">예</span><span class="sxs-lookup"><span data-stu-id="b0378-353">yes</span></span>            | <span data-ttu-id="b0378-354">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-354">no</span></span>           |
| <span data-ttu-id="b0378-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b0378-355">msdyn_project</span></span>                 | <span data-ttu-id="b0378-356">예</span><span class="sxs-lookup"><span data-stu-id="b0378-356">yes</span></span>            | <span data-ttu-id="b0378-357">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-357">no</span></span>           |
| <span data-ttu-id="b0378-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="b0378-358">msdyn_projectname</span></span>             | <span data-ttu-id="b0378-359">예</span><span class="sxs-lookup"><span data-stu-id="b0378-359">yes</span></span>            | <span data-ttu-id="b0378-360">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-360">no</span></span>           |
| <span data-ttu-id="b0378-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="b0378-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="b0378-362">예</span><span class="sxs-lookup"><span data-stu-id="b0378-362">yes</span></span>            | <span data-ttu-id="b0378-363">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-363">no</span></span>           |
| <span data-ttu-id="b0378-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="b0378-364">msdyn_successortask</span></span>           | <span data-ttu-id="b0378-365">예</span><span class="sxs-lookup"><span data-stu-id="b0378-365">yes</span></span>            | <span data-ttu-id="b0378-366">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-366">no</span></span>           |
| <span data-ttu-id="b0378-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="b0378-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="b0378-368">예</span><span class="sxs-lookup"><span data-stu-id="b0378-368">yes</span></span>            | <span data-ttu-id="b0378-369">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="b0378-370">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="b0378-370">Resource assignment</span></span>

| <span data-ttu-id="b0378-371">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="b0378-371">**Logical name**</span></span>             | <span data-ttu-id="b0378-372">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-372">**Can create**</span></span> | <span data-ttu-id="b0378-373">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="b0378-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="b0378-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="b0378-375">예</span><span class="sxs-lookup"><span data-stu-id="b0378-375">yes</span></span>            | <span data-ttu-id="b0378-376">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-376">no</span></span>           |
| <span data-ttu-id="b0378-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="b0378-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="b0378-378">예</span><span class="sxs-lookup"><span data-stu-id="b0378-378">yes</span></span>            | <span data-ttu-id="b0378-379">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-379">no</span></span>           |
| <span data-ttu-id="b0378-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="b0378-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="b0378-381">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-381">no</span></span>             | <span data-ttu-id="b0378-382">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-382">no</span></span>           |
| <span data-ttu-id="b0378-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="b0378-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="b0378-384">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-384">no</span></span>             | <span data-ttu-id="b0378-385">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-385">no</span></span>           |
| <span data-ttu-id="b0378-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="b0378-386">msdyn_committype</span></span>             | <span data-ttu-id="b0378-387">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-387">no</span></span>             | <span data-ttu-id="b0378-388">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-388">no</span></span>           |
| <span data-ttu-id="b0378-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="b0378-389">msdyn_committypename</span></span>         | <span data-ttu-id="b0378-390">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-390">no</span></span>             | <span data-ttu-id="b0378-391">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-391">no</span></span>           |
| <span data-ttu-id="b0378-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b0378-392">msdyn_effort</span></span>                 | <span data-ttu-id="b0378-393">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-393">no</span></span>             | <span data-ttu-id="b0378-394">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-394">no</span></span>           |
| <span data-ttu-id="b0378-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b0378-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="b0378-396">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-396">no</span></span>             | <span data-ttu-id="b0378-397">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-397">no</span></span>           |
| <span data-ttu-id="b0378-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b0378-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="b0378-399">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-399">no</span></span>             | <span data-ttu-id="b0378-400">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-400">no</span></span>           |
| <span data-ttu-id="b0378-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b0378-401">msdyn_finish</span></span>                 | <span data-ttu-id="b0378-402">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-402">no</span></span>             | <span data-ttu-id="b0378-403">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-403">no</span></span>           |
| <span data-ttu-id="b0378-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b0378-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="b0378-405">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-405">no</span></span>             | <span data-ttu-id="b0378-406">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-406">no</span></span>           |
| <span data-ttu-id="b0378-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="b0378-408">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-408">no</span></span>             | <span data-ttu-id="b0378-409">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-409">no</span></span>           |
| <span data-ttu-id="b0378-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b0378-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="b0378-411">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-411">no</span></span>             | <span data-ttu-id="b0378-412">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-412">no</span></span>           |
| <span data-ttu-id="b0378-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b0378-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="b0378-414">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-414">no</span></span>             | <span data-ttu-id="b0378-415">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-415">no</span></span>           |
| <span data-ttu-id="b0378-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="b0378-417">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-417">no</span></span>             | <span data-ttu-id="b0378-418">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-418">no</span></span>           |
| <span data-ttu-id="b0378-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b0378-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="b0378-420">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-420">no</span></span>             | <span data-ttu-id="b0378-421">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-421">no</span></span>           |
| <span data-ttu-id="b0378-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b0378-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="b0378-423">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-423">no</span></span>             | <span data-ttu-id="b0378-424">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-424">no</span></span>           |
| <span data-ttu-id="b0378-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="b0378-425">msdyn_projectid</span></span>              | <span data-ttu-id="b0378-426">예</span><span class="sxs-lookup"><span data-stu-id="b0378-426">yes</span></span>            | <span data-ttu-id="b0378-427">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-427">no</span></span>           |
| <span data-ttu-id="b0378-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="b0378-428">msdyn_projectidname</span></span>          | <span data-ttu-id="b0378-429">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-429">no</span></span>             | <span data-ttu-id="b0378-430">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-430">no</span></span>           |
| <span data-ttu-id="b0378-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="b0378-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="b0378-432">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-432">no</span></span>             | <span data-ttu-id="b0378-433">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-433">no</span></span>           |
| <span data-ttu-id="b0378-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="b0378-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="b0378-435">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-435">no</span></span>             | <span data-ttu-id="b0378-436">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-436">no</span></span>           |
| <span data-ttu-id="b0378-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b0378-437">msdyn_start</span></span>                  | <span data-ttu-id="b0378-438">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-438">no</span></span>             | <span data-ttu-id="b0378-439">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-439">no</span></span>           |
| <span data-ttu-id="b0378-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="b0378-440">msdyn_taskid</span></span>                 | <span data-ttu-id="b0378-441">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-441">no</span></span>             | <span data-ttu-id="b0378-442">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-442">no</span></span>           |
| <span data-ttu-id="b0378-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="b0378-443">msdyn_taskidname</span></span>             | <span data-ttu-id="b0378-444">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-444">no</span></span>             | <span data-ttu-id="b0378-445">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-445">no</span></span>           |
| <span data-ttu-id="b0378-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="b0378-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="b0378-447">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-447">no</span></span>             | <span data-ttu-id="b0378-448">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="b0378-449">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="b0378-449">Project team member</span></span>

| <span data-ttu-id="b0378-450">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="b0378-450">**Logical name**</span></span>                                 | <span data-ttu-id="b0378-451">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-451">**Can create**</span></span> | <span data-ttu-id="b0378-452">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="b0378-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="b0378-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="b0378-454">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-454">no</span></span>             | <span data-ttu-id="b0378-455">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-455">no</span></span>           |
| <span data-ttu-id="b0378-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="b0378-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="b0378-457">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-457">no</span></span>             | <span data-ttu-id="b0378-458">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-458">no</span></span>           |
| <span data-ttu-id="b0378-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="b0378-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="b0378-460">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-460">no</span></span>             | <span data-ttu-id="b0378-461">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-461">no</span></span>           |
| <span data-ttu-id="b0378-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="b0378-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="b0378-463">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-463">no</span></span>             | <span data-ttu-id="b0378-464">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-464">no</span></span>           |
| <span data-ttu-id="b0378-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b0378-465">msdyn_effort</span></span>                                     | <span data-ttu-id="b0378-466">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-466">no</span></span>             | <span data-ttu-id="b0378-467">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-467">no</span></span>           |
| <span data-ttu-id="b0378-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b0378-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="b0378-469">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-469">no</span></span>             | <span data-ttu-id="b0378-470">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-470">no</span></span>           |
| <span data-ttu-id="b0378-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b0378-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="b0378-472">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-472">no</span></span>             | <span data-ttu-id="b0378-473">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-473">no</span></span>           |
| <span data-ttu-id="b0378-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b0378-474">msdyn_finish</span></span>                                     | <span data-ttu-id="b0378-475">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-475">no</span></span>             | <span data-ttu-id="b0378-476">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-476">no</span></span>           |
| <span data-ttu-id="b0378-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="b0378-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="b0378-478">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-478">no</span></span>             | <span data-ttu-id="b0378-479">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-479">no</span></span>           |
| <span data-ttu-id="b0378-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="b0378-480">msdyn_hours</span></span>                                      | <span data-ttu-id="b0378-481">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-481">no</span></span>             | <span data-ttu-id="b0378-482">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-482">no</span></span>           |
| <span data-ttu-id="b0378-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="b0378-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="b0378-484">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-484">no</span></span>             | <span data-ttu-id="b0378-485">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-485">no</span></span>           |
| <span data-ttu-id="b0378-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="b0378-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="b0378-487">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-487">no</span></span>             | <span data-ttu-id="b0378-488">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-488">no</span></span>           |
| <span data-ttu-id="b0378-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b0378-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="b0378-490">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-490">no</span></span>             | <span data-ttu-id="b0378-491">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-491">no</span></span>           |
| <span data-ttu-id="b0378-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="b0378-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="b0378-493">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-493">no</span></span>             | <span data-ttu-id="b0378-494">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-494">no</span></span>           |
| <span data-ttu-id="b0378-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="b0378-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="b0378-496">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-496">no</span></span>             | <span data-ttu-id="b0378-497">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-497">no</span></span>           |
| <span data-ttu-id="b0378-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="b0378-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="b0378-499">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-499">no</span></span>             | <span data-ttu-id="b0378-500">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-500">no</span></span>           |
| <span data-ttu-id="b0378-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b0378-501">msdyn_start</span></span>                                      | <span data-ttu-id="b0378-502">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-502">no</span></span>             | <span data-ttu-id="b0378-503">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="b0378-504">Project</span><span class="sxs-lookup"><span data-stu-id="b0378-504">Project</span></span>

| <span data-ttu-id="b0378-505">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="b0378-505">**Logical name**</span></span>                       | <span data-ttu-id="b0378-506">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-506">**Can create**</span></span> | <span data-ttu-id="b0378-507">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="b0378-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="b0378-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="b0378-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="b0378-509">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-509">no</span></span>             | <span data-ttu-id="b0378-510">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-510">no</span></span>           |
| <span data-ttu-id="b0378-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="b0378-512">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-512">no</span></span>             | <span data-ttu-id="b0378-513">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-513">no</span></span>           |
| <span data-ttu-id="b0378-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="b0378-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="b0378-515">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-515">no</span></span>             | <span data-ttu-id="b0378-516">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-516">no</span></span>           |
| <span data-ttu-id="b0378-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="b0378-518">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-518">no</span></span>             | <span data-ttu-id="b0378-519">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-519">no</span></span>           |
| <span data-ttu-id="b0378-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b0378-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="b0378-521">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-521">no</span></span>             | <span data-ttu-id="b0378-522">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-522">no</span></span>           |
| <span data-ttu-id="b0378-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b0378-524">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-524">no</span></span>             | <span data-ttu-id="b0378-525">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-525">no</span></span>           |
| <span data-ttu-id="b0378-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="b0378-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="b0378-527">예</span><span class="sxs-lookup"><span data-stu-id="b0378-527">yes</span></span>            | <span data-ttu-id="b0378-528">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-528">no</span></span>           |
| <span data-ttu-id="b0378-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b0378-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="b0378-530">예</span><span class="sxs-lookup"><span data-stu-id="b0378-530">yes</span></span>            | <span data-ttu-id="b0378-531">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-531">no</span></span>           |
| <span data-ttu-id="b0378-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b0378-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="b0378-533">예</span><span class="sxs-lookup"><span data-stu-id="b0378-533">yes</span></span>            | <span data-ttu-id="b0378-534">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-534">no</span></span>           |
| <span data-ttu-id="b0378-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="b0378-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="b0378-536">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-536">no</span></span>             | <span data-ttu-id="b0378-537">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-537">no</span></span>           |
| <span data-ttu-id="b0378-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b0378-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="b0378-539">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-539">no</span></span>             | <span data-ttu-id="b0378-540">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-540">no</span></span>           |
| <span data-ttu-id="b0378-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b0378-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="b0378-542">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-542">no</span></span>             | <span data-ttu-id="b0378-543">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-543">no</span></span>           |
| <span data-ttu-id="b0378-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="b0378-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="b0378-545">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-545">no</span></span>             | <span data-ttu-id="b0378-546">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-546">no</span></span>           |
| <span data-ttu-id="b0378-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="b0378-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="b0378-548">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-548">no</span></span>             | <span data-ttu-id="b0378-549">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-549">no</span></span>           |
| <span data-ttu-id="b0378-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="b0378-550">msdyn_duration</span></span>                         | <span data-ttu-id="b0378-551">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-551">no</span></span>             | <span data-ttu-id="b0378-552">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-552">no</span></span>           |
| <span data-ttu-id="b0378-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b0378-553">msdyn_effort</span></span>                           | <span data-ttu-id="b0378-554">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-554">no</span></span>             | <span data-ttu-id="b0378-555">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-555">no</span></span>           |
| <span data-ttu-id="b0378-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b0378-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b0378-557">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-557">no</span></span>             | <span data-ttu-id="b0378-558">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-558">no</span></span>           |
| <span data-ttu-id="b0378-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b0378-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="b0378-560">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-560">no</span></span>             | <span data-ttu-id="b0378-561">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-561">no</span></span>           |
| <span data-ttu-id="b0378-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b0378-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="b0378-563">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-563">no</span></span>             | <span data-ttu-id="b0378-564">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-564">no</span></span>           |
| <span data-ttu-id="b0378-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b0378-565">msdyn_finish</span></span>                           | <span data-ttu-id="b0378-566">예</span><span class="sxs-lookup"><span data-stu-id="b0378-566">yes</span></span>            | <span data-ttu-id="b0378-567">예</span><span class="sxs-lookup"><span data-stu-id="b0378-567">yes</span></span>          |
| <span data-ttu-id="b0378-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="b0378-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="b0378-569">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-569">no</span></span>             | <span data-ttu-id="b0378-570">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-570">no</span></span>           |
| <span data-ttu-id="b0378-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="b0378-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="b0378-572">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-572">no</span></span>             | <span data-ttu-id="b0378-573">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-573">no</span></span>           |
| <span data-ttu-id="b0378-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="b0378-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="b0378-575">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-575">no</span></span>             | <span data-ttu-id="b0378-576">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-576">no</span></span>           |
| <span data-ttu-id="b0378-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="b0378-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="b0378-578">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-578">no</span></span>             | <span data-ttu-id="b0378-579">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-579">no</span></span>           |
| <span data-ttu-id="b0378-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="b0378-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="b0378-581">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-581">no</span></span>             | <span data-ttu-id="b0378-582">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-582">no</span></span>           |
| <span data-ttu-id="b0378-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="b0378-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="b0378-584">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-584">no</span></span>             | <span data-ttu-id="b0378-585">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-585">no</span></span>           |
| <span data-ttu-id="b0378-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="b0378-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="b0378-587">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-587">no</span></span>             | <span data-ttu-id="b0378-588">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-588">no</span></span>           |
| <span data-ttu-id="b0378-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="b0378-590">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-590">no</span></span>             | <span data-ttu-id="b0378-591">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-591">no</span></span>           |
| <span data-ttu-id="b0378-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="b0378-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="b0378-593">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-593">no</span></span>             | <span data-ttu-id="b0378-594">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-594">no</span></span>           |
| <span data-ttu-id="b0378-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="b0378-596">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-596">no</span></span>             | <span data-ttu-id="b0378-597">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-597">no</span></span>           |
| <span data-ttu-id="b0378-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b0378-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b0378-599">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-599">no</span></span>             | <span data-ttu-id="b0378-600">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-600">no</span></span>           |
| <span data-ttu-id="b0378-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b0378-602">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-602">no</span></span>             | <span data-ttu-id="b0378-603">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-603">no</span></span>           |
| <span data-ttu-id="b0378-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b0378-604">msdyn_progress</span></span>                         | <span data-ttu-id="b0378-605">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-605">no</span></span>             | <span data-ttu-id="b0378-606">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-606">no</span></span>           |
| <span data-ttu-id="b0378-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b0378-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b0378-608">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-608">no</span></span>             | <span data-ttu-id="b0378-609">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-609">no</span></span>           |
| <span data-ttu-id="b0378-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b0378-611">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-611">no</span></span>             | <span data-ttu-id="b0378-612">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-612">no</span></span>           |
| <span data-ttu-id="b0378-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b0378-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b0378-614">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-614">no</span></span>             | <span data-ttu-id="b0378-615">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-615">no</span></span>           |
| <span data-ttu-id="b0378-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b0378-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b0378-617">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-617">no</span></span>             | <span data-ttu-id="b0378-618">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-618">no</span></span>           |
| <span data-ttu-id="b0378-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="b0378-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="b0378-620">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-620">no</span></span>             | <span data-ttu-id="b0378-621">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-621">no</span></span>           |
| <span data-ttu-id="b0378-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="b0378-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="b0378-623">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-623">no</span></span>             | <span data-ttu-id="b0378-624">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-624">no</span></span>           |
| <span data-ttu-id="b0378-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b0378-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="b0378-626">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-626">no</span></span>             | <span data-ttu-id="b0378-627">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-627">no</span></span>           |
| <span data-ttu-id="b0378-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="b0378-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="b0378-629">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-629">no</span></span>             | <span data-ttu-id="b0378-630">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-630">no</span></span>           |
| <span data-ttu-id="b0378-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b0378-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b0378-632">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-632">no</span></span>             | <span data-ttu-id="b0378-633">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-633">no</span></span>           |
| <span data-ttu-id="b0378-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b0378-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b0378-635">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-635">no</span></span>             | <span data-ttu-id="b0378-636">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-636">no</span></span>           |
| <span data-ttu-id="b0378-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="b0378-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="b0378-638">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-638">no</span></span>             | <span data-ttu-id="b0378-639">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-639">no</span></span>           |
| <span data-ttu-id="b0378-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="b0378-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="b0378-641">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-641">no</span></span>             | <span data-ttu-id="b0378-642">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-642">no</span></span>           |
| <span data-ttu-id="b0378-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b0378-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b0378-644">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-644">no</span></span>             | <span data-ttu-id="b0378-645">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-645">no</span></span>           |
| <span data-ttu-id="b0378-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="b0378-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="b0378-647">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-647">no</span></span>             | <span data-ttu-id="b0378-648">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-648">no</span></span>           |
| <span data-ttu-id="b0378-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="b0378-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="b0378-650">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-650">no</span></span>             | <span data-ttu-id="b0378-651">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-651">no</span></span>           |
| <span data-ttu-id="b0378-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="b0378-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="b0378-653">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-653">no</span></span>             | <span data-ttu-id="b0378-654">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-654">no</span></span>           |
| <span data-ttu-id="b0378-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="b0378-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="b0378-656">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-656">no</span></span>             | <span data-ttu-id="b0378-657">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-657">no</span></span>           |
| <span data-ttu-id="b0378-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="b0378-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="b0378-659">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-659">no</span></span>             | <span data-ttu-id="b0378-660">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-660">no</span></span>           |
| <span data-ttu-id="b0378-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="b0378-662">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-662">no</span></span>             | <span data-ttu-id="b0378-663">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-663">no</span></span>           |
| <span data-ttu-id="b0378-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="b0378-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="b0378-665">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-665">no</span></span>             | <span data-ttu-id="b0378-666">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-666">no</span></span>           |
| <span data-ttu-id="b0378-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b0378-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="b0378-668">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-668">no</span></span>             | <span data-ttu-id="b0378-669">아니요</span><span class="sxs-lookup"><span data-stu-id="b0378-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="b0378-670">제한 사항 및 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="b0378-670">Limitations and known issues</span></span>
<span data-ttu-id="b0378-671">다음은 제한 사항 및 알려진 문제 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="b0378-672">프로젝트 일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="b0378-673">다음 사용자는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-673">They can't be used by:</span></span>
    - <span data-ttu-id="b0378-674">응용 프로그램 사용자</span><span class="sxs-lookup"><span data-stu-id="b0378-674">Application users</span></span>
    - <span data-ttu-id="b0378-675">시스템 사용자</span><span class="sxs-lookup"><span data-stu-id="b0378-675">System users</span></span>
    - <span data-ttu-id="b0378-676">통합 사용자</span><span class="sxs-lookup"><span data-stu-id="b0378-676">Integration users</span></span>
    - <span data-ttu-id="b0378-677">필요한 라이선스가 없는 다른 사용자</span><span class="sxs-lookup"><span data-stu-id="b0378-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="b0378-678">각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="b0378-679">각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="b0378-680">Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="b0378-681">**OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="b0378-682">프로젝트 및 작업에 대한 제한 및 경계</span><span class="sxs-lookup"><span data-stu-id="b0378-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="b0378-683">오류 처리</span><span class="sxs-lookup"><span data-stu-id="b0378-683">Error handling</span></span>

   - <span data-ttu-id="b0378-684">작업 세트에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **작업 세트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="b0378-685">프로젝트 일정 서비스에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **PSS 오류 로그** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="b0378-686">샘플 시나리오</span><span class="sxs-lookup"><span data-stu-id="b0378-686">Sample scenario</span></span>

<span data-ttu-id="b0378-687">이 시나리오에서는 프로젝트, 팀 구성원, 4개의 작업 및 2개의 리소스 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="b0378-688">다음으로 하나의 작업을 업데이트하고, 프로젝트를 업데이트하고, 하나의 작업을 삭제하고, 하나의 리소스 할당을 삭제하고, 작업 종속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0378-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="b0378-689">추가 샘플</span><span class="sxs-lookup"><span data-stu-id="b0378-689">Additional samples</span></span>

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
