---
title: 가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기
description: 이 항목은 사용자 정의 옵션 집합 또는 엔터티를 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080090"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="cd2d6-103">가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="cd2d6-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="cd2d6-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="cd2d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd2d6-105">맞춤 옵션 집합 또는 엔터티를 만들려는 경우 언제든지 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd2d6-106">별도의 솔루션에서 모든 맞춤 가격 책정 차원을 변경하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="cd2d6-107">이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="cd2d6-108">요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="cd2d6-109">가격 책정 차원에 대한 맞춤 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="cd2d6-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="cd2d6-110">**설정** > **솔루션** 으로 이동한 다음 **신규** 를 선택하여 새 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="cd2d6-111">솔루션을 명명하고( **\<your organization name>가격 책정 차원** ), 나머지 필수 정보를 입력한 다음, **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="cd2d6-112">가격 책정 차원 솔루션에서 맞춤 필드 및 옵션 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="cd2d6-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="cd2d6-113">가격 책정 차원은 옵션 집합 또는 엔터티일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="cd2d6-114">둘 다 가격 책정 솔루션에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="cd2d6-115">이 절차의 단계는 엔터티 기반 차원 및 옵션 집합 기반 차원을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="cd2d6-116">엔터티 기반 차원</span><span class="sxs-lookup"><span data-stu-id="cd2d6-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="cd2d6-117">**설정** > **솔루션** 으로 이동하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="cd2d6-118">솔루션 탐색기의 왼쪽 탐색 창에서 **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="cd2d6-119">**신규** 를 선택하면 **표준 직함** 으로 불리는 새 엔터티가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="cd2d6-120">나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="cd2d6-121">옵션 세트 기반 차원</span><span class="sxs-lookup"><span data-stu-id="cd2d6-121">Option set-based dimensions</span></span> 
<span data-ttu-id="cd2d6-122">두 개의 옵션 세트 기반 차원을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="cd2d6-123">**리소스 작업 위치** 를 사용하여 **홈** 위치 작업과 **현장** 작업의 가격을 추적하고, 작업이 완료되면 **정규** 및 **초과 근무** 값의 **리소스 작업 시간** 을 사용하여 마크업을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="cd2d6-124">**설정** > **솔루션** 으로 이동하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="cd2d6-125">솔루션 탐색기의 왼쪽 탐색 창에서 **옵션 집합** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="cd2d6-126">**신규** 를 선택하여 새 옵션 집합을 만들고, 나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="cd2d6-127">엔터티 기반 차원에 대한 데이터 만들기</span><span class="sxs-lookup"><span data-stu-id="cd2d6-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="cd2d6-128">엔터티 기반 차원에 대한 데이터를 수동으로 만들거나 Microsoft Excel가져오기 또는 서비스 호출을 사용하여 데이터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="cd2d6-129">이 절차의 단계를 사용하여 엔터티 기반 차원 **표준 직함** 에서 두 개의 표준 직함 **시스템 엔지니어** 및 **선임 시스템 엔지니어** 를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="cd2d6-130">만들려는 데이터가 작으면, 다음 예와 같이 표준 양식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="cd2d6-131">**고급 찾기** 를 선택하고 엔터티 **표준 직함** 을 선택한 다음 **결과** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="cd2d6-132">**표준 직함** 엔터티의 모든 행이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="cd2d6-133">**신규** 를 선택하고 **명칭** 필드에 "시스템 엔지니어"를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="cd2d6-134">양식을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-134">Close the form.</span></span> 
4. <span data-ttu-id="cd2d6-135">1-3 단계를 반복하여 "선임 시스템 엔지니어"를 위한 다른 표준 직함을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="cd2d6-136">가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="cd2d6-137">가격 책정 솔루션에 다음 엔터티를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="cd2d6-138">이 절차의 단계를 사용하여 가격 책정 솔루션에서 몇 가지 중요한 스키마를 변경하여 엔터티가 새 가격 책정 차원을 인식할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="cd2d6-139">**설정** > **솔루션** 을 선택하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="cd2d6-140">솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="cd2d6-141">**솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:</span><span class="sxs-lookup"><span data-stu-id="cd2d6-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="cd2d6-142">실제</span><span class="sxs-lookup"><span data-stu-id="cd2d6-142">Actual</span></span>
  - <span data-ttu-id="cd2d6-143">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="cd2d6-143">Bookable Resource</span></span>
  - <span data-ttu-id="cd2d6-144">추정 라인</span><span class="sxs-lookup"><span data-stu-id="cd2d6-144">Estimate Line</span></span>
  - <span data-ttu-id="cd2d6-145">송장 라인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd2d6-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="cd2d6-146">분개장 항목</span><span class="sxs-lookup"><span data-stu-id="cd2d6-146">Journal Line</span></span>
  - <span data-ttu-id="cd2d6-147">프로젝트 계약 내용 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd2d6-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="cd2d6-148">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="cd2d6-148">Project Team Member</span></span>
  - <span data-ttu-id="cd2d6-149">견적 라인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd2d6-149">Quote Line Detail</span></span>
  - <span data-ttu-id="cd2d6-150">역할 가격 인상</span><span class="sxs-lookup"><span data-stu-id="cd2d6-150">Role Price Markup</span></span>
  - <span data-ttu-id="cd2d6-151">역할 가격</span><span class="sxs-lookup"><span data-stu-id="cd2d6-151">Role Price</span></span> 
  - <span data-ttu-id="cd2d6-152">시간 항목</span><span class="sxs-lookup"><span data-stu-id="cd2d6-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="cd2d6-153">선택한 각 엔터티에 대한 모든 양식과 보기를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="cd2d6-154">위에서 선택한 엔터티에 대한 종속 엔터티를 포함하라는 메시지가 표시되면 **아니요** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

