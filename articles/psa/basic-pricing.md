---
title: 프로젝트 가격 책정
description: 이 항목은 Dynamics 365 Project Service Automation의 가격 책정 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: 88b791a1eb90d2aad67adba69169eab2c49c1318
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120776"
---
# <a name="project-pricing"></a><span data-ttu-id="6b480-103">프로젝트 가격 책정</span><span class="sxs-lookup"><span data-stu-id="6b480-103">Project pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6b480-104">Dynamics 365 Project Service Automation은 Dynamics 365 Sales에서 가격표 엔터티를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-104">Dynamics 365 Project Service Automation extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="6b480-105">주요 엔터티</span><span class="sxs-lookup"><span data-stu-id="6b480-105">Key entities</span></span>

<span data-ttu-id="6b480-106">가격표에는 네 가지 다른 엔터티에서 제공하는 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-106">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="6b480-107">**가격표** - 이 엔터티는 가격 책정 시간에 대한 컨텍스트, 통화, 날짜 유효성 및 시간 단위에 대한 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-107">**Price List** - This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="6b480-108">컨텍스트는 가격표가 비용 요금 또는 영업 요금을 나타내는지 여부를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-108">Context shows whether the price list is expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="6b480-109">**통화** - 이 엔터티는 가격표에 가격의 통화를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-109">**Currency** - This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="6b480-110">**날짜** - 이 엔터티는 시스템이 거래에 대한 기본 가격을 입력하려고 할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-110">**Date** - This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="6b480-111">PSA 가격 책정은 거래 날짜를 포함하는 날짜 유효성이 있는 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-111">PSA pricing selects the price list that has date effectivity that includes the date of the transaction.</span></span> <span data-ttu-id="6b480-112">PSA 가격 책정이 거래 날짜에 효과적인 두 개 이상의 가격표를 관련 견적, 계약 또는 조직 구성 단위에 첨부된 경우 가격이 기본값으로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-112">If PSA pricing finds more than one price list that is effective for the transaction date is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="6b480-113">**시간** - 이 엔터티는 일일 또는 시간당 요금과 같이 가격이 표시된 시간 단위를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-113">**Time** - This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="6b480-114">가격표 엔터티에는 가격을 저장하는 세 개의 관련 표가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-114">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="6b480-115">**역할 가격** - 이 표는 역할 및 조직 구성 단위 값의 조합에 대한 요금을 저장하며 인적 자원에 대한 역할 기반 가격을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-115">**Role Price** - This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="6b480-116">**거래 범주 가격** - 이 표는 거래 범주별로 가격을 저장하며 경비 범주 가격을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-116">**Transaction Category Price** - This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="6b480-117">**가격표 항목** - 이 표에는 카탈로그 제품의 가격이 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-117">**Price List Items** - This table stores prices for catalog products.</span></span>

> ![가격표를 사용하여 가격 구성](media/basic-guide-12.png)
 
<span data-ttu-id="6b480-119">가격표는 요금 카드입니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-119">The price list is a rate card.</span></span> <span data-ttu-id="6b480-120">요금 카드는 역할 가격, 거래 범주 가격 및 가격표 항목 표의 가격표 엔터티 및 관련 행의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="6b480-121">리소스 역할</span><span class="sxs-lookup"><span data-stu-id="6b480-121">Resource roles</span></span>

<span data-ttu-id="6b480-122">*리소스 역할* 이라는 용어는 사람이 프로젝트에서 특정 작업 집합을 수행해야 하는 기술, 역량 및 인증 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="6b480-123">인적 자원 시간은 일반적으로 리소스가 특정 프로젝트에서 채우는 역할에 따라 인용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-123">Human resources time is usually quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="6b480-124">인적 자원 시간의 경우 PSA는 리소스 역할을 기반으로 하는 비용 계산 및 청구를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-124">For human resource time, PSA supports costing and billing that are based on resource role.</span></span> <span data-ttu-id="6b480-125">시간은 **시간** 단위 그룹의 모든 단위로 가격이 책정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="6b480-126">PSA가 설치되면 **시간** 단위 그룹이 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-126">The **Time** unit group is crated when PSA is installed.</span></span> <span data-ttu-id="6b480-127">기본 **시간** 단위가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="6b480-128">**시간** 단위 그룹 또는 **시간** 단위에 있는 속성을 삭제, 이름 변경 또는 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-128">You can't delete, rename, or edit the attributes fo teh **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="6b480-129">그러나 **시간** 단위 그룹에 다른 단위를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="6b480-130">**시간** 단위 그룹 또는 **시간** 단위를 삭제하려고 하면 PSA 비즈니스 논리에 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the PSA business logic.</span></span>

