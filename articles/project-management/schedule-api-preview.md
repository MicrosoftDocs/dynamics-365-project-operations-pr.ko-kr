---
title: 일정 엔터티로 일정 API를 사용하여 작업 수행
description: 이 항목은 일정 API 사용에 대한 정보와 샘플을 제공합니다.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116805"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="c38b4-103">일정 엔터티로 일정 API를 사용하여 작업 수행</span><span class="sxs-lookup"><span data-stu-id="c38b4-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="c38b4-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="c38b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c38b4-105">이 항목에 언급된 일부 또는 모든 기능은 미리 보기 릴리스의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="c38b4-106">내용과 기능은 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="c38b4-107">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="c38b4-107">Scheduling entities</span></span>

<span data-ttu-id="c38b4-108">일정 API는 **예약 엔터티** 를 통해 생성, 업데이트 및 삭제 작업을 수행할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="c38b4-109">이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="c38b4-110">**예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="c38b4-111">다음 표는 **예약 엔터티** 전체 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="c38b4-112">엔터티 이름</span><span class="sxs-lookup"><span data-stu-id="c38b4-112">Entity name</span></span>  | <span data-ttu-id="c38b4-113">엔터티 논리적 이름</span><span class="sxs-lookup"><span data-stu-id="c38b4-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="c38b4-114">Project</span><span class="sxs-lookup"><span data-stu-id="c38b4-114">Project</span></span> | <span data-ttu-id="c38b4-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c38b4-115">msdyn_project</span></span> |
| <span data-ttu-id="c38b4-116">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="c38b4-116">Project Task</span></span>  | <span data-ttu-id="c38b4-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="c38b4-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="c38b4-118">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="c38b4-118">Project Task Dependency</span></span>  | <span data-ttu-id="c38b4-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="c38b4-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="c38b4-120">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="c38b4-120">Resource Assignment</span></span> | <span data-ttu-id="c38b4-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="c38b4-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="c38b4-122">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="c38b4-122">Project Bucket</span></span>  | <span data-ttu-id="c38b4-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="c38b4-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="c38b4-124">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="c38b4-124">Project Team Member</span></span> | <span data-ttu-id="c38b4-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="c38b4-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="c38b4-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="c38b4-126">OperationSet</span></span>

<span data-ttu-id="c38b4-127">OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="c38b4-128">일정 API</span><span class="sxs-lookup"><span data-stu-id="c38b4-128">Schedule APIs</span></span>

<span data-ttu-id="c38b4-129">다음은 현재 일정 API 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="c38b4-130">**msdyn_CreateProjectV1**: 이 API를 사용하여 프로젝트를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="c38b4-131">프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="c38b4-132">**msdyn_CreateTeamMemberV1**: 이 API를 사용하여 프로젝트 팀 구성원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="c38b4-133">팀 구성원 레코드가 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="c38b4-134">**msdyn_CreateOperationSetV1**: 이 API는 트랜잭션 내에서 수행해야 하는 여러 요청을 예약하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="c38b4-135">**msdyn_PSSCreateV1**: 이 API는 엔터티를 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="c38b4-136">엔터티는 만들기 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="c38b4-137">**msdyn_PSSUpdateV1**: 이 API는 엔터티를 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="c38b4-138">엔터티는 업데이트 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="c38b4-139">**msdyn_PSSDeleteV1**: 이 API는 엔터티를 삭제하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="c38b4-140">엔터티는 삭제 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="c38b4-141">**msdyn_ExecuteOperationSetV1**: 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="c38b4-142">OperationSet과 함께 일정 API 사용</span><span class="sxs-lookup"><span data-stu-id="c38b4-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="c38b4-143">**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="c38b4-144">그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="c38b4-145">지원되는 작업</span><span class="sxs-lookup"><span data-stu-id="c38b4-145">Supported operations</span></span>

