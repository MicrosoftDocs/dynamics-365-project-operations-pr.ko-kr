---
title: 단위 그룹 및 단위
description: 이 항목은 단위 그룹 및 단위에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291627"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="cd7b1-103">단위 그룹 및 단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cd7b1-104">단위 그룹 및 단위는 Microsoft Dynamics 365의 기본 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="cd7b1-105">단위는 단일 측정 단위이며 여러 단위를 단위 그룹으로 그룹화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="cd7b1-106">단위 그룹은 Dynamics 365 사용자 인터페이스(UI)에서 단위 일람표라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="cd7b1-107">다음은 단위 및 단위 그룹의 몇 가지 예입니다:</span><span class="sxs-lookup"><span data-stu-id="cd7b1-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="cd7b1-108">**단위 그룹**: 거리</span><span class="sxs-lookup"><span data-stu-id="cd7b1-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="cd7b1-109">**단위**: 마일, 킬로미터 등.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="cd7b1-110">**단위 그룹**: 시간</span><span class="sxs-lookup"><span data-stu-id="cd7b1-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="cd7b1-111">**단위**: 시간, 일, 주 등.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="cd7b1-112">단위 그룹에 여러 단위를 설정할 때, 단위 그룹의 기본 또는 제1차 단위로 설정하는 첫 번째 단위를 지정함으로써 그들 사이의 변환 계수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="cd7b1-113">예컨대, **시간** 단위 그룹에서 첫 번째 단위로 **시간** 을 설정하면 시스템은 **시간** 을 기본 단위로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="cd7b1-114">설정하는 다음 단위가 **일** 인 경우, **일** 에서 **시간** 으로의 변환 계수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="cd7b1-115">그런 다음 세 번째 단위로 **주** 를 추가하는 경우, **일** 또는 **시간** 측면에서 **주** 에 대한 변환 계수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="cd7b1-116">다음 이미지는 **일** 단위 설정의 예를 보여줍니다, 여기서 **수량** 필드는 하루에 있는 시간 수를 나타내고, **주** 단위 설정의 경우 **수량** 필드는 한 주에 있는 일 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![단위 그룹: 정보 페이지](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="cd7b1-118">단위 및 단위 그룹 사용</span><span class="sxs-lookup"><span data-stu-id="cd7b1-118">Using units and unit groups</span></span>

<span data-ttu-id="cd7b1-119">Dynamics 365 Project Service Automation은 단위 및 단위 그룹을 사용하여 경비와 시간에 대한 추산 및 항목을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="cd7b1-120">경비의 경우, 각 경비 카테고리는 기본 단위 그룹 및 단위를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="cd7b1-121">이러한 값은 경비 카테고리에 대한 가격표 항목에 기본값으로 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="cd7b1-122">예컨대, **마일리지** 라는 경비 카테고리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="cd7b1-123">**거리** 라는 단위 그룹과 **마일** 이라는 기본 단위가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="cd7b1-124">단위가 두 개(**마일** 및 **킬로미터**)인 를 설정하면 **거리** 단위 그룹을 설정하면 한  가격표의 **마일리지** 카테고리에 두 가지 가격을 설정할 수 있습니다: 마일당 가격 및 킬로미터당 가격.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="cd7b1-125">경비 카테고리</span><span class="sxs-lookup"><span data-stu-id="cd7b1-125">Expense category</span></span>  | <span data-ttu-id="cd7b1-126">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="cd7b1-126">Unit group</span></span>  | <span data-ttu-id="cd7b1-127">단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-127">Unit</span></span>      | <span data-ttu-id="cd7b1-128">가격 산정법</span><span class="sxs-lookup"><span data-stu-id="cd7b1-128">Pricing method</span></span>  | <span data-ttu-id="cd7b1-129">단가</span><span class="sxs-lookup"><span data-stu-id="cd7b1-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="cd7b1-130">마일리지</span><span class="sxs-lookup"><span data-stu-id="cd7b1-130">Mileage</span></span>           | <span data-ttu-id="cd7b1-131">거리</span><span class="sxs-lookup"><span data-stu-id="cd7b1-131">Distance</span></span>      | <span data-ttu-id="cd7b1-132">마일</span><span class="sxs-lookup"><span data-stu-id="cd7b1-132">Mile</span></span>      | <span data-ttu-id="cd7b1-133">단가</span><span class="sxs-lookup"><span data-stu-id="cd7b1-133">Price per unit</span></span>    | <span data-ttu-id="cd7b1-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="cd7b1-134">10 USD</span></span>            |
| <span data-ttu-id="cd7b1-135">마일리지</span><span class="sxs-lookup"><span data-stu-id="cd7b1-135">Mileage</span></span>           | <span data-ttu-id="cd7b1-136">거리</span><span class="sxs-lookup"><span data-stu-id="cd7b1-136">Distance</span></span>      | <span data-ttu-id="cd7b1-137">킬로미터</span><span class="sxs-lookup"><span data-stu-id="cd7b1-137">Kilometer</span></span> | <span data-ttu-id="cd7b1-138">단가</span><span class="sxs-lookup"><span data-stu-id="cd7b1-138">Price per unit</span></span>    |  <span data-ttu-id="cd7b1-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="cd7b1-139">6 USD</span></span>            |

