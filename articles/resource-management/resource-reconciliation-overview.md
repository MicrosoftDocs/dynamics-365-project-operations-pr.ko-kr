---
title: 리소스 조정 개요
description: 이 항목은 프로젝트에 대한 리소스 예약 및 할당이 정렬되었는지 확인하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125726"
---
# <a name="resource-reconciliation-overview"></a><span data-ttu-id="e217d-103">리소스 조정 개요</span><span class="sxs-lookup"><span data-stu-id="e217d-103">Resource reconciliation overview</span></span>

<span data-ttu-id="e217d-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e217d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e217d-105">팀 구성원의 경우 예약 및 할당이 느슨하게 결합됩니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-105">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="e217d-106">즉, 리소스는 할당을 가질 수 있지만 예약은 없을 수도 있고, 예약을 할 수 있지만 할당은 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-106">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="e217d-107">예약과 할당은 정렬되는 것이 좋습니다. 그래야 리소스가 작업 할당을 수행할 수 있는 생산 능력이 이행됩니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-107">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="e217d-108">그러나 예약은 가용성을 기반으로 할 수 있으며 프로젝트가 계속됨에 따라 작업 타이밍이 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-108">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="e217d-109">따라서 예약과 할당의 느슨한 결합은 유연성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-109">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="e217d-110">**프로젝트** 양식의 **조정** 탭을 사용하면 프로젝트 관리자가 프로젝트 팀을 위한 팀원 예약과 배정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-110">The **Reconciliation** tab on the **Project** form lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

<span data-ttu-id="e217d-111">**조정** 탭은 각 팀 구성원에 대해 개별 작업 할당의 수준으로 내려가는 예약 및 할당도 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-111">The **Reconciliation** tab also shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="e217d-112">시간에는 셀에 수 개월~수 일의 기간을 나타내는 시간이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-112">Hours are displayed in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="e217d-113">탭에는 **총** 열과 함께 프로젝트의 전체 순합계도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-113">The tab also shows an overall net total for the project, together with a **Total** column.</span></span>

<span data-ttu-id="e217d-114">각 리소스에 대해 탭은 팀 구성원의 예약과 해당 팀원의 과업 할당 롤업 사이의 차이를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-114">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="e217d-115">이상적으로는 이 차이가 0(제로)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-115">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="e217d-116">즉, 리소스의 예약과 작업 할당 사이에 차이가 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-116">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="e217d-117">차이점은 두 가지 조건에 주의를 끌기 위한 색상과 그늘입니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-117">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="e217d-118">**예약 부족** – 리소스에 예약보다 많은 작업이 있을 때 예약 부족이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-118">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="e217d-119">이 능력은 예약되지 않았므로 프로젝트 관리자는 부족을 충당하기 위해 리소스 예약을 연장하여 이 조건을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-119">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="e217d-120">**초과 예약** – 리소스가 프로젝트에 예약되었지만 과업에 할당되지 않은 경우 초과 예약이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-120">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="e217d-121">작업 할당이 발생하기 전에 리소스가 프로젝트에 예약된 경우 이 조건을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-121">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="e217d-122">그러나 다른 경우에는 작업에 이 리소스를 할당할 계획이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-122">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="e217d-123">이러한 경우 프로젝트 관리자는 다른 프로젝트에 능력을 사용할 수 있도록 리소스의 예약을 취소하는 것을 고려해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-123">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="e217d-124">경우에 따라 일 수준(예: 월 수준)보다 높은 수준에서 시간을 볼 때 리소스에 대한 순 차이(예: 예약 = 할당)가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-124">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="e217d-125">그러나 주 수준의 시간을 살펴보면 첫 주에 0시간의 할당과 40시간의 예약을 볼 수 있지만, 두 번째 주에 40시간의 할당과 0시간의 예약이 있는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-125">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="e217d-126">전반적으로, 예약 및 할당은 조정되지만 1주일에서 다음 주까지 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-126">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="e217d-127">더 높은 시간 수준을 볼 때 **조정** 탭의 셀은 낮은 수준에 차이가 있음을 알리는 표시등이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-127">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="e217d-128">셀을 두 번 클릭하여 확대하고 차이를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-128">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="e217d-129">그런 다음 마우스 오른쪽 단추로 클릭하여 축소할 수 있습니다. 리소스를 선택한 다음 그리드 도구 모음에서 **다음 차이** 컨트롤을 사용하여 해당 리소스에 대한 예약과 할당 간의 다음 차이로 이동하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-129">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="e217d-130">그런 다음 **이전 차이** 컨트롤을 사용하여 다시 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-130">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="e217d-131">**설정** 에서 차이 표시기 및 탐색 동작을 해제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-131">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>


<span data-ttu-id="e217d-132">리소스에 대한 작업 할당이 있지만 예약이 없는 경우, **조정** 탭의 **프로젝트** 페이지에서 예약 부족을 선택한 다음 **예약 연장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-132">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="e217d-133">**예약 연장** 대화 상자가 나타나고 리소스 부족을 해결하는 데 필요한 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-133">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="e217d-134">또한 모든 프로젝트 또는 기타 예약 가능한 엔터티에서 리소스의 기존 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-134">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="e217d-135">리소스의 가용성에 관계없이 리소스에 대한 예약을 만들려면 **확인** 을 선택하면 초과 예약이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-135">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

<span data-ttu-id="e217d-136">그런 다음 프로젝트 관리자 또는 리소스 관리자는 일정 게시판을 사용해서 리소스가 생산 능력을 초과해서 예약된 모든 상황을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e217d-136">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>

