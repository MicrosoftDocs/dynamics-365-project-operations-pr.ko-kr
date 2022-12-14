---
title: 원가율에서 판매 가격을 계산하도록 통화 변환 설정
description: 이 문서에서는 비용 트랜잭션에서 판매 트랜잭션이 생성될 때 Microsoft Dynamics 365 Project Operations에서 사용될 통화 변환 동작을 구성하는 방법에 대해 설명합니다.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816672"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>원가율에서 판매 가격을 계산하도록 통화 변환 설정

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Microsoft Dynamics 365 Project Operations에서 비용 범주의 판매 가격은 숫자 값으로 설정하거나 발생한 비용을 기준으로 계산되도록 설정할 수 있습니다.

발생한 비용을 기준으로 계산되도록 설정한 경우 다음 옵션을 사용할 수 있습니다.

- 원가
- 비용 대비 마크업 비율

프로젝트 계약의 판매 통화와 다른 통화로 비용 비용이 발생하는 경우 비용을 기준으로 판매 가격을 계산하려면 통화 변환이 필요합니다.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>기본 Dataverse 환율을 사용하는 통화 변환 동작

기본적으로 Project Operations는 Dataverse의 통화 테이블에 저장된 통화 환율을 사용합니다. 기본 환율을 사용하여 비용에서 판매 가격을 계산하도록 Project Operations를 구성하려면 다음 단계를 따르세요.

1. **Project Operations \> 설정 \> 매개 변수** 로 이동합니다.
1. **프로젝트 매개변수** 세부 정보 페이지를 엽니다.
1. **환율 변환 논리** 필드를 빈 값으로 설정합니다.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>금융 및 운영 앱의 환율을 사용하는 통화 변환 동작

기본적으로 Dataverse에서 사용할 수 있는 통화 테이블의 환율은 유효하지 않습니다. 따라서 원가율에서 판매 가격을 계산하기 위한 요구 사항에 따라 크기가 조정되지 않을 수도 있습니다.

금융 및 운영 환경의 환율을 사용하여 비용 통화의 비용 비율에서 판매 통화의 판매 가격을 계산할 수 있습니다. 이 통화 변환 동작을 구성하려면 다음 단계를 따르세요.

1. **프로젝트 매개변수** 페이지에서 **환율 변환 논리** 필드를 추가합니다. 그런 다음 사용자 지정을 저장하고 게시합니다.
1. **Project Operations \> 설정 \> 매개 변수** 로 이동합니다.
1. **프로젝트 매개변수** 세부 정보 페이지를 엽니다. 
1. **환율 변환 동작** 필드를 **대체와 함께 확장됨을 기본값** 으로 설정합니다.
1. **이중 쓰기 앱 사용자** 보안 역할에 다음 테이블에 대한 **전역 읽기** 권한을 부여합니다.

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. 금융 및 운영 환경에서 초기 동기화와 함께 다음 이중 쓰기 맵을 실행합니다.

    - 환율 유형(msdyn\_exchangeratetypes)
    - 환율 통화 쌍(msdyn\_currencyexchangeratepairs)
    - CDS 환율(msdyn\_currencyexchangerates)

이러한 변경이 완료되면 이중 쓰기를 통해 금융 및 운영 환경의 환율을 Dataverse에서 사용할 수 있습니다. 그런 다음 Project Operations는 해당 환율을 사용하여 원가율을 계약의 판매 통화로 변환합니다.

> [!NOTE]
> 이 통화 변환 동작은 원가율에서 판매 가격을 계산하는 경우에만 적용됩니다. 일반적으로 기본 통화 값을 계산하는 데 사용되지 않습니다. 기본 통화 값은 이 절차를 완료했는지 여부에 관계없이 항상 기본 Dataverse 환율을 사용합니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
