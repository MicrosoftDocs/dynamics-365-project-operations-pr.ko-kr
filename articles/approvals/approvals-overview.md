---
title: 승인 개요
description: 이 항목은 Project Operations에서 승인 작업에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852507"
---
# <a name="approvals-overview"></a><span data-ttu-id="6f0a8-103">승인 개요</span><span class="sxs-lookup"><span data-stu-id="6f0a8-103">Approvals overview</span></span>

<span data-ttu-id="6f0a8-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="6f0a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6f0a8-105">시간, 경비 및 재료 사용 제출은 승인 워크플로를 통해 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="6f0a8-106">입력이 승인되면 트랜잭션이 실제로 기록되거나 일정에 시간이 예약됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="6f0a8-107">승인 워크플로</span><span class="sxs-lookup"><span data-stu-id="6f0a8-107">Approvals workflow</span></span>
<span data-ttu-id="6f0a8-108">시간, 경비 또는 재료 사용 항목을 만들고 제출하면 승인 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="6f0a8-109">프로젝트 승인자 또는 관리자가 항목을 검토하고 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="6f0a8-110">항목이 프로젝트와 관련된 경우 승인되면 실제 항목이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="6f0a8-111">이를 통해 비용 및 청구를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="6f0a8-112">항목 승인</span><span class="sxs-lookup"><span data-stu-id="6f0a8-112">Approve an entry</span></span>
<span data-ttu-id="6f0a8-113">**승인** 페이지를 사용하면 다른 유형의 승인을 볼 수 있도록 다른 보기 간에 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="6f0a8-114">**승인** 페이지로 이동하고 **경비**, **시간**, **재료 사용** 또는 **회수** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="6f0a8-115">각 승인을 검토하고 승인할 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="6f0a8-116">**승인** 을 선택하여 선택한 항목을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="6f0a8-117">시스템은 이러한 항목을 처리하고 실제 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="6f0a8-118">항목 거부</span><span class="sxs-lookup"><span data-stu-id="6f0a8-118">Reject an entry</span></span>
<span data-ttu-id="6f0a8-119">프로젝트 승인자는 수정을 위해 사용자에게 항목을 다시 보내야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="6f0a8-120">**승인** 페이지로 이동하고 거부할 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="6f0a8-121">**거부** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-121">Select **Reject**.</span></span>
3. <span data-ttu-id="6f0a8-122">선택 사항으로, **거부 댓글** 대화 상자에서 항목이 거부되는 이유를 사용자에게 알리는 댓글을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="6f0a8-123">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-123">Select **OK**.</span></span> <span data-ttu-id="6f0a8-124">항목이 사용자에게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="6f0a8-125">승인 취소</span><span class="sxs-lookup"><span data-stu-id="6f0a8-125">Cancel approval</span></span>
<span data-ttu-id="6f0a8-126">경우에 따라 이전에 승인된 항목을 취소해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="6f0a8-127">이전에 승인된 항목을 취소하면 재무적 영향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="6f0a8-128">회수 요청 승인</span><span class="sxs-lookup"><span data-stu-id="6f0a8-128">Approving recall requests</span></span>
<span data-ttu-id="6f0a8-129">경우에 따라 컨설턴트가 이전에 승인된 항목을 회수해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="6f0a8-130">이전에 승인된 항목을 취소하면 재무적 영향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="6f0a8-131">프로젝트 승인자는 실제 트랜잭션을 취소하려면 회수를 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="6f0a8-132">프로젝트 승인자 지정</span><span class="sxs-lookup"><span data-stu-id="6f0a8-132">Specify Project approvers</span></span>
<span data-ttu-id="6f0a8-133">각 프로젝트에는 여러 프로젝트 팀 구성원이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-133">Each project has a number of project team members.</span></span> <span data-ttu-id="6f0a8-134">프로젝트 승인자이기도 한 팀 구성원을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="6f0a8-135">**프로젝트** 페이지로 이동하고 목록에서 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="6f0a8-136">**팀** 탭에서 프로젝트 승인자가 될 팀 구성원을 선택한 다음 **편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="6f0a8-137">**프로젝트 승인자** 필드를 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="6f0a8-138">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-138">Select **Save**.</span></span>
5. <span data-ttu-id="6f0a8-139">2-4단계를 반복하여 추가 프로젝트 승인자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="6f0a8-140">사용자의 관리자 구성</span><span class="sxs-lookup"><span data-stu-id="6f0a8-140">Configure the user's manager</span></span>

1. <span data-ttu-id="6f0a8-141">**설정** > **보안** > **사용자** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="6f0a8-142">관리자를 할당할 사용자를 선택하고 **조직 정보** 영역의 목록에서 관리자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="6f0a8-143">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6f0a8-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
