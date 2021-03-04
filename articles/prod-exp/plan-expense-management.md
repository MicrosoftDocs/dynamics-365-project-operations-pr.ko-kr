---
title: 경비 관리 구성
description: 이 문서에서는 Microsoft Dynamics 365 Finance에서 경비 관리를 구성하기 전에 계획 프로세스 중에 고려해야 할 사항과 결정 사항에 대해 설명합니다.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960345"
---
# <a name="configure-expense-management"></a><span data-ttu-id="0cfaf-103">경비 관리 구성</span><span class="sxs-lookup"><span data-stu-id="0cfaf-103">Configure expense management</span></span>

<span data-ttu-id="0cfaf-104">이 항목에서는 경비 관리를 구성하기 전에 계획 프로세스 중에 고려해야 할 사항과 결정 사항에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="0cfaf-105">경비 관리에서 결제 방법, 여행 요청, 경비 보고서, 정책 등에 대한 정보를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="0cfaf-106">경비 관리를 위한 구성을 계획할 때 내리는 많은 결정은 조직의 계층 및 재무 구조를 기반으로 하기 때문에 해당 영역에 대한 계획 문서를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="0cfaf-107">회사 간 경비</span><span class="sxs-lookup"><span data-stu-id="0cfaf-107">Intercompany expenses</span></span>

<span data-ttu-id="0cfaf-108">회사 간 경비를 활성화하면 법인 및 직원이 다른 법인을 대신하여 비용이 발생하도록 허용하고 조직 내 고용 법인으로부터 지불금을 징수합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="0cfaf-109">예를 들어, 법인 A의 직원이 법인 B의 프로젝트를 완료하고 프로젝트에 여행 관련 경비가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="0cfaf-110">회사 간 경비가 활성화된 경우 직원은 경비를 법인 B에 전기할 경비 보고서를 제출할 수 있으며, 그 경비는 법인 A가 지불해야 합니다. 조직에 법인이 여러 개 없는 경우 회사 간 경비를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="0cfaf-111">**결정:** 회사 간 경비를 활성화하시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="0cfaf-112">재무 관리</span><span class="sxs-lookup"><span data-stu-id="0cfaf-112">Financial management</span></span>

<span data-ttu-id="0cfaf-113">경비 관리는 조직의 재무 관리와 긴밀하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="0cfaf-114">경비 관리에 대한 많은 구성은 조직의 재정에 대해 내린 결정을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="0cfaf-115">다음 섹션에서는 조직의 재무 결정 및 리더십 팀의 지침에 따라 계획 및 결정이 필요한 다양한 영역을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="0cfaf-116">일비</span><span class="sxs-lookup"><span data-stu-id="0cfaf-116">Per diems</span></span>

<span data-ttu-id="0cfaf-117">조직이 제공하는 직원 일비를 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="0cfaf-118">일비는 일반적으로 식사, 숙박 및 기타 부수적 경비와 같은 경비를 충당하는 데 사용되기 때문에 조직에서 제공하는 일비 수당에 대한 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="0cfaf-119">일비 요율은 연중 시간, 여행 위치 또는 둘 다를 기반으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="0cfaf-120">일비 규칙을 정의할 때 근로자가 무료 급식 또는 서비스를 받는 경우 일비 비율의 일정 비율이 보류되도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="0cfaf-121">일비 요율이 근로자의 출장에 적용될 수 있는 최소 및 최대 시간을 설정하도록 일비 요율 계층을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="0cfaf-122">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-122">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-123">첫날과 마지막 날의 일비 기본 규칙:</span><span class="sxs-lookup"><span data-stu-id="0cfaf-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="0cfaf-124">직원이 하루 동안 청구하고 일비를 받을 수 있는 최소 시간은 얼마입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="0cfaf-125">첫날과 마지막 날 식사에 제공되는 금액이 감소합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="0cfaf-126">감소가 있는 경우 감소율은 얼마입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0cfaf-127">첫날과 마지막 날 호텔에 제공되는 금액이 감소합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="0cfaf-128">감소가 있는 경우 감소율은 얼마입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0cfaf-129">첫날과 마지막 날 발생하는 기타 경비에 제공되는 금액이 감소합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="0cfaf-130">감소가 있는 경우 감소율은 얼마입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="0cfaf-131">기본 일비 규칙:</span><span class="sxs-lookup"><span data-stu-id="0cfaf-131">Default per diem rules:</span></span>

    - <span data-ttu-id="0cfaf-132">예를 들어, 무료 식사인 경우 각 식사에 대한 일비 수당에서 비율 감소가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="0cfaf-133">감소가 있는 경우 각 식사에 대한 감소율은 얼마입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="0cfaf-134">식사 감소는 일일, 여행 당 또는 일일 식사 횟수로 계산됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="0cfaf-135">일비 금액을 정기적으로 반올림하거나 반올림해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="0cfaf-136">일비는 24시간제 또는 역일로 계산됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="0cfaf-137">위치를 기반으로 하는 일비 규칙:</span><span class="sxs-lookup"><span data-stu-id="0cfaf-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="0cfaf-138">일비 요율은 지역에 따라 다릅니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="0cfaf-139">어떤 위치가 포함됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-139">What locations are included?</span></span>
    - <span data-ttu-id="0cfaf-140">일비 요율이 위치에 따라 다를 경우, 각 위치에 대해 다음 유형의 비용에 대해 몇 퍼센트가 제공됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="0cfaf-141">식사</span><span class="sxs-lookup"><span data-stu-id="0cfaf-141">Meals</span></span>
        - <span data-ttu-id="0cfaf-142">호텔</span><span class="sxs-lookup"><span data-stu-id="0cfaf-142">Hotel</span></span>
        - <span data-ttu-id="0cfaf-143">기타 경비</span><span class="sxs-lookup"><span data-stu-id="0cfaf-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="0cfaf-144">경비 관리 분개 및 계정</span><span class="sxs-lookup"><span data-stu-id="0cfaf-144">Expense management journals and accounts</span></span>

