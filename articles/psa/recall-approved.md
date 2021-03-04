---
title: 승인된 시간 또는 경비 항목 철회
description: 이 주제는 이전에 승인된 프로젝트 시간 또는 경비 처리를 철회하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147850"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="0dab4-103">승인된 시간 또는 경비 항목 철회</span><span class="sxs-lookup"><span data-stu-id="0dab4-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0dab4-104">프로젝트 팀원 또는 기타 시간 또는 경비 항목을 제출한 사람은 승인된 후 해당 시간 또는 경비 항목을 철회할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="0dab4-105">승인된 시간 또는 경비 항목을 철회하는 프로세스에는 두 가지 단계가 있습니다:</span><span class="sxs-lookup"><span data-stu-id="0dab4-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="0dab4-106">제출인이 철회를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="0dab4-107">승인자가 철회를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="0dab4-108">철회 요청</span><span class="sxs-lookup"><span data-stu-id="0dab4-108">Request a recall</span></span>

<span data-ttu-id="0dab4-109">다음 단계에 따라 승인된 시간 또는 경비 항목의 철회를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="0dab4-110">시간 항목의 경우 **프로젝트** \> **내 작업** \> **시간 항목** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="0dab4-111">-또는-</span><span class="sxs-lookup"><span data-stu-id="0dab4-111">–or–</span></span>

    <span data-ttu-id="0dab4-112">경비 항목의 경우 **프로젝트** \> **내 작업** \> **경비** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="0dab4-113">시간 항목의 경우 프로젝트와 과업의 특정 조합에 대한 모든 시간 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="0dab4-114">또는 그리드에서 특정 프로젝트의 특정 날짜에 대한 개별 셀을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="0dab4-115">-또는-</span><span class="sxs-lookup"><span data-stu-id="0dab4-115">–or–</span></span>

    <span data-ttu-id="0dab4-116">경비 항목의 경우 철회할 경비 항목에 대한 행을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="0dab4-117">**철회** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-117">Select **Recall**.</span></span> <span data-ttu-id="0dab4-118">확인 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="0dab4-119">선택한 시간 및 경비 항목이 이미 승인된 경우 철회 이유를 입력하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="0dab4-120">철회 이유를 입력한 다음 **OK** 를 선택하여 조작을 확정합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="0dab4-121">시스템은 항목을 승인한 사람에게 철회 승인 요청을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="0dab4-122">승인된 시간 및 경비 항목을 철회할 수 있지만 승인된 시간 또는 경비가 이미 고객에게 청구된 경우에는 철회 요청을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="0dab4-123">철회 요청을 만들려고 시도하는 사용자는 이미 청구서가 발부되었기 때문에 시간 또는 경비를 철회할 수 없다는 메시지를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="0dab4-124">철회 요청 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="0dab4-124">Approve or reject a recall request</span></span>

<span data-ttu-id="0dab4-125">다음 단계에 따라 철회 요청을 승인하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="0dab4-126">**프로젝트** \> **내 작업** \> **결재** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="0dab4-127">**결재** 목록 페이지에서 보기를 **승인을 위한 철회 요청** 으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="0dab4-128">제출된 철회 요청 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="0dab4-129">하나 이상의 항목을 선택한 다음 **승인** 또는 **거부** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="0dab4-130">**승인** 을 선택한 경우 승인의 영향을 설명하는 경고 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="0dab4-131">**OK** 를 선택하여 조작을 확정합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="0dab4-132">철회 요청이 승인됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-132">The recall request is approved.</span></span>

    <span data-ttu-id="0dab4-133">-또는-</span><span class="sxs-lookup"><span data-stu-id="0dab4-133">–or–</span></span>

    <span data-ttu-id="0dab4-134">**거부** 를 선택한 경우 철회 요청이 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="0dab4-135">철회가 요청될 때와 마찬가지로 철회가 승인되면 시스템은 시간 또는 경비 항목에 대한 청구서 활동을 점검합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="0dab4-136">항목이 이미 청구서 발부되었거나 초안 청구서에 있는 경우 이미 청구서 발행된 상태이기 때문에 승인자는 시간 또는 경비 철회를 승인할 수 없다는 오류 메시지를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="0dab4-137">철회 요청의 영향</span><span class="sxs-lookup"><span data-stu-id="0dab4-137">Impact of a recall request</span></span>

<span data-ttu-id="0dab4-138">승인이 철회되면 운영상의 영향과 재무적 영향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="0dab4-139">운영상의 영향</span><span class="sxs-lookup"><span data-stu-id="0dab4-139">Operational impact</span></span>

<span data-ttu-id="0dab4-140">철회 요청이 승인되면 승인 레코드가 **거부됨** 으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="0dab4-141">항목의 상태는 시간 항목 또는 경비 항목에 따라 **반환됨** 또는 **거부됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="0dab4-142">프로젝트 팀원은 항목을 보고, 항목을 편집한 다음 다시 제출하거나, 항목을 완전히 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="0dab4-143">철회 요청이 거부되면 항목의 상태가 **승인됨** 상태로 유지되며 프로젝트 팀원 또는 프로젝트 승인자가 항목을 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="0dab4-144">재무적 영향</span><span class="sxs-lookup"><span data-stu-id="0dab4-144">Financial impact</span></span>

<span data-ttu-id="0dab4-145">철회 요청이 승인되면, 원가 및 매출액에 대한 해당 실제값이 다음과 같은 방식으로 업데이트됩니다:</span><span class="sxs-lookup"><span data-stu-id="0dab4-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="0dab4-146">**조정 상태** 필드가 **조정됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="0dab4-147">**청구 상태** 필드가 **취소됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="0dab4-148">다음으로 반전 항목이 실제값 표에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="0dab4-149">반전 항목을 만들기 위해 시스템은 원래 실제값의 필드 값을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="0dab4-150">복사되지 않는 값은 수량 값뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="0dab4-151">대신 이러한 값이 반전됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-151">These values are reversed instead.</span></span> <span data-ttu-id="0dab4-152">**원가** 및 **미청구 매출액** 의 실제값에 대한 반전된 실제값이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="0dab4-153">반전된 실제값의 **조정 상태** 필드가 **조정 불가능** 으로 설정되고, **청구 상태** 필드가 **취소됨** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="0dab4-154">이러한 변경 때문에 프로젝트에 기록된 지출과 수익 백로그가 더 이상 이러한 실제값이 나타내는 금액을 해명하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="0dab4-155">철회 요청이 거부되면 프로젝트에 재무적 영향이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="0dab4-156">시간 항목 레코드 변경</span><span class="sxs-lookup"><span data-stu-id="0dab4-156">Changes to time entry records</span></span>

<span data-ttu-id="0dab4-157">다음 그림은 승인된 시간 항목에 대해 철회될 때 발생하는 변경 사항을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![시간 항목 상태 전환](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="0dab4-159">경비 항목 레코드 변경</span><span class="sxs-lookup"><span data-stu-id="0dab4-159">Changes to expense entry records</span></span>

<span data-ttu-id="0dab4-160">다음 그림은 승인된 경비 항목에 대해 철회될 때 발생하는 변경 사항을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0dab4-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![경비 항목 상태 전환](media/ExpenseEntryStateTransitions.png)
