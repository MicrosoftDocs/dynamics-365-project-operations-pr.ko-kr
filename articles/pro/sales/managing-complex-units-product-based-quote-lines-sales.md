---
title: 제품 기반 견적 라인에 대한 사용자별, 월별 등 복잡한 단위 관리
description: 이 항목에서는 제품 기반 견적 라인의 복잡한 단위 관리에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965831"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="1782b-103">제품 기반 견적 라인에 대한 사용자별, 월별 등 복잡한 단위 관리</span><span class="sxs-lookup"><span data-stu-id="1782b-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="1782b-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="1782b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1782b-105">Dynamics 365 Project Operations는 수량 계수를 사용하여 신청 기반 제품의 판매를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1782b-106">신청 기반 제품의 경우 견적 또는 프로젝트 계약 행의 수량은 사용자 월 수로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="1782b-107">일반적으로 신청 소프트웨어의 가격은 월당 사용자당 가격으로 카탈로그에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="1782b-108">영업 프로세스 중에 견적 행의 가격은 일반적으로 IT 영업 에이전트가 협상하고 할인한 월당 사용자당 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="1782b-109">각 거래는 사용자 수가 다르고 가입 월 수가 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1782b-110">견적 라인을 계산하는 데 사용되는 수량은 사용자 수와 신청 월 수의 곱입니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1782b-111">이 타입의 판매를 지원하기 위해 Project Operations는 수량 계수라는 개념을 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="1782b-112">Dynamics 365에서 수량 계수는 제품 속성에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="1782b-113">제품에 대한 특정 속성을 구성할 때 Project Operations를 사용하면 하위 집합 또는 모든 속성에 수량 요소로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="1782b-114">Project Operations는 숫자 데이터 형식이 있는 숫자 속성 또는 제품 속성만 수량 계수로 플래그가 지정되어 있는지 검증합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1782b-115">수량 계수가 있는 제품을 견적 라인에 추가하면 **수량** 필드가 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="1782b-116">수량 계수인 제품 속성에 대한 값을 입력하면 Project Operations는 견적 라인의 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="1782b-117">예컨대, Dynamics 365 Sales는 다음 속성을 가질 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="1782b-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="1782b-118">**사용자 수**: 사용자들의 수</span><span class="sxs-lookup"><span data-stu-id="1782b-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="1782b-119">**월 수**: 가입 월 수</span><span class="sxs-lookup"><span data-stu-id="1782b-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="1782b-120">**제품 SKU**</span><span class="sxs-lookup"><span data-stu-id="1782b-120">**Product SKU**</span></span>

<span data-ttu-id="1782b-121">**사용자 수** 및 **월 수** 속성은 제품 행의 속성을 편집하여 수량 계수로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="1782b-122">제품 속성에서 수량 계수를 생성하려면 다음 단계를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="1782b-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="1782b-123">Project Operations 왼쪽 탐색 창에서 **영업** > **제품**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="1782b-124">수량 계수를 구성해야 하는 제품을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="1782b-125">제품에 이미 구성된 속성이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="1782b-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="1782b-126">제품의 **프로젝트 정보** 페이지에서 **수량 계수** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="1782b-127">하위 표에서 **+ 새 필드 계산**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="1782b-128">수량 계수의 이름을 입력하고 필드 계산에 매핑되는 속성 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="1782b-129">양식을 저장하고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-129">Save and close the form.</span></span> <span data-ttu-id="1782b-130">제품 기반 견적 라인의 수량을 계산하는 데 사용할 모든 속성에 대해 이 단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="1782b-131">제품에 대한 제품 기반 견적 라인을 생성하면 견적 라인의 수량이 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="1782b-132">수량은 해당 견적 라인에 대해 입력한 속성 값의 곱으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="1782b-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
