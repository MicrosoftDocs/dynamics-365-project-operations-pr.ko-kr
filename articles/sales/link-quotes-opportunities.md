---
title: 영업 기회에서 프로젝트 견적 작성
description: 이 항목은 영업 기회에서 프로젝트 견적 생성에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898540"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="00474-103">영업 기회에서 프로젝트 견적 작성</span><span class="sxs-lookup"><span data-stu-id="00474-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="00474-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="00474-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00474-105">다음과 같은 방법으로 프로젝트 영업 기회에서 견적을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="00474-106">**프로젝트 영업 기회** 페이지의 **견적** 탭에서</span><span class="sxs-lookup"><span data-stu-id="00474-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="00474-107">영업 기회 영업 프로세스 흐름에서</span><span class="sxs-lookup"><span data-stu-id="00474-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="00474-108">기존 견적에 대한 영업 기회 참조를 업데이트하여</span><span class="sxs-lookup"><span data-stu-id="00474-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="00474-109">프로젝트 영업 기회 페이지의 견적 탭에서</span><span class="sxs-lookup"><span data-stu-id="00474-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="00474-110">영업 기회에서 프로젝트 견적을 작성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="00474-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="00474-111">**프로젝트 영업 기회** 페이지를 열고 **견적** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="00474-112">**견적** 하위 표에서 **+** 영업 기회에 따라 새 프로젝트 견적을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="00474-113">모든 영업 기회 라인 및 관련 프로젝트 가격표가 영업 기회의 새 견적으로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="00474-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="00474-114">영업 기회 영업 프로세스 흐름에서</span><span class="sxs-lookup"><span data-stu-id="00474-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="00474-115">영업 기회 영업 프로세스 흐름에서 견적을 작성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="00474-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="00474-116">영업 기회 영업 프로세스 흐름에서 영업 기회를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="00474-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="00474-117">**우량으로 선별** 스테이지를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="00474-118">**다음**을 선택한 다음 **+ 만들기**를 선택하여 새 견적을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="00474-119">이 새 견적에 대한 **요약** 탭에 있는 대부분의 정보는 영업 기회에서 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="00474-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="00474-120">누락된 필수 정보를 입력하거나 **요약** 탭에서 필요에 따라 기본값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="00474-121">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-121">Select **Save**.</span></span> <span data-ttu-id="00474-122">새 견적이 생성되고 영업 기회에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="00474-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="00474-123">이제 **영업 기회** 페이지의 **견적** 탭에서 견적 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="00474-124">영업 기회 영업 프로세스는 다음 스테이지 **제안**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="00474-125">기존 견적에 대한 영업 기회 참조를 업데이트하여</span><span class="sxs-lookup"><span data-stu-id="00474-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="00474-126">기존 견적을 영업 기회에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="00474-127">기존 견적에 대한 영업 기회 정보를 업데이트하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="00474-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="00474-128">**견적** 페이지를 열고 **요약** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="00474-129">**영업 기회** 필드에서 견적에 연결할 영업 기회를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00474-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="00474-130">영업 기회의 **견적** 그리드에서 견적을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="00474-131">영업 기회 영업 프로세스를 사용하여 영업 기회를 다음 스테이지 **제안**으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="00474-132">영업 기회를 이 스테이지로 이동할 때 이 영업 기회와 연관된 견적 목록에서 이 견적을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="00474-133">이 견적을 선택하면 앞으로 진행하고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00474-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="00474-134">영업 기회와 관련된 다른 모든 견적은 그 중 하나를 얻을 때까지 계속 사용할 수 있으며 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="00474-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="00474-135">영업 프로세스를 이전 스테이지 **우량으로 선별**로 다시 이동하고 다른 견적을 선택하여 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00474-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
