---
title: 가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기
description: 이 항목은 사용자 정의 옵션 집합 또는 엔터티를 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275636"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="e6598-103">가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="e6598-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="e6598-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e6598-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6598-105">가격 책정 차원으로 사용하기 위한 사용자 지정 옵션 집합 또는 엔터티를 생성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6598-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="e6598-106">자세한 내용은 [가격 책정 차원 개요](pricing-dimensions-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6598-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e6598-107">별도의 솔루션에서 모든 맞춤 가격 책정 차원을 변경하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="e6598-108">이 중요한 모범 사례는 향후 필요에 따라 변경 사항을 업데이트하거나 제거할 수 있는 유연성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="e6598-109">이렇게 하면 작업을 재사용하는데도 도움이 되고 이러한 변경 사항을 다른 인스턴스로 쉽게 이식할 수 있습니다. 필요한 모든 변경을 수행한 후 이 솔루션을 **관리형 솔루션** 으로 내보내고 가격 설정을 재사용하기 위해 다른 인스턴스로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="e6598-110">가격 책정 차원 솔루션에서 맞춤 필드 및 옵션 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="e6598-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="e6598-111">가격 책정 차원은 옵션 집합 또는 엔터티일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="e6598-112">둘 다 가격 책정 솔루션에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="e6598-113">이 절차의 단계는 엔터티 기반 차원 및 옵션 집합 기반 차원을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="e6598-114">엔터티 기반 차원</span><span class="sxs-lookup"><span data-stu-id="e6598-114">Entity-based dimensions</span></span>
<span data-ttu-id="e6598-115">엔터티 기반 차원을 생성하려면 다음 단계를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="e6598-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="e6598-116">**설정** > **솔루션** 으로 이동하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="e6598-117">솔루션 탐색기의 왼쪽 탐색 창에서 **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="e6598-118">**신규** 를 선택하면 **표준 직함** 으로 불리는 새 엔터티가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="e6598-119">나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![표준 직함 엔터티 정의](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="e6598-121">옵션 세트 기반 차원</span><span class="sxs-lookup"><span data-stu-id="e6598-121">Option set-based dimensions</span></span> 
<span data-ttu-id="e6598-122">두 개의 옵션 세트 기반 차원을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="e6598-123">**리소스 작업 위치** 를 사용하여 **집** 위치 작업 및 **현장** 작업의 가격을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="e6598-124">**리소스 작업 시간** 을 값 **정상** 및 **초과 근무** 를 사용하여 작업이 완료되면 가격 인상을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="e6598-125">다음 그래픽은 **리소스 작업 위치** 차원의 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![리소스 작업 위치로 불리는 옵션 집합 기반 가격 책정 차원](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="e6598-127">다음 그래픽은 **리소스 작업 시간** 차원의 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![리소스 작업 시간으로 불리는 옵션 집합 기반 가격 책정 차원](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="e6598-129">**설정** > **솔루션** 으로 이동하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e6598-130">솔루션 탐색기의 왼쪽 탐색 창에서 **옵션 집합** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="e6598-131">**신규** 를 선택하여 새 옵션 집합을 만들고, 나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="e6598-132">엔터티 기반 차원에 대한 데이터 만들기</span><span class="sxs-lookup"><span data-stu-id="e6598-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="e6598-133">엔터티 기반 차원에 대한 데이터를 수동으로 만들거나 Microsoft Excel가져오기 또는 서비스 호출을 사용하여 데이터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="e6598-134">이 절차의 단계를 사용하여 엔터티 기반 차원 **표준 직함** 에서 두 개의 표준 직함 **시스템 엔지니어** 및 **선임 시스템 엔지니어** 를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="e6598-135">만들려는 데이터가 작으면, 다음 예와 같이 표준 양식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="e6598-136">**상세하게 찾기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="e6598-137">엔터티 **표준 직함** 을 선택한 다음 **결과** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="e6598-138">**표준 직함** 엔터티의 모든 행이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="e6598-139">**신규** 를 선택하고 **명칭** 필드에 "시스템 엔지니어"를 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="e6598-140">창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-140">Close the page.</span></span> 
5. <span data-ttu-id="e6598-141">1-3 단계를 반복하여 "선임 시스템 엔지니어"를 위한 다른 표준 직함을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6598-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![표준 직함 엔터티를 위한 샘플 데이터](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]