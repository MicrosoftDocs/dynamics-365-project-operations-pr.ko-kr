---
title: 경비 항목(라이트)
description: 이 항목은 라이트 배포에서 경비 항목 작업 방법에 대한 정보를 제공합니다.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276761"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="a65dc-103">경비 항목(라이트)</span><span class="sxs-lookup"><span data-stu-id="a65dc-103">Expense entry (lite)</span></span>

<span data-ttu-id="a65dc-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="a65dc-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a65dc-105">기본 또는 라이트 경비 관리는 간단한 경비를 기록하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="a65dc-106">프로젝트에 대한 경비를 기록할 수 있으며 프로젝트 승인자가 이를 검토하고 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="a65dc-107">Dynamics 365 Project Operations에서 경비 기능에 대한 자세한 내용은[경비 개요](expense-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a65dc-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="a65dc-108">기본 경비 캡처</span><span class="sxs-lookup"><span data-stu-id="a65dc-108">Capture a basic expense</span></span>

<span data-ttu-id="a65dc-109">승인자에게 제출할 수 있도록 경비를 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="a65dc-110">**경비** 로 이동하고 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="a65dc-111">**새 경비** 페이지에서 필요한 경비 정보를 입력하고 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="a65dc-112">기본 경비 제출</span><span class="sxs-lookup"><span data-stu-id="a65dc-112">Submit a basic expense</span></span>

<span data-ttu-id="a65dc-113">모든 경비 수집을 완료하고 승인을 받을 준비가 되었으면 이를 제출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="a65dc-114">**경비** 로 이동하고 경비를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="a65dc-115">또는 헤더의 확인란을 사용하여 모든 경비를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="a65dc-116">**제출** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-116">Select **Submit**.</span></span> <span data-ttu-id="a65dc-117">시스템은 선택한 항목을 처리한 다음 경비 승인 요청을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="a65dc-118">첨부 파일 추가</span><span class="sxs-lookup"><span data-stu-id="a65dc-118">Add an attachment</span></span>

<span data-ttu-id="a65dc-119">승인자에게 경비에 대한 추가 문서를 제공해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="a65dc-120">경비 항목의 타임라인에 영수증을 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="a65dc-121">**편집** 을 선택하고 **타임라인** 섹션을 선택한 다음 종이 클립 아이콘을 선택하여 영수증을 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="a65dc-122">기본 경비 회수</span><span class="sxs-lookup"><span data-stu-id="a65dc-122">Recall a basic expense</span></span>

<span data-ttu-id="a65dc-123">실수로 경비를 제출하면 회수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="a65dc-124">경비 항목을 회수하는 데 필요한 시간은 승인 스테이지에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="a65dc-125">승인자가 아직 항목을 승인하지 않은 경우 즉시 회수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="a65dc-126">그러나 입력이 이미 승인된 경우 승인자는 회수를 승인하고 트랜잭션을 취소하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="a65dc-127">**경비** 로 이동한 다음 경비 목록에서 회수할 경비를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="a65dc-128">**철회** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-128">Select **Recall**.</span></span> <span data-ttu-id="a65dc-129">경비 입력이 아직 승인되지 않은 경우 시스템은 즉시 이를 회수합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="a65dc-130">경비 항목이 이미 승인된 경우 승인자에게 경비를 취소할 것임을 알리는 회수 요청이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="a65dc-131">그런 다음 승인자는 취소를 수행할 수 있는지 확인하고 항목이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="a65dc-132">기본 경비 삭제</span><span class="sxs-lookup"><span data-stu-id="a65dc-132">Delete a basic expense</span></span>

<span data-ttu-id="a65dc-133">아직 제출되지 않은 경비는 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="a65dc-134">이미 제출된 경비를 삭제하려면 먼저 회수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dc-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a65dc-135">참조</span><span class="sxs-lookup"><span data-stu-id="a65dc-135">See also</span></span>

- [<span data-ttu-id="a65dc-136">승인 개요</span><span class="sxs-lookup"><span data-stu-id="a65dc-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]