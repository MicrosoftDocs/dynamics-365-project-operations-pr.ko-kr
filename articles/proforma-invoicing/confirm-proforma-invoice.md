---
title: 견적 프로젝트 기반 송장 확인
description: 이 항목은 견적 프로젝트 기반 송장 확인에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867139"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="10ccc-103">견적 프로젝트 기반 송장 확인</span><span class="sxs-lookup"><span data-stu-id="10ccc-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="10ccc-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="10ccc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="10ccc-105">견적 송장이 확인되면 프로젝트 송장의 상태가 **확인됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="10ccc-106">송장이 확인되면 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="10ccc-107">앞으로 송장은 고객이 시작한 수정 또는 크레딧이 있는 경우에만 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="10ccc-108">다음 표는 시스템에서 작성된 실제 값을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="10ccc-109">이러한 실제는 확정되기 전에 프로젝트 송장 초안에 대해 특정 작업이 수행될 때 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="10ccc-110">
                    <strong>시나리오</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10ccc-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="10ccc-111">
                    <strong>확정시 생성된 실제</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10ccc-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-112">선불 또는 보유자 송장 발행</span><span class="sxs-lookup"><span data-stu-id="10ccc-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-113">청구된 실제 판매 유형인 <strong>보유자</strong>는 선불 또는 보유자의 금액에 대해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-114">조정에 사용할 대출금 또는 대출 금액이 음수인 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-115">송장의 보유자 또는 선불을 완전히 조정한 후.</span><span class="sxs-lookup"><span data-stu-id="10ccc-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-116">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="10ccc-117">이 금액은 보유자 또는 선불이 청구될 때 생성된 음수를 취소하기 위한 것이므로 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-118">이 송장의 금액에 대한 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10ccc-119">송장의 보유자 또는 선불을 부분 조정한 후.</span><span class="sxs-lookup"><span data-stu-id="10ccc-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-120">조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="10ccc-121">이 금액은 보유자 또는 선불이 청구될 때 생성된 음수를 취소하기 위한 것이므로 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="10ccc-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-122">이 송장의 금액에 대한 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-123">향후 송장의 조정에 사용할 나머지 보유자 또는 선불 금액의 음수 청구되지 않은 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-124">초안 송장을 편집하지 않고 시간 트랜잭션을 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-125">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-126">최초 시간 승인의 시간 및 금액에 대해 청구된 실제 판매</span><span class="sxs-lookup"><span data-stu-id="10ccc-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10ccc-127">수량을 줄이기 위해 편집된 시간 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-128">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-129">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-130">편집된 송장 라인 상세 내역에서 수정된 수치를 공제한 후 남은 시간 및 금액에 대해 청구할 수 없는 신규 미청구 실제 판매, 실제 판매의 취소 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-131">수량을 늘리기 위해 편집된 시간 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-132">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-133">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-134">초안 송장을 편집하지 않고 경비 트랜잭션을 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-135">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-136">최초 경비 승인의 수량 및 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10ccc-137">수량을 줄이기 위해 편집된 경비 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-138">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-139">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-140">편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 수량 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-141">수량을 늘리기 위해 편집된 경비 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-142">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-143">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-144">송장 초안을 편집하지 않고 자재 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-145">최초 자재 사용 승인의 수량 및 금액에 대한 미청구 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="10ccc-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-146">최초 자재 사용 승인의 수량 및 금액에 대해 실제 청구된 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10ccc-147">수량을 줄이기 위해 편집된 자재 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-148">최초 승인시 수량 및 금액에 대한 미청구 판매 취소</span><span class="sxs-lookup"><span data-stu-id="10ccc-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-149">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-150">편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 수량 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-151">수량 증가를 위해 편집된 자재 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-152">최초 자재 사용 승인의 수량 및 금액에 대한 미청구 판매 취소.</span><span class="sxs-lookup"><span data-stu-id="10ccc-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-153">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10ccc-154">수수료 청구.</span><span class="sxs-lookup"><span data-stu-id="10ccc-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-155">최초 분개장 항목의 수수료 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="10ccc-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-156">최초 수수료 분개장 항목의 수량 및 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="10ccc-157">중요 시점 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="10ccc-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10ccc-158">프로젝트 계약 내용의 원래 중요 시점에 있는 중요 시점 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="10ccc-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
