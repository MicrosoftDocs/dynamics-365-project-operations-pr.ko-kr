---
title: 가격 책정 차원의 사용자 지정 필드 설정
description: 이 항목은 맞춤 가격 책정 차원 설정에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150361"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="52740-103">가격 책정 차원의 사용자 지정 필드 설정</span><span class="sxs-lookup"><span data-stu-id="52740-103">Setting up custom fields as pricing dimensions</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52740-104">시작하기 전에 이 항목은 귀하가 [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities.md) 및 [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](field-references.md) 항목의 절차를 완료했다고 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="52740-105">이러한 절차를 완료하지 않은 경우 돌아가서 완료한 다음 이 항목으로 돌아오십시오.</span><span class="sxs-lookup"><span data-stu-id="52740-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="52740-106">이 항목은 맞춤 가격 책정 차원 설정에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="52740-107">Project Service 웹 인터페이스에서 **파라미터** 페이지의 **금액 기반 가격 책정 차원** 탭은 가격 책정 차원 엔터티의 레코드를 보여줌을 인식하십시오.</span><span class="sxs-lookup"><span data-stu-id="52740-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="52740-108">기본적으로 Project Service 설치는 이 탭의 그리드에 2개의 행을 만듭니다:</span><span class="sxs-lookup"><span data-stu-id="52740-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="52740-109">**msdyn_resourcecategory** (역할)</span><span class="sxs-lookup"><span data-stu-id="52740-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="52740-110">**msdyn_OrganizationalUnit** (조직 단위)</span><span class="sxs-lookup"><span data-stu-id="52740-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52740-111">이러한 행을 삭제하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="52740-111">Do not delete these rows.</span></span> <span data-ttu-id="52740-112">단, 필요하지 않은 경우, **비용에 적용 가능**, **판매에 적용 가능** 및 **구매에 적용 가능** 을 모두 **아니오** 로 설정함으로써 특정 상황에서 그것이 적용되지 않도록 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="52740-113">이러한 속성 값을 **아니오** 로 설정하면 필드가 가격 책정 차원으로 포함되지 않은 것과 같은 효과가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="52740-114">필드가 가격 책정 차원이 되려면 다음이어야 합니다:</span><span class="sxs-lookup"><span data-stu-id="52740-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="52740-115">**역할 가격** 및 **역할 가격 인상** 엔터티의 필드로 만들어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="52740-116">이렇게 하는 방법에 대한 상세 설명은 [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](field-references.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="52740-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="52740-117">**가격 책정 차원** 표의 행으로 만들어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="52740-118">예컨대 다음 그래픽과 같이 가격 책정 차원 행을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![금액 기반 가격 책정 차원 행](media/Amt-based-PD.png)

