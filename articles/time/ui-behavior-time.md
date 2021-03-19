---
title: 시간 항목 UI 동작
description: 이 항목은 시간 항목의 UI 동작에 대한 정보를 제공합니다.
author: stsporen
manager: AnnBe
ms.date: 03/03/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b552266eddc4efc1b41fc500d157239388ad219b
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499622"
---
# <a name="time-entry-ui-behavior"></a><span data-ttu-id="16bf7-103">시간 항목 UI 동작</span><span class="sxs-lookup"><span data-stu-id="16bf7-103">Time entry UI behavior</span></span>

<span data-ttu-id="16bf7-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="16bf7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="16bf7-105">**주간 시간 항목** 그리드는 두 개의 주요 섹션인 **크기** 및 **기간** 이 있는 사용자 지정 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-105">The **Weekly time entry** grid is a custom control that has two main sections, **Dimensions** and **Duration**.</span></span>

## <a name="keyboard-shortcuts"></a><span data-ttu-id="16bf7-106">바로 가기 키</span><span class="sxs-lookup"><span data-stu-id="16bf7-106">Keyboard shortcuts</span></span>
| <span data-ttu-id="16bf7-107">작업</span><span class="sxs-lookup"><span data-stu-id="16bf7-107">Action</span></span>        | <span data-ttu-id="16bf7-108">바로 가기</span><span class="sxs-lookup"><span data-stu-id="16bf7-108">Shortcut</span></span>                  |
|------------   |------------------------   |
| <span data-ttu-id="16bf7-109">새 알림</span><span class="sxs-lookup"><span data-stu-id="16bf7-109">New</span></span>           | <span data-ttu-id="16bf7-110">Alt + Shift + n</span><span class="sxs-lookup"><span data-stu-id="16bf7-110">Alt + Shift + n</span></span>           |
| <span data-ttu-id="16bf7-111">행 복사</span><span class="sxs-lookup"><span data-stu-id="16bf7-111">Copy row</span></span>      | <span data-ttu-id="16bf7-112">Alt + Shift + c</span><span class="sxs-lookup"><span data-stu-id="16bf7-112">Alt + Shift + c</span></span>           |
| <span data-ttu-id="16bf7-113">항목 편집</span><span class="sxs-lookup"><span data-stu-id="16bf7-113">Edit 3ntry</span></span>    | <span data-ttu-id="16bf7-114">Alt + Shift + e</span><span class="sxs-lookup"><span data-stu-id="16bf7-114">Alt + Shift + e</span></span>           |
| <span data-ttu-id="16bf7-115">행 편집</span><span class="sxs-lookup"><span data-stu-id="16bf7-115">Edit row</span></span>      | <span data-ttu-id="16bf7-116">Alt + Shift + Ctrl + e</span><span class="sxs-lookup"><span data-stu-id="16bf7-116">Alt + Shift + Ctrl + e</span></span>    |
| <span data-ttu-id="16bf7-117">항목 열기</span><span class="sxs-lookup"><span data-stu-id="16bf7-117">Open 3ntry</span></span>    | <span data-ttu-id="16bf7-118">Alt + Shift + o</span><span class="sxs-lookup"><span data-stu-id="16bf7-118">Alt + Shift + o</span></span>           |
| <span data-ttu-id="16bf7-119">제출</span><span class="sxs-lookup"><span data-stu-id="16bf7-119">Submit</span></span>        | <span data-ttu-id="16bf7-120">Alt + Shift + s</span><span class="sxs-lookup"><span data-stu-id="16bf7-120">Alt + Shift + s</span></span>           |
| <span data-ttu-id="16bf7-121">리콜</span><span class="sxs-lookup"><span data-stu-id="16bf7-121">Recall</span></span>        | <span data-ttu-id="16bf7-122">Alt + Shift + r</span><span class="sxs-lookup"><span data-stu-id="16bf7-122">Alt + Shift + r</span></span>           |
| <span data-ttu-id="16bf7-123">Delete</span><span class="sxs-lookup"><span data-stu-id="16bf7-123">Delete</span></span>        | <span data-ttu-id="16bf7-124">Alt + Shift + d</span><span class="sxs-lookup"><span data-stu-id="16bf7-124">Alt + Shift + d</span></span>           |
| <span data-ttu-id="16bf7-125">주 복사</span><span class="sxs-lookup"><span data-stu-id="16bf7-125">Copy week</span></span>     | <span data-ttu-id="16bf7-126">Alt + Shift + w</span><span class="sxs-lookup"><span data-stu-id="16bf7-126">Alt + Shift + w</span></span>           |

