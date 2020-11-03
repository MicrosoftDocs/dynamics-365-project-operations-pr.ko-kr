---
title: 경비 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 가격이 경비 비용 실제 값에서 기본값이 0인 이유 해결
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080073"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>경비 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

이 FAQ는 트랜잭션 클래스가 경비로 설정되고 트랜잭션 유형이 비용인 경비 실제 값에 적용됩니다.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>경비 비용 실제 값에서 비용 문제 해결

관련 경비 항목으로 이동하여 경비 항목 필드에 금액이 있는지 확인합니다. 원래 경비 항목에 금액 필드가 채워지지 않은 경우 문제가 해결된 것입니다.
 
이 문제를 해결하려면 유효한 금액으로 경비 항목을 다시 만들고 승인하십시오.