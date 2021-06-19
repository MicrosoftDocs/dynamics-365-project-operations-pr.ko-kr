---
title: 승인 집합
description: 이 항목은 승인 집합, 요청 및 해당 작업의 하위 집합에 대한 정보를 제공합니다.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116879"
---
# <a name="approval-sets"></a><span data-ttu-id="90f65-103">승인 집합</span><span class="sxs-lookup"><span data-stu-id="90f65-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90f65-104">승인 집합은 승인 요청을 더 작은 작업 하위 집합으로 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="90f65-105">이 그룹화를 사용하면 프로젝트별로 승인을 순서대로 처리할 수 있으며 재시도 및 순서 지정이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="90f65-106">그룹화는 대량 승인에 대한 승인 처리의 신뢰성과 추적성을 향상시킵니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="90f65-107">승인 집합은 관련 레코드의 전체 처리 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="90f65-108">승인 집합을 사용하여 승인 레코드를 처리하면 레코드가 **제출됨** 에서 **승인됨** 으로 이동하며 승인 집합에서 연결 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="90f65-109">승인을 위해 제출할 때 레코드가 실패하면 레코드는 **제출됨** 상태로 유지되고 승인 집합은 실패로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="90f65-110">승인 집합은 실패 오류 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="90f65-111">승인 및 승인 집합 처리</span><span class="sxs-lookup"><span data-stu-id="90f65-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="90f65-112">처리 대기 중인 승인은 **승인 처리 중** 보기에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="90f65-113">시스템은 이전 시도가 실패한 경우 승인 재시도를 포함하여 모든 항목을 비동기적으로 여러 번 처리하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="90f65-114">**승인 집합 수명** 필드는 실패로 표시되기 전에 집합을 처리하기 위해 남은 시도 횟수를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="90f65-115">실패한 승인 및 승인 집합</span><span class="sxs-lookup"><span data-stu-id="90f65-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="90f65-116">**실패한 승인** 보기는 사용자 개입이 필요한 모든 승인을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="90f65-117">연관된 승인 집합 로그를 열어 실패 원인을 식별하십시오.</span><span class="sxs-lookup"><span data-stu-id="90f65-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="90f65-118">**재시도** 를 선택하면 승인 집합 수명 수가 추가되고 승인 집합이 다시 **처리 중** 상태로 이동하며 나머지 레코드 처리를 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="90f65-119">승인 집합 구성</span><span class="sxs-lookup"><span data-stu-id="90f65-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="90f65-120">승인 집합 기능 활성화</span><span class="sxs-lookup"><span data-stu-id="90f65-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="90f65-121">승인 집합 기능을 활성화하기 전에 현재 처리 중인 승인이 없는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="90f65-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="90f65-122">**프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 활성화** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="90f65-123">승인 집합 기능 끄기</span><span class="sxs-lookup"><span data-stu-id="90f65-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="90f65-124">승인 집합 기능을 끄기 전에 현재 처리 중인 승인이 없는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="90f65-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="90f65-125">**프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 비활성화** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="90f65-126">비동기 임계값 구성</span><span class="sxs-lookup"><span data-stu-id="90f65-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="90f65-127">승인 집합이 생성될 때 승인을 위해 선택한 레코드 수가 표시된 임계값을 초과하면 처리가 백그라운드로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="90f65-128">**비동기 임계값** 필드를 사용하여 승인 처리를 동기 또는 비동기적으로 실행해야 하는 시기를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="90f65-129">유효한 값:</span><span class="sxs-lookup"><span data-stu-id="90f65-129">Valid values are:</span></span>

  - <span data-ttu-id="90f65-130">0: 모든 요청이 비동기적으로 처리되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="90f65-131">0보다 큰 숫자: 제출된 승인 수가 이 값을 초과하는 경우에만 승인이 비동기적으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f65-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
