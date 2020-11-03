---
title: 공급업체 결제 유지 조건 만들기 및 적용
description: 이 항목은 공급업체 결제에 대한 보존 기간을 설정하고 유지하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080189"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="4bc6d-103">공급업체 결제 유지 조건 만들기 및 적용</span><span class="sxs-lookup"><span data-stu-id="4bc6d-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="4bc6d-104">프로젝트에 대한 공급업체 지불 유지 조건을 설정하는 것은 조직에서 공급업체에 대한 지불의 일부를 유지하려는 경우 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="4bc6d-105">예를 들어, 납품된 제품이 기대치를 충족할 때까지 공급업체에 지불을 보류하려는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="4bc6d-106">공급업체 계약을 협상할 때 공급업체 지불 유지 조건을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="4bc6d-107">공급업체 결제 유지 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="4bc6d-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="4bc6d-108">보유를 위한 공급업체 지불 비율과 해제할 이전 보유 금액의 비율을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="4bc6d-109">계약이 지정된 완료 상태에 도달할 때까지 금액이 공급업체 송장에 자동으로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="4bc6d-110">보존 기간을 설정한 후 해당 공급업체의 모든 프로젝트에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="4bc6d-111">다음 단계를 사용하여 공급업체 지불에 대한 보존 기간을 설정하고 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="4bc6d-112">**프로젝트 관리 및 회계** > **유지** > **공급업체 지불 유지 조건** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="4bc6d-113">**새로 만들기** 를 선택하여 새 공급업체 유지 기간을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="4bc6d-114">새 조건에 대한 **규칙 ID** 값이 자동으로 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="4bc6d-115">**설명** 필드에 간단한 설명을 입력하고 **조건** 빠른 탭에서 **라인 추가** 를 선택하여 다음에 대한 조건 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="4bc6d-116">**전달된 단위 비율** : 조건의 완료율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="4bc6d-117">프로젝트 완료 스테이지가 지정된 백분율과 같아질 때까지 금액이 공급업체 송장에 자동으로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="4bc6d-118">예를 들어 50.00을 입력하면 프로젝트가 50% 완료될 때까지 금액이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="4bc6d-119">**유지할 비율** : 유지할 공급업체 송장 금액의 백분율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="4bc6d-120">예를 들어, 10.00을 입력하면 공급업체 송장 금액의 10%는 프로젝트가 **전달된 단위 비율** 필드에 설정된 완료율에 도달할 때까지 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="4bc6d-121">**해제 비율** : **라인 추가** 를 선택하여 선택한 프로젝트 완료 레벨에 대해 해제할 이전에 보유한 금액의 백분율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="4bc6d-122">서로 다른 수준의 프로젝트 완료에 대한 중요 시점이 두 개 이상 있는 경우 각 보관 규칙에 대해 별도의 공급업체 보관 기간 줄을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="4bc6d-123">각 라인은 지정된 프로젝트 완료 수준마다 다른 보존 비율과 다른 해제 비율을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="4bc6d-124">공급업체에 대한 공급업체 유지 조건을 만든 후 해당 조건을 프로젝트에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="4bc6d-125">프로젝트에 공급업체 유지 조건 적용</span><span class="sxs-lookup"><span data-stu-id="4bc6d-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="4bc6d-126">**프로젝트 관리 및 회계** > **프로젝트** > **모든 프로젝트** 로 이동하고 프로젝트 목록 페이지에서 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="4bc6d-127">**공급업체 계약** 빠른 탭에서 **라인 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="4bc6d-128">**계정 코드 필드** 에서 다음 옵션 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="4bc6d-129">**테이블** : 공급업체 유지 조건은 단일 공급업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="4bc6d-130">**그룹** : 공급업체 유지 조건은 공급업체 그룹의 모든 공급 업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="4bc6d-131">**모두** : 공급업체 유지 조건은 모든 공급업체에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="4bc6d-132">**공급업체/공급업체 그룹 필드** 에서 공급업체 유지 조건이 적용되는 공급업체 또는 공급업체 그룹을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="4bc6d-133">**모두** 를 선택한 경우 이전 단계에서는 이 필드를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="4bc6d-134">**공급 업체 유지 조건** 필드에서 이전 절차에서 만든 유지 기간을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="4bc6d-135">프로젝트에 공급업체에 대해 설정된 PWP(지불시 지불) 조건도 있는 경우 **PWP 임계값 백분율** 필드에 해당 프로젝트에 대한 임계값 비율을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="4bc6d-136">공급업체 유지 기간은 공급업체에 대해 생성한 구매 주문에도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6d-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
