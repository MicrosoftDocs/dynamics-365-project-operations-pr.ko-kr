---
title: 진행 상황에 따라 청구를 위한 고급 계약 만들기
description: 이 항목은 완료된 작업의 백분율을 기준으로 고객에 대한 송장을 생성할 수 있도록 프로젝트 계약을 작성하는 방법을 설명합니다.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289512"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="bf808-103">진행 상황에 따라 청구를 위한 고급 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="bf808-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf808-104">이 항목은 완료된 작업의 백분율을 기준으로 고객에 대한 송장을 생성할 수 있도록 프로젝트 계약을 작성하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="bf808-105">프로젝트에 대해 설정한 작업의 예산 범주에 대해 송장 금액이 자동으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="bf808-106">송장 시기는 고객과 프로젝트 계약을 협상할 때 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="bf808-107">이 항목의 절차를 사용하여 프로젝트에 대해 설정한 작업의 예산 범주에 대한 송장 금액을 계산하는 계약, 관련 프로젝트 및 청구 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="bf808-108">계약 및 프로젝트를 생성한 후 프로젝트의 세부 정보를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="bf808-109">예를 들어 활동을 정의하고 작업자를 프로젝트에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="bf808-110">예제</span><span class="sxs-lookup"><span data-stu-id="bf808-110">Example</span></span>

<span data-ttu-id="bf808-111">귀하의 조직은 소프트웨어 개발 회사입니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-111">Your organization is a software development firm.</span></span> <span data-ttu-id="bf808-112">귀하는 총 20,000달 (USD)의 수수료로 고객을 위한 급여 회계 패키지를 개발하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="bf808-113">귀하의 조직은 프로젝트의 특정 비율을 완료하면 고객에게 송장을 보내는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="bf808-114">작업에 대해 다음 프로젝트 범주를 설정하여 청구 프로세스에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="bf808-115">컨설팅업</span><span class="sxs-lookup"><span data-stu-id="bf808-115">Consulting</span></span>
- <span data-ttu-id="bf808-116">설계</span><span class="sxs-lookup"><span data-stu-id="bf808-116">Design</span></span>
- <span data-ttu-id="bf808-117">설치</span><span class="sxs-lookup"><span data-stu-id="bf808-117">Installation</span></span>

<span data-ttu-id="bf808-118">또한 각 범주에 대해 완료된 프로젝트 작업 백분율에 대한 송장 금액을 자동으로 계산하는 청구 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="bf808-119">예산 관리자는 프로젝트 범주에 대한 예산을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="bf808-120">완료된 작업량은 예산 금액과 비교하여 실제 작업량의 백분율로 자동 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf808-121">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="bf808-121">Prerequisites</span></span>

<span data-ttu-id="bf808-122">결제 규칙을 사용하는 프로젝트를 생성하기 전에 결제 규칙 및 진행 결제를 게시하는 데 사용되는 수수료 분개에 대한 번호 시퀀스를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="bf808-123">**프로젝트 관리 및 회계** \> **설정** \> **프로젝트 관리 및 회계 매개 변수** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="bf808-124">**프로젝트 관리 및 회계 매개 변수** 페이지의 **숫자 시퀀스** 탭에서 결제 규칙을 만들 때 사용할 숫자 시퀀스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="bf808-125">**프로젝트 관리 및 회계** \> **분개장** \> **수수료** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="bf808-126">**수수료 분개** 페이지에서 **새로 만들기** 를 선택하고 분개장 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="bf808-127">진행 청구에 대한 계약 생성</span><span class="sxs-lookup"><span data-stu-id="bf808-127">Create a contract for progress billings</span></span>

