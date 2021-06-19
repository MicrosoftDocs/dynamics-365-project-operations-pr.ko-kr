---
title: 마일리지 비율 계층을 사용하여 마일리지 설정
description: 이 항목은 마일리지 비율 및 마일리지 비율 계층에 대한 정보를 제공합니다.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083679"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a><span data-ttu-id="4f6b7-103">마일리지 비율 계층을 사용하여 마일리지 설정</span><span class="sxs-lookup"><span data-stu-id="4f6b7-103">Set up mileage using mileage rate tiers</span></span>

<span data-ttu-id="4f6b7-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="4f6b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4f6b7-105">경비가 보고되고 선택한 경비 범주가 **마일리지** 인 경우 해당 경비 라인의 금액은 *마일리지당 비율* 금액에 따라 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-105">When an expense is reported and the selected expense category is **Mileage**, the amount for that expense line is calculated according to the *rate per mileage* amount.</span></span> <span data-ttu-id="4f6b7-106">이 금액은 정의된 마일리지 비율을 사용하거나 마일리지 비율이 설정되지 않은 경우 표준 마일리지 비율에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-106">This amount is determined by using defined mileage tiers or, if no mileage rate tiers are set up, by following a standard rate of mileage.</span></span> 

<span data-ttu-id="4f6b7-107">마일리지 비율 계층은 **경비 관리** > **설정** > **일반** > **경비 범주** > **마일리지** > **범주 설정** 으로 이동하여 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-107">Mileage rate tiers can be set up by going to **Expense Management** > **Setup** > **General** > **Expense categories** > **Mileage** > **Category setup**.</span></span>

<span data-ttu-id="4f6b7-108">10.0.18로 업그레이드한 후 조직에서 마일리지 경비 범주를 사용하는 경우 아래의 설계 변경 사항을 검토한 후 마일리지 기능을 활성화하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-108">After you upgrade to 10.0.18, if your organization uses the mileage expense category, consider enabling the mileage feature after reviewing the design changes below.</span></span> 

<span data-ttu-id="4f6b7-109">새로운 설계 마일리지 비율은 **수량** 필드의 값이 처리되는 방식에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-109">The new design of mileage rate tiers impacts how the value in the **Quantity** field is processed.</span></span> <span data-ttu-id="4f6b7-110">10.0.18 릴리스 이전에는 **수량** 필드의 값이 하한으로 간주되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-110">Prior to the release of 10.0.18, the value in the **Quantity** field was considered to be the lower limit.</span></span> <span data-ttu-id="4f6b7-111">누적이 해당 값을 초과하면 해당 비율이 사용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-111">When accumulation crossed that value, the corresponding rate was used.</span></span>  <span data-ttu-id="4f6b7-112">10.0.18부터는 **수량** 필드가 상한으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-112">As of 10.0.18, the value in the **Quantity** field is considered the upper limit.</span></span> <span data-ttu-id="4f6b7-113">마일리지 누적량이 **수량** 필드의 값보다 적을 때 해당 비율이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-113">The corresponding rate is used when mileage accumulation is less than the value in the **Quantity** field.</span></span>  <span data-ttu-id="4f6b7-114">마일리지 비율에 대한 새로운 모델은 마일리지 비율 간의 일관성과 더 나은 사용성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-114">The new model for mileage tiers helps with consistency across mileage tiers and better usability.</span></span>   

<span data-ttu-id="4f6b7-115">승인된 모든 경비 보고서는 새 디자인에 따라 게시하는 동안 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-115">All approved expense reports will be recalculated during posting according to the new design.</span></span>

## <a name="example"></a><span data-ttu-id="4f6b7-116">예제</span><span class="sxs-lookup"><span data-stu-id="4f6b7-116">Example</span></span>
 
