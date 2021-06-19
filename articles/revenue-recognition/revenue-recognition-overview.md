---
title: 수익 인식 개요
description: 이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013764"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="d2ba4-103">수익 인식 개요</span><span class="sxs-lookup"><span data-stu-id="d2ba4-103">Revenue recognition overview</span></span>

<span data-ttu-id="d2ba4-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d2ba4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2ba4-105">Dynamics 365 Project Operations에서 수익 인식 원칙은 프로젝트 또는 프로젝트 일부에 대해 선택한 청구 방법에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="d2ba4-106">이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="d2ba4-107">시간 및 자재 청구 방법을 사용하여 계산된 트랜잭션</span><span class="sxs-lookup"><span data-stu-id="d2ba4-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="d2ba4-108">비용과 수익 인식이 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="d2ba4-109">트랜잭션 비용 및 미 청구 판매는 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="d2ba4-110">프로젝트 비용 및 수익 프로필은 미 청구 판매 트랜잭션이 총계정 원장에 전기되는지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="d2ba4-111">**수익 발생** 을 선택하면 전기 중에 **WIP 판매 가치** 및 **발생한 수익 판매 가치** 계정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="d2ba4-112">다음은 이 방법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d2ba4-113">거래 유형</span><span class="sxs-lookup"><span data-stu-id="d2ba4-113">Transaction type</span></span> | <span data-ttu-id="d2ba4-114">차변/대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-114">Debit/Credit</span></span> | <span data-ttu-id="d2ba4-115">수량</span><span class="sxs-lookup"><span data-stu-id="d2ba4-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d2ba4-116">WIP 판매 가치</span><span class="sxs-lookup"><span data-stu-id="d2ba4-116">WIP Sales value</span></span> | <span data-ttu-id="d2ba4-117">차변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-117">Debit</span></span> | <span data-ttu-id="d2ba4-118">100</span><span class="sxs-lookup"><span data-stu-id="d2ba4-118">100</span></span> |
  | <span data-ttu-id="d2ba4-119">발생한 수익 판매 가치</span><span class="sxs-lookup"><span data-stu-id="d2ba4-119">Accrued revenue sales value</span></span> | <span data-ttu-id="d2ba4-120">대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-120">Credit</span></span> | <span data-ttu-id="d2ba4-121">100</span><span class="sxs-lookup"><span data-stu-id="d2ba4-121">100</span></span> |

- <span data-ttu-id="d2ba4-122">송장 발행 중에 수익이 인식됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="d2ba4-123">시스템은 게시하는 동안 **청구된 수익** 계정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="d2ba4-124">다음은 이 방법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d2ba4-125">거래 유형</span><span class="sxs-lookup"><span data-stu-id="d2ba4-125">Transaction type</span></span> | <span data-ttu-id="d2ba4-126">차변/대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-126">Debit/Credit</span></span> | <span data-ttu-id="d2ba4-127">수량</span><span class="sxs-lookup"><span data-stu-id="d2ba4-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d2ba4-128">고객 잔액</span><span class="sxs-lookup"><span data-stu-id="d2ba4-128">Customer balance</span></span> | <span data-ttu-id="d2ba4-129">차변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-129">Debit</span></span> | <span data-ttu-id="d2ba4-130">120</span><span class="sxs-lookup"><span data-stu-id="d2ba4-130">120</span></span> |
  | <span data-ttu-id="d2ba4-131">판매세 납부</span><span class="sxs-lookup"><span data-stu-id="d2ba4-131">Sales tax payable</span></span> | <span data-ttu-id="d2ba4-132">대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-132">Credit</span></span> | <span data-ttu-id="d2ba4-133">20</span><span class="sxs-lookup"><span data-stu-id="d2ba4-133">20</span></span> |
  | <span data-ttu-id="d2ba4-134">송장 발부된 수익</span><span class="sxs-lookup"><span data-stu-id="d2ba4-134">Invoiced Revenue</span></span> | <span data-ttu-id="d2ba4-135">대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-135">Credit</span></span> | <span data-ttu-id="d2ba4-136">100</span><span class="sxs-lookup"><span data-stu-id="d2ba4-136">100</span></span> |

- <span data-ttu-id="d2ba4-137">미 청구 판매가 전기될 때 수익이 발생한 경우 시스템은 송장 발행시 발생한 수익을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="d2ba4-138">거래 유형</span><span class="sxs-lookup"><span data-stu-id="d2ba4-138">Transaction type</span></span> | <span data-ttu-id="d2ba4-139">차변/대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-139">Debit/Credit</span></span> | <span data-ttu-id="d2ba4-140">수량</span><span class="sxs-lookup"><span data-stu-id="d2ba4-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d2ba4-141">WIP 판매 가치</span><span class="sxs-lookup"><span data-stu-id="d2ba4-141">WIP Sales value</span></span> | <span data-ttu-id="d2ba4-142">대변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-142">Credit</span></span> | <span data-ttu-id="d2ba4-143">100</span><span class="sxs-lookup"><span data-stu-id="d2ba4-143">100</span></span> |
  | <span data-ttu-id="d2ba4-144">발생한 수익 판매 가치</span><span class="sxs-lookup"><span data-stu-id="d2ba4-144">Accrued revenue sales value</span></span> | <span data-ttu-id="d2ba4-145">차변</span><span class="sxs-lookup"><span data-stu-id="d2ba4-145">Debit</span></span> | <span data-ttu-id="d2ba4-146">100</span><span class="sxs-lookup"><span data-stu-id="d2ba4-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="d2ba4-147">고정 가격 청구 방법을 사용하여 계산된 트랜잭션</span><span class="sxs-lookup"><span data-stu-id="d2ba4-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="d2ba4-148">비용과 수익 인식은 별도입니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="d2ba4-149">트랜잭션 비용은 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="d2ba4-150">미 청구 판매 트랜잭션은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="d2ba4-151">프로젝트 비용 및 수익 프로필에 **프로젝트 완료 계산에 사용되는 원칙** 이 **WIP 없음** 으로 설정된 경우 송장 발행 중에 수익을 인식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="d2ba4-152">이 방법은 단기적이고 간단한 프로젝트에만 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="d2ba4-153">수익은 **완료된 계약** 또는 **완료율 수익 인식** 방법으로 고정 가격 수익 추정치를 사용하여 인식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2ba4-154">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="d2ba4-154">Additional resources</span></span>
[<span data-ttu-id="d2ba4-155">청구 가능한 프로젝트에 대한 회계 구성 문서</span><span class="sxs-lookup"><span data-stu-id="d2ba4-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="d2ba4-156">고정 가격 수익 프로젝트 추정</span><span class="sxs-lookup"><span data-stu-id="d2ba4-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="d2ba4-157">수익 추정치 관리</span><span class="sxs-lookup"><span data-stu-id="d2ba4-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="d2ba4-158">방법을 완료하는 데 드는 비용</span><span class="sxs-lookup"><span data-stu-id="d2ba4-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]