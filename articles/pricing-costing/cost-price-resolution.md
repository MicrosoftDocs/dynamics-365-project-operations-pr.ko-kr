---
title: 추정 및 실제 원가 해결
description: 이 항목은 추정 및 실제의 원가를 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877320"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="f90ec-103">추정 및 실제 원가 해결</span><span class="sxs-lookup"><span data-stu-id="f90ec-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="f90ec-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f90ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f90ec-105">추정 및 실제에 대한 원가 및 비용 가격표를 해결하기 위해 시스템은 관련 프로젝트의 **날짜**, **통화** 및 **계약 단위** 필드의 정보를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="f90ec-106">비용 가격표가 해결된 후 응용 프로그램은 비용 요금을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="f90ec-107">시간에 대한 실제 및 추정 라인의 비용 요금 해결</span><span class="sxs-lookup"><span data-stu-id="f90ec-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="f90ec-108">시간에 대한 추정 라인은 프로젝트의 시간 및 리소스 지정에 대한 견적 및 계약 내용 세부 사항을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="f90ec-109">원가 가격표가 확인된 후 시스템은 시간에 대한 추정 라인의 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 필드를 사용하여 가격표의 역할 가격 라인과 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-109">After a cost price list is resolved, the system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="f90ec-110">이 일치는 인력 비용에 대해 기본 가격 책정 차원을 사용한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="f90ec-111">대신 또는 추가로 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 필드를 일치시키도록 시스템을 구성한 경우 다른 조합을 사용하여 일치하는 역할 가격 라인을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-111">If you configured the system to match fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="f90ec-112">응용 프로그램이 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 조합에 대한 비용 비율이 있는 역할 가격 라인을 찾은 경우 이것이 기본 비용 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-112">If the application finds a role price line that has a cost rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="f90ec-113">응용 프로그램이 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 값의 조합과 정확히 일치할 수 없는 경우 다음과 같은 역할 가격 라인을 검색합니다. 역할 값과 일치하지만 **리소싱 단위** 및 **리소싱 회사** 에 대해 null 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-113">If the application can't exactly match the combination of **Role**, **Resourcing Company**, and **Resourcing Unit** values, it will retrieve role price lines with a matching role value, but have null values for **Resourcing Unit** and **Resourcing Company**.</span></span> <span data-ttu-id="f90ec-114">역할 가격 값이 일치하는 일치하는 역할 가격 레코드를 찾으면 해당 레코드에서 비용 비율이 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-114">After a matching role price record with matching role price value is found, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="f90ec-115">**역할**, **리소싱 회사** 및 **리소스 조달 단위** 의 다른 우선 순위를 구성했거나 우선 순위가 더 높은 다른 차원이 있는 경우 이 동작은 그에 따라 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-115">If you configure a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="f90ec-116">시스템은 우선 순위에서 마지막에 오는 차원에 대해 null 값이 있는 행의 우선 순위에 따라 각 가격 책정 차원 값과 일치하는 값이 있는 역할 가격 레코드를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last in the priority order.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="f90ec-117">경비에 대한 실제 및 추정 라인의 비용 요금 해결</span><span class="sxs-lookup"><span data-stu-id="f90ec-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="f90ec-118">경비에 대한 추정 라인은 프로젝트의 경비 및 경비 추정 라인에 대한 견적 및 계약 내용 세부 사항을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="f90ec-119">원가 가격표가 확인된 후 시스템은 추정 라인의 **범주** 및 **단위** 필드의 조합을 사용하여 경비를 **범주 가격** 과 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="f90ec-120">시스템이 **범주** 및 **단위** 필드 조합에 대한 비용 요금이 있는 범주 가격 라인을 찾은 경우 이것이 비용 요금이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="f90ec-121">시스템이 **범주** 및 **단위** 값을 일치시킬 수 없거나 또는 일치하는 범주 가격 라인을 찾을 수 있지만 가격 책정 방법이 **단가** 가 아닌 경우 비용 요금은 기본적으로 영(0)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="f90ec-122">자재에 대한 실제 및 추정 라인에 대한 비용 요금 해결</span><span class="sxs-lookup"><span data-stu-id="f90ec-122">Resolving cost rates on actual and estimate lines for material</span></span>

<span data-ttu-id="f90ec-123">자재 견적 라인은 자재 견적 및 계약 내용 상세 내역과 프로젝트의 자재 견적 라인을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-123">Estimate lines for material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="f90ec-124">가격표 항목이 해결된 후 시스템은 추정 라인의 **제품** 및 **단위** 필드의 조합을 사용하여 해결된 가격표의 **가격표 항목** 라인과 일치하는 예상 재표를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="f90ec-125">시스템이 **제품** 및 **단위** 필드 조합에 대한 비용 요금이 있는 제품 가격 라인을 찾으면 비용 요금이 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="f90ec-126">시스템이 **제품** 및 **단위** 값과 일치할 수 없는 경우 단위 비용은 기본적으로 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-126">If the system can't match the **Product** and **Unit** values, the unit cost defaults to zero.</span></span> <span data-ttu-id="f90ec-127">이 기본값은 일치하는 가격표 항목 라인이 있지만 가격 책정 방법이 제품에 정의되지 않은 표준 비용 또는 현재 비용을 기반으로 하는 경우에도 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="f90ec-127">This default will also happen if there is a matching price list item line, but the pricing method is based on a standard cost or current cost that isn't defined in the product.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
