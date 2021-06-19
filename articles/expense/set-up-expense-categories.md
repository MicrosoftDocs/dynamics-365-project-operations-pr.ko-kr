---
title: 경비 범주 설정
description: 이 항목은 경비 보고서에 대한 경비 범주 및 공유 범주를 설정하는 방법에 대한 정보를 제공합니다.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001805"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="0f678-103">경비 범주 설정</span><span class="sxs-lookup"><span data-stu-id="0f678-103">Set up expense categories</span></span>

<span data-ttu-id="0f678-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0f678-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0f678-105">직원이 경비 보고서를 작성할 때 기록하는 각 경비는 경비 범주와 연관되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="0f678-106">경비 범주는 조직의 법인간에 공유할 수 있는 공유 범주에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="0f678-107">조직이 정의된 방식에 따라 이러한 경비 범주를 다른 영역에서도 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="0f678-108">조직의 정의와 구현 팀의 지침에 따라 경비 관리에 사용되는 범주가 경비 관리에만 사용되는지 아니면 다른 영역에서 공유되어야 하는지 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="0f678-109">이러한 범주는 프로젝트 관리와 회계 및 경비 관리 간에 또는 프로젝트 관리와 회계 및 생산 간에 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="0f678-110">그러나 경비 관리와 생산 간에 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="0f678-111">설정 프로세스를 시작하기 전에 각 경비 범주에 대해 다음 결정을 내려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="0f678-112">경비 범주란 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-112">What is the expense category?</span></span> <span data-ttu-id="0f678-113">예를 들어 항공편, 호텔 또는 마일리지 범주가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="0f678-114">경비 범주를 프로젝트 관리 및 회계에도 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="0f678-115">할 수 있다면 다음 사항도 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0f678-116">다음 경비에 어떤 비용 계정이 사용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="0f678-117">비용</span><span class="sxs-lookup"><span data-stu-id="0f678-117">Cost</span></span>
        - <span data-ttu-id="0f678-118">급여 할당</span><span class="sxs-lookup"><span data-stu-id="0f678-118">Payroll allocation</span></span>
        - <span data-ttu-id="0f678-119">WIP-비용 값</span><span class="sxs-lookup"><span data-stu-id="0f678-119">WIP-cost value</span></span>
        - <span data-ttu-id="0f678-120">비용-항목</span><span class="sxs-lookup"><span data-stu-id="0f678-120">Cost-item</span></span>
        - <span data-ttu-id="0f678-121">WIP-비용 값-항목</span><span class="sxs-lookup"><span data-stu-id="0f678-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="0f678-122">발생 손실</span><span class="sxs-lookup"><span data-stu-id="0f678-122">Accrued loss</span></span>
        - <span data-ttu-id="0f678-123">WIP-발생 손실</span><span class="sxs-lookup"><span data-stu-id="0f678-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="0f678-124">다음 수익원에 어떤 수익 계정이 사용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="0f678-125">송장 발부된 수익</span><span class="sxs-lookup"><span data-stu-id="0f678-125">Invoiced revenue</span></span>
        - <span data-ttu-id="0f678-126">미수 수익-영업 가치</span><span class="sxs-lookup"><span data-stu-id="0f678-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="0f678-127">WIP-영업 가치</span><span class="sxs-lookup"><span data-stu-id="0f678-127">WIP-sales value</span></span>
        - <span data-ttu-id="0f678-128">미수 수익-생산</span><span class="sxs-lookup"><span data-stu-id="0f678-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="0f678-129">WIP-생산</span><span class="sxs-lookup"><span data-stu-id="0f678-129">WIP-production</span></span>
        - <span data-ttu-id="0f678-130">미수 수익-이익</span><span class="sxs-lookup"><span data-stu-id="0f678-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="0f678-131">WIP-이익</span><span class="sxs-lookup"><span data-stu-id="0f678-131">WIP-profit</span></span>
        - <span data-ttu-id="0f678-132">미수 수익-구독</span><span class="sxs-lookup"><span data-stu-id="0f678-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="0f678-133">WIP-구독</span><span class="sxs-lookup"><span data-stu-id="0f678-133">WIP-subscription</span></span>

- <span data-ttu-id="0f678-134">경비 유형이란 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-134">What is the expense type?</span></span>
- <span data-ttu-id="0f678-135">경비 범주에 대한 기본 결제 방법은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="0f678-136">경비 범주의 경비를 항목별로 분류해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="0f678-137">경비 범주에 대한 기본 계정은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="0f678-138">경비 범주에 대한 기본 품목 판매세 그룹은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="0f678-139">경비 범주에 추가 결제 방법이 허용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="0f678-140">그렇다면 어떤 섹션이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-140">If so, what are they?</span></span>
- <span data-ttu-id="0f678-141">이 경비 범주에 하위 범주가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="0f678-142">하위 범주가 있다면 다음 사항도 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f678-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0f678-143">세금 공제에서 제외되는 하위 범주가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="0f678-144">하위 범주의 품목 판매세 그룹은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0f678-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]