| <span data-ttu-id="c38b4-146">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="c38b4-146">Scheduling entity</span></span> | <span data-ttu-id="c38b4-147">만들기</span><span class="sxs-lookup"><span data-stu-id="c38b4-147">Create</span></span> | <span data-ttu-id="c38b4-148">엽데이트</span><span class="sxs-lookup"><span data-stu-id="c38b4-148">Update</span></span> | <span data-ttu-id="c38b4-149">Delete</span><span class="sxs-lookup"><span data-stu-id="c38b4-149">Delete</span></span> | <span data-ttu-id="c38b4-150">중요 사항</span><span class="sxs-lookup"><span data-stu-id="c38b4-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="c38b4-151">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="c38b4-151">Project task</span></span> | <span data-ttu-id="c38b4-152">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-152">Yes</span></span> | <span data-ttu-id="c38b4-153">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-153">Yes</span></span> | <span data-ttu-id="c38b4-154">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-154">Yes</span></span> | <span data-ttu-id="c38b4-155">없음</span><span class="sxs-lookup"><span data-stu-id="c38b4-155">None</span></span> |
| <span data-ttu-id="c38b4-156">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="c38b4-156">Project task dependency</span></span> | <span data-ttu-id="c38b4-157">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-157">Yes</span></span> | <span data-ttu-id="c38b4-158">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-158">Yes</span></span> | | <span data-ttu-id="c38b4-159">프로젝트 작업 종속성 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="c38b4-160">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c38b4-161">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="c38b4-161">Resource assignment</span></span> | <span data-ttu-id="c38b4-162">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-162">Yes</span></span> | <span data-ttu-id="c38b4-163">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-163">Yes</span></span> | | <span data-ttu-id="c38b4-164">**BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="c38b4-165">리소스 할당 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="c38b4-166">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c38b4-167">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="c38b4-167">Project bucket</span></span> | <span data-ttu-id="c38b4-168">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c38b4-168">N/A</span></span> | <span data-ttu-id="c38b4-169">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c38b4-169">N/A</span></span> | <span data-ttu-id="c38b4-170">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c38b4-170">N/A</span></span> | <span data-ttu-id="c38b4-171">기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="c38b4-172">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="c38b4-172">Project team member</span></span> | <span data-ttu-id="c38b4-173">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-173">Yes</span></span> | <span data-ttu-id="c38b4-174">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-174">Yes</span></span> | <span data-ttu-id="c38b4-175">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-175">Yes</span></span> | <span data-ttu-id="c38b4-176">생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="c38b4-177">Project</span><span class="sxs-lookup"><span data-stu-id="c38b4-177">Project</span></span> | <span data-ttu-id="c38b4-178">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-178">Yes</span></span> | <span data-ttu-id="c38b4-179">네</span><span class="sxs-lookup"><span data-stu-id="c38b4-179">Yes</span></span> | <span data-ttu-id="c38b4-180">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c38b4-180">N/A</span></span> | <span data-ttu-id="c38b4-181">**StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="c38b4-182">이러한 API는 사용자 지정 필드를 포함하는 엔터티 개체를 사용하여 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="c38b4-183">ID 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-183">The ID property is optional.</span></span> <span data-ttu-id="c38b4-184">제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="c38b4-185">제공되지 않으면 시스템에서 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="c38b4-186">제한된 필드</span><span class="sxs-lookup"><span data-stu-id="c38b4-186">Restricted fields</span></span>

<span data-ttu-id="c38b4-187">다음 표는 **생성** 및 **편집** 에서 제한되는 필드를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="c38b4-188">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="c38b4-188">Project task</span></span>

