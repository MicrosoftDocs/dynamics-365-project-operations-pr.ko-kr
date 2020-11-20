---
title: 수정 분개장 생성 및 확인
description: 이 주제는 수정 분개장을 생성하고 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127767"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="897ef-103">수정 분개장 생성 및 확인</span><span class="sxs-lookup"><span data-stu-id="897ef-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="897ef-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="897ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="897ef-105">때때로 시간 또는 비용 입력이 잘못 입력될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="897ef-106">예를 들어, 컨설턴트는 시간 항목을 작성할 때 잘못된 날짜를 선택하거나 비용을 입력할 때 숫자를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="897ef-107">컨설턴트가 제출된 항목을 업데이트할 수 없는 경우 관리자는 프로젝트의 항목을 직접 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="897ef-108">이 항목의 절차를 완료하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="897ef-109">승인된 올바른 시간 항목</span><span class="sxs-lookup"><span data-stu-id="897ef-109">Correct approved time entries</span></span>     

<span data-ttu-id="897ef-110">프로젝트의 단일 또는 다중 시간 항목을 정정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="897ef-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="897ef-111">**영업** 영역에서 **트랜잭션** 을 선택한 다음 **승인된 시간** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="897ef-112">**승인된 시간** 목록에서 하나 이상의 승인된 시간 항목을 찾아서 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="897ef-113">필터를 사용하여 관련 항목을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="897ef-114">예를 들어, 프로젝트 ID를 필터링하고 해당 프로젝트 ID로 승인된 모든 시간 항목을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="897ef-115">**올바른 항목** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-115">Select **Correct entries**.</span></span> <span data-ttu-id="897ef-116">지정된 유형 **시간 수정** 으로 새로 수정된 분개장이 자동으로 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="897ef-117">선택한 항목이 분개장에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="897ef-118">**새 분개장** 페이지에 수정 분개장에 대한 **설명** 을 입력한 다음 **시간 항목 수정** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="897ef-119">**시간 항목에 대한 새 값** 섹션에서 필요에 따라 올바른 정보로 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="897ef-120">예를 들어, 할당된 프로젝트 또는 예약 가능 리소스를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="897ef-121">**미리 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-121">Select **Preview**.</span></span> <span data-ttu-id="897ef-122">대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="897ef-123">**분개장 항목** 탭에서 반전된 선택한 시간 항목 및 작성된 수정된 해당 항목과 관련된 원래 실제 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="897ef-124">추가 수정이 필요한 경우 5단계와 6단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="897ef-125">수정된 모든 실제는 **시간 항목에 대한 새로운 값** 섹션에서 선택한 값과 동일해집니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="897ef-126">수정 내용이 예상대로 나타나면 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="897ef-127">대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="897ef-128">**영업** 영역으로 돌아가서 **프로젝트** 를 선택한 다음 방금 시간 항목을 업데이트한 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="897ef-129">**프로젝트** 페이지의 **실제** 탭에서 변경한 내용을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="897ef-130">**실제** 탭이 보이지 않는 경우 **관련 항목** > **실제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="897ef-131">**실제 관련 보기** 목록에서 반전된 원래 시간 항목이 해당 수정 시간 항목과 같이 여전히 나열되어 있음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="897ef-132">예를 들어 다음 그래픽에는 금액 열에 차변이 표시된 수량이 8.00인 두 개의 광고 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="897ef-133">또한 금액 열에 대변 금액을 표시하는 수량이 -8.00인 두 개의 광고 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="897ef-134">이 수정은 수량을 0으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="897ef-135">승인된 올바른 경비 항목</span><span class="sxs-lookup"><span data-stu-id="897ef-135">Correct approved expense entries</span></span>

<span data-ttu-id="897ef-136">하나 이상의 경비 항목을 수정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="897ef-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="897ef-137">**영업** 영역에서 왼쪽 탐색 창의 **트랜잭션** 아래에서 **승인된 경비** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="897ef-138">**승인된 경비** 목록에서 수정하려는 프로젝트를 선택한 다음 **올바른 항목** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="897ef-139">지정된 유형 **경비 수정** 으로 새로 수정된 분개장이 자동으로 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="897ef-140">**새 분개장** 페이지에 수정에 대한 **설명** 을 입력하고 **경비 수정** 탭의 **경비에 대한 새 값** 섹션에서 선택한 경비 항목에 대해 수정할 데이터 필드를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="897ef-141">예를 들어, 경비를 다른 **프로젝트** 에 할당하거나 **경비 범주**, **경비 날짜** 또는 **예약 가능 리소스** 를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="897ef-142">**미리 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-142">Select **Preview**.</span></span> <span data-ttu-id="897ef-143">대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="897ef-144">**분개장 항목** 탭에서 수정 사항을 확인합니다. 반전된 선택한 경비 항목 및 작성된 수정된 해당 항목과 관련된 원래 실제 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="897ef-145">수정한 값이 예상대로 나타나면 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="897ef-146">대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="897ef-147">값이 예상대로 표시되지 않으면 **취소** 를 선택하여 **승인된 경비** 목록으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="897ef-148">2~5단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="897ef-149">수정된 실제는 **경비에 대한 새 값** 섹션에서 선택한 값과 동일해집니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="897ef-150">수정된 분개장을 확인한 후, 업데이트한 프로젝트로 다시 이동하여 변경 사항을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="897ef-151">프로젝트 페이지의 **실제** 탭에서 **실제 관련 보기** 를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="897ef-152">원래 항목과 수정 항목이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="897ef-153">다음 그래픽은 원래 경비 항목 금액과 해당 수정 경비 항목 금액을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="897ef-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