<span data-ttu-id="cd7b1-140">프로젝트에 대한 경비를 입력하면 시스템은 경비에 대한 카테고리와 단위의 조합을 통해 가격을 산정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="cd7b1-141">경비 설명</span><span class="sxs-lookup"><span data-stu-id="cd7b1-141">Expense description</span></span>        | <span data-ttu-id="cd7b1-142">경비 카테고리</span><span class="sxs-lookup"><span data-stu-id="cd7b1-142">Expense category</span></span>  | <span data-ttu-id="cd7b1-143">단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-143">Unit</span></span>  | <span data-ttu-id="cd7b1-144">수량</span><span class="sxs-lookup"><span data-stu-id="cd7b1-144">Quantity</span></span>  | <span data-ttu-id="cd7b1-145">단가</span><span class="sxs-lookup"><span data-stu-id="cd7b1-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="cd7b1-146">클라이언트 위치까지의 운전</span><span class="sxs-lookup"><span data-stu-id="cd7b1-146">Drive to client location</span></span> | <span data-ttu-id="cd7b1-147">마일리지</span><span class="sxs-lookup"><span data-stu-id="cd7b1-147">Mileage</span></span>             | <span data-ttu-id="cd7b1-148">마일</span><span class="sxs-lookup"><span data-stu-id="cd7b1-148">Mile</span></span>  | <span data-ttu-id="cd7b1-149">10</span><span class="sxs-lookup"><span data-stu-id="cd7b1-149">10</span></span>        | <span data-ttu-id="cd7b1-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="cd7b1-150">10 USD</span></span>         |

<span data-ttu-id="cd7b1-151">시간의 경우, 각 가격표 표제에 **기본 시간 단위** 필드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="cd7b1-152">그 값은 가격표 표제를 만들 때 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="cd7b1-153">그런 다음 이 단위를 사용하여 해당 가격표에 대한 모든 역할 기반 가격이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="cd7b1-154">**견적에서의 시간** 필드의 추산 행은 어떤 시간 단위로도 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="cd7b1-155">그러나 프로젝트의 추산 행과 프로젝트의 시간 항목은 **시간** 시간 단위만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="cd7b1-156">시간 항목 또는 추산 행에서의 단위가 해당 역할의 가격표 행에 있는 단위와 일치하지 않으면 시스템은 가격을 프로젝트 추산 또는 프로젝트 실제값 처리에서 정의된 단위로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="cd7b1-157">다음 예는 PSA가 단위 그룹, 단위 및 변환 요소를 사용하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="cd7b1-158">Units</span><span class="sxs-lookup"><span data-stu-id="cd7b1-158">Units</span></span>

   - <span data-ttu-id="cd7b1-159">**단위 그룹**: 시간</span><span class="sxs-lookup"><span data-stu-id="cd7b1-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="cd7b1-160">**단위**: 시간</span><span class="sxs-lookup"><span data-stu-id="cd7b1-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="cd7b1-161">**일** - 전환 계수: 8시간</span><span class="sxs-lookup"><span data-stu-id="cd7b1-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="cd7b1-162">**주** - 전환 계수: 8시간</span><span class="sxs-lookup"><span data-stu-id="cd7b1-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="cd7b1-163">프로젝트 A의 가격표 설정:</span><span class="sxs-lookup"><span data-stu-id="cd7b1-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="cd7b1-164">**명칭**: 2016년 영국 판매 가격</span><span class="sxs-lookup"><span data-stu-id="cd7b1-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="cd7b1-165">**기본 시간 단위**: 일</span><span class="sxs-lookup"><span data-stu-id="cd7b1-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="cd7b1-166">**통화**: GBP</span><span class="sxs-lookup"><span data-stu-id="cd7b1-166">**Currency**: GBP</span></span>

| <span data-ttu-id="cd7b1-167">역할</span><span class="sxs-lookup"><span data-stu-id="cd7b1-167">Role</span></span>      | <span data-ttu-id="cd7b1-168">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="cd7b1-168">Unit group</span></span> | <span data-ttu-id="cd7b1-169">단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-169">Unit</span></span> | <span data-ttu-id="cd7b1-170">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-170">Organizational unit</span></span> | <span data-ttu-id="cd7b1-171">가격</span><span class="sxs-lookup"><span data-stu-id="cd7b1-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="cd7b1-172">개발자</span><span class="sxs-lookup"><span data-stu-id="cd7b1-172">Developer</span></span> | <span data-ttu-id="cd7b1-173">Time</span><span class="sxs-lookup"><span data-stu-id="cd7b1-173">Time</span></span>       | <span data-ttu-id="cd7b1-174">Day</span><span class="sxs-lookup"><span data-stu-id="cd7b1-174">Day</span></span>  | <span data-ttu-id="cd7b1-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="cd7b1-175">Contoso UK</span></span>          | <span data-ttu-id="cd7b1-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="cd7b1-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="cd7b1-177">시간 항목</span><span class="sxs-lookup"><span data-stu-id="cd7b1-177">Time entry</span></span>

