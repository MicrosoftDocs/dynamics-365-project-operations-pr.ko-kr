---
title: 계약에 대한 임시 선불금 생성
description: 이 항목은 필요에 따라 계약에 대한 선불금을 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51e3b0ac8e111be70fe6ad0f9c162dfaec3339ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003504"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="e3a5c-103">계약에 대한 임시 선불금 생성</span><span class="sxs-lookup"><span data-stu-id="e3a5c-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="e3a5c-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e3a5c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3a5c-105">Microsoft Dynamics 365 Project Operations는 선결제 및 선불금을 포함하는 송장 발행 시나리오를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="e3a5c-106">**Project Operations** 에서 **선불금** 을 사용하는 과정은 **보유자** 계약과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="e3a5c-107">고객에게 선불금을 청구하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="e3a5c-108">**프로젝트 계약** 페이지로 이동한 다음 **선불금 및 보유자** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="e3a5c-109">이전에 기록된 모든 선불금 및 선결제를 나열하는 하위 표에서 **+ 새 프로젝트 계약 보유자** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="e3a5c-110">선결제 또는 선불금 기록을 위한 **빨리 만들기** 양식이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="e3a5c-111">아래 표에는 선불금 기록을 위한 필드와 새 선불금을 만들 때 염두에 두어야 할 고려 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="e3a5c-112">필드</span><span class="sxs-lookup"><span data-stu-id="e3a5c-112">Field</span></span> | <span data-ttu-id="e3a5c-113">설명</span><span class="sxs-lookup"><span data-stu-id="e3a5c-113">Description</span></span> | <span data-ttu-id="e3a5c-114">다운스트림 영향</span><span class="sxs-lookup"><span data-stu-id="e3a5c-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="e3a5c-115">**프로젝트 계약 고객**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-115">**Project Contract Customer**</span></span> | <span data-ttu-id="e3a5c-116">이 필드는 이 선불금에 대해 송장을 발행할 계약의 고객을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="e3a5c-117">계약에 여러 고객이 있고 각 고객에게 특정 보유자 또는 선불금에 대해 송장을 발행하려는 경우 각 고객에 대해 개별적으로 선불금을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="e3a5c-118">**설명**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-118">**Description**</span></span> | <span data-ttu-id="e3a5c-119">이 선불금을 식별하는 데 도움이 되는 선불금의 목적 또는 시기에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="e3a5c-120">이 설명은 이 선불금에 대한 송장 라인에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="e3a5c-121">**금액**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-121">**Amount**</span></span> | <span data-ttu-id="e3a5c-122">선결제 또는 선불금 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="e3a5c-123">이 금액은 이 선불금에 대한 송장 라인에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="e3a5c-124">**송장 날짜**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-124">**Invoice Date**</span></span> | <span data-ttu-id="e3a5c-125">이 선불금이 고객에게 청구되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="e3a5c-126">이것은 선불금에 대한 송장 라인을 생성하기 위한 자동 송장 생성 프로세스의 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="e3a5c-127">**송장 상태**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-127">**Invoice Status**</span></span> | <span data-ttu-id="e3a5c-128">이 선불금이 이 고객에 대한 초안 송장에 추가되는지 여부를 나타내는 옵션 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="e3a5c-129">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-129">The possible values are:</span></span></br><span data-ttu-id="e3a5c-130">- **송장 발부 준비 안 됨**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="e3a5c-131">- **송장 발부 준비 완료**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-131">- **Ready to invoice**</span></span> | <span data-ttu-id="e3a5c-132">선결제 또는 선불금이 **송장 발부 준비 완료** 로 표시된 경우 송장 초안에 항목 시간으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="e3a5c-133">다음 송장 기간 동안 프로젝트 원가를 조정하는 데 완전히 송장이 발행 된 선불금만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="e3a5c-134">빨리 만들기 대화 상자에서 **저장 후 닫기** 를 선택하여 선불금 또는 선결제를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]