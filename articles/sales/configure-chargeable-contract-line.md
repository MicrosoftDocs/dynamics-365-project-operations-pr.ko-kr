---
title: 프로젝트 계약 내용에 청구 가능 구성 요소 구성
description: 이 항목은 계약 내용에 포함된 청구 가능 및 청구 불가능 구성 요소에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858346"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a><span data-ttu-id="0fd74-103">프로젝트 계약 내용에 청구 가능 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="0fd74-103">Configure chargeable components of a project contract line</span></span>

<span data-ttu-id="0fd74-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0fd74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0fd74-105">프로젝트 기반 계약 내용에는 포함, 청구 가능 및 청구 불가능 구성 요소의 개념이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-105">A project-based contract line has the concept of included, chargeable, and non-chargeable components.</span></span>

<span data-ttu-id="0fd74-106">포함된 구성 요소는 프로젝트 기반 계약 내용에 정의된 청구 방법, 고객 분할, 초과하지 않는 한도 및 송장 빈도 설정의 적용을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based contract line.</span></span>

<span data-ttu-id="0fd74-107">포함 구성 요소의 하위 집합은 **청구 유형** 필드를 업데이트하여 청구 가능으로 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-107">A subset of the included components can be marked as chargeable by updating the **Billing Type** field.</span></span>

<span data-ttu-id="0fd74-108">청구 가능 구성 요소는 역할 및 트랜잭션 범주에 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-108">Chargeable components can be defined on roles, and transaction categories.</span></span>

<span data-ttu-id="0fd74-109">프로젝트 계약 내용의 경우 역할에 정의된 청구 가능성은 **시간** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-109">For a project contract line, the chargeability defined on a role only applies to the **Time** transaction class.</span></span> <span data-ttu-id="0fd74-110">프로젝트 계약 내용에서 **시간 포함** 이 **아니요** 로 설정된 경우 **청구 가능 역할** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-110">If **Include Time** is set to **No** on a project contract line, the **Chargeable roles** tab isn't available.</span></span>

<span data-ttu-id="0fd74-111">프로젝트 계약 내용의 트랜잭션 범주에 정의된 청구 가능성은 **경비** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-111">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="0fd74-112">프로젝트 계약 내용에서 **경비 포함** 이 **아니요** 로 설정된 경우 **청구 가능 범주** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-112">If **Include Expenses** is set to **No** on a project contract line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0fd74-113">역할을 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="0fd74-113">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0fd74-114">역할은 특정 프로젝트 기반 계약 내용에서 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-114">A role can be chargeable or non-chargeable on specific project-based contract line.</span></span>

<span data-ttu-id="0fd74-115">프로젝트 기반 계약 내용의 **청구 가능한 역할** 탭에 있는 **청구 가능한 범주** 하위 그리드의 **청구 유형** 필드에서 역할에 대한 청구 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-115">On the **Chargeable roles** tab of a projec-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a role.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0fd74-116">트랜잭션 범주를 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="0fd74-116">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0fd74-117">트랜잭션 범주는 특정 프로젝트 기반 계약 내용에서 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-117">A transaction category can be chargeable or non-chargeable on a specific project-based contract line.</span></span>

<span data-ttu-id="0fd74-118">프로젝트 기반 계약 내용의 **청구 가능한 범주** 탭에 있는 **청구 가능한 범주** 하위 그리드의 **청구 유형** 필드에서 트랜잭션에 대한 청구 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-118">On the **Chargeable Categories** tab of a project-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a transaction.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="0fd74-119">청구 가능성 해결</span><span class="sxs-lookup"><span data-stu-id="0fd74-119">Resolve chargeability</span></span>

<span data-ttu-id="0fd74-120">시간에 대해 생성된 추정 또는 실제는 시간이 계약 내용에 포함되어 있고 역할이 계약 내용에서 청구 가능으로 구성된 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-120">An estimate or actual created for time will only be considered chargeable if time is included on the contract line, and if the role is configured as chargeable on the contract line.</span></span>

