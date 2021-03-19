---
title: OCR을 사용하여 영수증 캡처
description: 이 항목은 영수증에 대한 광학 문자 인식(OCR) 처리에 대한 정보를 제공합니다.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499859"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="1f64c-103">OCR을 사용하여 영수증 캡처</span><span class="sxs-lookup"><span data-stu-id="1f64c-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="1f64c-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="1f64c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f64c-105">영수증에 대한 광학 문자 인식(OCR) 처리를 도입하여 경비 입력 기능이 강화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="1f64c-106">이 기능은 경비 보고서를 작성할 때 사용자 경험을 개선하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="1f64c-107">주요 기능</span><span class="sxs-lookup"><span data-stu-id="1f64c-107">Key features</span></span>

- <span data-ttu-id="1f64c-108">시스템은 영수증에서 판매자 이름, 날짜 및 총액을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="1f64c-109">시스템은 첨부되지 않은 영수증을 첨부되지 않은 경비 트랜잭션과 일치시키려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="1f64c-110">영수증에서 수동으로 입력한 경비 트랜잭션을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="1f64c-111">경비 보고서에 영수증 첨부</span><span class="sxs-lookup"><span data-stu-id="1f64c-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="1f64c-112">경비 보고서가 생성될 때 신용 카드 거래가 포함된 영수증을 자동으로 첨부하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f64c-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="1f64c-113">**경비 관리** 작업 영역을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="1f64c-114">**영수증** 탭에서 첨부되지 않은 영수증이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="1f64c-115">**영수증** 탭에서 영수증을 업로드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="1f64c-116">**경비** 탭에서 첨부되지 않은 경비가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="1f64c-117">일반적으로 경비 관리자는 신용 카드 공급자로부터 이러한 경비를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="1f64c-118">**새 경비 보고서** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-118">Select **New expense report**.</span></span> <span data-ttu-id="1f64c-119">이제 경비 보고서를 작성할 때 경비와 영수증도 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="1f64c-120">경비와 영수증을 모두 추가하면 경비에 대한 영수증의 자동 일치가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="1f64c-121">경비 보고서에 대한 영수증 생성 또는 일치</span><span class="sxs-lookup"><span data-stu-id="1f64c-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="1f64c-122">경비를 생성하거나 영수증의 비용을 대응시키려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f64c-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="1f64c-123">경비 보고서의 **영수증** 탭에서 **영수증 추가** 를 선택하여 영수증을 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="1f64c-124">영수증의 업로드된 이미지 아래에 **만들기** 및 **일치** 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="1f64c-125">**만들기** 를 선택하여 수동으로 입력한 경비 트랜잭션을 생성하고 영수증에서 추출된 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="1f64c-126">**일치** 를 선택하는 경우 시스템은 기존 경비를 영수증과 일치 시키려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="1f64c-127">설치</span><span class="sxs-lookup"><span data-stu-id="1f64c-127">Installation</span></span>

<span data-ttu-id="1f64c-128">이러한 고급 경비 기능을 사용하려면 Microsoft Dynamics 365 Finance용 경비 관리 서비스 추가 기능을 설치하고 인스턴스에서 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="1f64c-129">Microsoft Dynamics Lifecycle Services(LCS)의 프로젝트에서 추가 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="1f64c-130">LCS에 로그인하고 원하는 환경을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="1f64c-131">**전체 세부 사항** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="1f64c-132">**유지 관리** 를 선택하거나 **환경 추가 기능** 빠른 탭으로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="1f64c-133">**새 추가 기능 설치** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="1f64c-134">**경비 관리 서비스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="1f64c-135">설치 가이드를 따르고 이용 약관에 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="1f64c-136">**설치** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-136">Select **Install**.</span></span>

<span data-ttu-id="1f64c-137">**기능 관리** 작업 영역에서 다음 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="1f64c-138">재구상된 경비 보고서</span><span class="sxs-lookup"><span data-stu-id="1f64c-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="1f64c-139">영수증에서 경비 자동 일치 및 생성</span><span class="sxs-lookup"><span data-stu-id="1f64c-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="1f64c-140">이러한 기능을 켜면 다음 동작이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="1f64c-141">기존 **경비 관리** 작업 영역이 새 작업 영역으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="1f64c-142">경비 필드 가시성을 위한 새 메뉴 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="1f64c-143">**경비 관리 > 내 경비 > 경비 보고서** 로 이동하여 계속해서 이전의 **경비 보고서** 페이지를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="1f64c-144">워크플로 및 모든 승인은 여전히 기존 비용 보고서 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="1f64c-145">영수증은 Microsoft Azure Cognitive Services를 통해 처리되며 메타데이터가 추출 및 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="1f64c-146">첨부되지 않은 일치 영수증을 포함하는 경비 보고서를 생성 할 수 있는 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="1f64c-147">경비 보고서에 추가된 옵션을 사용하면 영수증에서 비용 라인을 생성하거나 기존 영수증을 기존 비용 라인에 일치시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1f64c-148">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="1f64c-148">Frequently asked questions</span></span>

<span data-ttu-id="1f64c-149">**Microsoft는 모델에 내 데이터를 사용합니까?**</span><span class="sxs-lookup"><span data-stu-id="1f64c-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="1f64c-150">아니요, Microsoft는 영수증 처리 서비스를 위해 일반 기계 학습 모델을 구축했습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="1f64c-151">이 모델은 업로드한 영수증을 기반으로 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="1f64c-152">**이 기능은 어디에서 사용 가능하고 처리됩니까?**</span><span class="sxs-lookup"><span data-stu-id="1f64c-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="1f64c-153">현재 미국이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="1f64c-154">**영수증은 어디로 갑니까?**</span><span class="sxs-lookup"><span data-stu-id="1f64c-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="1f64c-155">재무 부서는 Cognitive Services에 연락하여 필드 데이터를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="1f64c-156">Cognitive Services는 처리가 진행되는 동안 최대 24시간 동안 영수증 사본을 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="1f64c-157">처리가 완료되면 Cognitive Services에서 영수증을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="1f64c-158">영수증은 여전히 Finance에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f64c-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="1f64c-159">자세한 내용은 [Form Recognizer의 새로운 기능으로 영수증 이해 가능](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f64c-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
