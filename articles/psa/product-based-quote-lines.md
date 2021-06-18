---
title: 제품 기반 견적 행
description: 이 항목은 제품 기반 견적 행에 대한 정보를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998509"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="4256a-103">제품 기반 견적 행</span><span class="sxs-lookup"><span data-stu-id="4256a-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="4256a-104">Dynamics 365 Project Service Automation에서 제품 기반 견적 행을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4256a-105">제품 기반 견적 행은 "쓰기" 행이거나 제품 카탈로그의 항목일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4256a-106">제품 카탈로그</span><span class="sxs-lookup"><span data-stu-id="4256a-106">Product catalog</span></span>

<span data-ttu-id="4256a-107">Dynamics 365 제품 카탈로그의 제품은 기본 단위와 단위 그룹을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="4256a-108">여러 제품이 동일한 속성 집합을 공유하는 경우 그러한 속성을 갖는 제품군을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="4256a-109">한 제품군의 모든 제품은 동일한 속성 집합을 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="4256a-110">예컨대, 어떤 회사가 다양한 소프트웨어에 대한 신청 라이선스를 판매합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="4256a-111">모든 신청 소프트웨어는 다음 두 가지 속성을 갖습니다:</span><span class="sxs-lookup"><span data-stu-id="4256a-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4256a-112">사용자 수</span><span class="sxs-lookup"><span data-stu-id="4256a-112">Number of users</span></span> 
- <span data-ttu-id="4256a-113">가입 기간 (개월)</span><span class="sxs-lookup"><span data-stu-id="4256a-113">Subscription duration (in months)</span></span>

<span data-ttu-id="4256a-114">이 타입의 카탈로그를 유지하는 좋은 방법은 명칭이 **신청 소프트웨어** 이고, 속성으로서 **사용자 수** 와 **가입 기간** 을 갖는 제품군을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="4256a-115">그런 다음 **신청 소프트웨어** 제품군에 **Dynamics 365 Sales** 또는 **Dynamics 365 Field Service** 같은 개별 제품을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4256a-116">프로젝트 견적에 제품 카탈로그 항목 추가</span><span class="sxs-lookup"><span data-stu-id="4256a-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="4256a-117">프로젝트 견적 및 프로젝트 계약 페이지는 프로젝트 기반 행과 제품 기반 행의 두 가지 타입을 위한 섹션을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="4256a-118">제품 기반 행의 경우 Dynamics 365는 제품 카탈로그의 항목을 견적에 추가하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="4256a-119">견적 행 또는 프로젝트 계약 행의 드롭다운 목록은 견적 또는 프로젝트 계약에 첨부된 제품 가격 목록에 있는 모든 제품 및 단위를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="4256a-120">견적의 제품 가격 목록에 속하지 않은 제품을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="4256a-121">또한 다른 가격 목록에서 제품을 선택하거나 제품 카탈로그에서 직접 제품을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="4256a-122">제품 카탈로그에서 직접 제품을 선택하면 해당 제품의 기본 가격 목록이 제품의 판매 가격을 얻는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4256a-123">기본 가격 목록이 설정되지 않은 경우 가격은 0(제로)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="4256a-124">견적 행이 제품 카탈로그에 근거하는 경우 견적 행에서 직접 판매 가격을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4256a-125">Dynamics 365의 견적 행은 **가격** 필드를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="4256a-126">다음 두 값이 있습니다:</span><span class="sxs-lookup"><span data-stu-id="4256a-126">Two values are available:</span></span>

- <span data-ttu-id="4256a-127">가격 재정의</span><span class="sxs-lookup"><span data-stu-id="4256a-127">Override pricing</span></span>  
- <span data-ttu-id="4256a-128">기본값 사용</span><span class="sxs-lookup"><span data-stu-id="4256a-128">Use default</span></span>

<span data-ttu-id="4256a-129">이 필드를 **가격 재정의** 로 설정하면 Dynamics 365가 기본 가격을 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="4256a-130">견적 행에 제품의 가격을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4256a-131">이 필드를 **기본값 사용** 으로 설정하면 Dynamics 365는 기본 판매 가격을 사용하고 필드를 잠궈 편집을 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="4256a-132">PSA를 설치하면 견적의 제품 기반 행에 기본 판매 가격이 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="4256a-133">그런 다음 견적 행에서 기본 가격을 편집할 수 있도록 **가격** 필드를 **가격 재정의** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![가격 재정의 설정](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="4256a-135">제품의 수량 계수</span><span class="sxs-lookup"><span data-stu-id="4256a-135">Quantity factors for products</span></span>

<span data-ttu-id="4256a-136">PSA는 수량 계수를 사용하여 신청 기반 제품의 판매를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4256a-137">신청 기반 제품의 경우 견적 또는 프로젝트 계약 행의 수량은 사용자 월 수로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="4256a-138">일반적으로 신청 소프트웨어의 가격은 월당 사용자당 가격으로 카탈로그에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4256a-139">그러나 그 대신 다른 시간 설명을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="4256a-140">영업 프로세스 중에 견적 행의 가격은 일반적으로 IT 영업 에이전트가 협상하고 할인한 월당 사용자당 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4256a-141">각 거래는 사용자 수가 다르고 가입 월 수가 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4256a-142">견적 행의 양을 계산하는 데 사용되는 수량은 사용자 수와 신청 월 수의 곱입니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4256a-143">이 타입의 판매를 지원하기 위해 PSA는 수량 계수라는 개념을 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="4256a-144">Dynamics 365에서 수량 계수는 제품 속성에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4256a-145">제품에 대한 특정 속성을 구성할 때 PSA를 사용하면 해당 속성의 하위 집합 또는 모든 속성에 수량 요소로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="4256a-146">PSA는 숫자 데이터 형식이 있는 숫자 속성 또는 제품 속성만 수량 계수로 플래그가 지정되어 있는지 검증합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4256a-147">수량 계수가 구성된 제품이 견적 행에 추가되면 견적 행의 **수량** 필드가 읽기 전용 필드가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="4256a-148">수량 계수인 제품 속성에 대한 값을 입력하면 PSA는 견적 행의 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="4256a-149">예컨대, Dynamics 365는 다음 속성을 가질 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="4256a-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="4256a-150">**사용자 수** - 사용자들의 수</span><span class="sxs-lookup"><span data-stu-id="4256a-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="4256a-151">**월 수** - 가입 월 수</span><span class="sxs-lookup"><span data-stu-id="4256a-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="4256a-152">**제품 SKU**</span><span class="sxs-lookup"><span data-stu-id="4256a-152">**Product SKU**</span></span> 

<span data-ttu-id="4256a-153">**사용자 수** 및 **월 수** 속성은 제품 행의 속성을 편집하여 수량 계수로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4256a-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![사용자 수 및 월 수를 품질 계수로 플래그 지정](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]