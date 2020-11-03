---
title: 가격 책정 차원에 대한 맞춤 솔루션 만들기
description: 이 항목은 맞춤 가격 책정 측정 기준을 만들 때 맞춤 솔루션을 만드는 방법을 설명합니다.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080061"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="0a24d-103">가격 책정 차원에 대한 맞춤 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="0a24d-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a24d-104">모든 맞춤 가격 책정 차원 변경은 별도의 솔루션에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="0a24d-105">이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="0a24d-106">요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="0a24d-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="0a24d-107">**설정** > **솔루션** 을 선택한 다음 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="0a24d-108">솔루션을 명명하고( **\<your organization name>가격 책정 차원** ), 나머지 필수 정보를 입력한 다음, **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![가격 책정 차원에 대한 맞춤 솔루션 만들기](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="0a24d-110">가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="0a24d-111">가격 책정 솔루션에 다음 Project Service 엔터티를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="0a24d-112">이 절차의 단계를 완료하여 가격 책정 솔루션에서 몇 가지 중요한 스키마를 변경하여 엔터티가 새 가격 책정 차원을 인식할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="0a24d-113">**설정** > **솔루션** 을 선택하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="0a24d-114">솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="0a24d-115">**솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:</span><span class="sxs-lookup"><span data-stu-id="0a24d-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="0a24d-116">실제</span><span class="sxs-lookup"><span data-stu-id="0a24d-116">Actual</span></span>
- <span data-ttu-id="0a24d-117">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="0a24d-117">Bookable Resource</span></span>
- <span data-ttu-id="0a24d-118">추정 라인</span><span class="sxs-lookup"><span data-stu-id="0a24d-118">Estimate Line</span></span>
- <span data-ttu-id="0a24d-119">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="0a24d-119">Project Task</span></span>
- <span data-ttu-id="0a24d-120">송장 라인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="0a24d-120">Invoice Line Detail</span></span>
- <span data-ttu-id="0a24d-121">분개장 항목</span><span class="sxs-lookup"><span data-stu-id="0a24d-121">Journal Line</span></span>
- <span data-ttu-id="0a24d-122">프로젝트 계약 내용 세부 정보</span><span class="sxs-lookup"><span data-stu-id="0a24d-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="0a24d-123">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="0a24d-123">Project Team Member</span></span>
- <span data-ttu-id="0a24d-124">견적 라인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="0a24d-124">Quote Line Detail</span></span>
- <span data-ttu-id="0a24d-125">역할 가격 인상</span><span class="sxs-lookup"><span data-stu-id="0a24d-125">Role Price Markup</span></span>
- <span data-ttu-id="0a24d-126">역할 가격</span><span class="sxs-lookup"><span data-stu-id="0a24d-126">Role Price</span></span> 
- <span data-ttu-id="0a24d-127">시간 항목</span><span class="sxs-lookup"><span data-stu-id="0a24d-127">Time Entry</span></span> 

> ![가격 책정 차원 솔루션에 기존 엔터티 추가](media/Existing-entities-to-PD-solution.png)

> ![솔루션 구성 요소 선택](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="0a24d-130">선택한 각 엔터티에 대한 모든 양식과 보기를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="0a24d-131">선택한 엔터티에 대한 종속 엔터티를 포함하라는 메시지가 표시되면 **아니요** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a24d-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![모든 관련 구성 요소를 포함하지 마십시오](media/Do-not-include-required.png)


