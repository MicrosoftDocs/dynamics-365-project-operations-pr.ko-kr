---
title: 가격 및 원가 차원 홈 페이지
description: 이 항목은 가격 차원에 대한 개요를 제공합니다.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080093"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="5e3a6-103">가격 및 원가 차원 홈 페이지</span><span class="sxs-lookup"><span data-stu-id="5e3a6-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="5e3a6-104">프로젝트 기반 조직에서 인건비 가격 및 비용을 설정하는 데 사용되는 차원은 다음 속성의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="5e3a6-105">자신의 경험, 역할 또는 지리와 유사한 일을 하는 사람들</span><span class="sxs-lookup"><span data-stu-id="5e3a6-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="5e3a6-106">복잡성 또는 시간과 유사하게 수행할 작업</span><span class="sxs-lookup"><span data-stu-id="5e3a6-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="5e3a6-107">작업의 이러한 속성과 작업을 수행하는 데 필요한 사람의 일반적인 특성을 고려할 때 Project Service Automation에서 사용할 수 있는 두 가지 유형의 가격 책정 차원 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="5e3a6-108">**옵션 집합** - 값 집합에 대해 고정된 열거형인 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="5e3a6-109">**엔터티 기반 값** - 유한하지만 시간이 지남에 따라 변경될 수 있는 다양한 값 집합을 가질 수 있는 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="5e3a6-110">가격 책정 차원</span><span class="sxs-lookup"><span data-stu-id="5e3a6-110">Pricing dimensions</span></span>

<span data-ttu-id="5e3a6-111">PSA는 기본 가격 차원 집합으로 배송됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="5e3a6-112">이러한 것을 **Project Service** > **파라미터** 로 이동하여 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="5e3a6-113">파라미터 레코드에서 **금액 기반 가격 책정 차원** 탭에서 역할, **msdyn_resourcecategory** 및 리소싱 조직 단위, **msdyn_organizationalunit** 의 필드 **매출액에 해당** 및 **원가에 해당** 이 **예** 로 설정되어 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="5e3a6-114">이렇게 하면 각 역할 및 조직 단위 조합에 대한 가격과 원가를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

