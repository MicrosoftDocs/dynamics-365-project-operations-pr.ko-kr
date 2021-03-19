---
title: 경비 정책 정의
description: 작업자가 경비 보고서 및 출장 요청을 입력하고 제출할 때 따라야 하는 경비 정책을 정의할 수 있습니다.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276086"
---
# <a name="define-expense-policies"></a><span data-ttu-id="25149-103">경비 정책 정의</span><span class="sxs-lookup"><span data-stu-id="25149-103">Define expense policies</span></span>

<span data-ttu-id="25149-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="25149-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25149-105">작업자가 경비 보고서 및 출장 요청을 입력하고 제출할 때 따라야 하는 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="25149-106">경비 정책을 구현하면 경비를 효과적으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="25149-107">예를 들어 1박당 비용이 USD 250을 초과할 수 없음을 나타내는 뉴욕시의 호텔 경비에 대한 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="25149-108">작업자가 객실 요금이 이 금액을 초과하는 경비 보고서 또는 출장 요청을 제출하면 시스템은</span><span class="sxs-lookup"><span data-stu-id="25149-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="25149-109">경비에 대한 정책 금액이 초과되었음을 작업자에게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="25149-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="25149-110">정책을 정의할 때 작업자가 받을 메시지를 구성할 수</span><span class="sxs-lookup"><span data-stu-id="25149-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="25149-111">있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-111">define the policy.</span></span>      
        
<span data-ttu-id="25149-112">다음 세 가지 유형의 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="25149-113">**경고**: 작업자가 경비 보고서 또는 출장 요청서를 제출할 수 있지만 경비는 모든 승인자와 나중에 보고할 수 있도록</span><span class="sxs-lookup"><span data-stu-id="25149-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="25149-114">표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25149-114">for later reporting.</span></span>        

- <span data-ttu-id="25149-115">**오류**: 경비 보고서 또는 출장 요청서를 제출하기 전에 근로자가 정책을 준수하기 위해 경비를 수정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25149-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="25149-116">**정당화**: 경비 보고서 또는 출장 요청서를 제출하기 전에 작업자 또는 관리자가 정책 금액 초과에 대한 사유를 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25149-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="25149-117">정책 팁</span><span class="sxs-lookup"><span data-stu-id="25149-117">Policy tips</span></span>
<span data-ttu-id="25149-118">다음은 경비 관리를 위한 새 정책을 만들 때 도움이 될 수 있는 몇 가지 제안 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="25149-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="25149-119">정책은 유효 날짜이므로 경비가 발생한 날짜 이후의 날짜로 정책을 생성하면 정책이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="25149-120">예를 들어, $50의 최대 식사 비용을 적용하기 위해 오늘 새 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25149-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="25149-121">어제 입력된 기존 경비는 이 정책에서 확인되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="25149-122">항목별로 분류할 수 있는 경비 범주에 대한 정책을 생성할 때 경비 항목 유형에 대한 조건을 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="25149-123">영수증 요구와 같은 일부 정책은 항목별 라인에 적합하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="25149-124">이 상황에서 정책은 헤더 행 또는 항목화되지 않은 행에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="25149-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="25149-125">경비 관리 정책은 기본적으로 소스 엔터티에 대해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="25149-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="25149-126">내부 거래 시나리오의 경우 대신 대상 엔터티(차용 엔터티)에 대해 평가되도록 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="25149-127">대상 엔터티에 대해 정책을 실행하려면 **기능 관리** 작업 영역의 **차입 법인에 대한 경비 정책 평가** 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="25149-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="25149-128">정책 평가 시기</span><span class="sxs-lookup"><span data-stu-id="25149-128">When to evaluate policies</span></span>

<span data-ttu-id="25149-129">경비 관리 매개 변수에서 라인이 저장되거나 경비 보고서가 실행될 때 경비 관리 정책을 평가하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="25149-130">라인이 저장되는 시기를 평가하도록 선택하면 사용자는 경비 보고서를 한 번에 완료하기 위해 수행해야 하는 작업을 미리 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="25149-131">그렇지 않으면 워크플로에 제출하는 동안 마지막에 유효성을 검사하여 정책 평가를 지연하고 시간을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25149-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]