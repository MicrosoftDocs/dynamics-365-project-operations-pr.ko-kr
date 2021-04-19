---
title: 수정 프로젝트 기반 송장 만들기
description: 이 항목은 Project Operations의 수정 송장에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788874"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="7fc42-103">수정 프로젝트 기반 송장 만들기</span><span class="sxs-lookup"><span data-stu-id="7fc42-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="7fc42-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7fc42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7fc42-105">확인된 프로젝트 송장을 수정하여 고객 및 프로젝트 관리자와 협상한 대로 변경 또는 대변을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="7fc42-106">확인된 송장을 편집하려면 확인된 송장을 열고 **이 송장 수정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="7fc42-107">이 선택은 프로젝트 송장이 확인되지 않으면 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="7fc42-108">확인된 송장에서 새 송장 초안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="7fc42-109">이전에 확인된 송장의 모든 송장 라인 상세 내역이 신규 초안에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="7fc42-110">다음은 새로 수정된 송장의 라인 세부 사항에 대한 자세한 내용을 이해하는 데 도움이 되는 몇 가지 핵심 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="7fc42-111">모든 수량이 0으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-111">All quantities are updated to zero.</span></span> <span data-ttu-id="7fc42-112">이는 모든 송장 항목이 완전히 입금되었다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="7fc42-113">필요한 경우 차감되는 수량이 아니라 송장이 발행되는 수량을 반영하도록 이러한 수량을 수동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="7fc42-114">입력한 수량에 따라 응용 프로그램이 대변 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="7fc42-115">이 금액은 수정된 송장이 확인될 때 생성된 실제 금액에 반영됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="7fc42-116">세액을 변경하는 경우 공제되는 세액이 아니라 정확한 세액을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="7fc42-117">중요 시점 수정은 항상 전체 크레딧으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="7fc42-118">고객에게 잘못된 금액이 청구된 경우 보유자 또는 선급 금액을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="7fc42-119">이전에 확인된 송장의 요금을 조정하는 데 잘못된 금액이 사용된 경우 보유자 및 선불의 조정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fc42-120">이미 송장이 발행된 다른 경비에 대한 수정인 송장 라인 상세 내역에는 **수정** 필드가 **예** 로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="7fc42-121">송장 라인 상세 내역이 수정된 송장에는 **수정 사항 있음** 필드도 **예** 로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="7fc42-122">수정 송장 확인시 생성된 실제</span><span class="sxs-lookup"><span data-stu-id="7fc42-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="7fc42-123">다음 표에는 수정 송장이 확인될 때 생성되는 실제 항목이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7fc42-124">
                    <strong>시나리오</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7fc42-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7fc42-125">
                    <strong>확정시 생성된 실제</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7fc42-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7fc42-126">송장 선불 또는 보유자의 수정을 확인합니다.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7fc42-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-127">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7fc42-128">이 금액은 보유자 또는 선불이 청구될 때 생성된 음수를 취소하기 위한 것이므로 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-129">원래 청구된 판매를 취소하기 위해 보유자의 금액에 대해 청구된 판매 취소 실제 값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-130">보유자 또는 선불 기반 수정 송장 라인의 수정된 금액에 대해 신규 청구된 판매 실제 값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-131">조정에 사용되는 보유자 또는 선불 기반 수정된 송장 라인의 음수 금액의 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7fc42-132">이전에 조정된 보유자 또는 선불의 수정 확인.</span><span class="sxs-lookup"><span data-stu-id="7fc42-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-133">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7fc42-134">이 금액은 양수이며 이전 조정이 발생했을 때 생성된 음수를 취소하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-135">이전 송장의 금액에 대한 실제 청구된 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="7fc42-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-136">수정된 송장에 적용되는 수정된 보유자 금액에 대한 신규 청구된 판매 실제 값.</span><span class="sxs-lookup"><span data-stu-id="7fc42-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-137">수정된 잔여 보유자 또는 선불에서 음수 금액이 있고 이후 송장의 조정에 사용되는 미청구된 판매 실제 값.</span><span class="sxs-lookup"><span data-stu-id="7fc42-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7fc42-138">이전에 청구된 시간 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-139">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-140">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7fc42-141">시간 트랜잭션에 대한 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-142">시간에 대한 최초 송장 라인 상세 내역의 시간 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-143">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-144">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7fc42-145">이전에 청구된 경비 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-146">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-147">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7fc42-148">이전에 청구된 경비 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-149">경비에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-150">수정된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-151">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7fc42-152">이전에 청구된 요금 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-153">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-154">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7fc42-155">이전에 청구된 요금 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-156">요금에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-157">편집된 수정 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="7fc42-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7fc42-158">이전에 청구된 중요 시점의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-159">중요 시점에 대한 최초 송장 라인 상세 내역의 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="7fc42-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="7fc42-160">이정표의 송장 상태는 <b>고객 송장 게시됨</b>에서 <b>송장 발부 준비 완료</b>로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc42-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7fc42-161">이전에 청구된 중요 시점의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="7fc42-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7fc42-162">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="7fc42-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
