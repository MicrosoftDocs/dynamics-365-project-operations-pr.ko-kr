---
title: 회계 연도 끝에서 프로젝트 예산 이전
description: 이 문서에서는 남은 예산 금액을 미래 연도로 이전하고 예산 등록 세부 정보를 만드는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289737"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="74af8-103">회계 연도 끝에서 프로젝트 예산 이전</span><span class="sxs-lookup"><span data-stu-id="74af8-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74af8-104">다년 프로젝트를 진행할 때 회계 연도의 끝에 남은 예산이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="74af8-105">남은 예산 금액을 미래 연도로 이전하고 연관된 총계정 원장 계정의 금액에 대한 예산 등록 세부 정보를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="74af8-106">나머지 금액을 이월하기 전에 나머지 예산 금액을 검토하고 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="74af8-107">남은 예산 금액 검토 및 분석</span><span class="sxs-lookup"><span data-stu-id="74af8-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="74af8-108">다음 단계를 완료하여 프로젝트의 연말 예산 금액을 검토하지만 금액을 이월하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="74af8-109">**프로젝트 관리 및 회계** > **주기적** > **예산** > **예산 이월** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="74af8-110">**프로젝트 예산 이월 프로세스** 페이지의 **연말 옵션** 탭에서 **남은 프로젝트 예산 금액 이월** 이 활성화되지 않았는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="74af8-111">**매개 변수** 탭의 **프로젝트 예산 연도** 필드에서 남은 예산 금액을 보려는 회계 연도를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="74af8-112">**회계 연도 열기** 필드에서 남은 예산 금액을 보려는 회계 연도를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="74af8-113">**예측 모델에서** 필드에서 **남은 예산** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="74af8-114">선택한 기준을 충족하고 남은 예산이 없는 프로젝트를 포함하려면 **남은 0개 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="74af8-115">**예산 선택** 탭에서 **모든 예산 검색** 을 선택하여 선택한 기준과 일치하는 모든 예산을 로드한 다음 **프로세스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="74af8-116">특정 예산 집합을 창에 로드하는 데이터베이스 쿼리를 디자인하려면 **선택한 예산 검색** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="74af8-117">창의 특정 줄에 대한 자세한 내용을 보려면 해당 줄을 선택한 다음 **예산 세부 정보 보기** 또는 **계정 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="74af8-118">남은 예산 금액 이월</span><span class="sxs-lookup"><span data-stu-id="74af8-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="74af8-119">남은 예산 금액을 처리할 때 총계정 원장에서 이월할 금액에 대한 트랜잭션을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="74af8-120">총계정 원장 트랜잭션을 생성하려면 [예산 금액 이월 및 총계정 원장 트랜잭션 생성](#carry-forward) 섹션의 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="74af8-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="74af8-121">이월된 예산 금액은 **예측 모델** 페이지에서 이월 예측 모델로 선택한 예측 모델로 이전됩니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="74af8-122">예산 금액 이월 및 총계정 원장 거래 생성</span><span class="sxs-lookup"><span data-stu-id="74af8-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="74af8-123">**프로젝트 관리 및 회계** > **주기적** > **예산** > **예산 이월** 로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="74af8-124">**프로젝트 예산 이월 프로세스** 페이지에서 **연말** 을 선택한 다음 **남은 프로젝트 예산 금액 이월** 과 **총계정 원장에 예산 등록 항목 생성** 을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="74af8-125">**매개 변수** 탭의 **프로젝트 매개 변수** 필드 그룹에서 다음을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="74af8-126">**프로젝트 회계 연도**: 남은 예산 금액을 보려는 회계 연도의 시작을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="74af8-127">**이익과 손실**: 총계정 원장에서 손익 트랜잭션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="74af8-128">**WIP**: 총계정 원장에서 진행 중인 작업(WIP) 트랜잭션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="74af8-129">**급여**: 총계정 원장에서 급여 할당 트랜잭션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="74af8-130">**총계정 원장** 필드 그룹에 다음 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="74af8-131">**회계 연도 열기** 필드에서 프로젝트에 대한 남은 예산 금액을 이전하려는 회계 연도를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="74af8-132">기본값은 **프로젝트 예산 연도** 필드의 값 다음 1년 입니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="74af8-133">**이월 기간** 필드에서 총계정 원장에서 예산 등록 상세 내역을 생성할 기간을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="74af8-134">이것은 일반적으로 여는 회계 연도의 첫 번째 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="74af8-135">**복사 시작/위치** 필드 그룹에 다음 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="74af8-136">**예측 모델에서** 필드에서 프로젝트에 대해 이전하려는 나머지 예산 금액과 연관된 프로젝트 예산 예측 모델을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="74af8-137">**원장 예측 모델로** 필드에서 총계장 원장으로 이전하려는 예산 금액과 연관된 원장 예산 모델을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="74af8-138">**판매 통화 이전** 을 선택하여 프로젝트에 대한 예산 금액을 이전할 때 생성되는 총계정 원장 트랜잭션에 프로젝트의 판매 통화를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="74af8-139">이 옵션을 선택하지 않으면 트랜잭션은 회계 통화를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="74af8-140">**남은 0개 표시** 를 선택하여 남은 예산 금액이 없지만 아래쪽 창에 표시된 프로젝트에서 선택한 다른 기준을 충족하는 프로젝트를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="74af8-141">**예산 선택** 탭에서 **모든 예산 검색** 을 선택하여 선택한 기준과 일치하는 모든 예산을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="74af8-142">특정 프로젝트 예산 집합을 창에 로드하는 데이터베이스 쿼리를 디자인하려면 **선택한 예산 검색** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="74af8-143">처리할 각 프로젝트에 대해 프로젝트 줄의 시작 부분에 있는 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="74af8-144">전체 또는 대부분의 프로젝트를 선택하려면 왼쪽 상단 모서리에 있는 확인 표시를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="74af8-145">프로젝트 처리를 제외하려면 해당 프로젝트의 확인 표시를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="74af8-146">선택한 프로젝트의 남은 예산 금액을 선택한 회계 연도로 이전하고 총계정 원장에 예산 등록 세부 정보를 생성하려면 **프로세스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="74af8-147">총계정 원장 트랜잭션을 생성하지 않고 예산 금액 이월</span><span class="sxs-lookup"><span data-stu-id="74af8-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="74af8-148">**프로젝트 관리 및 회계** > **주기적** > **예산** > **예산 이월** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="74af8-149">**프로젝트 예산 이월 프로세스** 페이지의 **연말 옵션** 필드에서 **남은 프로젝트 예산 금액 이월** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="74af8-150">**매개 변수** 그룹의 **프로젝트 예산 연도** 필드에서 남은 예산 금액을 보려는 회계 연도를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="74af8-151">**복사 시작/위치** 그룹에 다음 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="74af8-152">**예측 모델에서** 필드에서 프로젝트에 대해 이전하려는 나머지 예산 금액과 연관된 프로젝트 예산 예측 모델을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="74af8-153">남은 예산 금액이 없지만 선택한 다른 기준을 충족하는 프로젝트를 포함하려면 **남은 0개 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="74af8-154">**예산 선택** 그룹에서 **모든 예산 검색** 을 선택하여 선택한 기준과 일치하는 모든 예산을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="74af8-155">특정 프로젝트 예산 집합을 창에 로드하는 데이터베이스 쿼리를 디자인하려면 **선택한 예산 검색** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="74af8-156">처리할 각 프로젝트에 대해 프로젝트 줄의 시작 부분에 있는 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="74af8-157">**프로세스** 를 선택하여 선택한 프로젝트의 나머지 예산 금액을 선택한 회계 연도로 이전합니다.</span><span class="sxs-lookup"><span data-stu-id="74af8-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]