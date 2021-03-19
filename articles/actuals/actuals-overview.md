---
title: 실제
description: 이 토픽은 Microsoft Dynamics 365 Project Operations에서 실제 값으로 작업하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291807"
---
# <a name="actuals"></a><span data-ttu-id="25a8e-103">실제 값</span><span class="sxs-lookup"><span data-stu-id="25a8e-103">Actuals</span></span> 

<span data-ttu-id="25a8e-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="25a8e-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="25a8e-105">실제값은 프로젝트에서 완료된 작업의 양입니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="25a8e-106">시간과 경비 항목, 분개장 항목과 송장의 결과로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="25a8e-107">분개장 항목 및 시간 제출</span><span class="sxs-lookup"><span data-stu-id="25a8e-107">Journal lines and time submission</span></span>

<span data-ttu-id="25a8e-108">시간 항목에 대한 자세한 내용은 [시간 항목 개요](../time/time-entry-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="25a8e-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="25a8e-109">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="25a8e-109">Time and materials</span></span>

<span data-ttu-id="25a8e-110">제출된 시간 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="25a8e-111">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-111">Fixed price</span></span>

<span data-ttu-id="25a8e-112">제출된 시간 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="25a8e-113">기본 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-113">Default pricing</span></span>

<span data-ttu-id="25a8e-114">기본 가격을 작성하는 논리는 분개장 항목에 들어있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="25a8e-115">시간 항목의 필드 값이 분개장 항목에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="25a8e-116">이러한 값에는 트랜잭션 날짜, 프로젝트가 매핑된 계약 내용 및 해당 가격표의 통화 결과가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="25a8e-117">기본 가격에 영향을 주는 **역할** 및 **조직 단위** 같은 필드는 분개장 항목에서 해당 가격을 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="25a8e-118">시간 항목에 사용자 지정 필드를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="25a8e-119">필드 값을 실제값에 전파하려는 경우, 실제값 엔터티에 필드를 만들고 필드 매핑을 사용하여 시간 항목의 필드를 실제값로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="25a8e-120">분개장 항목 및 기본 경비 제출</span><span class="sxs-lookup"><span data-stu-id="25a8e-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="25a8e-121">경비 항목에 대한 자세한 내용은 [경비 개요](../expense/expense-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="25a8e-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="25a8e-122">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="25a8e-122">Time and materials</span></span>

<span data-ttu-id="25a8e-123">제출된 기본 경비 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="25a8e-124">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-124">Fixed price</span></span>

<span data-ttu-id="25a8e-125">제출된 기본 경비 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="25a8e-126">기본 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-126">Default pricing</span></span>

<span data-ttu-id="25a8e-127">경비에 대한 기본 가격을 입력하는 논리는 경비 범주를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="25a8e-128">해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="25a8e-129">그러나 기본적으로 가격 자체에 대해 입력된 금액은 비용 및 매출액을 위한 관련 경비 분개장 행에 직접 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="25a8e-130">경비 항목에 대한 단위당 기본 가격의 범주 기반 입력은 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="25a8e-131">항목 분개장을 사용하여 비용 기록</span><span class="sxs-lookup"><span data-stu-id="25a8e-131">Use entry journals to record costs</span></span>

<span data-ttu-id="25a8e-132">항목 분개장을 사용하여 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="25a8e-133">분개장은 다음과 같은 목적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="25a8e-134">프로젝트의 실제 재료비 및 판매 비용을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="25a8e-135">다른 시스템의 트랜잭션 실제를 Microsoft Dynamics 365 Project Operations로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="25a8e-136">다른 시스템에서 발생한 비용을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="25a8e-137">이러한 비용에는 조달 또는 하도급 비용이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25a8e-138">애플리케이션은 분개장 항목 유형 또는 분개장 항목에 입력된 관련 가격을 검증하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="25a8e-139">따라서 실제 값이 프로젝트에 미치는 회계 영향을 완전히 알고 있는 사용자만 항목 분개장을 사용하여 실제 값을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="25a8e-140">이 분개장 유형의 영향으로 인해 항목 분개장을 만들 수 있는 액세스 권한이 있는 사람을 신중하게 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="25a8e-141">프로젝트 이벤트에 근거한 실제값 기록</span><span class="sxs-lookup"><span data-stu-id="25a8e-141">Record actuals based on project events</span></span>

<span data-ttu-id="25a8e-142">Project Operations는 프로젝트 중에 발생하는 재무 트랜잭션을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="25a8e-143">이러한 처리는 실제값으로 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="25a8e-144">다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="25a8e-145">리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다</span><span class="sxs-lookup"><span data-stu-id="25a8e-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="25a8e-146">이벤트</span><span class="sxs-lookup"><span data-stu-id="25a8e-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="25a8e-147">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="25a8e-148">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="25a8e-149">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="25a8e-150">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="25a8e-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="25a8e-151">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="25a8e-152">실제</span><span class="sxs-lookup"><span data-stu-id="25a8e-152">Actuals</span></span></th>
<th><span data-ttu-id="25a8e-153">거래 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-153">Transaction currency</span></span></th>
<th><span data-ttu-id="25a8e-154">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-154">Fixed price</span></span></th>
<th><span data-ttu-id="25a8e-155">거래 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="25a8e-156">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="25a8e-157">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-158">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="25a8e-159">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25a8e-160">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25a8e-161">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-161">Cost actual</span></span></td>
<td><span data-ttu-id="25a8e-162">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-163">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-164">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="25a8e-165">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-166">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-167">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="25a8e-168">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25a8e-169">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25a8e-170">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-170">Cost actual</span></span></td>
<td><span data-ttu-id="25a8e-171">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-172">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-173">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-174">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-175">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-176">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-177">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-178">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-179">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25a8e-180">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25a8e-181">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25a8e-182">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-183">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-184">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-185">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-186">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-187">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-187">Billed sales</span></span></td>
<td><span data-ttu-id="25a8e-188">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25a8e-189">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25a8e-190">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25a8e-191">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-192">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-193">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-194">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-195">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-196">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-197">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-198">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-199">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25a8e-200">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25a8e-201">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25a8e-202">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="25a8e-203">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="25a8e-204">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="25a8e-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="25a8e-205">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-206">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-207">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-208">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-208">Billed sales</span></span></td>
<td><span data-ttu-id="25a8e-209">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25a8e-210">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25a8e-211">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25a8e-212">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-213">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-214">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-215">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-216">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="25a8e-217">리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다</span><span class="sxs-lookup"><span data-stu-id="25a8e-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="25a8e-218">이벤트</span><span class="sxs-lookup"><span data-stu-id="25a8e-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="25a8e-219">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="25a8e-220">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="25a8e-221">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="25a8e-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="25a8e-222">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="25a8e-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="25a8e-223">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="25a8e-224">실제</span><span class="sxs-lookup"><span data-stu-id="25a8e-224">Actuals</span></span></th>
<th><span data-ttu-id="25a8e-225">거래 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-225">Transaction currency</span></span></th>
<th><span data-ttu-id="25a8e-226">고정 가격</span><span class="sxs-lookup"><span data-stu-id="25a8e-226">Fixed price</span></span></th>
<th><span data-ttu-id="25a8e-227">거래 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="25a8e-228">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="25a8e-229">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-230">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="25a8e-231">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="25a8e-232">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25a8e-233">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-233">Cost actual</span></span></td>
<td><span data-ttu-id="25a8e-234">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="25a8e-235">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="25a8e-236">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="25a8e-237">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="25a8e-238">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-239">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="25a8e-240">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-241">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="25a8e-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="25a8e-242">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-243">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="25a8e-244">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="25a8e-245">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="25a8e-246">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-246">Cost actual</span></span></td>
<td><span data-ttu-id="25a8e-247">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-248">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-249">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-250">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-251">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="25a8e-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-252">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="25a8e-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="25a8e-253">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-254">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="25a8e-255">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-256">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-257">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-258">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-259">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25a8e-260">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25a8e-261">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25a8e-262">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-263">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-264">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-265">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="25a8e-266">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-267">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-267">Billed sales</span></span></td>
<td><span data-ttu-id="25a8e-268">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25a8e-269">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="25a8e-270">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="25a8e-271">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-272">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-273">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-274">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="25a8e-275">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-276">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-277">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-278">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-279">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="25a8e-280">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25a8e-281">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25a8e-282">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="25a8e-283">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="25a8e-284">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="25a8e-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="25a8e-285">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-286">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="25a8e-287">해당 없음</span><span class="sxs-lookup"><span data-stu-id="25a8e-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-288">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-288">Billed sales</span></span></td>
<td><span data-ttu-id="25a8e-289">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="25a8e-290">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="25a8e-291">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="25a8e-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="25a8e-292">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-293">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="25a8e-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="25a8e-294">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25a8e-295">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="25a8e-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="25a8e-296">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="25a8e-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]