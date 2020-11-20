---
title: 제품 기반 계약 내용의 복잡한 단위 관리 - 라이트
description: 이 항목은 구독 기반 제품 영업 지원에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177384"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="31fb6-103">제품 기반 계약 내용의 복잡한 단위 관리 - 라이트</span><span class="sxs-lookup"><span data-stu-id="31fb6-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="31fb6-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="31fb6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31fb6-105">Dynamics 365 Project Operations는 수량 계수를 사용하여 신청 기반 제품의 판매를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="31fb6-106">신청 기반 제품의 경우 계약 또는 프로젝트 계약 행의 수량은 사용자 월 수로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="31fb6-107">신청 소프트웨어의 가격은 월당 사용자당 가격으로 카탈로그에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="31fb6-108">영업 프로세스 중에 계약 내용의 가격은 일반적으로 IT 영업 에이전트가 협상하고 할인한 월당 사용자당 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="31fb6-109">각 거래는 사용자 수가 다르고 가입 월 수가 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="31fb6-110">계약 내용의 금액을 계산하는 데 사용되는 수량은 사용자 수와 신청 월 수의 곱입니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="31fb6-111">이 유형의 판매를 지원하기 위해 Project Operations는 *수량 계수* 라는 개념을 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="31fb6-112">수량 계수는 제품 속성에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="31fb6-113">제품에 대한 특정 속성을 구성할 때 해당 속성의 하위 집합 또는 모든 속성에 수량 요소로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="31fb6-114">Project Operations는 숫자 데이터 형식이 있는 숫자 속성 또는 제품 속성만 수량 계수로 플래그가 지정되어 있는지 검증합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="31fb6-115">수량 계수가 구성된 제품이 계약 내용에 추가되면 **수량** 필드가 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="31fb6-116">수량 계수인 제품 속성에 대한 값을 입력하면 Project Operations는 계약 내용의 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="31fb6-117">예컨대, Dynamics 365 Sales는 다음 속성을 가질 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="31fb6-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="31fb6-118">**사용자 수**: 사용자들의 수.</span><span class="sxs-lookup"><span data-stu-id="31fb6-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="31fb6-119">**월 수**: 가입 월 수.</span><span class="sxs-lookup"><span data-stu-id="31fb6-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="31fb6-120">**제품 SKU**: 상품의 재고 보관 단위(SKU)입니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="31fb6-121">**사용자 수** 및 **월 수** 속성은 제품 행의 속성을 편집하여 수량 계수로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="31fb6-122">제품 속성에서 수량 계수를 생성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="31fb6-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="31fb6-123">**Project Operations** 에서 **영업-제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="31fb6-124">수량 계수를 설정해야 하는 제품을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="31fb6-125">제품에 이미 설정된 속성이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="31fb6-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="31fb6-126">**프로젝트 정보** 페이지에서 **수량 계수** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="31fb6-127">하위 표에서 **+ 새 필드 계산** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="31fb6-128">**수량 계수** 의 이름을 입력하고 필드 계산에 매핑되는 속성 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="31fb6-129">양식을 저장하고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-129">Save and close the form.</span></span>
7. <span data-ttu-id="31fb6-130">제품 기반 계약 내용의 수량을 구성할 모든 속성에 대해 2-6단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="31fb6-131">수량 계수가 설정되면 사용자가 이 제품에 대한 계약 내용을 생성하면 계약 내용의 수량이 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="31fb6-132">그런 다음 수량은 해당 계약 내용에 대한 속성 값의 곱으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="31fb6-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
