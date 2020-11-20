---
title: 제안된 리소스 검토
description: 이 항목은 프로젝트 리소스를 제안하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401181"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="b13c4-103">제안된 리소스 검토</span><span class="sxs-lookup"><span data-stu-id="b13c4-103">Review proposed resources</span></span>

<span data-ttu-id="b13c4-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="b13c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b13c4-105">리소스 관리자는 리소스 요청을 사용하여 프로젝트 관리자에게 리소스를 제안할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="b13c4-106">요청 그리드 또는 요청 자체에서 **리소스 찾기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="b13c4-107">**스케줄 도우미** 페이지에서 리소스를 선택한 다음 **리소스 예약 만들기** 창의 **예약 상태** 필드에서 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="b13c4-108">다음과 같은 상태 업데이트가 발생합니다:</span><span class="sxs-lookup"><span data-stu-id="b13c4-108">The following status updates occur:</span></span>

- <span data-ttu-id="b13c4-109">**스케줄 도우미** 페이지에서 상태 표시등이 업데이트되어 예약이 확정 예약이 아닌 제안된 상태임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="b13c4-110">리소스 요청에서 상태가 **검토 필요** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="b13c4-111">프로젝트의 **팀** 탭에서 일반 팀원의 **요청 상태** 값이 **검토 필요** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="b13c4-112">프로젝트 관리자는 제안을 수락하거나 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="b13c4-113">리소스 관리자가 리소스 요청을 처리할 때 다음 방법 중 하나를 사용할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="b13c4-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="b13c4-114">요구되는 시간을 충족할 수 있는 단일 리소스가 없는 경우 수요를 충족하기 위해 여러 리소스를 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="b13c4-115">그런 다음 제안된 시간은 요구되는 시간을 충족할 수 있는 여러 리소스로 분할됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="b13c4-116">이 시나리오에서는 시간이 겹칠 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="b13c4-117">요구되는 것보다 적은 리소스를 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="b13c4-118">이 시나리오에서 제안된 리소스 능력은 요청자가 지정한 요구되는 시간보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="b13c4-119">따라서 요청자가 제안된 리소스를 수락하면 나머지 수요를 포착하기 위해 충족되지 않은 리소스 요건이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="b13c4-120">작업을 완료하기 위해 사용할 수 있는 단일 리소스가 없는 경우 수요를 충족하기 위해 여러 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="b13c4-121">요구되는 것보다 적은 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-121">Book fewer resources than are required.</span></span> <span data-ttu-id="b13c4-122">이 시나리오에서는 예약된 시간이 요구되는 시간보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="b13c4-123">이 시스템은 예약 대신 리소스를 제안하도록 안내하므로 요청자가 남은 수요를 확인하고 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="b13c4-124">사용 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="b13c4-124">Resource availability</span></span>

<span data-ttu-id="b13c4-125">리소스 관리자는 리소스의 가용성을 확인하고 예약을 업데이트할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="b13c4-126">경우에 따라 공식적인 요청(리소스 요청)이 없지만 리소스 관리자는 이메일, 전화 통화 또는 인스턴트 메시지와 같은 채널을 통해 제공되는 계획되지 않은 수요에 대응해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="b13c4-127">리소스 관리자는 스케줄 보드를 사용하여 리소스 및 예약을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="b13c4-128">리소스 작업 시간은 리소스의 가용성을 계산하기 위한 기준으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="b13c4-129">리소스 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="b13c4-130">스케줄 게시판은 색상과 음영을 사용하여 예약, 이용 가능 여부 및 초과 예약 및 예약 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="b13c4-131">스케줄 보드 설정의 설정값을 사용하면 범례를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="b13c4-132">스케줄 게시판의 개별 예약 가능 리소스 옆에 오른쪽을 가리키는 화살표가 나타나면 리소스를 확장하여 리소스가 예약된 작업의 내역을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="b13c4-133">Dynamics 365 Project Operations는 Universal Resource Scheduling 엔진을 사용하기 때문에, Dynamics 365 Field Service도 설치된 경우, 프로젝트, 작업 명령 및 기타 귀하가 스케줄링을 확장한 엔터티를 위한 리소스 예약 내역을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="b13c4-134">개별 리소스에 대한 자세한 내용을 보려면 마우스 오른쪽 버튼을 클릭하여 리소스 카드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b13c4-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

