---
title: 프로젝트 및 작업을 프로젝트 기반 계약에 매핑 - 라이트
description: 이 항목은 계약 내용에 프로젝트 및 작업을 추가 및 제거하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994640"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a><span data-ttu-id="7566b-103">프로젝트 및 작업을 프로젝트 기반 계약 라인에 매핑</span><span class="sxs-lookup"><span data-stu-id="7566b-103">Map projects and tasks to a project-based contract line</span></span> 

<span data-ttu-id="7566b-104">_**적용 대상:** 라이트 배포 - 견적 송장 처리, 리소스/비 재고 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7566b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7566b-105">프로젝트 기반 계약 내용에서 프로젝트의 특정 작업을 계약 내용에 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-105">On project-based contract lines, you can map specific tasks in a project to the contract line.</span></span>

<span data-ttu-id="7566b-106">특정 작업을 계약 내용에 매핑할 때 청구 방법, 청구 가능성 옵션, 초과 안 함 한도 및 계약 내용에 정의된 고객은 해당 특정 작업에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-106">When you map specific tasks to a contract line, the billing method, chargeability options, Not-to-exceed limits, and the customers defined on the contract line will be applicable to those specific tasks only.</span></span>

<span data-ttu-id="7566b-107">프로젝트의 한 단계(예: 프로토타입 단계)가 고정 가격이고 다른 모든 단계가 시간과 재료인 시나리오가 있는 경우 고정 가격 청구 방법이 있는 해당 단계에 대해 프로토타입 단계와 연관된 모든 하위 작업을 계약 내용에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-107">If you have a scenario where one phase of a project, for example the Prototype Phase, is fixed price and all the other phases are time and material, you will be able to associate the Prototype phase and all the associated child tasks to the contract line for that phase with a fixed price billing method.</span></span>

<span data-ttu-id="7566b-108">프로젝트 작업 분할 구조(WBS)의 다른 모든 단계는 시간 및 재료 기반 계약 내용과 연관될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-108">All the other phases in your project work breakdown structure (WBS) can be associated to the time and material-based contract line.</span></span>

## <a name="associate-tasks-to-project-based-contract-lines"></a><span data-ttu-id="7566b-109">프로젝트 기반 계약 내용에 작업 연결</span><span class="sxs-lookup"><span data-stu-id="7566b-109">Associate tasks to project-based contract lines</span></span>

<span data-ttu-id="7566b-110">작업은 **계약 내용** 페이지의 **청구 가능한 작업** 탭 또는 **프로젝트** 페이지의 **작업 청구** 탭에서 계약 내용에 연관될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-110">Tasks can be associated to contract lines from the **Chargeable Tasks** tab on the **Contract Line** page or from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="7566b-111">계약 내용 페이지에서</span><span class="sxs-lookup"><span data-stu-id="7566b-111">From the Contract line page</span></span>

<span data-ttu-id="7566b-112">다음 단계를 완료하여 프로젝트 작업을 **계약 내용** 페이지의 **청구 가능한 작업** 탭의 계약 내용에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-112">Complete the following steps to associate project tasks to the contract line from the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="7566b-113">프로젝트 기반 계약 내용의 **일반** 탭에서 **프로젝트** 필드가 채워져 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-113">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="7566b-114">**포함된 작업** 필드에서 **선택한 작업만** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-114">In the **Included Tasks** field, select the **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="7566b-115">변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-115">Save your changes.</span></span> <span data-ttu-id="7566b-116">양식이 새로 고쳐지고 **청구 가능한 작업** 탭이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-116">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span>
4. <span data-ttu-id="7566b-117">**청구 가능한 작업** 탭을 선택하고 하위 표에서 **계약 내용 작업 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-117">Select the **Chargeable Tasks** tab, and in the subgrid, select **Add a Contract Line Task**.</span></span>
5. <span data-ttu-id="7566b-118">**계약 내용 작업** 페이지의 **작업** 드롭다운에서 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-118">On the **Contract Line Tasks** page, in the **Tasks** drop-down, select the task.</span></span> 
6. <span data-ttu-id="7566b-119">**청구 유형** 필드에 정보를 입력한 다음 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-119">Enter information in the **Billing Type** field, and then select **Save and Close**.</span></span> <span data-ttu-id="7566b-120">선택한 작업이 계약 내용과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-120">The selected task is associated to the contract line.</span></span>

