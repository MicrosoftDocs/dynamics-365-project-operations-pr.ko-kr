---
title: 견적 송장 확인
description: 이 항목에서는 견적 송장 확인에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128111"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="02f79-103">견적 송장 확인</span><span class="sxs-lookup"><span data-stu-id="02f79-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="02f79-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="02f79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="02f79-105">견적 송장이 확인되면 프로젝트 송장의 상태가 **확인됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f79-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="02f79-106">송장이 확인되면 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f79-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="02f79-107">앞으로 송장이 지불된 것으로 표시된 경우 고객이 시작한 수정 또는 크레딧이 있는 경우에만 송장을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02f79-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="02f79-108">다음 표는 시스템에서 작성된 실제 값을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="02f79-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="02f79-109">이러한 실제는 확정되기 전에 프로젝트 송장 초안에 대해 특정 작업이 수행될 때 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f79-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="02f79-110">
                    <strong>시나리오</strong>
                </span><span class="sxs-lookup"><span data-stu-id="02f79-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="02f79-111">
                    <strong>확정시 생성된 실제</strong>
                </span><span class="sxs-lookup"><span data-stu-id="02f79-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02f79-112">초안 송장을 편집하지 않고 시간 트랜잭션을 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-113">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-114">최초 시간 승인의 시간 및 금액에 대해 청구된 실제 판매</span><span class="sxs-lookup"><span data-stu-id="02f79-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="02f79-115">수량을 줄이기 위해 편집된 시간 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-116">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-117">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-118">편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 시간 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02f79-119">수량을 늘리기 위해 편집된 시간 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-120">최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-121">편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02f79-122">초안 송장을 편집하지 않고 경비 트랜잭션을 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-123">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-124">최초 경비 승인의 수량 및 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="02f79-125">수량을 줄이기 위해 편집된 경비 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-126">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-127">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-128">편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 수량 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02f79-129">수량을 늘리기 위해 편집된 경비 트랜잭션 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-130">최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-131">편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="02f79-132">수수료 청구.</span><span class="sxs-lookup"><span data-stu-id="02f79-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-133">최초 분개장 항목의 수수료 금액에 대한 청구되지 않은 매출액 전환.</span><span class="sxs-lookup"><span data-stu-id="02f79-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-134">최초 수수료 분개장 항목의 수량 및 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="02f79-135">중요 시점 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="02f79-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="02f79-136">프로젝트 계약 내용의 원래 중요 시점에 있는 중요 시점 금액에 대해 청구된 실제 판매.</span><span class="sxs-lookup"><span data-stu-id="02f79-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