<span data-ttu-id="cd7b1-178">다음 표는 PSA가 3시간짜리 프로젝트에 대해 만든 판매측 처리를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="cd7b1-179">프로젝트</span><span class="sxs-lookup"><span data-stu-id="cd7b1-179">Project</span></span>   | <span data-ttu-id="cd7b1-180">작업</span><span class="sxs-lookup"><span data-stu-id="cd7b1-180">Task</span></span>    | <span data-ttu-id="cd7b1-181">역할</span><span class="sxs-lookup"><span data-stu-id="cd7b1-181">Role</span></span>      | <span data-ttu-id="cd7b1-182">수량</span><span class="sxs-lookup"><span data-stu-id="cd7b1-182">Quantity</span></span> | <span data-ttu-id="cd7b1-183">단위</span><span class="sxs-lookup"><span data-stu-id="cd7b1-183">Unit</span></span>  | <span data-ttu-id="cd7b1-184">단가</span><span class="sxs-lookup"><span data-stu-id="cd7b1-184">Unit price</span></span> | <span data-ttu-id="cd7b1-185">미청구 매출액</span><span class="sxs-lookup"><span data-stu-id="cd7b1-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="cd7b1-186">프로젝트 A</span><span class="sxs-lookup"><span data-stu-id="cd7b1-186">Project A</span></span> | <span data-ttu-id="cd7b1-187">디자인</span><span class="sxs-lookup"><span data-stu-id="cd7b1-187">Design</span></span>  | <span data-ttu-id="cd7b1-188">개발자</span><span class="sxs-lookup"><span data-stu-id="cd7b1-188">Developer</span></span> | <span data-ttu-id="cd7b1-189">3</span><span class="sxs-lookup"><span data-stu-id="cd7b1-189">3</span></span>        | <span data-ttu-id="cd7b1-190">Hour</span><span class="sxs-lookup"><span data-stu-id="cd7b1-190">Hour</span></span>  | <span data-ttu-id="cd7b1-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="cd7b1-191">100 GBP</span></span>    | <span data-ttu-id="cd7b1-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="cd7b1-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="cd7b1-193">시간 단위 FAQ</span><span class="sxs-lookup"><span data-stu-id="cd7b1-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="cd7b1-194">경비의 경우 PSA는 다른 단위로 변환됩니까?</span><span class="sxs-lookup"><span data-stu-id="cd7b1-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="cd7b1-195">번호</span><span class="sxs-lookup"><span data-stu-id="cd7b1-195">No.</span></span> <span data-ttu-id="cd7b1-196">단위 변환은 시간을 위해서만 기능합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-196">Unit conversion works only for time.</span></span> <span data-ttu-id="cd7b1-197">경비의 경우, 시스템이 경비 카테고리와 단위의 조합을 위한 가격을 찾을 수 없는 경우 가격은 기본적으로 0.00으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="cd7b1-198">PSA가 시간 단위를 변환하는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="cd7b1-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="cd7b1-199">일부 국가 또는 지역에서는 며칠 안에 청구서 요율을 설정해야 하는 법적 요건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="cd7b1-200">견적 주기 동안 가격 협상 및 할인은 각 청구 가능한 역할에 대한 일 요율을 사용하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="cd7b1-201">스케줄 추산 및 시간 항목은 시간에서 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="cd7b1-202">시간 단위의 이러한 차이를 지원하기 위해 PSA는 시간 단위를 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="cd7b1-203">프로젝트 추산에서 시간 단위를 변경할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="cd7b1-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="cd7b1-204">번호</span><span class="sxs-lookup"><span data-stu-id="cd7b1-204">No.</span></span> <span data-ttu-id="cd7b1-205">현재 스케줄 추산은 시간으로 제약되어 있으며 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="cd7b1-206">단위 및 단위 그룹을 편집, 삭제 및 추가할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="cd7b1-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="cd7b1-207">예.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-207">Yes.</span></span> <span data-ttu-id="cd7b1-208">**시간** 단위 그룹 및 **시간** 단위를 예외로 하고, 모든 단위를 삭제하거나 편집할 수 있으며 새 단위를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="cd7b1-209">PSA에서는 **시간** 단위 그룹과 **시간** 단위를 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="cd7b1-210">그러나 **이름** 필드에 대한 번역된 텍스트로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7b1-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]