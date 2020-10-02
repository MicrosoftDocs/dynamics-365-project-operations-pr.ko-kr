---
title: 가격 책정 차원 개요
description: 이 항목은 Dynamics 365 Project Operations에서 가격 책정 차원에 대한 정보를 제공합니다.
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898224"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="d75dd-103">가격 책정 차원 개요</span><span class="sxs-lookup"><span data-stu-id="d75dd-103">Pricing dimensions overview</span></span>

<span data-ttu-id="d75dd-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="d75dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d75dd-105">인적 자원에서 가격 및 원가를 설정하는 데 사용되는 차원은 두 가지 카테고리로 나뉩니다:</span><span class="sxs-lookup"><span data-stu-id="d75dd-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d75dd-106">사람</span><span class="sxs-lookup"><span data-stu-id="d75dd-106">People</span></span>
- <span data-ttu-id="d75dd-107">계획된 작업</span><span class="sxs-lookup"><span data-stu-id="d75dd-107">Planned work</span></span>

<span data-ttu-id="d75dd-108">따라서 사용할 수 있는 가격 차원 값에는 두 가지 타입이 있습니다:</span><span class="sxs-lookup"><span data-stu-id="d75dd-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="d75dd-109">**옵션 집합**: 값 집합에 대해 고정된 열거형인 차원입니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d75dd-110">**엔터티 기반 값**: 다양한 값 집합일 수 있는 차원입니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d75dd-111">가격 책정 차원</span><span class="sxs-lookup"><span data-stu-id="d75dd-111">Pricing dimensions</span></span>

<span data-ttu-id="d75dd-112">Dynamics 365 Project Operations는 기본 가격 책정 차원 집합과 함께 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d75dd-113">**프로젝트 작업** > **매개 변수**로 이동하여 이러한 가격 책정 차원을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="d75dd-114">파라미터 레코드에서 **금액 기반 가격 책정 차원** 탭에서 역할, **msdyn_resourcecategory** 및 리소싱 조직 단위, **msdyn_organizationalunit**의 필드 **매출액에 해당** 및 **원가에 해당**이 **예**로 설정되어 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="d75dd-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d75dd-115">이러한 필드를 활성화하면 각 역할 및 조직 단위 조합에 대한 가격과 원가를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="d75dd-116">추가 속성을 사용하는 리소스에 대한 가격 또는 원가가 필요한 경우 맞춤화된 필드, 엔터티 및 차원을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d75dd-117">인적 자원 시간 가격 책정</span><span class="sxs-lookup"><span data-stu-id="d75dd-117">Pricing human resource time</span></span>
<span data-ttu-id="d75dd-118">조직이 인적 자원 시간을 어떻게 책정하는지는 종종 조직의 수익성에 직접적인 영향을 미치는 중요한 전략적 고려 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d75dd-119">귀하의 조직이 인적 자원 시간을 위한 청구서 및 원가 요율을 설정하는 방법을 파악할 준비가 되면 재무팀 및 실무 책임자들과 협력하십시오.</span><span class="sxs-lookup"><span data-stu-id="d75dd-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d75dd-120">가격 책정에 대한 다른 고려 사항으로는 현재 가격 책정 차원이 아니지만 조직의 가격 책정 차원으로 적용되는 필드 또는 엔터티를 다시 사용할지 여부가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d75dd-121">**처리 카테고리**(**msdyn_transactioncategory**) 및 **예약 가능한 리소스**(**bookableresource**) 같은 필드는 후보 차원의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d75dd-122">가격 책정 차원이 표여야 하는지 옵션 집합이어야 하는지도 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d75dd-123">10 또는 12를 초과하는 차원값의 변경을 예측하고 이러한 값에 추가 속성이 필요한 경우 옵션 집합보다는 엔터티를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d75dd-124">값 추가 또는 제거와 같은 옵션 집합을 유지하려면 관리자 또는 개발자가 요구되지만 표에 새 행을 추가하는 것은 대부분의 사용자가 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d75dd-125">다음 예는 리소스가 속한 역할 및 리소스 조직 단위를 기반으로 설정된 청구 요율을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d75dd-126">원가 요율은 일반적으로 직원의 급여대와 그들이 속한 조직 단위에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d75dd-127">이 예에서는 청구서 요율 및 원가 요율 표가 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d75dd-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d75dd-128">**샘플 청구서 요율**</span><span class="sxs-lookup"><span data-stu-id="d75dd-128">**Sample bill rates**</span></span>

