---
title: 프로젝트 리소싱
description: 이 항목은 프로젝트 리소싱에 대한 정보를 제공합니다.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753212"
---
# <a name="project-resourcing"></a><span data-ttu-id="8ccda-103">프로젝트 리소싱</span><span class="sxs-lookup"><span data-stu-id="8ccda-103">Project resourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ccda-104">이 항목은 프로젝트 리소싱에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="8ccda-105">프로젝트 계획 단계에서 프로젝트 관리자와 리소스 관리자가 겪는 한 가지 과제는 리소스 할당으로, 프로젝트에서 작업할 올바른 리소스를 결정하고 예약해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="8ccda-106">Dynamics 365 Finance에서는 프로젝트에 대한 리소스 기능을 사용하면 특정 참여 또는 참여의 일부를 위해 예약할 수 있는 임시 리소스로 처리되는 역할을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-106">In Dynamics 365 Finance, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="8ccda-107">이러한 유형의 리소싱을 통해 프로젝트 관리자와 리소스 관리자는 다음 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="8ccda-108">리소스를 쉽게 일치시킬 수 있도록 필요한 역량이 있는 역할을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="8ccda-109">역할을 사용하여 예약된 리소스를 기반으로 하는 초기 참여 일정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="8ccda-110">프로젝트에 할당된 역할 및 리소스를 기반으로 비용을 추정하고 초기 예산을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="8ccda-111">역할을 사용하여 각 참여에 필요한 리소스 예약 수를 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="8ccda-112">프로젝트의 전체 수명 주기에 필요한 리소스 수를 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="8ccda-113">초기 리소스 할당을 사용하여 작업 분할 구조(WBS) 초안을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="8ccda-114">[![프로젝트 수명 주기](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="8ccda-115">프로젝트 계획이 진행됨에 따라 계획된 리소스는 인력이 있는 리소스로 대체될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="8ccda-116">프로젝트 관리자는 모든 프로젝트 단계에서 다시 돌아가 리소스 예약을 업데이트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="8ccda-117">프로젝트 리소스 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-117">Set up project resources</span></span>
<span data-ttu-id="8ccda-118">일정을 설정하고 이를 직원 또는 근로자와 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="8ccda-119">일정은 프로젝트와 프로젝트를 위해 예약된 자원의 작업 시간을 예약하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="8ccda-120">일정 설정 중에 프로젝트 관리자는 리소스 최적화의 일부로 리소스 평준화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-120">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="8ccda-121">일정 예약에 따라 리소스에 제한을 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-121">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="8ccda-122">**일정** 페이지에서 일정을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-122">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="8ccda-123">작업자를 프로젝트 리소스로 설정할 때 리소스를 설정하려는 회사에서 근무하는 작업자 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-123">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="8ccda-124">또는 조직의 다른 회사에서 근무하는 근로자를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-124">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="8ccda-125">이러한 작업자를 회사 간 리소스라고합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-125">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="8ccda-126">다음 절차에서는 회사에서 작업자를 프로젝트 리소스로 설정하는 방법과 회사 간 프로젝트 리소스를 설정하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-126">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="8ccda-127">작업자를 프로젝트 리소스로 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-127">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="8ccda-128">**작업자** 페이지의 **작업자** 목록에서 프로젝트 리소스로 추가할 작업자를 선택하고 작업자 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-128">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="8ccda-129">작업 창에서 **프로젝트** &gt; **설정** &gt; **프로젝트 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-129">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="8ccda-130">일정을 선택한 다음 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-130">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="8ccda-131">리소스에 대한 기본 프로젝트를 사전 할당 유형으로 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-131">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="8ccda-132">사전 할당은 리소스 관리자 또는 프로젝트 관리자가 리소스가 미리 작업할 프로젝트를 알고 있을 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-132">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="8ccda-133">사전 할당은 프로젝트 후원자 또는 고객의 요청을 기반으로 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-133">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="8ccda-134">프로젝트를 사전 할당하려면 **프로젝트 할당** 페이지의 **프로젝트** 탭에 있는 **남은 프로젝트** 목록에서 적절한 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-134">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="8ccda-135">회사 간 리소스 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-135">Set up an intercompany resource</span></span>

<span data-ttu-id="8ccda-136">작업자를 회사 간 리소스로 설정하는 경우 대출 회사와 차용 회사 모두에서 설정을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-136">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

<span data-ttu-id="8ccda-137">**대출 회사에서**</span><span class="sxs-lookup"><span data-stu-id="8ccda-137">**In the lending company**</span></span>

