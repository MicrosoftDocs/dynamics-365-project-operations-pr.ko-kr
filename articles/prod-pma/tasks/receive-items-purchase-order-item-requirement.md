---
title: 품목 요구 사항에서 구매 주문에 대한 품목 수신
description: 이 항목은 품목 요구 사항에서 구매 주문서의 항목을 수신하는 방법을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080219"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="9a2ab-103">품목 요구 사항에서 구매 주문에 대한 품목 수신</span><span class="sxs-lookup"><span data-stu-id="9a2ab-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a2ab-104">이 항목은 품목 요구 사항에서 구매 주문서의 항목을 수신하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="9a2ab-105">품목 거래 대신 품목 소요량을 사용하면 품목이 실제로 사용되기 직전에 납품을 계획하고 구매 주문을 생성하고 거래 계약 프레임워크에 품목을 포함하고 생산 계획에 품목 소요량을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="9a2ab-106">이 작업은 USSI 데이터 집합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9a2ab-107">탐색 창에서 **모듈 > 프로젝트 관리 및 회계 > 프로젝트 > 모든 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="9a2ab-108">목록에서 원하는 행의 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="9a2ab-109">작업 창에서 **계획** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="9a2ab-110">**품목 요구 사항** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="9a2ab-111">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-111">Select **New**.</span></span>
6. <span data-ttu-id="9a2ab-112">새 행에서 **품목 번호** 필드에 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="9a2ab-113">**수량** 필드에 숫자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="9a2ab-114">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-114">Select **Save**.</span></span>
9. <span data-ttu-id="9a2ab-115">작업 창에서 **관리** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="9a2ab-116">**함수** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-116">Select **Functions**.</span></span>
11. <span data-ttu-id="9a2ab-117">**구매 주문 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="9a2ab-118">**모두 포함** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="9a2ab-119">**공급업체 계정** 필드에서 값을 입력하거나 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="9a2ab-120">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-120">Select **OK**.</span></span>
15. <span data-ttu-id="9a2ab-121">탐색 창에서 **모듈 > 지급 계정 > 구매 주문 > 모든 구매 주문** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="9a2ab-122">목록에서 원하는 행의 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="9a2ab-123">작업 창에서 **구매** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="9a2ab-124">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="9a2ab-125">작업 창에서 **수신** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="9a2ab-126">**제품 수령** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="9a2ab-127">**제품 수령** 필드에 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="9a2ab-128">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2ab-128">Select **OK**.</span></span>