## <a name="dimensions"></a><span data-ttu-id="16bf7-127">차원</span><span class="sxs-lookup"><span data-stu-id="16bf7-127">Dimensions</span></span>
<span data-ttu-id="16bf7-128">**크기** 섹션에는 시간을 입력할 수 있는 크기가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-128">The **Dimensions** section shows the dimensions that time can be entered against.</span></span> <span data-ttu-id="16bf7-129">다음과 같은 크기가 기본 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-129">The following dimensions are supported out-of-the-box:</span></span>

  - <span data-ttu-id="16bf7-130">Project</span><span class="sxs-lookup"><span data-stu-id="16bf7-130">Project</span></span>
  - <span data-ttu-id="16bf7-131">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="16bf7-131">Project Task</span></span>
  - <span data-ttu-id="16bf7-132">역할</span><span class="sxs-lookup"><span data-stu-id="16bf7-132">Role</span></span>
  - <span data-ttu-id="16bf7-133">종류</span><span class="sxs-lookup"><span data-stu-id="16bf7-133">Type</span></span>
  - <span data-ttu-id="16bf7-134">항목 상태</span><span class="sxs-lookup"><span data-stu-id="16bf7-134">Entry Status</span></span>

<span data-ttu-id="16bf7-135">**크기** 섹션에서는 인라인 편집이 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-135">The **Dimensions** section doesn't allow inline editing.</span></span> <span data-ttu-id="16bf7-136">이 섹션은 사용자 지정 필드를 주간 시간 항목 표에 추가할 수 있는 보기에 의해 뒷받침됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-136">This section is backed by a view that enables custom fields to be added to the weekly time entry grid.</span></span>

## <a name="duration"></a><span data-ttu-id="16bf7-137">기간</span><span class="sxs-lookup"><span data-stu-id="16bf7-137">Duration</span></span>
<span data-ttu-id="16bf7-138">기간 섹션은 요일을 열 머리글로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-138">The Duration section shows the days of the week as column headers.</span></span> <span data-ttu-id="16bf7-139">이 섹션에서는 인라인 편집을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-139">This section allows inline editing.</span></span> <span data-ttu-id="16bf7-140">적절한 크기가 있는 시간 입력 행이 만들어지면 사용자는 해당 크기에 소요된 시간을 빠르게 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-140">After a time entry row is created with the appropriate dimensions, users can quickly enter the amount of time that they spent on those dimensions.</span></span>

## <a name="create-a-new-time-entry"></a><span data-ttu-id="16bf7-141">새 시간 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="16bf7-141">Create a new time entry</span></span>

1. <span data-ttu-id="16bf7-142">시간 항목 그리드에서 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-142">In the time entry grid, select **New**.</span></span> 
2. <span data-ttu-id="16bf7-143">**시간 항목 빨리 만들기** 대화 상자에서 시간 항목 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-143">In the **Time Entry Quick Create** dialog box, select the time entry date.</span></span>
3. <span data-ttu-id="16bf7-144">**프로젝트**, **프로젝트 작업**, **역할** 및 **기간** 크기에 데이터를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-144">Enter data for the **Project**, **Project Task**, **Role**, and **Duration** dimensions.</span></span> <span data-ttu-id="16bf7-145">이 정보는 숫자와 함께 **h**, **m** 또는 **d** 를 입력하여 분, 시간 또는 일에 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-145">This information should be added in minutes, hours, or days by typing **h**, **m**, or **d**, together with the number.</span></span> 
4. <span data-ttu-id="16bf7-146">항목에 대한 설명과 시간 항목과 관련하여 외부에서 공유할 수 있는 모든 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-146">Enter a description for the entry and any comments that can be shared externally regarding time entry.</span></span> 

<span data-ttu-id="16bf7-147">항목을 저장하면 입력한 값이 **크기** 섹션에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-147">When you save the entry, the entered values appear in the **Dimensions** section.</span></span> <span data-ttu-id="16bf7-148">**기간** 필드에 입력한 정보는 시간 항목이 생성된 날짜에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-148">The information entered in the **Duration** field appears on the date that the time entry was created for.</span></span>

<span data-ttu-id="16bf7-149">조회 필드는 시스템 보기에 의해 백업됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-149">Lookup fields are backed by system views.</span></span> <span data-ttu-id="16bf7-150">예를 들어 사용자가 프로젝트를 입력하면 **프로젝트 작업** 필드가 기본적으로 **복사** 보기로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-150">For example, after a user enters a project, the **Project Task** field is set to the **Copy** view by default.</span></span> <span data-ttu-id="16bf7-151">사용자에게 할당되지 않은 작업에 대한 시간 항목을 만들려면 조회 대화 상자에서 **보기 변경** 을 선택한 다음 **모든 활성 프로젝트 작업** 보기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-151">To create time entries for tasks that aren't assigned to a user, select **Change View** in the lookup dialog box, and then select the **All Active Project Tasks** view.</span></span>