| <span data-ttu-id="c38b4-189">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="c38b4-189">**Logical name**</span></span>                       | <span data-ttu-id="c38b4-190">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-190">**Can create**</span></span> | <span data-ttu-id="c38b4-191">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="c38b4-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="c38b4-193">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-193">no</span></span>             | <span data-ttu-id="c38b4-194">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-194">no</span></span>               |
| <span data-ttu-id="c38b4-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="c38b4-196">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-196">no</span></span>             | <span data-ttu-id="c38b4-197">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-197">no</span></span>               |
| <span data-ttu-id="c38b4-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="c38b4-198">msdyn_actualend</span></span>                        | <span data-ttu-id="c38b4-199">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-199">no</span></span>             | <span data-ttu-id="c38b4-200">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-200">no</span></span>               |
| <span data-ttu-id="c38b4-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="c38b4-202">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-202">no</span></span>             | <span data-ttu-id="c38b4-203">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-203">no</span></span>               |
| <span data-ttu-id="c38b4-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="c38b4-205">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-205">no</span></span>             | <span data-ttu-id="c38b4-206">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-206">no</span></span>               |
| <span data-ttu-id="c38b4-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="c38b4-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="c38b4-208">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-208">no</span></span>             | <span data-ttu-id="c38b4-209">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-209">no</span></span>               |
| <span data-ttu-id="c38b4-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="c38b4-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="c38b4-211">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-211">no</span></span>             | <span data-ttu-id="c38b4-212">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-212">no</span></span>               |
| <span data-ttu-id="c38b4-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="c38b4-214">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-214">no</span></span>             | <span data-ttu-id="c38b4-215">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-215">no</span></span>               |
| <span data-ttu-id="c38b4-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="c38b4-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="c38b4-217">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-217">no</span></span>             | <span data-ttu-id="c38b4-218">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-218">no</span></span>               |
| <span data-ttu-id="c38b4-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c38b4-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="c38b4-220">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-220">no</span></span>             | <span data-ttu-id="c38b4-221">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-221">no</span></span>               |
| <span data-ttu-id="c38b4-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c38b4-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="c38b4-223">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-223">no</span></span>             | <span data-ttu-id="c38b4-224">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-224">no</span></span>               |
| <span data-ttu-id="c38b4-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="c38b4-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="c38b4-226">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-226">no</span></span>             | <span data-ttu-id="c38b4-227">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-227">no</span></span>               |
| <span data-ttu-id="c38b4-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="c38b4-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="c38b4-229">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-229">no</span></span>             | <span data-ttu-id="c38b4-230">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-230">no</span></span>               |
| <span data-ttu-id="c38b4-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="c38b4-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="c38b4-232">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-232">no</span></span>             | <span data-ttu-id="c38b4-233">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-233">no</span></span>               |
| <span data-ttu-id="c38b4-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="c38b4-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="c38b4-235">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-235">no</span></span>             | <span data-ttu-id="c38b4-236">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-236">no</span></span>               |
| <span data-ttu-id="c38b4-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="c38b4-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="c38b4-238">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-238">no</span></span>             | <span data-ttu-id="c38b4-239">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-239">no</span></span>               |
| <span data-ttu-id="c38b4-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="c38b4-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="c38b4-241">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-241">no</span></span>             | <span data-ttu-id="c38b4-242">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-242">no</span></span>               |
| <span data-ttu-id="c38b4-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="c38b4-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="c38b4-244">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-244">no</span></span>             | <span data-ttu-id="c38b4-245">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-245">no</span></span>               |
| <span data-ttu-id="c38b4-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="c38b4-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="c38b4-247">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-247">no</span></span>             | <span data-ttu-id="c38b4-248">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-248">no</span></span>               |
| <span data-ttu-id="c38b4-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="c38b4-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="c38b4-250">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-250">no</span></span>             | <span data-ttu-id="c38b4-251">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-251">no</span></span>               |
| <span data-ttu-id="c38b4-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="c38b4-253">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-253">no</span></span>             | <span data-ttu-id="c38b4-254">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-254">no</span></span>               |
| <span data-ttu-id="c38b4-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="c38b4-256">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-256">no</span></span>             | <span data-ttu-id="c38b4-257">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-257">no</span></span>               |
| <span data-ttu-id="c38b4-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="c38b4-259">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-259">no</span></span>             | <span data-ttu-id="c38b4-260">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-260">no</span></span>               |
| <span data-ttu-id="c38b4-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="c38b4-262">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-262">no</span></span>             | <span data-ttu-id="c38b4-263">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-263">no</span></span>               |
| <span data-ttu-id="c38b4-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="c38b4-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="c38b4-265">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-265">no</span></span>             | <span data-ttu-id="c38b4-266">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-266">no</span></span>               |
| <span data-ttu-id="c38b4-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="c38b4-267">msdyn_progress</span></span>                         | <span data-ttu-id="c38b4-268">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-268">no</span></span>             | <span data-ttu-id="c38b4-269">아니요(P4W의 경우 예)</span><span class="sxs-lookup"><span data-stu-id="c38b4-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="c38b4-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="c38b4-271">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-271">no</span></span>             | <span data-ttu-id="c38b4-272">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-272">no</span></span>               |
| <span data-ttu-id="c38b4-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="c38b4-274">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-274">no</span></span>             | <span data-ttu-id="c38b4-275">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-275">no</span></span>               |
| <span data-ttu-id="c38b4-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="c38b4-277">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-277">no</span></span>             | <span data-ttu-id="c38b4-278">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-278">no</span></span>               |
| <span data-ttu-id="c38b4-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="c38b4-280">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-280">no</span></span>             | <span data-ttu-id="c38b4-281">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-281">no</span></span>               |
| <span data-ttu-id="c38b4-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="c38b4-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="c38b4-283">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-283">no</span></span>             | <span data-ttu-id="c38b4-284">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-284">no</span></span>               |
| <span data-ttu-id="c38b4-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="c38b4-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="c38b4-286">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-286">no</span></span>             | <span data-ttu-id="c38b4-287">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-287">no</span></span>               |
| <span data-ttu-id="c38b4-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="c38b4-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="c38b4-289">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-289">no</span></span>             | <span data-ttu-id="c38b4-290">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-290">no</span></span>               |
| <span data-ttu-id="c38b4-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="c38b4-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="c38b4-292">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-292">no</span></span>             | <span data-ttu-id="c38b4-293">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-293">no</span></span>               |
| <span data-ttu-id="c38b4-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="c38b4-295">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-295">no</span></span>             | <span data-ttu-id="c38b4-296">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-296">no</span></span>               |
| <span data-ttu-id="c38b4-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="c38b4-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="c38b4-298">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-298">no</span></span>             | <span data-ttu-id="c38b4-299">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-299">no</span></span>               |
| <span data-ttu-id="c38b4-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c38b4-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="c38b4-301">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-301">no</span></span>             | <span data-ttu-id="c38b4-302">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-302">no</span></span>               |
| <span data-ttu-id="c38b4-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="c38b4-304">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-304">no</span></span>             | <span data-ttu-id="c38b4-305">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-305">no</span></span>               |
| <span data-ttu-id="c38b4-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="c38b4-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="c38b4-307">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-307">no</span></span>             | <span data-ttu-id="c38b4-308">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-308">no</span></span>               |
| <span data-ttu-id="c38b4-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="c38b4-310">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-310">no</span></span>             | <span data-ttu-id="c38b4-311">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-311">no</span></span>               |
| <span data-ttu-id="c38b4-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="c38b4-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="c38b4-313">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-313">no</span></span>             | <span data-ttu-id="c38b4-314">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-314">no</span></span>               |
| <span data-ttu-id="c38b4-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="c38b4-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="c38b4-316">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-316">no</span></span>             | <span data-ttu-id="c38b4-317">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-317">no</span></span>               |
| <span data-ttu-id="c38b4-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="c38b4-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="c38b4-319">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-319">no</span></span>             | <span data-ttu-id="c38b4-320">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-320">no</span></span>               |
| <span data-ttu-id="c38b4-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="c38b4-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="c38b4-322">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-322">no</span></span>             | <span data-ttu-id="c38b4-323">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-323">no</span></span>               |
| <span data-ttu-id="c38b4-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="c38b4-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="c38b4-325">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-325">no</span></span>             | <span data-ttu-id="c38b4-326">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-326">no</span></span>               |
| <span data-ttu-id="c38b4-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="c38b4-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="c38b4-328">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-328">no</span></span>             | <span data-ttu-id="c38b4-329">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-329">no</span></span>               |
| <span data-ttu-id="c38b4-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="c38b4-330">msdyn_summary</span></span>                          | <span data-ttu-id="c38b4-331">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-331">no</span></span>             | <span data-ttu-id="c38b4-332">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-332">no</span></span>               |
| <span data-ttu-id="c38b4-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="c38b4-334">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-334">no</span></span>             | <span data-ttu-id="c38b4-335">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-335">no</span></span>               |
| <span data-ttu-id="c38b4-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="c38b4-337">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-337">no</span></span>             | <span data-ttu-id="c38b4-338">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="c38b4-339">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="c38b4-339">Project task dependency</span></span>

