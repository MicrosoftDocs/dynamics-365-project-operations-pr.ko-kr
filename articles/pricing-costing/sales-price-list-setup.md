---
title: 판매 가격표 설정
description: 이 항목은 프로젝트 가격 책정을 위한 판매 가격표에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896469"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="60290-103">판매 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="60290-103">Sales price list setup</span></span>

<span data-ttu-id="60290-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="60290-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="60290-105">프로젝트 견적 및 계약의 경우 프로젝트 가격표는 제품 가격표와 다른 가격 재정의 패턴을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="60290-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="60290-106">제품 카탈로그 기반 견적 라인에서 각 견적 라인이 정확히 하나의 카탈로그 항목을 가리키므로 견적 라인에서 직접 역할 및 범주로 가격을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="60290-107">그러나 프로젝트 기반 견적 라인에서는 견적 라인에서 직접 역할 및 범주에 대한 가격을 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="60290-108">프로젝트 가격표를 사용하여 두 가지 다른 대체 패턴으로 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="60290-109">가격 책정을 재정의할 때 둘 사이의 동작 차이로 인해 프로젝트 리소스및 카탈로그 항목에 대해 별도의 가격표를 두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="60290-110">다음 각 엔터티에는 프로젝트 가격 책정에 대해 하나 이상의 관련 영업 가격표가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="60290-111">고객 (거래처)</span><span class="sxs-lookup"><span data-stu-id="60290-111">Customer (account)</span></span> 
- <span data-ttu-id="60290-112">영업 기회</span><span class="sxs-lookup"><span data-stu-id="60290-112">Opportunity</span></span> 
- <span data-ttu-id="60290-113">견적</span><span class="sxs-lookup"><span data-stu-id="60290-113">Quote</span></span> 
- <span data-ttu-id="60290-114">프로젝트 계약</span><span class="sxs-lookup"><span data-stu-id="60290-114">Project Contract</span></span>

<span data-ttu-id="60290-115">가격표와 이러한 엔터티의 연결은 프로젝트 가격표로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60290-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="60290-116">하나 이상의 가격표를 고객, 영업 기회, 견적 및 프로젝트 계약 판매 엔터티와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="60290-117">고객 레코드에 기본 프로젝트 가격표가 자동으로 입력되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="60290-118">그러나 프로젝트 가격표를 고객 레코드에 수동으로 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="60290-119">그럼에도 불구하고 고객과 사용자 지정 가격 책정 계약을 체결한 경우에만 프로젝트 가격표를 수동으로 첨부해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="60290-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="60290-120">프로젝트 가격표가 영업 엔터티에 첨부되면 다음 정보의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60290-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="60290-121">가격표에는 **영업**의 컨텍스트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="60290-122">가격표 통화는 고객 통화와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="60290-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="60290-123">프로젝트 계약에서 다음 우선 순위를 사용하여 관련 프로젝트 가격표를 자동으로 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="60290-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="60290-124">견적</span><span class="sxs-lookup"><span data-stu-id="60290-124">Quote</span></span>
2. <span data-ttu-id="60290-125">영업 기회</span><span class="sxs-lookup"><span data-stu-id="60290-125">Opportunity</span></span>
3. <span data-ttu-id="60290-126">고객</span><span class="sxs-lookup"><span data-stu-id="60290-126">Customer</span></span> 
4. <span data-ttu-id="60290-127">전역 설정</span><span class="sxs-lookup"><span data-stu-id="60290-127">Global settings</span></span> 

<span data-ttu-id="60290-128">기본적으로 프로젝트 가격표가 입력되면 시스템은 통화가 고객의 통화와 일치하는지, 입력된 기본 가격표에 **영업**의 컨텍스트가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="60290-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="60290-129">여러 프로젝트 가격표를 고객, 영업 기회, 견적 및 프로젝트 계약 엔터티와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="60290-130">이 기능은 장기 실행 프로젝트 계약에 대한 날짜별 기본 가격을 지원하며, 인플레이션으로 인해 발생하는 가격 업데이트를 설명하기 위해 두 개 이상의 가격표가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="60290-131">그러나 고객, 영업 기회, 견적 또는 프로젝트 계약 엔터티와 연결하는 가격표에 날짜 유효성이 겹치는 경우 기본 가격이 올바르지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60290-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="60290-132">따라서 날짜 유효성이 겹치는 프로젝트 가격표가 해당 엔터티와 연결되지 않았는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="60290-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
