---
title: 프로젝트 계약
description: 이 항목은 다양한 유형의 프로젝트 및 자금 출처에 대해 생성할 수 있는 프로젝트 계약의 예와 계약 및 송장 프로젝트 고객을 관리하는 방법을 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289557"
---
# <a name="project-contracts"></a><span data-ttu-id="95b8e-103">프로젝트 계약</span><span class="sxs-lookup"><span data-stu-id="95b8e-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95b8e-104">이 문서는 다양한 유형의 프로젝트 및 자금 출처에 대해 생성할 수 있는 프로젝트 계약의 예와 계약 및 송장 프로젝트 고객을 관리하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="95b8e-105">프로젝트 계약에 대해 생성하는 프로젝트 유형에 따라 프로젝트 고객에게 송장을 보내는 데 사용되는 방법이 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="95b8e-106">프로젝트 계약 및 관련 프로젝트를 수정할 수 있지만 프로젝트 유형은 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="95b8e-107">프로젝트 계약을 사용하여 동시에 하나 이상의 프로젝트에 송장을 청구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="95b8e-108">프로젝트 계약은 또한 프로젝트 구조의 모든 하위 프로젝트에 대해 일관된 송장 발행 절차를 보장하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="95b8e-109">청구될 모든 프로젝트는 프로젝트 계약과 연결되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="95b8e-110">프로젝트 계약에 대한 설정은 해당 프로젝트 계약과 연결된 모든 프로젝트 및 하위 프로젝트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="95b8e-111">프로젝트 계약은 하나 이상의 자금 출처를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="95b8e-112">따라서 여러 자금 제공자 간에 청구를 분할하고 자금 출처에 지정된 금액 이상이 청구되지 않도록 자금 한도를 설정하고 비용 청구에 대한 자금 조달 규칙을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="95b8e-113">프로젝트 계약 자금</span><span class="sxs-lookup"><span data-stu-id="95b8e-113">Funding for project contracts</span></span>
<span data-ttu-id="95b8e-114">일부 프로젝트 계약은 여러 당사자가 프로젝트 비용을 조달할 책임을 공유하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="95b8e-115">다음 몇 가지 예를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="95b8e-115">Here are some examples:</span></span>

