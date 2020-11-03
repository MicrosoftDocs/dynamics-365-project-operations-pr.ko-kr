---
title: 경비 관리 워크플로
description: 이 항목은 경비 관리에서 경비 보고서에 대한 검토 프로세스를 설정하기 위해 Microsoft Dynamics 365 Finance에서 워크플로 시스템을 사용하는 방법을 설명합니다.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080207"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="eca1a-103">경비 관리 워크플로</span><span class="sxs-lookup"><span data-stu-id="eca1a-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eca1a-104">경비 관리에서 경비 보고서에 대한 검토 프로세스를 설정하기 위해 워크플로 시스템을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="eca1a-105">다음 기준을 사용하여 경비 보고서를 승인하는 사람을 결정하는 워크플로를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="eca1a-106">직원 보고 계층 및 사전 정의된 승인 한도</span><span class="sxs-lookup"><span data-stu-id="eca1a-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="eca1a-107">중간 승인자와 최종 승인자를 지원하는 다단계 승인</span><span class="sxs-lookup"><span data-stu-id="eca1a-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="eca1a-108">재무 차원 및 프로젝트 책임</span><span class="sxs-lookup"><span data-stu-id="eca1a-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="eca1a-109">특정 사용자 또는 사용자 그룹에 할당</span><span class="sxs-lookup"><span data-stu-id="eca1a-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="eca1a-110">경비 보고서, 출장 요청, 현금 서비스 및 부가가치세(VAT) 공제를 위해 워크플로 승인을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="eca1a-111">**예제**</span><span class="sxs-lookup"><span data-stu-id="eca1a-111">**Example**</span></span>

<span data-ttu-id="eca1a-112">다음 프로세스는 경비 보고서에 대한 경비 관리 워크플로의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="eca1a-113">직원이 경비 보고서를 작성하고 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="eca1a-114">직원이 승인을 위해 경비 보고서를 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="eca1a-115">승인자는 워크플로가 설정될 때 정의된 규칙에 따라 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="eca1a-116">승인자는 경비 보고서를 승인할 준비가 되었다는 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="eca1a-117">승인자는 경비 보고서를 검토하고 다음 조건이 충족되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="eca1a-118">경비는 경비 정책을 위반하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="eca1a-119">경비가 정책을 위반하는 경우 승인자는 경비 보고서에 유효한 비즈니스 근거가 포함되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="eca1a-120">전자 영수증은 경비 보고서에 첨부됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="eca1a-121">승인자는 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="eca1a-122">경비 보고서는 전기를 위해 채무 코디네이터에게 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="eca1a-123">자동 전기 구성 여부에 따라 다음 단계 중 하나가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="eca1a-124">자동 전기가 구성된 경우 경비 보고서가 결제를 위해 처리되고 경비 보고서의 상태가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="eca1a-125">자동 전기가 구성되지 않은 경우 미지급금 코디네이터는 모든 원본 영수증이 제출되었고 영수증이 경비 보고서의 경비와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="eca1a-126">경비 보고서에 입력된 모든 세금 코드도 올바른지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="eca1a-127">이러한 요구 사항이 확인되면 경비 보고서가 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="eca1a-128">경비 보고서가 전기된 후 경비 보고서에 대한 지불이 승인되고 직원이 상환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca1a-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
