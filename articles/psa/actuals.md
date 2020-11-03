---
title: 실제 개요
description: 이 항목은 프로젝트 실제값에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080250"
---
# <a name="actuals-overview"></a><span data-ttu-id="c8806-103">실제 개요</span><span class="sxs-lookup"><span data-stu-id="c8806-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c8806-104">실제값은 프로젝트에서 완료된 작업의 양입니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="c8806-105">프로젝트 실제값은 소스 문서까지 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="c8806-106">그러한 소스 문서에는 시간, 비용 및 분개장 항목과 송장도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![프로젝트 실제값가 소스 문서까지 추적되는 방법](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="c8806-108">시간 항목 제출</span><span class="sxs-lookup"><span data-stu-id="c8806-108">Submitting a time entry</span></span>

<span data-ttu-id="c8806-109">PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 두 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c8806-110">한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c8806-111">고정 가격 계약 행에 매핑되는 프로젝트에 대해 시간 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="c8806-112">기본 가격을 입력하는 논리는 분개장 행에 들어있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="c8806-113">시간 항목의 모든 필드 값이 분개장 행에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="c8806-114">처리 날짜, 프로젝트가 매핑된 계약 행 및 통화의 필드들이 사용되어 해당 가격표가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="c8806-115">기본 가격에 영향을 주는 **역할** 및 **조직 단위** 같은 필드는 기본적으로 해당 가격이 분개장 행에 입력되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="c8806-116">시간 항목에 맞춤 필드를 추가하고 필드 값을 실제값에 전파하려는 경우, 실제값 엔터티에 필드를 만들고 필드 매핑을 사용하여 시간 항목의 필드를 실제값로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="c8806-117">경비 항목 제출</span><span class="sxs-lookup"><span data-stu-id="c8806-117">Submitting an expense entry</span></span>

<span data-ttu-id="c8806-118">PSA에서 시간 및 자재 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 두 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c8806-119">한 행은 비용, 다른 행은 청구되지 않은 매출액을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c8806-120">고정 가격 계약 행에 매핑되는 프로젝트에 대해 경비 항목이 제출되면 비용만을 위한 한 개의 분개장 행이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="c8806-121">경비를 위한 기본 가격을 입력하는 논리는 **경비 입력** 페이지에서 선택하는 경비 카테고리에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="c8806-122">해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c8806-123">그러나 가격 자체의 경우, 사용자가 입력한 금액은 기본적으로 비용 및 매출액을 위한 관련 경비 분개장 행에 직접 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="c8806-124">현재 버전의 PSA에서는 경비 항목에 대한 단위당 기본 가격의 카테고리별 입력은 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="c8806-125">항목 분개장을 사용한 비용 기록</span><span class="sxs-lookup"><span data-stu-id="c8806-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="c8806-126">PSA에서는 항목 분개장을 사용하면 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c8806-127">분개장에는 표제, 행 및 **확인** 작업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="c8806-128">다음은 분개장을 사용할 수 있는 몇 가지 시나리오입니다:</span><span class="sxs-lookup"><span data-stu-id="c8806-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="c8806-129">귀하가 프로젝트에 대한 자재 실제값 비용 및 매출액을 기록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="c8806-130">다른 시스템의 처리 실제값를 PSA로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="c8806-131">다른 시스템에서 발생한, 조달 또는 하청 비용과 같은 비용을 기록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8806-132">항목 분개장을 사용하여 실제를 생성하는 것은 실제가 프로젝트에 미치는 회계 영향을 완전히 알고 있는 사용자만 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="c8806-133">이는 애플리케이션이 분개장 항목 유형 또는 분개장 항목에 입력된 관련 가격을 검증하지 않기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="c8806-134">이 분개장 유형의 영향으로 항목 분개장을 작성할 수 있는 액세스 권한이 부여된 사람에 대해 적절한 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="c8806-135">프로젝트 이벤트에 근거한 실제값 기록</span><span class="sxs-lookup"><span data-stu-id="c8806-135">Recording actuals based on project events</span></span>

