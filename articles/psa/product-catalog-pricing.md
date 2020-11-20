---
title: 제품 카탈로그 가격
description: 이 항목은 Dynamics 365 Project Service Automation(PSA)에서 제품 카탈로그 가격이 기능하는 방식에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 11f1d237be4540a64f1854fbed4e5c72ebbce18d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132296"
---
# <a name="product-catalog-pricing"></a><span data-ttu-id="70edb-103">제품 카탈로그 가격</span><span class="sxs-lookup"><span data-stu-id="70edb-103">Product catalog pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="70edb-104">가격표 및 가격표 항목 엔터티는 제품 카탈로그 가격을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-104">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="70edb-105">대부분의 경우 이 기능은 프로젝트 견적 및 프로젝트 계약의 카탈로그 기반 행에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-105">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="70edb-106">프로젝트 기반 행의 경우, 계약은 수주 후 거래를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-106">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="70edb-107">협상 프로세스는 일반적으로 승리에 우선하기 때문에 견적에 첨부된 가격은 항상 있는 대로 복사되어 새 가격표에 첨부되고 계약에 첨부됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-107">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="70edb-108">이 새 가격표는 계약 범위를 벗어나 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-108">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="70edb-109">이 제한은 마스터 가격표에서 발생하는 모든 가격 변동으로부터 협상된 요율표를 보호하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-109">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="70edb-110">제품 카탈로그에 기본 원가 및 가격표가 있도록 제품을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-110">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="70edb-111">정가, 표준 원가 및 현재 원가를 사용하여 기본 원가 및 정가를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-111">You must use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="70edb-112">시스템이 제품 가격표에서 견적 또는 프로젝트 계약을 위한 해당 제품의 가격표 행을 찾을 수 없는 경우에만 견적 행 또는 프로젝트 계약 행에 기본 정가가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-112">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="70edb-113">견적들 사이에 제품 카탈로그 행의 원가를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-113">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="70edb-114">이 기능은 원가를 정확하게 추적하지 않으면 프로젝트 계약에 대한 운영 수익을 결정할 수 없기 때문에 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-114">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="70edb-115">기본적으로 제품의 표준 원가가 원가로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-115">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="70edb-116">그러나 해당 견적에 대해 다른 원가가 있는 경우 견적 행에서 기본 원가를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-116">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="70edb-117">가격표 항목</span><span class="sxs-lookup"><span data-stu-id="70edb-117">Price list items</span></span>

<span data-ttu-id="70edb-118">제품 카탈로그의 제품을 다른 가격표에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-118">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="70edb-119">제품의 가격표 행은 항상 특정 단위를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-119">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="70edb-120">가격표 항목의 제품 가격은 통화 금액으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-120">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="70edb-121">또는 제품 가격은 정가, 현재 원가 또는 표준 원가의 함수로 구성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-121">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="70edb-122">가격이 정가, 표준 원가 또는 현재 원가의 함수로 구성된 경우 PSA는 다양한 반올림 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-122">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="70edb-123">여러 가격 책정 방법 및 반올림 옵션을 활용하는 것 외에도 할인 목록을 가격표 항목과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-123">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

> ![카탈로그의 제품을 다른 가격표에 추가하기](media/basic-guide-16.png)

<span data-ttu-id="70edb-125">**프로젝트 견적** 페이지에서 **맞춤 가격 생성** 을 선택하여 견적을 위한 새 맞춤 가격표를 만들면 PSA가 가격표의 복사본을 만들고, 새 가격표의 표제에 있는 **엔터티** 필드가 **매출액 엔터티** 에 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, PSA makes a copy of the price list, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="70edb-126">새 가격표의 명칭이 견적의 명칭 및 타임스탬프와 함께 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="70edb-127">귀하는 또한 새 가격표의 명칭과 맞춤 워크플로우에서 견적의 명칭을 사용하여 맞춤 가격 책정을 사용하는 견적에 대한 추가 검토 및 승인을 촉발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="70edb-128">기본 제품 가격표</span><span class="sxs-lookup"><span data-stu-id="70edb-128">Default product price list</span></span>
<span data-ttu-id="70edb-129">각 고객 레코드에는 **기본 가격표** 필드가 있어서, 고객의 통화와 일치하는 가격표를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="70edb-130">PSA에서 기본값은 이 필드에 자동으로 입력되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-130">In PSA, a default value isn't automatically entered in this field.</span></span> <span data-ttu-id="70edb-131">특정 고객과의 맞춤 가격 책정 계약이 있는 경우 이 필드를 사용하여 가격표를 해당 고객과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="70edb-132">기회, 견적 및 프로젝트 계약 엔터티는 다음 순서를 사용하여 기본 제품 가격표를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="70edb-133">프로젝트 가격표에 동일한 순서가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="70edb-134">견적</span><span class="sxs-lookup"><span data-stu-id="70edb-134">Quote</span></span>
2.  <span data-ttu-id="70edb-135">영업 기회</span><span class="sxs-lookup"><span data-stu-id="70edb-135">Opportunity</span></span>
3.  <span data-ttu-id="70edb-136">고객</span><span class="sxs-lookup"><span data-stu-id="70edb-136">Customer</span></span>
4.  <span data-ttu-id="70edb-137">PSA용 전역 설정</span><span class="sxs-lookup"><span data-stu-id="70edb-137">Global settings for PSA</span></span>

<span data-ttu-id="70edb-138">기본적으로 견적 행의 **제품** 필드에는 견적의 제품 가격표에 있는 모든 활성 제품이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="70edb-139">제품이 비활성화되었거나 초안 제품인 경우 가격표에 있더라도 제품이 나열되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="70edb-140">제품 카탈로그 행은 프로젝트 계약에 대해 작성된 첫 번째 청구서의 행으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="70edb-141">초안 청구서에서 이러한 청구서 행을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="70edb-142">이 경우 청구서가 발행될 때까지 또는 고객에게 청구서가 발송될 때까지 후속 청구서에 행이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="70edb-143">PSA에서는 제품 청구서 행의 부분 수량에 대해 청구서를 발행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-143">In PSA, you can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="70edb-144">프로젝트 계약의 제품 행이 청구서 발행되면 실제값이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="70edb-145">그러나 이러한 실제값이 관련 프로젝트 엔터티에 연계되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="70edb-146">즉, 제품 기반 프로젝트 계약 행은 프로젝트 기반 사용량과 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="70edb-147">PSA는 프로젝트에 대한 자재 소비량을 추적하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70edb-147">PSA doesn't track material consumption on projects.</span></span>
