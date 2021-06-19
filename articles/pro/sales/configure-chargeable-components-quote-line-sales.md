---
title: 견적 라인의 청구 가능 구성 요소 구성
description: 이 항목은 프로젝트 기반 견적 라인에서 청구 가능 및 청구 불가능 구성 요소 설정에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003774"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="03b3b-103">견적 라인의 청구 가능 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="03b3b-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="03b3b-104">_**적용 대상:** 라이트 배포 - 견적 송장 처리, 리소스/비 재고 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="03b3b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="03b3b-105">프로젝트 기반 견적 라인에는 *포함* 구성 요소 및 *청구 가능* 구성 요소의 개념이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="03b3b-106">포함된 구성 요소는 다음 항목에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-106">Included components are subject to:</span></span>

  - <span data-ttu-id="03b3b-107">청구 방법 및 고객 분할</span><span class="sxs-lookup"><span data-stu-id="03b3b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="03b3b-108">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="03b3b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="03b3b-109">프로젝트 기반 견적 라인에 정의된 송장 빈도 설정</span><span class="sxs-lookup"><span data-stu-id="03b3b-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="03b3b-110">포함 구성 요소의 하위 집합은 **청구 유형** 필드를 사용하여 청구 가능으로 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="03b3b-111">**청구 유형** 필드는 견적 라인의 컨텍스트에서 다음 값을 허용하는 옵션 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="03b3b-112">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-112">Chargeable</span></span>
  - <span data-ttu-id="03b3b-113">청구 불가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-113">Non-chargeable</span></span>

<span data-ttu-id="03b3b-114">청구 가능 구성 요소는 작업, 역할 및 트랜잭션 범주에 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="03b3b-115">청구 가능성은 견적 라인의 작업에 정의되며 해당 라인에 포함된 모든 트랜잭션 클래스에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="03b3b-116">**작업 포함** 필드가 **전체 프로젝트** 로 설정되거나 비어 있는 경우 **청구 가능 작업** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="03b3b-117">청구 가능성은 견적 라인의 역할에 정의되며 **시간** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="03b3b-118">프로젝트 견적 라인에서 **시간 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 역할** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="03b3b-119">청구 가능성은 견적 라인의 트랜잭션 범주에 정의되며 **경비** 트랜잭션 클래스에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="03b3b-120">프로젝트 견적 라인에서 **경비 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 범주** 탭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="03b3b-121">프로젝트 작업을 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="03b3b-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="03b3b-122">특정 프로젝트 기반 연적 라인의 컨텍스트에서 프로젝트 작업은 청구 가능하거나 청구 불가능할 수 있으므로 다음 설정이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="03b3b-123">프로젝트 기반 견적 라인에 **시간** 및 작업 **T1** 이 포함된 경우 작업은 청구 가능으로 견적 라인에 연관됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="03b3b-124">**경비** 를 포함하는 두 번째 견적 라인이 있는 경우, 견적 라인의 **T1** 작업을 청구 불가능으로 연관시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="03b3b-125">결과적으로 작업에 기록된 모든 시간은 청구 가능하며 작업에 기록된 모든 경비는 청구 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="03b3b-126">작업의 청구 유형은 **견적 라인 작업** 하위 표에서 **청구 유형** 필드를 업데이트하여 프로젝트 기반 견적 라인의 **청구 가능한 작업** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="03b3b-127">또는 작업과 연결된 견적 라인을 표시하는 프로젝트의 작업 청구 설정에 있는 하위 표의 **청구 유형** 필드에서 프로젝트 작업에 대한 청구 유형을 업데이트 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="03b3b-128">역할을 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="03b3b-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="03b3b-129">특정 프로젝트 기반 견적 라인의 컨텍스트에서 역할은 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="03b3b-130">역할의 청구 유형은 **청구 가능 역할** 하위 표에서 **청구 유형** 필드를 업데이트하여 견적 라인의 **청구 가능한 역할** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="03b3b-131">트랜잭션 범주를 청구 가능 또는 청구 불가능으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="03b3b-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="03b3b-132">트랜잭션 범주는 특정 견적 라인에서 청구 가능하거나 청구 불가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="03b3b-133">트랜잭션의 청구 유형은 **청구 가능 범주** 하위 표에서 **청구 유형** 필드를 업데이트하여 견적 라인의 **청구 가능한 범주** 탭에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="03b3b-134">청구 가능성 해결</span><span class="sxs-lookup"><span data-stu-id="03b3b-134">Resolve chargeability</span></span>
<span data-ttu-id="03b3b-135">시간에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="03b3b-136">**시간** 은 견적 라인에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="03b3b-137">**역할** 은 견적 라인에서 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="03b3b-138">**포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="03b3b-139">이 세 가지 사항이 참이면 **작업** 도 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="03b3b-140">경비에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="03b3b-141">**경비** 는 견적 라인에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="03b3b-142">**트랜잭션 범주** 는 견적 라인에서 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="03b3b-143">**포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="03b3b-144">이 세 가지 사항이 참이면 **작업** 도 청구 가능으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="03b3b-145">재료에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="03b3b-146">**재료** 는 견적 라인에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="03b3b-147">**포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="03b3b-148">이 두 가지 사항이 참이면 **작업** 도 청구 가능으로 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b3b-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-149">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="03b3b-150">
                    <strong>경비 포함</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="03b3b-151">
                    <strong>재료 포함</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="03b3b-152">
                    <strong>포함된 작업</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-153">
                    <strong>역할</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-154">
                    <strong>카테고리</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-155">
                    <strong>작업</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="03b3b-156">
                    <strong>청구 가능성 영향</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-157">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-158">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-159">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-160">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-161">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-162">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-163">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-164">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-165">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-166">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-167">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-168">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-169">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-170">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="03b3b-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-171">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-172">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-173">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-174">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-175">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-176">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-177">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-178">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-179">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-180">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="03b3b-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-181">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-182">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-183">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-184">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-185">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-186">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-187">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-188">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-189">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-190">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="03b3b-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-191">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-192">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-193">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-194">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-195">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-196">실제 재료 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-197">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-198">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-199">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-200">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="03b3b-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-201">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-202">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-203">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-204">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-205">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-206">실제 재료 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-207">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-208">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-209">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-210">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="03b3b-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-211">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-212">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-213">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-214">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-215">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-216">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-217">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-218">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-219">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-220">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-221">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-222">
                    <strong>청구 가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-223">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-224">실제 시간 청구: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-225">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-226">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-227">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-228">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-229">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-230">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-231">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-232">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-233">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-234">실제 시간 청구: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-235">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-236">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-237">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="03b3b-238">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-239">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-240">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-241">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-242">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-243">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-244">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-245">실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-246">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-247">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="03b3b-248">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="03b3b-249">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-250">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-251">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-252">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-253">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-254">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-255">실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-256">실제 재료 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-257">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-258">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="03b3b-259">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-260">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-261">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-262">청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-263">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-264">실제 시간 청구: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-265">실제 경비 청구 유형: 청구 가능</span><span class="sxs-lookup"><span data-stu-id="03b3b-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="03b3b-266">실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="03b3b-267">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="03b3b-268">네</span><span class="sxs-lookup"><span data-stu-id="03b3b-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="03b3b-269">
                    <strong>없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="03b3b-270">전체 프로젝트</span><span class="sxs-lookup"><span data-stu-id="03b3b-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03b3b-271">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="03b3b-272">
                    <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03b3b-273">설정할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03b3b-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="03b3b-274">실제 시간 청구: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-275">실제 경비 청구 유형: <strong>청구 불가능</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="03b3b-276">실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03b3b-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
