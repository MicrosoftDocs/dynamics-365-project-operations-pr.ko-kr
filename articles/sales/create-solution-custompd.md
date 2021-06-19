---
title: 사용자 지정 가격 책정 차원에 대한 솔루션 만들기
description: 이 토픽은 맞춤 가격 책정 차원에 대한 솔루션을 만드는 방법에 대한 정보를 제공합니다.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010344"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7a12a-103">사용자 지정 가격 책정 차원에 대한 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="7a12a-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="7a12a-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="7a12a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="7a12a-105">모든 맞춤 가격 책정 차원 변경은 별도의 솔루션에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="7a12a-106">이 중요한 모범 사례는 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="7a12a-107">요구되는 변경을 수행한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 다시 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="7a12a-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7a12a-108">사용자 지정 가격 책정 차원에 대한 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="7a12a-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="7a12a-109">**설정** > **솔루션** 을 선택한 다음 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="7a12a-110">솔루션의 이름을 *<your organization name> 가격 책정 차원* 으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="7a12a-111">나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![사용자 지정 가격 책정 차원 솔루션 만들기](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7a12a-113">가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="7a12a-114">다음 Project Service 엔터티를 가격 책정 솔루션에 추가하여 가격 책정 솔루션에서 중요한 스키마를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="7a12a-115">이 절차를 완료하면 엔터티는 새 가격 책정 차원을 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="7a12a-116">**설정** > **솔루션** 을 클릭한 다음 **<*조직 명칭*> 가격 책정 차원** 을 더블클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="7a12a-117">솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="7a12a-118">**솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:</span><span class="sxs-lookup"><span data-stu-id="7a12a-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="7a12a-119">**실제**</span><span class="sxs-lookup"><span data-stu-id="7a12a-119">**Actual**</span></span>
   - <span data-ttu-id="7a12a-120">**예약 가능한 리소스**</span><span class="sxs-lookup"><span data-stu-id="7a12a-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="7a12a-121">**추정 라인**</span><span class="sxs-lookup"><span data-stu-id="7a12a-121">**Estimate Line**</span></span>
   - <span data-ttu-id="7a12a-122">**프로젝트 작업**</span><span class="sxs-lookup"><span data-stu-id="7a12a-122">**Project Task**</span></span>
   - <span data-ttu-id="7a12a-123">**송장 라인 세부 정보**</span><span class="sxs-lookup"><span data-stu-id="7a12a-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="7a12a-124">**분개장 항목**</span><span class="sxs-lookup"><span data-stu-id="7a12a-124">**Journal Line**</span></span>
   - <span data-ttu-id="7a12a-125">**프로젝트 계약 내용 세부 정보**</span><span class="sxs-lookup"><span data-stu-id="7a12a-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="7a12a-126">**프로젝트 팀 구성원**</span><span class="sxs-lookup"><span data-stu-id="7a12a-126">**Project Team Member**</span></span>
   - <span data-ttu-id="7a12a-127">**견적 라인 세부 정보**</span><span class="sxs-lookup"><span data-stu-id="7a12a-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="7a12a-128">**역할 가격 인상**</span><span class="sxs-lookup"><span data-stu-id="7a12a-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="7a12a-129">**역할 가격**</span><span class="sxs-lookup"><span data-stu-id="7a12a-129">**Role Price**</span></span>
   - <span data-ttu-id="7a12a-130">**시간 항목**</span><span class="sxs-lookup"><span data-stu-id="7a12a-130">**Time Entry**</span></span>
 
   ![기존 엔터티 사용자 지정 가격 책정 차원 솔루션 추가](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="7a12a-132">각 엔터티에 대해 추가되는 구성 요소와 각 엔터티에 대한 엔터티 자산의 최종 목록을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="7a12a-133">선택한 각 엔터티에 대한 모든 양식과 보기를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-133">Include all forms and views for each of the selected entities.</span></span>

  ![추가된 엔터티](./media/solution-component-selection.png)


5.  <span data-ttu-id="7a12a-135">선택한 엔터티에 대한 종속 엔터티를 포함할지 묻는 메시지가 표시되면 **아니요, 필수 구성 요소를 포함하지 마십시오.** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12a-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![종속 엔터티 포함](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]