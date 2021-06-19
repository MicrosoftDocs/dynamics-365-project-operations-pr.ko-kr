---
title: 프로젝트 기반 계약 내용의 청구 가능 구성 요소 구성
description: 이 항목은 Project Operations의 계약 내용에 청구 가능 구성 요스를 추가하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003729"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="46683-103">프로젝트 기반 계약 내용의 청구 가능 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="46683-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="46683-104">_**적용 대상:** 라이트 배포 - 견적 송장 처리, 리소스/비 재고 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="46683-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="46683-105">프로젝트 기반 계약 내용에는 *포함* 구성 요소 및 *청구 가능* 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="46683-106">포함 구성 요소는 다음과 같은 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="46683-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="46683-107">청구 방법 및 고객 분할</span><span class="sxs-lookup"><span data-stu-id="46683-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="46683-108">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="46683-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="46683-109">프로젝트 기반 계약 내용에 정의된 송장 빈도 설정</span><span class="sxs-lookup"><span data-stu-id="46683-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="46683-110">포함 구성 요소의 하위 집합은 **청구 유형** 필드를 사용하여 청구 가능으로 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="46683-111">**청구 유형** 필드는 계약 내용의 컨텍스트에서 다음 값을 허용하는 옵션 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="46683-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="46683-112">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-112">Chargeable</span></span>
  - <span data-ttu-id="46683-113">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="46683-113">Non-chargeable</span></span>

<span data-ttu-id="46683-114">청구 가능 구성 요소는 작업, 역할 및 트랜잭션 범주에 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="46683-115">청구 가능성은 프로젝트 계약 내용의 작업에 정의되며 라인에 포함된 모든 트랜잭션 클래스에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="46683-116">계약 내용의 **작업 포함** 필드가 비어 있거나 **전체 프로젝트** 로 설정된 경우 **청구 가능 작업** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="46683-117">프로젝트 계약 내용의 역할에 정의된 청구 가능성은 **시간** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="46683-118">계약 내용의 **시간 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 역할** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="46683-119">프로젝트 계약 내용의 트랜잭션 범주에 정의된 청구 가능성은 **경비** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="46683-120">**경비 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 범주** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="46683-121">프로젝트 작업을 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="46683-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="46683-122">프로젝트 작업은 특정 계약 내용에 대해 청구 가능하거나 청구 불가능할 수 있으므로 다음 설정이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="46683-123">프로젝트 기반 계약 내용에 **시간** 이 포함되고 특정 작업, **T1** 이 청구 가능으로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="46683-124">**경비** 를 포함하는 두 번째 계약 내용이 있는 경우, 계약 내용의 T1작업을 청구 불가능으로 연관시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="46683-125">결과적으로 작업에 기록된 모든 시간은 청구 가능하며 모든 경비는 청구 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="46683-126">작업의 청구 유형은 계약 내용 작업 하위 표에서 **청구 유형** 필드를 업데이트하여 계약 내용의 **청구 가능한 작업** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="46683-127">또는 작업과 연결된 계약 내용을 표시하는 프로젝트의 작업 청구 설정에 있는 하위 표의 **청구 유형** 필드에서 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="46683-128">역할을 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="46683-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="46683-129">역할은 특정 계약 내용에서 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="46683-130">역할의 청구 유형은 계약 내용의 **청구 가능한 역할** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="46683-131">이렇게 하려면 **청구 가능한 역할** 하위 표에서 **청구 유형** 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="46683-132">트랜잭션 범주를 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="46683-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="46683-133">트랜잭션 범주는 특정 계약 내용에서 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="46683-134">트랜잭션의 청구 유형은 프로젝트 기반 계약 내용의 **청구 가능한 범주** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="46683-135">이렇게 하려면 **청구 가능한 범주** 하위 표에서 **청구 유형** 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="46683-136">청구 가능성 해결</span><span class="sxs-lookup"><span data-stu-id="46683-136">Resolve chargeability</span></span>

