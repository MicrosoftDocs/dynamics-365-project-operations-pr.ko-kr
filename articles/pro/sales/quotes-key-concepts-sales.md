---
title: 프로젝트 견적 주요 개념
description: 이 항목은 Project Operations의 프로젝트 견적 사용에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079976"
---
# <a name="project-quote-key-concepts"></a><span data-ttu-id="3aee6-103">프로젝트 견적 주요 개념</span><span class="sxs-lookup"><span data-stu-id="3aee6-103">Project quote key concepts</span></span>

<span data-ttu-id="3aee6-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="3aee6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3aee6-105">다음은 Dynamics 365 Project Operations에서 프로젝트 견적 사용을 시작하기 전에 알아야 할 주요 개념입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-105">The following are key concepts to be aware of before you begin using project quotes in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="3aee6-106">계약 단위</span><span class="sxs-lookup"><span data-stu-id="3aee6-106">Contracting unit</span></span>

<span data-ttu-id="3aee6-107">계약 단위는 프로젝트 납품을 담당하는 부서 또는 관행을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-107">The contracting unit represents the division or practice that owns the project delivery.</span></span> <span data-ttu-id="3aee6-108">각 계약 단위에 대한 리소스 비용을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="3aee6-109">계약 단위의 리소스에 대한 리소스 비용을 지정하면 이 계약 단위가 기업 내의 다른 부서 또는 관행에서 차용하는 리소스에 대해 다른 비용 요율을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-109">When you specify resource cost for a resource in the contracting unit, you will also be able to set up different cost rates for resources that this contracting unit borrows from, or other division or practices within the enterprise.</span></span> <span data-ttu-id="3aee6-110">이를 이전 가격, 리소스 차용 또는 교환 가격이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-110">These are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="3aee6-111">다른 부서에서 리소스를 차용하는 비용을 설정할 때 대출 부서의 통화로 해당 비용 비율을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-111">When you set up the cost of borrowing resources from other divisions, you can also choose to set up those cost rates in the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="3aee6-112">비용 통화</span><span class="sxs-lookup"><span data-stu-id="3aee6-112">Cost currency</span></span>

<span data-ttu-id="3aee6-113">Project Operations의 비용 통화는 비용이 보고되는 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-113">Cost currency in Project Operations is the currency in which costs are reported.</span></span> <span data-ttu-id="3aee6-114">이 통화는 견적, 계약 및 프로젝트의 **계약 단위** 필드에 연결된 통화에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-114">This currency is derived from the currency attached to the **Contracting unit** field on the quote, contract, and project.</span></span> <span data-ttu-id="3aee6-115">비용은 프로젝트에 대해 모든 통화로 기록될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-115">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="3aee6-116">그러나 기록된 통화 비용에서 프로젝트 비용 통화로의 통화 변환이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-116">However, there is currency conversion from the currency costs were recorded in, to the cost currency of the project.</span></span>

<span data-ttu-id="3aee6-117">CDS 플랫폼의 환율은 날짜를 유효화할 수 없기 때문에 통화 환율을 업데이트하면 시간이 지남에 따라 화면상의 비용 합계가 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-117">Because of the exchange rates in the CDS platform can't be date-effective, the on-screen totals for cost may change over time if you update currency exchange rates.</span></span> <span data-ttu-id="3aee6-118">그러나 데이터베이스에 기록된 비용은 금액이 발생한 통화로 저장되기 때문에 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-118">However, costs recorded in the database remain unchanged because the amounts are stored in the currency that they were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="3aee6-119">판매 통화</span><span class="sxs-lookup"><span data-stu-id="3aee6-119">Sales currency</span></span>

<span data-ttu-id="3aee6-120">Project Operations의 판매 통화는 예상 및 실제 판매 금액이 기록되고 표시되는 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-120">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="3aee6-121">또한 거래에 대해 고객에게 송장 발부되는 통화이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-121">It is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="3aee6-122">프로젝트 견적에서 판매 통화는 고객 또는 계정 레코드의 기본값이며 견적이 생성될 때 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-122">On a project quote, the sales currency defaults from the customer or account record and can be changed when the quote is created.</span></span> <span data-ttu-id="3aee6-123">견적을 저장한 후에는 판매 통화를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-123">After the quote is saved, the sales currency can't be changed.</span></span> <span data-ttu-id="3aee6-124">제품 및 프로젝트 가격표는 견적의 판매 통화를 기준으로 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-124">Product and project price lists default based on the sales currency of the quote.</span></span>

