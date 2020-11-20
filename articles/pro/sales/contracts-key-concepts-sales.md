---
title: 프로젝트 계약 - 주요 개념 - 라이트
description: 이 항목은 프로젝트 계약의 주요 개념에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ce37c9dd18fd01e599e8766389e42c066e182547
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177069"
---
# <a name="project-contracts---key-concepts---lite"></a><span data-ttu-id="0e3b6-103">프로젝트 계약 - 주요 개념 - 라이트</span><span class="sxs-lookup"><span data-stu-id="0e3b6-103">Project contracts - Key concepts - lite</span></span>

<span data-ttu-id="0e3b6-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="0e3b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e3b6-105">이 항목에서는 Dynamics 365 Project Operations에서 프로젝트 계약 사용을 시작하기 전에 알아야 할 주요 개념을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="0e3b6-106">계약 단위</span><span class="sxs-lookup"><span data-stu-id="0e3b6-106">Contracting Unit</span></span>

<span data-ttu-id="0e3b6-107">계약 단위는 프로젝트 납품을 담당하는 부서 또는 관행을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-107">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="0e3b6-108">각 계약 단위에 대한 리소스 비용을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="0e3b6-109">리소스에 대한 리소스 비용을 지정할 때 리소스에 대해 다른 비용 요율을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-109">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="0e3b6-110">이 계약 단위는 기업 내의 다른 부서 또는 관행에서 이러한 리소스를 차용합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-110">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="0e3b6-111">리소스에 대한 비용 요금을 이전 가격, 리소스 차용 또는 교환 가격이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-111">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="0e3b6-112">다른 부서에서 리소스를 차용하기 위해 비용 요금을 설정할 때 대출 부서의 통화를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-112">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="0e3b6-113">비용 통화</span><span class="sxs-lookup"><span data-stu-id="0e3b6-113">Cost Currency</span></span>

<span data-ttu-id="0e3b6-114">비용 통화는 비용이 화면에 보고되는 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-114">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="0e3b6-115">이 통화는 계약 및 프로젝트의 **계약 단위** 필드에 연결된 통화에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-115">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="0e3b6-116">비용은 프로젝트에 대해 모든 통화로 기록될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-116">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="0e3b6-117">그러나 기록된 통화 비용에서 화면에 표시될 때 프로젝트 비용 통화로의 통화 변환이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-117">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="0e3b6-118">Common Data Service(CDS) 플랫폼의 환율은 날짜를 유효화할 수 없기 때문에 통화 환율을 업데이트하면 시간이 지남에 따라 화면상의 비용 합계가 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-118">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="0e3b6-119">그러나 데이터베이스에 기록된 비용은 금액이 발생한 통화로 저장되기 때문에 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-119">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="0e3b6-120">판매 통화</span><span class="sxs-lookup"><span data-stu-id="0e3b6-120">Sales Currency</span></span>

<span data-ttu-id="0e3b6-121">Project Operations의 판매 통화는 예상 및 실제 판매 금액이 기록되고 표시되는 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-121">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="0e3b6-122">또한 판매 통화는 거래에 대해 고객에게 송장 발부되는 통화이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-122">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="0e3b6-123">프로젝트 계약에서 판매 통화는 고객 또는 계정 레코드의 기본값이며 계약이 생성될 때 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-123">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="0e3b6-124">견적을 성공으로 마감하여 계약이 생성되면 계약의 통화가 견적의 통화에서 기본값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-124">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="0e3b6-125">처음부터 프로젝트 계약을 작성하면 **판매 통화** 필드는 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-125">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="0e3b6-126">제품 및 프로젝트 가격표는 계약에서 이 통화를 기준으로 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-126">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="0e3b6-127">비용과 달리 판매 값은 판매 통화로만 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-127">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="0e3b6-128">청구 방법</span><span class="sxs-lookup"><span data-stu-id="0e3b6-128">Billing Method</span></span>

<span data-ttu-id="0e3b6-129">일반적으로 프로젝트에 대한 두 가지 유형의 계약 모델, 고정 수수료 및 소비 기반이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-129">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="0e3b6-130">이러한 모델은 Project Operations에서 두 가지 가능한 값이 있는 청구 방법으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-130">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="0e3b6-131">시간 및 재료: 발생한 각 비용이 해당 수익으로 뒷받침되는 소비 기반 계약 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-131">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="0e3b6-132">더 많은 비용을 예상하거나 발생하면 해당 예상 및 실제 판매도 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-132">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="0e3b6-133">실제 수익을 상한하는 이 청구 방법이 있는 계약 내용에 대해 초과하지 않는 한도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-133">Specify not-to-exceed limits on contract lines that have this billing method that caps off the actual revenue.</span></span> <span data-ttu-id="0e3b6-134">예상 수익은 초과하지 않는 한도의 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-134">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="0e3b6-135">고정 가격: 판매 값이 발생한 비용과 무관함을 나타내는 고정 수수료 계약 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-135">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="0e3b6-136">판매 값은 고정되어 있으며 더 많은 비용을 예상하거나 발생해도 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-136">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="0e3b6-137">프로젝트 가격표</span><span class="sxs-lookup"><span data-stu-id="0e3b6-137">Project Price lists</span></span>

