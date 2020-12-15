---
title: 수익 인식 개요
description: 이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531482"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="35194-103">수익 인식 개요</span><span class="sxs-lookup"><span data-stu-id="35194-103">Revenue recognition overview</span></span>

<span data-ttu-id="35194-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="35194-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="35194-105">Dynamics 365 Project Operations에서 수익 인식 원칙은 프로젝트 또는 프로젝트 일부에 대해 선택한 청구 방법에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="35194-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="35194-106">이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="35194-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="35194-107">시간 및 자재 청구 방법을 사용하여 계산된 트랜잭션</span><span class="sxs-lookup"><span data-stu-id="35194-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="35194-108">비용과 수익 인식이 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="35194-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="35194-109">트랜잭션 비용 및 미 청구 판매는 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="35194-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="35194-110">프로젝트 비용 및 수익 프로필은 미 청구 판매 트랜잭션이 총계정 원장에 전기되는지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="35194-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="35194-111">**수익 발생** 을 선택하면 전기 중에 **WIP 판매 가치** 및 **발생한 수익 판매 가치** 계정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="35194-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="35194-112">다음은 이 방법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="35194-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="35194-113">거래 유형</span><span class="sxs-lookup"><span data-stu-id="35194-113">Transaction type</span></span> | <span data-ttu-id="35194-114">차변/대변</span><span class="sxs-lookup"><span data-stu-id="35194-114">Debit/Credit</span></span> | <span data-ttu-id="35194-115">수량</span><span class="sxs-lookup"><span data-stu-id="35194-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35194-116">WIP 판매 가치</span><span class="sxs-lookup"><span data-stu-id="35194-116">WIP Sales value</span></span> | <span data-ttu-id="35194-117">차변</span><span class="sxs-lookup"><span data-stu-id="35194-117">Debit</span></span> | <span data-ttu-id="35194-118">100</span><span class="sxs-lookup"><span data-stu-id="35194-118">100</span></span> |
  | <span data-ttu-id="35194-119">발생한 수익 판매 가치</span><span class="sxs-lookup"><span data-stu-id="35194-119">Accrued revenue sales value</span></span> | <span data-ttu-id="35194-120">대변</span><span class="sxs-lookup"><span data-stu-id="35194-120">Credit</span></span> | <span data-ttu-id="35194-121">100</span><span class="sxs-lookup"><span data-stu-id="35194-121">100</span></span> |

- <span data-ttu-id="35194-122">송장 발행 중에 수익이 인식됩니다.</span><span class="sxs-lookup"><span data-stu-id="35194-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="35194-123">시스템은 게시하는 동안 **청구된 수익** 계정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="35194-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="35194-124">다음은 이 방법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="35194-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="35194-125">거래 유형</span><span class="sxs-lookup"><span data-stu-id="35194-125">Transaction type</span></span> | <span data-ttu-id="35194-126">차변/대변</span><span class="sxs-lookup"><span data-stu-id="35194-126">Debit/Credit</span></span> | <span data-ttu-id="35194-127">수량</span><span class="sxs-lookup"><span data-stu-id="35194-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35194-128">고객 잔액</span><span class="sxs-lookup"><span data-stu-id="35194-128">Customer balance</span></span> | <span data-ttu-id="35194-129">차변</span><span class="sxs-lookup"><span data-stu-id="35194-129">Debit</span></span> | <span data-ttu-id="35194-130">120</span><span class="sxs-lookup"><span data-stu-id="35194-130">120</span></span> |
  | <span data-ttu-id="35194-131">판매세 납부</span><span class="sxs-lookup"><span data-stu-id="35194-131">Sales tax payable</span></span> | <span data-ttu-id="35194-132">대변</span><span class="sxs-lookup"><span data-stu-id="35194-132">Credit</span></span> | <span data-ttu-id="35194-133">20</span><span class="sxs-lookup"><span data-stu-id="35194-133">20</span></span> |
  | <span data-ttu-id="35194-134">송장 발부된 수익</span><span class="sxs-lookup"><span data-stu-id="35194-134">Invoiced Revenue</span></span> | <span data-ttu-id="35194-135">대변</span><span class="sxs-lookup"><span data-stu-id="35194-135">Credit</span></span> | <span data-ttu-id="35194-136">100</span><span class="sxs-lookup"><span data-stu-id="35194-136">100</span></span> |

- <span data-ttu-id="35194-137">미 청구 판매가 전기될 때 수익이 발생한 경우 시스템은 송장 발행시 발생한 수익을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="35194-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="35194-138">거래 유형</span><span class="sxs-lookup"><span data-stu-id="35194-138">Transaction type</span></span> | <span data-ttu-id="35194-139">차변/대변</span><span class="sxs-lookup"><span data-stu-id="35194-139">Debit/Credit</span></span> | <span data-ttu-id="35194-140">수량</span><span class="sxs-lookup"><span data-stu-id="35194-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35194-141">WIP 판매 가치</span><span class="sxs-lookup"><span data-stu-id="35194-141">WIP Sales value</span></span> | <span data-ttu-id="35194-142">대변</span><span class="sxs-lookup"><span data-stu-id="35194-142">Credit</span></span> | <span data-ttu-id="35194-143">100</span><span class="sxs-lookup"><span data-stu-id="35194-143">100</span></span> |
  | <span data-ttu-id="35194-144">발생한 수익 판매 가치</span><span class="sxs-lookup"><span data-stu-id="35194-144">Accrued revenue sales value</span></span> | <span data-ttu-id="35194-145">차변</span><span class="sxs-lookup"><span data-stu-id="35194-145">Debit</span></span> | <span data-ttu-id="35194-146">100</span><span class="sxs-lookup"><span data-stu-id="35194-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="35194-147">고정 가격 청구 방법을 사용하여 계산된 트랜잭션</span><span class="sxs-lookup"><span data-stu-id="35194-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="35194-148">비용과 수익 인식은 별도입니다.</span><span class="sxs-lookup"><span data-stu-id="35194-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="35194-149">트랜잭션 비용은 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="35194-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="35194-150">미 청구 판매 트랜잭션은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35194-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="35194-151">프로젝트 비용 및 수익 프로필에 **프로젝트 완료 계산에 사용되는 원칙** 이 **WIP 없음** 으로 설정된 경우 송장 발행 중에 수익을 인식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35194-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="35194-152">이 방법은 단기적이고 간단한 프로젝트에만 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="35194-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="35194-153">수익은 **완료된 계약** 또는 **완료율 수익 인식** 방법으로 고정 가격 수익 추정치를 사용하여 인식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35194-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35194-154">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="35194-154">Additional resources</span></span>
[<span data-ttu-id="35194-155">청구 가능한 프로젝트에 대한 회계 구성 문서</span><span class="sxs-lookup"><span data-stu-id="35194-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="35194-156">고정 가격 수익 프로젝트 추정</span><span class="sxs-lookup"><span data-stu-id="35194-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="35194-157">수익 추정치 관리</span><span class="sxs-lookup"><span data-stu-id="35194-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="35194-158">방법을 완료하는 데 드는 비용</span><span class="sxs-lookup"><span data-stu-id="35194-158">Cost to complete methods</span></span>](cost-complete-methods.md)
