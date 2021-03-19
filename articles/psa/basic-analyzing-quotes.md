---
title: 프로젝트 견적 분석
description: 이 항목은 프로젝트 견적 분석에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291267"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="0e0b3-103">프로젝트 견적 분석</span><span class="sxs-lookup"><span data-stu-id="0e0b3-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0e0b3-104">Dynamics 365 Project Service Automation은 프로젝트 견적을 분석하여 수익성을 추산합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="0e0b3-105">또한 견적이 인도일 또는 완료일에 대한 고객의 기대와 예산에 얼마나 잘 부합하는지를 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="0e0b3-106">수익성 분석</span><span class="sxs-lookup"><span data-stu-id="0e0b3-106">Profitability analysis</span></span>

<span data-ttu-id="0e0b3-107">Project Service Automation은 총 마진과 조정된 총 마진을 사용하여 수익성을 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="0e0b3-108">총 마진은 다음 공식을 사용하여 계산됩니다:</span><span class="sxs-lookup"><span data-stu-id="0e0b3-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="0e0b3-109">조정된 총 마진은 다음 공식을 사용하여 계산됩니다:</span><span class="sxs-lookup"><span data-stu-id="0e0b3-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="0e0b3-110">총 마진과 조정된 총 마진의 값들이 큰 폭으로 다른 경우, 견적에서 작업의 대부분은 청구 불가능으로 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="0e0b3-111">고객 기대 분석</span><span class="sxs-lookup"><span data-stu-id="0e0b3-111">Analysis of customer expectations</span></span>

<span data-ttu-id="0e0b3-112">다음 필드에 값을 입력하면 견적을 분석하고 스케줄 및 예산에 대한 고객 기대에 대한 차트를 생성할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="0e0b3-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="0e0b3-113">견적 표제의 **요청된 인도일** 필드.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="0e0b3-114">각 견적 행에 대한 **고객 예산** 필드(프로젝트 기반 행 및 제품 기반 행의 경우).</span><span class="sxs-lookup"><span data-stu-id="0e0b3-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="0e0b3-115">스케줄에 대한 고객 기대 분석은 견적 행 내역의 가장 늦은 종료 날짜와 요청된 인도일을 비교하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="0e0b3-116">예산에 대한 고객 기대 분석은 총 고객 예산의 합과 모든 견적 행의 견적 금액을 비교하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b3-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]