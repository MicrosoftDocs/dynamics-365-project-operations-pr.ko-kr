---
title: 실제
description: 이 항목은 프로젝트 실제값에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753338"
---
# <a name="actuals"></a><span data-ttu-id="0844c-103">실제</span><span class="sxs-lookup"><span data-stu-id="0844c-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0844c-104">실제값은 프로젝트에서 완료된 작업의 양입니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0844c-105">프로젝트 실제값은 소스 문서까지 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0844c-106">그러한 소스 문서에는 시간, 비용 및 분개장 항목과 송장도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![프로젝트 실제값가 소스 문서까지 추적되는 방법](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0844c-108">시간 항목 제출</span><span class="sxs-lookup"><span data-stu-id="0844c-108">Submitting a time entry</span></span>

<span data-ttu-id="0844c-109">PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 두 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0844c-110">한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0844c-111">고정 가격 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0844c-112">기본 가격을 입력하는 논리는 분개장 행에 들어있습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0844c-113">시간 항목의 모든 필드 값이 분개장 행에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0844c-114">처리 날짜, 프로젝트가 매핑된 계약 행 및 통화의 필드들이 사용되어 해당 가격표가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0844c-115">기본 가격에 영향을 주는 **역할** 및 **조직 단위** 같은 필드는 기본적으로 해당 가격이 분개장 행에 입력되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0844c-116">시간 항목에 맞춤 필드를 추가하고 필드 값을 실제값에 전파하려는 경우, 실제값 엔터티에 필드를 만들고 필드 매핑을 사용하여 시간 항목의 필드를 실제값로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0844c-117">경비 항목 제출</span><span class="sxs-lookup"><span data-stu-id="0844c-117">Submitting an expense entry</span></span>

<span data-ttu-id="0844c-118">PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 두 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0844c-119">한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0844c-120">고정 가격 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0844c-121">경비를 위한 기본 가격을 입력하는 논리는 **경비 입력** 페이지에서 선택하는 경비 카테고리에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0844c-122">해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0844c-123">그러나 가격 자체의 경우, 사용자가 입력한 금액은 기본적으로 비용 및 매출액을 위한 관련 경비 분개장 행에 직접 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0844c-124">현재 버전의 PSA에서는 경비 항목에 대한 단위당 기본 가격의 카테고리별 입력은 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="0844c-125">분개장을 사용한 비용 기록</span><span class="sxs-lookup"><span data-stu-id="0844c-125">Using journals to record costs</span></span>

<span data-ttu-id="0844c-126">PSA에서는 분개장을 사용하면 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0844c-127">분개장에는 표제, 행 및**확인** 작업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0844c-128">다음은 분개장을 사용할 수 있는 몇 가지 시나리오입니다:</span><span class="sxs-lookup"><span data-stu-id="0844c-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0844c-129">귀하가 프로젝트에 대한 자재 실제값 비용 및 매출액을 기록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0844c-130">다른 시스템의 처리 실제값를 PSA로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0844c-131">다른 시스템에서 발생한, 조달 또는 하청 비용과 같은 비용을 기록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0844c-132">프로젝트 이벤트에 근거한 실제값 기록</span><span class="sxs-lookup"><span data-stu-id="0844c-132">Recording actuals based on project events</span></span>

