---
title: 경비 관리 워크플로 설정
description: 출장 및 경비 문서를 검토하고 승인하는 워크플로 프로세스를 설정할 수 있습니다.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005124"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="e5303-103">경비 관리 워크플로 설정</span><span class="sxs-lookup"><span data-stu-id="e5303-103">Set up Expense management workflows</span></span>

<span data-ttu-id="e5303-104">출장 및 경비 문서를 검토하고 승인하는 데 사용되는 워크플로 프로세스를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="e5303-105">워크플로를 정의할 수 있는 문서에는 경비 보고서, 여행 요청 및 현금 서비스 요청이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e5303-106">워크플로는 비즈니스 프로세스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-106">A workflow represents a business process.</span></span> <span data-ttu-id="e5303-107">문서가 시스템을 통과하는 방식을 정의하고 작업을 완료하거나 문서를 승인해야 하는 사람을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e5303-108">조직에서 워크플로 시스템을 사용하면 다음과 같은 몇 가지 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="e5303-109">**일관된 프로세스** - 구매 요청, 경비 보고서 등 특정 문서에 대한 승인 프로세스를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e5303-110">워크플로 시스템을 사용하면 문서를 일관되고 효율적인 방식으로 처리하고 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="e5303-111">프로세스 가시성 - 특정 워크플로 인스턴스의 상태, 기록 및 성능 메트릭을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e5303-112">이를 통해 효율성 향상을 위해 워크플로를 변경해야 하는지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="e5303-113">중앙 집중식 작업 목록 - 사용자는 중앙 집중식 작업 목록을 보고 자신에게 할당된 워크플로 작업 및 승인을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="e5303-114">**만들 수 있는 워크플로 유형**</span><span class="sxs-lookup"><span data-stu-id="e5303-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="e5303-115">다음 표에는 **경비** 에서 만들 수 있는 워크플로 유형이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="e5303-116"><strong>유형</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="e5303-117"><strong>이 유형 사용</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="e5303-118"><strong>비용 보고서</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="e5303-119">경비 보고서에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="e5303-120"><strong>경비 보고서 자동 게시</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="e5303-121">경비 보고서에 대한 자동 게시 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="e5303-122"><strong>경비 라인 항목</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="e5303-123">경비 보고서에 라인 항목에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="e5303-124"><strong>경비 라인 항목 자동 게시</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="e5303-125">경비 보고서에 라인 항목에 대한 자동 게시 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="e5303-126"><strong>여행 요청</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="e5303-127">여행 요청에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="e5303-128"><strong>현금 서비스 요청</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="e5303-129">현금 서비스 요청에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="e5303-130"><strong>VAT 세금 회수</strong></span><span class="sxs-lookup"><span data-stu-id="e5303-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="e5303-131">부가가치세(VAT) 회수를 위한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5303-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]