> [!NOTE]
> <span data-ttu-id="7566b-121">이는 프로젝트 작업을 계약 내용에 연결하는 데 가장 최적의 경험이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-121">This is not the most optimal experience for associating project tasks to contract lines.</span></span> <span data-ttu-id="7566b-122">이 환경에서는 각 프로젝트를 수동으로 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-122">Each project will have to be manually associated in this experience.</span></span> <span data-ttu-id="7566b-123">선호하는 방법은 **프로젝트** 페이지의 **작업 청구** 탭을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-123">The preferred way is from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="7566b-124">프로젝트 페이지에서</span><span class="sxs-lookup"><span data-stu-id="7566b-124">From the project page</span></span>

<span data-ttu-id="7566b-125">작업을 계약 내용에 연결하는 최적의 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-125">This is the optimal method to associate tasks to contract lines.</span></span> <span data-ttu-id="7566b-126">여러 작업을 선택하고 모든 작업과 해당 하위 작업을 선택한 계약 내용에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-126">You can select multiple tasks and associate all of the them and their child tasks to the selected contract line.</span></span> <span data-ttu-id="7566b-127">작업을 계약 내용에 연결하려면 **프로젝트** 페이지에서 계약 내용에 작업을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-127">Complete the following steps to associate tasks to the contract line from the **Project** page.</span></span>

1. <span data-ttu-id="7566b-128">프로젝트 기반 계약 내용의 **일반** 탭에서 **프로젝트** 필드가 채워져 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-128">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="7566b-129">**포함된 작업** 필드에서 **선택한 작업만** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-129">On the **Included Tasks** field, select **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="7566b-130">프로젝트 기반 계약을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-130">Save the project-based contract line.</span></span> <span data-ttu-id="7566b-131">양식이 새로 고쳐지고 **청구 가능한 작업** 탭이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-131">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span> <span data-ttu-id="7566b-132">이것은 확인 목적으로만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-132">This is just for verification purposes only.</span></span>
4. <span data-ttu-id="7566b-133">프로젝트 기반 계약 내용에서 **일반** 탭의 **프로젝트** 필드에서 프로젝트 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-133">On the **General** tab of the project-based contract line, in the **Project** field, select the project link.</span></span>
5. <span data-ttu-id="7566b-134">**프로젝트** 페이지에서 **작업 청구 설정** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-134">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
6. <span data-ttu-id="7566b-135">여기에는 두 가지 그리드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-135">There are two grids.</span></span> <span data-ttu-id="7566b-136">한 그리드는 전체 프로젝트에 적용되는 계약 내용을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-136">One grid is for contract lines that apply to the whole project.</span></span> <span data-ttu-id="7566b-137">두 번째 그리드는 작업별 결제 설정에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-137">The second grid applies to task-specific billing setup.</span></span> <span data-ttu-id="7566b-138">두 번째 그리드에서 하나 이상의 작업을 선택한 다음 **계약 내용 연결** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-138">In the second grid, select one or more tasks, and then select **Associate Contract Lines**.</span></span>
7. <span data-ttu-id="7566b-139">열리는 대화 페이지의 드롭다운에서 계약 내용을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-139">In the dialog page that opens, select a contract line from the drop-down.</span></span>
8. <span data-ttu-id="7566b-140">**청구 유형** 드롭다운을 사용하여 작업을 청구 가능 또는 청구 불가능으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-140">Use the **Billing Type** drop-down to mark the tasks as chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="7566b-141">연결에 선택한 작업의 하위 작업도 포함해야하는지 여부를 표시하려면 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-141">Select the check box to indicate if the association should also include child tasks of the selected tasks.</span></span> <span data-ttu-id="7566b-142">상자를 선택하면 선택한 작업의 하위 작업도 계약 내용에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-142">Checking the box will also associate the child tasks of the selected tasks to the contract line.</span></span>
10. <span data-ttu-id="7566b-143">**확인** 을 선택하여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-143">Select **OK** to close the dialog.</span></span>

## <a name="unassociate-tasks-from-project-based-contract-lines"></a><span data-ttu-id="7566b-144">프로젝트 기반 계약 내용에서 작업 연결 해제</span><span class="sxs-lookup"><span data-stu-id="7566b-144">Unassociate tasks from project-based contract lines</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="7566b-145">계약 내용 페이지에서</span><span class="sxs-lookup"><span data-stu-id="7566b-145">From the contract line page</span></span>

