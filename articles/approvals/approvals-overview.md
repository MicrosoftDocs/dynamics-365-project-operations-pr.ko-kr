---
title: 승인 개요
description: 이 항목은 Project Operations에서 승인 작업에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079912"
---
# <a name="approvals-overview"></a><span data-ttu-id="2b807-103">승인 개요</span><span class="sxs-lookup"><span data-stu-id="2b807-103">Approvals overview</span></span>

<span data-ttu-id="2b807-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="2b807-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b807-105">시간 및 경비 제출은 승인 워크플로를 통해 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="2b807-106">입력이 승인되면 트랜잭션이 실제로 기록되거나 일정에 시간이 예약됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="2b807-107">승인 워크플로</span><span class="sxs-lookup"><span data-stu-id="2b807-107">Approvals workflow</span></span>
<span data-ttu-id="2b807-108">시간 또는 경비 항목을 생성하고 실행하면 승인 항목이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="2b807-109">프로젝트 승인자 또는 관리자가 항목을 검토하고 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="2b807-110">항목이 프로젝트와 관련된 경우 승인되면 실제 항목이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="2b807-111">이를 통해 비용 및 청구를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="2b807-112">항목 승인</span><span class="sxs-lookup"><span data-stu-id="2b807-112">Approve an entry</span></span>
<span data-ttu-id="2b807-113">**승인** 양식을 사용하면 다른 유형의 승인을 볼 수 있도록 다른 보기 간에 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="2b807-114">**승인** 양식으로 이동하고 **경비** , **시간** 또는 **리콜** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="2b807-115">각 승인을 검토하고 승인할 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="2b807-116">**승인** 을 선택하여 선택한 항목을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="2b807-117">시스템은 이러한 항목을 처리하고 실제 또는 예약을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="2b807-118">항목 거부</span><span class="sxs-lookup"><span data-stu-id="2b807-118">Reject an entry</span></span>
<span data-ttu-id="2b807-119">프로젝트 승인자는 수정을 위해 사용자에게 항목을 다시 보내야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="2b807-120">**승인** 양식으로 이동하고 거부할 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="2b807-121">**거부** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-121">Select **Reject**.</span></span>
3. <span data-ttu-id="2b807-122">선택 사항 - **거부 댓글** 대화 상자에 댓글을 추가하여 항목이 거부되는 이유를 사용자에게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="2b807-123">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-123">Select **OK**.</span></span> <span data-ttu-id="2b807-124">항목이 사용자에게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="2b807-125">항목 리콜</span><span class="sxs-lookup"><span data-stu-id="2b807-125">Recall entries</span></span>
<span data-ttu-id="2b807-126">어느 시점에서 제출된 항목을 리콜해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="2b807-127">항목이 승인되지 않은 경우 즉시 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="2b807-128">그러나 승인된 항목은 중대한 영향을 미칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="2b807-129">실제에서 트랜잭션을 취소하려면 프로젝트 승인자가 리콜을 승인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="2b807-130">프로젝트 승인자 지정</span><span class="sxs-lookup"><span data-stu-id="2b807-130">Specify Project approvers</span></span>
<span data-ttu-id="2b807-131">각 프로젝트에는 여러 프로젝트 팀 구성원이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-131">Each project has a number of project team members.</span></span> <span data-ttu-id="2b807-132">프로젝트 승인자이기도 한 팀 구성원을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="2b807-133">**프로젝트** 양식으로 이동하고 목록에서 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="2b807-134">**팀** 탭에서 프로젝트 승인자가 될 팀 구성원을 선택한 다음 **편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="2b807-135">**프로젝트 승인자** 필드를 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="2b807-136">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-136">Select **Save**.</span></span>
5. <span data-ttu-id="2b807-137">2-4단계를 반복하여 추가 프로젝트 승인자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="2b807-138">사용자의 관리자 구성</span><span class="sxs-lookup"><span data-stu-id="2b807-138">Configure the user's manager</span></span>

1. <span data-ttu-id="2b807-139">**설정** > **보안** > **사용자** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="2b807-140">관리자를 할당할 사용자를 선택하고 **조직 정보** 영역의 목록에서 관리자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="2b807-141">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2b807-141">Select **Save**.</span></span>


