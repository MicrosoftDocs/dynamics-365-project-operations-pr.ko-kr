---
title: 경비 영수증 처리
description: 이 항목은 영수증에 대한 광학 문자 인식(OCR) 처리에 대한 정보를 제공합니다. 이 기능은 Microsoft Dynamics 365 Finance에서 경비 보고서를 작성할 때 사용자 경험을 개선하도록 설계되었습니다.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993514"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="262c8-104">경비 영수증 처리</span><span class="sxs-lookup"><span data-stu-id="262c8-104">Expense receipt processing</span></span>

<span data-ttu-id="262c8-105">영수증에 대한 광학 문자 인식(OCR) 처리를 도입하여 경비 입력 기능이 강화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="262c8-106">이 기능은 경비 보고서를 작성할 때 사용자 경험을 개선하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="262c8-107">주요 기능</span><span class="sxs-lookup"><span data-stu-id="262c8-107">Key features</span></span>

- <span data-ttu-id="262c8-108">영수증에서 판매자 이름, 날짜 및 총액이 추출됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="262c8-109">이 기능은 첨부되지 않은 영수증을 첨부되지 않은 경비 트랜잭션과 일치시키려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="262c8-110">영수증에서 수동으로 입력한 경비 트랜잭션을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="262c8-111">사용법 예제</span><span class="sxs-lookup"><span data-stu-id="262c8-111">Usage examples</span></span>

<span data-ttu-id="262c8-112">경비 보고서가 생성될 때 신용 카드 거래가 포함된 영수증을 자동으로 첨부하려면 다음을 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="262c8-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="262c8-113">**경비 관리** 작업 영역을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="262c8-114">**영수증** 탭에서 첨부되지 않은 영수증이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="262c8-115">**영수증** 탭에서 영수증을 업로드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="262c8-116">**경비** 탭에서 첨부되지 않은 경비가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="262c8-117">일반적으로 경비 관리자는 신용 카드 공급자로부터 이러한 경비를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="262c8-118">**새 경비 보고서** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-118">Select **New expense report**.</span></span> <span data-ttu-id="262c8-119">이제 경비 보고서를 작성할 때 경비와 영수증도 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="262c8-120">경비와 영수증을 모두 추가하면 경비에 대한 영수증의 자동 일치가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="262c8-121">경비를 생성하거나 영수증의 비용을 대응시키려면 다음을 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="262c8-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="262c8-122">경비 보고서의 **영수증** 탭에서 **영수증 추가** 를 선택하여 영수증을 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="262c8-123">영수증의 업로드된 이미지 아래에 **만들기** 및 **일치** 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="262c8-124">**만들기** 를 선택하여 수동으로 입력한 경비 트랜잭션을 생성하고 영수증에서 추출된 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="262c8-125">**일치** 를 선택하는 경우 시스템은 기존 경비를 영수증과 일치 시키려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="262c8-126">설치</span><span class="sxs-lookup"><span data-stu-id="262c8-126">Installation</span></span>

<span data-ttu-id="262c8-127">이 기능은 경비 경험을 단순화하기 위해 **재구상된 경비 보고서** 와 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="262c8-128">이 기능은 Sandbox 및 Production인 Tier 2+ 환경에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="262c8-129">이러한 고급 경비 기능을 사용하려면 Microsoft Dynamics 365 Finance용 경비 관리 서비스 추가 기능을 설치하고 인스턴스에서 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="262c8-130">Microsoft Dynamics Lifecycle Services(LCS)의 프로젝트에서 추가 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="262c8-131">LCS에 로그인하고 원하는 환경을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="262c8-132">**전체 세부 사항** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="262c8-133">**유지 관리** 를 선택하거나 **환경 추가 기능** 빠른 탭으로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="262c8-134">**새 추가 기능 설치** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="262c8-135">**경비 관리 서비스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="262c8-136">설치 가이드를 따르고 이용 약관에 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="262c8-137">**설치** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-137">Select **Install**.</span></span>

<span data-ttu-id="262c8-138">**기능 관리** 작업 영역에서 다음 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="262c8-139">재구상된 경비 보고서</span><span class="sxs-lookup"><span data-stu-id="262c8-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="262c8-140">영수증에서 경비 자동 일치 및 생성</span><span class="sxs-lookup"><span data-stu-id="262c8-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="262c8-141">이러한 기능을 켜면 다음 동작이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="262c8-142">기존 **경비 관리** 작업 영역이 새 작업 영역으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="262c8-143">경비 필드 가시성을 위한 새 메뉴 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="262c8-144">**경비 관리 > 내 경비 > 경비 보고서** 로 이동하여 계속해서 이전의 **경비 보고서** 페이지를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="262c8-145">워크플로 및 모든 승인은 여전히 기존 비용 보고서 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="262c8-146">영수증은 Microsoft Azure Cognitive Services를 통해 처리되며 메타데이터가 추출 및 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="262c8-147">첨부되지 않은 일치 영수증을 포함하는 경비 보고서를 생성 할 수 있는 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="262c8-148">경비 보고서에 추가된 옵션을 사용하면 영수증에서 비용 라인을 생성하거나 기존 영수증을 기존 비용 라인에 일치시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="262c8-149">재구상된 경비 보고서 기능에 대한 자세한 내용은 [재구상된 경비 보고서](ExpenseWorkspaceNew.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="262c8-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="262c8-150">자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="262c8-150">Frequently asked questions</span></span>

<span data-ttu-id="262c8-151">**Microsoft는 모델에 내 데이터를 사용합니까?**</span><span class="sxs-lookup"><span data-stu-id="262c8-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="262c8-152">아니요, Microsoft는 영수증 처리 서비스를 위해 일반 기계 학습 모델을 구축했습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="262c8-153">이 모델은 업로드한 영수증을 기반으로 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="262c8-154">**이 기능은 어디에서 사용 가능하고 처리됩니까?**</span><span class="sxs-lookup"><span data-stu-id="262c8-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="262c8-155">현재 미국이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="262c8-156">**영수증은 어디로 갑니까?**</span><span class="sxs-lookup"><span data-stu-id="262c8-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="262c8-157">재무 부서는 Cognitive Services에 연락하여 필드 데이터를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="262c8-158">Cognitive Services는 처리가 진행되는 동안 최대 24시간 동안 영수증 사본을 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="262c8-159">처리가 완료되면 Cognitive Services에서 영수증을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="262c8-160">영수증은 여전히 Finance에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="262c8-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="262c8-161">자세한 내용은 [Form Recognizer의 새로운 기능으로 영수증 이해 가능](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="262c8-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]