<span data-ttu-id="0844c-133">PSA는 프로젝트 중에 발생하는 재무 처리를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0844c-134">이러한 처리는 **실제값**으로 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0844c-135">다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0844c-136">**리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다**</span><span class="sxs-lookup"><span data-stu-id="0844c-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0844c-137">이벤트</span><span class="sxs-lookup"><span data-stu-id="0844c-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0844c-138">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0844c-139">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0844c-140">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0844c-141">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="0844c-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0844c-142">고정 가격</span><span class="sxs-lookup"><span data-stu-id="0844c-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0844c-143">실제</span><span class="sxs-lookup"><span data-stu-id="0844c-143">Actuals</span></span></th>
<th><span data-ttu-id="0844c-144">거래 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-144">Transaction currency</span></span></th>
<th><span data-ttu-id="0844c-145">고정 가격</span><span class="sxs-lookup"><span data-stu-id="0844c-145">Fixed price</span></span></th>
<th><span data-ttu-id="0844c-146">거래 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0844c-147">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0844c-148">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-149">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0844c-150">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0844c-151">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0844c-152">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-152">Cost actual</span></span></td>
<td><span data-ttu-id="0844c-153">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-154">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-155">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0844c-156">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-157">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-158">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0844c-159">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0844c-160">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0844c-161">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-161">Cost actual</span></span></td>
<td><span data-ttu-id="0844c-162">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-163">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-164">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-165">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-166">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-167">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-168">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-169">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0844c-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-170">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0844c-171">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0844c-172">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0844c-173">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-174">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-175">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-176">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-177">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-178">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-178">Billed sales</span></span></td>
<td><span data-ttu-id="0844c-179">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0844c-180">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0844c-181">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0844c-182">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-183">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-184">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-185">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-186">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-187">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-188">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-189">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0844c-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-190">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0844c-191">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0844c-192">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0844c-193">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0844c-194">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0844c-195">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="0844c-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0844c-196">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-197">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-198">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-199">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-199">Billed sales</span></span></td>
<td><span data-ttu-id="0844c-200">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0844c-201">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0844c-202">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0844c-203">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-204">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-205">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-206">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-207">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0844c-208">**리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다**</span><span class="sxs-lookup"><span data-stu-id="0844c-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0844c-209">이벤트</span><span class="sxs-lookup"><span data-stu-id="0844c-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0844c-210">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0844c-211">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0844c-212">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0844c-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0844c-213">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="0844c-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0844c-214">고정 가격</span><span class="sxs-lookup"><span data-stu-id="0844c-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0844c-215">실제</span><span class="sxs-lookup"><span data-stu-id="0844c-215">Actuals</span></span></th>
<th><span data-ttu-id="0844c-216">거래 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-216">Transaction currency</span></span></th>
<th><span data-ttu-id="0844c-217">고정 가격</span><span class="sxs-lookup"><span data-stu-id="0844c-217">Fixed price</span></span></th>
<th><span data-ttu-id="0844c-218">거래 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0844c-219">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0844c-220">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-221">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0844c-222">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0844c-223">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0844c-224">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-224">Cost actual</span></span></td>
<td><span data-ttu-id="0844c-225">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0844c-226">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0844c-227">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0844c-228">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0844c-229">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-230">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0844c-231">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-232">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="0844c-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0844c-233">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-234">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0844c-235">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0844c-236">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0844c-237">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-237">Cost actual</span></span></td>
<td><span data-ttu-id="0844c-238">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-239">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-240">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-241">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-242">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="0844c-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-243">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="0844c-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0844c-244">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-245">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0844c-246">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-247">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-248">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-249">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0844c-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-250">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0844c-251">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0844c-252">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0844c-253">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-254">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-255">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-256">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0844c-257">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-258">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-258">Billed sales</span></span></td>
<td><span data-ttu-id="0844c-259">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0844c-260">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0844c-261">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0844c-262">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-263">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-264">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-265">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0844c-266">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-267">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-268">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-269">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="0844c-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-270">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0844c-271">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0844c-272">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0844c-273">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0844c-274">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0844c-275">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="0844c-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0844c-276">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-277">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0844c-278">해당 없음</span><span class="sxs-lookup"><span data-stu-id="0844c-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-279">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-279">Billed sales</span></span></td>
<td><span data-ttu-id="0844c-280">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0844c-281">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0844c-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0844c-282">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="0844c-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0844c-283">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-284">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="0844c-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0844c-285">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0844c-286">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="0844c-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0844c-287">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="0844c-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
