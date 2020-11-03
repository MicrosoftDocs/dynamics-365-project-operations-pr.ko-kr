---
title: 프로젝트 구매 주문
description: 이 문서에서는 프로젝트에 대한 구매 주문을 생성하는 데 사용할 수 있는 다양한 방법에 대해 설명합니다. 사용하는 방법은 구매 주문의 목적과 구매한 항목이 소비되고 프로젝트에 청구되는 시기에 따라 다릅니다.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080040"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="555fc-104">프로젝트 구매 주문</span><span class="sxs-lookup"><span data-stu-id="555fc-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="555fc-105">이 문서에서는 프로젝트에 대한 구매 주문을 생성하는 데 사용할 수 있는 다양한 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="555fc-106">사용하는 방법은 구매 주문의 목적과 구매한 항목이 소비되고 프로젝트에 청구되는 시기에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="555fc-107">구매 주문 생성 방법</span><span class="sxs-lookup"><span data-stu-id="555fc-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="555fc-108">다음 방법 중 하나를 사용하여 프로젝트 관리 및 회계에서 구매 주문을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="555fc-109">구매 주문의 목적에 따라 구매 주문이 소비되는 시기와 항목이 프로젝트에 청구되는 시기가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="555fc-110">방법</span><span class="sxs-lookup"><span data-stu-id="555fc-110">Method</span></span></th>
<th><span data-ttu-id="555fc-111">용도</span><span class="sxs-lookup"><span data-stu-id="555fc-111">Purpose</span></span></th>
<th><span data-ttu-id="555fc-112">품목 소비</span><span class="sxs-lookup"><span data-stu-id="555fc-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="555fc-113">프로젝트에서 구매 주문을 직접 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="555fc-114">프로젝트에서 소비하기 위해 이 방법을 사용하여 외부 공급업체로부터 품목을 구매합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="555fc-115">두 가지 방법으로 구매 주문을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="555fc-116">프로젝트 자체에서.</span><span class="sxs-lookup"><span data-stu-id="555fc-116">From the project itself.</span></span> <span data-ttu-id="555fc-117">이 경우 프로젝트는 구매 주문에 대해 이미 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="555fc-118">프로젝트 구매 주문으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="555fc-119">구매 주문을 생성할 공급업체와 프로젝트를 모두 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="555fc-120">공급업체 송장이 업데이트되면 항목이 소비됩니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="555fc-121">판매 주문에서 구매 주문을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="555fc-122">이 방법을 사용하여 프로젝트에서 판매 주문을 생성할 때 품목을 구매합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="555fc-123">판매 주문이 고객에게 청구될 때 품목이 소비됩니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="555fc-124">품목 요구 사항에서 구매 주문을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="555fc-125">이 방법을 사용하여 프로젝트에서 품목 요구 사항을 생성할 때 품목을 구매합니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="555fc-126">품목 요구 사항 패킹 슬립이 업데이트될 때 품목이 소비됩니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="555fc-127">공급업체 송장 또는 패킹 슬립을 업데이트할 때 품목 요구 사항에 대한 패킹 슬립을 업데이트하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="555fc-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="555fc-128">자세한 내용은 [품목 요구 사항에서 구매 주문에 대한 품목 수령](tasks/receive-items-purchase-order-item-requirement.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="555fc-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

