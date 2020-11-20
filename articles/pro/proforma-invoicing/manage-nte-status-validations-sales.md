---
title: 초과하지 않는 상태 및 유효성 검사 관리
description: 이 항목은 Project Operations에서 수행되는 초과 제한 검사에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130001"
---
# <a name="manage-not-to-exceed-status-and-validations"></a><span data-ttu-id="9b9e0-103">초과하지 않는 상태 및 유효성 검사 관리</span><span class="sxs-lookup"><span data-stu-id="9b9e0-103">Manage not-to-exceed status and validations</span></span> 

<span data-ttu-id="9b9e0-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="9b9e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="not-to-exceed-on-approvals"></a><span data-ttu-id="9b9e0-105">승인 시 초과 안 함</span><span class="sxs-lookup"><span data-stu-id="9b9e0-105">Not-to-exceed on approvals</span></span>

<span data-ttu-id="9b9e0-106">시간 또는 경비 입력이 제출되면 승인 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-106">When a time or expense entry is submitted, an approval record is created.</span></span> <span data-ttu-id="9b9e0-107">승인이 청구 가능하고 시간 및 재료 계약 내용에 매핑되는 경우 시스템은 다음 수준에서 초과 안 함 유효성 검사를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-107">If the approval is chargeable and maps to a time and material contract line, the system completes a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="9b9e0-108">프로젝트 계약 내용에서 고객에 대해 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-108">Check against the limit set up for the customer on the project contract line</span></span>
  - <span data-ttu-id="9b9e0-109">계약 내용에서 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-109">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="9b9e0-110">고객에 대해 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-110">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="9b9e0-111">계약에서 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-111">Check against the limit set up on the contract</span></span>

<span data-ttu-id="9b9e0-112">각 수준의 확인에는 이미 기록된 청구 백로그 금액과 해당 수준에서 현재까지 청구된 금액을 고려한 후 이 승인의 판매 금액이 해당 수준에서 초과하지 않는 한도를 위반하지 않는지 확인하는 것이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-112">The checks at each level involve ensuring that the amount of sales value on this approval will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="9b9e0-113">확인을 통과하면 승인에 **성공** 의 유효성 검사 상태가 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-113">If the check passes, the approval is given a validation status of **Success**.</span></span>

<span data-ttu-id="9b9e0-114">확인을 실패하면 승인에 **실패** 의 유효성 검사 상태가 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-114">If the check fails, the approval is given a validation status of **Failed**.</span></span> <span data-ttu-id="9b9e0-115">초과 안 함 유효성 검사 세부 정보는 유효성 검사가 실패한 수준을 사용자에게 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-115">The not-to-exceed validation detail will inform the user at which level the validation failed.</span></span>

<span data-ttu-id="9b9e0-116">제출된 시간 또는 비용 입력이 청구 불가능한 것으로 간주되면 초과하지 않는 유효성 검증 상태는 유효성 검사 세부 정보가 **해당 없음** 과 동일한 **해당 없음** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-116">When the submitted time or expense entry is considered non-chargeable, the not-to-exceed validation status is set to **Not Applicable** with the validation detail equal to **Not applicable**.</span></span>

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a><span data-ttu-id="9b9e0-117">미청구 판매 실적에서 초과 안 함</span><span class="sxs-lookup"><span data-stu-id="9b9e0-117">Not-to-exceed on unbilled sales actuals</span></span>

<span data-ttu-id="9b9e0-118">시간 또는 경비 입력이 승인되면 비용 및 미청구 판매 실적 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-118">When a time or expense entry is approved, cost and unbilled sales actuals records are created.</span></span> <span data-ttu-id="9b9e0-119">생성 중인 미청구 실제 판매가 청구 가능하고 시간 및 재료 계약 내용에 매핑되는 경우 애플리케이션은 다음 수준에서 초과 안 함 유효성 검사를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-119">If the unbilled sales actual being created is chargeable and maps to a time and material contract line, the application performs a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="9b9e0-120">프로젝트 계약 내용에서 고객에 대해 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-120">Check against the limit set up for the customer of the project contract line</span></span>
  - <span data-ttu-id="9b9e0-121">계약 내용에서 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-121">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="9b9e0-122">고객에 대해 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-122">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="9b9e0-123">계약에서 설정된 한도 확인</span><span class="sxs-lookup"><span data-stu-id="9b9e0-123">Check against the limit set up on the contract</span></span>