<span data-ttu-id="52740-120">리소스 작업 시간(**msdyn_resourceworkhours**)이 가격 인상 기반 차원으로 추가되었으며 **인상 기반 가격 책정 차원** 탭의 그리드에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![인상 기반 가격 책정 차원 행](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="52740-122">이 표에서 기존이든 신규이든 가격 책정 차원 데이터의 변경은 캐시를 새로 고친 후에만 Project Service 가격 책정 비즈니스 논리에 전파됩니다.</span><span class="sxs-lookup"><span data-stu-id="52740-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="52740-123">캐시 새로 고침 시간은 최대 10분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="52740-124">이 기간을 허용하여 가격 책정 차원 데이터의 변경으로 인해 발생해야 하는 가격 기본 논리의 변경을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="52740-125">가격 책정 차원 표의 속성</span><span class="sxs-lookup"><span data-stu-id="52740-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="52740-126">다음 섹션들은 **가격 책정 차원** 표의 다양한 속성에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="52740-127">가격 책정 차원 명칭</span><span class="sxs-lookup"><span data-stu-id="52740-127">Pricing Dimension Name</span></span>
<span data-ttu-id="52740-128">이 값은 맞춤 가격 책정 차원에 대한 **역할 가격** 표에 추가되는 필드의 스키마 명칭과 정확히 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="52740-129">**역할 가격** 표에 필드를 추가하는 자세한 방법은 [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](field-references.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="52740-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="52740-130">차원 타입</span><span class="sxs-lookup"><span data-stu-id="52740-130">Type of dimension</span></span>
<span data-ttu-id="52740-131">다음 두 가지 타입의 가격 책정 차원이 있습니다:</span><span class="sxs-lookup"><span data-stu-id="52740-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="52740-132">**금액 기반 차원**: 입력 컨텍스트의 차원 값은 **역할 가격** 행의 차원 값과 일치하며 가격/비용은 **역할 가격** 표에서 직접 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52740-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="52740-133">**가격 인상 기반 차원**: 가격/비용을 얻기 위해 Project Service가 다음과 같은 3단계 프로세스를 채택하는 차원입니다.</span><span class="sxs-lookup"><span data-stu-id="52740-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="52740-134">Project Service가 입력 컨텍스트의 비마크업 기반 차원 값을 역할 가격 행에 짝지어 기본 요율을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="52740-135">Project Service가 입력 컨텍스트의 모든 차원 값을 **역할 가격 마크업** 행에 짝지어 마크업 퍼센트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="52740-136">Project Service가 첫 번째 단계의 **역할 가격** 표에서 얻은 기본 요율에 두 번째 단계의 마크업 백분율을 적용하여 최종 가격/비용에 도달합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="52740-137">다음 표는 가격 마크업 계산을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="52740-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="52740-138">역할</span><span class="sxs-lookup"><span data-stu-id="52740-138">Role</span></span>        | <span data-ttu-id="52740-139">조직 단위</span><span class="sxs-lookup"><span data-stu-id="52740-139">Org Unit</span></span>    |<span data-ttu-id="52740-140">작업 위치</span><span class="sxs-lookup"><span data-stu-id="52740-140">Work Location</span></span>      |<span data-ttu-id="52740-141">표준 직함</span><span class="sxs-lookup"><span data-stu-id="52740-141">Standard Title</span></span>      |<span data-ttu-id="52740-142">리소스 작업 시간 수</span><span class="sxs-lookup"><span data-stu-id="52740-142">Resource Work Hours</span></span>      |  <span data-ttu-id="52740-143">마크업</span><span class="sxs-lookup"><span data-stu-id="52740-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="52740-144">Contoso India</span><span class="sxs-lookup"><span data-stu-id="52740-144">Contoso India</span></span>|<span data-ttu-id="52740-145">현장</span><span class="sxs-lookup"><span data-stu-id="52740-145">Onsite</span></span>            |                    |<span data-ttu-id="52740-146">초과 근무</span><span class="sxs-lookup"><span data-stu-id="52740-146">Overtime</span></span>                 |<span data-ttu-id="52740-147">15</span><span class="sxs-lookup"><span data-stu-id="52740-147">15</span></span>     |
|             | <span data-ttu-id="52740-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="52740-148">Contoso India</span></span>|<span data-ttu-id="52740-149">로컬</span><span class="sxs-lookup"><span data-stu-id="52740-149">Local</span></span>             |                    |<span data-ttu-id="52740-150">초과 근무</span><span class="sxs-lookup"><span data-stu-id="52740-150">Overtime</span></span>                 |<span data-ttu-id="52740-151">10</span><span class="sxs-lookup"><span data-stu-id="52740-151">10</span></span>     |
|             | <span data-ttu-id="52740-152">Contoso US</span><span class="sxs-lookup"><span data-stu-id="52740-152">Contoso US</span></span>   |<span data-ttu-id="52740-153">로컬</span><span class="sxs-lookup"><span data-stu-id="52740-153">Local</span></span>             |                    |<span data-ttu-id="52740-154">초과 근무</span><span class="sxs-lookup"><span data-stu-id="52740-154">Overtime</span></span>                 |<span data-ttu-id="52740-155">20</span><span class="sxs-lookup"><span data-stu-id="52740-155">20</span></span>     |


<span data-ttu-id="52740-156">Contoso India에서 기본 요율이 100 USD인 어떤 리소스가 현장에서 작업중인데, 그가 시간 항목에서 정규 시간 8시간과 초과 근무 2시간을 기록하는 경우, Project Service 가격 책정 엔진은 8시간에 대해 100의 기본 요율을 사용하여 800 USD를 기록할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="52740-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="52740-157">2시간 초과 근무의 경우 기본 요율에 15%의 마크업이 적용되어 115 USD 단가를 얻고 총 230 USD의 비용을 기록할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="52740-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="52740-158">비용에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="52740-158">Applicable to Cost</span></span> 
<span data-ttu-id="52740-159">이것이 **예** 로 설정되면 비용 및 마크업 비율을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업** 과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="52740-160">판매에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="52740-160">Applicable to Sales</span></span>
<span data-ttu-id="52740-161">이것이 **예** 로 설정되면 청구 및 마크업 비율을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업** 과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="52740-162">구매에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="52740-162">Applicable to Purchase</span></span>
<span data-ttu-id="52740-163">이것이 **예** 로 설정되면 구매 가격을 검색할 때 입력 컨텍스트의 차원 값을 사용하여 **역할 가격** 및 **역할 가격 마크업** 과 일치하도록 해야 함을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="52740-164">현재 Project Service는 하청 시나리오를 지원하지 않으므로 이 필드는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52740-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="52740-165">우선 순위</span><span class="sxs-lookup"><span data-stu-id="52740-165">Priority</span></span>
<span data-ttu-id="52740-166">차원 우선순위를 설정하면 Project Service 가격 책정이 입력 차원 값과 **역할 가격** 또는 **역할 가격 마크업** 표의 값 사이에 정확히 일치하는 값을 찾을 수 없는 경우에도 가격을 생성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52740-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="52740-167">이 시나리오에서 Project Service는 차원을 우선순위 순으로 가늠하여 불일치 차원 값에 null 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="52740-168">**비용 우선순위**: 차원의 비용 우선순위 값은 비용 가격 설정과 일치할 때 해당 차원의 가중치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="52740-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="52740-169">**비용 우선순위** 의 값은 **비용에 적용되는** 차원에 걸쳐 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="52740-170">**판매 우선순위**: 차원의 판매 우선순위 값은 판매 가격 또는 청구 요율 설정과 일치할 때 해당 차원의 가중치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="52740-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="52740-171">**판매 우선순위** 의 값은 **판매에 적용되는** 차원에 걸쳐 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52740-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