## <a name="edit-a-time-entry"></a><span data-ttu-id="16bf7-152">시간 항목 편집</span><span class="sxs-lookup"><span data-stu-id="16bf7-152">Edit a time entry</span></span> 
<span data-ttu-id="16bf7-153">**설명** 및 **외부 주석** 과 같은 시간 항목 페이지의 일부 필드의 세부 정보는 주간 시간 입력 표에 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-153">Details from some fields on the time entry page, such as **Description** and **External Comments**, aren't shown in the weekly time entry grid.</span></span> <span data-ttu-id="16bf7-154">대신, 이러한 추가 세부 정보가 있는 **기간** 셀에 작은 삼각형 표시등이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-154">Instead, a small triangular indicator appears in the **Duration** cells that have these additional details.</span></span> 

1. <span data-ttu-id="16bf7-155">시간 항목을 편집하려면 시간 항목에서 업데이트할 셀을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-155">To edit a time entry, select the cell you want to update in the time entry.</span></span>
2. <span data-ttu-id="16bf7-156">**세부 정보 편집** 을 선택하여 **시간 항목 기본 양식** 창에서 데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-156">Select **Edit Details** to update the data in the **Time Entry Mainform** pane.</span></span> 

## <a name="copy-a-time-entry-row"></a><span data-ttu-id="16bf7-157">시간 항목 행 복사</span><span class="sxs-lookup"><span data-stu-id="16bf7-157">Copy a time entry row</span></span>
<span data-ttu-id="16bf7-158">행을 만든 후 **행 복사** 를 선택하여 전체 행을 새 행에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-158">After the row has been created, you can select **Copy Row** to copy the whole row to a new row.</span></span> <span data-ttu-id="16bf7-159">이러한 방식으로 행을 복사하면 크기와 기간도 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-159">When a row is copied in this way, dimensions and durations are also copied.</span></span> <span data-ttu-id="16bf7-160">**행 편집** 을 선택하여 **기간** 섹션에서 크기 값 및 기간을 업데이트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-160">You can also select **Edit Row** to update dimension values and durations in the **Duration** section.</span></span>

## <a name="open-a-time-entry-behavior"></a><span data-ttu-id="16bf7-161">시간 항목 열기 동작</span><span class="sxs-lookup"><span data-stu-id="16bf7-161">Open a time entry behavior</span></span>
<span data-ttu-id="16bf7-162">가장 눈에 띄는 필드에서 최적의 빠른 입력을 지원하기 위해 주간 시간 항목 표에는 선택한 크기 및 시간 기간의 하위 집합이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-162">To support optimal and quick entry in the most prominent fields, the weekly time entry grid shows a subset of selected dimensions and time durations.</span></span> <span data-ttu-id="16bf7-163">단일 시간 항목의 모든 세부 정보를 보려면 **항목 편집** 에서 **열기** 를선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-163">To view all the details of a single time entry, under **Edit Entry**, select **Open**.</span></span>

## <a name="submit-a-time-entry"></a><span data-ttu-id="16bf7-164">시간 항목 제출</span><span class="sxs-lookup"><span data-stu-id="16bf7-164">Submit a time entry</span></span>
<span data-ttu-id="16bf7-165">셀 블록 또는 전체 시간 항목 행을 선택한 다음 **제출** 을 선택하여 단일 시간 항목 또는 시간 항목 그룹을 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-165">You can submit a single time entry or a group of time entries by selecting a block of cells or a whole time entry row, and then selecting **Submit**.</span></span> <span data-ttu-id="16bf7-166">제출된 시간 항목은 승인자의 **승인** 페이지에서 승인을 보류 중인 항목으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-166">Submitted time entries appear as entries that are pending approval on the approvers' **Approval** page.</span></span> <span data-ttu-id="16bf7-167">시간 항목이 성공적으로 제출되면 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-167">After time entries are successfully submitted, they can't be edited.</span></span>

## <a name="recall-a-time-entry"></a><span data-ttu-id="16bf7-168">시간 항목 철회</span><span class="sxs-lookup"><span data-stu-id="16bf7-168">Recall a time entry</span></span>
<span data-ttu-id="16bf7-169">제출한 시간 항목을 철회할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-169">You can recall time entries that you've submitted.</span></span> <span data-ttu-id="16bf7-170">단일 시간 항목, 시간 항목 블록 또는 전체 시간 항목을 철회할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-170">You can recall a single time entry, a block of time entries, or a whole row of time entries.</span></span> <span data-ttu-id="16bf7-171">호출된 시간 항목을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-171">Recalled time entries can be edited.</span></span>

## <a name="time-entry-status"></a><span data-ttu-id="16bf7-172">시간 항목 상태</span><span class="sxs-lookup"><span data-stu-id="16bf7-172">Time entry status</span></span>

