---
title: 추정 및 실제에 대한 판매 가격 해결
description: 이 항목은 추정 및 실제 판매율을 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9ce095723e8ac300caf7d11ae37b5c721b57795
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877453"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a><span data-ttu-id="7c635-103">추정 및 실제에 대한 판매 가격 해결</span><span class="sxs-lookup"><span data-stu-id="7c635-103">Resolve sales prices for estimates and actuals</span></span>

<span data-ttu-id="7c635-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7c635-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7c635-105">추정 및 실제의 판매 가격이 Dynamics 365 Project Operations에서 해결되면 시스템은 먼저 관련 프로젝트 견적 또는 계약의 날짜 및 통화를 사용하여 판매 가격표를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-105">When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list.</span></span> <span data-ttu-id="7c635-106">판매 가격표가 해결되면 시스템이 판매 또는 청구 비율을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-106">After the sales price list is resolved, the system resolves the sales or bill rate.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="7c635-107">시간에 대한 실제 및 추정 라인의 판매율 해결</span><span class="sxs-lookup"><span data-stu-id="7c635-107">Resolve sales rates on actual and estimate lines for time</span></span>

<span data-ttu-id="7c635-108">Project Operations에서 시간에 대한 추정 라인은 시간에 대한 견적 라인 및 계약 내용 세부 사항 및 프로젝트의 리소스 지정을 표시하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-108">In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.</span></span>

<span data-ttu-id="7c635-109">판매 가격표가 해결되면 시스템은 다음 단계를 완료하여 청구 비율을 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-109">After a price list for sales is resolved, the system completes the following steps to default the bill rate.</span></span>

1. <span data-ttu-id="7c635-110">시스템은 시간에 대한 추정 라인의 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 필드를 사용하여 해결된 가격표의 역할 가격 라인과 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-110">The system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list.</span></span> <span data-ttu-id="7c635-111">이 일치는 청구 요금에 대해 기본 가격 책정 차원을 사용 중이라고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-111">This matching assumes that out-of-box pricing dimensions for bill rates are being used.</span></span> <span data-ttu-id="7c635-112">대신 또는 추가로 다른 필드를 기반으로 가격을 구성한 경우 **역할**, **리소싱 회사** 및 **리소스 조달 단위**, 일치하는 역할 가격 라인을 검색하는 데 사용되는 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-112">If you have configured pricing based on any other fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then that is the combination that will be used to retrieve a matching role price line.</span></span>
2. <span data-ttu-id="7c635-113">시스템이 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 필드 조합에 대한 청구 비율이 있는 역할 가격 라인을 찾은 경우 해당 청구 비율이 기본값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-113">If the system finds a role price line that has a bill rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** field combination, then that bill rate is defaulted.</span></span>
3. <span data-ttu-id="7c635-114">시스템이 **역할**, **리소싱 회사** 및 **리소스 조달 단위** 필드 값을 일치시킬 수 없는 경우 역할은 일치하지만 **리소스 단위** 값이 널인 역할 가격 라인을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-114">If the system is unable to match the **Role**, **Resourcing Company**, and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**.</span></span> <span data-ttu-id="7c635-115">시스템이 일치하는 역할 가격 레코드를 찾으면 해당 레코드의 청구 요금을 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-115">After the system finds a matching role price record, it will default the bill rate from that record.</span></span> <span data-ttu-id="7c635-116">이 일치는 **역할** 대 **리소스 조달 단위** 의 상대 우선 순위에 대한 기본 구성을 판매 가격 책정 차원으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-116">This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.</span></span>

> [!NOTE]
> <span data-ttu-id="7c635-117">**역할**, **리소싱 회사** 및 **리소스 조달 단위** 의 다른 우선 순위를 구성했거나 우선 순위가 더 높은 다른 차원이 있는 경우 이 동작은 그에 따라 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-117">If you configured a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="7c635-118">시스템은 마지막에 오는 해당 차원에 대해 null 값이 있는 행의 우선 순위에 따라 각 가격 책정 차원 값과 일치하는 값이 있는 역할 가격 레코드를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-118">The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="7c635-119">경비에 대한 실제 및 추정 라인의 판매율 해결</span><span class="sxs-lookup"><span data-stu-id="7c635-119">Resolve sales rates on actual and estimate lines for expense</span></span>

<span data-ttu-id="7c635-120">Project Operations에서 경비에 대한 추정 라인은 경비에 대한 견적 라인 및 계약 내용 세부 사항 및 프로젝트의 경비 추정 라인을 표시하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-120">In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.</span></span>

