---
title: 맞춤 필드 및 엔터티 만들기
description: 이 항목은 Power Apps 플랫폼의 자체 솔루션에서 옵션 집합 및 엔터티를 만드는 방법을 설명합니다.
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
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144871"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="9b35a-103">맞춤 필드 및 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="9b35a-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9b35a-104">Power Apps플랫폼에서 맞춤 옵션 집합 또는 엔터티를 만들려는 경우 언제든지 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b35a-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="9b35a-105">이 주제의 절차는 Project Service Automation(PSA)의 웹 인터페이스를 사용하여 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b35a-106">별도의 솔루션에서 모든 맞춤 가격 책정 차원을 변경하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="9b35a-107">이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="9b35a-108">요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b35a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="9b35a-109">가격 책정 차원 솔루션에서 맞춤 필드 및 옵션 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="9b35a-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="9b35a-110">가격 책정 차원은 옵션 집합 또는 엔터티일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="9b35a-111">둘 다 가격 책정 솔루션에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="9b35a-112">이 절차의 단계는 엔터티 기반 차원 및 옵션 집합 기반 차원을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="9b35a-113">엔터티 기반 차원</span><span class="sxs-lookup"><span data-stu-id="9b35a-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="9b35a-114">PSA에서 **설정** > **솔루션** 을 클릭하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="9b35a-115">솔루션 탐색기의 왼쪽 탐색 창에서 **엔터티** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="9b35a-116">**신규** 를 클릭하면 **표준 직함** 으로 불리는 새 엔터티가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="9b35a-117">나머지 필수 정보를 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![표준 직함 엔터티 정의](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="9b35a-119">옵션 세트 기반 차원</span><span class="sxs-lookup"><span data-stu-id="9b35a-119">Option set-based dimensions</span></span> 
<span data-ttu-id="9b35a-120">두 개의 옵션 세트 기반 차원을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="9b35a-121">**리소스 작업 위치** 를 사용하여 **홈** 위치 작업과 **현장** 작업의 가격을 추적하고, 작업이 완료되면 **정규** 및 **초과 근무** 값의 **리소스 작업 시간** 을 사용하여 마크업을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="9b35a-122">PSA에서 **설정** > **솔루션** 을 클릭하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9b35a-123">솔루션 탐색기의 왼쪽 탐색 창에서 **옵션 집합** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="9b35a-124">**신규** 를 클릭하여 새 옵션 집합을 만들고, 나머지 필수 정보를 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="9b35a-125">리소스 작업 위치로 불리는 옵션 집합 기반 가격 책정 차원</span><span class="sxs-lookup"><span data-stu-id="9b35a-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="9b35a-126">리소스 작업 시간으로 불리는 옵션 집합 기반 가격 책정 차원</span><span class="sxs-lookup"><span data-stu-id="9b35a-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="9b35a-127">엔터티 기반 차원에 대한 데이터 만들기</span><span class="sxs-lookup"><span data-stu-id="9b35a-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="9b35a-128">엔터티 기반 차원에 대한 데이터를 수동으로 만들거나 Microsoft Excel가져오기 또는 서비스 호출을 사용하여 데이터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="9b35a-129">이 절차의 단계를 사용하여 엔터티 기반 차원 **표준 직함** 에서 두 개의 표준 직함 **시스템 엔지니어** 및 **선임 시스템 엔지니어** 를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="9b35a-130">만들려는 데이터가 작으면, 다음 예와 같이 표준 양식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="9b35a-131">PSA에서 **상세하게 찾기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="9b35a-132">엔터티 **표준 직함** 을 선택한 다음 **결과** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="9b35a-133">**표준 직함** 엔터티의 모든 행이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="9b35a-134">**새로 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-134">Click **New**.</span></span> <span data-ttu-id="9b35a-135">**명칭** 필드에 "시스템 엔지니어"를 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="9b35a-136">양식을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-136">Close the form.</span></span> 
4. <span data-ttu-id="9b35a-137">1-3 단계를 반복하여 "선임 시스템 엔지니어"를 위한 다른 표준 직함을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b35a-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="9b35a-138">표준 직함 엔터티를 위한 샘플 데이터</span><span class="sxs-lookup"><span data-stu-id="9b35a-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