<span data-ttu-id="7566b-146">다음 단계를 완료하여 프로젝트 작업을 **계약 내용** 페이지의 **청구 가능한 작업** 탭의 계약 내용에서 연결을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-146">Complete the following steps to unassociate project tasks from the contract line on the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="7566b-147">**청구 가능한 작업** 탭에서 **계약 내용 작업 삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-147">On the **Chargeable Tasks** tab, select **Delete a Contract Line Task**.</span></span>
2. <span data-ttu-id="7566b-148">경고 메시지는 이 연결을 제거하면 이전에 작업에 기록된 실제 값이 취소될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-148">A warning message indicates that removing this association could result in reversal of any actuals previously recorded on the task.</span></span> <span data-ttu-id="7566b-149">대화 상자에서 **확인** 을 선택하여 작업과 프로젝트 기반 계약 내용 간의 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-149">Select **OK** on the dialog to remove the association between the task and the project-based contract line.</span></span> 

> [!NOTE]
> <span data-ttu-id="7566b-150">이것은 프로젝트에서 작업을 삭제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-150">This doesn't delete the task from the project.</span></span> <span data-ttu-id="7566b-151">대신 프로젝트 기반 계약 내용에서 작업 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-151">Instead, it removes the task association from the project-based contract line.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="7566b-152">프로젝트 페이지에서</span><span class="sxs-lookup"><span data-stu-id="7566b-152">From the project page</span></span>

<span data-ttu-id="7566b-153">이는 계약 내용에서 작업 연결을 해제하는 데 더 최적의 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-153">This is the more optimal experience for unassociating tasks from contract lines.</span></span> <span data-ttu-id="7566b-154">여러 작업을 선택하고 모든 작업과 해당 하위 작업을 선택한 계약 내용에서 연결 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-154">You can select multiple tasks and unassociate all of the them and their child tasks from the selected contract line.</span></span> <span data-ttu-id="7566b-155">계약 내용에서 작업 연결을 해제하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="7566b-155">Complete the following steps to unassociate tasks from the contract line.</span></span>

1. <span data-ttu-id="7566b-156">프로젝트 기반 계약 내용에서 **일반** 탭의 **프로젝트** 필드에서 프로젝트 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-156">From **General** tab of the project-based contract line, in the **Project** field, click on the link for project.</span></span>
2. <span data-ttu-id="7566b-157">**프로젝트** 페이지에서 **작업 청구 설정** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-157">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
3. <span data-ttu-id="7566b-158">페이지에는 두 개의 그리드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-158">There are two grids on the page.</span></span> <span data-ttu-id="7566b-159">한 그리드는 전체 프로젝트에 적용되는 계약 내용을 위한 것이고 두 번째 그리드는 작업별 청구 설정에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-159">One grid is for contract lines that apply to the whole project and the second applies to task-specific billing setup.</span></span> <span data-ttu-id="7566b-160">두 번째 그리드에서 하나 이상의 작업을 선택한 다음 **계약 내용 연결 해제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-160">In the second grid, select one or more tasks and the select **Disassociate Contract Lines**.</span></span>
4. <span data-ttu-id="7566b-161">열리는 대화 페이지의 드롭다운에서 계약 내용을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-161">In the  dialog page that opens, select a contract line from the drop-down.</span></span>
5. <span data-ttu-id="7566b-162">연결에 선택한 작업의 하위 작업에서도 제거해야 하는지 여부를 표시하려면 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-162">Select the check box to indicate if the association should also be removed from any child tasks of the selected tasks.</span></span> <span data-ttu-id="7566b-163">상자를 선택하면 선택한 작업의 하위 작업도 계약 내용에서 연결 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-163">Checking the box will also unassociate the child tasks of the selected tasks from the contract line.</span></span>
6. <span data-ttu-id="7566b-164">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-164">Select **OK**.</span></span> <span data-ttu-id="7566b-165">경고 메시지는 이 연결을 제거하면 이전에 작업에 기록된 실제 값이 취소될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-165">A warning message indicates that removing this association could result in reversal of any actuals recorded on the task previously.</span></span> <span data-ttu-id="7566b-166">경고 대화 상자에서 **확인** 을 선택하여 작업과 프로젝트 기반 계약 내용 간의 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-166">Select **OK** on the warning dialog to remove the association between the task and the project-based contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
