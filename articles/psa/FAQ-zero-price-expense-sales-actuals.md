---
title: 경비 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 다음 세 가지 검사를 수행하면 경비 판매 실제 값에 대해 가격이 기본값 0이 되는 이유를 쉽게 해결할 수 있습니다.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285895"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="5d741-103">경비 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="5d741-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5d741-104">이 FAQ는 트랜잭션 클래스가 경비로 설정되고 트랜잭션 유형이 미청구된 판매인 경비 실제 값에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="5d741-105">다음 세 가지 검사를 수행하면 경비 판매 실제 값에 대해 가격(대금 청구 요금)이 기본값 0이 되는 이유를 쉽게 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="5d741-106">확인 1: 프로젝트에 대한 판매 가격표 식별</span><span class="sxs-lookup"><span data-stu-id="5d741-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="5d741-107">실제 값의 프로젝트 필드에서 프로젝트를 찾아 프로젝트로 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="5d741-108">그런 다음 영업 탭으로 이동합니다. 프로젝트 계약 내용 표에서 프로젝트 계약 필드의 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="5d741-109">프로젝트 계약 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-109">The Project Contract page will open.</span></span> <span data-ttu-id="5d741-110">프로젝트 계약 페이지에서 프로젝트 가격표 탭으로 이동합니다. 여기에 가격표가 하나 이상 첨부되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="5d741-111">프로젝트 계약의 프로젝트 가격표 표에 첨부된 가격표가 없는 경우:</span><span class="sxs-lookup"><span data-stu-id="5d741-111">If there is no price list attached in the Project Price Lists grid of the Project Contract:</span></span>

- <span data-ttu-id="5d741-112">가격표를 프로젝트 가격표 표에 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="5d741-113">여기에 첨부할 수 있는 가격표에는 컨텍스트 필드가 판매로 설정되어 있고 가격표의 통화 필드는 프로젝트 계약의 통화 필드와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="5d741-114">필요한 수정 프로그램을 만든 후에는 경비 항목을 다시 만들고 승인하며 미청구 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="5d741-115">프로젝트 계약의 프로젝트 가격표 표에 하나 이상의 가격표가 첨부되어 있는 경우 확인 2로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="5d741-116">확인 2: 경비 실제 값의 특정 날짜에 대해 위의서 식별된 가격표가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="5d741-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="5d741-117">Project Service에서 기본 가격에 대한 가격표를 고려하려면 해당 가격표가 경비 판매 실제 값의 날짜에 적용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="5d741-118">위에서 확인한 가격표가 적용 가능한 경우 다음을 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="5d741-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="5d741-119">첨부된 가격표에 대한 일반 탭에서 시작 날짜와 종료 날짜가 비어 있지 않은 것을 확인하여 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="5d741-120">위에서 확인한 가격표의 시작 날짜와 종료 날짜가 비어 있으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="5d741-121">경비 판매 실제 값에 시작 날짜 필드를 기록해 두고 식별된 가격표가 해당 날짜에 적용되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="5d741-122">예를 들어 경비 실제 값의 날짜는 가격표의 시작 날짜와 종료 날짜 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="5d741-123">경비 판매 실제 값에 해당 날짜를 포함하는 가격표가 없는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="5d741-124">가격표가 경비 실제 값의 날짜를 포함하도록 하려면 가격펴의 시작 및 종료 날짜를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="5d741-125">경비 판매 실제 값에 해당 날짜를 포함하는 가격표가 하나 이상 있는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="5d741-126">경비 실제 값의 날짜를 포함하는 가격표가 하나만 있도록 가격표의 시작 및 종료 날짜를 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-126">Edit the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="5d741-127">경비 실제 값의 해당 날짜를 포함하는 가격표가 하나만 있는 경우 확인 3으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="5d741-128">필요한 수정 프로그램을 만든 후에는 경비 항목을 다시 만들고 승인하며 미청구 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="5d741-129">확인 3: 해당 프로젝트 가격표에 경비 범주에 대한 유효한 가격이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="5d741-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="5d741-130">확인 1 및 확인 2를 성공적으로 완료한 경우 이제 경비 판매 실제 값의 날짜에 적용할 수 있는 프로젝트 가격표가 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="5d741-131">이 프로젝트 가격표를 열고 범주 가격 탭으로 이동합니다. 경비 실제 값의 특정 경비 범주에 대한 표에 행이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="5d741-132">행이 없으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="5d741-133">경비 실제 값의 범주에 대한 범주 가격 표에서 행을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="5d741-134">그런 다음 경비 항목을 다시 만들고 승인하며 미청구 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-134">Then, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="5d741-135">범주 가격 표에 경비 범주에 대한 행이 있는 경우 유효한 가격이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="5d741-136">유효한 가격이 무엇인지 이해하려면 다음 방법을 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="5d741-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="5d741-137">범주 가격 라인의 가격 산정법 필드가 원가로 설정된 경우 경비 판매 실제 값의 단위 비율은 경비 항목의 값에 기본값으로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="5d741-138">범주 가격 라인의 가격 산정법 필드가 원가 가산율로 설정된 경우 백분율 필드가 유효한 값으로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="5d741-139">경비 판매 실제 값의 단위 비율은 이 원가 가산율을 경비 항목의 가격에 적용하여 기본값으로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="5d741-140">범주 가격 라인의 가격 산정법 필드가 단가로 설정된 경우 가격 필드가 유효한 값으로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="5d741-141">경비 판매 실제 값의 단위 비율은 가격 필드에 지정된 통화 금액이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="5d741-142">경비 범주에 대한 가격 설정이 유효하지 않은 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="5d741-143">해결책은 상기의 규칙에 따라 경비 범주에 대한 유효한 가격을 가진 범주 가격 라인을 편집하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="5d741-144">작업이 완료되면 경비 항목을 다시 만들고 승인한 다음 미청구 판매 실제 값이 유효한 가격인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d741-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="5d741-145">위의 세 가지 확인을 수행한 후에도 경비 판매 실제 값에 유효한 가격이 표시되지 않으면 지원 티켓을 기록해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="5d741-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, log a support ticket.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]