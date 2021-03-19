---
title: 프로젝트 리소스 제안
description: 이 항목은 프로젝트 리소스 제안에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283016"
---
# <a name="propose-project-resources"></a><span data-ttu-id="23537-103">프로젝트 리소스 제안</span><span class="sxs-lookup"><span data-stu-id="23537-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="23537-104">리소스 관리자는 리소스 요청을 사용하여 프로젝트 관리자에게 리소스를 제안할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="23537-105">요청 그리드 또는 요청 자체에서 **리소스 찾기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="23537-106">**스케줄 도우미** 페이지에서 리소스를 선택한 다음 **리소스 예약 만들기** 창의 **예약 상태** 필드에서 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![선택된 제안된 리소스](media/Resource-Management-image62.png)

<span data-ttu-id="23537-108">다음과 같은 상태 업데이트가 발생합니다:</span><span class="sxs-lookup"><span data-stu-id="23537-108">The following status updates occur:</span></span>

- <span data-ttu-id="23537-109">**스케줄 도우미** 페이지에서 상태 표시등이 업데이트되어 예약이 확정 예약이 아닌 제안된 상태임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23537-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![스케줄 도우미 페이지에서 제안된 예약에 대한 상태 표시등](media/Resource-Management-image63.png)

- <span data-ttu-id="23537-111">리소스 요청에서 상태가 **검토 필요** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![검토 필요로 변경된 리소스 요청 상태](media/Resource-Management-image64.png)

- <span data-ttu-id="23537-113">프로젝트의 **팀** 탭에서 일반 팀원의 **요청 상태** 값이 **검토 필요** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![팀 탭에서 일반 팀원의 요청 상태 값이 검토 필요로 변경됨](media/Resource-Management-image48.png)

<span data-ttu-id="23537-115">프로젝트 관리자는 제안을 수락하거나 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="23537-116">리소스 관리자가 리소스 요청을 처리할 때 다음 방법 중 하나를 사용할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="23537-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="23537-117">요구되는 시간을 충족할 수 있는 단일 리소스가 없는 경우 수요를 충족하기 위해 여러 리소스를 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="23537-118">그런 다음 제안된 시간은 요구되는 시간을 충족할 수 있는 여러 리소스로 분할됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="23537-119">이 시나리오에서는 시간이 겹칠 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="23537-120">요구되는 것보다 적은 리소스를 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="23537-121">이 시나리오에서 제안된 리소스 능력은 요청자가 지정한 요구되는 시간보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="23537-122">따라서 요청자가 제안된 리소스를 수락하면 나머지 수요를 포착하기 위해 충족되지 않은 리소스 요건이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="23537-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="23537-123">작업을 완료하기 위해 사용할 수 있는 단일 리소스가 없는 경우 수요를 충족하기 위해 여러 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="23537-124">요구되는 것보다 적은 리소스를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-124">Book fewer resources than are required.</span></span> <span data-ttu-id="23537-125">이 시나리오에서는 예약된 시간이 요구되는 시간보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="23537-126">이 시스템은 예약 대신 리소스를 제안하도록 안내하므로 요청자가 남은 수요를 확인하고 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="23537-127">청구 가능 활용도</span><span class="sxs-lookup"><span data-stu-id="23537-127">Billable utilization</span></span>

<span data-ttu-id="23537-128">리소스는 목표 청구 가능 활용도를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="23537-129">이 목표 활용도는 리소스의 기본 역할에 대한 특성으로 정의되거나 개별 예약 가능 리소스의 레코드에 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="23537-130">활용도 계산은 승인된 시간 항목을 사용하여 리소스가 보고한 실제 시간을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="23537-131">활용도를 계산하는 데 다음 공식이 사용됩니다:</span><span class="sxs-lookup"><span data-stu-id="23537-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="23537-132">청구 가능 활용도 = 청구 가능 실제값 시간 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="23537-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="23537-133">청구 가능 활용도 = 청구 타입 ID가 있는 실제값 시간 = 비청구, 보완 또는 사용할 수 없음 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="23537-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="23537-134">내부 = 판매 계약이 없는 실제 시간 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="23537-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="23537-135">리소스 능력 = 리소스 작업 시간 – 업무 외 – 휴무일</span><span class="sxs-lookup"><span data-stu-id="23537-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="23537-136">**리소스** 창에서 **리소스 활용도** 보기를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![리소스 활용도 보기](media/Resource-Management-image65.png)