<span data-ttu-id="0cfaf-145">경비 관리를 위해서는 여러 분개와 계정을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="0cfaf-146">예를 들어 현금 서비스 및 신용 카드 분쟁에 동일한 계정이 사용되는지 여부를 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="0cfaf-147">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-147">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-148">승인된 경비 보고서가 전기되는 원장 분개장은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="0cfaf-149">현금 서비스에 사용되는 계정은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="0cfaf-150">현금 서비스를 즉시 전기해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="0cfaf-151">결제 방법</span><span class="sxs-lookup"><span data-stu-id="0cfaf-151">Payment methods</span></span>

<span data-ttu-id="0cfaf-152">직원이 회사를 대신하여 경비를 부담하도록 허용하는 경우 직원이 사용할 수 있는 결제 방법을 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="0cfaf-153">예를 들어 직원이 현금이나 회사 신용 카드를 사용하도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="0cfaf-154">직원이 개인 신용 카드를 사용하도록 허용한 다음 직원에게 상환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="0cfaf-155">허용하는 각 결제 방법에 대해 다음 결정을 내려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="0cfaf-156">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-156">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-157">어떤 결제 방법이 허용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="0cfaf-158">결제 방법 경비는 누가 소유합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="0cfaf-159">상쇄 계정 유형이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-159">Is there an offset account type?</span></span> <span data-ttu-id="0cfaf-160">상쇄 계정 유형이 있는 경우 이것은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="0cfaf-161">상쇄 계정이 있는 경우 계정은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="0cfaf-162">결제 방법이 신용 카드인 경우 수입 트랜잭션에만 결제 방법을 사용해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="0cfaf-163">경비 범주 및 공유 범주</span><span class="sxs-lookup"><span data-stu-id="0cfaf-163">Expense categories and shared categories</span></span>

<span data-ttu-id="0cfaf-164">직원이 경비 보고서를 작성할 때 기록하는 각 경비는 경비 범주와 연관되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="0cfaf-165">경비 범주는 조직의 법인간에 공유할 수 있는 공유 범주에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="0cfaf-166">이러한 범주는 조직이 정의된 방식에 따라 프로젝트 관리 및 회계에서도 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="0cfaf-167">조직의 정의와 구현 팀의 지침에 따라 경비 관리에 사용되는 범주가 경비 관리에만 사용되는지 또는 프로젝트 관리와 회계 및 경비 관리 간에 공유되어야 하는지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="0cfaf-168">이러한 범주는 프로젝트와 경비 또는 프로젝트와 생산 간에 공유할 수 있지만 경비와 생산 간에는 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="0cfaf-169">각 경비 범주에 대해 다음과 같은 결정을 내려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="0cfaf-170">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-170">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-171">경비 범주란 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-171">What is the expense category?</span></span> <span data-ttu-id="0cfaf-172">예를 들어 항공편, 호텔 또는 마일리지 범주가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="0cfaf-173">경비 범주를 프로젝트 관리 및 회계에도 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="0cfaf-174">경비 유형이란 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-174">What is the expense type?</span></span>
- <span data-ttu-id="0cfaf-175">경비 범주에 대한 기본 결제 방법은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="0cfaf-176">경비 범주의 경비를 항목별로 분류해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="0cfaf-177">경비 범주에 대한 기본 계정은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="0cfaf-178">경비 범주에 대한 기본 품목 판매세 그룹은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="0cfaf-179">경비 범주에 추가 결제 방법이 허용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="0cfaf-180">추가 결제 방법이 허용되는 경우 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="0cfaf-181">이 경비 범주에 하위 범주가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="0cfaf-182">하위 범주가 있다면 다음 사항도 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0cfaf-183">세금 공제에서 제외되는 하위 범주가 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="0cfaf-184">하위 범주의 품목 판매세 그룹은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="0cfaf-185">경비 범주가 프로젝트 관리 및 회계에서도 사용되는 경우 나머지 질문에 답하십시오.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="0cfaf-186">그렇지 않으면 다음 섹션으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="0cfaf-187">다음 경비에 어떤 비용 계정이 사용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="0cfaf-188">비용</span><span class="sxs-lookup"><span data-stu-id="0cfaf-188">Cost</span></span>
    - <span data-ttu-id="0cfaf-189">급여 할당</span><span class="sxs-lookup"><span data-stu-id="0cfaf-189">Payroll allocation</span></span>
    - <span data-ttu-id="0cfaf-190">WIP-비용 값</span><span class="sxs-lookup"><span data-stu-id="0cfaf-190">WIP-cost value</span></span>
    - <span data-ttu-id="0cfaf-191">비용-항목</span><span class="sxs-lookup"><span data-stu-id="0cfaf-191">Cost-item</span></span>
    - <span data-ttu-id="0cfaf-192">WIP-비용 값-항목</span><span class="sxs-lookup"><span data-stu-id="0cfaf-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="0cfaf-193">발생 손실</span><span class="sxs-lookup"><span data-stu-id="0cfaf-193">Accrued loss</span></span>
    - <span data-ttu-id="0cfaf-194">WIP-발생 손실</span><span class="sxs-lookup"><span data-stu-id="0cfaf-194">WIP-accrued loss</span></span>