-   <span data-ttu-id="95b8e-116">여러 부서가 있는 대규모 고객이 프로젝트 자금을 부서별로 분할하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="95b8e-117">귀사는 대규모 프로젝트 비용을 외부 조직과 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="95b8e-118">도로 프로젝트는 두 지자체에서 공동 자금을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="95b8e-119">다리 프로젝트는 정부 보조금과 민간 기업이 자금을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="95b8e-120">Dynamics 365 Finance에서 단일 거래 또는 전체 프로젝트에 대한 청구를 여러 고객, 보조금 또는 조직간에 분할할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="95b8e-121">여러 자금 제공자를 보유한 프로젝트에서 고급 자금 조달 프로젝트의 자금 조달에 기여하는 모든 당사자를 자금 출처라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="95b8e-122">고객, 조직 또는 보조금이 자금 조달 출처로 정의된 후 하나 이상의 자금 조달 규칙에 할당될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="95b8e-123">자금 조달 규칙에는 프로젝트의 다양한 자금 출처에 비용을 할당하는 방법을 결정하는 기준이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="95b8e-124">구매 요청 및 구매 주문에 나타나는 것과 같은 재고 품목은 분할할 수 없기 때문에 분배시 비용 금액을 여러 자금 출처로 분할할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="95b8e-125">따라서 재고 출고가 전기될 때까지 자금 조달 출처 값은 0(영)으로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="95b8e-126">재고 출고가 전기되면 프로젝트의 계정 분배 규칙에 따라 비용 금액이 분배됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="95b8e-127">다음은 여러 자금 출처간에 청구를 더 쉽게 분할하기 위해 취할 수 있는 몇 가지 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="95b8e-128">프로젝트에 입력된 모든 트랜잭션이 프로젝트 계약과 동일한 판매 통화를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="95b8e-129">자금 조달 한도를 설정하여 자금 출처가 프로젝트에 대해 지정된 금액 이상으로 청구되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="95b8e-130">각 근로자, 품목, 범주, 범주 그룹 및 거래 유형(또는 모든 트랜잭션 유형에 대해)에 대한 자금 조달 규칙 및 자금 한도를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="95b8e-131">선택적 시작 및 종료 날짜를 선택하여 각 자금 조달 규칙이 유효한 기간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="95b8e-132">각 자금 출처가 담당하는 비율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="95b8e-133">자금 할당 계산으로 인해 발생하는 차이를 반올림할 책임이 있는 자금 출처를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="95b8e-134">프로젝트 비용이 외부 고객에게 청구되고 내부 조직에 청구되는 방식을 결정하는 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="95b8e-135">추가 자금을 확보하거나 내부적으로 비용을 부담하기로 결정할 때까지 보류 자금 계정에 거래를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="95b8e-136">트랜잭션과 연관시킬 세금 그룹을 결정하기 위해 프로젝트에서 세금 그룹 지정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="95b8e-137">프로젝트 수준에서 세금 그룹이 지정되지 않은 경우 프로젝트 계약이 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="95b8e-138">예: 여러 자금 출처(단순)</span><span class="sxs-lookup"><span data-stu-id="95b8e-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="95b8e-139">다음 표는 여러 자금 출처 간의 자금 할당을 관리하기 위한 시나리오를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="95b8e-140">이러한 시나리오는 다음 가정을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="95b8e-141">우선 순위 설정은 다른 자금 조달 규칙 기준이 적용되기 전에 자금 할당에 반영됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="95b8e-142">자금 조달 규칙이 유효한 기간 d를 정의하기 위해 지정된 날짜 범위가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95b8e-143"><strong>시나리오</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="95b8e-144"><strong>자금 출처</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="95b8e-145"><strong>할당 비율</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="95b8e-146"><strong>할당 우선 순위</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95b8e-147">자금이 소진될 때까지 하나의 자금 출처에 비용을 할당하고 자금이 소진될 때까지 두 번째 자금 출처에 비용을 할당한 다음 마지막으로 나머지 비용을 세 번째 자금 출처에 할당하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-148">자금　출처　1</span><span class="sxs-lookup"><span data-stu-id="95b8e-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="95b8e-149">자금　출처　2</span><span class="sxs-lookup"><span data-stu-id="95b8e-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="95b8e-150">자금　출처　3</span><span class="sxs-lookup"><span data-stu-id="95b8e-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-151">100%</span><span class="sxs-lookup"><span data-stu-id="95b8e-151">100%</span></span></li>
<li><span data-ttu-id="95b8e-152">100%</span><span class="sxs-lookup"><span data-stu-id="95b8e-152">100%</span></span></li>
<li><span data-ttu-id="95b8e-153">100%</span><span class="sxs-lookup"><span data-stu-id="95b8e-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-154">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-154">1</span></span></li>
<li><span data-ttu-id="95b8e-155">2</span><span class="sxs-lookup"><span data-stu-id="95b8e-155">2</span></span></li>
<li><span data-ttu-id="95b8e-156">3</span><span class="sxs-lookup"><span data-stu-id="95b8e-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95b8e-157">비용의 75%를 하나의 자금 출처에 할당하고 25%를 두 번째 자금 출처에 할당하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="95b8e-158">이러한 자금 출처 중 하나가 모두 소진되면 세 번째 자금 출처에서 나머지 비용을 지불하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-159">자금　출처　1</span><span class="sxs-lookup"><span data-stu-id="95b8e-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="95b8e-160">자금　출처　2</span><span class="sxs-lookup"><span data-stu-id="95b8e-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="95b8e-161">자금　출처　3</span><span class="sxs-lookup"><span data-stu-id="95b8e-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-162">75%</span><span class="sxs-lookup"><span data-stu-id="95b8e-162">75%</span></span></li>
<li><span data-ttu-id="95b8e-163">25%</span><span class="sxs-lookup"><span data-stu-id="95b8e-163">25%</span></span></li>
<li><span data-ttu-id="95b8e-164">100%</span><span class="sxs-lookup"><span data-stu-id="95b8e-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-165">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-165">1</span></span></li>
<li><span data-ttu-id="95b8e-166">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-166">1</span></span></li>
<li><span data-ttu-id="95b8e-167">2</span><span class="sxs-lookup"><span data-stu-id="95b8e-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95b8e-168">비용의 75%를 하나의 자금 출처에 할당하고 25%를 두 번째 자금 출처에 할당하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="95b8e-169">이러한 자금 출처 중 하나가 모두 소진되면 나머지 비용을 세 번째 자금 출처와 네 번째 자금 출처간에 분할하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-170">자금　출처　1</span><span class="sxs-lookup"><span data-stu-id="95b8e-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="95b8e-171">자금　출처　2</span><span class="sxs-lookup"><span data-stu-id="95b8e-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="95b8e-172">자금　출처　3</span><span class="sxs-lookup"><span data-stu-id="95b8e-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="95b8e-173">자금　출처　4</span><span class="sxs-lookup"><span data-stu-id="95b8e-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-174">75%</span><span class="sxs-lookup"><span data-stu-id="95b8e-174">75%</span></span></li>
<li><span data-ttu-id="95b8e-175">25%</span><span class="sxs-lookup"><span data-stu-id="95b8e-175">25%</span></span></li>
<li><span data-ttu-id="95b8e-176">50%</span><span class="sxs-lookup"><span data-stu-id="95b8e-176">50%</span></span></li>
<li><span data-ttu-id="95b8e-177">50%</span><span class="sxs-lookup"><span data-stu-id="95b8e-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-178">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-178">1</span></span></li>
<li><span data-ttu-id="95b8e-179">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-179">1</span></span></li>
<li><span data-ttu-id="95b8e-180">2</span><span class="sxs-lookup"><span data-stu-id="95b8e-180">2</span></span></li>
<li><span data-ttu-id="95b8e-181">2</span><span class="sxs-lookup"><span data-stu-id="95b8e-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95b8e-182">비용의 처음 25%를 하나의 자금 출처에 할당하고 나머지를 두 번째 자금 출처에 할당하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-183">자금　출처　1</span><span class="sxs-lookup"><span data-stu-id="95b8e-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="95b8e-184">자금　출처　2</span><span class="sxs-lookup"><span data-stu-id="95b8e-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-185">25%</span><span class="sxs-lookup"><span data-stu-id="95b8e-185">25%</span></span></li>
<li><span data-ttu-id="95b8e-186">100%</span><span class="sxs-lookup"><span data-stu-id="95b8e-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="95b8e-187">6</span><span class="sxs-lookup"><span data-stu-id="95b8e-187">1</span></span></li>
<li><span data-ttu-id="95b8e-188">2</span><span class="sxs-lookup"><span data-stu-id="95b8e-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="95b8e-189">예: 여러 자금 출처(복잡)</span><span class="sxs-lookup"><span data-stu-id="95b8e-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="95b8e-190">다음 순서로 사용할 자금 출처가 세 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="95b8e-191">자금 출처 2가 소진될 때까지 자금 출처 2와 자금 출처 3을 동일하게 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="95b8e-192">소진될 때까지 자금 출처 3을 계속 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="95b8e-193">자금 출처 3이 소진된 후 자금 출처 1을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="95b8e-194">이 목표를 달성하려면 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="95b8e-195">자금 출처 2와 자금 출처 3에 대한 자금 한도를 각각의 금액으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="95b8e-196">다음 자금 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="95b8e-197">규칙 1(우선 순위 1): 거래의 50%를 자금 출처 2에 할당하고 50%를 자금 출처 3에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="95b8e-198">규칙 2(우선 순위 2): 거래의 100%를 자금 출처 3에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="95b8e-199">규칙 3(우선 순위 3): 거래의 100%를 자금 출처 1에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="95b8e-200">이 설정은 트랜잭션이 트랜잭션에 적용되는지 여부를 결정하기 위해 규칙 및 제한에 대해 확인되기 때문에 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="95b8e-201">트랜잭션에 적용되는 특정 규칙이나 제한이 없는 경우 모든 트랜잭션 규칙이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="95b8e-202">모든 트랜잭션 규칙은 모든 트랜잭션과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="95b8e-203">트랜잭션과 일치하는 규칙이 발견되면 해당 규칙에 할당된 백분율이 먼저 적용되지만 설정된 제한과 일치하는지 확인한 후에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="95b8e-204">한도에 도달하고 자금 출처의 자금이 소진되면 자금 한도와 연관된 자금 조달 규칙이 무시되고 프로그램은 적용되는 다음 규칙을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="95b8e-205">어떤 경우에는 트랜잭션의 일부만 규칙에 따라 할당될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="95b8e-206">이는 트랜잭션이 할당될 때 한계에 도달하기 때문에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="95b8e-207">이 경우 해당 규칙에 따라 특정 금액만 할당됩니다(예: 각 자금 출처에 50%).</span><span class="sxs-lookup"><span data-stu-id="95b8e-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="95b8e-208">이 섹션의 앞부분에서 설명한 규칙 1의 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="95b8e-209">나머지는 시퀀스의 다음 규칙에 따라 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="95b8e-210">다음 표에서는 이 시나리오를 자세히 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95b8e-211"><strong>초점</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="95b8e-212"><strong>세부 정보</strong></span><span class="sxs-lookup"><span data-stu-id="95b8e-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95b8e-213">자금 조달 규칙</span><span class="sxs-lookup"><span data-stu-id="95b8e-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-214">규칙 1(우선 순위 1): 모든 트랜잭션.</span><span class="sxs-lookup"><span data-stu-id="95b8e-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="95b8e-215">자금 출처 2를 50%로, 자금 출처 3을 50%로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="95b8e-216">규칙 2(우선 순위 2): 모든 트랜잭션.</span><span class="sxs-lookup"><span data-stu-id="95b8e-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="95b8e-217">자금 출처 3을 100%로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="95b8e-218">규칙 3(우선 순위 2): 모든 트랜잭션.</span><span class="sxs-lookup"><span data-stu-id="95b8e-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="95b8e-219">자금 출처 1을 100%로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95b8e-220">자금 한도</span><span class="sxs-lookup"><span data-stu-id="95b8e-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-221">자금 출처 1 한도 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="95b8e-222">자금 출처 2 한도 = 500.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="95b8e-223">자금 출처 3 한도 = 750.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95b8e-224">거래 1</span><span class="sxs-lookup"><span data-stu-id="95b8e-224">Transaction 1</span></span></td>
<td><span data-ttu-id="95b8e-225"><strong>거래 금액:</strong> 100.00 <strong> 자금 조달:</strong> 규칙 1이 적용된 후 트랜잭션이 완전히 지급되기 때문에 트랜잭션은 규칙 1에 따라서 만 지급됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="95b8e-226">트랜잭션은 자금 출처 2와 자금 출처 3간에 동일하게 자금이 조달됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="95b8e-227">자금 출처 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="95b8e-228">자금 출처 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95b8e-229">거래 2</span><span class="sxs-lookup"><span data-stu-id="95b8e-229">Transaction 2</span></span></td>
<td><span data-ttu-id="95b8e-230"><strong>트랜잭션 금액: </strong> 5,000.00<strong> 자금 조달: </strong> 트랜잭션은 세 가지 규칙 모두에 따라 지불됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="95b8e-231"><strong>규칙 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="95b8e-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="95b8e-232">자금 출처 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="95b8e-233">자금 출처 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="95b8e-234">
<strong>규칙 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="95b8e-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="95b8e-235">자금 출처 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="95b8e-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="95b8e-236">
<strong>규칙 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="95b8e-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="95b8e-237">자금 출처 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="95b8e-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95b8e-238">각 자금 출처에 대해 분배된 총 자금</span><span class="sxs-lookup"><span data-stu-id="95b8e-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="95b8e-239">자금 출처 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="95b8e-240">자금 출처 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="95b8e-241">자금 출처 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="95b8e-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="95b8e-242">청구 규칙</span><span class="sxs-lookup"><span data-stu-id="95b8e-242">Billing rules</span></span>
<span data-ttu-id="95b8e-243">고객과 프로젝트 계약을 협상할 때 프로젝트 작업에 대해 고객에게 청구할 수 있는 방법과 시기를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="95b8e-244">프로젝트 계약 및 프로젝트를 설정한 후 프로젝트에 대한 결제 규칙을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="95b8e-245">청구 규칙은 프로젝트 계약에 지정된 프로젝트 조건을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="95b8e-246">생성할 수 있는 청구 규칙은 프로젝트 계약 조건 및 청구 규칙과 연결하는 프로젝트 유형(예: 시간 및 자재 또는 고정 가격)에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="95b8e-247">프로젝트 계약에 대해 둘 이상의 청구 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="95b8e-248">동일한 프로젝트 계약과 연결되어 있고 청구 조건이 유사한 여러 프로젝트에 청구 규칙을 할당할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="95b8e-249">다음 유형의 청구 규칙을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="95b8e-250">**납품 단위** – 납품 단위를 완료하면 고객에게 송장을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="95b8e-251">계약에서 납품 단위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="95b8e-252">**진행** – 프로젝트의 지정된 비율을 완료하면 고객에게 송장을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="95b8e-253">완료된 작업 비율을 자동으로 계산하도록 청구 규칙을 설정하거나 완료된 작업 비율과 고객에게 청구할 금액을 수동으로 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="95b8e-254">**중요 시점** – 중요 시점에 도달하면 프로젝트 중요 시점의 전체 금액에 대해 고객에게 청구합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="95b8e-255">**요금** – 일반적으로 서비스 비용의 일정 비율인 관리 수수료와 서비스에 대해 고객에게 청구합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="95b8e-256">**시간과 재료** – 프로젝트에 사용된 시간과 재료의 가치에 대해 고객에게 청구합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="95b8e-257">모든 유형의 청구 규칙에 대해 프로젝트가 합의된 단계에 도달할 때까지 고객 송장에서 공제되는 보존 비율을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="95b8e-258">지급 유지율은 프로젝트 계약서에 명시되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="95b8e-259">금액은 고객 송장에 있는 라인의 총 금액을 기준으로 계산되고 차감됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="95b8e-260">**시간과 재료** 및 **진행** 청구 규칙에 따라 청구 가능 범주를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="95b8e-261">청구 가능 범주는 고객 송장에 포함되어야 하는 거래를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="95b8e-262">고객에게 송장을 보낼 준비가 되면 프로젝트 송장 금액이 청구 규칙에 따라 계산되고 프로젝트 송장 제안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="95b8e-263">다음 섹션에서는 프로젝트의 결제 규칙을 설정하고 관리하는 방법을 보여주는 예를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="95b8e-264">예: 전달된 단위 수를 기반으로 하는 청구 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="95b8e-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="95b8e-265">조직은 교육 세션당 10,000개의 비용으로 고객의 직원에게 총 5개의 교육 세션을 제공하기로 합의했습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="95b8e-266">각 교육 세션 후에 고객에게 송장을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="95b8e-267">계약에 대한 청구 규칙을 설정할 때 다음 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="95b8e-268">전달 단위는 하나의 교육 세션입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="95b8e-269">단가는 교육 세션당 10,000입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="95b8e-270">총 단위 수는 5개의 교육 세션입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="95b8e-271">하나의 교육 세션을 완료하면 배달된 첫 번째 단위에 대해 10,000개의 송장을 생성하고 고객에게 송장을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="95b8e-272">예: 지정된 프로젝트 완료 비율(수동 계산)을 기반으로 하는 청구 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="95b8e-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="95b8e-273">소프트웨어 컨설팅 회사인 귀사는 고객이 개발 중인 제품의 일부를 개발하기 위해 고객과 계약을 체결합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="95b8e-274">조직은 6개월 동안 소프트웨어 코드를 제공하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="95b8e-275">고객은 작업에 대해 총 100,000개의 비용을 조직에 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="95b8e-276">계약에 지정된 대로 프로젝트에서 완료된 작업 백분율을 기반으로 고객에게 청구하는 청구 규칙을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="95b8e-277">첫 달 말에 고객을 만나 작업 완료율을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="95b8e-278">귀하와 고객이 프로젝트를 검토한 후 프로젝트가 15% 완료되었다고 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="95b8e-279">100,000의 15,000(15%)에 대한 송장을 생성하여 고객에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="95b8e-280">예: 지정된 프로젝트 완료 비율(자동 계산)을 기반으로 하는 청구 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="95b8e-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="95b8e-281">소프트웨어 개발 회사인 귀하의 조직은 고객을 위해 30,000 달러에 대한 급여 회계 패키지를 개발하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="95b8e-282">고객은 완료된 작업 비율을 기반으로 조직에 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="95b8e-283">프로젝트 비용이 20,000이라고 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="95b8e-284">프로젝트 계약은 청구 프로세스에서 사용하는 작업 범주를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="95b8e-285">각 범주에 대해 완료된 작업 백분율에 대한 송장 금액을 자동으로 계산하는 청구 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="95b8e-286">각 범주에 대한 예산을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="95b8e-287">**개발** – 비용 15,000, 수익 20,000</span><span class="sxs-lookup"><span data-stu-id="95b8e-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="95b8e-288">**설치** – 비용 5,000, 수익 10,000</span><span class="sxs-lookup"><span data-stu-id="95b8e-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="95b8e-289">고객 송장을 처음 생성할 때 송장 금액은 다음 정보를 기반으로 자동 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="95b8e-290">한 달 후 프로젝트의 작업자는 프로젝트에 대한 작업 표를 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="95b8e-291">작업자의 시간 비용은 개발에 5,000, 설치에 1,000입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="95b8e-292">개발 작업은 33% 완료(실제 비용 5,000/15,000 예산 비용), 설치 작업은 20% 완료(실제 비용 1,000/예산 비용 5,000)입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="95b8e-293">송장 금액 8,667이 자동으로 계산됩니다(20,000의 33% + 10,000의 20%).</span><span class="sxs-lookup"><span data-stu-id="95b8e-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="95b8e-294">8,667에 대한 송장을 생성하여 고객에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="95b8e-295">예: 합의된 중요 시점을 기반으로 하는 청구 규칙 생성</span><span class="sxs-lookup"><span data-stu-id="95b8e-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="95b8e-296">관리 컨설팅 회사인 귀사는 고객이 판매하려는 소비자 제품에 대한 시장 조사를 수행하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="95b8e-297">고객은 3월부터 3개월 동안 귀하의 서비스를 사용하는 데 동의하고 조직에 50,000달러를 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="95b8e-298">이 프로젝트에는 세 가지 중요 시점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-298">The project has three milestones:</span></span>