<span data-ttu-id="7c635-121">판매 가격표가 해결되면 시스템은 다음 단계를 완료하여 단위 판매 가격을 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-121">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="7c635-122">시스템은 해결된 가격표의 범주 가격 라인에 대해 경비를 일치시키기 위해 추정 라인에서 **범주** 및 **단위** 필드 조합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-122">The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="7c635-123">시스템이 **범주** 및 **단위** 필드 조합에 대한 판매율이 있는 범주 가격 라인을 찾은 경우 이것이 판매율 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-123">If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.</span></span>
3. <span data-ttu-id="7c635-124">시스템이 일치하는 범주 가격 라인을 찾으면 가격 책정 방법을 사용하여 판매 가격을 기본값으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-124">If the system finds a matching category price line, the pricing method may be used to default the sales price.</span></span> <span data-ttu-id="7c635-125">아래 표는 Project Operations의 경비 가격 기본값 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-125">The following table below shows the expense price defaulting behavior in Project Operations.</span></span>

    | <span data-ttu-id="7c635-126">컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7c635-126">Context</span></span> | <span data-ttu-id="7c635-127">가격 산정법</span><span class="sxs-lookup"><span data-stu-id="7c635-127">Pricing method</span></span> | <span data-ttu-id="7c635-128">기본 설정 가격</span><span class="sxs-lookup"><span data-stu-id="7c635-128">Price defaulted</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="7c635-129">추정</span><span class="sxs-lookup"><span data-stu-id="7c635-129">Estimate</span></span> | <span data-ttu-id="7c635-130">단가</span><span class="sxs-lookup"><span data-stu-id="7c635-130">Price per unit</span></span> | <span data-ttu-id="7c635-131">범주 가격 라인 기준</span><span class="sxs-lookup"><span data-stu-id="7c635-131">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="7c635-132">원가</span><span class="sxs-lookup"><span data-stu-id="7c635-132">At cost</span></span> | <span data-ttu-id="7c635-133">0.00</span><span class="sxs-lookup"><span data-stu-id="7c635-133">0.00</span></span> |
    | &nbsp; | <span data-ttu-id="7c635-134">비용 초과 가격 인상액</span><span class="sxs-lookup"><span data-stu-id="7c635-134">Markup over cost</span></span> | <span data-ttu-id="7c635-135">0.00</span><span class="sxs-lookup"><span data-stu-id="7c635-135">0.00</span></span> |
    | <span data-ttu-id="7c635-136">실제</span><span class="sxs-lookup"><span data-stu-id="7c635-136">Actual</span></span> | <span data-ttu-id="7c635-137">단가</span><span class="sxs-lookup"><span data-stu-id="7c635-137">Price per unit</span></span> | <span data-ttu-id="7c635-138">범주 가격 라인 기준</span><span class="sxs-lookup"><span data-stu-id="7c635-138">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="7c635-139">원가</span><span class="sxs-lookup"><span data-stu-id="7c635-139">At cost</span></span> | <span data-ttu-id="7c635-140">실제 관련 비용 기준</span><span class="sxs-lookup"><span data-stu-id="7c635-140">Based on the related cost actual</span></span> |
    | &nbsp; | <span data-ttu-id="7c635-141">비용 초과 가격 인상액</span><span class="sxs-lookup"><span data-stu-id="7c635-141">Markup over cost</span></span> | <span data-ttu-id="7c635-142">관련 실제 비용의 단위 비용 비율에 범주 가격 라인에 정의된 인상을 적용</span><span class="sxs-lookup"><span data-stu-id="7c635-142">By applying a markup as defined by the category price line on the unit cost rate of the related cost actual</span></span> |

4. <span data-ttu-id="7c635-143">시스템이 **범주** 및 **단위** 필드 값을 일치시킬 수 없는 경우 판매율은 기본적으로 영(0)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-143">If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="7c635-144">재료에 대한 실제 및 추정 라인에 대한 판매율 해결</span><span class="sxs-lookup"><span data-stu-id="7c635-144">Resolve sales rates on actual and estimate lines for material</span></span>

<span data-ttu-id="7c635-145">Project Operations에서 자재 견적 라인은 자재 견적 라인 및 프로젝트의 자재 견적 라인을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-145">In Project Operations, estimate lines for material are used to denote the quote line and contract line details for materials and the material estimate lines on the project.</span></span>

<span data-ttu-id="7c635-146">판매 가격표가 해결되면 시스템은 다음 단계를 완료하여 단위 판매 가격을 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-146">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="7c635-147">시스템은 해결된 가격표의 가격표 항목 라인과 일치시킬 자재에 대한 추정 라인의 **제품** 및 **단위** 필드 조합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-147">The system uses the **Product** and **Unit** field combination on the estimate line for material to match against the price list item lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="7c635-148">시스템이 **제품** 및 **단위** 필드 조합에 대한 판매율이 있고 가격 책정 방법이 **통화 금액** 인 가격표 항목 라인을 찾은 경우, 가격 목록 라인에 지정된 판매 가격이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-148">If the system finds a price list item line that has a sales rate for the **Product** and **Unit** field combination and pricing method is **Currency amount**, the sales price that is specified on the price list line is used.</span></span>
3. <span data-ttu-id="7c635-149">**제품** 및 **단위** 필드 값이 일치하지 않는 경우 판매율은 기본적으로 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c635-149">If the **Product** and **Unit** field values aren't a match, the sales rate defaults to zero.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
