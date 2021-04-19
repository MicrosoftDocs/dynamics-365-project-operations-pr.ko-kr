---
title: 수정 프로젝트 기반 송장
description: 이 항목은 Project Operations에서 수정 프로젝트 기반 송장을 만들고 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867049"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="136e3-103">수정 프로젝트 기반 송장</span><span class="sxs-lookup"><span data-stu-id="136e3-103">Corrective project-based invoices</span></span>

<span data-ttu-id="136e3-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="136e3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="136e3-105">확인된 프로젝트 송장을 수정하여 고객 및 프로젝트 관리자와 협상한 대로 변경 또는 대변을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="136e3-106">확인된 송장을 편집하려면 확인된 송장을 열고 **이 송장 수정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="136e3-107">이 선택 사항은 프로젝트 송장이 확인되거나 프로젝트 기반 송장에 선금 또는 보유자 또는 대출 또는 보유자의 조정이 있는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="136e3-108">확인된 송장에서 새 송장 초안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="136e3-109">이전에 확인된 송장의 모든 송장 라인 상세 내역이 신규 초안에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="136e3-110">다음은 새로 수정된 송장의 라인 세부 정보에 대해 이해해야 할 몇 가지 핵심 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="136e3-111">모든 수량이 0으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-111">All quantities are updated to zero.</span></span> <span data-ttu-id="136e3-112">Dynamics 365 Project Operations에서는 모든 송장 항목이 완전히 입금되었다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="136e3-113">필요한 경우 차감되는 수량이 아니라 송장이 발행되는 수량을 반영하도록 이러한 수량을 수동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="136e3-114">입력한 수량에 따라 응용 프로그램이 대변 수량을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="136e3-115">이 금액은 수정된 송장이 확인될 때 생성된 실제 금액에 반영됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="136e3-116">세액을 변경하는 경우 공제되는 세액이 아니라 정확한 세액을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="136e3-117">중요 시점 수정은 항상 전체 크레딧으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="136e3-118">이미 송장이 발행된 다른 경비에 대한 수정인 송장 라인 상세 내역에는 **수정** 필드가 **예** 로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="136e3-119">송장 라인 세부 정보가 수정된 송장의 경우 **수정 사항 있음** 필드가 **예** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="136e3-120">수정 송장 확인시 생성된 실제</span><span class="sxs-lookup"><span data-stu-id="136e3-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="136e3-121">다음 표에는 수정 송장이 확인될 때 생성되는 실제 항목이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="136e3-122">
                    <strong>시나리오</strong>
                </span><span class="sxs-lookup"><span data-stu-id="136e3-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="136e3-123">
                    <strong>확정시 생성된 실제</strong>
                </span><span class="sxs-lookup"><span data-stu-id="136e3-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="136e3-124">이전에 청구된 시간 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-125">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-126">시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="136e3-127">시간 트랜잭션에 대한 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-128">시간에 대한 최초 송장 라인 상세 내역의 시간 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-129">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-130">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="136e3-131">이전에 청구된 경비 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-132">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-133">경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="136e3-134">이전에 청구된 경비 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-135">경비에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-136">수정된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-137">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="136e3-138">이전에 송장을 발행한 재료 트랜잭션의 전체 대변 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-139">재료에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="136e3-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-140">재료에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 실제 신규 미청구 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="136e3-141">재료 트랜잭션에 대한 부분 신용 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-142">재료에 대한 최초 송장 라인 상세 내역의 송장 발부된 수량 및 금액에 대한 청구된 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="136e3-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-143">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 미청구 판매 실제, 이것의 취소 및 이에 상응하는 청구된 판매 실제.</span><span class="sxs-lookup"><span data-stu-id="136e3-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-144">송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="136e3-145">이전에 청구된 요금 트랜잭션의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-146">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-147">요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="136e3-148">이전에 청구된 요금 트랜잭션의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-149">요금에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-150">편집된 수정 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="136e3-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="136e3-151">이전에 청구된 중요 시점의 전체 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-152">중요 시점에 대한 최초 송장 라인 상세 내역의 금액에 대한 청구된 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="136e3-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="136e3-153">이정표의 송장 상태는 <b>고객 송장 게시됨</b>에서 <b>송장 발부 준비 완료</b>로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="136e3-154">이전에 청구된 중요 시점의 부분 크레딧 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="136e3-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="136e3-155">이 시나리오는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="136e3-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