<span data-ttu-id="46683-137">시간에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="46683-138">**시간** 은 계약 내용에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="46683-139">**역할** 은 계약 내용에서 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="46683-140">**포함된 작업** 은 계약 내용에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="46683-141">이 세 가지 사항이 참이면 작업이 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="46683-142">경비에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="46683-143">**경비** 는 계약 내용에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="46683-144">**트랜잭션 범주** 는 계약 내용에서 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="46683-145">**포함된 작업** 은 계약 내용에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="46683-146">이 세 가지 사항이 참이면 **작업** 이 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="46683-147">재료에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="46683-148">**재료** 는 계약 내용에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="46683-149">**포함된 작업** 은 계약 내용에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="46683-150">이 두 가지 사항이 참이면 **작업** 이 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-151">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="46683-152">
                    <strong>경비 포함</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="46683-153">
                    <strong>재료 포함</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="46683-154">
                    <strong>포함된 작업</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-155">
                    <strong>역할</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-156">
                    <strong>카테고리</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-157">
                    <strong>작업</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="46683-158">
                    <strong>청구 가능성 영향</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-159">네</span><span class="sxs-lookup"><span data-stu-id="46683-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-160">네</span><span class="sxs-lookup"><span data-stu-id="46683-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-161">네</span><span class="sxs-lookup"><span data-stu-id="46683-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-162">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-163">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-164">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-165">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-166">실제 시간 청구: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-167">실제 경비 청구 유형: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-168">실제 재료 청구 유형: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-169">네</span><span class="sxs-lookup"><span data-stu-id="46683-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-170">네</span><span class="sxs-lookup"><span data-stu-id="46683-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-171">네</span><span class="sxs-lookup"><span data-stu-id="46683-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-172">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="46683-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-173">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-174">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-175">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-176">실제 시간 청구: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-177">실제 경비 청구 유형: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-178">실제 재료 청구 유형: <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-179">네</span><span class="sxs-lookup"><span data-stu-id="46683-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-180">네</span><span class="sxs-lookup"><span data-stu-id="46683-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-181">네</span><span class="sxs-lookup"><span data-stu-id="46683-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-182">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="46683-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-183">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-184">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-185">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-186">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-187">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="46683-188">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-189">네</span><span class="sxs-lookup"><span data-stu-id="46683-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-190">네</span><span class="sxs-lookup"><span data-stu-id="46683-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-191">네</span><span class="sxs-lookup"><span data-stu-id="46683-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-192">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="46683-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-193">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-194">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-195">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-196">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-197">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-198">실제 재료 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-199">네</span><span class="sxs-lookup"><span data-stu-id="46683-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-200">네</span><span class="sxs-lookup"><span data-stu-id="46683-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-201">네</span><span class="sxs-lookup"><span data-stu-id="46683-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-202">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="46683-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-203">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-204">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-205">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-206">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-207">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-208">실제 재료 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-209">네</span><span class="sxs-lookup"><span data-stu-id="46683-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-210">네</span><span class="sxs-lookup"><span data-stu-id="46683-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-211">네</span><span class="sxs-lookup"><span data-stu-id="46683-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-212">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="46683-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-213">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-214">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-215">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-216">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-217">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-218">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-219">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-220">네</span><span class="sxs-lookup"><span data-stu-id="46683-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-221">네</span><span class="sxs-lookup"><span data-stu-id="46683-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-222">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-223">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-224">
                    <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-225">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-226">실제 시간 청구: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-227">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="46683-228">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-229">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-230">네</span><span class="sxs-lookup"><span data-stu-id="46683-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-231">네</span><span class="sxs-lookup"><span data-stu-id="46683-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-232">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-233">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-234">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-235">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-236">실제 시간 청구: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-237">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-238">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-239">네</span><span class="sxs-lookup"><span data-stu-id="46683-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="46683-240">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-241">네</span><span class="sxs-lookup"><span data-stu-id="46683-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-242">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-243">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-244">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-245">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-246">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="46683-247">실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-248">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-249">네</span><span class="sxs-lookup"><span data-stu-id="46683-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="46683-250">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="46683-251">네</span><span class="sxs-lookup"><span data-stu-id="46683-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-252">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-253">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-254">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-255">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-256">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-257">실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-258">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-259">네</span><span class="sxs-lookup"><span data-stu-id="46683-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-260">네</span><span class="sxs-lookup"><span data-stu-id="46683-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="46683-261">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-262">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-263">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-264">청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-265">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-266">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="46683-267">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="46683-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="46683-268">실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="46683-269">네</span><span class="sxs-lookup"><span data-stu-id="46683-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="46683-270">네</span><span class="sxs-lookup"><span data-stu-id="46683-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="46683-271">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="46683-272">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="46683-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="46683-273">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="46683-274">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="46683-275">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="46683-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="46683-276">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-277">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="46683-278">실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="46683-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