### <a name="before-version-10018"></a><span data-ttu-id="4f6b7-117">10.0.18 이전 버전</span><span class="sxs-lookup"><span data-stu-id="4f6b7-117">Before version 10.0.18</span></span>
<span data-ttu-id="4f6b7-118">두 마일리지 비율 계층으로 각 계층의 **수량** 필드는 마일리지 하한을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-118">With two mileage rate tiers, the **Quantity** field in each tier represents the lower mileage limit.</span></span> <span data-ttu-id="4f6b7-119">현재 계층 1의 값은 0이고 비율은 0.45이고 계층 2는 값이 1000이고 비율은 0.25입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-119">Currently, tier one has a value of zero (0) and a rate of 0.45, and tier two has a value of 1000 and a rate of 0.25.</span></span> <span data-ttu-id="4f6b7-120">누적된 마일 또는 킬로미터가 필드의 값을 초과하는 경우 관련 비율이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-120">If the accumulated miles or kilometers crosses the value in the field, the related rate is used.</span></span> <span data-ttu-id="4f6b7-121">수량이 0인 라인이 없는 경우 시스템은 경비 관리에 정의된 마일리지 비율을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-121">If there's no line with zero quantity, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="4f6b7-122">직원이 1,500 마일의 경비 보고서를 제출하는 경우 게시된 경비 보고서의 두 마일리지 라인은 1000(비율 0.45) + 500(비율 0.25) = 575.00입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-122">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575.00.</span></span>

### <a name="after-version-10018"></a><span data-ttu-id="4f6b7-123">버전 10.0.18 이후</span><span class="sxs-lookup"><span data-stu-id="4f6b7-123">After version 10.0.18</span></span>
<span data-ttu-id="4f6b7-124">10.0.18에서는 각 계층의 **수량** 필드는 계층의 상한을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-124">In 10.0.18, the **Quantity** field in each tier represents the upper limit of the tier.</span></span> <span data-ttu-id="4f6b7-125">현재 계층 1의 값은 999이고 비율은 0.45이고 계층 2는 값이 999,999,999.00이고 비율은 0.25입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-125">Currently, tier one has a value of 999 and a rate of 0.45, and tier two has a value of 999,999,999.00 and a rate of 0.25.</span></span> <span data-ttu-id="4f6b7-126">누적된 마일 또는 킬로미터가 **수량** 필드의 값을 초과하는 경우 관련 비율이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-126">If the accumulated miles or kilometers crosses the value in the **Quantity** field, the related rate is used.</span></span> <span data-ttu-id="4f6b7-127">모든 상한이 초과된 경우 시스템은 경비 관리에 정의된 마일리지 비율을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-127">If all upper limits are exceeded, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="4f6b7-128">동일한 시나리오를 올바르게 계산하려면 계층 설정을 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-128">To correctly calculate the same scenario, the tier set up must be changed.</span></span> <span data-ttu-id="4f6b7-129">계층 1의 **수량** 필드 값은 999.00이고 계층 2의 값은 999,999,999.00입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-129">The **Quantity** field in tier one has a value of 999.00 and a value of 999,999,999.00 in tier two.</span></span> <span data-ttu-id="4f6b7-130">직원이 계층 1의 총 마일 또는 킬로미터를 초과하는 경우 시스템은 경비 관리에 정의된 마일리지 비율을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-130">If an employee exceeds the total quantity of miles or kilometers in tier one, the system uses the rate of mileage that is defined in Expense management.</span></span> 
  
<span data-ttu-id="4f6b7-131">직원이 1,500 마일의 경비 보고서를 제출하는 경우 게시된 경비 보고서의 두 마일리지 라인은 1000(비율 0.45) + 500(비율 0.25) = 575입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-131">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575</span></span>

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a><span data-ttu-id="4f6b7-132">동일한 비율 기능으로 여러 마일리지 계층에 대해 마일리지 금액 계산을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-132">Enable the Mileage amount calculation for multiple mileage tiers with same rate feature</span></span>

<span data-ttu-id="4f6b7-133">**동일한 비율 기능으로 여러 마일리지 계층에 대해 마일리지 금액 계산** 기능은 마일리지 비율 계산을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-133">The **Mileage amount calculation for multiple mileage tiers with same rate** feature improves mileage rate calculation.</span></span> <span data-ttu-id="4f6b7-134">이 기능을 사용하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-134">Complete the following steps to enable this feature.</span></span>

1. <span data-ttu-id="4f6b7-135">**작업 영역** > **기능 관리** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-135">Go to **Workspaces** > **Feature Management**.</span></span> 
2. <span data-ttu-id="4f6b7-136">목록에서 **동일한 비율의 여러 마일리지 등급에 대한 마일리지 금액 계산** 을 찾아 선택한 다음 **지금 사용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-136">In the list, locate and select **Mileage amount calculation for multiple mileage tiers with same rate**, and then select **Enable now**.</span></span>

<span data-ttu-id="4f6b7-137">기능을 활성화한 후 마일리지 등급을 재설정하여 **수량** 필드의 값을 올바르게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b7-137">After you enable the feature, reset the mileage tiers to correctly reflect the value of the **Quantity** field.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
