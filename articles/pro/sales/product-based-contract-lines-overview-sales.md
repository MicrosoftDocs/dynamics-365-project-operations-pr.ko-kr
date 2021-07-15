---
title: 제품 기반 계약 내용 개요 - 라이트
description: 이 항목은 제품 기반 계약 라인에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369744"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="7cb62-103">제품 기반 계약 내용 개요 - 라이트</span><span class="sxs-lookup"><span data-stu-id="7cb62-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="7cb62-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="7cb62-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7cb62-105">Dynamics 365 Project Operations에서 제품 기반 계약 내용을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="7cb62-106">제품 기반 계약 라인은 수동으로 생성된 라인이거나 제품 카탈로그의 항목일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="7cb62-107">제품 카탈로그</span><span class="sxs-lookup"><span data-stu-id="7cb62-107">Product catalog</span></span>

<span data-ttu-id="7cb62-108">제품 카탈로그의 제품은 기본 단위와 단위 그룹을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="7cb62-109">여러 제품이 동일한 속성 집합을 공유하는 경우 그러한 속성을 갖는 제품군을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="7cb62-110">한 제품군의 모든 제품은 동일한 속성 집합을 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="7cb62-111">예컨대, 어떤 회사가 다양한 소프트웨어에 대한 신청 라이선스를 판매합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="7cb62-112">모든 신청 소프트웨어는 다음 두 가지 속성을 갖습니다:</span><span class="sxs-lookup"><span data-stu-id="7cb62-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="7cb62-113">사용자 수</span><span class="sxs-lookup"><span data-stu-id="7cb62-113">Number of users</span></span>
- <span data-ttu-id="7cb62-114">가입 기간 (개월)</span><span class="sxs-lookup"><span data-stu-id="7cb62-114">Subscription duration (in months)</span></span>

<span data-ttu-id="7cb62-115">이러한 유형의 카탈로그를 유지하기 위해 **구독 소프트웨어** 라는 제품군을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="7cb62-116">속성 **사용자 수** 및 **구독 기간** 을 제품군에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="7cb62-117">그런 다음 개별 제품을 **구독 소프트웨어** 제품군에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="7cb62-118">프로젝트 계약에 제품 카탈로그 항목 추가</span><span class="sxs-lookup"><span data-stu-id="7cb62-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="7cb62-119">프로젝트 계약에는 프로젝트 기반 및 제품 기반의 두 가지 유형의 라인에 대한 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="7cb62-120">제품 기반 라인에는 계약의 제품 가격표에 있는 모든 제품 및 단위가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="7cb62-121">계약의 제품 가격표에 포함되지 않은 제품을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="7cb62-122">다른 가격표에서 제품을 선택하거나 제품 카탈로그에서 직접 제품을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="7cb62-123">제품 카탈로그에서 직접 제품을 선택하면 해당 제품의 기본 가격 목록이 제품의 판매 가격을 얻는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="7cb62-124">기본 가격 목록이 설정되지 않은 경우 가격은 0(제로)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="7cb62-125">계약 라인이 제품 카탈로그에 근거하는 경우 라인에서 직접 판매 가격을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="7cb62-126">계약 내용에는 두 값이 있는 **가격 책정** 필드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="7cb62-127">**가격 재정의**</span><span class="sxs-lookup"><span data-stu-id="7cb62-127">**Override pricing**</span></span>
- <span data-ttu-id="7cb62-128">**기본값 사용**</span><span class="sxs-lookup"><span data-stu-id="7cb62-128">**Use default**</span></span>

<span data-ttu-id="7cb62-129">**가격 책정** 필드를 **가격 재정의** 로 설정하면 기본 가격이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="7cb62-130">계약 내용의 제품에 대한 가격을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="7cb62-131">필드를 **기본값 사용** 으로 설정하는 경우 기본 판매 가격이 사용되며 필드를 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="7cb62-132">Project Operations를 설치하면 계약의 제품 기반 라인에 기본 판매 가격이 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="7cb62-133">계약 내용에서 기본 가격을 편집할 수 있도록 **가격 책정** 필드를 **가격 재정의** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="7cb62-134">이는 Dynamics 365 Sales의 제품 기반 라인 동작에 대한 Project Operations 관련 재정의입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb62-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]