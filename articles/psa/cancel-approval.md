---
title: 이전에 승인된 시간 및 경비 항목 취소
description: 이 주제는 승인된 프로젝트 시간 및 경비 처리를 취소하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290862"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="77c2b-103">이전에 승인된 시간 또는 경비 항목 취소</span><span class="sxs-lookup"><span data-stu-id="77c2b-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="77c2b-104">최신 버전의 Dynamics 365 Project Service Automation에서 결재자는 이전에 승인한 시간 또는 경비 항목을 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="77c2b-105">이전에 승인된 시간 또는 경비 항목 취소</span><span class="sxs-lookup"><span data-stu-id="77c2b-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="77c2b-106">다음 단계에 따라 이전에 승인한 시간 또는 경비 항목을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="77c2b-107">**프로젝트** \> **내 작업** \> **결재** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="77c2b-108">**결재** 목록 페이지에서 보기를 **내 과거 결재** 로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="77c2b-109">이전에 승인한 시간 및 경비 항목 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="77c2b-110">하나 이상의 항목을 선택한 다음 **승인 취소** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="77c2b-111">경고 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-111">You receive a warning message.</span></span>
4. <span data-ttu-id="77c2b-112">**OK** 를 선택하여 승인을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="77c2b-113">시간 또는 경비 항목 승인 취소의 영향 이해</span><span class="sxs-lookup"><span data-stu-id="77c2b-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="77c2b-114">승인이 취소되면 운영상의 영향과 재무적 영향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="77c2b-115">운영상의 영향</span><span class="sxs-lookup"><span data-stu-id="77c2b-115">Operational impact</span></span>

<span data-ttu-id="77c2b-116">운영 측면에서는 승인이 취소되면 레코드 상태가 **초안** 으로 재설정되고 승인이 **내 과거 결재** 보기에 더 이상 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="77c2b-117">그 대신 취소된 승인은 그것이 시간 항목이냐 경비 항목이냐에 따라 **결재 대상 시간 항목** 보기 또는 **결재 대상 경비 항목** 보기에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="77c2b-118">또한 관련 시간 또는 경비 항목의 상태가 **제출됨** 으로 변경되어 관련 항목이 **초안** 상태에 있는 결재와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="77c2b-119">결재자로서 귀하는 **초안** 상태에 있는 승인 필드 중 일부를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="77c2b-120">이러한 필드로는 **청구 타입** 과 **시간 항목에 대한 청구 가능 시간** 이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="77c2b-121">변경한 후 레코드를 다시 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="77c2b-122">또는 항목을 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="77c2b-123">시간 항목의 승인을 거부하면 항목 상태가 **반려됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="77c2b-124">경비 항목의 승인을 거부하면 항목 상태가 **거부됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="77c2b-125">기능적으로 설명하면, 반려된 항목과 거부된 항목은 **초안** 상태에 있는 항목과 동일하게 기능합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="77c2b-126">프로젝트 팀원은 항목에 필요한 사항을 변경한 다음 결재를 위해 항목을 다시 제출하거나 항목을 완전히 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="77c2b-127">재무적 영향</span><span class="sxs-lookup"><span data-stu-id="77c2b-127">Financial impact</span></span>

<span data-ttu-id="77c2b-128">승인이 취소되면 프로젝트는 재정적으로도 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="77c2b-129">첫째, 비용 및 판매에 대한 해당 실제값이 다음과 같은 방식으로 업데이트됩니다:</span><span class="sxs-lookup"><span data-stu-id="77c2b-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="77c2b-130">조정 상태가 **조정됨** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="77c2b-131">청구 상태가 **취소됨** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="77c2b-132">다음으로 반전 항목이 실제값 표에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="77c2b-133">반전 항목을 만들기 위해 시스템은 원래 실제값의 필드 값을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="77c2b-134">복사되지 않는 값은 수량 값뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="77c2b-135">대신 이러한 값이 반전됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-135">These values are reversed instead.</span></span> <span data-ttu-id="77c2b-136">**원가** 및 **미청구 매출액** 의 실제값에 대한 반전된 실제값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="77c2b-137">반전된 실제값의 **조정 상태** 필드가 **조정 불가능** 으로 설정되고, 청구 상태가 **취소됨** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="77c2b-138">이러한 변경이 이루어지면 프로젝트에 지출된 것으로 기록된 금액과 프로젝트의 수익 백로그가 더 이상 이러한 실제값이 나타내는 금액을 해명하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="77c2b-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]