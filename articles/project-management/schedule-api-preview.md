---
title: 일정 엔터티로 일정 API를 사용하여 작업 수행
description: 이 항목은 일정 API 사용에 대한 정보와 샘플을 제공합니다.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868137"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="a8837-103">일정 엔터티로 일정 API를 사용하여 작업 수행</span><span class="sxs-lookup"><span data-stu-id="a8837-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="a8837-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a8837-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a8837-105">이 항목에 언급된 일부 또는 모든 기능은 미리 보기 릴리스의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="a8837-106">내용과 기능은 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="a8837-107">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="a8837-107">Scheduling entities</span></span>

<span data-ttu-id="a8837-108">일정 API는 **예약 엔터티** 를 통해 생성, 업데이트 및 삭제 작업을 수행할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="a8837-109">이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="a8837-110">**예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="a8837-111">다음 표는 **예약 엔터티** 전체 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="a8837-112">엔터티 이름</span><span class="sxs-lookup"><span data-stu-id="a8837-112">Entity name</span></span>  | <span data-ttu-id="a8837-113">엔터티 논리적 이름</span><span class="sxs-lookup"><span data-stu-id="a8837-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="a8837-114">Project</span><span class="sxs-lookup"><span data-stu-id="a8837-114">Project</span></span> | <span data-ttu-id="a8837-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a8837-115">msdyn_project</span></span> |
| <span data-ttu-id="a8837-116">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="a8837-116">Project Task</span></span>  | <span data-ttu-id="a8837-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="a8837-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="a8837-118">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="a8837-118">Project Task Dependency</span></span>  | <span data-ttu-id="a8837-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="a8837-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="a8837-120">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="a8837-120">Resource Assignment</span></span> | <span data-ttu-id="a8837-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="a8837-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="a8837-122">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="a8837-122">Project Bucket</span></span>  | <span data-ttu-id="a8837-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="a8837-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="a8837-124">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="a8837-124">Project Team Member</span></span> | <span data-ttu-id="a8837-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="a8837-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="a8837-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="a8837-126">OperationSet</span></span>

<span data-ttu-id="a8837-127">OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="a8837-128">일정 API</span><span class="sxs-lookup"><span data-stu-id="a8837-128">Schedule APIs</span></span>

<span data-ttu-id="a8837-129">다음은 현재 일정 API 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="a8837-130">**msdyn_CreateProjectV1**: 이 API를 사용하여 프로젝트를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="a8837-131">프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="a8837-132">**msdyn_CreateTeamMemberV1**: 이 API를 사용하여 프로젝트 팀 구성원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="a8837-133">팀 구성원 레코드가 즉시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="a8837-134">**msdyn_CreateOperationSetV1**: 이 API는 트랜잭션 내에서 수행해야 하는 여러 요청을 예약하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="a8837-135">**msdyn_PSSCreateV1**: 이 API는 엔터티를 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="a8837-136">엔터티는 만들기 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="a8837-137">**msdyn_PSSUpdateV1**: 이 API는 엔터티를 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="a8837-138">엔터티는 업데이트 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="a8837-139">**msdyn_PSSDeleteV1**: 이 API는 엔터티를 삭제하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="a8837-140">엔터티는 삭제 작업을 지원하는 일정 엔터티 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="a8837-141">**msdyn_ExecuteOperationSetV1**: 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="a8837-142">OperationSet과 함께 일정 API 사용</span><span class="sxs-lookup"><span data-stu-id="a8837-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="a8837-143">**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="a8837-144">그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="a8837-145">지원되는 작업</span><span class="sxs-lookup"><span data-stu-id="a8837-145">Supported operations</span></span>