> ![역할별로 가격 구성](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="6b480-132">거래 범주 및 경비 범주</span><span class="sxs-lookup"><span data-stu-id="6b480-132">Transaction categories and expense categories</span></span>

<span data-ttu-id="6b480-133">프로젝트 컨설턴트가 부담하는 여행 및 기타 경비는 일반적으로 고객에게 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-133">Travel and other expenses that project consultants incur are usually billed to the customer.</span></span> <span data-ttu-id="6b480-134">PSA는 가격 목록을 사용하여 경비 범주의 가격을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-134">PSA supports pricing of expense categories by using price lists.</span></span> <span data-ttu-id="6b480-135">항공료, 호텔 및 렌터카는 경비 범주의 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-135">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="6b480-136">경비에 대한 각 가격표는 특정 경비 범주에 대한 가격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-136">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="6b480-137">경비 범주의 가격 책정을 위해 PSA는 다음과 같은 세 가지 가격 책정 방법을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-137">For pricing of expense categories, PSA supports the following three pricing methods:</span></span>

- <span data-ttu-id="6b480-138">**비용** - 경비 비용은 고객에게 청구되며 가격 인상이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-138">**At cost** - The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="6b480-139">**원가 가산율** - 실제 비용에 대한 가산율은 고객에게 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-139">**Markup percentage** - The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="6b480-140">**단위당 가격** - 경비 범주의 각 단위에 대해 청구 가격이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-140">**Price per unit** - A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="6b480-141">고객이 청구하는 금액은 컨설턴트가 보고하는 경비 단위 수를 기준으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-141">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="6b480-142">마일리지는 단위당 가격 책정 방식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-142">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="6b480-143">예를 들어, 마일리지 경비 범주는 하루에 30달러(USD) 또는 마일당 2달러(USD)로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-143">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="6b480-144">컨설턴트가 프로젝트에 대한 마일리지를 보고하면 청구서 금액은 컨설턴트가 보고한 마일 수를 기준으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-144">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>

> ![경비 범주에 대한 가격 책정 구성](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="6b480-146">프로젝트 영업 가격 측정 및 재정의</span><span class="sxs-lookup"><span data-stu-id="6b480-146">Project sales pricing and overrides</span></span>

<span data-ttu-id="6b480-147">프로젝트 견적 및 계약의 경우 프로젝트 가격표는 제품 가격표와 다른 가격 재정의 패턴을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-147">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="6b480-148">제품 카탈로그 기반 견적 라인에서 각 견적 라인이 정확히 하나의 카탈로그 항목을 가리키므로 견적 라인에서 직접 역할 및 범주로 가격을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-148">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="6b480-149">그러나 프로젝트 기반 견적 라인에서는 견적 라인에서 직접 역할 및 범주에 대한 가격을 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-149">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="6b480-150">PSA는 두 가지 고유한 재정의 패턴을 지원하기 위해 프로젝트 가격표인 새로운 가격표 연결을 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-150">To support the two distinct override patterns, PSA has introduced a new price list association, the project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="6b480-151">가격 책정을 재정의할 때 둘 사이의 동작 차이로 인해 프로젝트 리소스및 카탈로그 항목에 대해 별도의 가격표를 두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-151">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="6b480-152">다음 각 엔터티에는 프로젝트 가격 책정에 대해 하나 이상의 관련 영업 가격표가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-152">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="6b480-153">고객 (거래처)</span><span class="sxs-lookup"><span data-stu-id="6b480-153">Customer (account)</span></span> 
- <span data-ttu-id="6b480-154">영업 기회</span><span class="sxs-lookup"><span data-stu-id="6b480-154">Opportunity</span></span> 
- <span data-ttu-id="6b480-155">견적</span><span class="sxs-lookup"><span data-stu-id="6b480-155">Quote</span></span> 
- <span data-ttu-id="6b480-156">프로젝트 계약</span><span class="sxs-lookup"><span data-stu-id="6b480-156">Project Contract</span></span>

<span data-ttu-id="6b480-157">가격표와 이러한 엔터티의 연결은 프로젝트 가격표로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-157">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="6b480-158">하나 이상의 가격표를 고객, 영업 기회, 견적 및 프로젝트 계약 판매 엔터티와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-158">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="6b480-159">고객 레코드에 기본 프로젝트 가격표가 자동으로 입력되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-159">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="6b480-160">그러나 프로젝트 가격표를 고객 레코드에 수동으로 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-160">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="6b480-161">그럼에도 불구하고 고객과 사용자 지정 가격 책정 계약을 체결한 경우에만 프로젝트 가격표를 수동으로 첨부해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-161">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="6b480-162">프로젝트 가격표가 영업 엔터티에 첨부되면 PSA는 다음 정보의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-162">When a project price list is attached to a sales entity, PSA validates the following information:</span></span>

- <span data-ttu-id="6b480-163">가격표에는 **영업** 의 컨텍스트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-163">The price list las a context of **Sales**.</span></span> 
- <span data-ttu-id="6b480-164">가격표 통화는 고객 통화와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-164">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="6b480-165">프로젝트 계약에서 PSA는 다음 우선 순위를 사용하여 관련 프로젝트 가격표를 자동으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-165">On a project contract, PSA uses the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="6b480-166">견적</span><span class="sxs-lookup"><span data-stu-id="6b480-166">Quote</span></span>
2. <span data-ttu-id="6b480-167">영업 기회</span><span class="sxs-lookup"><span data-stu-id="6b480-167">Opportunity</span></span>
3. <span data-ttu-id="6b480-168">고객</span><span class="sxs-lookup"><span data-stu-id="6b480-168">Customer</span></span> 
4. <span data-ttu-id="6b480-169">PSA용 전역 설정</span><span class="sxs-lookup"><span data-stu-id="6b480-169">Global settings for PSA</span></span>

<span data-ttu-id="6b480-170">기본적으로 프로젝트 가격표가 입력되면 PSA는 통화가 고객의 통화와 일치하는지, 입력된 기본 가격표에 **영업** 의 컨텍스트가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-170">When a project price list is entered by default, PSA validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="6b480-171">여러 프로젝트 가격표를 고객, 영업 기회, 견적 및 프로젝트 계약 엔터티와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-171">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="6b480-172">이 기능은 장기 실행 프로젝트 계약에 대한 날짜별 기본 가격을 지원하며, 인플레이션으로 인해 발생하는 가격 업데이트를 설명하기 위해 두 개 이상의 가격표가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-172">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="6b480-173">그러나 고객, 영업 기회, 견적 또는 프로젝트 계약 엔터티와 연결하는 가격표에 날짜 유효성이 겹치는 경우 기본 가격이 올바르지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-173">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="6b480-174">따라서 날짜 유효성이 겹치는 프로젝트 가격표가 해당 엔터티와 연결되지 않았는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-174">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="6b480-175">거래별 가격 재정의</span><span class="sxs-lookup"><span data-stu-id="6b480-175">Deal-specific price overrides</span></span>

<span data-ttu-id="6b480-176">PSA에서는 기본적으로 견적 또는 프로젝트 계약에 입력된 프로젝트 가격표에서 선택한 가격에 대한 거래별 재정의를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-176">In PSA, you can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="6b480-177">기본적으로 프로젝트 계약은 항상 마스터 영업 가격표에 대한 직접 링크 대신 마스터 영업 가격표의 복사본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-177">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="6b480-178">이 동작은 마스터 가격표를 변경해도 SOW(작업 명세서)에 대해 고객과 체결한 가격 계약이 변경되지 않도록 보장하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-178">This behavior helps guarantee that price agreements that are made iwth a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="6b480-179">그러나 견적에서 마스터 가격표를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-179">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="6b480-180">또는 마스터 가격표를 복사하여 편집하여 해당 견적에만 적용되는 사용자 지정 가격표를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-180">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="6b480-181">견적과 관련된 새 가격표를 만들려면 **견적** 페이지에서 **사용자 지정 가격 책정 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-181">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="6b480-182">견적에서만 거래별 프로젝트 가격표에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-182">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="6b480-183">사용자 지정 프로젝트 가격표를 만들 때 가격표의 프로젝트 구성 요소만 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-183">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="6b480-184">즉, 견적에 첨부된 기존 프로젝트 가격표의 복사본으로 만든 새 가격표이며, 이 새 가격표에는 관련 역할 가격 및 거래 범주 가격만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-184">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>

> ![프로젝트 계약에 대한 사용자 지정 가격 책정 보기 및 구성](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a><span data-ttu-id="6b480-186">비용 추적</span><span class="sxs-lookup"><span data-stu-id="6b480-186">Tracking costs</span></span>

<span data-ttu-id="6b480-187">PSA는 프로젝트에서 인적 자원 시간을 사용하는 데 드는 비용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-187">PSA tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="6b480-188">또한 출장 경비와 같이 프로젝트 중에 발생하는 기타 경비에 대한 비용도 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-188">It also tracks costs for other expenses that are incurrred during hte project, such as travel expenses.</span></span>

<span data-ttu-id="6b480-189">청구서 요금과 마찬가지로 인적 자원에 대한 비용 요금도 가격 목록을 사용하여 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-189">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="6b480-190">다음은 비용 가격표 및 영업 가격표의 동작의 주요 차이점입니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-190">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="6b480-191">리소스의 비용 요금은 특정 프로젝트, 계약 또는 견적에서 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-191">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="6b480-192">그러나 거래의 특성에 따라 변경 사항이 있는 경우 청구서 요금은 거래별로 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-192">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="6b480-193">다음 주문은 비용 가격표를 해결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-193">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="6b480-194">조직 구성 단위에 첨부된 비용 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-194">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="6b480-195">프로젝트 서비스 매개 변수에 첨부된 비용 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-195">The cost price list that is attached to the project service parameters.</span></span> <span data-ttu-id="6b480-196">PSA는 여러 다른 통화의 비용 가격표를 프로젝트 서비스 매개 변수에 연결할 수 있으므로 PSA는 프로젝트, 계약 또는 견적의 계약 조직 구성 단위의 통화와 비용 가격표의 통화 간에 통화 일치를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-196">Because cost price lists in many different currencies can be attached to project service parameters, PSA does a currency match between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="6b480-197">경비의 경우 비용 및 가격 인상 초과 비용 가격 책정 방법은 비용 가격표에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-197">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="6b480-198">이러한 가격 책정 방법을 비용 가격표 라인에서 거래 범주 비용을 설정하는 데 사용되더라도 시스템은 이를 무시하고 기본 비용 가격을 입력하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b480-198">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>