<span data-ttu-id="0e3b6-138">프로젝트 가격표는 시간, 비용 및 기타 프로젝트 관련 구성 요소에 대한 비용이 아닌 기본 가격에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-138">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="0e3b6-139">여러 가격표가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-139">There can be multiple prices lists.</span></span> <span data-ttu-id="0e3b6-140">각 가격표에는 각 프로젝트 계약에 대한 고유한 날짜 유효성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-140">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="0e3b6-141">프로젝트 가격표에 대한 중복 날짜 유효성은 Project Operations에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-141">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="0e3b6-142">프로젝트 견적을 받아 프로젝트 계약이 생성되면 계약 이름과 날짜가 포함된 프로젝트 가격표가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-142">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="0e3b6-143">이 정보를 복사하면 이 프로젝트 계약의 프로젝트 구성 요소에 대한 사용자 정의 가격이 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-143">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="0e3b6-144">제품 가격표</span><span class="sxs-lookup"><span data-stu-id="0e3b6-144">Product price lists</span></span>

<span data-ttu-id="0e3b6-145">제품 가격표는 계약의 제품 기반 라인에 대해 원가가 아닌 기본 가격에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-145">Product price lists are used to default prices, not cost rates, for product-based lines on contract.</span></span> <span data-ttu-id="0e3b6-146">계약당 하나의 제품 가격표만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-146">There is only one product price list per contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="0e3b6-147">트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="0e3b6-147">Transaction Classes</span></span>

<span data-ttu-id="0e3b6-148">Project Operations는 네 가지 유형의 트랜잭션 클래스를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="0e3b6-149">시간</span><span class="sxs-lookup"><span data-stu-id="0e3b6-149">Time</span></span>
- <span data-ttu-id="0e3b6-150">경비</span><span class="sxs-lookup"><span data-stu-id="0e3b6-150">Expense</span></span>
- <span data-ttu-id="0e3b6-151">재료</span><span class="sxs-lookup"><span data-stu-id="0e3b6-151">Material</span></span>
- <span data-ttu-id="0e3b6-152">금액</span><span class="sxs-lookup"><span data-stu-id="0e3b6-152">Fee</span></span>

<span data-ttu-id="0e3b6-153">비용 및 판매 값은 시간, 경비 및 재료 트랜잭션 클래스에서 추정되고 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="0e3b6-154">요금은 수익 전용 트랜잭션 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="0e3b6-155">작업 항목 및 청구 항목</span><span class="sxs-lookup"><span data-stu-id="0e3b6-155">Work entities and Billing entities</span></span>

<span data-ttu-id="0e3b6-156">작업을 나타내는 엔터티는 프로젝트 및 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="0e3b6-157">청구를 나타내는 엔터티는 계약 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="0e3b6-158">다른 작업 엔터티를 계약 내용과 연관시켜 청구 옵션에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="0e3b6-159">다중 고객 거래</span><span class="sxs-lookup"><span data-stu-id="0e3b6-159">Multi-customer deals</span></span>

<span data-ttu-id="0e3b6-160">다중 고객 거래에는 거래에 청구할 고객이 두 명 이상 있습입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="0e3b6-161">일반적인 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-161">Common examples include:</span></span>

- <span data-ttu-id="0e3b6-162">OEM 기업 및 파트너: 파트너 및 리셀러는 일반적으로 고객과의 특정 거래와 관련된 일부 부가 가치 서비스가 포함된 제품을 판매합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="0e3b6-163">OEM은 프로젝트의 일부에 자금을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="0e3b6-164">공공 부문 프로젝트: 지방 정부의 여러 부서가 프로젝트 자금 조달에 동의하고 이전에 합의한 분할에 따라 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="0e3b6-165">예를 들어, 학군과 지방 정부가 수영장 건축 자금에 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="0e3b6-166">송장 일정</span><span class="sxs-lookup"><span data-stu-id="0e3b6-166">Invoice Schedules</span></span>

<span data-ttu-id="0e3b6-167">송장 일정은 각 계약 내용에 따라 다르며 자동 송장 발행이 작동하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="0e3b6-168">송장 일정은 특정 시작 및 종료 날짜와 송장 빈도에 따라 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="0e3b6-169">이 일정은 자동 송장 생성 프로세스가 구성될 때 계약 스테이지에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="0e3b6-170">견적에서 프로젝트 계약이 생성되면 송장 일정이 견적에서 프로젝트 계약으로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-the-dynamics-365-sales-contract"></a><span data-ttu-id="0e3b6-171">Dynamics 365 Sales 계약의 변경 사항</span><span class="sxs-lookup"><span data-stu-id="0e3b6-171">Changes from the Dynamics 365 Sales contract</span></span>

<span data-ttu-id="0e3b6-172">Project Operations 계약은 Dynamics 365 Sales 계약을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-172">Project Operations contracts are built on Dynamics 365 Sales contracts.</span></span> <span data-ttu-id="0e3b6-173">그러나 알아야 할 기능에는 몇 가지 중요한 편차와 차이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-173">However, there are some important deviations and differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="0e3b6-174">Project Operations 계약에는 프로젝트와 제품에 대한 두 가지 유형의 라인이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-174">Project Operations contracts have two different types of lines, one for projects and one for products.</span></span>
- <span data-ttu-id="0e3b6-175">Project Operations 계약에는 고유한 양식 및 UI 요소, 비즈니스 규칙, 플러그인의 비즈니스 논리, 판매 계약에서 고유하게 만드는 클라이언트 측 스크립트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-175">Project Operations contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales contracts.</span></span>

<span data-ttu-id="0e3b6-176">이러한 이유로 판매 계약과 프로젝트 계약을 서로 바꿔서 사용해서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3b6-176">For these reasons, you shouldn't use a Sales contract and Project contract interchangeably.</span></span>
