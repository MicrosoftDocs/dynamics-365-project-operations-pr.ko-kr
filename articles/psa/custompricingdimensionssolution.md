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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144647"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>가격 책정 차원에 대한 맞춤 솔루션 만들기

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> 모든 맞춤 가격 책정 차원 변경은 별도의 솔루션에 있어야 합니다. 이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다. 요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.

1. **설정** > **솔루션** 을 선택한 다음 **새로 만들기** 를 선택합니다. 
2. 솔루션을 명명하고(**\<your organization name>가격 책정 차원**), 나머지 필수 정보를 입력한 다음, **저장** 을 선택합니다.

> ![가격 책정 차원에 대한 맞춤 솔루션 만들기](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.
가격 책정 솔루션에 다음 Project Service 엔터티를 추가해야 합니다. 이 절차의 단계를 완료하여 가격 책정 솔루션에서 몇 가지 중요한 스키마를 변경하여 엔터티가 새 가격 책정 차원을 인식할 수 있도록 합니다.

1. **설정** > **솔루션** 을 선택하고 **\<your organization name>가격 책정 차원** 을 두 번 클릭합니다. 
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티** 를 선택합니다.
3. **솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:

- 실제
- 예약 가능한 리소스
- 추정 라인
- 프로젝트 작업
- 송장 라인 세부 정보
- 분개장 항목
- 프로젝트 계약 내용 세부 정보
- 프로젝트 팀 구성원
- 견적 라인 세부 정보
- 역할 가격 인상
- 역할 가격 
- 시간 항목 

> ![가격 책정 차원 솔루션에 기존 엔터티 추가](media/Existing-entities-to-PD-solution.png)

> ![솔루션 구성 요소 선택](media/Dimension-Components.png)

> [!NOTE]
> 선택한 각 엔터티에 대한 모든 양식과 보기를 포함해야 합니다.

4. 선택한 엔터티에 대한 종속 엔터티를 포함하라는 메시지가 표시되면 **아니요** 를 선택합니다.

> ![모든 관련 구성 요소를 포함하지 마십시오](media/Do-not-include-required.png)