| <span data-ttu-id="c38b4-340">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="c38b4-340">**Logical name**</span></span>              | <span data-ttu-id="c38b4-341">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-341">**Can create**</span></span> | <span data-ttu-id="c38b4-342">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="c38b4-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="c38b4-343">msdyn_linktype</span></span>                | <span data-ttu-id="c38b4-344">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-344">no</span></span>             | <span data-ttu-id="c38b4-345">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-345">no</span></span>           |
| <span data-ttu-id="c38b4-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="c38b4-346">msdyn_linktypename</span></span>            | <span data-ttu-id="c38b4-347">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-347">no</span></span>             | <span data-ttu-id="c38b4-348">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-348">no</span></span>           |
| <span data-ttu-id="c38b4-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="c38b4-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="c38b4-350">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-350">yes</span></span>            | <span data-ttu-id="c38b4-351">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-351">no</span></span>           |
| <span data-ttu-id="c38b4-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="c38b4-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="c38b4-353">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-353">yes</span></span>            | <span data-ttu-id="c38b4-354">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-354">no</span></span>           |
| <span data-ttu-id="c38b4-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c38b4-355">msdyn_project</span></span>                 | <span data-ttu-id="c38b4-356">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-356">yes</span></span>            | <span data-ttu-id="c38b4-357">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-357">no</span></span>           |
| <span data-ttu-id="c38b4-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="c38b4-358">msdyn_projectname</span></span>             | <span data-ttu-id="c38b4-359">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-359">yes</span></span>            | <span data-ttu-id="c38b4-360">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-360">no</span></span>           |
| <span data-ttu-id="c38b4-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="c38b4-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="c38b4-362">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-362">yes</span></span>            | <span data-ttu-id="c38b4-363">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-363">no</span></span>           |
| <span data-ttu-id="c38b4-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="c38b4-364">msdyn_successortask</span></span>           | <span data-ttu-id="c38b4-365">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-365">yes</span></span>            | <span data-ttu-id="c38b4-366">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-366">no</span></span>           |
| <span data-ttu-id="c38b4-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="c38b4-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="c38b4-368">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-368">yes</span></span>            | <span data-ttu-id="c38b4-369">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="c38b4-370">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="c38b4-370">Resource assignment</span></span>

