---
title: 프로젝트 예약
description: 이 항목은 프로젝트에 리소스를 예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c87b0c32ef081f601ed79c11687f008bb454dd45
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131081"
---
# <a name="book-to-a-project"></a><span data-ttu-id="e6847-103">프로젝트 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-103">Book to a project</span></span>

<span data-ttu-id="e6847-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e6847-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6847-105">프로젝트 관리자 또는 리소스 관리자가 일반 팀 구성원으로부터 특정 요구 사항을 정의하지 않고 프로젝트에 리소스를 할당해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="e6847-106">이는 세 가지 방법 중 하나로 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="e6847-107">팀 구성원 그리드에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-107">Book from the team member grid</span></span>
- <span data-ttu-id="e6847-108">일정 게시판에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-108">Book from the schedule board</span></span>
- <span data-ttu-id="e6847-109">**프로젝트** 양식에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="e6847-110">팀 구성원 그리드에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-110">Book from the team member grid</span></span>

<span data-ttu-id="e6847-111">조직이 하이브리드 리소스 할당 모드에서 운영 중인 경우 프로젝트 관리자는 다음 단계를 완료하여 프로젝트에 직접 리소스를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="e6847-112">프로젝트에서 팀 구성원 그리드로 이동하여 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="e6847-113">위치 이름과 리소스의 역할을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="e6847-114">사용 가능한 조회에서 예약 가능한 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="e6847-115">리소스를 선택한 후 다음 필드 정보를 정의하여 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="e6847-116">시작 날짜</span><span class="sxs-lookup"><span data-stu-id="e6847-116">Start date</span></span>
    - <span data-ttu-id="e6847-117">완료 날짜</span><span class="sxs-lookup"><span data-stu-id="e6847-117">Finish date</span></span>
    - <span data-ttu-id="e6847-118">할당 방법</span><span class="sxs-lookup"><span data-stu-id="e6847-118">Allocation method</span></span>
    - <span data-ttu-id="e6847-119">시간(해당되는 경우)</span><span class="sxs-lookup"><span data-stu-id="e6847-119">Hours, if applicable</span></span>
    - <span data-ttu-id="e6847-120">프로젝트 승인자</span><span class="sxs-lookup"><span data-stu-id="e6847-120">Project approver</span></span>

6. <span data-ttu-id="e6847-121">**저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="e6847-122">일정 게시판에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-122">Book from the schedule board</span></span>

<span data-ttu-id="e6847-123">리소스 관리자가 프로젝트에 직접 리소스를 예약해야 하는 경우 일정 게시판과 프로젝트 요구 사항을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="e6847-124">프로젝트 요구 사항은 항상 예약할 수 있는 리소스 요구 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="e6847-125">일정 게시판에서 프로젝트를 직접 예약하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6847-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="e6847-126">일정 게시판으로 이동하고 왼쪽 페이지에서 요구 사항에 대해 고려중인 리소스를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="e6847-127">하단 창에서 **프로젝트** 탭을 선택하여 프로젝트 요구 사항 목록을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="e6847-128">요구 사항을 리소스로 끌어오고 다음 정보를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="e6847-129">시작 날짜</span><span class="sxs-lookup"><span data-stu-id="e6847-129">Start date</span></span>
    - <span data-ttu-id="e6847-130">완료 날짜</span><span class="sxs-lookup"><span data-stu-id="e6847-130">Finish date</span></span>
    - <span data-ttu-id="e6847-131">예약 상태</span><span class="sxs-lookup"><span data-stu-id="e6847-131">Booking status</span></span>
    - <span data-ttu-id="e6847-132">예약 방법</span><span class="sxs-lookup"><span data-stu-id="e6847-132">Booking method</span></span>
    - <span data-ttu-id="e6847-133">기간</span><span class="sxs-lookup"><span data-stu-id="e6847-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="e6847-134">프로젝트 양식에서 예약</span><span class="sxs-lookup"><span data-stu-id="e6847-134">Book from the Project form</span></span>

<span data-ttu-id="e6847-135">프로젝트 관리자는 프로젝트에 리소스를 예약해야 할 수 있지만 리소스 이름보다는 기준만 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="e6847-136">일정 지원을 사용하여 리소스의 사용 가능한 속성을 기반으로 리소스를 찾으려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6847-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="e6847-137">프로젝트로 이동하고 **예약** 을 선택하여 일정 도우미를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="e6847-138">일정 도우미의 왼쪽에 있는 필터를 사용하여 기준을 좁히고 **검색** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="e6847-139">결과에 반환된 리소스를 기반으로 리소스를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="e6847-140">이 방법은 리소스에 대한 예약을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="e6847-141">대신 팀에 리소스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="e6847-142">팀 구성원이 프로젝트에 추가되면 프로젝트 관리자는 예약을 유지하거나 예약을 연장하여 필요한 예약을 리소스에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6847-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
