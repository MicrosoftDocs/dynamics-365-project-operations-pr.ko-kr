---
title: 지불시 결제 공급업체 결제 설정 및 사용
description: 이 항목은 고객 지불을 기반으로 부분 공급업체 지불을 해제할 수 있도록 지불시 결제(PWP) 조건을 작성하는 방법을 설명합니다.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288611"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="ae8dd-103">지불시 결제 공급업체 결제 설정 및 사용</span><span class="sxs-lookup"><span data-stu-id="ae8dd-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae8dd-104">공급업체가 하청업체로 일하도록 승인할 때 고객이 프로젝트 비용을 결제할 때까지 공급업체에 대한 지불을 보류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="ae8dd-105">이 시나리오를 지원하기 위해 공급업체와 구매 주문(PO)을 설정할 때 PWP(지불시 결제) 조건을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="ae8dd-106">예를 들어, 고객이 프로젝트 송장에 대한 금액을 지불하면 공급업체 송장 금액의 일부 또는 전체를 릴리스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="ae8dd-107">고객으로부터 관련 지불금의 일정 비율을 받은 후 공급업체가 지불을 받도록 지정하는 PWP 조건을 설정하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="ae8dd-108">고객으로부터 부분 지급을 받은 경우 지급을 위해 일부 관련 공급업체 송장을 수동으로 릴리스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="ae8dd-109">다음 예에서는 PWP 용어가 사용되는 프로세스를 간략하게 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="ae8dd-110">예제</span><span class="sxs-lookup"><span data-stu-id="ae8dd-110">Example</span></span>

<span data-ttu-id="ae8dd-111">귀하의 조직은 고객에게 소프트웨어가 설치된 100대의 컴퓨터를 컴퓨터당 미화 150달러의 가격으로 제공하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="ae8dd-112">그런 다음 공급업체를 고용하여 소프트웨어가 설치된 컴퓨터를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="ae8dd-113">계약에 따르면 고객은 조직에 비용을 지불하기 전에 컴퓨터의 품질을 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="ae8dd-114">조직의 정책은 고객이 지불할 때까지 공급업체에 대한 지불을 보류하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="ae8dd-115">따라서 PWP 백분율이 100%가 되도록 프로젝트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="ae8dd-116">공급업체는 소프트웨어가 설치된 100대의 컴퓨터를 10,000.00 USD에 대한 청구서와 함께 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="ae8dd-117">프로젝트에 대해 PWP 조건이 설정되어 있으므로 컴퓨터를 받을 때 공급업체에 비용을 지불하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="ae8dd-118">대신 15,000.00에 대한 송장과 함께 컴퓨터를 고객에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="ae8dd-119">고객은 컴퓨터를 검사하고 프로젝트 송장의 전체 금액을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="ae8dd-120">고객으로부터 전체 지불을 받은 후 공급업체 송장의 전체 금액인 10,000.00를 공급업체에 지불합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="ae8dd-121">프로젝트에 대한 PWP 조건 설정</span><span class="sxs-lookup"><span data-stu-id="ae8dd-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="ae8dd-122">프로젝트에 대한 PWP 조건을 설정할 때 공급업체에 지불하기 전에 고객이 프로젝트에 대해 지불해야 하는 최소 금액을 백분율로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="ae8dd-123">임계 금액은 프로젝트에 대한 고객 송장에서 자동으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="ae8dd-124">다음 단계에 따라 PWP 용어에 대한 임계값 백분율을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="ae8dd-125">**프로젝트 관리 및 회계** \> **프로젝트** \> **모든 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ae8dd-126">PWP 조건을 설정할 프로젝트를 찾아서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="ae8dd-127">**공급업체 계약** 빠른 탭에서 **라인 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="ae8dd-128">**계정 코드 필드** 필드에서 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="ae8dd-129">**테이블** - PWP 조건은 단일 공급업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="ae8dd-130">**그룹** - PWP 조건은 공급업체 그룹의 모든 공급 업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="ae8dd-131">**모두** - PWP 조건은 모든 공급업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="ae8dd-132">이전 단계에서 **표** 또는 **그룹** 을 선택한 경우 **공급업체/공급업체 그룹** 필드에서 PWP 조건이 적용되는 공급업체 또는 공급업체 그룹을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="ae8dd-133">이전 단계에서 **모두** 를 선택한 경우 **공급업체/공급업체 그룹** 필드는 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="ae8dd-134">프로젝트의 공급업체에 대해 공급업체 유지 조건이 설정된 경우 **공급 업체 유지 조건** 필드에서 유지 기간의 규칙 ID를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="ae8dd-135">**PWP 임계값 백분율** 필드에 프로젝트의 임계값 백분율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="ae8dd-136">프로젝트에 대해 입력하는 백분율은 공급업체에 지불하기 전에 고객이 지불해야 하는 최소 금액을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="ae8dd-137">PWP 조건이 있는 PO 생성</span><span class="sxs-lookup"><span data-stu-id="ae8dd-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="ae8dd-138">공급업체로부터 송장을 전기할 때 공급업체에 PWP 조건이 적용되는 경우 해당 조건이 PO 라인에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="ae8dd-139">PWP 조건이 있는 PO를 생성하려면 다음 단계를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="ae8dd-140">**조달 및 소싱**\>**구매 주문**\>**모든 구매 주문** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="ae8dd-141">작업 창에서 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="ae8dd-142">그런 다음 **구매 주문 만들기** 대화 상자에서 필요한 정보를 입력하고 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="ae8dd-143">또는 **모든 구매 주문** 목록 페이지에서 기존 PO를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="ae8dd-144">**구매 주문** 페이지의 **구매 주문 라인** 빠른 탭에서 공급업체의 PO 라인 세부 정보를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="ae8dd-145">**지불시 결제** 옵션이 자동으로 선택되고 **PWP 임계값 백분율** 필드는 **프로젝트** 페이지의 **PWP 임계값 백분율** 필드에서 자동으로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="ae8dd-146">PO 라인의 공급업체에 PWP 조건을 적용하지 않으려면 **지불시 결제** 옵션을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="ae8dd-147">이 경우 PO 라인의 **PWP 임계값 백분율** 필드는 0(영)으로 재설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="ae8dd-148">고객 결제 업데이트 및 공급업체 결제</span><span class="sxs-lookup"><span data-stu-id="ae8dd-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="ae8dd-149">공급업체가 프로젝트 작업을 완료하고 송장을 보내면 프로젝트 상태 및 고객 송장을 검토하여 프로젝트에 대한 PWP 조건이 충족되었는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="ae8dd-150">공급업체에 대한 PWP 조건이 충족되면 프로젝트에 대한 고객 지급을 기준으로 공급업체 송장에서 지급할 라인을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="ae8dd-151">PWP 조건이 충족되지 않은 경우에도 공급업체에 지불하기로 결정한 경우 **지불시 결제가 포함된 공급업체 송장** 페이지에서 PWP 조건을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="ae8dd-152">**프로젝트 관리 및 회계**\>**문의 및 신고**\>**유지 문의**\>**지불시 결제가 포함된 공급업체 송장** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="ae8dd-153">**지불시 결제가 포함된 공급업체 송장** 페이지의 검색 필드에 값을 입력하여 검토할 공급업체 송장을 찾은 다음 **검색** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="ae8dd-154">**공급업체 송장 라인** 빠른 탭에서 변경할 라인을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="ae8dd-155">송장 라인에 대한 **결제시 지불** 조건이 충족되면 **공급 업체 지불 해제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="ae8dd-156">**지불시 결제** 옵션이 지워지고 **결제 준비** 필드가 **예** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae8dd-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]