| <span data-ttu-id="a8837-146">예약 엔터티</span><span class="sxs-lookup"><span data-stu-id="a8837-146">Scheduling entity</span></span> | <span data-ttu-id="a8837-147">만들기</span><span class="sxs-lookup"><span data-stu-id="a8837-147">Create</span></span> | <span data-ttu-id="a8837-148">엽데이트</span><span class="sxs-lookup"><span data-stu-id="a8837-148">Update</span></span> | <span data-ttu-id="a8837-149">Delete</span><span class="sxs-lookup"><span data-stu-id="a8837-149">Delete</span></span> | <span data-ttu-id="a8837-150">중요 사항</span><span class="sxs-lookup"><span data-stu-id="a8837-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="a8837-151">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="a8837-151">Project task</span></span> | <span data-ttu-id="a8837-152">네</span><span class="sxs-lookup"><span data-stu-id="a8837-152">Yes</span></span> | <span data-ttu-id="a8837-153">네</span><span class="sxs-lookup"><span data-stu-id="a8837-153">Yes</span></span> | <span data-ttu-id="a8837-154">네</span><span class="sxs-lookup"><span data-stu-id="a8837-154">Yes</span></span> | <span data-ttu-id="a8837-155">없음</span><span class="sxs-lookup"><span data-stu-id="a8837-155">None</span></span> |
| <span data-ttu-id="a8837-156">프로젝트 작업 종속성</span><span class="sxs-lookup"><span data-stu-id="a8837-156">Project task dependency</span></span> | <span data-ttu-id="a8837-157">네</span><span class="sxs-lookup"><span data-stu-id="a8837-157">Yes</span></span> | <span data-ttu-id="a8837-158">네</span><span class="sxs-lookup"><span data-stu-id="a8837-158">Yes</span></span> | | <span data-ttu-id="a8837-159">프로젝트 작업 종속성 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="a8837-160">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a8837-161">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="a8837-161">Resource assignment</span></span> | <span data-ttu-id="a8837-162">네</span><span class="sxs-lookup"><span data-stu-id="a8837-162">Yes</span></span> | <span data-ttu-id="a8837-163">네</span><span class="sxs-lookup"><span data-stu-id="a8837-163">Yes</span></span> | | <span data-ttu-id="a8837-164">**BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="a8837-165">리소스 할당 레코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="a8837-166">대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a8837-167">프로젝트 버킷</span><span class="sxs-lookup"><span data-stu-id="a8837-167">Project bucket</span></span> | <span data-ttu-id="a8837-168">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a8837-168">N/A</span></span> | <span data-ttu-id="a8837-169">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a8837-169">N/A</span></span> | <span data-ttu-id="a8837-170">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a8837-170">N/A</span></span> | <span data-ttu-id="a8837-171">기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="a8837-172">프로젝트 팀원</span><span class="sxs-lookup"><span data-stu-id="a8837-172">Project team member</span></span> | <span data-ttu-id="a8837-173">네</span><span class="sxs-lookup"><span data-stu-id="a8837-173">Yes</span></span> | <span data-ttu-id="a8837-174">네</span><span class="sxs-lookup"><span data-stu-id="a8837-174">Yes</span></span> | <span data-ttu-id="a8837-175">네</span><span class="sxs-lookup"><span data-stu-id="a8837-175">Yes</span></span> | <span data-ttu-id="a8837-176">생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="a8837-177">Project</span><span class="sxs-lookup"><span data-stu-id="a8837-177">Project</span></span> | <span data-ttu-id="a8837-178">네</span><span class="sxs-lookup"><span data-stu-id="a8837-178">Yes</span></span> | <span data-ttu-id="a8837-179">네</span><span class="sxs-lookup"><span data-stu-id="a8837-179">Yes</span></span> | <span data-ttu-id="a8837-180">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a8837-180">N/A</span></span> | <span data-ttu-id="a8837-181">**StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="a8837-182">이러한 API는 사용자 지정 필드를 포함하는 엔터티 개체를 사용하여 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="a8837-183">ID 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-183">The ID property is optional.</span></span> <span data-ttu-id="a8837-184">제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="a8837-185">제공되지 않으면 시스템에서 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="a8837-186">제한 사항 및 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="a8837-186">Limitations and known issues</span></span>
<span data-ttu-id="a8837-187">다음은 제한 사항 및 알려진 문제 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="a8837-188">일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="a8837-189">다음 사용자는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-189">They can't be used by:</span></span>
    - <span data-ttu-id="a8837-190">응용 프로그램 사용자</span><span class="sxs-lookup"><span data-stu-id="a8837-190">Application users</span></span>
    - <span data-ttu-id="a8837-191">시스템 사용자</span><span class="sxs-lookup"><span data-stu-id="a8837-191">System users</span></span>
    - <span data-ttu-id="a8837-192">통합 사용자</span><span class="sxs-lookup"><span data-stu-id="a8837-192">Integration users</span></span>
    - <span data-ttu-id="a8837-193">필요한 라이선스가 없는 다른 사용자</span><span class="sxs-lookup"><span data-stu-id="a8837-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="a8837-194">각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="a8837-195">각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="a8837-196">Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="a8837-197">**OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="a8837-198">일정 API는 공개 미리 보기입니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="a8837-199">프로덕션 환경에서 이러한 API를 사용하는 것은 Microsoft에서 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="a8837-200">샘플 시나리오</span><span class="sxs-lookup"><span data-stu-id="a8837-200">Sample scenario</span></span>

<span data-ttu-id="a8837-201">이 시나리오에서는 프로젝트, 팀 구성원, 4개의 작업 및 2개의 리소스 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="a8837-202">다음으로 하나의 작업을 업데이트하고, 프로젝트를 업데이트하고, 하나의 작업을 삭제하고, 하나의 리소스 할당을 삭제하고, 작업 종속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8837-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="a8837-203">추가 샘플</span><span class="sxs-lookup"><span data-stu-id="a8837-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