-   <span data-ttu-id="95b8e-299">중요 시점 1: 소비자 데이터 수집 – 3월 31일</span><span class="sxs-lookup"><span data-stu-id="95b8e-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="95b8e-300">중요 시점 2: 소비자 데이터 분석 – 4월 30일</span><span class="sxs-lookup"><span data-stu-id="95b8e-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="95b8e-301">중요 시점 3: 제품 실행 가능성 제안 제시 – 5월 31일</span><span class="sxs-lookup"><span data-stu-id="95b8e-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="95b8e-302">고객은 조직에 첫 번째 중요 시점에 10,000, 두 번째 중요 시점에 20,000, 세 번째 중요 시점에 20,000을 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="95b8e-303">프로젝트 계약을 설정할 때 완료된 중요 시점을 기반으로 고객에게 청구하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="95b8e-304">결제 규칙 설정에는 다음 단계가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="95b8e-305">프로젝트 중요 시점을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-305">Define the project milestones.</span></span>
-   <span data-ttu-id="95b8e-306">각 중요 시점이 완료 될 때 고객에게 청구할 금액을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="95b8e-307">3월 31일에 첫 번째 중요 시점이 완료되면 중요 시점을 완료된 것으로 표시한 다음 10,000에 대한 송장을 생성하여 고객에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="95b8e-308">중요 시점을 완료로 표시할 때까지 중요 시점에 대한 송장을 생성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="95b8e-309">예: 서비스 및 관리 수수료를 기반으로 하는 청구 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="95b8e-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="95b8e-310">관리 컨설팅 회사인 귀사는 소매 회사인 고객이 개발 중인 제품의 실행 가능성을 평가하기 위해 시장 조사를 수행하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="95b8e-311">계약 조건은 시간 및 재료를 기준으로 연구를 수행할 상위 3명의 경영 컨설턴트의 서비스를 제공할 것임을 명시합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="95b8e-312">고객은 프로젝트에 부과되는 컨설팅 시간에 대해 10% 관리 수수료와 함께 시간당 100을 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="95b8e-313">프로젝트 계약을 설정할 때 프로젝트에 부과되는 컨설팅 시간에 10% 관리 수수료를 추가하는 청구 규칙을 생성하십시오.</span><span class="sxs-lookup"><span data-stu-id="95b8e-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="95b8e-314">고객에 대한 송장을 생성하면 고객에게 10%의 관리 수수료와 컨설팅 시간 비용이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="95b8e-315">예를 들어 세 명의 컨설턴트가 프로젝트에서 총 200시간을 작업한 경우 다음 계산을 기반으로 22,000에 대한 송장이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="95b8e-316">시간당 100에서 200 시간 = 20,000</span><span class="sxs-lookup"><span data-stu-id="95b8e-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="95b8e-317">10% 관리비 = 2,000</span><span class="sxs-lookup"><span data-stu-id="95b8e-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="95b8e-318">총 송장 금액 = 22,000</span><span class="sxs-lookup"><span data-stu-id="95b8e-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="95b8e-319">수수료가 고객에게 과세되고 프로젝트 계약에서 판매 세 그룹을 선택하면 판매 세 그룹이 수수료 청구 규칙에 자동으로 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="95b8e-320">예: 시간 및 재료 값에 대한 청구 규칙 생성</span><span class="sxs-lookup"><span data-stu-id="95b8e-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="95b8e-321">소프트웨어 컨설팅 회사인 귀사는 향후 6개월 동안 고객을 위해 소프트웨어 개발 프로젝트를 수행할 5 명의 기술 컨설턴트를 제공하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="95b8e-322">고객은 각 컨설팅 시간에 150을 지불하고 사무용품 비용을 지불하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="95b8e-323">귀하의 조직은 매월 말에 고객에게 송장을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="95b8e-324">프로젝트 계약을 설정할 때 프로젝트의 시간과 재료에 대해 매달 고객에게 청구하는 데 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="95b8e-325">다음 정보를 포함하는 청구 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="95b8e-326">계약 기간은 6개월입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-326">The contract period is six months.</span></span>
-   <span data-ttu-id="95b8e-327">컨설팅 시간은 시간당 150의 비율로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="95b8e-328">사무용품은 비용으로 청구되며 프로젝트 총 비용은 10,000을 초과하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="95b8e-329">프로젝트 기간 동안 매월 말에 고객 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="95b8e-330">첫 달 동안 컨설턴트는 프로젝트에 총 800 시간을 기록했습니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="95b8e-331">프로젝트에 부과되는 사무용품 비용은 2,000입니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="95b8e-332">따라서 월말에 122,000에 대한 송장을 생성합니다. 이는 시간당 150 시간에 800 시간에 사무용품에 대한 2,000을 더한 것으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="95b8e-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]