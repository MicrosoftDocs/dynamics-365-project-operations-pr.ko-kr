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
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284861"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>새 맞춤 엔터티 양식 추가 (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>타입 필드 

Dynamics 365 Project Service Automation은 기회, 견적, 주문 또는 청구서 엔터티의 **타입**(**msdyn\_ordertype**) 필드에 의존하여 이러한 엔터티의 **작업 기반** 버전을 **품목 기반** 및 **서비스 기반** 버전과 구분합니다. 이러한 엔터티의 작업 기반 버전은 PSA가 취급합니다. 클라이언트측 및 서버측 솔루션의 많은 비즈니스 논리가 **타입** 필드에 의존합니다. 따라서 엔터티를 만들 때 필드를 올바른 값으로 초기화하는 것이 중요합니다. 값이 잘못되면 잘못된 동작이 발생할 수 있으며 일부 비즈니스 논리가 올바르게 실행되지 않을 수 있습니다.

## <a name="automatic-form-switching"></a>자동 양식 전환

매출액 엔터티 레코드의 잘못된 초기화 및 편집으로 인해 발생할 수 있는 데이터 손상 및 예상치 못한 동작의 가능성을 방지하기 위해 PSA에는 이제 즉시 사용 양식에서 자동 양식 전환에 대한 논리가 포함되어 있습니다. 이 논리는 사용자를 작업 기반 버전 또는 다른 타입의 기회, 견적, 주문 또는 청구서 엔터티 작업을 위한 올바른 양식으로 데려갑니다. 사용자가 작업 기반 버전의 기회, 견적, 주문 또는 청구서 엔터티를 열면 양식이 **프로젝트 정보** 로 전환됩니다.

자동 양식 전환 논리는 **formId** 값과 **msdyn\_ordertype** 필드 사이의 매핑에 의존합니다. 해당 매핑에 모든 즉시 사용 양식이 추가되었습니다. 단, 맞춤 양식을 수동으로 추가하여 취급하려는 엔터티 버전을 나타내야 합니다. 이는 **msdyn\_ordertype** 필드에 근거합니다. 매핑에서 양식 전환이 누락된 경우 논리는 엔터티의 **msdyn\_ordertype** 필드에 저장된 값에 근거하여 즉시 사용 가능한 양식으로 전환됩니다.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>맞춤 양식을 추가하고 양식 전환 논리를 켜십시오.

다음 예는 맞춤 양식인 **내 프로젝트 정보** 를 추가함으로써 작업 기반 기회와 함께 작동하도록 하는 방법을 보여 줍니다. 동일한 프로세스를 사용하여 맞춤 양식을 추가함으로써 견적, 주문 및 청구서와 함께 작동하도록 합니다.

이러한 단계를 따라 **프로젝트 정보** 양식의 맞춤 버전을 만듭니다.

1. 기회 엔터티에서 **프로젝트 정보** 양식을 열고, **내 프로젝트 정보** 라는 이름으로 복사본을 저장합니다.
2. 새 양식을 연 다음 특성에서 **프로젝트 정보** 양식의 양식 초기화 스크립트가 있는지 확인합니다. 

    > [!IMPORTANT]
    > 스크립트를 제거하지 마십시오. 제거하면 일부 데이터가 잘못 초기화될 수 있습니다.

3. 양식에 **타입**(**msdyn\_ordertype**) 필드가 있는지 확인합니다. 

    > [!IMPORTANT]
    > 이 필드를 제거하지 마십시오. 제거하면 초기화 스크립트가 실패합니다.

4. 새 양식의 **formId** 값을 찾습니다. 이 단계를 두 가지 방법으로 완료할 수 있습니다:

    - **내 프로젝트 정보** 양식을 비관리 솔루션의 일부로 내보낸 다음, 내보낸 솔루션의 customization.xml 파일에서 **formId** 값을 찾습니다.
    - 양식 편집기에서 **내 프로젝트 정보** 양식을 연 다음, 다음 그림과 같이 URL에서 **fromId** 파라미터 옆에 있는 전역 고유 식별자(GUID)를 찾습니다.

    ![URL에서 새 양식의 formId 값](media/how-to-add-custom-forms-in-v2.0.png)

5. msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js 웹 리소스를 편집하여 **formId** 값을 위한 **msdyn\_ordertype** 매핑을 만듭니다. 리소스에서 코드를 제거하고 다음 코드로 대체합니다.

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

6. 맞춤화를 저장한 다음 게시합니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]