---
title: 경비 보고서에 대한 여러 승인자
description: 이 항목은 여러 사람의 승인이 필요한 경비 보고서에 대한 정보를 제공합니다.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271721"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="7e499-103">경비 보고서에 대한 여러 승인자</span><span class="sxs-lookup"><span data-stu-id="7e499-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="7e499-104">조직의 경비 승인 정책에 따라 두 명 이상의 사람이 직원이 제출한 경비 보고서를 승인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="7e499-105">경비 보고서 승인을 위한 워크플로 프로세스를 설정할 때 하나 이상의 경비 보고서 승인자에 대한 작업 또는 단계를 포함하는 워크플로 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="7e499-106">예를 들어, 모든 경비 보고서는 보고서를 제출한 직원의 관리자가 먼저 승인한 다음 채무 코디네이터가 승인하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="7e499-107">여러 경비 보고서 승인자를 요구하기로 결정한 경우 다음 방법 중 하나로 워크플로 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="7e499-108">한 단계가 있는 하나의 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-108">Add one approval element that has one step.</span></span> <span data-ttu-id="7e499-109">예를 들어 이 단계에서는 경비 보고서를 사용자 그룹에 할당하고 사용자 그룹 구성원의 50 %가 이를 승인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="7e499-110">여러 단계가 있는 하나의 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="7e499-111">예를 들어 승인 요소에는 다음 단계가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="7e499-112">경비 보고서를 제출한 직원의 관리자가 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="7e499-113">미지급금 사무원은 영수증 및 경비 보고서 항목을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="7e499-114">예산 소유자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="7e499-115">각각 하나의 단계가 있는 여러 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="7e499-116">예를 들어 다음 각 단계에 대해 별도의 승인 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="7e499-117">직원의 관리자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="7e499-118">예산 소유자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]