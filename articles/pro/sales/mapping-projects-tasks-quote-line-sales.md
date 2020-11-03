---
title: 프로젝트 및 작업을 프로젝트 기반 견적 라인에 매핑
description: 이 항목은 프로젝트 및 작업을 프로젝트 기반 작업 줄에 매핑하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079944"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="25ea1-103">프로젝트 및 작업을 프로젝트 기반 견적 라인에 매핑</span><span class="sxs-lookup"><span data-stu-id="25ea1-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="25ea1-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="25ea1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25ea1-105">프로젝트 기반 견적 라인에서 견적 라인에 이미 연결된 프로젝트의 특정 작업을 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="25ea1-106">작업을 견적 라인에 매핑하면 견적 라인에 정의한 다음 항목이 해당 작업에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="25ea1-107">청구 방법</span><span class="sxs-lookup"><span data-stu-id="25ea1-107">Billing method</span></span>
- <span data-ttu-id="25ea1-108">청구 가능성 옵션</span><span class="sxs-lookup"><span data-stu-id="25ea1-108">Chargeability options</span></span>
- <span data-ttu-id="25ea1-109">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="25ea1-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="25ea1-110">고객</span><span class="sxs-lookup"><span data-stu-id="25ea1-110">Customers</span></span>

<span data-ttu-id="25ea1-111">예를 들어 한 단계가 고정 가격이고 다른 모든 단계가 시간과 재료인 프로젝트가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="25ea1-112">이 경우 첫 번째 단계와 모든 하위 작업을 고정 가격 청구 방법을 사용하여 해당 단계의 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="25ea1-113">그런 다음 다른 모든 단계를 시간 및 자재 기반 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="25ea1-114">프로젝트 기반 견적 라인에 작업 연결</span><span class="sxs-lookup"><span data-stu-id="25ea1-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="25ea1-115">다음 위치에서 작업을 견적 라인과 연관시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="25ea1-116">**프로젝트** 페이지 > **작업 청구** 탭(최적)</span><span class="sxs-lookup"><span data-stu-id="25ea1-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="25ea1-117">**견적 라인** 페이지 > **청구 가능한 작업** 탭</span><span class="sxs-lookup"><span data-stu-id="25ea1-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="25ea1-118">프로젝트 페이지에서</span><span class="sxs-lookup"><span data-stu-id="25ea1-118">From the Project page</span></span>

<span data-ttu-id="25ea1-119">**프로젝트** 페이지는 작업을 견적 라인에 연결하기 위한 최적의 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="25ea1-120">이 페이지를 사용하여 여러 작업을 선택하고 모든 작업과 해당 하위 작업을 선택한 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="25ea1-121">프로젝트 기반 견적 라인의 **일반** 탭에서 **프로젝트** 필드가 채워져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="25ea1-122">**포함된 작업** 필드에서 **선택한 작업만** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="25ea1-123">프로젝트 기반 견적 라인을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-123">Save the project-based quote line.</span></span> <span data-ttu-id="25ea1-124">양식이 새로 고쳐지면 **청구 가능한 작업** 탭이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="25ea1-125">**일반** 탭의 **계획** 필드에서 프로젝트 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="25ea1-126">**프로젝트** 페이지에서 **작업 청구** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="25ea1-127">작업별 결제 설정에 적용되는 두 번째 그리드에서 하나 이상의 작업을 선택한 다음 **견적 라인 연결** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="25ea1-128">나타나는 대화 상자 페이지에서 견적에 프로젝트 기반 견적 라인을 표시하는 견적 라인을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="25ea1-129">**청구 유형** 필드에 이러한 작업이 청구 가능한지 또는 청구 불가능한지 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="25ea1-130">연결에 선택한 작업의 하위 작업이 포함되어야 하는지 여부를 나타내려면 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="25ea1-131">확인란을 선택하면 선택한 작업의 하위 작업이 견적 라인에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="25ea1-132">**확인** 을 선택하여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="25ea1-133">견적 라인 페이지에서</span><span class="sxs-lookup"><span data-stu-id="25ea1-133">From the Quote line page</span></span>