!["매출액에 해당"이 강조 표시된 Project Service 파라미터의 스크린샷](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="5e3a6-116">PSA 버전 3 이전에 역할 및 조직 단위의 즉시 사용 필드가 가격 차원으로 사용된 경우 관찰 가능한 변경 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="5e3a6-117">평소와 같이 Project Service를 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="5e3a6-118">추가 속성을 사용하는 리소스에 대한 가격 또는 원가가 필요한 경우 맞춤화된 필드, 엔터티 및 차원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="5e3a6-119">자세한 내용은 다음 항목을 참조하지만 아래 나열된 순서대로 절차를 완료해야 합니다:</span><span class="sxs-lookup"><span data-stu-id="5e3a6-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="5e3a6-120">맞춤 필드 및 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="5e3a6-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="5e3a6-121">가격 설정 및 처리 엔터티에 맞춤 필드 추가</span><span class="sxs-lookup"><span data-stu-id="5e3a6-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="5e3a6-122">가격 책정 차원의 사용자 지정 필드 설정</span><span class="sxs-lookup"><span data-stu-id="5e3a6-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="5e3a6-123">새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5e3a6-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="5e3a6-124">인적 자원 시간 가격 책정</span><span class="sxs-lookup"><span data-stu-id="5e3a6-124">Pricing human resource time</span></span>
<span data-ttu-id="5e3a6-125">조직이 인적 자원 시간을 어떻게 책정하는지는 종종 조직의 수익성에 직접적인 영향을 미치는 중요한 전략적 고려 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="5e3a6-126">귀하의 조직이 인적 자원 시간을 위한 청구서 및 원가 요율을 설정하는 방법을 파악할 준비가 되면 재무팀 및 실무 책임자들과 협력하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="5e3a6-127">가격 책정에 대한 다른 고려 사항으로는 현재 가격 책정 차원이 아니지만 조직의 가격 책정 차원으로 적용되는 필드 또는 엔터티를 다시 사용할지 여부가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="5e3a6-128">**처리 카테고리** ( **msdyn_transactioncategory** ) 및 **예약 가능한 리소스** ( **bookableresource** ) 같은 필드는 후보 차원의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="5e3a6-129">가격 책정 차원이 표여야 하는지 옵션 집합이어야 하는지도 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="5e3a6-130">10 또는 12를 초과하는 차원값의 변경을 예측하고 이러한 값에 추가 속성이 필요한 경우 옵션 집합보다는 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="5e3a6-131">값 추가 또는 제거와 같은 옵션 집합을 유지하려면 관리자 또는 개발자가 요구되지만 표에 새 행을 추가하는 것은 대부분의 비즈니스 사용자가 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="5e3a6-132">다음 예는 리소스가 속한 역할 및 리소스 조직 단위를 기반으로 설정된 청구 요율을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="5e3a6-133">원가 요율은 일반적으로 직원의 급여대와 그들이 속한 조직 단위에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="5e3a6-134">이 예에서는 청구서 요율 및 원가 요율 표가 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3a6-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="5e3a6-135">**샘플 청구서 요율**</span><span class="sxs-lookup"><span data-stu-id="5e3a6-135">**Sample bill rates**</span></span>

| <span data-ttu-id="5e3a6-136">역할</span><span class="sxs-lookup"><span data-stu-id="5e3a6-136">Role</span></span>        | <span data-ttu-id="5e3a6-137">조직 단위</span><span class="sxs-lookup"><span data-stu-id="5e3a6-137">Org Unit</span></span>    |<span data-ttu-id="5e3a6-138">단위</span><span class="sxs-lookup"><span data-stu-id="5e3a6-138">Unit</span></span>      |<span data-ttu-id="5e3a6-139">가격</span><span class="sxs-lookup"><span data-stu-id="5e3a6-139">Price</span></span>      |<span data-ttu-id="5e3a6-140">통화</span><span class="sxs-lookup"><span data-stu-id="5e3a6-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5e3a6-141">개발자</span><span class="sxs-lookup"><span data-stu-id="5e3a6-141">Developer</span></span>   | <span data-ttu-id="5e3a6-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5e3a6-142">Contoso US</span></span>  |<span data-ttu-id="5e3a6-143">Hour</span><span class="sxs-lookup"><span data-stu-id="5e3a6-143">Hour</span></span> | <span data-ttu-id="5e3a6-144">200</span><span class="sxs-lookup"><span data-stu-id="5e3a6-144">200</span></span>|<span data-ttu-id="5e3a6-145">USD</span><span class="sxs-lookup"><span data-stu-id="5e3a6-145">USD</span></span>     |
| <span data-ttu-id="5e3a6-146">개발자</span><span class="sxs-lookup"><span data-stu-id="5e3a6-146">Developer</span></span>   | <span data-ttu-id="5e3a6-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5e3a6-147">Contoso India</span></span> |<span data-ttu-id="5e3a6-148">Hour</span><span class="sxs-lookup"><span data-stu-id="5e3a6-148">Hour</span></span>|   <span data-ttu-id="5e3a6-149">112</span><span class="sxs-lookup"><span data-stu-id="5e3a6-149">112</span></span>|<span data-ttu-id="5e3a6-150">USD</span><span class="sxs-lookup"><span data-stu-id="5e3a6-150">USD</span></span>     |


<span data-ttu-id="5e3a6-151">**샘플 원가 요율**</span><span class="sxs-lookup"><span data-stu-id="5e3a6-151">**Sample cost rates**</span></span>

| <span data-ttu-id="5e3a6-152">급여대</span><span class="sxs-lookup"><span data-stu-id="5e3a6-152">Salary Band</span></span>     | <span data-ttu-id="5e3a6-153">조직 단위</span><span class="sxs-lookup"><span data-stu-id="5e3a6-153">Org Unit</span></span>    |<span data-ttu-id="5e3a6-154">단위</span><span class="sxs-lookup"><span data-stu-id="5e3a6-154">Unit</span></span>      |<span data-ttu-id="5e3a6-155">가격</span><span class="sxs-lookup"><span data-stu-id="5e3a6-155">Price</span></span>      |<span data-ttu-id="5e3a6-156">통화</span><span class="sxs-lookup"><span data-stu-id="5e3a6-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5e3a6-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="5e3a6-157">My company_Band1</span></span> | <span data-ttu-id="5e3a6-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5e3a6-158">Contoso US</span></span>  |<span data-ttu-id="5e3a6-159">Hour</span><span class="sxs-lookup"><span data-stu-id="5e3a6-159">Hour</span></span> | <span data-ttu-id="5e3a6-160">145</span><span class="sxs-lookup"><span data-stu-id="5e3a6-160">145</span></span>|<span data-ttu-id="5e3a6-161">USD</span><span class="sxs-lookup"><span data-stu-id="5e3a6-161">USD</span></span>     |
| <span data-ttu-id="5e3a6-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="5e3a6-162">My company_Band2</span></span> | <span data-ttu-id="5e3a6-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5e3a6-163">Contoso India</span></span> |<span data-ttu-id="5e3a6-164">Hour</span><span class="sxs-lookup"><span data-stu-id="5e3a6-164">Hour</span></span>|   <span data-ttu-id="5e3a6-165">67</span><span class="sxs-lookup"><span data-stu-id="5e3a6-165">67</span></span>|<span data-ttu-id="5e3a6-166">USD</span><span class="sxs-lookup"><span data-stu-id="5e3a6-166">USD</span></span>     |
