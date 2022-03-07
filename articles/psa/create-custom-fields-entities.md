---
title: 맞춤 필드 및 엔터티 만들기
description: 이 항목은 Power Apps 플랫폼의 자체 솔루션에서 옵션 집합 및 엔터티를 만드는 방법을 설명합니다.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f501bcc106a296f35bba996b6ab3a8b758cefb1926033faf04ee23c42bc94d39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992439"
---
# <a name="create-custom-fields-and-entities"></a>맞춤 필드 및 엔터티 만들기 

[!include [banner](../includes/psa-now-project-operations.md)]

Power Apps플랫폼에서 맞춤 옵션 집합 또는 엔터티를 만들려는 경우 언제든지 다음 단계를 완료하십시오.  
이 주제의 절차는 Project Service Automation(PSA)의 웹 인터페이스를 사용하여 완료해야 합니다.

> [!IMPORTANT]
> 별도의 솔루션에서 모든 맞춤 가격 책정 차원을 변경하는 것이 좋습니다. 이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다. 요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>가격 책정 차원 솔루션에서 맞춤 필드 및 옵션 세트 만들기

가격 책정 차원은 옵션 집합 또는 엔터티일 수 있습니다. 둘 다 가격 책정 솔루션에서 만들어야 합니다. 이 절차의 단계는 엔터티 기반 차원 및 옵션 집합 기반 차원을 만드는 방법을 설명합니다.

### <a name="entity-based-dimensions"></a>엔터티 기반 차원

1. PSA에서 **설정** > **솔루션** 을 클릭하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다.
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **엔터티** 를 선택합니다.
3. **신규** 를 클릭하면 **표준 직함** 으로 불리는 새 엔터티가 만들어집니다. 나머지 필수 정보를 입력한 다음 **저장** 을 클릭합니다.

> ![표준 직함 엔터티 정의.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>옵션 세트 기반 차원 
두 개의 옵션 세트 기반 차원을 생성할 수 있습니다. **리소스 작업 위치** 를 사용하여 **홈** 위치 작업과 **현장** 작업의 가격을 추적하고, 작업이 완료되면 **정규** 및 **초과 근무** 값의 **리소스 작업 시간** 을 사용하여 마크업을 적용합니다.


1. PSA에서 **설정** > **솔루션** 을 클릭하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다. 
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **옵션 집합** 을 선택합니다. 
3. **신규** 를 클릭하여 새 옵션 집합을 만들고, 나머지 필수 정보를 입력한 다음 **저장** 을 클릭합니다.

> ![리소스 작업 위치로 불리는 옵션 집합 기반 가격 책정 차원.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![리소스 작업 시간으로 불리는 옵션 집합 기반 가격 책정 차원.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>엔터티 기반 차원에 대한 데이터 만들기

엔터티 기반 차원에 대한 데이터를 수동으로 만들거나 Microsoft Excel가져오기 또는 서비스 호출을 사용하여 데이터를 만들 수 있습니다. 이 절차의 단계를 사용하여 엔터티 기반 차원 **표준 직함** 에서 두 개의 표준 직함 **시스템 엔지니어** 및 **선임 시스템 엔지니어** 를 생성합니다. 만들려는 데이터가 작으면, 다음 예와 같이 표준 양식을 사용할 수 있습니다.

1. PSA에서 **상세하게 찾기** 를 클릭합니다. 엔터티 **표준 직함** 을 선택한 다음 **결과** 를 클릭합니다. **표준 직함** 엔터티의 모든 행이 표시됩니다.
2. **새로 만들기** 를 클릭합니다. **명칭** 필드에 "시스템 엔지니어"를 입력한 다음 **저장** 을 클릭합니다.
3. 양식을 닫습니다. 
4. 1-3 단계를 반복하여 "선임 시스템 엔지니어"를 위한 다른 표준 직함을 만듭니다.

> ![표준 직함 엔터티를 위한 샘플 데이터.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]