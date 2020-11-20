---
title: 경비 보고서 및 여러 승인자
description: 이 항목은 여러 사람의 승인이 필요한 경비 보고서에 대한 정보를 제공합니다.
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
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121001"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="bc754-103">경비 보고서 및 여러 승인자</span><span class="sxs-lookup"><span data-stu-id="bc754-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="bc754-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="bc754-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bc754-105">조직의 경비 승인 정책에 따라 두 명 이상의 사람이 제출된 경비 보고서를 승인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="bc754-106">경비 보고서 승인을 위한 워크플로 프로세스를 설정할 때 하나 이상의 경비 보고서 승인자에 대한 작업 또는 단계를 포함하는 워크플로 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="bc754-107">예를 들어, 모든 경비 보고서는 보고서를 제출한 직원의 관리자와 채무 코디네이터라는 두 명의 개별 사람이 승인하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="bc754-108">여러 경비 보고서 승인자를 요구하기로 결정한 경우 다음 방법 중 하나로 워크플로 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="bc754-109">한 단계가 있는 하나의 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-109">Add one approval element that has one step.</span></span> <span data-ttu-id="bc754-110">예를 들어 이 단계에서는 경비 보고서를 사용자 그룹에 할당하고 사용자 그룹 구성원의 50 %가 이를 승인해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="bc754-111">여러 단계가 있는 하나의 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="bc754-112">예를 들어 승인 요소에는 다음 단계가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="bc754-113">경비 보고서를 제출한 직원의 관리자가 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="bc754-114">미지급금 사무원은 영수증 및 경비 보고서 항목을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="bc754-115">예산 소유자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="bc754-116">각각 하나의 단계가 있는 여러 승인 요소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="bc754-117">예를 들어 다음 각 단계에 대해 별도의 승인 요소를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="bc754-118">직원의 관리자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="bc754-119">예산 소유자가 경비 보고서를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="bc754-119">The budget owner approves the expense report.</span></span>
