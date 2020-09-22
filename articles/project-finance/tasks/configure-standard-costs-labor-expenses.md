---
title: 인건비 및 비용에 대한 표준 비용 구성
description: 이 항목은 프로젝트의 인건비 및 비용에 대한 표준 비용을 설정하는 방법을 설명합니다.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753367"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f0f3c-103">인건비 및 비용에 대한 표준 비용 구성</span><span class="sxs-lookup"><span data-stu-id="f0f3c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0f3c-104">이 항목은 프로젝트의 인건비 및 비용에 대한 표준 비용을 설정하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f0f3c-105">이 작업은 USSI 데이터 집합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f0f3c-106">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 원가(시간)** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="f0f3c-107">**새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-107">Select **New**.</span></span>
3. <span data-ttu-id="f0f3c-108">**유효 날짜** 필드에 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="f0f3c-109">**원가** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f0f3c-110">프로젝트 범주에 대한 표준 원가를 설정하거나 작업자 번호, 프로젝트 번호, 범주, 날짜 또는 이들의 조합으로 원가를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f0f3c-111">적용되는 원가는 세부 수준이 가장 높은 원가입니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f0f3c-112">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-112">Select **Save**.</span></span>
6. <span data-ttu-id="f0f3c-113">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 판매 가격(시간)** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="f0f3c-114">**새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-114">Select **New**.</span></span>
8. <span data-ttu-id="f0f3c-115">**유효 날짜** 필드에 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="f0f3c-116">**유효 기간** 필드에서 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="f0f3c-117">**가격 책정** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f0f3c-118">시간 거래 또는 프로젝트 범주에 대한 표준 판매 가격을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f0f3c-119">작업자 번호, 프로젝트 번호, 범주, 트랜잭션 날짜 또는 이들의 조합으로 판매 가격을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f0f3c-120">작업자가 시간 저널에 트랜잭션을 입력할 때 적용되는 실제 판매 가격은 세부 수준이 가장 높은 판매 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f0f3c-121">예를 들어 일반 판매 가격과 작업자별 판매 가격이 모두 설정된 경우 작업자별 판매 가격이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="f0f3c-122">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-122">Select **Save**.</span></span>
12. <span data-ttu-id="f0f3c-123">창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-123">Close the page.</span></span>
13. <span data-ttu-id="f0f3c-124">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 원가(경비)** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="f0f3c-125">**새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-125">Select **New**.</span></span>
15. <span data-ttu-id="f0f3c-126">**유효 날짜** 필드에 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="f0f3c-127">**원가** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f0f3c-128">여러 필드를 채울 수 있지만 이는 레코드를 저장하는 데 필요한 최소값입니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="f0f3c-129">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-129">Select **Save**.</span></span>
18. <span data-ttu-id="f0f3c-130">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 판매 가격(경비)** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="f0f3c-131">**새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-131">Select **New**.</span></span>
20. <span data-ttu-id="f0f3c-132">**유효 날짜** 필드에 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="f0f3c-133">**유효 기간** 필드에서 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="f0f3c-134">**가격 책정** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f0f3c-135">작업자가 경비 저널에 트랜잭션을 입력할 때 적용되는 실제 판매 가격은 세부 수준이 가장 높은 판매 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f0f3c-136">예를 들어 일반 및 작업자별 판매 가격이 모두 설정된 경우 작업자별 판매 가격이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="f0f3c-137">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f0f3c-137">Select **Save**.</span></span>

