---
title: 가격 책정 차원의 사용자 지정 필드 설정
description: 이 항목은 사용자 지정 필드를 사용하여 가격 책정 차원 설정 방법에 대한 정보를 제공합니다.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896604"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="a366d-103">가격 책정 차원의 사용자 지정 필드 설정</span><span class="sxs-lookup"><span data-stu-id="a366d-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="a366d-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a366d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a366d-105">시작하기 전에 이 항목은 귀하가 [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities-pricing-dimensions.md) 및 [가격 설정 및 트랜잭션 엔터티에 필수 맞춤 필드 추가](add-custom-fields-price-setup-transactional-entities.md) 항목의 절차를 완료했다고 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="a366d-106">이러한 절차를 완료하지 않은 경우 돌아가서 완료한 다음 이 항목으로 돌아오십시오.</span><span class="sxs-lookup"><span data-stu-id="a366d-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="a366d-107">이 항목은 맞춤 가격 책정 차원 설정에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="a366d-108">**매개 변수** 페이지의 **금액 기반 가격 책정 차원** 탭에는 가격 책정 차원 엔터티의 레코드가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="a366d-109">기본적으로 이 탭의 그리드에는 두 개의 행이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="a366d-110">**msdyn_resourcecategory** (역할)</span><span class="sxs-lookup"><span data-stu-id="a366d-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="a366d-111">**msdyn_OrganizationalUnit** (조직 단위)</span><span class="sxs-lookup"><span data-stu-id="a366d-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a366d-112">이러한 행을 삭제하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a366d-112">Do not delete these rows.</span></span> <span data-ttu-id="a366d-113">단, 필요하지 않은 경우, **비용에 적용 가능**, **판매에 적용 가능** 및 **구매에 적용 가능**을 모두 **아니오**로 설정함으로써 특정 상황에서 그것이 적용되지 않도록 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="a366d-114">이러한 속성 값을 **아니오**로 설정하면 필드가 가격 책정 차원으로 포함되지 않은 것과 같은 효과가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="a366d-115">필드가 가격 책정 차원이 되려면 다음이어야 합니다:</span><span class="sxs-lookup"><span data-stu-id="a366d-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="a366d-116">**역할 가격** 및 **역할 가격 인상** 엔터티의 필드로 만들어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="a366d-117">이렇게 하는 방법에 대한 상세 설명은 [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](add-custom-fields-price-setup-transactional-entities.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a366d-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>
- <span data-ttu-id="a366d-118">**가격 책정 차원** 표의 행으로 만들어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="a366d-119">예컨대 다음 그래픽과 같이 가격 책정 차원 행을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

<span data-ttu-id="a366d-120">리소스 작업 시간(**msdyn_resourceworkhours**)이 가격 인상 기반 차원으로 추가되었으며 **인상 기반 가격 책정 차원** 탭의 그리드에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-120">Resource Work hours (**msdyn_resourceworkhours**) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a366d-121">이 표에서 기존이든 신규이든 가격 책정 차원 데이터의 변경은 캐시를 새로 고친 후에만 가격 책정 비즈니스 논리에 전파됩니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-121">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="a366d-122">캐시 새로 고침 시간은 최대 10분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-122">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="a366d-123">이 기간을 허용하여 가격 책정 차원 데이터의 변경으로 인해 발생해야 하는 가격 기본 논리의 변경을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-123">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="a366d-124">가격 책정 차원 표의 속성</span><span class="sxs-lookup"><span data-stu-id="a366d-124">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="a366d-125">다음 섹션들은 **가격 책정 차원** 표의 다양한 속성에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-125">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="a366d-126">가격 책정 차원 명칭</span><span class="sxs-lookup"><span data-stu-id="a366d-126">Pricing Dimension Name</span></span>
<span data-ttu-id="a366d-127">이 값은 맞춤 가격 책정 차원에 대한 **역할 가격** 표에 추가되는 필드의 스키마 명칭과 정확히 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-127">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="a366d-128">**역할 가격** 표에 필드를 추가하는 자세한 방법은 [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](add-custom-fields-price-setup-transactional-entities.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a366d-128">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="a366d-129">차원 타입</span><span class="sxs-lookup"><span data-stu-id="a366d-129">Type of dimension</span></span>
<span data-ttu-id="a366d-130">다음 두 가지 타입의 가격 책정 차원이 있습니다:</span><span class="sxs-lookup"><span data-stu-id="a366d-130">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="a366d-131">**금액 기반 차원**: 입력 컨텍스트의 차원 값은 **역할 가격** 행의 차원 값과 일치하며 가격/비용은 **역할 가격** 표에서 직접 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-131">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="a366d-132">**가격 인상 기반 차원**: 가격/비용을 얻기 위해 다음과 같은 3단계 프로세스를 채택하는 차원이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-132">**Markup-based dimensions**: These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="a366d-133">입력 컨텍스트의 비마크업 기반 차원 값을 역할 가격 행에 짝지어 기본 요율을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-133">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="a366d-134">입력 컨텍스트의 모든 차원 값을 **역할 가격 마크업** 행에 짝지어 마크업 퍼센트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-134">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="a366d-135">첫 번째 단계의 **역할 가격** 표에서 얻은 기본 요율에 두 번째 단계의 마크업 백분율을 적용하여 최종 가격/비용에 도달합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-135">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="a366d-136">다음 표는 가격 마크업 계산을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-136">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="a366d-137">역할</span><span class="sxs-lookup"><span data-stu-id="a366d-137">Role</span></span>        | <span data-ttu-id="a366d-138">조직 단위</span><span class="sxs-lookup"><span data-stu-id="a366d-138">Org Unit</span></span>    |<span data-ttu-id="a366d-139">작업 위치</span><span class="sxs-lookup"><span data-stu-id="a366d-139">Work Location</span></span>      |<span data-ttu-id="a366d-140">표준 직함</span><span class="sxs-lookup"><span data-stu-id="a366d-140">Standard Title</span></span>      |<span data-ttu-id="a366d-141">리소스 작업 시간 수</span><span class="sxs-lookup"><span data-stu-id="a366d-141">Resource Work Hours</span></span>      |  <span data-ttu-id="a366d-142">마크업</span><span class="sxs-lookup"><span data-stu-id="a366d-142">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="a366d-143">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a366d-143">Contoso India</span></span>|<span data-ttu-id="a366d-144">현장</span><span class="sxs-lookup"><span data-stu-id="a366d-144">Onsite</span></span>            |                    |<span data-ttu-id="a366d-145">초과 근무</span><span class="sxs-lookup"><span data-stu-id="a366d-145">Overtime</span></span>                 |<span data-ttu-id="a366d-146">15</span><span class="sxs-lookup"><span data-stu-id="a366d-146">15</span></span>     |
|             | <span data-ttu-id="a366d-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a366d-147">Contoso India</span></span>|<span data-ttu-id="a366d-148">로컬</span><span class="sxs-lookup"><span data-stu-id="a366d-148">Local</span></span>             |                    |<span data-ttu-id="a366d-149">초과 근무</span><span class="sxs-lookup"><span data-stu-id="a366d-149">Overtime</span></span>                 |<span data-ttu-id="a366d-150">10</span><span class="sxs-lookup"><span data-stu-id="a366d-150">10</span></span>     |
|             | <span data-ttu-id="a366d-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a366d-151">Contoso US</span></span>   |<span data-ttu-id="a366d-152">로컬</span><span class="sxs-lookup"><span data-stu-id="a366d-152">Local</span></span>             |                    |<span data-ttu-id="a366d-153">초과 근무</span><span class="sxs-lookup"><span data-stu-id="a366d-153">Overtime</span></span>                 |<span data-ttu-id="a366d-154">20</span><span class="sxs-lookup"><span data-stu-id="a366d-154">20</span></span>     |


<span data-ttu-id="a366d-155">Contoso India에서 기본 요율이 100 USD인 어떤 리소스가 현장에서 작업중인데, 그가 시간 항목에서 정규 시간 8시간과 초과 근무 2시간을 기록하는 경우, 가격 책정 엔진은 8시간에 대해 100의 기본 요율을 사용하여 800 USD를 기록할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-155">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="a366d-156">2시간 초과 근무의 경우 기본 요율에 15%의 마크업이 적용되어 115 USD 단가를 얻고 총 230 USD의 비용을 기록할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-156">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="a366d-157">비용에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="a366d-157">Applicable to Cost</span></span> 
<span data-ttu-id="a366d-158">이것이 **예**로 설정되면 비용 및 마크업 비율을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업**과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-158">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="a366d-159">판매에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="a366d-159">Applicable to Sales</span></span>
<span data-ttu-id="a366d-160">이것이 **예**로 설정되면 청구 및 마크업 비율을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업**과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-160">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="a366d-161">구매에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="a366d-161">Applicable to Purchase</span></span>
<span data-ttu-id="a366d-162">이것이 **예**로 설정되면 구매 가격을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업**과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-162">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="a366d-163">하도급 시나리오는 지원되지 않으므로 이 필드는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-163">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="a366d-164">우선 순위</span><span class="sxs-lookup"><span data-stu-id="a366d-164">Priority</span></span>
<span data-ttu-id="a366d-165">차원 우선순위를 설정하면 가격 책정이 입력 차원 값과 **역할 가격** 또는 **역할 가격 마크업** 표의 값 사이에 정확히 일치하는 값을 찾을 수 없는 경우에도 가격을 생성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-165">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="a366d-166">이 시나리오에서 차원을 우선순위 순으로 가늠하여 불일치 차원 값에 null 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-166">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="a366d-167">**비용 우선순위**: 차원의 비용 우선순위 값은 비용 가격 설정과 일치할 때 해당 차원의 가중치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-167">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="a366d-168">**비용 우선순위**의 값은 **비용에 적용되는** 차원에 걸쳐 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-168">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="a366d-169">**판매 우선순위**: 차원의 판매 우선순위 값은 판매 가격 또는 청구 요율 설정과 일치할 때 해당 차원의 가중치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-169">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="a366d-170">**판매 우선순위**의 값은 **판매에 적용되는** 차원에 걸쳐 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a366d-170">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
