---
title: 회사 간 프로젝트 송장 구성
description: 이 항목은 조직의 두 회사 간에 프로젝트 송장을 설정하는 방법을 보여줍니다.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080111"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="fe097-103">회사 간 프로젝트 송장 구성</span><span class="sxs-lookup"><span data-stu-id="fe097-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe097-104">이 항목은 조직의 두 회사 간에 프로젝트 송장을 설정하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="fe097-105">이 작업은 USSI 데이터 집합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="fe097-106">탐색 창에서 **모듈 > 지급 계정 > 공급업체 > 모든 공급업체** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="fe097-107">**모든 공급업체** 목록에서 원하는 레코드를 찾아 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="fe097-108">작업 창에서 **일반** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="fe097-109">**회사 간** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="fe097-110">**활성화** 를 **예** 로 설정하여 회사 간 거래를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="fe097-111">**고객 회사** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="fe097-112">**내 계정** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="fe097-113">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-113">Select **Save**.</span></span>
9. <span data-ttu-id="fe097-114">홈 페이지로 돌아가려면 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="fe097-115">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 프로젝트 관리 및 회계 매개 변수** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="fe097-116">**회사 간** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="fe097-117">슬라이더를 **예** 로 이동하여 회사 간 리소스 일정 및 작업 표를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="fe097-118">목록에서 선택한 행을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="fe097-119">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-119">Select **New**.</span></span>
15. <span data-ttu-id="fe097-120">**차용 법인** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="fe097-121">**수익 발생** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="fe097-122">**기본 작업 표 범주** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="fe097-123">**기본 경비 범주** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="fe097-124">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-124">Select **Save**.</span></span>
20. <span data-ttu-id="fe097-125">창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-125">Close the page.</span></span>
21. <span data-ttu-id="fe097-126">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 전기 > 원장 전기 설정** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="fe097-127">**원장 계정 유형** 필드에서 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="fe097-128">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-128">Select **New**.</span></span>
24. <span data-ttu-id="fe097-129">새 행의 **주요 계정** 필드에서 원하는 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="fe097-130">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-130">Select **Save**.</span></span>
26. <span data-ttu-id="fe097-131">창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-131">Close the page.</span></span>
27. <span data-ttu-id="fe097-132">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 설정 > 가격 > 이전 가격** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="fe097-133">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-133">Select **New**.</span></span>
29. <span data-ttu-id="fe097-134">**유효 날짜** 필드에 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="fe097-135">**차용 법인** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="fe097-136">**이전 가격 모델** 필드에서 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="fe097-137">**가격 책정** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="fe097-138">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fe097-138">Select **Save**.</span></span>

