---
title: 제품
description: 이 항목은 조직에서 제공하는 제품 및 가격에 대한 정보를 고객에게 제공하는 데 사용할 수 있는 제품 카탈로그에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 606d44b64e5e1cd92ff3ab057a9cce408f972574
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277436"
---
# <a name="products"></a><span data-ttu-id="a099e-103">제품</span><span class="sxs-lookup"><span data-stu-id="a099e-103">Products</span></span>

<span data-ttu-id="a099e-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a099e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a099e-105">제품은 비즈니스의 핵심입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-105">Products are the backbone of your business.</span></span> <span data-ttu-id="a099e-106">Dynamics 365 Sales Professional의 제품 카탈로그는 제품 모음 및 가격 산정 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="a099e-107">영업 담당자가 제품 카탈로그를 신속하게 만들어 판매를 신장하기 쉽도록 해줍니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="a099e-108">제품 추가</span><span class="sxs-lookup"><span data-stu-id="a099e-108">Add a product</span></span>

1.  <span data-ttu-id="a099e-109">Dynamics 365 Sales Professional에서 제품을 추가할 수 있도록 Sales Professional 관리자 또는 시스템 관리자 역할이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="a099e-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="a099e-110">사이트 맵의 **설정** 에서 **제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="a099e-111">**제품 추가** 를 선택하고 다음 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="a099e-112">**이름**</span><span class="sxs-lookup"><span data-stu-id="a099e-112">**Name**</span></span>
    -  <span data-ttu-id="a099e-113">**제품 ID**</span><span class="sxs-lookup"><span data-stu-id="a099e-113">**Product ID**</span></span>
    -  <span data-ttu-id="a099e-114">**상위 항목**: 제품의 상위 제품군을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="a099e-115">제품군의 하위 제품을 생성하는 경우 상위 제품군의 이름이 여기 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="a099e-116">레코드가 저장된 이후에는 변경이 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="a099e-117">**유효 기간 시작**/**유효 기간 종료**: **유효 기간 시작** 및 **유효 기간 종료** 날짜를 선택하여 제품이 유효한 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="a099e-118">**단위 그룹**: 단위 그룹을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="a099e-119">단위 그룹은 제품이 판매되는 다양한 제품 단위의 모음이며 개별 항목을 더 큰 수량으로 그룹화하는 방법을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="a099e-120">예를 들어, 씨앗을 제품으로 추가하는 경우 "씨앗"이라고 하는 단위 그룹을 만들고 기본 단위를 "패킷"으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="a099e-121">**기본 단위**: 제품이 판매되는 가장 일반적인 단위를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="a099e-122">단위는 제품을 판매하는 수량 또는 규격입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="a099e-123">예를 들어, 씨앗을 제품으로 추가하는 경우 패킷, 상자 또는 팰릿에 넣어 판매할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="a099e-124">이러한 각 단위가 제품의 단위가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="a099e-125">시드가 주로 패킷으로 판매되는 경우 이것을 단위로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="a099e-126">**기본 가격표**: 새 제품의 경우 이 필드는 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="a099e-127">기본 가격표를 선택하려면 먼저 모든 필수 필드를 입력하고 레코드를 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="a099e-128">기본 가격표가 반드시 필요한 것은 아니지만 제품 레코드를 저장한 후에는 각 제품의 기본 가격표를 설정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="a099e-129">그러면 고객 레코드에 가격표가 없는 경우 Sales에서 견적, 주문 및 송장을 생성하는 데 기본 가격표가 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="a099e-130">**지원되는 소수 자릿수**: 0~5의 정수를 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="a099e-131">제품은 분수로 나뉘지 않는 경우 0을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="a099e-132">견적, 주문, 또는 송장 제품 레코드에서 **수량** 필드의 정확성은 제품이 연관된 가격 리스트를 갖고 있지 않은 경우 필드값에 대해 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="a099e-133">**주제**: 이 제품을 주제에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="a099e-134">주제를 통해 제품을 분류하고 보고서를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="a099e-135">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-135">Select **Save**.</span></span>
5.  <span data-ttu-id="a099e-136">**추가 세부 사항** 탭의 **가격표 항목** 섹션에서 **추가 명령** 을 선택한 다음 **새 가격표 항목 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="a099e-137">**추가 세부 사항** 탭의 **제품 관계** 섹션에서 **추가 명령** 아이콘을 선택한 다음 **새 제품 관계 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="a099e-138">**새 제품 관계** 양식에서 다음 세부 정보를 입력하고 명령 모음에서 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="a099e-139">**관련 제품**: 작업 중인 기존 제품 레코드에 관련 제품을 추가하려는 제품을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="a099e-140">**영업 관계 유형**: 상향 판매, 교차 판매, 보조 제품 또는 대체 제품으로 제품을 추가할지 여부를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="a099e-141">**방향**: 제품 간의 관계가 단방향 또는 양방향인지 여부를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="a099e-142">단방향을 선택하면 **관련 제품** 에서 선택하는 제품은 기존 제품의 권장 사항으로 표시되지만 그 반대는 해당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="a099e-143">제품 양식에서 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="a099e-144">제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="a099e-144">Import products</span></span>

<span data-ttu-id="a099e-145">가져오기 템플릿을 사용하여 대량 제품 데이터를 Dynamics 365 Sales Professional로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="a099e-146">제품 수정</span><span class="sxs-lookup"><span data-stu-id="a099e-146">Revise a product</span></span>

<span data-ttu-id="a099e-147">필요하면 제품의 속성을 신속하게 수정하고 정보를 다시 게시하여 제품 재고를 업데이트하므로 영업 상담원은 재고에 대한 최신 변경 내용을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="a099e-148">시스템 관리자, 시스템 사용자 지정자, 영업 관리자, 영업 부서장, 마케팅 부서장, CEO 비즈니스 관리자 중 하나의 보안 역할 또는 그와 동등한 권한이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="a099e-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="a099e-149">사이트 맵에서 **제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="a099e-150">수정을 원하는 활성화된 제품을 열어, 명령 모음에서 **수정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="a099e-151">**수정 확인** 대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="a099e-152">그러면 제품 상태가 **개정 중** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="a099e-153">변경이 끝나면 명령 모음에서 **게시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="a099e-154">변경 사항을 되돌리고 마지막 활성 버전의 제품으로 계속하려면 **되돌리기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="a099e-155">그러면 제품의 상태가 다시 **활성** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="a099e-156">제품 복제</span><span class="sxs-lookup"><span data-stu-id="a099e-156">Clone a product</span></span> 

<span data-ttu-id="a099e-157">새로운 제품을 만들 때 기존 것을 복제하여 시간을 절약합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="a099e-158">그러면 이름 및 ID를 제외하고 모든 정보가 있는 원래 레코드의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="a099e-159">시스템 관리자, 시스템 사용자 지정자, 영업 관리자, 영업 부서장, 마케팅 부서장, CEO 비즈니스 관리자 중 하나의 보안 역할 또는 그와 동등한 권한이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="a099e-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="a099e-160">사이트 맵에서 **제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="a099e-161">복제하려는 제품 레코드를 선택하고 명령 모음에서 **복제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="a099e-162">확인 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="a099e-163">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-163">Select **Confirm**.</span></span>

<span data-ttu-id="a099e-164">새 제품 레코드는 이름과 ID를 제외하고 원래 레코드와 동일한 정보로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="a099e-165">제품 사용 중지</span><span class="sxs-lookup"><span data-stu-id="a099e-165">Retire a product</span></span> 

<span data-ttu-id="a099e-166">조직이 제품을 더 이상 판매하지 않는 경우 영업 담당자가 제품을 더 이상 사용할 수 없도록 사용 중지시킵니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="a099e-167">시스템 관리자 또는 Sales Professional 관리자 역할이나 이와 동급의 권한이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="a099e-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="a099e-168">사이트 맵에서 **제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="a099e-169">사용 중지를 원하는 활성화된 제품을 열어, 명령 모음에서 **사용 중지** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="a099e-170">**중지 확인** 대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="a099e-171">제품 삭제</span><span class="sxs-lookup"><span data-stu-id="a099e-171">Delete a product</span></span>

<span data-ttu-id="a099e-172">제품 판매를 중지하려면 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a099e-173">삭제된 레코드는 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="a099e-174">시스템 관리자 또는 Sales Professional 관리자 역할이나 이와 동급의 권한이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="a099e-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="a099e-175">사이트 맵에서 **제품** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="a099e-176">삭제하려는 제품 레코드를 선택하고 명령 모음에서 **삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="a099e-177">**삭제 확인** 대화 상자에서 **계속** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="a099e-178">제품의 수량 계수</span><span class="sxs-lookup"><span data-stu-id="a099e-178">Quantity factors for products</span></span>

<span data-ttu-id="a099e-179">수량 계수는 신청 기반 제품의 판매를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="a099e-180">신청 기반 제품의 경우 견적 또는 프로젝트 계약 행의 수량은 사용자 월 수로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="a099e-181">일반적으로 신청 소프트웨어의 가격은 월당 사용자당 가격으로 카탈로그에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="a099e-182">그러나 그 대신 다른 시간 설명을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="a099e-183">영업 프로세스 중에 견적 행의 가격은 일반적으로 IT 영업 에이전트가 협상하고 할인한 월당 사용자당 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="a099e-184">각 거래는 사용자 수가 다르고 가입 월 수가 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="a099e-185">견적 행의 양을 계산하는 데 사용되는 수량은 사용자 수와 신청 월 수의 곱입니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="a099e-186">수량 계수는 제품 속성에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="a099e-187">제품에 대한 특정 속성을 구성할 때 해당 속성의 하위 집합 또는 모든 속성에 수량 요소로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="a099e-188">시스템은 숫자 데이터 형식이 있는 숫자 속성 또는 제품 속성만 수량 계수로 플래그가 지정되어 있는지 검증합니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="a099e-189">수량 계수가 구성된 제품이 견적 행에 추가되면 견적 행의 **수량** 필드가 읽기 전용 필드가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="a099e-190">수량 계수인 제품 속성에 대한 값을 입력하면 견적 행의 수량이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="a099e-191">예를 들어 다음 속성이 있는 경우:</span><span class="sxs-lookup"><span data-stu-id="a099e-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="a099e-192">**사용자 수**: 사용자들의 수</span><span class="sxs-lookup"><span data-stu-id="a099e-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="a099e-193">**월 수**: 가입 월 수</span><span class="sxs-lookup"><span data-stu-id="a099e-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="a099e-194">**제품 SKU**</span><span class="sxs-lookup"><span data-stu-id="a099e-194">**Product SKU**</span></span> 

<span data-ttu-id="a099e-195">**사용자 수** 및 **월 수** 속성은 제품 행의 속성을 편집하여 수량 계수로 플래그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a099e-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]