<span data-ttu-id="3aee6-125">비용과 달리 판매 값은 판매 통화로만 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-125">Unlike costs, sales values can only be recorded in the Sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="3aee6-126">청구 방법</span><span class="sxs-lookup"><span data-stu-id="3aee6-126">Billing method</span></span>

<span data-ttu-id="3aee6-127">프로젝트에는 일반적으로 고정 수수료 및 소비 기반 계약 모델이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-127">Projects typically have fixed fee and consumption-based contracting models.</span></span> <span data-ttu-id="3aee6-128">이것은 Project Operations에서 **청구 방법** 으로 표현되며 시간과 재료, 고정 가격의 두 가지 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-128">This is represented in Project Operations as **Billing Method** and has two values, time and material and fixed price.</span></span>

- <span data-ttu-id="3aee6-129">**시간 및 재료:** 이는 발생한 각 비용이 해당 수익으로 뒷받침되는 소비 기반 계약 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-129">**Time and material:** This is a consumption-based contract model where each cost incurred is backed by corresponding revenue.</span></span> <span data-ttu-id="3aee6-130">더 많은 비용을 예상하거나 발생하면 해당 예상 및 실제 판매도 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-130">As you estimate or incur more costs, the corresponding estimated and actual sales will also increase.</span></span> <span data-ttu-id="3aee6-131">이 청구 방법이 있는 견적 라인에 초과하지 않는 한도를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-131">You can specify not-to-exceed limits on quote lines that have this billing method.</span></span> <span data-ttu-id="3aee6-132">이것은 실제 수익을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-132">This will cap off the actual revenue.</span></span> <span data-ttu-id="3aee6-133">예상 수익은 초과하지 않는 한도의 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-133">Estimated revenue is not impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="3aee6-134">**고정 가격:** 이것은 판매 값이 발생한 비용과 무관함을 나타내는 고정 수수료 계약 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-134">**Fixed price:** This is a fixed fee contract model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="3aee6-135">판매 값은 고정되어 있으며 더 많은 비용을 예상하거나 발생해도 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-135">The sales value is fixed and does not change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="3aee6-136">프로젝트 가격표</span><span class="sxs-lookup"><span data-stu-id="3aee6-136">Project price lists</span></span>

<span data-ttu-id="3aee6-137">프로젝트 가격표는 시간, 비용 및 기타 프로젝트 관련 구성 요소에 대한 비용이 아닌 기본 가격에 사용되는 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-137">Project price lists are price lists that are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="3aee6-138">여러 가격표가 있을 수 있으며 각 목록은 각 프로젝트 견적에 대해 고유한 날짜 유효성을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-138">There can be multiple prices lists, and each list can have its own date effectivity for each project quote.</span></span> <span data-ttu-id="3aee6-139">프로젝트 가격표에 대한 중복 날짜 유효성은 Project Operations에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-139">Overlapping date effectivity on project price lists is not supported in Project Operations.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="3aee6-140">제품 가격표</span><span class="sxs-lookup"><span data-stu-id="3aee6-140">Product price lists</span></span>

<span data-ttu-id="3aee6-141">제품 가격표는 견적의 제품 기반 라인에 대해 원가가 아닌 기본 가격에 사용되는 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-141">Product price lists are price lists that are used to default prices, not cost rates, for product-based lines on a quote.</span></span> <span data-ttu-id="3aee6-142">견적당 하나의 제품 가격표만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-142">There is only one product price list per quote.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="3aee6-143">트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="3aee6-143">Transaction classes</span></span>

<span data-ttu-id="3aee6-144">Project Operations는 네 가지 유형의 트랜잭션 클래스를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-144">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="3aee6-145">시간</span><span class="sxs-lookup"><span data-stu-id="3aee6-145">Time</span></span>
- <span data-ttu-id="3aee6-146">경비</span><span class="sxs-lookup"><span data-stu-id="3aee6-146">Expense</span></span>
- <span data-ttu-id="3aee6-147">재료</span><span class="sxs-lookup"><span data-stu-id="3aee6-147">Material</span></span>
- <span data-ttu-id="3aee6-148">금액</span><span class="sxs-lookup"><span data-stu-id="3aee6-148">Fee</span></span>

<span data-ttu-id="3aee6-149">비용 및 판매 값은 시간, 경비 및 재료 트랜잭션 클래스에서 추정되고 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-149">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="3aee6-150">요금은 수익 전용 트랜잭션 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-150">Fee is a revenue only class of transactions.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="3aee6-151">작업 항목 및 청구 항목</span><span class="sxs-lookup"><span data-stu-id="3aee6-151">Work entities and billing entities</span></span>

