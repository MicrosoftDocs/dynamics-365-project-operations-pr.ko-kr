---
title: 수익 추정치 관리
description: 이 토픽은 프로젝트의 수익 추정치로 작업하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279011"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="94a36-103">수익 추정치 관리</span><span class="sxs-lookup"><span data-stu-id="94a36-103">Manage revenue estimates</span></span>

<span data-ttu-id="94a36-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="94a36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94a36-105">수익 추정치를 생성, 계산, 전기, 반전 또는 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="94a36-106">수동으로 또는 정기적인 프로세스를 사용하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="94a36-107">이 토픽은 프로젝트의 수익 추정치로 작업하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="94a36-108">수동으로 수익 추정치 관리</span><span class="sxs-lookup"><span data-stu-id="94a36-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="94a36-109">고정 가격 수익 추정 프로젝트 또는 **견적 문의** 페이지(**프로젝트 관리 및 회계** > **보고서 및 문의** > **추정치 문의 및 보고서**)에서 **추정치** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="94a36-110">정기적인 프로세스를 사용하여 수익 추정치 관리</span><span class="sxs-lookup"><span data-stu-id="94a36-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="94a36-111">**프로젝트 관리 및 회계** > **주기적** > **추정치** 로 이동하고 해당 프로세스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="94a36-112">수익 추정치 만들기</span><span class="sxs-lookup"><span data-stu-id="94a36-112">Create a revenue estimate</span></span>

<span data-ttu-id="94a36-113">수익 추정치를 만들려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="94a36-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="94a36-114">**프로젝트 관리 및 회계** > **주기적** > **추정치** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="94a36-115">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-115">Select **New**.</span></span> <span data-ttu-id="94a36-116">**추정치 만들기** 페이지에서 다음 매개 변수를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="94a36-117">**기간 코드**: 이 코드는 견적이 전기되는 빈도를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="94a36-118">**추정 날짜**: 추정이 처리된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="94a36-119">**연속**: 추정이 이전 기간에 전기되었거나 추정이 생성된 첫 번째 추정인 경우에만 추정을 생성하려면 이 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="94a36-120">이 옵션을 선택하지 않으면 이전 기간에 추정치가 전기되지 않았더라도 추정치가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="94a36-121">**방법을 완료하는 데 드는 비용**: 남은 프로젝트 작업을 추정하는 방법을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="94a36-122">자세한 내용은 [방법을 완료하는 데 드는 비용](cost-complete-methods.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="94a36-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="94a36-123">**완료 방법**: 다음 옵션에서 완료 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="94a36-124">**자동**: 완료율은 계산에 포함된 비용 라인을 기준으로 자동 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="94a36-125">비용 템플릿은 포함된 비용 라인을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="94a36-126">**수동**: 완료율은 마지막 추정치의 완료율과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="94a36-127">추정이 생성된 후 **추정** 페이지에서 **수동 계산** 을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="94a36-128">**비용 템플릿에서**: 자동 및 수동 방법의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="94a36-129">이 옵션은 비용 템플릿의 기본값에 따라 자동 또는 수동으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="94a36-130">**추정 모델**: 추정에 대한 예측 모델을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="94a36-131">**추정 목록 인쇄**: 추정 목록을 생성하여 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="94a36-132">목록에는 현재 기능의 상태가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-132">The list contains the status of the current function.</span></span> <span data-ttu-id="94a36-133">보고서에 추정치에 대한 경고를 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="94a36-134">다음 조건으로 인해 추정 목록에 경고가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="94a36-135">100% 이상의 완료율.</span><span class="sxs-lookup"><span data-stu-id="94a36-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="94a36-136">0% 미만의 완료율.</span><span class="sxs-lookup"><span data-stu-id="94a36-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="94a36-137">**완료까지** 열의 음수 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="94a36-138">해당 계약 금액이 없는 추정입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="94a36-139">비용 추정이 첨부되지 않은 추정입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="94a36-140">**정보 로그 표시**: 작업이 실행될 때 처리된 추정 프로젝트에 대한 정보가 포함된 메시지를 수신하려면 이 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="94a36-141">WIP 또는 실제 전기</span><span class="sxs-lookup"><span data-stu-id="94a36-141">Post WIP or accruals</span></span>

<span data-ttu-id="94a36-142">추정치가 평가된 후 추정치는 유지, 감소 또는 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="94a36-143">그런 다음 **완료된 계약** 평가 원칙으로 작업할 때 WIP를 전기하거나 **완료율** 평가 원칙으로 작업할 때 발생을 전기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="94a36-144">추정 기간 상태는 **만들어짐** 에서 **전기됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="94a36-145">WIP 또는 발생 취소</span><span class="sxs-lookup"><span data-stu-id="94a36-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="94a36-146">취소 옵션을 사용하여 이미 전기된 WIP 또는 발생을 차감한 다음 기간에 대한 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="94a36-147">다른 기간 사이에 있는 기간을 취소하려면 필요한 추정 기간을 취소한 다음 다시 전기합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="94a36-148">모든 후속 기간은 이전 기간의 추정치에 따라 다르므로 기간을 건너 뛰지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="94a36-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="94a36-149">추정 프로젝트 제거 및 프로젝트 완료</span><span class="sxs-lookup"><span data-stu-id="94a36-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="94a36-150">추정 프로세스의 마지막 단계는 완료율이 100%에 도달하면 추정 프로젝트를 제거하고 고정 가격 프로젝트를 종료하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="94a36-151">제거를 실행할 때 다음이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="94a36-152">계약이 완료된 고정 가격 프로젝트의 경우 WIP 값이 잔액 계정에서 지워지고 손익 계정에 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="94a36-153">완료된 백분율이 있는 고정 가격 프로젝트의 경우 발생액이 손익 계정에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="94a36-154">추정은 상태를 **제거됨** 으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="94a36-155">특별한 경우에는 백분율이 100% 이상으로 확장될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="94a36-156">이 경우 **0으로 완료하는 비용 설정 방법** 을 사용하여 100%에 도달하도록 완료율을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="94a36-157">제거 취소</span><span class="sxs-lookup"><span data-stu-id="94a36-157">Reverse elimination</span></span>

1. <span data-ttu-id="94a36-158">**프로젝트 관리 및 회계** > **주기적** > **추정** > **제거 취소** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="94a36-159">작업 창에서 **프로세스** 탭의 **유지** 그룹에서 **추정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="94a36-160">**제거 취소** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="94a36-161">이 페이지를 사용하여 지정된 추정 날짜 및 추정 상태가 **제거됨** 인 모든 제거를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="94a36-162">적절한 필드를 선택하면 트랜잭션 상태가 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="94a36-163">또한 프로젝트 단계가 완료됨으로 설정된 경우 프로젝트 상태를 **진행 중** 으로 자동 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="94a36-164">프로젝트 기간의 추정 상태가 **전기됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a36-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]