<span data-ttu-id="23537-138">그리드의 각 셀은 일, 주 또는 월과 같은 기간 동안 리소스의 청구 가능 활용도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23537-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="23537-139">셀을 컬러링하는 데 다음 공식이 사용됩니다:</span><span class="sxs-lookup"><span data-stu-id="23537-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="23537-140">**녹색:** 청구 가능 활용도 \>= 리소스 목표 활용도</span><span class="sxs-lookup"><span data-stu-id="23537-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="23537-141">**노랑:** 목표 활용도 – 20 \<= 청구 가능 활용도 \< 목표 활용도</span><span class="sxs-lookup"><span data-stu-id="23537-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="23537-142">**빨강:** 청구 가능 활용도 \< 목표 활용도 – 20</span><span class="sxs-lookup"><span data-stu-id="23537-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="23537-143">**리소스 활용도** 보기는 스케줄 보드를 기반으로 하므로 스케줄 보드의 필터링 기능을 사용하여 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="23537-144">그리드는 귀하가 역할 또는 개별 리소스에 대한 목표 활용도를 설정할 것을 요구합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="23537-145">이 설정을 하려면 **리소스** \> **리소스 역할** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="23537-146">또한 기본 역할은 각 예약 가능한 리소스에 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="23537-147">**리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="23537-148">**Project Service** 탭에서 리소스 역할이 정의되어 있는지, 리소스 역할에 대한 **기본값임** 이 **예** 로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="23537-149">**기본값임 = 아니오** 인 추가 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="23537-150">해당 역할의 목표 대비 리소스의 활용도를 평가하기 위해 **기본값임 = 예** 인 역할이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![설정된 기본 역할](media/Resource-Management-image67.png)

<span data-ttu-id="23537-152">**Project Service** 탭에서 리소스에 대한 개별 목표 활용도를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="23537-153">그런 다음 활용도 계산은 해당 목표 활용도를 사용하여 리소스의 기본 역할 목표 대신 리소스의 목표를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="23537-154">해당 리소스가 그리드에 표시되는 기간 동안 승인된 청구 가능 시간인 경우에만 리소스에 대한 활용도가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="23537-155">사용 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="23537-155">Resource availability</span></span>

<span data-ttu-id="23537-156">리소스 관리자는 리소스의 가용성을 확인하고 예약을 업데이트할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="23537-157">경우에 따라 공식적인 요청(리소스 요청)이 없지만 리소스 관리자는 이메일, 전화 통화 또는 인스턴트 메시지와 같은 채널을 통해 제공되는 계획되지 않은 수요에 대응해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="23537-158">리소스 관리자는 스케줄 보드를 사용하여 리소스 및 예약을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="23537-159">리소스 작업 시간은 리소스의 가용성을 계산하기 위한 기준으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="23537-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="23537-160">리소스 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-160">Resource bookings consume the capacity of the resources.</span></span>

![일정 게시판](media/Resource-Management-image68.png)

<span data-ttu-id="23537-162">스케줄 게시판은 색상과 음영을 사용하여 예약, 이용 가능 여부 및 초과 예약 및 예약 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="23537-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="23537-163">스케줄 보드 설정의 설정값을 사용하면 범례를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="23537-164">스케줄 게시판의 개별 예약 가능 리소스 옆에 오른쪽을 가리키는 화살표가 나타나면 리소스를 확장하여 리소스가 예약된 작업의 내역을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![스케줄 게시판에 펼쳐진 예약 가능한 리소스](media/Resource-Management-image69.png)

<span data-ttu-id="23537-166">Dynamics 365 Project Service Automation은 Universal Resource Scheduling 엔진을 사용하기 때문에, Dynamics 365 Field Service도 설치된 경우, 프로젝트, 작업 명령 및 기타 귀하가 스케줄링을 확장한 엔터티를 위한 리소스 예약 내역을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23537-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![프로젝트 및 작업 명령을 위한 리소스 예약에 대한 세부 정보](media/Resource-Management-image70.png)

<span data-ttu-id="23537-168">개별 리소스에 대한 자세한 내용을 보려면 마우스 오른쪽 버튼을 클릭하여 리소스 카드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="23537-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![리소스 카드](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]