---
title: 재료에 대한 비용 및 판매율 설정
description: 이 문서에서는 프로젝트에 사용되는 자재의 비용 및 판매율을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911788"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>재료에 대한 비용 및 판매율 설정

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations의 제품에 대한 비용 및 판매 가격을 설정할 수 있습니다. 제품의 비용 및 판매 가격은 가격 목록 헤더의 통화여야 하는 하나의 통화로만 나열될 수 있습니다.

제품에 대한 비용 및 판매율을 설정하려면 다음 단계를 완료하십시오. 

1. **판매** > **고객** > **가격표** 로 이동하고 **새로 만들기** 를 선택하여 새 가격표를 만듭니다. 
2. 하위 표 메뉴의 **가격표 항목** 에서 **새로운 가격표 항목** 을 선택합니다. 
3. **빨리 만들기** 페이지에서 새 가격을 생성할 제품 및 단위를 입력합니다.

카탈로그 항목의 가격을 정의하는 방법에 대한 자세한 내용은 [가격표 및 가격표 항목으로 제품 가격 정의](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) 및 [통화 및 가격의 소수 자릿수](/dynamics365/sales/decimal-precision-currency-pricing)를 참조하십시오.
> [!NOTE]
> Dynamics 365 Project Operations는 Dynamics 365 Sales로 제품에 대한 모든 가격 책정 방법을 지원하지는 않습니다. 프로젝트에 사용할 제품에 대해 지원되는 유일한 가격 책정 방법은 *통화 금액* 입니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
