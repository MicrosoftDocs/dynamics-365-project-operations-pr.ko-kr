---
title: 실제
description: 이 토픽은 Microsoft Dynamics 365 Project Operations에서 실제 값으로 작업하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852552"
---
# <a name="actuals"></a><span data-ttu-id="b22f8-103">실제 값</span><span class="sxs-lookup"><span data-stu-id="b22f8-103">Actuals</span></span> 

<span data-ttu-id="b22f8-104">_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="b22f8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b22f8-105">실제는 프로젝트에 대한 검토 및 승인된 재무 및 일정 진행 상황을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="b22f8-106">시간, 경비, 재료 사용 항목, 분개장 항목 및 송장의 승인 결과로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="b22f8-107">분개장 항목 및 시간 제출</span><span class="sxs-lookup"><span data-stu-id="b22f8-107">Journal lines and time submission</span></span>

<span data-ttu-id="b22f8-108">시간 항목에 대한 자세한 내용은 [시간 항목 개요](../time/time-entry-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b22f8-109">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="b22f8-109">Time and materials</span></span>

<span data-ttu-id="b22f8-110">제출된 시간 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b22f8-111">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-111">Fixed price</span></span>

<span data-ttu-id="b22f8-112">제출된 시간 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b22f8-113">기본 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-113">Default pricing</span></span>

<span data-ttu-id="b22f8-114">기본 가격을 작성하는 논리는 분개장 항목에 들어있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="b22f8-115">시간 항목의 필드 값이 분개장 항목에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="b22f8-116">이러한 값에는 트랜잭션 날짜, 프로젝트가 매핑된 계약 내용 및 해당 가격표의 통화 결과가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="b22f8-117">기본 가격에 영향을 주는 **역할** 및 **리소싱 단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b22f8-118">시간 항목에 사용자 지정 필드를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="b22f8-119">필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b22f8-120">사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b22f8-121">트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="b22f8-122">분개장 항목 및 기본 경비 제출</span><span class="sxs-lookup"><span data-stu-id="b22f8-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="b22f8-123">경비 항목에 대한 자세한 내용은 [경비 개요](../expense/expense-overview.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b22f8-124">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="b22f8-124">Time and materials</span></span>

<span data-ttu-id="b22f8-125">제출된 기본 경비 항목이 시간 및 자재 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용 및 미 청구 판매에 하나씩 두 개의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b22f8-126">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-126">Fixed price</span></span>

<span data-ttu-id="b22f8-127">제출된 기본 경비 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b22f8-128">기본 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-128">Default pricing</span></span>

<span data-ttu-id="b22f8-129">경비에 대한 기본 가격을 입력하는 논리는 경비 범주를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="b22f8-130">해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b22f8-131">기본 가격에 영향을 주는 **트랜잭션 범주** 및 **단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b22f8-132">그러나 이것은 가격표의 가격 책정 방법이 **단가** 인 경우에만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="b22f8-133">가격 책정 방법이 **원가** 또는 **비용 초과 가격 인상액** 인 경우 경비 항목이 생성될 때 입력된 가격이 비용에 사용되며 판매 분개장 항목의 가격은 가격 책정 방법을 기준으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="b22f8-134">경비 항목에 사용자 정의 필드를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="b22f8-135">필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b22f8-136">사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b22f8-137">트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="b22f8-138">분개장 항목 및 재료 사용량 로그 제출</span><span class="sxs-lookup"><span data-stu-id="b22f8-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="b22f8-139">경비 항목에 대한 자세한 내용은 [재료 사용량 로그](../material/material-usage-log.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b22f8-140">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="b22f8-140">Time and materials</span></span>

<span data-ttu-id="b22f8-141">제출된 재료 사용량 로그 항목이 시간 및 재료 계약 내용에 매핑된 프로젝트에 링크되면 시스템은 비용 및 미청구 판매에 대한 두 개의 분개장 항목을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b22f8-142">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-142">Fixed price</span></span>

<span data-ttu-id="b22f8-143">제출된 재료 사용량 로그 항목이 고정 가격 계약 내용에 매핑된 프로젝트에 연결되면 시스템은 비용에 대해 하나의 분개장 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b22f8-144">기본 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-144">Default pricing</span></span>

<span data-ttu-id="b22f8-145">재료의 기본 가격을 입력하는 논리는 제품 및 단위 조합을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="b22f8-146">해당 가격표를 결정하기 위해 처리 날짜, 프로젝트가 매핑된 계약 행 및 통화가 모두 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b22f8-147">기본 가격에 영향을 주는 **제품 ID** 및 **단위** 같은 필드는 분개장 항목에서 적절한 가격을 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b22f8-148">그러나 이것은 카탈로그 제품에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-148">However, this only works for catalog products.</span></span> <span data-ttu-id="b22f8-149">직접 입력 제품의 경우 재료 사용량 로그 항목 생성시 입력한 가격이 분개장 항목의 원가 및 판매 가격에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="b22f8-150">**재료 사용량 로그** 항목에 사용자 정의 필드를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="b22f8-151">필드 값을 실제 값으로 전파하려면 **실제** 및 **분개장 항목** 테이블에 필드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b22f8-152">사용자 정의 코드를 사용하여 트랜잭션 출처를 사용하는 분개장 항목을 통해 선택한 필드 값을 시간 입력에서 실제로 전파합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b22f8-153">트랜잭션 기원 및 연결에 대한 자세한 내용은 [실제 데이터를 원본 레코드에 연결](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b22f8-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="b22f8-154">항목 분개장을 사용하여 비용 기록</span><span class="sxs-lookup"><span data-stu-id="b22f8-154">Use entry journals to record costs</span></span>

<span data-ttu-id="b22f8-155">항목 분개장을 사용하여 비용 또는 수익을 자재, 수수료, 시간, 경비 또는 세금 처리 등급에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="b22f8-156">분개장은 다음과 같은 목적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="b22f8-157">다른 시스템의 트랜잭션 실제를 Microsoft Dynamics 365 Project Operations로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="b22f8-158">다른 시스템에서 발생한 비용을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="b22f8-159">이러한 비용에는 조달 또는 하도급 비용이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b22f8-160">애플리케이션은 분개장 항목 유형 또는 분개장 항목에 입력된 관련 가격을 검증하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="b22f8-161">따라서 실제 값이 프로젝트에 미치는 회계 영향을 완전히 알고 있는 사용자만 항목 분개장을 사용하여 실제 값을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="b22f8-162">이 분개장 유형의 영향으로 인해 항목 분개장을 만들 수 있는 액세스 권한이 있는 사람을 신중하게 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="b22f8-163">프로젝트 이벤트에 근거한 실제값 기록</span><span class="sxs-lookup"><span data-stu-id="b22f8-163">Record actuals based on project events</span></span>

<span data-ttu-id="b22f8-164">Project Operations는 프로젝트 중에 발생하는 재무 트랜잭션을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="b22f8-165">이러한 처리는 실제값으로 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="b22f8-166">다음 표들은 프로젝트가 시간 및 자재 또는 고정 가격 프로젝트인지, 판매전 단계에 있는지, 또는 내부 프로젝트인지에 따라 생성되는 다양한 타입의 실제값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="b22f8-167">리소스가 프로젝트의 계약 단위와 같은 조직 단위에 속합니다</span><span class="sxs-lookup"><span data-stu-id="b22f8-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b22f8-168">이벤트</span><span class="sxs-lookup"><span data-stu-id="b22f8-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b22f8-169">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b22f8-170">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b22f8-171">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b22f8-172">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="b22f8-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b22f8-173">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b22f8-174">실제</span><span class="sxs-lookup"><span data-stu-id="b22f8-174">Actuals</span></span></th>
<th><span data-ttu-id="b22f8-175">거래 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-175">Transaction currency</span></span></th>
<th><span data-ttu-id="b22f8-176">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-176">Fixed price</span></span></th>
<th><span data-ttu-id="b22f8-177">거래 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f8-178">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b22f8-179">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-180">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b22f8-181">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b22f8-182">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b22f8-183">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-183">Cost actual</span></span></td>
<td><span data-ttu-id="b22f8-184">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-185">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-186">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="b22f8-187">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-188">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-189">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b22f8-190">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b22f8-191">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b22f8-192">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-192">Cost actual</span></span></td>
<td><span data-ttu-id="b22f8-193">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-194">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-195">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-196">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-197">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-198">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-199">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-200">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-201">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b22f8-202">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b22f8-203">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b22f8-204">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-205">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-206">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-207">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-208">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-209">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-209">Billed sales</span></span></td>
<td><span data-ttu-id="b22f8-210">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b22f8-211">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b22f8-212">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b22f8-213">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-214">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-215">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-216">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-217">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-218">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-219">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-220">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-221">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b22f8-222">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b22f8-223">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b22f8-224">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b22f8-225">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b22f8-226">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="b22f8-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b22f8-227">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-228">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-229">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-230">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-230">Billed sales</span></span></td>
<td><span data-ttu-id="b22f8-231">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b22f8-232">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b22f8-233">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b22f8-234">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-235">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-236">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-237">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-238">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="b22f8-239">리소스가 프로젝트의 계약 단위와 다른 조직 단위에 속합니다</span><span class="sxs-lookup"><span data-stu-id="b22f8-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b22f8-240">이벤트</span><span class="sxs-lookup"><span data-stu-id="b22f8-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b22f8-241">청구 가능 또는 판매된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b22f8-242">판매전 단계의 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b22f8-243">내부 프로젝트</span><span class="sxs-lookup"><span data-stu-id="b22f8-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b22f8-244">시간 및 자재</span><span class="sxs-lookup"><span data-stu-id="b22f8-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b22f8-245">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b22f8-246">실제</span><span class="sxs-lookup"><span data-stu-id="b22f8-246">Actuals</span></span></th>
<th><span data-ttu-id="b22f8-247">거래 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-247">Transaction currency</span></span></th>
<th><span data-ttu-id="b22f8-248">고정 가격</span><span class="sxs-lookup"><span data-stu-id="b22f8-248">Fixed price</span></span></th>
<th><span data-ttu-id="b22f8-249">거래 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f8-250">시간 항목이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b22f8-251">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-252">시간 항목이 제출되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b22f8-253">실제값 엔터티의 활동 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b22f8-254">시간이 승인되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b22f8-255">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-255">Cost actual</span></span></td>
<td><span data-ttu-id="b22f8-256">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b22f8-257">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b22f8-258">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b22f8-259">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b22f8-260">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-261">청구되지 않은 매출액 실제값 – 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b22f8-262">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-263">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="b22f8-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b22f8-264">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-265">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b22f8-266">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b22f8-267">시간이 승인되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b22f8-268">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-268">Cost actual</span></span></td>
<td><span data-ttu-id="b22f8-269">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-270">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-271">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-272">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-273">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="b22f8-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-274">리소스 단위 비용</span><span class="sxs-lookup"><span data-stu-id="b22f8-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b22f8-275">리소스 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-276">조직간 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b22f8-277">계약 단위 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-278">청구되지 않은 매출액 실제값 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-279">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-280">청구되지 않은 매출액 실제값 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-281">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b22f8-282">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 변경 또는 증가가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b22f8-283">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b22f8-284">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-285">이정표를 위한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-286">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-287">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b22f8-288">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-289">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-289">Billed sales</span></span></td>
<td><span data-ttu-id="b22f8-290">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b22f8-291">청구서가 확정되었으며, 승인 중에 청구 가능 시간의 감소가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b22f8-292">청구되지 않은 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b22f8-293">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-294">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-295">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-296">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b22f8-297">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-298">청구된 매출액 – 새 수량에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-299">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-300">청구된 매출액 – 차이에 대해 청구 불가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-301">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b22f8-302">청구 가능한 수량을 늘리기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b22f8-303">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b22f8-304">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b22f8-305">이정표를 위한 청구된 매출액 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b22f8-306">이정표 상태를 <strong>청구서 발부됨</strong>에서 <strong>청구서 발부 준비</strong>로 변경</span><span class="sxs-lookup"><span data-stu-id="b22f8-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b22f8-307">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-308">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b22f8-309">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b22f8-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-310">청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-310">Billed sales</span></span></td>
<td><span data-ttu-id="b22f8-311">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b22f8-312">청구 가능한 수량을 줄이기 위해 청구서가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22f8-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b22f8-313">청구된 매출액 – 전환</span><span class="sxs-lookup"><span data-stu-id="b22f8-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b22f8-314">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-315">새 수량에 대한 청구된 매출액</span><span class="sxs-lookup"><span data-stu-id="b22f8-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b22f8-316">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f8-317">미청구된 매출액 – 차이에 대해 청구 가능</span><span class="sxs-lookup"><span data-stu-id="b22f8-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b22f8-318">프로젝트 계약 통화</span><span class="sxs-lookup"><span data-stu-id="b22f8-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
