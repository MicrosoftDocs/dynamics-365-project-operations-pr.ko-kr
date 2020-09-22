---
title: 시간 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 가격이 시간 비용 실제 값에서 기본값이 0인 이유 해결
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753380"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="58970-103">시간 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="58970-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="58970-104">이 FAQ는 트랜잭션 클래스가 시간으로 설정되고 트랜잭션 유형이 비용인 실제 값에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="58970-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="58970-105">다음 세 가지 검사를 수행하면 시간 비용 실제 값에 대해 가격이 기본값 0이 되는 이유를 쉽게 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58970-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="58970-106">확인 1: 프로젝트에 대한 원가 목록 식별</span><span class="sxs-lookup"><span data-stu-id="58970-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="58970-107">실제 값의 프로젝트 필드에서 프로젝트를 찾아 프로젝트로 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="58970-108">필드에서 계약 단위 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="58970-109">계약 단위 페이지에서 계약 단위가 원가 목록 표에 가격표가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="58970-110">가격표가 둘 이상인 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="58970-111">Project Service는 조직 단위 당 하나의 가격표만 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="58970-112">조직 구성 단위의 원가 목록 표에 연결된 가격표가 하나만 있을 때까지 이 엔터티에서 모든 가격표를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="58970-113">조직 단위에 가격표가 연결되어 있지 않으면 조직 구성 단위의 통화를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="58970-114">Project Service로 이동한 다음 파라미터를 열고 가격표 탭을 엽니다. 컨텍스트가 조직 단위의 통화와 일치하는 비용 및 통화로 설정된 가격표가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="58970-115">해당 기준과 일치하는 가격표가 없으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="58970-116">컨텍스트가 비용으로 설정되고 통화가 조직 단위의 통화와 일치하는 가격표가 하나 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="58970-117">해당 기준과 일치하는 가격표가 두 개 이상인 경우 이 문서를 계속 읽어 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="58970-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="58970-118">확인 2: 시간 비용 실제 값의 특정 날짜에 대해 위의서 식별된 가격표가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="58970-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="58970-119">Project Service에서 기본 가격에 대한 가격표를 고려하려면 해당 가격표가 시간 비용 실제 값의 날짜에 적용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="58970-120">위에서 확인한 가격표가 적용 가능한 경우 다음을 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="58970-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="58970-121">첨부된 가격표에 대한 일반 탭에서 시작 날짜와 종료 날짜가 비어 있지 않은지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="58970-122">위에서 확인한 가격표의 시작 날짜와 종료 날짜가 비어 있으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="58970-123">시간 비용 실제 값에 시작 날짜 필드를 기록해 두고 식별된 가격표가 해당 날짜에 적용되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="58970-124">예를 들어 시간 비용 실제 값의 날짜는 가격표의 시작 날짜와 종료 날짜 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="58970-125">시간 비용 실제 값에 해당 날짜를 포함하는 가격표가 없는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="58970-126">가격표가 시간 비용 실제 값의 날짜를 포함하도록 하려면 가격펴의 시작 및 종료 날짜를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="58970-127">시간 비용 실제 값에 해당 날짜를 포함하는 가격표가 하나 이상 있는 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="58970-128">시간 비용 실제 값의 날짜를 포함하는 가격표가 하나만 있도록 가격표의 시작 및 종료 날짜를 편집하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58970-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="58970-129">시간 비용 실제 값의 해당 날짜를 포함하는 가격표가 하나만 있는 경우 문서에서 다음 확인으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="58970-130">필요한 수정 프로그램을 만든 후에는 시간 항목을 다시 만들고 승인하며 시간 비용 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="58970-131">확인 3: 시간 비용 실제 값에 대한 가격 산정 차원에 대한 가격표에 가격이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="58970-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="58970-132">확인 1 및 확인 2를 성공적으로 완료한 경우 이제 시간 비용 실제 값의 날짜에 적용할 수 있는 가격표가 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="58970-133">이 가격표를 열고 역할 가격 탭으로 이동합니다. 시간 비용 실제 값의 가격 산정 차원에 대한 표에 행이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="58970-134">시간 비용 실제 값의 가격 산정 차원에 대한 역할 가격표에 행이 없으면 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58970-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="58970-135">시간 비용 실제 값의 가격 산정 차원에 대한 역할 가격 표에 행을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58970-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="58970-136">작업이 완료되면 시간 항목을 다시 만들고 승인하며 시간 비용 실제 값이 유효한 가격을 표시하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58970-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="58970-137">위의 세 가지 확인을 수행한 후에도 시간 비용 실제 값에 유효한 가격이 표시되지 않으면 지원 티켓을 기록해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="58970-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



