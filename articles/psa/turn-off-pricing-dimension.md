---
title: 가격 책정 차원 끄기
description: 이 주제는 Project Service 솔루션에서 가격 책정 차원을 설정하는 방법을 보여줍니다.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014304"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="0e67f-103">가격 책정 차원 끄기</span><span class="sxs-lookup"><span data-stu-id="0e67f-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0e67f-104">몇 년마다 가격 책정 전략을 검토하고 업데이트해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="0e67f-105">업데이트를 통해 기존 가격 책정 차원을 해제하고 새 것을 만들어야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="0e67f-106">예컨대, 이전에는 **역할** 별로 가격이 책정되었을 수 있지만 이제 귀하는 **작업 경험** 별로 가격을 책정하기로 결정했습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="0e67f-107">이렇게 하려면 가격 책정 차원으로서의 **역할** 을 해제하고 새로운 가격 책정 차원으로서 **작업 경험** 을 만들어야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="0e67f-108">그것이 즉시 사용할 수 있는 것이든 또는 맞춤이든 관계없이, 가격 책정 차원의 **비용에 적용 가능** 및 **판매에 적용 가능** 필드를 **아니오** 로 설정함으로써 가격 책정 차원을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="0e67f-109">단, 그렇게 하면 다음 오류 메시지를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-109">However, when you do this, you might receive the following error message.</span></span>

![가격 책정 차원을 해제할 때 비즈니스 프로세스 오류 발생 가능성](media/Business-Process-Error.png)


<span data-ttu-id="0e67f-111">이 오류 메시지는 해제되는 차원에 대해 이전에 설정된 가격 레코드가 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="0e67f-112">차원에 준거하는 모든 **역할 가격** 및 **역할 가격 마크업** 레코드를 삭제해야 차원의 적용 가능성을 **아니오** 로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="0e67f-113">이 규칙은 즉시 사용 가능한 가격 책정 차원과 생성된 맞춤 가격 책정 차원 모두에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="0e67f-114">이 유효성 검사의 이유는 Project Service에 각 **역할 가격** 레코드는 차원들의 고유한 조합을 가져야 한다는 제약 조건이 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="0e67f-115">예컨대, **US Cost Rates 2018** 이라는 가격표에 다음 **역할 가격** 행이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="0e67f-116">표준 직함</span><span class="sxs-lookup"><span data-stu-id="0e67f-116">Standard Title</span></span>         | <span data-ttu-id="0e67f-117">조직 단위</span><span class="sxs-lookup"><span data-stu-id="0e67f-117">Org Unit</span></span>    |<span data-ttu-id="0e67f-118">단위</span><span class="sxs-lookup"><span data-stu-id="0e67f-118">Unit</span></span>   |<span data-ttu-id="0e67f-119">가격</span><span class="sxs-lookup"><span data-stu-id="0e67f-119">Price</span></span>  |<span data-ttu-id="0e67f-120">통화</span><span class="sxs-lookup"><span data-stu-id="0e67f-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="0e67f-121">시스템 엔지니어</span><span class="sxs-lookup"><span data-stu-id="0e67f-121">Systems Engineer</span></span>|<span data-ttu-id="0e67f-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0e67f-122">Contoso US</span></span>|<span data-ttu-id="0e67f-123">시간</span><span class="sxs-lookup"><span data-stu-id="0e67f-123">Hour</span></span>| <span data-ttu-id="0e67f-124">100</span><span class="sxs-lookup"><span data-stu-id="0e67f-124">100</span></span>|<span data-ttu-id="0e67f-125">USD</span><span class="sxs-lookup"><span data-stu-id="0e67f-125">USD</span></span>|
| <span data-ttu-id="0e67f-126">선임 시스템 엔지니어</span><span class="sxs-lookup"><span data-stu-id="0e67f-126">Senior Systems Engineer</span></span>|<span data-ttu-id="0e67f-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0e67f-127">Contoso US</span></span>|<span data-ttu-id="0e67f-128">시간</span><span class="sxs-lookup"><span data-stu-id="0e67f-128">Hour</span></span>| <span data-ttu-id="0e67f-129">150</span><span class="sxs-lookup"><span data-stu-id="0e67f-129">150</span></span>| <span data-ttu-id="0e67f-130">USD</span><span class="sxs-lookup"><span data-stu-id="0e67f-130">USD</span></span>|


<span data-ttu-id="0e67f-131">가격 책정 차원으로서의 **표준 직함** 을 끄고 Project Service 가격 책정 엔진이 가격을 검색하면 입력 컨텍스트에서 **조직 단위** 값만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="0e67f-132">입력 컨텍스트의 **조직 단위** 가 "Contoso US"인 경우 두 행이 모두 일치하므로 결과가 결정적이지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="0e67f-133">이 시나리오를 피하기 위해 **역할 가격** 레코드를 만들 때 Project Service는 차원의 조합이 고유한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="0e67f-134">**역할 가격** 레코드를 만든 후 차원을 해제하면 이 제약 조건을 위반할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="0e67f-135">따라서 차원을 끄기 전에, 해당 차원 값이 채워진 모든 **역할 가격** 및 **역할 가격 마크업** 행을 삭제할 것이 요구됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e67f-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]