---
title: 제품 기반 견적 라인 개요 - 라이트
description: 이 항목은 제품 기반 견적 라인 작업에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178196"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="11cbe-103">제품 기반 견적 라인 개요 - 라이트</span><span class="sxs-lookup"><span data-stu-id="11cbe-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="11cbe-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="11cbe-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11cbe-105">Dynamics 365 Project Operations에서 제품 기반 견적 행을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="11cbe-106">제품 기반 견적 라인은 수동으로 추가할 수 있거나 제품 카탈로그의 항목일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="11cbe-107">제품 카탈로그</span><span class="sxs-lookup"><span data-stu-id="11cbe-107">Product catalog</span></span>

<span data-ttu-id="11cbe-108">제품 카탈로그의 각 제품에는 기본 단위 및 단위 그룹이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="11cbe-109">여러 제품이 동일한 속성 집합을 공유하는 경우 그러한 속성을 공유하는 제품군을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="11cbe-110">예컨대, 어떤 회사가 다양한 소프트웨어에 대한 신청 라이선스를 판매합니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="11cbe-111">모든 신청 소프트웨어는 다음 두 가지 속성을 갖습니다:</span><span class="sxs-lookup"><span data-stu-id="11cbe-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="11cbe-112">사용자 수</span><span class="sxs-lookup"><span data-stu-id="11cbe-112">Number of users</span></span>
- <span data-ttu-id="11cbe-113">개월 단위로 측정된 구독 기간</span><span class="sxs-lookup"><span data-stu-id="11cbe-113">A subscription duration measured in months</span></span>

<span data-ttu-id="11cbe-114">이러한 유형의 카탈로그를 유지하려면 **구독 소프트웨어** 라는 제품군을 만들고 사용자 수와 구독 기간을 속성으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="11cbe-115">그런 다음 개별 제품을 **구독 소프트웨어** 제품군에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="11cbe-116">프로젝트 견적에 제품 카탈로그 항목 추가</span><span class="sxs-lookup"><span data-stu-id="11cbe-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="11cbe-117">**프로젝트 견적** 및 **프로젝트 계약** 페이지는 프로젝트 기반 행과 제품 기반 행을 위한 섹션을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="11cbe-118">제품 기반 라인의 경우 견적 라인 또는 프로젝트 계약 내용의 드롭다운 목록에는 제품 가격표의 모든 제품과 단위가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="11cbe-119">제품 가격표에 속하지 않은 제품을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="11cbe-120">또한 다른 가격 목록에서 제품을 선택하거나 제품 카탈로그에서 직접 제품을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="11cbe-121">제품 카탈로그에서 직접 제품을 선택하면 해당 제품의 기본 가격 목록이 제품의 판매 가격을 얻는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="11cbe-122">기본 가격 목록이 설정되지 않은 경우 가격은 0(제로)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="11cbe-123">견적 행이 제품 카탈로그에 근거하는 경우 견적 행에서 직접 판매 가격을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="11cbe-124">두 개의 사용 가능한 값이 있는 **가격** 필드의 견적 라인:</span><span class="sxs-lookup"><span data-stu-id="11cbe-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="11cbe-125">**가격 재정의**</span><span class="sxs-lookup"><span data-stu-id="11cbe-125">**Override Pricing**</span></span>
- <span data-ttu-id="11cbe-126">**기본값 사용**</span><span class="sxs-lookup"><span data-stu-id="11cbe-126">**Use Default**</span></span>

<span data-ttu-id="11cbe-127">**가격 무시** 를 선택하면 기본 가격이 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="11cbe-128">대신 견적 라인에 제품의 가격을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="11cbe-129">**기본값 사용** 을 선택하면 기본 판매 가격이 사용되며 편집하지 못하도록 필드가 잠겨 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="11cbe-130">견적의 제품 기반 라인에 기본 판매 가격이 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="11cbe-131">그런 다음 견적 행에서 기본 가격을 편집할 수 있도록 **가격** 필드를 **가격 재정의** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="11cbe-132">이는 Dynamics 365 Sales의 제품 기반 라인 동작에 대한 Project Operations 관련 재정의입니다.</span><span class="sxs-lookup"><span data-stu-id="11cbe-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
