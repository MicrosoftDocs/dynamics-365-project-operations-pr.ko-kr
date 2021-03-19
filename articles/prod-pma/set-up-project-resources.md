---
title: 프로젝트 리소스 설정
description: 이 항목은 프로젝트 리소스를 설정 또는 요청하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
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
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288747"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="88ec3-103">프로젝트 리소스 설정</span><span class="sxs-lookup"><span data-stu-id="88ec3-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88ec3-104">일정을 설정하고 이를 직원 또는 근로자와 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="88ec3-105">일정은 프로젝트와 프로젝트를 위해 예약된 자원의 작업 시간을 예약하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="88ec3-106">일정 설정 중에 프로젝트 관리자는 리소스 최적화의 일부로 리소스 평준화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="88ec3-107">일정 예약에 따라 리소스에 제한을 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="88ec3-108">**일정** 페이지에서 일정을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="88ec3-109">작업자를 프로젝트 리소스로 설정할 때 리소스를 설정하려는 회사에서 근무하는 작업자 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="88ec3-110">또는 조직의 다른 회사에서 근무하는 근로자를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="88ec3-111">이러한 작업자를 회사 간 리소스라고합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="88ec3-112">다음 절차에서는 회사에서 작업자를 프로젝트 리소스로 설정하는 방법과 회사 간 프로젝트 리소스를 설정하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="88ec3-113">작업자를 프로젝트 리소스로 설정</span><span class="sxs-lookup"><span data-stu-id="88ec3-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="88ec3-114">**작업자** 페이지의 **작업자** 목록에서 프로젝트 리소스로 추가할 작업자를 선택하고 작업자 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="88ec3-115">작업 창에서 **프로젝트** &gt; **설정** &gt; **프로젝트 설정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="88ec3-116">일정을 선택한 다음 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="88ec3-117">리소스에 대한 기본 프로젝트를 사전 할당 유형으로 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="88ec3-118">사전 할당은 리소스 관리자 또는 프로젝트 관리자가 리소스가 미리 작업할 프로젝트를 알고 있을 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="88ec3-119">사전 할당은 프로젝트 후원자 또는 고객의 요청을 기반으로 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="88ec3-120">프로젝트를 사전 할당하려면 **프로젝트 할당** 페이지의 **프로젝트** 탭에 있는 **남은 프로젝트** 목록에서 적절한 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="88ec3-121">회사 간 리소스 설정</span><span class="sxs-lookup"><span data-stu-id="88ec3-121">Set up an intercompany resource</span></span>

<span data-ttu-id="88ec3-122">작업자를 회사 간 리소스로 설정하는 경우 대출 회사와 차용 회사 모두에서 설정을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="88ec3-123">대출 회사에서</span><span class="sxs-lookup"><span data-stu-id="88ec3-123">In the lending company</span></span>

1. <span data-ttu-id="88ec3-124">Finance에서 대출 회사가 선택되었는지 확인한 다음 이전 섹션인 "작업자를 프로젝트 리소스로 설정"의 절차를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="88ec3-125">**회사 간 회계** 페이지에서 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="88ec3-126">**법인 ID** 필드에서 대출 회사를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="88ec3-127">나머지 필드를 적절히 입력한 다음, **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="88ec3-128">**이전 가격** 페이지에서 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="88ec3-129">**차용 법인** 필드에서 적절한 회사를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="88ec3-130">이 섹션의 시작 부분에서 생성한 리소스만 차용 회사에 빌려주려면 **리소스** 필드에서 생성한 리소스의 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="88ec3-131">대출 회사의 모든 리소스를 차용 회사가 사용할 수 있도록 하려면 **리소스** 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="88ec3-132">**프로젝트 관리 및 회계 매개 변수** 페이지의 **회사 간** 탭에서 **회사 간 리소스 일정 및 작업 표 사용** 옵션을 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="88ec3-133">차용 회사에서</span><span class="sxs-lookup"><span data-stu-id="88ec3-133">In the borrowing company</span></span>

- <span data-ttu-id="88ec3-134">**리소스 목록** 페이지의 검색 필터에 대출 회사에 대해 생성한 리소스의 이름을 입력하여 이름이 차용 회사의 리소스 목록에 포함되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="88ec3-135">프로젝트 리소스 요청</span><span class="sxs-lookup"><span data-stu-id="88ec3-135">Request project resources</span></span>
<span data-ttu-id="88ec3-136">프로젝트 리소스 예약 기능을 사용하면 리소스 관리자가 참여 또는 프로젝트에 직원 리소스를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="88ec3-137">이 기능을 사용하려면 다음 작업을 완료하거나 완료되었는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="88ec3-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="88ec3-138">번호 순서를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-138">Set up number sequences.</span></span>
- <span data-ttu-id="88ec3-139">프로젝트 관리 및 회계 워크플로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="88ec3-140">리소스 요청 워크플로를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-140">Enable resource request workflows.</span></span>

<span data-ttu-id="88ec3-141">이전 작업이 완료된 후 필요에 따라 다음 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="88ec3-142">확정 예약 인력이 있는 리소스에서 리소스 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="88ec3-143">리소스 요청을 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-143">Monitor resource requests.</span></span>
- <span data-ttu-id="88ec3-144">리소스 요청을 이행합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="88ec3-145">WBS에 인력이 있는 리소스를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="88ec3-146">직원이 있는 리소스를 요청하지 않고 프로젝트에 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec3-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]