<span data-ttu-id="c8806-136">PSA는 프로젝트 중에 발생하는 재무 처리를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c8806-137">이러한 처리는 **실제값** 으로 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="c8806-138">다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="c8806-139">**리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다**</span><span class="sxs-lookup"><span data-stu-id="c8806-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c8806-140">이벤트</span><span class="sxs-lookup"><span data-stu-id="c8806-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c8806-141">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c8806-142">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c8806-143">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c8806-144">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="c8806-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c8806-145">고정 가격</span><span class="sxs-lookup"><span data-stu-id="c8806-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c8806-146">실제</span><span class="sxs-lookup"><span data-stu-id="c8806-146">Actuals</span></span></th>
<th><span data-ttu-id="c8806-147">거래 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-147">Transaction currency</span></span></th>
<th><span data-ttu-id="c8806-148">고정 가격</span><span class="sxs-lookup"><span data-stu-id="c8806-148">Fixed price</span></span></th>
<th><span data-ttu-id="c8806-149">거래 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c8806-150">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c8806-151">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-152">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c8806-153">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8806-154">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8806-155">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-155">Cost actual</span></span></td>
<td><span data-ttu-id="c8806-156">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-157">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-158">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c8806-159">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-160">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-161">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c8806-162">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8806-163">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8806-164">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-164">Cost actual</span></span></td>
<td><span data-ttu-id="c8806-165">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-166">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-167">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-168">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-169">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-170">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-171">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-172">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="c8806-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-173">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8806-174">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8806-175">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8806-176">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-177">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-178">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-179">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-180">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-181">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-181">Billed sales</span></span></td>
<td><span data-ttu-id="c8806-182">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8806-183">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8806-184">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8806-185">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-186">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-187">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-188">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-189">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-190">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-191">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-192">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="c8806-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-193">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8806-194">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8806-195">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8806-196">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c8806-197">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c8806-198">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="c8806-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c8806-199">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-200">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-201">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-202">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-202">Billed sales</span></span></td>
<td><span data-ttu-id="c8806-203">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8806-204">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8806-205">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8806-206">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-207">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-208">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-209">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-210">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c8806-211">**리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다**</span><span class="sxs-lookup"><span data-stu-id="c8806-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c8806-212">이벤트</span><span class="sxs-lookup"><span data-stu-id="c8806-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c8806-213">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c8806-214">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c8806-215">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c8806-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c8806-216">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="c8806-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c8806-217">고정 가격</span><span class="sxs-lookup"><span data-stu-id="c8806-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c8806-218">실제</span><span class="sxs-lookup"><span data-stu-id="c8806-218">Actuals</span></span></th>
<th><span data-ttu-id="c8806-219">거래 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-219">Transaction currency</span></span></th>
<th><span data-ttu-id="c8806-220">고정 가격</span><span class="sxs-lookup"><span data-stu-id="c8806-220">Fixed price</span></span></th>
<th><span data-ttu-id="c8806-221">거래 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c8806-222">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c8806-223">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-224">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c8806-225">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c8806-226">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8806-227">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-227">Cost actual</span></span></td>
<td><span data-ttu-id="c8806-228">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c8806-229">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c8806-230">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c8806-231">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c8806-232">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-233">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c8806-234">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-235">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="c8806-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c8806-236">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-237">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c8806-238">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c8806-239">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8806-240">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-240">Cost actual</span></span></td>
<td><span data-ttu-id="c8806-241">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-242">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-243">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-244">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-245">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="c8806-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-246">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="c8806-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c8806-247">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-248">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c8806-249">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-250">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-251">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-252">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="c8806-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-253">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8806-254">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8806-255">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8806-256">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-257">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-258">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-259">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c8806-260">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-261">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-261">Billed sales</span></span></td>
<td><span data-ttu-id="c8806-262">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8806-263">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8806-264">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8806-265">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-266">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-267">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-268">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8806-269">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-270">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-271">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-272">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="c8806-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-273">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8806-274">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8806-275">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8806-276">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c8806-277">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c8806-278">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="c8806-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c8806-279">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-280">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c8806-281">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c8806-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-282">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-282">Billed sales</span></span></td>
<td><span data-ttu-id="c8806-283">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8806-284">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8806-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8806-285">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="c8806-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8806-286">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-287">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="c8806-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c8806-288">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8806-289">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="c8806-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8806-290">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="c8806-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