| <span data-ttu-id="c38b4-371">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="c38b4-371">**Logical name**</span></span>             | <span data-ttu-id="c38b4-372">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-372">**Can create**</span></span> | <span data-ttu-id="c38b4-373">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="c38b4-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="c38b4-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="c38b4-375">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-375">yes</span></span>            | <span data-ttu-id="c38b4-376">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-376">no</span></span>           |
| <span data-ttu-id="c38b4-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="c38b4-378">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-378">yes</span></span>            | <span data-ttu-id="c38b4-379">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-379">no</span></span>           |
| <span data-ttu-id="c38b4-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="c38b4-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="c38b4-381">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-381">no</span></span>             | <span data-ttu-id="c38b4-382">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-382">no</span></span>           |
| <span data-ttu-id="c38b4-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="c38b4-384">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-384">no</span></span>             | <span data-ttu-id="c38b4-385">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-385">no</span></span>           |
| <span data-ttu-id="c38b4-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="c38b4-386">msdyn_committype</span></span>             | <span data-ttu-id="c38b4-387">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-387">no</span></span>             | <span data-ttu-id="c38b4-388">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-388">no</span></span>           |
| <span data-ttu-id="c38b4-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="c38b4-389">msdyn_committypename</span></span>         | <span data-ttu-id="c38b4-390">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-390">no</span></span>             | <span data-ttu-id="c38b4-391">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-391">no</span></span>           |
| <span data-ttu-id="c38b4-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c38b4-392">msdyn_effort</span></span>                 | <span data-ttu-id="c38b4-393">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-393">no</span></span>             | <span data-ttu-id="c38b4-394">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-394">no</span></span>           |
| <span data-ttu-id="c38b4-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c38b4-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="c38b4-396">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-396">no</span></span>             | <span data-ttu-id="c38b4-397">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-397">no</span></span>           |
| <span data-ttu-id="c38b4-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c38b4-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="c38b4-399">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-399">no</span></span>             | <span data-ttu-id="c38b4-400">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-400">no</span></span>           |
| <span data-ttu-id="c38b4-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c38b4-401">msdyn_finish</span></span>                 | <span data-ttu-id="c38b4-402">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-402">no</span></span>             | <span data-ttu-id="c38b4-403">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-403">no</span></span>           |
| <span data-ttu-id="c38b4-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="c38b4-405">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-405">no</span></span>             | <span data-ttu-id="c38b4-406">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-406">no</span></span>           |
| <span data-ttu-id="c38b4-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="c38b4-408">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-408">no</span></span>             | <span data-ttu-id="c38b4-409">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-409">no</span></span>           |
| <span data-ttu-id="c38b4-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="c38b4-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="c38b4-411">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-411">no</span></span>             | <span data-ttu-id="c38b4-412">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-412">no</span></span>           |
| <span data-ttu-id="c38b4-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="c38b4-414">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-414">no</span></span>             | <span data-ttu-id="c38b4-415">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-415">no</span></span>           |
| <span data-ttu-id="c38b4-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="c38b4-417">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-417">no</span></span>             | <span data-ttu-id="c38b4-418">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-418">no</span></span>           |
| <span data-ttu-id="c38b4-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="c38b4-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="c38b4-420">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-420">no</span></span>             | <span data-ttu-id="c38b4-421">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-421">no</span></span>           |
| <span data-ttu-id="c38b4-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="c38b4-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="c38b4-423">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-423">no</span></span>             | <span data-ttu-id="c38b4-424">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-424">no</span></span>           |
| <span data-ttu-id="c38b4-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="c38b4-425">msdyn_projectid</span></span>              | <span data-ttu-id="c38b4-426">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-426">yes</span></span>            | <span data-ttu-id="c38b4-427">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-427">no</span></span>           |
| <span data-ttu-id="c38b4-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-428">msdyn_projectidname</span></span>          | <span data-ttu-id="c38b4-429">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-429">no</span></span>             | <span data-ttu-id="c38b4-430">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-430">no</span></span>           |
| <span data-ttu-id="c38b4-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="c38b4-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="c38b4-432">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-432">no</span></span>             | <span data-ttu-id="c38b4-433">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-433">no</span></span>           |
| <span data-ttu-id="c38b4-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="c38b4-435">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-435">no</span></span>             | <span data-ttu-id="c38b4-436">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-436">no</span></span>           |
| <span data-ttu-id="c38b4-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="c38b4-437">msdyn_start</span></span>                  | <span data-ttu-id="c38b4-438">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-438">no</span></span>             | <span data-ttu-id="c38b4-439">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-439">no</span></span>           |
| <span data-ttu-id="c38b4-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="c38b4-440">msdyn_taskid</span></span>                 | <span data-ttu-id="c38b4-441">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-441">no</span></span>             | <span data-ttu-id="c38b4-442">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-442">no</span></span>           |
| <span data-ttu-id="c38b4-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-443">msdyn_taskidname</span></span>             | <span data-ttu-id="c38b4-444">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-444">no</span></span>             | <span data-ttu-id="c38b4-445">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-445">no</span></span>           |
| <span data-ttu-id="c38b4-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="c38b4-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="c38b4-447">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-447">no</span></span>             | <span data-ttu-id="c38b4-448">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="c38b4-449">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="c38b4-449">Project team member</span></span>