<span data-ttu-id="9b9e0-124">각 수준의 확인에는 이미 기록된 청구 백로그 금액과 해당 수준에서 현재까지 청구된 금액을 고려한 후 실제의 판매 금액이 해당 수준에서 초과하지 않는 한도를 위반하지 않는지 확인하는 것이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-124">The checks at each level ensure that the amount of sales value on the actual will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="9b9e0-125">확인이 통과하면 미청구 실제 판매에는 **커밋됨** 의 초과 안 함 상태가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-125">If the check passes, the unbilled sales actual is given a not-to-exceed status of **Committed**.</span></span>

<span data-ttu-id="9b9e0-126">확인이 실패하면 미청구 실제 판매에는 **실패** 의 초과 안 함 상태가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-126">If the check fails, the unbilled sales actual is given a not-to-exceed status of **Failed**.</span></span> <span data-ttu-id="9b9e0-127">유효성 검사 세부 정보는 유효성 검사가 실패한 수준을 사용자에게 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-127">The validation detail informs the user at which level the validation failed.</span></span>

<span data-ttu-id="9b9e0-128">미청구 실제 판매가 청구 불가능 또는 무료로 간주되는 경우, 네 가지 수준 중 하나에서 초과하지 않는 한도 설정이 없거나 생성 중인 실제가 비용, 보유자, 리소스 조달 단위 또는 조직 간 판매인 경우, **초과 안 함 상태** 와 **초과 안 함 유효성 검사 세부 정보** 필드는 **해당 없음** 으로 설정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-128">When the unbilled sales actual is considered non-chargeable or complimentary, if there is no not-to-exceed limit setup at any of the four levels, or if the actual being created is Cost, Retainer, Resourcing Unit, or Inter-organization Sales, the **Not-to-Exceed Status** and **Not-to-Exceed Validation Detail** fields must be set to **Not Applicable**.</span></span>

## <a name="reset-the-not-to-exceed-status"></a><span data-ttu-id="9b9e0-129">초과 안 함 상태 다시 설정</span><span class="sxs-lookup"><span data-stu-id="9b9e0-129">Reset the not-to-exceed status</span></span>

<span data-ttu-id="9b9e0-130">초과 안 함 상태의 대량 다시 설정을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-130">You can perform a bulk reset of the not-to-exceed status.</span></span> <span data-ttu-id="9b9e0-131">이를 통해 프로젝트 관리자는 사용 가능한 초과 안 함 금액에서 이미 약정된 다른 작업, 시간 또는 경비의 특정 작업, 시간 또는 경비에 대한 송장의 우선 순위를 지정하기 위해 초과 안 함 유효성 검사를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-131">This allows Project managers to adjust not-to-exceed validation to prioritize invoicing of one particular body of work, time, or expenses over others that are already committed from the available not-to-exceed amount.</span></span>

<span data-ttu-id="9b9e0-132">미청구 판매 실적에서 초과 안 함 상태가 다시 설정되면 약정 금액이 감소합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-132">After the not-to-exceed status is reset on unbilled sales actuals, the committed amount is reduced.</span></span> <span data-ttu-id="9b9e0-133">프로젝트 관리자는 이전에 초과 안 함 유효성 검사에 실패한 다른 작업, 시간 또는 경비를 선택하고 재평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-133">The Project manager can select another body of work, time, or expenses that previously failed the not-to-exceed validation and reevaluate them.</span></span> <span data-ttu-id="9b9e0-134">커밋된 금액이 감소하면 이러한 실제 값이 이제 유효성 검사를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-134">With the reduction in the committed amount, these actuals will now pass the validation.</span></span> <span data-ttu-id="9b9e0-135">이를 통해 프로젝트 관리자는 해당 기간 동안 청구 가능한 트랜잭션에 대해 더 큰 영향력을 행사하고 통제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-135">This helps the Project manager exert greater influence and control over the invoiceable transactions for that period.</span></span>

