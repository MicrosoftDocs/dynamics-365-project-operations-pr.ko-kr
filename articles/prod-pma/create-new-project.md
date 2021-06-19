---
title: 새 프로젝트 만들기
description: 이 주제는 새 프로젝트를 만드는 방법에 대한 정보를 제공합니다.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006249"
---
# <a name="create-a-new-project"></a><span data-ttu-id="ac51e-103">새 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="ac51e-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac51e-104">새 프로젝트를 생성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="ac51e-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="ac51e-105">**프로젝트 관리** 페이지에서 **새 프로젝트** 를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="ac51e-106">**프로젝트 유형:** 시간과 재료</span><span class="sxs-lookup"><span data-stu-id="ac51e-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="ac51e-107">**프로젝트 이름:** XYZ 업그레이드 2단계</span><span class="sxs-lookup"><span data-stu-id="ac51e-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="ac51e-108">**프로젝트 그룹:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="ac51e-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="ac51e-109">**프로젝트 계약 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="ac51e-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="ac51e-110">**프로젝트 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="ac51e-111">프로젝트에 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="ac51e-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="ac51e-112">**작업자** 페이지의 **작업자** 목록에서 이전에 역량을 설정한 작업자의 레코드를 선택하고 작업자 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="ac51e-113">작업 창의 **프로젝트** 탭에 있는 **설정** 그룹에서 **프로젝트 할당** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="ac51e-114">**리소스 유휴성 검사 프로젝트 할당** 페이지의 **프로젝트** 탭에 있는 **선택한 프로젝트에 프로젝트 추가** 필드에서 **XYZ 업그레이드 2단계** 프로젝트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="ac51e-115">**남은 프로젝트** 창에서 프로젝트를 선택한 다음 화살표 단추를 선택하여 **선택한 프로젝트** 창에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="ac51e-116">필요에 따라 리소스에 대한 범주를 할당할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="ac51e-117">범주 유형은 **비용** 또는 **수익** 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="ac51e-118">범주 유형은 조직에서 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-118">The category type is determined by your organization.</span></span> <span data-ttu-id="ac51e-119">리소스에 할당된 범주가 없는 경우 Finance는 비용 및 수익에 대한 시간 가격의 기본 범주를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="ac51e-120">프로젝트 리소스 및 역할 특성 설정</span><span class="sxs-lookup"><span data-stu-id="ac51e-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="ac51e-121">프로젝트 관리자는 프로젝트 리소싱 기능을 사용하여 프로젝트에 필요한 역할을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="ac51e-122">리소스를 예약할 때 확인된 리소스를 알 수 없는 경우 역할을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="ac51e-123">프로젝트 계획 단계를 계속할 수 있도록 역할을 계획된 리소스로 임시로 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="ac51e-124">[![역할의 예](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="ac51e-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="ac51e-125">**시나리오:** Contoso는 승인된 프로젝트 헌장이 있는 시간 및 재료 프로젝트를 완료하기 위해 고용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="ac51e-126">주니어 프로젝트 관리자는 아직 프로젝트 범위를 완료하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="ac51e-127">리소스 관리자는 현재 새 프로젝트에서 작업하기 위해 예약할 특정 리소스를 식별하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="ac51e-128">프로젝트의 중요한 특성 때문에 프로젝트 후원자는 역할 중 하나로 수석 프로젝트 관리자를 요청했습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="ac51e-129">리소스 관리자는 새 리소스를 획득하고 하위 프로젝트 관리자가 프로젝트 계획 중에 리소스 정보를 요구하는 경우 시스템에서 역할을 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="ac51e-130">다음 단계는 리소스 관리자가 수석 프로젝트 관리자 역할을 설정하고 리소스 특성을 연관시키는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="ac51e-131">나중에 역할을 사용하여 필요한 리소스 역량과 일치하는 사용 가능한 리소스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="ac51e-132">**역할 설정** 페이지에서 **신규** 를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="ac51e-133">**역할 ID:** 수석 프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="ac51e-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="ac51e-134">**설명:** 수석 프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="ac51e-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="ac51e-135">**만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-135">Select **Create**.</span></span>
3. <span data-ttu-id="ac51e-136">**수석 프로젝트 관리자** 역할을 선택한 다음 **특성 구성** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="ac51e-137">**특징 유형** 필드에서 **기술** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="ac51e-138">**사용 가능한 특징** 필드에 검색할 기술을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="ac51e-139">**특징 유형** 필드에서 **인증서** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="ac51e-140">**사용 가능한 특징** 필드에 검색할 인증서 유형을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="ac51e-141">프로젝트에 프로젝트 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="ac51e-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="ac51e-142">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="ac51e-143">**프로젝트 팀 및 일정** 탭에서 **추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="ac51e-144">**역할** 필드에서 **팀 구성원** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="ac51e-145">**일정에서 예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="ac51e-146">**리소스 가용성** 페이지에서 **설정 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="ac51e-147">**보기 설정 조정** 페이지에서 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="ac51e-148">**날짜 범위 보기 형식:** 일</span><span class="sxs-lookup"><span data-stu-id="ac51e-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="ac51e-149">**가용성 설명 표시:** 예</span><span class="sxs-lookup"><span data-stu-id="ac51e-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="ac51e-150">**남은 용량 표시:** 예</span><span class="sxs-lookup"><span data-stu-id="ac51e-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="ac51e-151">리소스 목록에서 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="ac51e-152">**확정 예약** 과 **전체 생산 능력** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="ac51e-153">기본 역할에 리소스 할당</span><span class="sxs-lookup"><span data-stu-id="ac51e-153">Assign a resource to a default role</span></span>

<span data-ttu-id="ac51e-154">프로젝트 또는 리소스 관리자를 돕기 위해 프로젝트에 예약할 수 있는 리소스에 대해 추가로 드릴다운할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="ac51e-155">기본 역할을 기존 리소스 또는 새로 획득한 리소스와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="ac51e-156">예를 들어 Daniel이 고용되었을 때 비즈니스 분석가 역할을 수행할 수 있는 경험과 기술이 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="ac51e-157">리소스 관리자가 이 역할을 Daniel의 기본 역할로 할당했습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="ac51e-158">따라서 리소스 관리자는 Daniel을 프로젝트 작업에 사용할 수 있는 비즈니스 분석가 풀에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="ac51e-159">리소스 예약 중에 프로젝트 관리자는 프로젝트 작업에 사용할 수 있는 역할 리소스를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="ac51e-160">리소스 이행 중에 다중 기준 결정 분석을 수행할 때 이 정보를 하나의 기준으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="ac51e-161">또한 필터에 다른 리소스 특성을 추가하여 특정 프로젝트에 대한 특정 기술, 교육 및 경험이 있는 리소스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="ac51e-162">**시나리오:** 승인된 프로젝트가 시작되었으며 프로젝트 계획 단계에서 수석 프로젝트 관리자 역할이 계획된 리소스로 예약되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="ac51e-163">리소스 관리자는 이제 수석 프로젝트 관리자 역할을 수행할 리소스를 획득했습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="ac51e-164">**리소스 목록** 페이지에서 **Daniel Goldschmidt** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="ac51e-165">**리소스 역할** 페이지에서 **신규** 를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="ac51e-166">**유효:** 현재 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="ac51e-167">**만료:** **사용 안 함** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="ac51e-168">**역할:** **수석 프로젝트 관리자** 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="ac51e-169">**저장** 을 선택한 다음 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="ac51e-170">**역량** 탭에서 **ProjectMgmt** 기술 및 **PMP** 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ac51e-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]