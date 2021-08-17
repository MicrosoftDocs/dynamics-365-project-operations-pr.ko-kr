---
title: 사용자 지정 가격 책정 차원에 대한 솔루션 만들기
description: 이 토픽은 맞춤 가격 책정 차원에 대한 솔루션을 만드는 방법에 대한 정보를 제공합니다.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992214"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>사용자 지정 가격 책정 차원에 대한 솔루션 만들기

 _**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_ 

>[!IMPORTANT]
>모든 맞춤 가격 책정 차원 변경은 별도의 솔루션에 있어야 합니다. 이 중요한 모범 사례는 필요에 따라 변경 내용을 업데이트하거나 제거할 수 있는 유연성을 제공하고, 작업을 다시 사용하는 데 도움이 되며, 이러한 변경 내용을 다른 인스턴스로 쉽게 나를 수 있도록 합니다. 요구되는 변경을 수행한 후, 이 솔루션을 **관리형 솔루션** 으로 내보내고 다른 인스턴스로 가져와 다시 사용하십시오.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>사용자 지정 가격 책정 차원에 대한 솔루션 만들기

1.  **설정** > **솔루션** 을 선택한 다음 **새로 만들기** 를 선택합니다.
2.  솔루션의 이름을 *<your organization name> 가격 책정 차원* 으로 지정합니다.
3. 나머지 필수 정보를 입력한 다음 **저장** 을 선택합니다.

  ![사용자 지정 가격 책정 차원 솔루션 만들기.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>가격 책정 차원 솔루션을 위한 모든 필수 엔터티 및 관련 구성 요소를 추가합니다.

다음 Project Service 엔터티를 가격 책정 솔루션에 추가하여 가격 책정 솔루션에서 중요한 스키마를 변경합니다. 이 절차를 완료하면 엔터티는 새 가격 책정 차원을 인식합니다.

1.  **설정** > **솔루션** 을 클릭한 다음 **<*조직 명칭*> 가격 책정 차원** 을 더블클릭합니다.
2.  솔루션 탐색기의 왼쪽 탐색 창에서 **기존 추가** > **엔터티** 를 선택합니다.
3.  **솔루션 구성 요소** 대화 상자에서 다음 엔터티를 선택합니다:
 
   - **실제**
   - **예약 가능한 리소스**
   - **추정 라인**
   - **프로젝트 작업**
   - **송장 라인 세부 정보**
   - **분개장 항목**
   - **프로젝트 계약 내용 세부 정보**
   - **프로젝트 팀 구성원**
   - **견적 라인 세부 정보**
   - **역할 가격 인상**
   - **역할 가격**
   - **시간 항목**
 
   ![기존 엔터티 사용자 지정 가격 책정 차원 솔루션 추가.](./media/Existing-entities-to-PD-solution.png)
 
 4. 각 엔터티에 대해 추가되는 구성 요소와 각 엔터티에 대한 엔터티 자산의 최종 목록을 검토합니다. 

   >[!NOTE]
   > 선택한 각 엔터티에 대한 모든 양식과 보기를 포함합니다.

  ![추가된 엔터티.](./media/solution-component-selection.png)


5.  선택한 엔터티에 대한 종속 엔터티를 포함할지 묻는 메시지가 표시되면 **아니요, 필수 구성 요소를 포함하지 마십시오.** 를 선택합니다.

    ![종속 엔터티 포함.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]