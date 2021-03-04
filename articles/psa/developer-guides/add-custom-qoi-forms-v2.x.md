---
title: 새 맞춤 엔터티 양식 추가 (Project Service Automation 2.x)
description: 이 항목은 Dynamics 365 Project Service Automation 2.x에서 기회, 견적, 주문 또는 청구서를 위한 맞춤 엔터티 양식을 추가하는 방법에 대한 정보를 제공합니다.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144601"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="ae6d1-103">새 맞춤 엔터티 양식 추가 (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="ae6d1-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="ae6d1-104">타입 필드</span><span class="sxs-lookup"><span data-stu-id="ae6d1-104">Type field</span></span> 

<span data-ttu-id="ae6d1-105">Dynamics 365 Project Service Automation은 기회, 견적, 주문 또는 청구서 엔터티의 **타입**(**msdyn\_ordertype**) 필드에 의존하여 이러한 엔터티의 **작업 기반** 버전을 **품목 기반** 및 **서비스 기반** 버전과 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="ae6d1-106">이러한 엔터티의 작업 기반 버전은 PSA가 취급합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="ae6d1-107">클라이언트측 및 서버측 솔루션의 많은 비즈니스 논리가 **타입** 필드에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="ae6d1-108">따라서 엔터티를 만들 때 필드를 올바른 값으로 초기화하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="ae6d1-109">값이 잘못되면 잘못된 동작이 발생할 수 있으며 일부 비즈니스 논리가 올바르게 실행되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="ae6d1-110">자동 양식 전환</span><span class="sxs-lookup"><span data-stu-id="ae6d1-110">Automatic form switching</span></span>

<span data-ttu-id="ae6d1-111">매출액 엔터티 레코드의 잘못된 초기화 및 편집으로 인해 발생할 수 있는 데이터 손상 및 예상치 못한 동작의 가능성을 방지하기 위해 PSA에는 이제 즉시 사용 양식에서 자동 양식 전환에 대한 논리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="ae6d1-112">이 논리는 사용자를 작업 기반 버전 또는 다른 타입의 기회, 견적, 주문 또는 청구서 엔터티 작업을 위한 올바른 양식으로 데려갑니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="ae6d1-113">사용자가 작업 기반 버전의 기회, 견적, 주문 또는 청구서 엔터티를 열면 양식이 **프로젝트 정보** 로 전환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="ae6d1-114">자동 양식 전환 논리는 **formId** 값과 **msdyn\_ordertype** 필드 사이의 매핑에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="ae6d1-115">해당 매핑에 모든 즉시 사용 양식이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="ae6d1-116">단, 맞춤 양식을 수동으로 추가하여 취급하려는 엔터티 버전을 나타내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="ae6d1-117">이는 **msdyn\_ordertype** 필드에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="ae6d1-118">매핑에서 양식 전환이 누락된 경우 논리는 엔터티의 **msdyn\_ordertype** 필드에 저장된 값에 근거하여 즉시 사용 가능한 양식으로 전환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="ae6d1-119">맞춤 양식을 추가하고 양식 전환 논리를 켜십시오.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="ae6d1-120">다음 예는 맞춤 양식인 **내 프로젝트 정보** 를 추가함으로써 작업 기반 기회와 함께 작동하도록 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="ae6d1-121">동일한 프로세스를 사용하여 맞춤 양식을 추가함으로써 견적, 주문 및 청구서와 함께 작동하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="ae6d1-122">이러한 단계를 따라 **프로젝트 정보** 양식의 맞춤 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="ae6d1-123">기회 엔터티에서 **프로젝트 정보** 양식을 열고, **내 프로젝트 정보** 라는 이름으로 복사본을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="ae6d1-124">새 양식을 연 다음 특성에서 **프로젝트 정보** 양식의 양식 초기화 스크립트가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="ae6d1-125">스크립트를 제거하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-125">Don't remove the scripts.</span></span> <span data-ttu-id="ae6d1-126">제거하면 일부 데이터가 잘못 초기화될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="ae6d1-127">양식에 **타입**(**msdyn\_ordertype**) 필드가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="ae6d1-128">이 필드를 제거하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-128">Don't remove this field.</span></span> <span data-ttu-id="ae6d1-129">제거하면 초기화 스크립트가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="ae6d1-130">새 양식의 **formId** 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="ae6d1-131">이 단계를 두 가지 방법으로 완료할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="ae6d1-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="ae6d1-132">**내 프로젝트 정보** 양식을 비관리 솔루션의 일부로 내보낸 다음, 내보낸 솔루션의 customization.xml 파일에서 **formId** 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="ae6d1-133">양식 편집기에서 **내 프로젝트 정보** 양식을 연 다음, 다음 그림과 같이 URL에서 **fromId** 파라미터 옆에 있는 전역 고유 식별자(GUID)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![URL에서 새 양식의 formId 값](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="ae6d1-135">msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js 웹 리소스를 편집하여 **formId** 값을 위한 **msdyn\_ordertype** 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="ae6d1-136">리소스에서 코드를 제거하고 다음 코드로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="ae6d1-137">맞춤화를 저장한 다음 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-137">Save and then publish the customizations.</span></span>
