---
title: Project Service Automation에서 송장 발부
description: 이 주제는 송장 발부에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080116"
---
# <a name="invoicing-in-project-service-automation"></a><span data-ttu-id="c0bae-103">Project Service Automation에서 송장 발부</span><span class="sxs-lookup"><span data-stu-id="c0bae-103">Invoicing in Project Service Automation</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c0bae-104">Dynamics 365 Project Service Automation의 송장 발부는 프로젝트 관리자가 고객을 위한 송장을 만들기 전에 두 번째 수준의 승인을 제공하기 때문에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-104">Invoicing in Dynamics 365 Project Service Automation is useful because it gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="c0bae-105">첫 번째 승인 수준은 프로젝트 팀 구성원이 제출하는 시간 및 경비 항목이 승인되면 완료됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-105">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="c0bae-106">PSA는 다음과 같은 이유로 고객 관련 송장을 생성하도록 설계되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-106">PSA isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="c0bae-107">세금 정보가 포함되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-107">It doesn't contain tax information.</span></span>
- <span data-ttu-id="c0bae-108">올바르게 구성된 환율을 사용하여 다른 통화를 송장 통화로 변환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-108">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="c0bae-109">송장을 인쇄할 수 있도록 송장의 형식을 올바르게 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-109">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="c0bae-110">대신 재무 또는 회계 시스템을 사용하여 PSA에서 생성된 송장 제안서의 정보를 사용하는 고객 대면 송장을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-110">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from invoice proposals that are generated in PSA.</span></span>

## <a name="creating-project-invoices-in-psa"></a><span data-ttu-id="c0bae-111">PSA에서 프로젝트 송장 만들기</span><span class="sxs-lookup"><span data-stu-id="c0bae-111">Creating project invoices in PSA</span></span>

<span data-ttu-id="c0bae-112">프로젝트 송장은 한 번에 하나씩 또는 일괄로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-112">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="c0bae-113">수동으로 만들거나 자동화된 실행에서 생성되도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-113">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices-in-psa"></a><span data-ttu-id="c0bae-114">PSA에서 수동으로 프로젝트 송장 만들기</span><span class="sxs-lookup"><span data-stu-id="c0bae-114">Manually create project invoices in PSA</span></span>

<span data-ttu-id="c0bae-115">**프로젝트 계약** 목록 페이지에서 각 프로젝트 계약에 대해 프로젝트 송장을 별도로 만들거나 여러 프로젝트 계약에 대해 대량으로 송장을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-115">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="c0bae-116">이 단계를 수행하여 특정 프로젝트 계약에 대한 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-116">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="c0bae-117">**프로젝트 계약** 목록 페이지에서 프로젝트 계약을 연 다음 **송장 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-117">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    ![특정 프로젝트 계약에 대한 프로젝트 송장 만들기](media/CreateProjectInvoicesOneByOne.png)

    <span data-ttu-id="c0bae-119">**송장 준비** 상태가 있는 선택한 프로젝트 계약에 대한 모든 트랜잭션에 대한 송장이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="c0bae-120">이러한 거래에는 시간, 비용, 이정표 및 제품 기반 계약 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="c0bae-121">다음 단계에 따라 대량으로 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="c0bae-122">**프로젝트 계약** 목록 페이지에서 송장을 만들어야 하는 하나 이상의 프로젝트 계약을 선택한 다음 **프로젝트 송장 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    ![대량으로 프로젝트 송장 만들기](media/CreateProjectInvoicesBulk.png)

    <span data-ttu-id="c0bae-124">송장을 만들기 전에 지연될 수 있다는 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-124">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="c0bae-125">프로세스도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-125">The process is also shown.</span></span>

2. <span data-ttu-id="c0bae-126">**확인** 을 선택하여 메시지 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-126">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="c0bae-127">**송장 준비** 상태가 있는 선택한 계약 내용의 대한 모든 트랜잭션에 대한 송장이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-127">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="c0bae-128">이러한 거래에는 시간, 비용, 이정표 및 제품 기반 계약 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-128">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="c0bae-129">생성된 송장을 보려면 **영업** \> **청구** \> **송장** 으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="c0bae-129">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="c0bae-130">각 프로젝트 계약에 대해 하나의 송장이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-130">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a><span data-ttu-id="c0bae-131">PSA에서 프로젝트 송장 자동 생성 설정</span><span class="sxs-lookup"><span data-stu-id="c0bae-131">Set up automated creation of project invoices in PSA</span></span>

