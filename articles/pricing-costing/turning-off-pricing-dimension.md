---
title: 가격 책정 차원 끄기
description: 이 항목은 가격 책정 차원을 끄는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080148"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="4162b-103">가격 책정 차원 끄기</span><span class="sxs-lookup"><span data-stu-id="4162b-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="4162b-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="4162b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4162b-105">몇 년마다 가격 책정 전략을 검토하고 업데이트해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="4162b-106">업데이트를 통해 기존 가격 책정 차원을 해제하고 새 것을 만들어야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="4162b-107">예컨대, 이전에는 **역할** 별로 가격이 책정되었을 수 있지만 이제 귀하는 **작업 경험** 별로 가격을 책정하기로 결정했습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-107">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="4162b-108">이렇게 하려면 가격 책정 차원으로서의 **역할** 을 해제하고 새로운 가격 책정 차원으로서 **작업 경험** 을 만들어야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="4162b-109">그것이 즉시 사용할 수 있는 것이든 또는 맞춤이든 관계없이, 가격 책정 차원의 **비용에 적용 가능** 및 **판매에 적용 가능** 필드를 **아니오** 로 설정함으로써 가격 책정 차원을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="4162b-110">그러나 이렇게 하면 **연관된 가격 레코드가 있는 경우 가격 책정 차원을 업데이트하거나 삭제할 수 없습니다.** 오류 메시지가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="4162b-111">이 오류 메시지는 해제되는 차원에 대해 이전에 설정된 가격 레코드가 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="4162b-112">차원에 준거하는 모든 **역할 가격** 및 **역할 가격 마크업** 레코드를 삭제해야 차원의 적용 가능성을 **아니오** 로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="4162b-113">이 규칙은 즉시 사용 가능한 가격 책정 차원과 생성된 맞춤 가격 책정 차원 모두에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="4162b-114">이 유효성 검사의 이유는 각 **역할 가격** 레코드는 차원들의 고유한 조합을 가져야 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="4162b-115">예컨대, **US Cost Rates 2018** 이라는 가격표에 다음 **역할 가격** 행이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="4162b-116">표준 직함</span><span class="sxs-lookup"><span data-stu-id="4162b-116">Standard Title</span></span>         | <span data-ttu-id="4162b-117">조직 단위</span><span class="sxs-lookup"><span data-stu-id="4162b-117">Org Unit</span></span>    |<span data-ttu-id="4162b-118">단위</span><span class="sxs-lookup"><span data-stu-id="4162b-118">Unit</span></span>   |<span data-ttu-id="4162b-119">가격</span><span class="sxs-lookup"><span data-stu-id="4162b-119">Price</span></span>  |<span data-ttu-id="4162b-120">통화</span><span class="sxs-lookup"><span data-stu-id="4162b-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="4162b-121">시스템 엔지니어</span><span class="sxs-lookup"><span data-stu-id="4162b-121">Systems Engineer</span></span>|<span data-ttu-id="4162b-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4162b-122">Contoso US</span></span>|<span data-ttu-id="4162b-123">Hour</span><span class="sxs-lookup"><span data-stu-id="4162b-123">Hour</span></span>| <span data-ttu-id="4162b-124">100</span><span class="sxs-lookup"><span data-stu-id="4162b-124">100</span></span>|<span data-ttu-id="4162b-125">USD</span><span class="sxs-lookup"><span data-stu-id="4162b-125">USD</span></span>|
| <span data-ttu-id="4162b-126">선임 시스템 엔지니어</span><span class="sxs-lookup"><span data-stu-id="4162b-126">Senior Systems Engineer</span></span>|<span data-ttu-id="4162b-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4162b-127">Contoso US</span></span>|<span data-ttu-id="4162b-128">Hour</span><span class="sxs-lookup"><span data-stu-id="4162b-128">Hour</span></span>| <span data-ttu-id="4162b-129">150</span><span class="sxs-lookup"><span data-stu-id="4162b-129">150</span></span>| <span data-ttu-id="4162b-130">USD</span><span class="sxs-lookup"><span data-stu-id="4162b-130">USD</span></span>|


<span data-ttu-id="4162b-131">가격 책정 차원으로서의 **표준 직함** 을 끄고 가격 책정 엔진이 가격을 검색하면 입력 컨텍스트에서 **조직 단위** 값만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="4162b-132">입력 컨텍스트의 **조직 단위** 가 "Contoso US"인 경우 두 행이 모두 일치하므로 결과가 결정적이지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="4162b-133">이 시나리오를 피하기 위해 **역할 가격** 레코드를 만들 때 시스템은 차원의 조합이 고유한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="4162b-134">**역할 가격** 레코드를 만든 후 차원을 해제하면 이 제약 조건을 위반할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="4162b-135">따라서 차원을 끄기 전에, 해당 차원 값이 채워진 모든 **역할 가격** 및 **역할 가격 마크업** 행을 삭제할 것이 요구됩니다.</span><span class="sxs-lookup"><span data-stu-id="4162b-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
