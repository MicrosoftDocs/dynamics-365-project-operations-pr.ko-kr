---
title: 프로젝트 스테이지 비즈니스 프로세스 흐름을 사용자 지정하려면 어떻게 해야 합니까?
description: 프로젝트 단계의 비즈니스 프로세스 흐름을 맞춤화하는 방법의 개요.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286166"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="f4a5d-103">프로젝트 스테이지 비즈니스 프로세스 흐름을 사용자 지정하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="f4a5d-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="f4a5d-104">이전 버전의 Project Service 응용 프로그램에는 프로젝트 스테이지 비즈니스 프로세스 흐름의 스테이지 이름이 예상되는 영어 이름(**Quote**, **Plan**, **Close**)과 정확히 일치해야 한다는 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="f4a5d-105">그렇지 않으면 영어 스테이지 이름에 의존하는 비즈니스 논리가 예상대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="f4a5d-106">그렇기 때문에 프로젝트 양식에서 **스위치 프로세스** 또는 **편집 프로세스** 와 같은 익숙한 작업을 볼 수 없으며 비즈니스 프로세스 흐름을 사용자 지정하는 것은 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="f4a5d-107">이 제한은 버전 2.4.5.48 이상에서 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="f4a5d-108">이 문서에서는 기본 비즈니스 프로세스 흐름을 사용자 지정해야 하는 경우 이전 버전에 대한 권장 해결 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="f4a5d-109">비즈니스 논리는 영어 스테이지 이름과 정확히 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="f4a5d-110">프로젝트 스테이지 비즈니스 프로세스 흐름에는 앱에서 다음 동작을 구동하는 비즈니스 논리가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="f4a5d-111">프로젝트가 견적과 연결되면 코드는 비즈니스 프로세스 흐름을 **Quote** 스테이지로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="f4a5d-112">프로젝트가 계약과 연결되면 코드는 비즈니스 프로세스 흐름을 **Plan** 스테이지로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="f4a5d-113">비즈니스 프로세스 흐름이 **Close** 단계로 진행되면 프로젝트 레코드가 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="f4a5d-114">프로젝트가 비활성화되면 프로젝트 양식 및 WBS(작업 분할 구조)가 읽기 전용으로 설정되고 명명된 리소스 예약이 해제되며 관련 가격표는 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="f4a5d-115">이 비즈니스 논리는 프로젝트 스테이지의 영어 이름에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="f4a5d-116">영어 스테이지 이름에 대한 이러한 의존성은 프로젝트 스테이지 비즈니스 프로세스 흐름의 사용자 지정을 권장하지 않는 주요 이유는 물론, 프로젝트 엔터티에 **스위치 프로세스** 또는 **프로세스 편집** 과 같은 일반적인 비즈니스 프로세스 흐름 동작이 표시되지 않는 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="f4a5d-117">스테이지 이름이 영어 이름과 일치하지 않으면 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="f4a5d-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="f4a5d-118">8.2 플랫폼의 Project Service 앱 버전 1.x에서 비즈니스 프로세스 흐름의 스테이지 이름이 영어 스테이지 이름과 정확하게 일치하지 않으면 견적 또는 계약에 적합한 스테이지를 설정하거나 프로젝트를 닫는 비즈니스 논리가 생략됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="f4a5d-119">오류 메시지는 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-119">No error messages are displayed.</span></span> <span data-ttu-id="f4a5d-120">따라서 프로젝트 스테이지 비즈니스 프로세스 흐름을 사용자 지정할 수 있는 것으로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="f4a5d-121">그러나 견적, 계약 및 프로젝트 종료에 대해 작동하는 자동 프로세스는 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="f4a5d-122">9.0 플랫폼의 Project Service 앱 버전 2.4.4.30 또는 그 이전에는 비즈니스 프로세스 흐름에 중요한 아키텍처가 변경되었으며, 이는 비즈니스 프로세스 흐름 비즈니스 논리를 다시 작성해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="f4a5d-123">따라서 프로세스 스테이지 이름이 예상되는 영어 이름과 일치하지 않으면 오류 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="f4a5d-124">따라서 프로젝트 엔터티에 대한 프로젝트 스테이지 비즈니스 프로세스 흐름을 사용자 지정하려는 경우 프로젝트 엔터티의 기본 비즈니스 프로세스 흐름에 완전히 새로운 스테이지를 추가할 수 있을 뿐 아니라 **Quote**, **Plan** 및 **Close** 스테이지를 그대로 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="f4a5d-125">이 제한은 비즈니스 프로세스 흐름에서 영어 스테이지 이름이 예상되는 비즈니스 논리에서 오류가 발생하지 않도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="f4a5d-126">버전 2.4.5.48 이상에서는 이 문서에서 설명하는 비즈니스 논리가 프로젝트 엔터티의 기본 비즈니스 프로세스 흐름에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="f4a5d-127">해당 버전 이상으로 업그레이드하면 기본 비즈니스 프로세스 흐름을 사용자 지정하거나 자신의 것으로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="f4a5d-128">이전 버전의 해결 방법</span><span class="sxs-lookup"><span data-stu-id="f4a5d-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="f4a5d-129">업그레이드가 옵션이 아닌 경우 다음 두 가지 방법 중 하나로 프로젝트 엔터티에 대한 프로젝트 스테이지 비즈니스 프로세스 흐름을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="f4a5d-130">**Quote**, **Plan** 및 **Close** 에 대한 영어 스테이지 이름을 유지하면서 기본 구성에 추가 스테이지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![기본 구성에 스테이지를 추가하는 스크린샷](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="f4a5d-132">고유한 비즈니스 프로세스 흐름을 만들고 이를 프로젝트 엔터티의 주요 비즈니스 프로세스 흐름으로 만들어 원하는 모든 스테이지 이름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="f4a5d-133">그러나 동일한 표준 프로젝트 단계 **Quote**, **Plan** 및 **Close** 를 사용하려는 경우 사용자 지정 스테이지 이름에서 구동되는 일부 사용자 지정을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="f4a5d-134">더 복잡한 논리는 프로젝트를 종료하는 것이며, 프로젝트 레코드를 비활성화하는 것 만으로도 트리거될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF 사용자 지정](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="f4a5d-136">플랫폼 9.0의 Project Service 앱 버전 2.4.4.30 이전 버전에 대한 추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="f4a5d-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="f4a5d-137">플랫폼 9.0의 Project Service 2.4.4.30 또는 이전 버전에서 사용자 지정 비즈니스 프로세스 흐름을 사용하여 **스테이지별 프로젝트** 차트 및 프로젝트 목록에 사용되는 프로젝트 엔터티의 **스테이지 이름** 필드는 기본 프로젝트 스테이지 비즈니스 프로세스 흐름에 복사되므로 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="f4a5d-138">이 문제는 다음 단계를 통해 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="f4a5d-139">사용자 지정 비즈니스 프로세스 흐름을 진행하면서 업데이트되는 현재 비즈니스 프로세스 흐름 스테이지를 캡처하는 사용자 지정 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="f4a5d-140">기본 구성 대신 사용자 지정 필드로 작업할 수 있도록 **스테이지별 프로젝트** 차트를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="f4a5d-141">프로젝트 엔터티에 대한 사용자 고유의 비즈니스 프로세스 흐름을 만드는 단계</span><span class="sxs-lookup"><span data-stu-id="f4a5d-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="f4a5d-142">프로젝트 엔터티에 대한 사용자 고유의 비즈니스 프로세스 흐름을 만들려면 다음을 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="f4a5d-143">**설정** > **프로세스 센터** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="f4a5d-144">Project Service 비즈니스 논리도 복사하기 때문에 프로젝트 스테이지 비즈니스 프로세스 흐름은 복사하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![프로세스 만들기](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="f4a5d-146">프로세스 디자이너를 사용하여 원하는 스테이지 이름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="f4a5d-147">**Quote**, **Plan** 및 **Close** 를 위한 기본 스테이지와 동일한 기능을 원하는 경우 사용자 지정 비즈니스 프로세스 흐름의 스테이지 이름을 기반으로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![BPF를 사용자 지정하는 데 사용되는 프로세스 디자이너의 스크린샷](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="f4a5d-149">프로세스 디자이너에서 **주문 프로세스 흐름** 을 클릭하여 프로젝트 스테이지 비즈니스 프로세스 흐름을 목록의 맨 위로 이동시켜 사용자 지정 비즈니스 프로세스 흐름이 프로젝트 엔터티에 대한 기본 비즈니스 프로세스 흐름이 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="f4a5d-150">주문 프로세스 흐름 사용의 스크린샷</span><span class="sxs-lookup"><span data-stu-id="f4a5d-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="f4a5d-151">다음 단계는 9.0 플랫폼의 Project Service 앱 2.4.4.30 이전 버전에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="f4a5d-152">프로젝트 엔터티에 새 사용자 지정 필드를 추가하여 사용자 지정 비즈니스 프로세스 흐름의 사용자 지정 스테이지를 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="f4a5d-153">사용자 지정 비즈니스 프로세스 흐름의 스테이지가 업데이트될 때 이 필드를 업데이트하려면 비즈니스 논리(플러그 인/워크플로)를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![프로젝트 엔터티 사용자 지정 스크린샷](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="f4a5d-155">스테이지에 대해 새로운 사용자 지정 필드를 사용하도록 **스테이지별 프로젝트** 차트를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![스테이지별 프로젝트 차트 사용의 스크린샷](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="f4a5d-157">스테이지에 대해 새로운 사용자 지정 필드를 포함하도록 프로젝트 엔터티에 대한 보기를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![프로젝트 엔터티의 보기 수정 스크린샷](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]