<span data-ttu-id="3aee6-152">작업을 나타내는 엔터티는 프로젝트 및 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-152">Entities that represent work are Projects and Tasks.</span></span> <span data-ttu-id="3aee6-153">청구를 나타내는 엔터티는 견적 라인과 계약 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-153">Entities that represent billing are Quote lines and Contract lines.</span></span> <span data-ttu-id="3aee6-154">다른 작업 엔터티를 견적 또는 계약 내용과 연관시켜 청구 옵션에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-154">You can link different work entities to billing options by associating them with Quote or Contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="3aee6-155">다중 고객 거래</span><span class="sxs-lookup"><span data-stu-id="3aee6-155">Multi-customer deals</span></span>

<span data-ttu-id="3aee6-156">다중 고객 거래는 청구할 고객이 두 명 이상일 때 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-156">Multi-customer deals occur are when there is more than one customer to invoice.</span></span> <span data-ttu-id="3aee6-157">일반적인 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-157">Common examples of this include:</span></span>

- <span data-ttu-id="3aee6-158">**OEM 기업 및 파트너:** 파트너와 리셀러는 부가가치 서비스가 포함된 제품을 판매합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-158">**OEM Enterprises and their partners:** Partners and resellers sell a product with value-added services.</span></span> <span data-ttu-id="3aee6-159">이것은 일반적으로 고객과의 특정 거래 중에 OEM이 프로젝트의 일부에 자금을 제공하는 시나리오입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-159">This is usually a scenario where during a particular deal with a customer, the OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="3aee6-160">**공공 부문 프로젝트:** 지방 정부의 여러 부서가 프로젝트 자금 조달에 동의하고 이전에 합의한 분할에 따라 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-160">**Public sector projects:** Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="3aee6-161">예를 들어, 학군과 시 또는 지방 정부 부서가 수영장 건축 자금에 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-161">For example, a school district and the city or local government department agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="3aee6-162">송장 일정</span><span class="sxs-lookup"><span data-stu-id="3aee6-162">Invoice schedules</span></span>

<span data-ttu-id="3aee6-163">송장 일정은 각 견적 라인에 따라 다르며 선택 사항이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-163">Invoice schedules are specific to each quote line and are also optional.</span></span> <span data-ttu-id="3aee6-164">송장 일정은 특정 시작 및 종료 날짜와 송장 빈도에 따라 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-164">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="3aee6-165">송장 일정은 자동 송장 생성 프로세스가 구성될 때 계약 스테이지에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-165">Invoice schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="3aee6-166">견적 스테이지에서 일정은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-166">In the quote stage, the schedules are optional.</span></span> <span data-ttu-id="3aee6-167">**견적** 스테이지에서 송장 일정이 생성되면 프로젝트 견적이 성공할 때 생성되는 프로젝트 계약에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-167">When invoice schedules are created in the **Quote** stage, they are copied to the project contract that is created when a project quote is won.</span></span>

## <a name="changes-from-dynamics-365-sales-quote"></a><span data-ttu-id="3aee6-168">Dynamics 365 Sales 견적의 변경 사항:</span><span class="sxs-lookup"><span data-stu-id="3aee6-168">Changes from Dynamics 365 Sales quote:</span></span>

<span data-ttu-id="3aee6-169">Project Operations 견적은 Dynamics 365 Sales 견적을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-169">Project Operations quotes are built on the Dynamics 365 Sales quotes.</span></span> <span data-ttu-id="3aee6-170">그러나 알아야 할 기능에는 몇 가지 중요한 차이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-170">However, there are some important differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="3aee6-171">**수정** 및 **활성화** 작업은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-171">The **Revise** and **Activate** actions are not supported.</span></span>
- <span data-ttu-id="3aee6-172">Project Operations 견적에는 두 가지 유형의 라인이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-172">Project Operations quotes have two different types of lines.</span></span> <span data-ttu-id="3aee6-173">하나는 프로젝트용이고 다른 하나는 제품용입니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-173">One is for projects and the other is for products.</span></span>
- <span data-ttu-id="3aee6-174">Project Operations 견적에는 고유한 양식 및 UI 요소, 비즈니스 규칙, 플러그인의 비즈니스 논리, 판매 견적에서 고유하게 만드는 클라이언트 측 스크립트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-174">Project Operations quotes have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales quotes.</span></span>

<span data-ttu-id="3aee6-175">이러한 이유로 판매 견적과 Project Operations 견적을 서로 바꿔서 사용하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3aee6-175">For these reasons, it is not recommended to use a Sales quote and a Project Operations quote interchangeably.</span></span>