- <span data-ttu-id="0cfaf-195">다음에 대해 어떤 수익 계정이 사용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="0cfaf-196">송장 발부된 수익</span><span class="sxs-lookup"><span data-stu-id="0cfaf-196">Invoiced revenue</span></span>
    - <span data-ttu-id="0cfaf-197">미수 수익-영업 가치</span><span class="sxs-lookup"><span data-stu-id="0cfaf-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="0cfaf-198">WIP-영업 가치</span><span class="sxs-lookup"><span data-stu-id="0cfaf-198">WIP-sales value</span></span>
    - <span data-ttu-id="0cfaf-199">미수 수익-생산</span><span class="sxs-lookup"><span data-stu-id="0cfaf-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="0cfaf-200">WIP-생산</span><span class="sxs-lookup"><span data-stu-id="0cfaf-200">WIP-production</span></span>
    - <span data-ttu-id="0cfaf-201">미수 수익-이익</span><span class="sxs-lookup"><span data-stu-id="0cfaf-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="0cfaf-202">WIP-이익</span><span class="sxs-lookup"><span data-stu-id="0cfaf-202">WIP-profit</span></span>
    - <span data-ttu-id="0cfaf-203">미수 수익-구독</span><span class="sxs-lookup"><span data-stu-id="0cfaf-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="0cfaf-204">WIP-구독</span><span class="sxs-lookup"><span data-stu-id="0cfaf-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="0cfaf-205">세금</span><span class="sxs-lookup"><span data-stu-id="0cfaf-205">Taxes</span></span>

<span data-ttu-id="0cfaf-206">경비 관련 세금의 경우 경비 보고서에 포함되거나 활성화된 항목을 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="0cfaf-207">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-207">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-208">경비에 판매세가 포함되어 있습니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="0cfaf-209">경비에 대해 세금 공제를 활성화해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="0cfaf-210">총계정 원장을 계획할 때 미국 판매세 및 사용세 규칙을 적용하기로 결정한 경우 경비에 대한 세금 공제를 활성화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="0cfaf-211">(미국 판매세 및 사용세 규칙을 적용하려면 **판매세 과세 규칙 적용** 옵션을 **예** 로 설정합니다.)</span><span class="sxs-lookup"><span data-stu-id="0cfaf-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="0cfaf-212">정책</span><span class="sxs-lookup"><span data-stu-id="0cfaf-212">Policies</span></span>

<span data-ttu-id="0cfaf-213">경비 보고서 정책을 작성하면 직원이 대신 경비를 부담할 때 조직에서 시간과 경비를 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="0cfaf-214">정책은 직원이 예산을 유지하고 필요한 모든 정보를 제공하며 필요한 경우에만 돈을 지출하도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="0cfaf-215">작성하는 각 경비 보고서 정책 및 각 경비 보고서 승인 정책에 대해 다음과 같은 결정을 내려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfaf-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="0cfaf-216">**결정:**</span><span class="sxs-lookup"><span data-stu-id="0cfaf-216">**Decisions:**</span></span>

- <span data-ttu-id="0cfaf-217">정책 이름은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-217">What is the name of the policy?</span></span>
- <span data-ttu-id="0cfaf-218">무엇을 위한 경비 정책입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-218">What is the expense policy for?</span></span>
- <span data-ttu-id="0cfaf-219">이전에 회사 간 경비를 사용하기로 결정한 경우 조직의 어느 회사에 이 정책이 적용됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="0cfaf-220">정책은 언제 발효됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-220">When does the policy become effective?</span></span>
- <span data-ttu-id="0cfaf-221">정책은 언제 만료됩니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-221">When does the policy expire?</span></span>
- <span data-ttu-id="0cfaf-222">정책 규칙은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-222">What is the policy rule?</span></span>
- <span data-ttu-id="0cfaf-223">정책 규칙의 결과는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="0cfaf-223">What is the outcome of the policy rule?</span></span>
