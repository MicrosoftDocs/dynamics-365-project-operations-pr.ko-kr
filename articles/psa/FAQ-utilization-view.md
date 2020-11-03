---
title: 청구 가능한 리소스 활용도 보기
description: 이 항목은 리소스 활용도 보기에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080074"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="59e2d-103">청구 가능한 리소스 활용도 보기</span><span class="sxs-lookup"><span data-stu-id="59e2d-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="59e2d-104">**Project Service 리소스 활용도** 페이지의 **활용도 보기** 는 예약 가능한 각 리소스에 대한 청구 가능한 활용도를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="59e2d-105">보기는 스케줄 게시판에 근거하므로 같은 기능 대부분을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![사용률 보기의 스크린샷](media/FAQ-utilization-1.png)
 

<span data-ttu-id="59e2d-107">청구 가능한 사용률 계산은 다음과 같이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="59e2d-108">청구 가능한 활용도 = (청구 가능한 실제값 시간) / (리소스 능력)</span><span class="sxs-lookup"><span data-stu-id="59e2d-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="59e2d-109">셀은 선택한 기간(일, 주 또는 월) 동안의 계산된 청구 가능한 활용도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="59e2d-110">각 셀의 색은 대상의 사용 가능한 사용률과 비교한 리소스에 대한 청구 가능한 사용률을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="59e2d-111">목표 활용도를 기본 역할 또는 개별 리소스 자체에서 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="59e2d-112">계산은 먼저 대상의 개인을 찾은 다음 리소스의 기본 역할을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="59e2d-113">리소스에 대한 목표 설정</span><span class="sxs-lookup"><span data-stu-id="59e2d-113">Set target on a resource</span></span>

1. <span data-ttu-id="59e2d-114">**리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="59e2d-115">리소스를 선택하여 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="59e2d-116">**Project Service** 탭에서 리소스의 목표 활용도를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Project Service 탭을 사용하여 대상 사용률을 설정하는 스크린샷](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="59e2d-118">역할에 대한 목표 활용도 설정</span><span class="sxs-lookup"><span data-stu-id="59e2d-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="59e2d-119">**리소스** \> **리소스 역할** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="59e2d-120">역할을 선택하여 레코드를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="59e2d-121">역할에 대한 대상 사용률을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-121">Set the target utilization for the role.</span></span>

> ![리소스 역할을 사용하여 대상 사용률을 설정하는 스크린샷](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="59e2d-123">리소스에 대한 청구 가능한 활용도 계산</span><span class="sxs-lookup"><span data-stu-id="59e2d-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="59e2d-124">리소스에 대한 청구 가능한 활용도를 계산하려면 일부 전제조건을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="59e2d-125">개별 리소스에 대한 기본 역할 설정</span><span class="sxs-lookup"><span data-stu-id="59e2d-125">Set default role for individual resource</span></span>

<span data-ttu-id="59e2d-126">먼저, 개별 리소스에 대한 또는 리소스 역할에 대한 목표 활용도를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="59e2d-127">대상에 대한 리소스 역할을 사용하는 경우 각 개별 리소스에 기본 역할이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="59e2d-128">이를 설정하려면 **리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="59e2d-129">리소스를 선택하고 레코드를 연 다음 **Project Service** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="59e2d-130">**리소스** 역할 그리드에서 리소스에 대한 역할이 하나 있고 **기본값임** 이 **예** 로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="59e2d-131">리소스 역할을 위한 대금 청구 타입 변경</span><span class="sxs-lookup"><span data-stu-id="59e2d-131">Change billing type for resource role</span></span>

<span data-ttu-id="59e2d-132">리소스 역할은 청구 타입이 **청구 가능** 으로 설정되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="59e2d-133">**리소스** \> **리소스 역할** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="59e2d-134">업데이트하려는 레코드를 연 다음 청구 타입 기본값을 **청구 가능** 으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="59e2d-135">리소스 역할을 위한 작업 시간 설정</span><span class="sxs-lookup"><span data-stu-id="59e2d-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="59e2d-136">리소스에는 생산 능력 계산을 위한 작업 시간이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="59e2d-137">**리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="59e2d-138">리소스를 선택하여 레코드를 연 다음 **작업 시간 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="59e2d-139">**리소스 목록** 보기에서 **작업 시간 템플릿** 을 적용함으로써 리소스 목록을 대량 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="59e2d-140">청구 가능한 실제값 시간 문제 해결</span><span class="sxs-lookup"><span data-stu-id="59e2d-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="59e2d-141">청구 가능한 실제값 시간은 **실제값** 엔터티에서 구합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="59e2d-142">청구 타입이 **청구 가능** 인 실제값이 계산에 포함되며 이러한 이유로 청구 가능한 실제값이 있는 프로젝트가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="59e2d-143">청구 가능한 사용률이 표시되지 않는 경우 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="59e2d-144">리소스에는 생산 능력에 대한 근무 시간이 정의되었습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="59e2d-145">리소스에 개별적으로 정의된 사용률 대상이 있거나 기본 역할이 할당되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="59e2d-146">역할에 대해 정의된 사용률 대상이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="59e2d-147">실제값은 활용도 계산을 예상하는 기간에 대해 **청구 가능** 인 청구 타입을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="59e2d-148">청구 가능 이외의 청구 타입을 갖는 실제값이 보이는 경우 다음을 체크하십시오:</span><span class="sxs-lookup"><span data-stu-id="59e2d-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="59e2d-149">실제에 사용되는 역할에는 청구 가능 이외의 기본 청구 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="59e2d-150">프로젝트를 백업하는 프로젝트 계약 내용에 대한 역할이 청구 가능 아님으로 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="59e2d-151">프로젝트에 연결된 계약 라인이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="59e2d-151">The project does not have an associated contract line.</span></span>

