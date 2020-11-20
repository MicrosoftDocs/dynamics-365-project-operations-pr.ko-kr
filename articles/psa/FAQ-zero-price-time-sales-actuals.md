---
title: 시간 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 가격이 시간 판매 실제 값에서 기본값이 0인 이유 해결
author: rumant
manager: kfend
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
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125951"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="c34cc-103">시간 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="c34cc-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c34cc-104">이 FAQ는 트랜잭션 클래스가 시간으로 설정되고 트랜잭션 유형이 미청구된 판매인 실제 값에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="c34cc-105">다음 세 가지 검사를 수행하면 시간 판매 실제 값에 대해 가격(대금 청구 요금)이 기본값 0이 되는 이유를 쉽게 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="c34cc-106">확인 1: 프로젝트에 대한 판매 가격표 식별</span><span class="sxs-lookup"><span data-stu-id="c34cc-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="c34cc-107">실제 값의 프로젝트 필드에서 프로젝트를 찾아 프로젝트로 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="c34cc-108">그런 다음 영업 탭으로 이동하고 프로젝트 계약 내용 표에서 프로젝트 계약 필드의 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="c34cc-109">프로젝트 계약 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-109">The project Contract page will open.</span></span> <span data-ttu-id="c34cc-110">프로젝트 계약 페이지에서 프로젝트 가격표 탭으로 이동합니다. 여기에 가격표가 하나 이상 첨부되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="c34cc-111">프로젝트 계약의 프로젝트 가격표 표에 첨부된 가격표가 없는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="c34cc-112">가격표를 프로젝트 가격표 표에 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="c34cc-113">여기에 첨부할 수 있는 가격표에는 컨텍스트 필드가 판매로 설정되어 있고 가격표의 통화 필드는 프로젝트 계약의 통화 필드와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="c34cc-114">필요한 수정 프로그램을 만든 후에는 시간 항목을 다시 만들고 승인하며 미청구 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="c34cc-115">프로젝트 계약의 프로젝트 가격표 표에 하나 이상의 가격표가 첨부되어 있는 경우 문서의 다음 확인으로 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="c34cc-116">확인 2: 시간 판매 실제 값의 특정 날짜에 대해 위의서 식별된 가격표가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="c34cc-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="c34cc-117">Project Service에서 기본 가격에 대한 가격표를 고려하려면 해당 가격표가 시간 판매 실제 값의 날짜에 적용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="c34cc-118">위에서 확인한 가격표가 적용 가능한 경우 다음을 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="c34cc-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="c34cc-119">첨부된 가격표에 대한 일반 탭에서 시작 날짜와 종료 날짜가 비어 있지 않은지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="c34cc-120">위에서 확인한 가격표의 시작 날짜와 종료 날짜가 비어 있으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="c34cc-121">시간 판매 실제 값에 시작 날짜 필드를 기록해 두고 식별된 가격표가 해당 날짜에 적용되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="c34cc-122">예를 들어 시간 판매 실제 값의 날짜는 가격표의 시작 날짜와 종료 날짜 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="c34cc-123">시간 판매 실제 값에 해당 날짜를 포함하는 가격표가 없는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="c34cc-124">가격표가 시간 판매 실제 값의 날짜를 포함하도록 하려면 가격표의 시작 및 종료 날짜를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="c34cc-125">시간 판매 실제 값에 해당 날짜를 포함하는 가격표가 하나 이상 있는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="c34cc-126">시간 판매 실제 값의 날짜를 포함하는 가격표가 하나만 있도록 가격표의 시작 및 종료 날짜를 편집하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="c34cc-127">시간 판매 실제 값의 해당 날짜를 포함하는 가격표가 하나만 있는 경우 확인 3으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="c34cc-128">필요한 수정 프로그램을 만든 후에는 시간 항목을 다시 만들고 승인하며 시간 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="c34cc-129">확인 3: 시간 판매 실제 값에 대한 가격 산정 차원에 대한 가격표에 가격이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="c34cc-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="c34cc-130">확인 1 및 확인 2를 성공적으로 완료한 경우 이제 시간 판매 실제 값의 날짜에 적용할 수 있는 가격표가 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="c34cc-131">이 가격표를 열고 역할 가격 탭으로 이동합니다. 시간 판매 실제 값의 가격 산정 차원에 대한 표에 행이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="c34cc-132">시간 판매 실제 값의 가격 산정 차원에 대한 역할 가격표에 행이 없으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="c34cc-133">시간 판매 실제 값의 가격 산정 차원에 대한 역할 가격 표에 행을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="c34cc-134">작업이 완료되면 시간 항목을 다시 만들고 승인하며 시간 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c34cc-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="c34cc-135">위의 세 가지 확인을 수행한 후에도 시간 판매 실제 값에 유효한 가격이 표시되지 않으면 지원 티켓을 기록해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="c34cc-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 

