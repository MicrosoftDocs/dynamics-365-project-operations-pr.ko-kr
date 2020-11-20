---
title: 자동 송장 만들기 구성
description: 이 항목은 시스템이 송장을 자동으로 생성하도록 구성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122441"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="fa91d-103">자동 송장 만들기 구성</span><span class="sxs-lookup"><span data-stu-id="fa91d-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="fa91d-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fa91d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="fa91d-105">Dynamics 365 Project Operations에서 자동 송장 실행을 구성하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="fa91d-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="fa91d-106">**설정** > **일괄 작업** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="fa91d-107">일괄 처리 작업을 만들고 **Project Operations 생성 송장** 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="fa91d-108">일괄 처리 작업의 이름에는 "송장 만들기"라는 단어가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="fa91d-109">**작업 유형** 필드에서 **없음** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="fa91d-110">기본적으로 **일일 빈도** 및 **활성** 옵션은 **예** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="fa91d-111">**워크플로 실행** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-111">Select **Run Workflow**.</span></span> <span data-ttu-id="fa91d-112">**레코드 보기** 대화 상자에는 세 가지 워크플로가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="fa91d-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="fa91d-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="fa91d-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="fa91d-114">ProcessRunner</span></span>
    - <span data-ttu-id="fa91d-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="fa91d-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="fa91d-116">**ProcessRunCaller** 를 선택한 다음 **추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="fa91d-117">다음 대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="fa91d-118">**절전** 워크플로 뒤에 **프로세스** 워크플로가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fa91d-119">5단계에서 **ProcessRunner** 를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="fa91d-120">그런 다음 **확인** 을 선택하면 **프로세스** 워크플로가 **절전** 워크플로를 뒤따릅니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="fa91d-121">**ProcessRunCaller** 및 **ProcessRunner** 워크플로는 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="fa91d-122">**ProcessRunCaller** 는 **ProcessRunner** 를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="fa91d-123">**ProcessRunner** 는 실제로 송장을 만드는 워크플로입니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="fa91d-124">송장을 만들어야 하는 모든 계약 내용을 통해 해당 라인에 대한 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="fa91d-125">송장을 만들어야 하는 계약 내용을 확인하려면 작업 계약 내용에 대한 송장 실행 날짜를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="fa91d-126">한 계약에 속한 계약 내용에 동일한 송장 실행 날짜가 있는 경우 트랜잭션은 두 개의 송장 라인이 있는 하나의 송장에 결합됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="fa91d-127">송장을 만들 트랜잭션이 없는 경우 작업에서 송장 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="fa91d-128">**ProcessRunner** 가 완료되면 **ProcessRunCaller** 를 호출하고 종료 시간을 제공하면, 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="fa91d-129">그런 다음 **ProcessRunCaller** 는 지정된 종료 시간에서 24시간 동안 실행되는 타이머를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="fa91d-130">타이머가 끝나면 **ProcessRunCaller가** 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="fa91d-131">송장을 만들기 위한 일괄 처리 작업은 되풀이 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="fa91d-132">이 일괄 처리 프로세스가 여러 번 실행되는 경우 작업의 여러 인스턴스가 만들어지고 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="fa91d-133">따라서 일괄 처리 프로세스를 한 번만 시작해야 하며 실행이 중지된 경우에만 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="fa91d-134">일괄 처리 송장 발행은 송장 스케줄에 의해 구성된 프로젝트 계약 라인에 대해서만 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="fa91d-135">고정 가격 청구 방법이 있는 계약 내용에는 이정표가 구성되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="fa91d-136">시간 및 자재 청구 방법이 있는 프로젝트 계약 내용에는 날짜 기반 송장 일정을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="fa91d-137">프로젝트 기반 계약 내용에도 동일하게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa91d-137">The same applies to a project-based contract line.</span></span>     
