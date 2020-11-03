---
title: 여행 요청
description: 이 항목은 여행 요청에 대한 정보를 제공합니다.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079921"
---
# <a name="travel-requisitions"></a><span data-ttu-id="cc099-103">여행 요청</span><span class="sxs-lookup"><span data-stu-id="cc099-103">Travel requisitions</span></span>

<span data-ttu-id="cc099-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="cc099-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc099-105">여행 요청은 여행 목적으로 발생할 경비를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="cc099-106">검토를 위해 여행 요청을 제출하고 경비를 승인하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="cc099-107">조직에 청구되는 경비가 발생하기 전에 여행 요청을 제출해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="cc099-108">이 요구 사항은 회사 신용 카드로 경비를 청구하든, 현금 서비스로 받은 현금을 사용하든, 조직에서 상환할 본인 부담 비용이 발생하든 관계없이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="cc099-109">여행 요청 및 정책을 사용하여 조직 지출을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="cc099-110">예를 들어 조직에서 출장이 필요한 고정 가격 프로젝트를 진행하는 경우 프로젝트 팀 구성원의 출장 경비가 프로젝트 예산에 맞아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="cc099-111">출장 경비가 발생하기 전에 승인되도록 요청함으로써 조직은 프로젝트가 예산 내에서 유지되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="cc099-112">구성</span><span class="sxs-lookup"><span data-stu-id="cc099-112">Configuration</span></span> 

<span data-ttu-id="cc099-113">경비 관리 매개 변수에서 "여행 사전 승인은 필수" 매개 변수를 활성화하여 여행 요청을 "필수"로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="cc099-114">여행 요청 작성 및 제출</span><span class="sxs-lookup"><span data-stu-id="cc099-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="cc099-115">**내 경비: 여행 요청** 으로 이동하고 **새로운 여행 요청** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="cc099-116">요청의 목적과 목적지를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="cc099-117">**여행 설명** 필드에 추가 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="cc099-118">비행, 식사 또는 렌터카와 같은 예상 경비 각각에 대해 경비 라인 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="cc099-119">각 경비의 예상 날짜, 예상 금액 및 통화를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="cc099-120">예상 경비 추가를 마쳤으면 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="cc099-121">여행 요청을 제출할 준비가되면 **워크플로** > **제출** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="cc099-122">승인된 여행 요청은 **내 경비: 여행 요청** 에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="cc099-123">사용 가능한 여행 요청 보기</span><span class="sxs-lookup"><span data-stu-id="cc099-123">View available travel requisitions</span></span>

<span data-ttu-id="cc099-124">모든 여행 요청은 **내 경비: 여행 요청** 에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="cc099-125">여행 요청 승인</span><span class="sxs-lookup"><span data-stu-id="cc099-125">Approve travel requisitions</span></span>

<span data-ttu-id="cc099-126">승인할 여행 요청을 선택한 다음 **워크플로** > **승인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="cc099-127">승인된 여행 요청을 사용하여 경비 보고서를 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="cc099-128">새 경비 보고서를 작성하고 경비 보고서 헤더에서 승인된 여행 요청 목록에서 **여행 요청에 매핑** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="cc099-129">**여행 요청 금액** 필드는 경비 보고서 헤더에서 자동으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="cc099-130">여행에 발생한 각 경비를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="cc099-131">**사전 승인** 필드가 활성화되면 조정된 금액과 특정 경비 범주에 대한 승인된 금액이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="cc099-132">경비 보고서를 승인된 여행 요청에 매핑할 때 트랜잭션 금액은 승인된 금액보다 클 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cc099-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