- <span data-ttu-id="16bf7-173">**초안**: 새 시간 항목에는 자동으로 **초안** 의 상태가 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-173">**Draft**: New time entries are automatically assigned a status of **Draft**.</span></span> <span data-ttu-id="16bf7-174">**초안** 상태가 있는 시간 항목만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-174">Only time entries that have a status of **Draft** can be deleted.</span></span>
- <span data-ttu-id="16bf7-175">**제출됨**: 시간 항목이 제출되면 상태가 **제출됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-175">**Submitted**: When a time entry is submitted, the status is updated to **Submitted**.</span></span> 
- <span data-ttu-id="16bf7-176">**승인됨**: 제출된 시간 항목이 승인되면 상태가 **승인됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-176">**Approved**: When a submitted time entry is approved, the status is updated to **Approved**.</span></span> 
- <span data-ttu-id="16bf7-177">**반환됨**: 시간 항목이 거부되면 상태가 **반환됨** 으로 업데이트되고 항목을 수정 및 다시 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-177">**Returned**: If a time entry is rejected, the status is updated to **Returned**, and the entry becomes available for correction and resubmission.</span></span> 

## <a name="view-rejection-comments"></a><span data-ttu-id="16bf7-178">거부 댓글 보기</span><span class="sxs-lookup"><span data-stu-id="16bf7-178">View rejection comments</span></span>
<span data-ttu-id="16bf7-179">승인자가 시간 항목을 거부하면 승인자가 주석을 추가하여 리소스가 거부 이유를 이해하는 데 도움을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-179">When a time entry is rejected by an approver, the approver might add comments to help the resource understand the reason for the rejection.</span></span> <span data-ttu-id="16bf7-180">시간 항목에 대한 거부 주석을 보려면 **항목 열기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-180">To view the rejection comments for a time entry, select **Open entry**.</span></span> <span data-ttu-id="16bf7-181">거부 주석은 타임라인에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-181">The rejection comments will be shown in the timeline.</span></span> <span data-ttu-id="16bf7-182">사용자는 항목을 다시 제출하기 전에 거부 의견에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-182">The user can respond to the rejection comments before they resubmit the entry.</span></span>

## <a name="copy-week"></a><span data-ttu-id="16bf7-183">주 복사</span><span class="sxs-lookup"><span data-stu-id="16bf7-183">Copy week</span></span>
<span data-ttu-id="16bf7-184">몇 개의 시간 항목이 생성된 후 사용자는 동시에 여러 시간 항목을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-184">After a few time entries have been created, users can create multiple time entries at the same time.</span></span>

1. <span data-ttu-id="16bf7-185">**시간 항목** 양식에서 **주 복사** 를 선택하여 추가 시간 항목을 대량 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-185">In the **Time Entries** form, select **Copy Week** to bulk-create additional time entries.</span></span> 
2. <span data-ttu-id="16bf7-186">**복사** 대화 상자의 **시작 기간** 섹션에서 **Start시작 날짜** 및 **종료 날짜** 필드를 사용하여 시간 항목을 복사할 날짜 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-186">In the **Copy** dialog box, in the **From period** section, use the **Start Date** and **End Date** fields to define the date range to copy time entries from.</span></span> 
3. <span data-ttu-id="16bf7-187">**끝 기간** 섹션의 **시작 날짜** 필드에서 시간 항목을 만들 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-187">In the **To Period** section, in the **Start Date** field, specify the date to create time entries for.</span></span> 
4. <span data-ttu-id="16bf7-188">**복사** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-188">Select **Copy**.</span></span> <span data-ttu-id="16bf7-189">**종료 기간** 의 지정된 날짜에 대해 **시작 기간** 의 해당 요일에 대한 시간 항목의 복사본이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-189">For the specified date in the **To period**, a copy of the time entries for the corresponding day of the week in the **From period** is created.</span></span> <span data-ttu-id="16bf7-190">예컨대, 지난 주 월요일의 시간 항목은 **종료 기간** 으로 지정된 주의 월요일로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-190">For example, Monday's time entry from last week is copied into Monday of the week that is specified as the **To period**.</span></span>

## <a name="import"></a><span data-ttu-id="16bf7-191">가져오기</span><span class="sxs-lookup"><span data-stu-id="16bf7-191">Import</span></span>
<span data-ttu-id="16bf7-192">동일한 기본 프로세스가 예약, 할당 및 교환에서 가져오는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-192">The same basic process is used to import from bookings, assignments, and exchanges.</span></span> <span data-ttu-id="16bf7-193">예약을 가져오는 날짜 범위를 지정한 다음 초안 시간 항목에 복사해야 하는 예약을 명시적으로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16bf7-193">You can specify the date range that bookings are imported from and then explicitly select the bookings that should be copied into draft time entries.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
