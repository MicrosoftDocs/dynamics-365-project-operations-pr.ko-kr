---
title: 크레딧 및 수정된 송장
description: 이 항목은 Project Operations에서 수정된 송장에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080163"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="d82ef-103">크레딧 및 수정된 송장</span><span class="sxs-lookup"><span data-stu-id="d82ef-103">Credits and corrected invoices</span></span>

<span data-ttu-id="d82ef-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="d82ef-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d82ef-105">확인된 프로젝트 송장을 수정하여 고객 및 프로젝트 관리자와 협상한 대로 변경 또는 대변을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="d82ef-106">확인된 송장을 편집하려면 확인된 송장을 열고 **이 송장 수정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d82ef-107">이 선택은 프로젝트 송장이 확인되지 않으면 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="d82ef-108">확인된 송장에서 새 송장 초안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="d82ef-109">이전에 확인된 송장의 모든 송장 라인 상세 내역이 신규 초안에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="d82ef-110">다음은 새로 수정된 송장의 라인 세부 정보에 대해 이해해야 할 몇 가지 핵심 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="d82ef-111">모든 수량이 0으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-111">All quantities are updated to zero.</span></span> <span data-ttu-id="d82ef-112">응용 프로그램은 모든 송장 항목이 완전히 입금되었다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="d82ef-113">필요한 경우 차감되는 수량이 아니라 송장이 발행되는 수량을 반영하도록 이러한 수량을 수동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="d82ef-114">입력한 수량에 따라 응용 프로그램이 대변 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="d82ef-115">이 금액은 수정된 송장이 확인될 때 생성된 실제 금액에 반영됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="d82ef-116">세액을 변경하는 경우 공제되는 세액이 아니라 정확한 세액을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="d82ef-117">이전에 확인된 제품 기반 계약 내용은 복사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="d82ef-118">제품 기반 프로젝트 송장에 대한 수정 처리는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="d82ef-119">중요 시점 수정은 항상 전체 크레딧으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="d82ef-120">고객에게 잘못된 금액이 청구된 경우 보유자 또는 선급 금액을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="d82ef-121">이전에 확인된 송장의 요금을 조정하는 데 잘못된 금액이 사용된 경우 보유자 및 선불의 조정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d82ef-122">이미 송장이 발행된 다른 비용에 대한 수정인 송장 라인 상세 내역에는 **수정** 필드가 **예** 로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="d82ef-123">송장 라인 상세 내역이 수정된 송장에는 **수정 사항 있음** 필드도 **예** 로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="d82ef-124">수정 송장 확인시 생성된 실제:</span><span class="sxs-lookup"><span data-stu-id="d82ef-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="d82ef-125">다음은 확인 전에 초안 수정 송장에 대해 수행된 작업을 기반으로 수정 확인시 응용 프로그램에서 생성한 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d82ef-126">
                    <strong>시나리오</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d82ef-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d82ef-127">
                    <strong>확정시 생성된 실제</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d82ef-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d82ef-128">송장 선불 또는 보유자의 수정을 확인합니다.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d82ef-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-129">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d82ef-130">이 금액은 보유자 또는 선불이 청구될 때 생성된 음수를 취소하기 위한 것이므로 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-131">원래 청구된 판매를 취소하기 위해 보유자의 금액에 대해 청구된 판매 취소 실제 값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-132">보유자 또는 선불 기반 수정 송장 라인의 수정된 금액에 대해 신규 청구된 판매 실제 값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-133">조정에 사용되는 보유자 또는 선불 기반 수정된 송장 라인의 음수 금액의 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d82ef-134">이전에 조정된 보유자 또는 선불의 수정 확인.</span><span class="sxs-lookup"><span data-stu-id="d82ef-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-135">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d82ef-136">이 금액은 양수이며 이전 조정이 발생했을 때 생성된 음수를 취소하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-137">이전 송장의 금액에 대한 실제 청구된 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="d82ef-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-138">수정된 송장에 적용되는 수정된 보유자 금액에 대한 신규 청구된 판매 실제 값.</span><span class="sxs-lookup"><span data-stu-id="d82ef-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-139">수정된 잔여 보유자 또는 선불에서 음수 금액이 있고 이후 송장의 조정에 사용되는 미청구된 판매 실제 값.</span><span class="sxs-lookup"><span data-stu-id="d82ef-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d82ef-140">이전에 청구된 시간 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-141">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-142">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d82ef-143">시간 트랜잭션에 대한 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-144">시간에 대한 최초 송장 라인 상세 내역의 시간 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-145">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-146">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d82ef-147">이전에 청구된 경비 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-148">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-149">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d82ef-150">이전에 청구된 경비 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-151">경비에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-152">수정된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-153">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d82ef-154">이전에 청구된 요금 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-155">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-156">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d82ef-157">이전에 청구된 요금 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-158">요금에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-159">편집된 수정 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="d82ef-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d82ef-160">이전에 청구된 중요 시점의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-161">중요 시점에 대한 최초 송장 라인 상세 내역의 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="d82ef-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="d82ef-162">프로젝트 계약 내용의 중요 시점 송장 또는 청구 상태가 **송장 준비** 로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="d82ef-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d82ef-163">이전에 청구된 중요 시점의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="d82ef-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-164">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="d82ef-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d82ef-165">이전에 송장을 발행한 제품 기반 계약 내용의 크레딧 및 수정.</span><span class="sxs-lookup"><span data-stu-id="d82ef-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d82ef-166">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="d82ef-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
