---
title: 경비 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 가격이 경비 비용 실제 값에서 기본값이 0인 이유 해결
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285852"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="0bf00-103">경비 비용 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0bf00-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0bf00-104">이 FAQ는 트랜잭션 클래스가 경비로 설정되고 트랜잭션 유형이 비용인 경비 실제 값에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bf00-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="0bf00-105">경비 비용 실제 값에서 비용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="0bf00-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="0bf00-106">관련 경비 항목으로 이동하여 경비 항목 필드에 금액이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf00-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="0bf00-107">원래 경비 항목에 금액 필드가 채워지지 않은 경우 문제가 해결된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf00-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="0bf00-108">이 문제를 해결하려면 유효한 금액으로 경비 항목을 다시 만들고 승인하십시오.</span><span class="sxs-lookup"><span data-stu-id="0bf00-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]