<span data-ttu-id="25ea1-134">**견적 라인** 페이지의 **청구 가능한 작업** 탭에서 프로젝트 작업을 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="25ea1-135">프로젝트 작업을 견적 라인에 연결하는 최적의 위치는 **계획** 페이지의 **작업 청구** 탭에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="25ea1-136">**견적 라인** 페이지의 **청구 가능한 작업** 탭에서 작업을 연결하는 경우 각 프로젝트를 수동으로 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="25ea1-137">프로젝트 기반 견적 라인의 **일반** 탭에서 **프로젝트** 필드에 선택한 프로젝트가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="25ea1-138">**포함된 작업** 필드에서 **선택한 작업만** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="25ea1-139">프로젝트 기반 견적 라인을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-139">Save the project-based quote line.</span></span> <span data-ttu-id="25ea1-140">양식이 새로 고쳐지면 **청구 가능한 작업** 탭이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="25ea1-141">**청구 가능한 작업** 탭에서 **견적 라인 작업 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="25ea1-142">**견적 라인 작업** 페이지의 **작업** 필드에서 작업을 선택하고 **청구 유형** 필드에서 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="25ea1-143">창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-143">Close the page.</span></span> <span data-ttu-id="25ea1-144">이제 선택한 작업이 견적 라인에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="25ea1-145">프로젝트 기반 견적 라인에서 작업 연결 분리</span><span class="sxs-lookup"><span data-stu-id="25ea1-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="25ea1-146">프로젝트 페이지에서</span><span class="sxs-lookup"><span data-stu-id="25ea1-146">From the Project page</span></span>

<span data-ttu-id="25ea1-147">이 방법은 견적 라인에서 작업을 분리하는 데 가장 최적의 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="25ea1-148">여러 작업을 선택하고 선택한 견적 라인에서 모든 작업과 하위 작업을 분리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="25ea1-149">프로젝트 기반 견적 라인의 **일반** 탭에 있는 **프로젝트** 필드에서 프로젝트 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="25ea1-150">**프로젝트** 페이지에서 **작업 청구** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="25ea1-151">작업별 결제 설정에 적용되는 두 번째 그리드에서 하나 이상의 작업을 선택한 다음 **견적 라인 분리** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="25ea1-152">나타나는 대화 페이지에서 견적 라인을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="25ea1-153">선택한 작업의 하위 작업에서도 연결을 제거해야 하는지 여부를 나타내는 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="25ea1-154">확인란을 선택하면 선택한 작업의 하위 작업도 견적 라인에서 분리됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="25ea1-155">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-155">Select **OK**.</span></span> <span data-ttu-id="25ea1-156">이 연결을 제거하면 이전에 작업에 기록된 실제 값이 취소될 수 있다는 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="25ea1-157">**확인** 을 선택하여 계속하고 작업과 프로젝트 기반 견적 라인 간의 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="25ea1-158">견적 라인 페이지에서</span><span class="sxs-lookup"><span data-stu-id="25ea1-158">From the Quote line page</span></span>

<span data-ttu-id="25ea1-159">**견적 라인** 페이지의 **청구 가능한 작업** 탭에서 프로젝트 작업을 견적 라인에서 분리할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="25ea1-160">**청구 가능한 작업** 탭에서 **견적 라인 작업 삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="25ea1-161">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-161">Select **OK**.</span></span> <span data-ttu-id="25ea1-162">이 연결을 제거하면 이전에 작업에 기록된 실제 값이 취소될 수 있다는 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="25ea1-163">**확인** 을 선택하여 계속하고 작업과 프로젝트 기반 견적 라인 간의 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="25ea1-164">이 절차는 프로젝트에서 작업을 삭제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="25ea1-165">프로젝트 기반 견적 라인에서 작업 연결만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea1-165">It only removes the task association from the project-based quote line.</span></span>
