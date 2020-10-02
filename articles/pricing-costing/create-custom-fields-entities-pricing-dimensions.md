---
title: 가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기
description: 이 항목은 사용자 정의 옵션 집합 또는 엔터티를 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898269"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>가격 책정 차원으로 사용자 지정 필드 및 엔터티 만들기

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

맞춤 옵션 집합 또는 엔터티를 만들려는 경우 언제든지 다음 단계를 완료하십시오.

> [!IMPORTANT]
> 별도의 솔루션에서 모든 맞춤 가격 책정 차원을 변경하는 것이 좋습니다. 이 중요한 모범 사례는 나중에 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다. 요구되는 모든 변경을 한 후, 이 솔루션을 **관리형 솔루션**으로 내보내고 다른 인스턴스로 가져와 가격 책정 설정을 다시 사용하십시오.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>가격 책정 차원에 대한 맞춤 솔루션 만들기
1. **설정** > **솔루션**으로 이동한 다음 **신규**를 선택하여 새 솔루션을 만듭니다. 
2. 솔루션을 명명하고(**\<your organization name>가격 책정 차원**), 나머지 필수 정보를 입력한 다음, **저장**을 선택합니다.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>가격 책정 차원 솔루션에서 맞춤 필드 및 옵션 세트 만들기

가격 책정 차원은 옵션 집합 또는 엔터티일 수 있습니다. 둘 다 가격 책정 솔루션에서 만들어야 합니다. 이 절차의 단계는 엔터티 기반 차원 및 옵션 집합 기반 차원을 만드는 방법을 설명합니다.

### <a name="entity-based-dimensions"></a>엔터티 기반 차원

1. **설정** > **솔루션**으로 이동하고 **\<your organization name>가격 책정 차원**을 두 번 클릭합니다.
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **엔터티**를 선택합니다.
3. **신규**를 선택하면 **표준 직함**으로 불리는 새 엔터티가 만들어집니다. 
4. 나머지 필수 정보를 입력한 다음 **저장**을 선택합니다.


### <a name="option-set-based-dimensions"></a>옵션 세트 기반 차원 
두 개의 옵션 세트 기반 차원을 생성할 수 있습니다. **리소스 작업 위치**를 사용하여 **홈** 위치 작업과 **현장** 작업의 가격을 추적하고, 작업이 완료되면 **정규** 및 **초과 근무** 값의 **리소스 작업 시간**을 사용하여 마크업을 적용합니다.


1. **설정** > **솔루션**으로 이동하고 **\<your organization name>가격 책정 차원**을 두 번 클릭합니다. 
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **옵션 집합**을 선택합니다. 
3. **신규**를 선택하여 새 옵션 집합을 만들고, 나머지 필수 정보를 입력한 다음 **저장**을 선택합니다.

## <a name="create-data-for-entity-based-dimensions"></a>엔터티 기반 차원에 대한 데이터 만들기

엔터티 기반 차원에 대한 데이터를 수동으로 만들거나 Microsoft Excel가져오기 또는 서비스 호출을 사용하여 데이터를 만들 수 있습니다. 이 절차의 단계를 사용하여 엔터티 기반 차원 **표준 직함**에서 두 개의 표준 직함 **시스템 엔지니어** 및 **선임 시스템 엔지니어**를 생성합니다. 만들려는 데이터가 작으면, 다음 예와 같이 표준 양식을 사용할 수 있습니다.

1. **고급 찾기**를 선택하고 엔터티 **표준 직함**을 선택한 다음 **결과**를 선택합니다. **표준 직함** 엔터티의 모든 행이 표시됩니다.
2. **신규**를 선택하고 **명칭** 필드에 "시스템 엔지니어"를 입력한 다음 **저장**을 선택합니다.
3. 양식을 닫습니다. 
4. 1-3 단계를 반복하여 "선임 시스템 엔지니어"를 위한 다른 표준 직함을 만듭니다.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.
가격 책정 솔루션에 다음 엔터티를 추가해야 합니다. 이 절차의 단계를 사용하여 가격 책정 솔루션에서 몇 가지 중요한 스키마를 변경하여 엔터티가 새 가격 책정 차원을 인식할 수 있도록 합니다.

1. **설정** > **솔루션**을 선택하고 **\<your organization name>가격 책정 차원**을 두 번 클릭합니다. 
2. 솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티**를 선택합니다.
3. **솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:

  - 실제
  - 예약 가능한 리소스
  - 추정 라인
  - 송장 라인 세부 정보
  - 분개장 항목
  - 프로젝트 계약 내용 세부 정보
  - 프로젝트 팀 구성원
  - 견적 라인 세부 정보
  - 역할 가격 인상
  - 역할 가격 
  - 시간 항목 


> [!NOTE]
> 선택한 각 엔터티에 대한 모든 양식과 보기를 포함해야 합니다.

4. 위에서 선택한 엔터티에 대한 종속 엔터티를 포함하라는 메시지가 표시되면 **아니요**를 선택합니다.