<span data-ttu-id="c0bae-132">다음 단계를 따라서 PSA에서 자동화된 송장 실행을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-132">Follow these steps to configure an automated invoice run in PSA.</span></span>

1. <span data-ttu-id="c0bae-133">**Project Service** \> **설정** \> **일괄 처리 작업** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-133">Go to **Project Service** \> **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="c0bae-134">일괄 처리 작업을 만들고 **PSA 생성 송장** 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-134">Create a batch job, and name it **PSA Create Invoices**.</span></span> <span data-ttu-id="c0bae-135">일괄 처리 작업의 이름에는 "송장 만들기"라는 용어가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-135">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="c0bae-136">**작업 유형** 필드에서 **없음** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-136">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="c0bae-137">기본적으로 **일일 빈도** 및 **활성** 옵션은 **예** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-137">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="c0bae-138">**워크플로 실행** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-138">Select **Run Workflow**.</span></span> <span data-ttu-id="c0bae-139">**레코드 보기** 대화 상자에는 세 가지 워크플로가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-139">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="c0bae-140">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="c0bae-140">ProcessRunCaller</span></span>
    - <span data-ttu-id="c0bae-141">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="c0bae-141">ProcessRunner</span></span>
    - <span data-ttu-id="c0bae-142">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="c0bae-142">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="c0bae-143">**ProcessRunCaller** 를 선택한 다음 **추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-143">Select **ProcessRunCaller** , and then select **Add**.</span></span>