1. <span data-ttu-id="8ccda-138">Finance에서 대출 회사가 선택되었는지 확인한 다음 이전 섹션인 "작업자를 프로젝트 리소스로 설정"의 절차를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-138">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="8ccda-139">**회사 간 회계** 페이지에서 **신규**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-139">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="8ccda-140">**법인 ID** 필드에서 대출 회사를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-140">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="8ccda-141">나머지 필드를 적절히 입력한 다음, **저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-141">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="8ccda-142">**이전 가격** 페이지에서 **신규**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-142">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="8ccda-143">**차용 법인** 필드에서 적절한 회사를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-143">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="8ccda-144">이 섹션의 시작 부분에서 생성한 리소스만 차용 회사에 빌려주려면 **리소스** 필드에서 생성한 리소스의 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-144">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="8ccda-145">대출 회사의 모든 리소스를 차용 회사가 사용할 수 있도록 하려면 **리소스** 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-145">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="8ccda-146">**프로젝트 관리 및 회계 매개 변수** 페이지의 **회사 간** 탭에서 **회사 간 리소스 일정 및 작업 표 사용** 옵션을 **예**로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-146">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

<span data-ttu-id="8ccda-147">**차용 회사에서**</span><span class="sxs-lookup"><span data-stu-id="8ccda-147">**In the borrowing company**</span></span>

