---
title: 경비 관리를 위한 워크플로 설정
description: 출장 및 경비 문서를 검토하고 승인하는 데 사용되는 워크플로 프로세스를 설정할 수 있습니다.
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
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127706"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="e0acb-103">경비 관리를 위한 워크플로 설정</span><span class="sxs-lookup"><span data-stu-id="e0acb-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="e0acb-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e0acb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e0acb-105">출장 및 경비 문서를 검토하고 승인하는 워크플로 프로세스를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="e0acb-106">경비 보고서, 출장 요청 및 현금 서비스 요청에 대한 워크플로를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e0acb-107">워크플로는 비즈니스 프로세스를 나타내며 문서가 시스템을 통과하는 방식을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="e0acb-108">워크플로는 또한 작업을 완료하거나 문서를 승인해야 하는 사람을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e0acb-109">조직에서 워크플로 시스템을 사용하면 다음과 같은 몇 가지 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="e0acb-110">**일관된 프로세스**: 구매 요청, 경비 보고서 등 특정 문서에 대한 승인 프로세스를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e0acb-111">워크플로 시스템을 사용하면 문서를 일관되고 효율적인 방식으로 처리하고 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="e0acb-112">**프로세스 가시성**: 특정 워크플로 인스턴스의 상태, 기록 및 성능 메트릭을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e0acb-113">이를 통해 효율성 향상을 위해 워크플로를 변경해야 하는지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="e0acb-114">**중앙 집중식 작업 목록**: 사용자는 중앙 집중식 작업 목록을 보고 자신에게 할당된 워크플로 작업 및 승인을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="e0acb-115">워크플로 유형</span><span class="sxs-lookup"><span data-stu-id="e0acb-115">Workflow types</span></span>

<span data-ttu-id="e0acb-116">다음 표에는 **경비 관리** 에서 만들 수 있는 워크플로 유형이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="e0acb-117"><strong>유형</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="e0acb-118"><strong>이 유형 사용</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="e0acb-119"><strong>경비 보고서 자동 승인</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="e0acb-120">경비 보고서에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="e0acb-121"><strong>경비 보고서 자동 게시</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="e0acb-122">경비 보고서에 대한 자동 게시 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="e0acb-123"><strong>경비 라인 항목</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="e0acb-124">경비 보고서에 라인 항목에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="e0acb-125"><strong>경비 라인 항목 자동 게시</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="e0acb-126">경비 보고서에 라인 항목에 대한 자동 게시 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="e0acb-127"><strong>여행 요청</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="e0acb-128">여행 요청에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="e0acb-129"><strong>현금 서비스 요청</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="e0acb-130">현금 서비스 요청에 대한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="e0acb-131"><strong>VAT 세금 회수</strong></span><span class="sxs-lookup"><span data-stu-id="e0acb-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="e0acb-132">부가가치세(VAT) 회수를 위한 승인 워크플로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0acb-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