6. <span data-ttu-id="c0bae-144">다음 대화 상자에서 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-144">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="c0bae-145">**절전** 워크플로 뒤에 **프로세스** 워크플로가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-145">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="c0bae-146">5단계에서 **ProcessRunner** 를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-146">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="c0bae-147">그런 다음 **확인** 을 선택하면 **프로세스** 워크플로가 **절전** 워크플로를 뒤따릅니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-147">Then, when you select **OK** , a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="c0bae-148">**ProcessRunCaller** 및 **ProcessRunner** 워크플로는 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-148">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="c0bae-149">**ProcessRunCaller** 는 **ProcessRunner** 를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-149">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="c0bae-150">**ProcessRunner** 는 실제로 송장을 만드는 워크플로입니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-150">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="c0bae-151">송장을 만들어야 하는 모든 계약 내용을 통해 해당 라인에 대한 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-151">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="c0bae-152">송장을 만들어야 하는 계약 내용을 확인하려면 작업 계약 내용에 대한 송장 실행 날짜를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-152">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="c0bae-153">한 계약에 속한 계약 내용에 동일한 송장 실행 날짜가 있는 경우 트랜잭션은 두 개의 송장 라인이 있는 하나의 송장에 결합됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-153">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="c0bae-154">송장을 만들 트랜잭션이 없는 경우 작업에서 송장 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-154">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="c0bae-155">**ProcessRunner** 가 완료되면 **ProcessRunCaller** 를 호출하고 종료 시간을 제공하면, 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-155">After **ProcessRunner** has finished running, it calls **ProcessRunCaller** , provides the end time, and is closed.</span></span> <span data-ttu-id="c0bae-156">그런 다음 **ProcessRunCaller** 는 지정된 종료 시간에서 24시간 동안 실행되는 타이머를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-156">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="c0bae-157">타이머가 끝나면 **ProcessRunCaller가** 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-157">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="c0bae-158">송장을 만들기 위한 일괄 처리 작업은 되풀이 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-158">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="c0bae-159">이 일괄 처리 프로세스가 여러 번 실행되는 경우 작업의 여러 인스턴스가 만들어지고 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-159">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="c0bae-160">따라서 일괄 처리 프로세스를 한 번만 시작해야 하며 실행이 중지된 경우에만 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-160">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="c0bae-161">Project Service Automation의 일괄 송장 발행은 송장 일정으로 구성된 프로젝트 계약 내용에 대해서만 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-161">Batch invoicing in Project Service Automation only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="c0bae-162">고정 가격 청구 방법이 있는 계약 내용에는 이정표가 구성되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-162">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="c0bae-163">시간 및 자재 청구 방법이 있는 프로젝트 계약 내용에는 날짜 기반 송장 일정을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-163">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="c0bae-164">견적 라인을 기반으로 하는 프로젝트의 컨텍스트에서 송장 발행 빈도를 설정하는 방법에 대한 정보는 토픽, [견적 및 견적 라인](basic-quote-lines.md#invoice-schedule)에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-164">Information about setting up invoicing frequencies in the context of a project that is based on a quote line, is provided in the topic, [Quotes and quote lines](basic-quote-lines.md#invoice-schedule).</span></span> <span data-ttu-id="c0bae-165">프로젝트 기반 계약 내용에도 동일하게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-165">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-psa-invoice"></a><span data-ttu-id="c0bae-166">초안 PSA 송장 편집</span><span class="sxs-lookup"><span data-stu-id="c0bae-166">Edit a draft PSA invoice</span></span>

<span data-ttu-id="c0bae-167">임시 프로젝트 송장을 만들 때 시간 및 경비 항목이 승인될 때 생성된 모든 청구되지 않은 판매 트랜잭션이 송장에 당겨지게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-167">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="c0bae-168">송장이 아직 초안 단계에 있는 동안 다음을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-168">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="c0bae-169">송장 라인 세부 정보를 삭제하거나 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-169">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="c0bae-170">수량 및 청구 유형을 편집하고 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-170">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="c0bae-171">송장에 시간, 비용 및 수수료를 거래로 직접 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-171">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="c0bae-172">송장 라인이 이러한 트랜잭션 클래스를 허용하는 계약 내용에 매핑된 경우 이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-172">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="c0bae-173">송장을 확인하려면 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-173">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="c0bae-174">확인 작업은 단방향 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-174">The Confirm action is a one-way action.</span></span> <span data-ttu-id="c0bae-175">**확인** 을 선택하면 시스템에서 송장을 읽기 전용으로 만들고 각 송장 라인에 대한 각 송장 라인 세부 정보에서 청구된 영업 실제 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-175">When you select **Confirm** , the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="c0bae-176">송장 라인 세부 정보가 청구되지 않은 실제 영업을 참조하는 경우 시스템은 청구되지 않은 실제 영업도 반대로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-176">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="c0bae-177">(시간 또는 경비 항목에서 만든 모든 송장 라인 세부 정보 실제 청구되지 않은 판매를 참조합니다.) 총원장 통합 시스템은 이 반전을 사용하여 회계 목적으로 진행 중인 WIP(프로젝트 작업)를 되돌릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-177">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-psa-invoice"></a><span data-ttu-id="c0bae-178">확인된 PSA 송장 수정</span><span class="sxs-lookup"><span data-stu-id="c0bae-178">Correct a confirmed PSA invoice</span></span>

<span data-ttu-id="c0bae-179">확인된 PSA 송장을 편집(수정)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-179">Confirmed PSA invoices can be edited (corrected).</span></span> <span data-ttu-id="c0bae-180">확인된 송장을 수정하면 새 임시 수정 송장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-180">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="c0bae-181">원래 송장의 모든 트랜잭션 및 수량을 되돌리려는 가정이기 때문에 이 수정 송장에는 원래 송장의 모든 트랜잭션이 포함되며 모든 수량은 0(제로)입니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-181">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="c0bae-182">트랜잭션에 수정이 필요하지 않은 경우 초안 수정 송장에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-182">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="c0bae-183">일부 수량만 되돌리거나 반환하려면 라인 세부 사항에서 **수량** 필드를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-183">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="c0bae-184">송장 라인 세부 정보를 열면 원래 송장 수량을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-184">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="c0bae-185">그런 다음 원래 송장 수량보다 적거나 많은 현재 송장 수량을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-185">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="c0bae-186">수정 송장을 확인할 때 원래 청구된 영업 실제가 반대이며, 새 청구된 영업 실제가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-186">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="c0bae-187">수량이 줄어든 경우 그 차이로 인해 실제 청구되지 않은 새 영업도 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-187">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="c0bae-188">예를 들어 원래 청구된 영업이 8시간이고 수정된 송장 라인 세부 정보가 6시간으로 줄어든 경우 PSA는 원래 청구된 영업 라인을 반대로 하고 두 개의 새 실제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-188">For example, if the original billed sales was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, PSA reverses the original billed sales line and creates two new actuals:</span></span>

- <span data-ttu-id="c0bae-189">6시간 동안 실제 청구된 영업.</span><span class="sxs-lookup"><span data-stu-id="c0bae-189">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="c0bae-190">나머지 2시간 동안 청구되지 않은 영업 실제.</span><span class="sxs-lookup"><span data-stu-id="c0bae-190">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="c0bae-191">이 거래는 고객과의 협상에 따라 나중에 청구되거나 요금이 부과되지 않는 것으로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0bae-191">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