- <span data-ttu-id="8ccda-148">**리소스 목록** 페이지의 검색 필터에 대출 회사에 대해 생성한 리소스의 이름을 입력하여 이름이 차용 회사의 리소스 목록에 포함되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-148">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="8ccda-149">리소스 역량 관리</span><span class="sxs-lookup"><span data-stu-id="8ccda-149">Manage resource competencies</span></span>
<span data-ttu-id="8ccda-150">리소스 역량은 리소스 관리의 필수적인 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-150">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="8ccda-151">역량은 기술, 교육, 인증 및 프로젝트 경험이 올바르게 균형을 이루는 리소스를 결정하는 기준으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-151">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="8ccda-152">각 리소스에 대해 이 정보를 설정하고 정기적으로 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-152">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="8ccda-153">이러한 방식으로 프로젝트 리소스 할당 중에 특정 리소스 역량이 일치할 때 기능을 최대화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-153">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="8ccda-154">[![기술, 인증, 교육 및 프로젝트 경험의 예](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-154">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="8ccda-155">다음 절차에서는 리소스에 대한 일부 역량을 설정하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-155">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="8ccda-156">작업자에 대한 역량을 설정하려면 인적 자원의 **작업자** 목록 페이지 또는 프로젝트 관리 및 회계의 **리소스** 목록 페이지 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-156">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="8ccda-157">다음 절차의 경우 인적 자원의 **작업자** 목록 페이지가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-157">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="8ccda-158">역량 설정: 인증서</span><span class="sxs-lookup"><span data-stu-id="8ccda-158">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="8ccda-159">**작업자** 목록 페이지에서 작업자가 인증서 정보를 추가할 행을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-159">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="8ccda-160">작업 창의 **작업자** 탭에 있는 **역량** 그룹에서 **인증서**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-160">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="8ccda-161">**새로 만들기**를 선택한 다음 **인증 유형** 필드에서 **PMP**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-161">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="8ccda-162">**시작 날짜** 필드에서 **2015년 10월 1일**을 선택하고 **저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-162">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="8ccda-163">역량 설정: 기술</span><span class="sxs-lookup"><span data-stu-id="8ccda-163">Set up competencies: Skills</span></span>

1. <span data-ttu-id="8ccda-164">**작업자** 목록 페이지에서 이전 절차에서 사용한 작업자가 여전히 선택되어 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ccda-164">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="8ccda-165">그런 다음 작업 창의 **작업자** 탭에 있는 **역량** 그룹에서 **기술**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-165">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="8ccda-166">**새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-166">Select **New**.</span></span>
3. <span data-ttu-id="8ccda-167">**기술** 필드에서 **프로젝트 관리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-167">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="8ccda-168">**수준** 필드에서 **5 전문가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-168">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="8ccda-169">**수준 날짜** 필드에서 **1-/14/2014**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-169">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="8ccda-170">**경험 년수** 필드에 **10**을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-170">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="8ccda-171">**저장**을 선택한 다음 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="8ccda-172">새 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="8ccda-172">Create a new project</span></span>
1. <span data-ttu-id="8ccda-173">**프로젝트 관리** 페이지에서 **새 프로젝트**를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-173">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="8ccda-174">**프로젝트 유형:** 시간과 재료</span><span class="sxs-lookup"><span data-stu-id="8ccda-174">**Project type:** Time and material</span></span>
    - <span data-ttu-id="8ccda-175">**프로젝트 이름:** XYZ 업그레이드 2단계</span><span class="sxs-lookup"><span data-stu-id="8ccda-175">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="8ccda-176">**프로젝트 그룹:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="8ccda-176">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="8ccda-177">**프로젝트 계약 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="8ccda-177">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="8ccda-178">**프로젝트 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-178">Select **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="8ccda-179">프로젝트에 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="8ccda-179">Assign a resource to a project</span></span>

1. <span data-ttu-id="8ccda-180">**작업자** 페이지의 **작업자** 목록에서 이전에 역량을 설정한 작업자의 레코드를 선택하고 작업자 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-180">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="8ccda-181">작업 창의 **프로젝트** 탭에 있는 **설정** 그룹에서 **프로젝트 할당**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-181">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="8ccda-182">**리소스 유휴성 검사 프로젝트 할당** 페이지의 **프로젝트** 탭에 있는 **선택한 프로젝트에 프로젝트 추가** 필드에서 **XYZ 업그레이드 2단계** 프로젝트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-182">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="8ccda-183">**남은 프로젝트** 창에서 프로젝트를 선택한 다음 화살표 단추를 선택하여 **선택한 프로젝트** 창에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-183">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="8ccda-184">필요에 따라 리소스에 대한 범주를 할당할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-184">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="8ccda-185">범주 유형은 **비용** 또는 **수익** 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-185">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="8ccda-186">범주 유형은 조직에서 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-186">The category type is determined by your organization.</span></span> <span data-ttu-id="8ccda-187">리소스에 할당된 범주가 없는 경우 Finance는 비용 및 수익에 대한 시간 가격의 기본 범주를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-187">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="8ccda-188">프로젝트 리소스 및 역할 특성 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-188">Set up project resource and role characteristics</span></span>

<span data-ttu-id="8ccda-189">프로젝트 관리자는 프로젝트 리소싱 기능을 사용하여 프로젝트에 필요한 역할을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-189">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="8ccda-190">리소스를 예약할 때 확인된 리소스를 알 수 없는 경우 역할을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-190">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="8ccda-191">프로젝트 계획 단계를 계속할 수 있도록 역할을 계획된 리소스로 임시로 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-191">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="8ccda-192">[![역할의 예](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-192">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="8ccda-193">**시나리오:** Contoso는 승인된 프로젝트 헌장이 있는 시간 및 재료 프로젝트를 완료하기 위해 고용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-193">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="8ccda-194">주니어 프로젝트 관리자는 아직 프로젝트 범위를 완료하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-194">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="8ccda-195">리소스 관리자는 현재 새 프로젝트에서 작업하기 위해 예약할 특정 리소스를 식별하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-195">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="8ccda-196">프로젝트의 중요한 특성 때문에 프로젝트 후원자는 역할 중 하나로 수석 프로젝트 관리자를 요청했습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-196">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="8ccda-197">리소스 관리자는 새 리소스를 획득하고 하위 프로젝트 관리자가 프로젝트 계획 중에 리소스 정보를 요구하는 경우 시스템에서 역할을 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-197">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="8ccda-198">다음 단계는 리소스 관리자가 수석 프로젝트 관리자 역할을 설정하고 리소스 특성을 연관시키는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-198">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="8ccda-199">나중에 역할을 사용하여 필요한 리소스 역량과 일치하는 사용 가능한 리소스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-199">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="8ccda-200">**역할 설정** 페이지에서 **신규**를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-200">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="8ccda-201">**역할 ID:** 수석 프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="8ccda-201">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="8ccda-202">**설명:** 수석 프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="8ccda-202">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="8ccda-203">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-203">Select **Create**.</span></span>
3. <span data-ttu-id="8ccda-204">**수석 프로젝트 관리자** 역할을 선택한 다음 **특성 구성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-204">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="8ccda-205">**특징 유형** 필드에서 **기술**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-205">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="8ccda-206">**사용 가능한 특징** 필드에 검색할 기술을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-206">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="8ccda-207">**특징 유형** 필드에서 **인증서**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-207">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="8ccda-208">**사용 가능한 특징** 필드에 검색할 인증서 유형을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-208">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="8ccda-209">프로젝트에 프로젝트 리소스를 배정</span><span class="sxs-lookup"><span data-stu-id="8ccda-209">Assign a project resource to a project</span></span>

1. <span data-ttu-id="8ccda-210">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-210">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="8ccda-211">**프로젝트 팀 및 일정** 탭에서 **추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-211">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="8ccda-212">**역할** 필드에서 **팀 구성원**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-212">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="8ccda-213">**일정에서 예약**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-213">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="8ccda-214">**리소스 가용성** 페이지에서 **설정 보기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-214">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="8ccda-215">**보기 설정 조정** 페이지에서 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-215">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="8ccda-216">**날짜 범위 보기 형식:** 일</span><span class="sxs-lookup"><span data-stu-id="8ccda-216">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="8ccda-217">**가용성 설명 표시:** 예</span><span class="sxs-lookup"><span data-stu-id="8ccda-217">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="8ccda-218">**남은 용량 표시:** 예</span><span class="sxs-lookup"><span data-stu-id="8ccda-218">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="8ccda-219">리소스 목록에서 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-219">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="8ccda-220">**확정 예약**과 **전체 생산 능력**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-220">Select **Hard book** and **Full capacity**.</span></span>


### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="8ccda-221">기본 역할에 리소스 할당</span><span class="sxs-lookup"><span data-stu-id="8ccda-221">Assign a resource to a default role</span></span>

<span data-ttu-id="8ccda-222">프로젝트 또는 리소스 관리자를 돕기 위해 프로젝트에 예약할 수 있는 리소스에 대해 추가로 드릴다운할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-222">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="8ccda-223">기본 역할을 기존 리소스 또는 새로 획득한 리소스와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-223">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="8ccda-224">예를 들어 Daniel이 고용되었을 때 비즈니스 분석가 역할을 수행할 수 있는 경험과 기술이 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-224">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="8ccda-225">리소스 관리자가 이 역할을 Daniel의 기본 역할로 할당했습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-225">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="8ccda-226">따라서 리소스 관리자는 Daniel을 프로젝트 작업에 사용할 수 있는 비즈니스 분석가 풀에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-226">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="8ccda-227">리소스 예약 중에 프로젝트 관리자는 프로젝트 작업에 사용할 수 있는 역할 리소스를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-227">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="8ccda-228">리소스 이행 중에 다중 기준 결정 분석을 수행할 때 이 정보를 하나의 기준으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-228">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="8ccda-229">또한 필터에 다른 리소스 특성을 추가하여 특정 프로젝트에 대한 특정 기술, 교육 및 경험이 있는 리소스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-229">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="8ccda-230">**시나리오:** 승인된 프로젝트가 시작되었으며 프로젝트 계획 단계에서 수석 프로젝트 관리자 역할이 계획된 리소스로 예약되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-230">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="8ccda-231">리소스 관리자는 이제 수석 프로젝트 관리자 역할을 수행할 리소스를 획득했습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-231">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="8ccda-232">**리소스 목록** 페이지에서 **Daniel Goldschmidt**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-232">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="8ccda-233">**리소스 역할** 페이지에서 **신규**를 선택하고 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-233">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="8ccda-234">**유효:** 현재 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-234">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="8ccda-235">**만료:** **사용 안 함**을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-235">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="8ccda-236">**역할:** **수석 프로젝트 관리자**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-236">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="8ccda-237">**저장**을 선택한 다음 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-237">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="8ccda-238">**역량** 탭에서 **ProjectMgmt** 기술 및 **PMP** 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-238">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="8ccda-239">역할 기반 가격 책정 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-239">Set up role-based pricing</span></span>
<span data-ttu-id="8ccda-240">역할에 대해 모든 비용, 판매 및 이전 가격을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-240">All cost, sales, and transfer prices can be set up for roles.</span></span>

1. <span data-ttu-id="8ccda-241">**판매 가격(시간)** 페이지에서 **신규**를 선택하고 유효 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-241">On the **Sales price (hour)** page, select **New**, and enter an effective date.</span></span>
2. <span data-ttu-id="8ccda-242">**역할** 열에서 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-242">In the **Role** column, select a role.</span></span>
3. <span data-ttu-id="8ccda-243">**가격 책정** 열에 선택한 리소스 역할에 대한 가격을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-243">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="8ccda-244">프로젝트 팀 양식</span><span class="sxs-lookup"><span data-stu-id="8ccda-244">Form a project team</span></span>
<span data-ttu-id="8ccda-245">프로젝트에서 이전에 설정한 역할을 사용하려면 프로젝트 관리자가 역할을 프로젝트와 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-245">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="8ccda-246">프로젝트에 여러 역할을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-246">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="8ccda-247">혼동을 방지하기 위해 이러한 역할은 예약 중에 자동으로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-247">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="8ccda-248">예를 들어 프로젝트 관리자에게 세 명의 소프트웨어 엔지니어가 필요한 경우 **소프트웨어 엔지니어 1**, **소프트웨어 엔지니어 2** 및 **소프트웨어 엔지니어 3** 레이블이 자동으로 생성되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-248">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="8ccda-249">역할에 대해 이전에 역할 특성을 설정한 경우 리소스 검색 중에 필터로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-249">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="8ccda-250">검색을 더 세분화하기 위해 필요에 따라 추가 특성을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-250">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="8ccda-251">리소스 가용성을 더 잘 볼 수 있도록 보기 설정을 사용자 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-251">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="8ccda-252">시간별, 일별, 주별, 월별, 분기별 및 연간 가용성을 표시하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-252">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="8ccda-253">리소스의 사용 가능한 용량과 남은 용량을 표시하는 옵션도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-253">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="8ccda-254">이 옵션은 활동 또는 리소스 가용성에 대해 사용 가능한 시간을 추정할 때 시간 관리에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-254">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="8ccda-255">프로젝트 관리자는 페이지에서 역할을 선택한 다음 요구 사항에 맞는 사용 가능한 리소스가 있는 경우 역할을 수행할 리소스를 예약하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-255">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="8ccda-256">계획 단계의 이 시점에서 리소스를 예약할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-256">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="8ccda-257">WBS를 만들 때 역할을 프로젝트의 인력 리소스로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-257">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="8ccda-258">역할이 WBS에서 인력이 있는 리소스로 대체되면 리소스 설정에서 프로젝트 팀 목록 및 일정을 자동으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-258">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="8ccda-259">[![역할과 실제 리소스가 모두 포함된 프로젝트 팀 목록](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-259">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="8ccda-260">프로젝트 관리자는 **남은 용량**, **전체 용량**, **용량 비율** 및 **시간 지정** 같이 프로젝트 리소스를 예약할 수 있는 다양한 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-260">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="8ccda-261">이러한 예약 옵션은 리소스 할당이 변경되는 경우 언제든지 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-261">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="8ccda-262">두 가지 유형의 예약이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-262">Two types of booking are supported:</span></span>

- <span data-ttu-id="8ccda-263">**확정 예약** – 리소스 예약이 승인되고 지정된 기간 동안 참여에 대해 작동하도록 확인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-263">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="8ccda-264">**가예약** – 리소스 예약은 지정된 기간 동안 참여에 대해 작동하도록 잠정적으로 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-264">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="8ccda-265">다음 절차는 프로젝트 팀을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-265">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="8ccda-266">프로젝트 팀 만들기</span><span class="sxs-lookup"><span data-stu-id="8ccda-266">Create a project team</span></span>

1. <span data-ttu-id="8ccda-267">**모든 프로젝트** 목록 페이지에서 프로젝트를 선택한 다음 **편집**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-267">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="8ccda-268">**프로젝트 팀 및 일정** 탭의 **종료 날짜 예약** 필드에 예약 시작 날짜에 1개월을 더한 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-268">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="8ccda-269">예를 들어 예약 시작 날짜가 2017년 6월 24일(24/06/2017)이면 **24/06/2017**을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-269">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="8ccda-270">**추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-270">Select **Add**.</span></span>
4. <span data-ttu-id="8ccda-271">**프로젝트에 역할 추가** 창의 **역할**필드에서 **수석 프로젝트 관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-271">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="8ccda-272">**필수 역량**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-272">Select **Required competencies**.</span></span>
6. <span data-ttu-id="8ccda-273">**특성 선택** 페이지에서 이전에 수석 프로젝트 관리자 역할에 대해 설정한 특성이 기본적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-273">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="8ccda-274">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-274">Select **OK**.</span></span>
7. <span data-ttu-id="8ccda-275">**프로젝트에 역할 추가** 페이지의 **리소스 수** 필드에 **1**을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-275">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="8ccda-276">**리소스** 필드에서 조회는 필요한 역량이 있는 모든 리소스를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-276">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="8ccda-277">**Daniel Goldschmidt**를 선택한 다음 **만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-277">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="8ccda-278">**프로젝트** 페이지에서 **추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-278">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="8ccda-279">**프로젝트에 역할 추가** 창의 **역할**필드에서 **팀 구성원**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-279">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="8ccda-280">**리소스 수** 필드에 **5**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-280">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="8ccda-281">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-281">Select **Create**.</span></span>
12. <span data-ttu-id="8ccda-282">**프로젝트** 페이지에서 **리소스 이행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-282">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="8ccda-283">리소스 생산 능력 동기화</span><span class="sxs-lookup"><span data-stu-id="8ccda-283">Resource capacity synchronization</span></span>
<span data-ttu-id="8ccda-284">리소스 동기화를 위한 프로세스는 일정 및 기본 일정에 대한 정보가 프로젝트 리소스 스케줄링으로 흘러 들어가는 것을 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-284">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="8ccda-285">일정이 변경되면 프로세스가 프로젝트 리소스 일정에 필요한 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-285">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="8ccda-286">일정의 리소스 정보가 미리 동기화되기 때문에 프로세스는 성능 향상에도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-286">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="8ccda-287">따라서 리소스 예약 정보에 대한 업데이트가 더 빨리 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-287">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="8ccda-288">프로세스를 한 번에 하나씩이 아닌 일괄 처리로 예약하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-288">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="8ccda-289">그렇지 않으면 정보가 마지막으로 동기화된 포함 날짜를 잊어 버릴 위험이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-289">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="8ccda-290">포함 날짜를 사용하지 않으면 날짜 동기화 중에 간격이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-290">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![일정 동기화](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="8ccda-292">리소스 생산 능력 롤업 동기화</span><span class="sxs-lookup"><span data-stu-id="8ccda-292">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="8ccda-293">동기화 프로세스는 모든 리소스 일정 정보를 동기화하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-293">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="8ccda-294">이 정보에는 프로젝트의 리소스 일정 생산 능력 테이블 변경 사항에 대한 기본 일정 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-294">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="8ccda-295">프로젝트에 새 리소스가 추가된 경우 동기화를 통해 업데이트된 일정 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-295">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="8ccda-296">이 동기화는 언제든지 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-296">This synchronization can be done at any time.</span></span>

<span data-ttu-id="8ccda-297">일괄 처리를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-297">We recommend that you use a batch.</span></span> <span data-ttu-id="8ccda-298">이 옵션은 용량 예약 동기화 중에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-298">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="8ccda-299">**프로젝트 관리 및 회계** &gt; **주기적** &gt; **용량 동기화** &gt; **리소스 용량 롤업 동기화**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-299">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="8ccda-300">다음 표에서 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-300">Set the options in the following table.</span></span>

    | <span data-ttu-id="8ccda-301">옵션</span><span class="sxs-lookup"><span data-stu-id="8ccda-301">Option</span></span>      | <span data-ttu-id="8ccda-302">설명</span><span class="sxs-lookup"><span data-stu-id="8ccda-302">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="8ccda-303">기간 코드</span><span class="sxs-lookup"><span data-stu-id="8ccda-303">Period code</span></span> | <span data-ttu-id="8ccda-304">선택적으로 총계정 원장 날짜 간격 코드를 선택하여 리소스 용량 롤업을 위한 동기화 프로세스의 시작 및 종료 날짜를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-304">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8ccda-305">시작 날짜</span><span class="sxs-lookup"><span data-stu-id="8ccda-305">Start date</span></span>  | <span data-ttu-id="8ccda-306">리소스 용량 롤업을 위한 동기화 프로세스의 시작 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-306">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8ccda-307">종료 날짜</span><span class="sxs-lookup"><span data-stu-id="8ccda-307">End date</span></span>    | <span data-ttu-id="8ccda-308">리소스 용량 롤업을 위한 동기화 프로세스의 종료 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-308">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="8ccda-309">[![동기화 프로세스](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-309">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="8ccda-310">WBS 템플릿에서 역할 설정</span><span class="sxs-lookup"><span data-stu-id="8ccda-310">Set up roles on WBS templates</span></span>
<span data-ttu-id="8ccda-311">프로젝트 관리자는 새 프로젝트용 WBS를 만들 때 적용할 수 있는 WBS 템플릿을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-311">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="8ccda-312">프로젝트 관리자는 템플릿을 만들 때 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-312">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="8ccda-313">다음 절차에 따라 WBS 템플릿에 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-313">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="8ccda-314">**프로젝트 관리 및 회계** &gt; **설정** &gt; **프로젝트** &gt; **작업 분할 구조 템플릿**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-314">Select **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="8ccda-315">선택한 WBS 템플릿에 대한 **세부 정보**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-315">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="8ccda-316">목록에서 작업을 선택한 다음 **역할** 필드에서 작업에 할당할 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-316">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="8ccda-317">WBS에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="8ccda-317">Work with a WBS</span></span>

<span data-ttu-id="8ccda-318">새 WBS를 만들거나 기존 WBS 템플릿에서 WBS를 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-318">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="8ccda-319">프로젝트 관리자는 WBS의 새 작업에 역할을 할당하여 리소스를 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-319">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="8ccda-320">리소스를 획득한 후 또는 작업을 수행할 확인된 리소스가 식별된 후 역할을 교체할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-320">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="8ccda-321">이러한 유연성 덕분에 프로젝트 관리자는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-321">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="8ccda-322">WBS 작업 패키지에 필요한 리소스 수를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-322">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="8ccda-323">프로젝트 비용을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-323">Estimate project costs.</span></span>
- <span data-ttu-id="8ccda-324">예비 예산을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-324">Determine a preliminary budget.</span></span>
- <span data-ttu-id="8ccda-325">역할 및 리소스를 기반으로 활동 기간을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-325">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="8ccda-326">사용 가능한 프로젝트 정보를 기반으로 몇 가지 프로젝트 관리 계획을 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-326">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="8ccda-327">리소싱 기능을 더 잘 사용하기 위해 WBS에 추가 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-327">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ccda-328">옵션</span><span class="sxs-lookup"><span data-stu-id="8ccda-328">Option</span></span></th>
<th><span data-ttu-id="8ccda-329">설명</span><span class="sxs-lookup"><span data-stu-id="8ccda-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ccda-330">리소스 할당</span><span class="sxs-lookup"><span data-stu-id="8ccda-330">Resource assignments</span></span></td>
<td><span data-ttu-id="8ccda-331">WBS의 작업에 할당된 리소스, 날짜, 시간 및 예약 유형을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-331">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ccda-332">팀 자동 생성</span><span class="sxs-lookup"><span data-stu-id="8ccda-332">Auto generate team</span></span></td>
<td><span data-ttu-id="8ccda-333">작업과 관련된 역할을 사용하여 계획된 리소스를 자동으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-333">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="8ccda-334">Finance는 역할에 기반한 다중 기준 의사 결정 분석을 사용하여 계획된 리소스를 자동으로 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-334">Finance automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="8ccda-335">WBS의 작업에 대한 역할 및 노력(시간)을 설정한 후 구조가 해제된 후 <strong>팀 자동 생성</strong>을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-335">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="8ccda-336">필요한 수의 계획된 리소스가 WBS 및 <strong>프로젝트 및 팀 일정</strong>탭에 추가됩니다 .</span><span class="sxs-lookup"><span data-stu-id="8ccda-336">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ccda-337">리소스(드롭다운 목록)</span><span class="sxs-lookup"><span data-stu-id="8ccda-337">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="8ccda-338"><strong>리소스 할당 시작</strong> 페이지에서 지정된 기간에 따라 확정 예약 또는 가예약할 리소스를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-338">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="8ccda-339">보기 설정을 조정하여 리소스 활동 기간을 보고 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-339">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="8ccda-340">다음 옵션을 사용하여 작업 패키지 수준에서 리소스를 선택하고 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-340">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="8ccda-341"><strong>수락</strong> – 작업에 할당된 자원의 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-341"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="8ccda-342"><strong>취소</strong> – 작업에 할당된 자원의 변경 사항을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-342"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="8ccda-343"><strong>자동 할당</strong> – 일치하는 역할이 있는 사용 가능한 인력이 있는 리소스가 자동으로 선택되고 선택한 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-343"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="8ccda-344">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-344">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="8ccda-345">**계획** &gt; **활동** &gt; **작업 분할 구조**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-345">Select **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
3. <span data-ttu-id="8ccda-346">**신규**를 선택하여 다음 수준 1 활동을 WBS에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-346">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="8ccda-347">시작</span><span class="sxs-lookup"><span data-stu-id="8ccda-347">Initiating</span></span>
    - <span data-ttu-id="8ccda-348">계획</span><span class="sxs-lookup"><span data-stu-id="8ccda-348">Planning</span></span>
    - <span data-ttu-id="8ccda-349">실행 중</span><span class="sxs-lookup"><span data-stu-id="8ccda-349">Executing</span></span>
    - <span data-ttu-id="8ccda-350">모니터링 및 제어</span><span class="sxs-lookup"><span data-stu-id="8ccda-350">Monitoring and Control</span></span>
    - <span data-ttu-id="8ccda-351">종료</span><span class="sxs-lookup"><span data-stu-id="8ccda-351">Close</span></span>

4. <span data-ttu-id="8ccda-352">다음 그림과 같이 날짜와 노력(시간)을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-352">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="8ccda-353">[![날짜와 노력 설정](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ccda-353">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="8ccda-354">**시작** 작업 줄을 선택한 다음 **역할** 필드에서 **수석 프로젝트 관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-354">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="8ccda-355">**게시**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-355">Select **Publish**.</span></span>
7. <span data-ttu-id="8ccda-356">같은 줄의 **리소스** 필드에서 **Daniel Goldschmidt**를 선택한 다음 **수락**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-356">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="8ccda-357">**계획** 작업 줄을 선택한 다음 **역할** 필드에서 **비즈니스 분석가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-357">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="8ccda-358">**게시**를 선택한 다음 **팀 자동 생성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-358">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="8ccda-359">표시되는 메시지 상자에서 **예**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-359">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="8ccda-360">**리소스** 필드에서 값이 **비즈니스 분석가 1**인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-360">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="8ccda-361">**비즈니스 분석가 1** 리소스의 경우 조회를 열고 **리소스 할당 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-361">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="8ccda-362">그런 다음 작업에 대한 작업자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-362">Then select a worker for the task.</span></span>
13. <span data-ttu-id="8ccda-363">**소프트 할당** &gt; **전체 용량**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-363">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="8ccda-364">리소스 수가 1로 남아 있으므로 지정된 리소스가 이제 2라는 경고를 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-364">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="8ccda-365">**작업 분할 구조** 페이지에서 WBS에서 리소스 할당을 확인한 다음 **저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-365">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="8ccda-366">계획된 리소스에 대한 리소스 이행</span><span class="sxs-lookup"><span data-stu-id="8ccda-366">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="8ccda-367">프로젝트 관리자는 프로젝트에 필요한 리소스 역할을 계획할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-367">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="8ccda-368">리소스 관리자는 이러한 계획된 리소스를 **리소스 이행** 페이지에서 요청으로 확인하고 실제 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-368">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="8ccda-369">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-369">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="8ccda-370">**프로젝트**를 선택한 후 **편집**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-370">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="8ccda-371">**프로젝트 팀 및 일정** 탭에서 **추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-371">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="8ccda-372">**역할 추가** 대화 상자에서 **소프트웨어 개발자** 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-372">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="8ccda-373">**만들기**를 선택한 다음 프로젝트 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-373">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="8ccda-374">**리소스 이행** 페이지에서 **XYZ 업그레이드 프로젝트 2단계** 프로젝트에 대해 **소프트웨어 개발자 1**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-374">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="8ccda-375">작업자를 선택한 후 **할당**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-375">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="8ccda-376">**소프트웨어 개발자 1** 줄이 **XYZ 업그레이드 프로젝트 2단계** 프로젝트에 대해 제거되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-376">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="8ccda-377">**프로젝트 팀 및 일정** 탭의 **XYZ 업그레이드 2단계** 프로젝트에 대해 이전 단계에서 선택한 작업자가 **소프트웨어 개발자**로 추가되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-377">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="8ccda-378">프로젝트 리소스에 대한 요청</span><span class="sxs-lookup"><span data-stu-id="8ccda-378">Requests for project resources</span></span>
<span data-ttu-id="8ccda-379">프로젝트 리소스 예약 기능을 사용하면 리소스 관리자가 참여 또는 프로젝트에 직원 리소스를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-379">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="8ccda-380">이 기능을 사용하려면 다음 작업을 완료하거나 완료되었는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ccda-380">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="8ccda-381">번호 순서를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-381">Set up number sequences.</span></span>
- <span data-ttu-id="8ccda-382">프로젝트 관리 및 회계 워크플로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-382">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="8ccda-383">리소스 요청 워크플로를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-383">Enable resource request workflows.</span></span>

<span data-ttu-id="8ccda-384">이전 작업이 완료된 후 필요에 따라 다음 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-384">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="8ccda-385">확정 예약 인력이 있는 리소스에서 리소스 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-385">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="8ccda-386">리소스 요청을 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-386">Monitor resource requests.</span></span>
- <span data-ttu-id="8ccda-387">리소스 요청을 이행합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-387">Fulfill resource requests.</span></span>
- <span data-ttu-id="8ccda-388">WBS에 인력이 있는 리소스를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-388">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="8ccda-389">직원이 있는 리소스를 요청하지 않고 프로젝트에 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-389">Book resources to a project without having a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="8ccda-390">프로젝트 팀 모니터링</span><span class="sxs-lookup"><span data-stu-id="8ccda-390">Monitor project teams</span></span>
1. <span data-ttu-id="8ccda-391">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트에 대한 **프로젝트 ID** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccda-391">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="8ccda-392">**프로젝트 팀 및 일정** 빠른 탭에서 나열된 프로젝트 리소스가 올바른지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ccda-392">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