| <span data-ttu-id="d75dd-129">역할</span><span class="sxs-lookup"><span data-stu-id="d75dd-129">Role</span></span>        | <span data-ttu-id="d75dd-130">조직 단위</span><span class="sxs-lookup"><span data-stu-id="d75dd-130">Org Unit</span></span>    |<span data-ttu-id="d75dd-131">단위</span><span class="sxs-lookup"><span data-stu-id="d75dd-131">Unit</span></span>      |<span data-ttu-id="d75dd-132">가격</span><span class="sxs-lookup"><span data-stu-id="d75dd-132">Price</span></span>      |<span data-ttu-id="d75dd-133">통화</span><span class="sxs-lookup"><span data-stu-id="d75dd-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d75dd-134">개발자</span><span class="sxs-lookup"><span data-stu-id="d75dd-134">Developer</span></span>   | <span data-ttu-id="d75dd-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d75dd-135">Contoso US</span></span>  |<span data-ttu-id="d75dd-136">Hour</span><span class="sxs-lookup"><span data-stu-id="d75dd-136">Hour</span></span> | <span data-ttu-id="d75dd-137">200</span><span class="sxs-lookup"><span data-stu-id="d75dd-137">200</span></span>|<span data-ttu-id="d75dd-138">USD</span><span class="sxs-lookup"><span data-stu-id="d75dd-138">USD</span></span>     |
| <span data-ttu-id="d75dd-139">개발자</span><span class="sxs-lookup"><span data-stu-id="d75dd-139">Developer</span></span>   | <span data-ttu-id="d75dd-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d75dd-140">Contoso India</span></span> |<span data-ttu-id="d75dd-141">Hour</span><span class="sxs-lookup"><span data-stu-id="d75dd-141">Hour</span></span>|   <span data-ttu-id="d75dd-142">112</span><span class="sxs-lookup"><span data-stu-id="d75dd-142">112</span></span>|<span data-ttu-id="d75dd-143">USD</span><span class="sxs-lookup"><span data-stu-id="d75dd-143">USD</span></span>     |


<span data-ttu-id="d75dd-144">**샘플 원가 요율**</span><span class="sxs-lookup"><span data-stu-id="d75dd-144">**Sample cost rates**</span></span>

| <span data-ttu-id="d75dd-145">급여대</span><span class="sxs-lookup"><span data-stu-id="d75dd-145">Salary Band</span></span>     | <span data-ttu-id="d75dd-146">조직 단위</span><span class="sxs-lookup"><span data-stu-id="d75dd-146">Org Unit</span></span>    |<span data-ttu-id="d75dd-147">단위</span><span class="sxs-lookup"><span data-stu-id="d75dd-147">Unit</span></span>      |<span data-ttu-id="d75dd-148">가격</span><span class="sxs-lookup"><span data-stu-id="d75dd-148">Price</span></span>      |<span data-ttu-id="d75dd-149">통화</span><span class="sxs-lookup"><span data-stu-id="d75dd-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d75dd-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="d75dd-150">My company_Band1</span></span> | <span data-ttu-id="d75dd-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d75dd-151">Contoso US</span></span>  |<span data-ttu-id="d75dd-152">Hour</span><span class="sxs-lookup"><span data-stu-id="d75dd-152">Hour</span></span> | <span data-ttu-id="d75dd-153">145</span><span class="sxs-lookup"><span data-stu-id="d75dd-153">145</span></span>|<span data-ttu-id="d75dd-154">USD</span><span class="sxs-lookup"><span data-stu-id="d75dd-154">USD</span></span>     |
| <span data-ttu-id="d75dd-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="d75dd-155">My company_Band2</span></span> | <span data-ttu-id="d75dd-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d75dd-156">Contoso India</span></span> |<span data-ttu-id="d75dd-157">Hour</span><span class="sxs-lookup"><span data-stu-id="d75dd-157">Hour</span></span>|   <span data-ttu-id="d75dd-158">67</span><span class="sxs-lookup"><span data-stu-id="d75dd-158">67</span></span>|<span data-ttu-id="d75dd-159">USD</span><span class="sxs-lookup"><span data-stu-id="d75dd-159">USD</span></span>     |