| <span data-ttu-id="c38b4-450">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="c38b4-450">**Logical name**</span></span>                                 | <span data-ttu-id="c38b4-451">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-451">**Can create**</span></span> | <span data-ttu-id="c38b4-452">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="c38b4-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="c38b4-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="c38b4-454">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-454">no</span></span>             | <span data-ttu-id="c38b4-455">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-455">no</span></span>           |
| <span data-ttu-id="c38b4-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="c38b4-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="c38b4-457">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-457">no</span></span>             | <span data-ttu-id="c38b4-458">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-458">no</span></span>           |
| <span data-ttu-id="c38b4-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="c38b4-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="c38b4-460">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-460">no</span></span>             | <span data-ttu-id="c38b4-461">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-461">no</span></span>           |
| <span data-ttu-id="c38b4-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="c38b4-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="c38b4-463">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-463">no</span></span>             | <span data-ttu-id="c38b4-464">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-464">no</span></span>           |
| <span data-ttu-id="c38b4-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c38b4-465">msdyn_effort</span></span>                                     | <span data-ttu-id="c38b4-466">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-466">no</span></span>             | <span data-ttu-id="c38b4-467">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-467">no</span></span>           |
| <span data-ttu-id="c38b4-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c38b4-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="c38b4-469">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-469">no</span></span>             | <span data-ttu-id="c38b4-470">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-470">no</span></span>           |
| <span data-ttu-id="c38b4-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c38b4-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="c38b4-472">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-472">no</span></span>             | <span data-ttu-id="c38b4-473">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-473">no</span></span>           |
| <span data-ttu-id="c38b4-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c38b4-474">msdyn_finish</span></span>                                     | <span data-ttu-id="c38b4-475">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-475">no</span></span>             | <span data-ttu-id="c38b4-476">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-476">no</span></span>           |
| <span data-ttu-id="c38b4-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="c38b4-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="c38b4-478">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-478">no</span></span>             | <span data-ttu-id="c38b4-479">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-479">no</span></span>           |
| <span data-ttu-id="c38b4-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="c38b4-480">msdyn_hours</span></span>                                      | <span data-ttu-id="c38b4-481">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-481">no</span></span>             | <span data-ttu-id="c38b4-482">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-482">no</span></span>           |
| <span data-ttu-id="c38b4-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="c38b4-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="c38b4-484">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-484">no</span></span>             | <span data-ttu-id="c38b4-485">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-485">no</span></span>           |
| <span data-ttu-id="c38b4-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="c38b4-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="c38b4-487">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-487">no</span></span>             | <span data-ttu-id="c38b4-488">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-488">no</span></span>           |
| <span data-ttu-id="c38b4-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="c38b4-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="c38b4-490">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-490">no</span></span>             | <span data-ttu-id="c38b4-491">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-491">no</span></span>           |
| <span data-ttu-id="c38b4-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="c38b4-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="c38b4-493">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-493">no</span></span>             | <span data-ttu-id="c38b4-494">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-494">no</span></span>           |
| <span data-ttu-id="c38b4-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="c38b4-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="c38b4-496">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-496">no</span></span>             | <span data-ttu-id="c38b4-497">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-497">no</span></span>           |
| <span data-ttu-id="c38b4-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="c38b4-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="c38b4-499">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-499">no</span></span>             | <span data-ttu-id="c38b4-500">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-500">no</span></span>           |
| <span data-ttu-id="c38b4-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="c38b4-501">msdyn_start</span></span>                                      | <span data-ttu-id="c38b4-502">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-502">no</span></span>             | <span data-ttu-id="c38b4-503">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="c38b4-504">Project</span><span class="sxs-lookup"><span data-stu-id="c38b4-504">Project</span></span>

