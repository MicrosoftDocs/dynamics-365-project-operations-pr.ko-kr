---
title: 프로젝트 팀 만들기
description: 이 항목은 프로젝트 팀을 생성하고 관리하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270866"
---
# <a name="create-a-project-team"></a><span data-ttu-id="d0ac1-103">프로젝트 팀 만들기</span><span class="sxs-lookup"><span data-stu-id="d0ac1-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0ac1-104">프로젝트에서 이전에 설정한 역할을 사용하려면 프로젝트 관리자가 역할을 프로젝트와 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="d0ac1-105">프로젝트에 여러 역할을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="d0ac1-106">혼동을 방지하기 위해 이러한 역할은 예약 중에 자동으로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="d0ac1-107">예를 들어 프로젝트 관리자에게 세 명의 소프트웨어 엔지니어가 필요한 경우 **소프트웨어 엔지니어 1**, **소프트웨어 엔지니어 2** 및 **소프트웨어 엔지니어 3** 레이블이 자동으로 생성되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="d0ac1-108">역할에 대해 이전에 역할 특성을 설정한 경우 리소스 검색 중에 필터로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="d0ac1-109">검색을 더 세분화하기 위해 필요에 따라 추가 특성을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="d0ac1-110">리소스 가용성을 더 잘 볼 수 있도록 보기 설정을 사용자 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="d0ac1-111">시간별, 일별, 주별, 월별, 분기별 및 연간 가용성을 표시하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="d0ac1-112">리소스의 사용 가능한 용량과 남은 용량을 표시하는 옵션도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="d0ac1-113">이 옵션은 활동 또는 리소스 가용성에 대해 사용 가능한 시간을 추정할 때 시간 관리에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="d0ac1-114">프로젝트 관리자는 페이지에서 역할을 선택한 다음 요구 사항에 맞는 사용 가능한 리소스가 있는 경우 역할을 수행할 리소스를 예약하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="d0ac1-115">계획 단계의 이 시점에서 리소스를 예약할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="d0ac1-116">WBS를 만들 때 역할을 프로젝트의 인력 리소스로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="d0ac1-117">역할이 WBS에서 인력이 있는 리소스로 대체되면 리소스 설정에서 프로젝트 팀 목록 및 일정을 자동으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="d0ac1-118">[![역할과 실제 리소스가 모두 포함된 프로젝트 팀 목록](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="d0ac1-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="d0ac1-119">프로젝트 관리자는 **남은 용량**, **전체 용량**, **용량 비율** 및 **시간 지정** 같이 프로젝트 리소스를 예약할 수 있는 다양한 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="d0ac1-120">이러한 예약 옵션은 리소스 할당이 변경되는 경우 언제든지 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="d0ac1-121">두 가지 유형의 예약이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="d0ac1-122">**확정 예약** – 리소스 예약이 승인되고 지정된 기간 동안 참여에 대해 작동하도록 확인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="d0ac1-123">**가예약** – 리소스 예약은 지정된 기간 동안 참여에 대해 작동하도록 잠정적으로 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="d0ac1-124">다음 절차는 프로젝트 팀을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="d0ac1-125">프로젝트 팀 만들기</span><span class="sxs-lookup"><span data-stu-id="d0ac1-125">Create a project team</span></span>

1. <span data-ttu-id="d0ac1-126">**모든 프로젝트** 목록 페이지에서 프로젝트를 선택한 다음 **편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="d0ac1-127">**프로젝트 팀 및 일정** 탭의 **종료 날짜 예약** 필드에 예약 시작 날짜에 1개월을 더한 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="d0ac1-128">예를 들어 예약 시작 날짜가 2017년 6월 24일(24/06/2017)이면 **24/06/2017** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="d0ac1-129">**추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-129">Select **Add**.</span></span>
4. <span data-ttu-id="d0ac1-130">**프로젝트에 역할 추가** 창의 **역할** 필드에서 **수석 프로젝트 관리자** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="d0ac1-131">**필수 역량** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="d0ac1-132">**특성 선택** 페이지에서 이전에 수석 프로젝트 관리자 역할에 대해 설정한 특성이 기본적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="d0ac1-133">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-133">Select **OK**.</span></span>
7. <span data-ttu-id="d0ac1-134">**프로젝트에 역할 추가** 페이지의 **리소스 수** 필드에 **1** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="d0ac1-135">**리소스** 필드에서 조회는 필요한 역량이 있는 모든 리소스를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="d0ac1-136">**Daniel Goldschmidt** 를 선택한 다음 **만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="d0ac1-137">**프로젝트** 페이지에서 **추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="d0ac1-138">**프로젝트에 역할 추가** 창의 **역할** 필드에서 **팀 구성원** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="d0ac1-139">**리소스 수** 필드에 **5** 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="d0ac1-140">**만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-140">Select **Create**.</span></span>
12. <span data-ttu-id="d0ac1-141">**프로젝트** 페이지에서 **리소스 이행** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="d0ac1-142">프로젝트 팀 모니터링</span><span class="sxs-lookup"><span data-stu-id="d0ac1-142">Monitor project teams</span></span>
1. <span data-ttu-id="d0ac1-143">**모든 프로젝트** 페이지에서 **XYZ 업그레이드 2단계** 프로젝트에 대한 **프로젝트 ID** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="d0ac1-144">**프로젝트 팀 및 일정** 빠른 탭에서 나열된 프로젝트 리소스가 올바른지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0ac1-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]