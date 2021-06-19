---
title: 제품 가격표
description: 이 항목은 프로젝트 견적 및 계약에 사용되는 카탈로그 가격 책정의 가격 목록에 대한 정보를 제공합니다.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004944"
---
# <a name="product-price-lists"></a><span data-ttu-id="8b043-103">제품 가격표</span><span class="sxs-lookup"><span data-stu-id="8b043-103">Product price lists</span></span>

<span data-ttu-id="8b043-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="8b043-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="8b043-105">Project Operations에서 **제품 가격표** 및 관련 가격표 항목 엔터티는 제품 기반 견적 및 계약 내용에서 제품 가격 책정 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="8b043-106">프로젝트에 사용되는 제품의 경우 프로젝트 가격표에 대한 가격표 항목 레코드가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="8b043-107">제품 카탈로그에 기본 원가 및 가격표가 있도록 제품을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="8b043-108">정가, 표준 원가 및 현재 원가를 사용하여 기본 원가 및 정가를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="8b043-109">시스템이 제품 가격표에서 견적 또는 프로젝트 계약을 위한 해당 제품의 가격표 행을 찾을 수 없는 경우에만 견적 행 또는 프로젝트 계약 행에 기본 정가가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="8b043-110">견적들 사이에 제품 카탈로그 행의 원가를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="8b043-111">이 기능은 원가를 정확하게 추적하지 않으면 프로젝트 계약에 대한 운영 수익을 결정할 수 없기 때문에 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="8b043-112">기본적으로 제품의 표준 원가가 원가로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="8b043-113">그러나 해당 견적에 대해 다른 원가가 있는 경우 견적 행에서 기본 원가를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="8b043-114">가격표 항목</span><span class="sxs-lookup"><span data-stu-id="8b043-114">Price list items</span></span>

<span data-ttu-id="8b043-115">제품 카탈로그의 제품을 다른 가격표에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="8b043-116">제품의 가격표 행은 항상 특정 단위를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="8b043-117">가격표 항목의 제품 가격은 통화 금액으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="8b043-118">또는 제품 가격은 정가, 현재 원가 또는 표준 원가의 함수로 구성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="8b043-119">제품 가격이 정가, 표준 원가 또는 현재 원가의 함수로 구성된 경우 가격 책정 기능은 다양한 반올림 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="8b043-120">여러 가격 책정 방법 및 반올림 옵션을 활용하는 것 외에도 할인 목록을 가격표 항목과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="8b043-121">기본 제품 가격표</span><span class="sxs-lookup"><span data-stu-id="8b043-121">Default product price list</span></span>
<span data-ttu-id="8b043-122">각 고객 레코드에는 **기본 가격표** 필드가 있어서, 고객의 통화와 일치하는 가격표를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="8b043-123">기본값은 이 필드에 자동으로 입력되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="8b043-124">특정 고객과의 맞춤 가격 책정 계약이 있는 경우 이 필드를 사용하여 가격표를 해당 고객과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="8b043-125">기회, 견적 및 프로젝트 계약 엔터티는 다음 순서를 사용하여 기본 제품 가격표를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="8b043-126">프로젝트 가격표에 동일한 순서가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="8b043-127">견적</span><span class="sxs-lookup"><span data-stu-id="8b043-127">Quote</span></span>
2.  <span data-ttu-id="8b043-128">영업 기회</span><span class="sxs-lookup"><span data-stu-id="8b043-128">Opportunity</span></span>
3.  <span data-ttu-id="8b043-129">고객</span><span class="sxs-lookup"><span data-stu-id="8b043-129">Customer</span></span>
4.  <span data-ttu-id="8b043-130">전역 설정</span><span class="sxs-lookup"><span data-stu-id="8b043-130">Global settings</span></span> 

<span data-ttu-id="8b043-131">기본적으로 견적 행의 **제품** 필드에는 견적의 제품 가격표에 있는 모든 활성 제품이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="8b043-132">제품이 비활성화되었거나 초안 제품인 경우 가격표에 있더라도 제품이 나열되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="8b043-133">제품 카탈로그 행은 프로젝트 계약에 대해 작성된 첫 번째 청구서의 행으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="8b043-134">초안 청구서에서 이러한 청구서 행을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="8b043-135">이 경우 청구서가 발행될 때까지 또는 고객에게 청구서가 발송될 때까지 후속 청구서에 행이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="8b043-136">제품 청구서 행의 부분 수량에 대해 청구서를 발행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="8b043-137">프로젝트 계약의 제품 행이 청구서 발행되면 실제값이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="8b043-138">그러나 이러한 실제값이 관련 프로젝트 엔터티에 연계되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="8b043-139">즉, 제품 기반 프로젝트 계약 행은 프로젝트 기반 사용량과 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8b043-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