| <span data-ttu-id="c38b4-505">**논리적 이름**</span><span class="sxs-lookup"><span data-stu-id="c38b4-505">**Logical name**</span></span>                       | <span data-ttu-id="c38b4-506">**생성 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-506">**Can create**</span></span> | <span data-ttu-id="c38b4-507">**편집 가능**</span><span class="sxs-lookup"><span data-stu-id="c38b4-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="c38b4-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="c38b4-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="c38b4-509">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-509">no</span></span>             | <span data-ttu-id="c38b4-510">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-510">no</span></span>           |
| <span data-ttu-id="c38b4-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="c38b4-512">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-512">no</span></span>             | <span data-ttu-id="c38b4-513">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-513">no</span></span>           |
| <span data-ttu-id="c38b4-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="c38b4-515">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-515">no</span></span>             | <span data-ttu-id="c38b4-516">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-516">no</span></span>           |
| <span data-ttu-id="c38b4-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="c38b4-518">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-518">no</span></span>             | <span data-ttu-id="c38b4-519">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-519">no</span></span>           |
| <span data-ttu-id="c38b4-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="c38b4-521">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-521">no</span></span>             | <span data-ttu-id="c38b4-522">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-522">no</span></span>           |
| <span data-ttu-id="c38b4-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="c38b4-524">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-524">no</span></span>             | <span data-ttu-id="c38b4-525">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-525">no</span></span>           |
| <span data-ttu-id="c38b4-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="c38b4-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="c38b4-527">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-527">yes</span></span>            | <span data-ttu-id="c38b4-528">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-528">no</span></span>           |
| <span data-ttu-id="c38b4-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="c38b4-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="c38b4-530">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-530">yes</span></span>            | <span data-ttu-id="c38b4-531">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-531">no</span></span>           |
| <span data-ttu-id="c38b4-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="c38b4-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="c38b4-533">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-533">yes</span></span>            | <span data-ttu-id="c38b4-534">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-534">no</span></span>           |
| <span data-ttu-id="c38b4-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="c38b4-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="c38b4-536">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-536">no</span></span>             | <span data-ttu-id="c38b4-537">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-537">no</span></span>           |
| <span data-ttu-id="c38b4-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c38b4-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="c38b4-539">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-539">no</span></span>             | <span data-ttu-id="c38b4-540">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-540">no</span></span>           |
| <span data-ttu-id="c38b4-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="c38b4-542">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-542">no</span></span>             | <span data-ttu-id="c38b4-543">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-543">no</span></span>           |
| <span data-ttu-id="c38b4-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="c38b4-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="c38b4-545">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-545">no</span></span>             | <span data-ttu-id="c38b4-546">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-546">no</span></span>           |
| <span data-ttu-id="c38b4-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="c38b4-548">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-548">no</span></span>             | <span data-ttu-id="c38b4-549">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-549">no</span></span>           |
| <span data-ttu-id="c38b4-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="c38b4-550">msdyn_duration</span></span>                         | <span data-ttu-id="c38b4-551">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-551">no</span></span>             | <span data-ttu-id="c38b4-552">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-552">no</span></span>           |
| <span data-ttu-id="c38b4-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c38b4-553">msdyn_effort</span></span>                           | <span data-ttu-id="c38b4-554">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-554">no</span></span>             | <span data-ttu-id="c38b4-555">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-555">no</span></span>           |
| <span data-ttu-id="c38b4-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c38b4-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="c38b4-557">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-557">no</span></span>             | <span data-ttu-id="c38b4-558">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-558">no</span></span>           |
| <span data-ttu-id="c38b4-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="c38b4-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="c38b4-560">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-560">no</span></span>             | <span data-ttu-id="c38b4-561">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-561">no</span></span>           |
| <span data-ttu-id="c38b4-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c38b4-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="c38b4-563">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-563">no</span></span>             | <span data-ttu-id="c38b4-564">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-564">no</span></span>           |
| <span data-ttu-id="c38b4-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c38b4-565">msdyn_finish</span></span>                           | <span data-ttu-id="c38b4-566">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-566">yes</span></span>            | <span data-ttu-id="c38b4-567">예</span><span class="sxs-lookup"><span data-stu-id="c38b4-567">yes</span></span>          |
| <span data-ttu-id="c38b4-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="c38b4-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="c38b4-569">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-569">no</span></span>             | <span data-ttu-id="c38b4-570">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-570">no</span></span>           |
| <span data-ttu-id="c38b4-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="c38b4-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="c38b4-572">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-572">no</span></span>             | <span data-ttu-id="c38b4-573">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-573">no</span></span>           |
| <span data-ttu-id="c38b4-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="c38b4-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="c38b4-575">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-575">no</span></span>             | <span data-ttu-id="c38b4-576">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-576">no</span></span>           |
| <span data-ttu-id="c38b4-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="c38b4-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="c38b4-578">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-578">no</span></span>             | <span data-ttu-id="c38b4-579">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-579">no</span></span>           |
| <span data-ttu-id="c38b4-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="c38b4-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="c38b4-581">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-581">no</span></span>             | <span data-ttu-id="c38b4-582">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-582">no</span></span>           |
| <span data-ttu-id="c38b4-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="c38b4-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="c38b4-584">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-584">no</span></span>             | <span data-ttu-id="c38b4-585">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-585">no</span></span>           |
| <span data-ttu-id="c38b4-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="c38b4-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="c38b4-587">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-587">no</span></span>             | <span data-ttu-id="c38b4-588">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-588">no</span></span>           |
| <span data-ttu-id="c38b4-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="c38b4-590">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-590">no</span></span>             | <span data-ttu-id="c38b4-591">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-591">no</span></span>           |
| <span data-ttu-id="c38b4-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="c38b4-593">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-593">no</span></span>             | <span data-ttu-id="c38b4-594">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-594">no</span></span>           |
| <span data-ttu-id="c38b4-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="c38b4-596">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-596">no</span></span>             | <span data-ttu-id="c38b4-597">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-597">no</span></span>           |
| <span data-ttu-id="c38b4-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="c38b4-599">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-599">no</span></span>             | <span data-ttu-id="c38b4-600">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-600">no</span></span>           |
| <span data-ttu-id="c38b4-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="c38b4-602">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-602">no</span></span>             | <span data-ttu-id="c38b4-603">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-603">no</span></span>           |
| <span data-ttu-id="c38b4-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="c38b4-604">msdyn_progress</span></span>                         | <span data-ttu-id="c38b4-605">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-605">no</span></span>             | <span data-ttu-id="c38b4-606">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-606">no</span></span>           |
| <span data-ttu-id="c38b4-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="c38b4-608">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-608">no</span></span>             | <span data-ttu-id="c38b4-609">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-609">no</span></span>           |
| <span data-ttu-id="c38b4-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="c38b4-611">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-611">no</span></span>             | <span data-ttu-id="c38b4-612">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-612">no</span></span>           |
| <span data-ttu-id="c38b4-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="c38b4-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="c38b4-614">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-614">no</span></span>             | <span data-ttu-id="c38b4-615">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-615">no</span></span>           |
| <span data-ttu-id="c38b4-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="c38b4-617">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-617">no</span></span>             | <span data-ttu-id="c38b4-618">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-618">no</span></span>           |
| <span data-ttu-id="c38b4-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="c38b4-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="c38b4-620">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-620">no</span></span>             | <span data-ttu-id="c38b4-621">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-621">no</span></span>           |
| <span data-ttu-id="c38b4-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="c38b4-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="c38b4-623">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-623">no</span></span>             | <span data-ttu-id="c38b4-624">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-624">no</span></span>           |
| <span data-ttu-id="c38b4-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="c38b4-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="c38b4-626">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-626">no</span></span>             | <span data-ttu-id="c38b4-627">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-627">no</span></span>           |
| <span data-ttu-id="c38b4-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="c38b4-629">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-629">no</span></span>             | <span data-ttu-id="c38b4-630">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-630">no</span></span>           |
| <span data-ttu-id="c38b4-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="c38b4-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="c38b4-632">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-632">no</span></span>             | <span data-ttu-id="c38b4-633">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-633">no</span></span>           |
| <span data-ttu-id="c38b4-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="c38b4-635">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-635">no</span></span>             | <span data-ttu-id="c38b4-636">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-636">no</span></span>           |
| <span data-ttu-id="c38b4-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="c38b4-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="c38b4-638">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-638">no</span></span>             | <span data-ttu-id="c38b4-639">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-639">no</span></span>           |
| <span data-ttu-id="c38b4-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="c38b4-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="c38b4-641">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-641">no</span></span>             | <span data-ttu-id="c38b4-642">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-642">no</span></span>           |
| <span data-ttu-id="c38b4-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="c38b4-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="c38b4-644">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-644">no</span></span>             | <span data-ttu-id="c38b4-645">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-645">no</span></span>           |
| <span data-ttu-id="c38b4-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="c38b4-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="c38b4-647">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-647">no</span></span>             | <span data-ttu-id="c38b4-648">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-648">no</span></span>           |
| <span data-ttu-id="c38b4-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="c38b4-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="c38b4-650">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-650">no</span></span>             | <span data-ttu-id="c38b4-651">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-651">no</span></span>           |
| <span data-ttu-id="c38b4-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="c38b4-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="c38b4-653">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-653">no</span></span>             | <span data-ttu-id="c38b4-654">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-654">no</span></span>           |
| <span data-ttu-id="c38b4-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="c38b4-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="c38b4-656">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-656">no</span></span>             | <span data-ttu-id="c38b4-657">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-657">no</span></span>           |
| <span data-ttu-id="c38b4-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="c38b4-659">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-659">no</span></span>             | <span data-ttu-id="c38b4-660">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-660">no</span></span>           |
| <span data-ttu-id="c38b4-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="c38b4-662">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-662">no</span></span>             | <span data-ttu-id="c38b4-663">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-663">no</span></span>           |
| <span data-ttu-id="c38b4-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="c38b4-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="c38b4-665">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-665">no</span></span>             | <span data-ttu-id="c38b4-666">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-666">no</span></span>           |
| <span data-ttu-id="c38b4-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c38b4-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="c38b4-668">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-668">no</span></span>             | <span data-ttu-id="c38b4-669">아니요</span><span class="sxs-lookup"><span data-stu-id="c38b4-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="c38b4-670">제한 사항 및 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="c38b4-670">Limitations and known issues</span></span>
<span data-ttu-id="c38b4-671">다음은 제한 사항 및 알려진 문제 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="c38b4-672">일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="c38b4-673">다음 사용자는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-673">They can't be used by:</span></span>
    - <span data-ttu-id="c38b4-674">응용 프로그램 사용자</span><span class="sxs-lookup"><span data-stu-id="c38b4-674">Application users</span></span>
    - <span data-ttu-id="c38b4-675">시스템 사용자</span><span class="sxs-lookup"><span data-stu-id="c38b4-675">System users</span></span>
    - <span data-ttu-id="c38b4-676">통합 사용자</span><span class="sxs-lookup"><span data-stu-id="c38b4-676">Integration users</span></span>
    - <span data-ttu-id="c38b4-677">필요한 라이선스가 없는 다른 사용자</span><span class="sxs-lookup"><span data-stu-id="c38b4-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="c38b4-678">각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="c38b4-679">각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="c38b4-680">Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="c38b4-681">**OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="c38b4-682">프로젝트 및 작업에 대한 제한 및 경계</span><span class="sxs-lookup"><span data-stu-id="c38b4-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="c38b4-683">오류 처리</span><span class="sxs-lookup"><span data-stu-id="c38b4-683">Error handling</span></span>

   - <span data-ttu-id="c38b4-684">작업 세트에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **작업 세트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="c38b4-685">Project Scheduling Service에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **PSS 오류 로그** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="c38b4-686">샘플 시나리오</span><span class="sxs-lookup"><span data-stu-id="c38b4-686">Sample scenario</span></span>

<span data-ttu-id="c38b4-687">이 시나리오에서는 프로젝트, 팀 구성원, 4개의 작업 및 2개의 리소스 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="c38b4-688">다음으로 하나의 작업을 업데이트하고, 프로젝트를 업데이트하고, 하나의 작업을 삭제하고, 하나의 리소스 할당을 삭제하고, 작업 종속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c38b4-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="c38b4-689">추가 샘플</span><span class="sxs-lookup"><span data-stu-id="c38b4-689">Additional samples</span></span>

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