<span data-ttu-id="0fd74-121">경비에 대해 생성된 추정 또는 실제는 경비가 계약 내용에 포함되어 있고 트랜잭션 범주가 계약 내용에서 청구 가능으로 구성된 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fd74-121">An estimate or actual created for expense will only be considered chargeable if expense is included on the contract line, and if the transaction category is configured as chargeable on the contract line.</span></span>

| <span data-ttu-id="0fd74-122">시간 포함</span><span class="sxs-lookup"><span data-stu-id="0fd74-122">Includes time</span></span> | <span data-ttu-id="0fd74-123">경비 포함</span><span class="sxs-lookup"><span data-stu-id="0fd74-123">Includes expense</span></span> | <span data-ttu-id="0fd74-124">역할</span><span class="sxs-lookup"><span data-stu-id="0fd74-124">Role</span></span> | <span data-ttu-id="0fd74-125">카테고리</span><span class="sxs-lookup"><span data-stu-id="0fd74-125">Category</span></span> | <span data-ttu-id="0fd74-126">작업</span><span class="sxs-lookup"><span data-stu-id="0fd74-126">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="0fd74-127">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-127">Yes</span></span> | <span data-ttu-id="0fd74-128">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-128">Yes</span></span> | <span data-ttu-id="0fd74-129">청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-129">Chargeable</span></span> | <span data-ttu-id="0fd74-130">청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-130">Chargeable</span></span> | <span data-ttu-id="0fd74-131">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-131">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="0fd74-132">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-132">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="0fd74-133">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-133">Yes</span></span> | <span data-ttu-id="0fd74-134">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-134">Yes</span></span> | <span data-ttu-id="0fd74-135">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-135">Non - Chargeable</span></span> | <span data-ttu-id="0fd74-136">청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-136">Chargeable</span></span> | <span data-ttu-id="0fd74-137">실제 시간 청구: 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-137">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="0fd74-138">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-138">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="0fd74-139">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-139">Yes</span></span> | <span data-ttu-id="0fd74-140">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-140">Yes</span></span> | <span data-ttu-id="0fd74-141">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-141">Non-Chargeable</span></span> | <span data-ttu-id="0fd74-142">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-142">Non-Chargeable</span></span> | <span data-ttu-id="0fd74-143">실제 시간 청구: 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-143">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="0fd74-144">실제 경비 청구 유형: 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-144">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="0fd74-145">없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-145">No</span></span> | <span data-ttu-id="0fd74-146">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-146">Yes</span></span> | <span data-ttu-id="0fd74-147">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-147">Can't be set</span></span> | <span data-ttu-id="0fd74-148">청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-148">Chargeable</span></span> | <span data-ttu-id="0fd74-149">실제 시간 청구: 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-149">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="0fd74-150">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-150">Billing type on an expense actual:Chargeable</span></span> |
| <span data-ttu-id="0fd74-151">없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-151">No</span></span> | <span data-ttu-id="0fd74-152">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-152">Yes</span></span> | <span data-ttu-id="0fd74-153">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-153">Can't be set</span></span> | <span data-ttu-id="0fd74-154">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-154">Non-Chargeable</span></span> | <span data-ttu-id="0fd74-155">실제 시간 청구: 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-155">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="0fd74-156">실제 경비 청구 유형: 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-156">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="0fd74-157">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-157">Yes</span></span> | <span data-ttu-id="0fd74-158">없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-158">No</span></span> | <span data-ttu-id="0fd74-159">청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-159">Chargeable</span></span> | <span data-ttu-id="0fd74-160">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-160">Can't be set</span></span> | <span data-ttu-id="0fd74-161">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-161">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="0fd74-162">실제 경비 청구 유형: 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-162">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="0fd74-163">예</span><span class="sxs-lookup"><span data-stu-id="0fd74-163">Yes</span></span> | <span data-ttu-id="0fd74-164">없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-164">No</span></span> | <span data-ttu-id="0fd74-165">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-165">Non-Chargeable</span></span> | <span data-ttu-id="0fd74-166">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-166">Can't be set</span></span> | <span data-ttu-id="0fd74-167">실제 시간 청구: 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0fd74-167">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="0fd74-168">실제 경비 청구 유형: 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fd74-168">Billing type on an expense actual: Not available</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