<span data-ttu-id="9b9e0-136">초과 안 함 상태를 다시 설정하려면 **시간 및 재료 청구 백로그** 또는 **실제** 보기에서 하나 이상의 실제 값을 선택한 다음 **초과 안 함 상태 다시 설정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-136">To reset the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and then select **Reset Not-to-Exceed Status**.</span></span>

<span data-ttu-id="9b9e0-137">초과 안 함 상태는 선택한 모든 실제 항목에 대해 **평가되지 않음** 으로 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-137">The not-to-exceed status is reset to **Not Evaluated** on all of the relevant selected actuals.</span></span> <span data-ttu-id="9b9e0-138">초과 안 함 상태가 다시 설정된 실제는 초안 송장이 아니라 아직 송장이 발행되지 않은 미청구 판매 실제이며 청구 가능으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-138">Actuals that have their not-to-exceed status reset are unbilled sales actuals that aren't already invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="9b9e0-139">다른 선택된 실제 값은 모두 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-139">Any other selected actuals are ignored.</span></span>

## <a name="reevaluate-not-to-exceed-status"></a><span data-ttu-id="9b9e0-140">초과 안 함 상태 다시 평가</span><span class="sxs-lookup"><span data-stu-id="9b9e0-140">Reevaluate not-to-exceed status</span></span>

<span data-ttu-id="9b9e0-141">초과 안 함 상태의 대량 다시 평가를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-141">You can perform a bulk re-evaluation of the not-to-exceed status.</span></span> <span data-ttu-id="9b9e0-142">초과 안 함 상태의 다시 평가는 다음과 같은 경우에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-142">Re-evaluation of the not-to-exceed status is useful when:</span></span>

  - <span data-ttu-id="9b9e0-143">고객과 초과 안 함 한도에 대한 재협상이 있었고 실제 값을 다시 평가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-143">There was a renegotiation of not-to-exceed limits with the customer and actuals will need to be reevaluated.</span></span>
  - <span data-ttu-id="9b9e0-144">프로젝트 관리자가 한 작업의 우선 순위를 다른 작업보다 우선하여 미청구 판매 백로그의 송장 발행을 미세 조정하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-144">The Project manager wants to fine-tune the invoicing of unbilled sales backlog by prioritizing one body of work over another.</span></span>

<span data-ttu-id="9b9e0-145">초과 안 함 상태를 다시 평가하려면 **시간 및 재료 청구 백로그** 또는 **실제** 보기에서 하나 이상의 실제 값을 선택한 다음 **초과 안 함 상태 다시 평가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-145">To reevaluate the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and select **Reevaluate Not-to-Exceed Status**.</span></span>

<span data-ttu-id="9b9e0-146">초과 안 함 한도가 있는 모든 관련 선택된 실제는 초과 안 함 한도 설정에 대해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-146">All of the relevant selected actuals with a not-to-exceed limit will be evaluated against the not-to-exceed limit setup.</span></span> <span data-ttu-id="9b9e0-147">초과 안 함 상태의 다시 평가와 관련된 실제는 초안 송장이 아니라 송장이 발행되지 않은 미청구 판매 실제이며 청구 가능으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-147">Actuals that are relevant for re-evaluating the not-to-exceed status are unbilled sales actuals that are not invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="9b9e0-148">다른 선택 실제 항목이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b9e0-148">Any other select actuals selected.</span></span>
