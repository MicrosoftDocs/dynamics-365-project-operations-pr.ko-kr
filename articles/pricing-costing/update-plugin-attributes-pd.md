---
title: 새 가격 책정 차원을 포함하도록 플러그인 특성 업데이트
description: 이 주제는 가격 책정 차원에 대한 플러그인 특성을 업데이트하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004629"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>새 가격 책정 차원을 포함하도록 플러그인 특성 업데이트

이 주제는 가격 책정 차원에 대한 플러그인 특성을 업데이트하는 방법에 대한 정보를 제공합니다.

> [!NOTE]
> 이 토픽은 Dynamics 365 Project Operations의 견적 및 계약 기능에만 적용됩니다.

## <a name="prerequisites"></a>필수 구성 요소
이 토픽의 단계를 완료하기 전에 다음 토픽의 절차를 완료해야 합니다.

  - [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities-pricing-dimensions.md) 
  - [가격 설정 및 거래 엔터티에 사용자 지정 필드 추가](add-custom-fields-price-setup-transactional-entities.md)
  - [가격 책정 차원의 사용자 지정 필드 설정](set-up-custom-fields-pricing-dimensions.md). 
  
이러한 절차를 완료하지 않은 경우 완료한 다음 이 항목으로 돌아오십시오.

## <a name="register-a-plug-in"></a>플러그 인 등록
견적 라인 세부 정보가 생성되면 프로젝트 견적 라인의 **견적 라인** 페이지에서 시스템은 두 개의 견적 라인을 생성합니다. 한 라인은 견적의 비용 측면이고 다른 라인은 판매 측면입니다. 프로젝트 계약 행에도 마찬가지입니다.

원가 측면에서 수량 또는 필드를 변경하면 해당 변경이 매출액 측에서 이루어집니다. 이것은 Quotelinedetail 및 contractline 세부 항목의 PreOperation 플러그인이 비용 측면의 특정 속성을 트랜잭션의 판매 측면에 연결하기 때문에 가능합니다. 판매 측의 가격 책정 차원 값을 비용 측에서도 변경해야 하는 경우 가격 책정 차원을 변경한 후 다음 플러그인을 다시 등록해야 합니다.

다음은 업데이트 및 재등록할 플러그인입니다.

- PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction 업데이트**
- PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction 업데이트**

플러그인을 업데이트하고 다시 등록하려면 다음 단계를 완료하십시오.

1. **PluginRegistrationTool** 을 열고 Project Operations Dataverse 환경에 연결합니다.
2. **검색** 을 선택하고 업데이트할 플러그인의 처음 몇 글자를 입력합니다.
3. 플러그인을 찾은 후 플러그인을 선택한 다음 **기본 양식에서 선택** 을 선택합니다.
4. **msdyn_orderlinetransaction 업데이트** 단계를 선택하고 마우스 오른쪽 버튼으로 클릭한 다음, **업데이트** 를 선택합니다.
5. **업데이트** 대화 상자 페이지에서 필터링 속성의 타원(**...**)을 클릭합니다.
6. 필터링 속성 창이 열리고 엔터티 및 가격 책정 차원의 모든 특성 목록이 제공됩니다. 가격 책정 차원 특성의 선택란을 선택합니다.
7. **OK** 를 선택하여 페이지를 닫은 다음 **업데이트 단계** 를 선택합니다.
8. 두 번째 플러그인 **PreOperationQuoteLineDetail** 에 대해 2-7 단계를 반복합니다. 이 플러그인의 경우 **msdyn_quotelinetransaction 업데이트** 단계를 업데이트해야 합니다.
9. **PluginRegistrationTool** 을 닫습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]