<span data-ttu-id="bf808-128">이 절차를 사용하여 고정 가격 프로젝트에 대한 프로젝트 계약을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="bf808-129">프로젝트에서 완료된 작업이 지정된 비율에 도달하면 프로젝트 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="bf808-130">**프로젝트 관리 및 회계** \> **프로젝트** \> **프로젝트 계약** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="bf808-131">**프로젝트 계약** 페이지에서 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="bf808-132">**새 프로젝트 계약** 대화 상자에서 다음 필드를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="bf808-133">**이름**</span><span class="sxs-lookup"><span data-stu-id="bf808-133">**Name**</span></span>
    - <span data-ttu-id="bf808-134">**자금 유형**</span><span class="sxs-lookup"><span data-stu-id="bf808-134">**Funding type**</span></span>
    - <span data-ttu-id="bf808-135">**자금 출처**</span><span class="sxs-lookup"><span data-stu-id="bf808-135">**Funding source**</span></span>
    - <span data-ttu-id="bf808-136">**판매 통화** – 기본적으로 이 통화는 프로젝트 계약과 연관된 고객 송장에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="bf808-137">그러나 특정 고객 송장의 판매 통화를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="bf808-138">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-138">Select **OK**.</span></span> <span data-ttu-id="bf808-139">정보는 **프로젝트 계약** 페이지의 헤더에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="bf808-140">**프로젝트 계약** 페이지에서 프로젝트에 필요한 나머지 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="bf808-141">진행 청구에 대한 프로젝트 생성</span><span class="sxs-lookup"><span data-stu-id="bf808-141">Create a project for progress billings</span></span>

<span data-ttu-id="bf808-142">다음 단계에 따라 프로젝트 및 프로젝트 계약과 연결된 모든 하위 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="bf808-143">**프로젝트 관리 및 회계** \> **프로젝트** \> **모든 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="bf808-144">**모든 프로젝트** 페이지에서 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="bf808-145">**새 프로젝트** 대화 상자의 **프로젝트 유형** 필드에서 **시간 및 재료** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="bf808-146">프로젝트 그룹을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-146">Select a project group.</span></span> <span data-ttu-id="bf808-147">프로젝트 그룹은 그룹에 지정된 프로젝트에 대한 전기 정보를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="bf808-148">**프로젝트 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-148">Select **Create project**.</span></span>
6. <span data-ttu-id="bf808-149">프로젝트가 생성된 후 프로젝트 단계를 **처리 중** 으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="bf808-150">프로젝트용 예산 만들기</span><span class="sxs-lookup"><span data-stu-id="bf808-150">Create a budget for a project</span></span>

<span data-ttu-id="bf808-151">예산 범주는 각 범주에 대해 완료된 작업 백분율에 대한 송장 금액을 자동으로 계산하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="bf808-152">다음 단계에 따라 예상 비용에 대한 예산 범주를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="bf808-153">**프로젝트 관리 및 회계** \> **프로젝트** \> **모든 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="bf808-154">**모든 프로젝트** 페이지에서 원하는 프로젝트를 선택하고 엽니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="bf808-155">**프로젝트** 페이지에 있는 작업 창의 **계획** 탭의 **예산** 그룹에서 **프로젝트 예산** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="bf808-156">**프로젝트 예산** 페이지에서 프로젝트의 각 범주에 대한 예상 비용을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="bf808-157">진행 청구에 대한 청구 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="bf808-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="bf808-158">**프로젝트 관리 및 회계** \> **프로젝트** \> **프로젝트 계약** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="bf808-159">**프로젝트 계약** 페이지에서 프로젝트 계약을 선택하고 엽니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="bf808-160">프로젝트 계약 페이지의 **청구 규칙** 빠른 탭에서 **추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="bf808-161">**청구 규칙** 페이지의 **라인 유형** 필드에서 **진행** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="bf808-162">**청구 규칙 라인 세부 정보** 빠른 탭의 **계약 값** 필드에 계약 총액을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="bf808-163">**범주** 필드에서 수수료 거래를 전기할 범주를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="bf808-164">**프로젝트** 필드에서 이 청구 규칙을 사용하는 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="bf808-165">선택 사항: 추가 프로젝트에 청구 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="bf808-166">**프로젝트** 빠른 탭의 **사용 가능한 프로젝트** 섹션에서 프로젝트를 선택한 다음 오른쪽 화살표 단추를 선택하여 프로젝트를 **선택한 프로젝트** 섹션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="bf808-167">선택 사항: 고객이 송장 지급에서 원천 징수하는 퍼센트 금액을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="bf808-168">**결제 유지 조건** 빠른 탭에서 자금 출처를 선택한 다음 **유지율** 필드에 유지율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="bf808-169">이 단계를 반복하여 프로젝트 계약에 대한 추가 청구 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf808-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]