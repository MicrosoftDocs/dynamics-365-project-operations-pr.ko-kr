---
title: 프로젝트 기반 계약 내용 추정
description: 이 항목은 프로젝트 기반 계약 내용 추정에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180470"
---
# <a name="estimate-a-projectbased-contract-line"></a><span data-ttu-id="67d3f-103">프로젝트 기반 계약 내용 추정</span><span class="sxs-lookup"><span data-stu-id="67d3f-103">Estimate a project–based contract line</span></span>

<span data-ttu-id="67d3f-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="67d3f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span> 

<span data-ttu-id="67d3f-105">Dynamics 365 Project Operations에서 프로젝트 기반 계약 내용에는 계약 내용을 제공하는 데 관련된 작업의 비용 및 잠재적 수익을 추정하는 데 도움이 되는 세부 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-105">In Dynamics 365 Project Operations, a project-based contract line has details that help estimate the cost and potential revenue of the work involved to deliver the contract line.</span></span>

<span data-ttu-id="67d3f-106">프로젝트 기반 계약 내용을 추정하려면 프로젝트 기반 **계약 내용** 의 **계약 내용 세부 정보** 탭으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-106">To estimate a project-based contract line, go to the **Contract Line Detail** tab on the project-based **Contract Line**.</span></span>  <span data-ttu-id="67d3f-107">프로젝트 기반 계약 내용에 대한 견적을 생성하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-107">There are two ways to create an estimate on a project-based contract line:</span></span>

   - <span data-ttu-id="67d3f-108">계약 내용 세부 정보를 수동으로 추가하여 계약 내용에서 직접 견적을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-108">Create an estimate directly on the contract line by manually adding contract line details.</span></span>
   - <span data-ttu-id="67d3f-109">프로젝트 및 프로젝트 계획을 생성한 다음 프로젝트 및 작업을 프로젝트의 계약 내용에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-109">Create a project and a project plan, and then associate the project and tasks to the project's contract line.</span></span> <span data-ttu-id="67d3f-110">이를 통해 계약 내용에 포함된 구성 요소를 기준으로 프로젝트 계획 추정을 계약 내용으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-110">This enables the process by which you can import the project plan estimate into the contract line based on the components included on the contract line.</span></span>

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a><span data-ttu-id="67d3f-111">프로젝트 기반 계약 내용에서 직접 추정 만들기</span><span class="sxs-lookup"><span data-stu-id="67d3f-111">Create an estimate directly on a project–based contract line</span></span>

1. <span data-ttu-id="67d3f-112">계약 내용으로 이동하여 **계약 내용 세부 정보** 탭을 선택합니다. 이 탭에서 생성한 내용은 요약되고 이 **계약 내용** 에 대해 **약정된 값** 으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-112">Go to the contract line and select the **Contract Line Detail** tab. The lines you create on this tab are summarized and display as the **Contracted Value** for this **Contract Line**.</span></span> 
2. <span data-ttu-id="67d3f-113">**계약 내용 세부 정보** 하위 표에서 **+ 새 계약 내용 세부 정보** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-113">In the **Contract Line Details** subgrid, select **+ New Contract Line Detail**.</span></span> <span data-ttu-id="67d3f-114">빨리 만들기 슬라이더가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-114">A quick-create slider opens.</span></span> <span data-ttu-id="67d3f-115">다음 필드는 **계약 내용 세부 정보** 양식에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-115">The following fields are available on the **Contract Line Details** form:</span></span>

| <span data-ttu-id="67d3f-116">필드</span><span class="sxs-lookup"><span data-stu-id="67d3f-116">Field</span></span> | <span data-ttu-id="67d3f-117">위치</span><span class="sxs-lookup"><span data-stu-id="67d3f-117">Location</span></span> | <span data-ttu-id="67d3f-118">설명</span><span class="sxs-lookup"><span data-stu-id="67d3f-118">Description</span></span> | <span data-ttu-id="67d3f-119">다운스트림 영향</span><span class="sxs-lookup"><span data-stu-id="67d3f-119">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="67d3f-120">**설명**</span><span class="sxs-lookup"><span data-stu-id="67d3f-120">**Description**</span></span> | <span data-ttu-id="67d3f-121">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-121">**Quick Create**</span></span> | <span data-ttu-id="67d3f-122">특정 추정치에 대한 설명.</span><span class="sxs-lookup"><span data-stu-id="67d3f-122">A description of the specific estimate.</span></span> | <span data-ttu-id="67d3f-123">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-123">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-124">**거래 클래스**</span><span class="sxs-lookup"><span data-stu-id="67d3f-124">**Transaction Class**</span></span> | <span data-ttu-id="67d3f-125">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-125">**Quick Create**</span></span> | <span data-ttu-id="67d3f-126">이 드롭다운은 프로젝트 기반 계약 내용의 **일반** 탭에 포함된 트랜잭션 클래스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-126">This drop-down is a list of transaction classes included on the **General** tab of the project-based contract line.</span></span> | <span data-ttu-id="67d3f-127">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-127">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-128">**역할**</span><span class="sxs-lookup"><span data-stu-id="67d3f-128">**Role**</span></span> | <span data-ttu-id="67d3f-129">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-129">**Quick Create**</span></span> | <span data-ttu-id="67d3f-130">이 작업을 수행하거나 이 경비를 부담하는 사람의 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-130">The role of the person who is performing this work or incurring this expense.</span></span> | <span data-ttu-id="67d3f-131">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-131">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-132">**범주**</span><span class="sxs-lookup"><span data-stu-id="67d3f-132">**Category**</span></span> | <span data-ttu-id="67d3f-133">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-133">**Quick Create**</span></span> | <span data-ttu-id="67d3f-134">작업 또는 경비의 범주입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-134">The category of the work or expense.</span></span> | <span data-ttu-id="67d3f-135">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-135">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-136">**시작 날짜**</span><span class="sxs-lookup"><span data-stu-id="67d3f-136">**Start Date**</span></span> | <span data-ttu-id="67d3f-137">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-137">**Quick Create**</span></span> | <span data-ttu-id="67d3f-138">작업의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-138">The start date of the work.</span></span> | <span data-ttu-id="67d3f-139">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-139">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-140">**종료 날짜**</span><span class="sxs-lookup"><span data-stu-id="67d3f-140">**End Date**</span></span> | <span data-ttu-id="67d3f-141">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-141">**Quick Create**</span></span> | <span data-ttu-id="67d3f-142">작업의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-142">The end date of the work.</span></span> | <span data-ttu-id="67d3f-143">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-143">This field defaults to the related contract line detail for the cost that is automatically created.</span></span> |
| <span data-ttu-id="67d3f-144">**리소싱 회사**</span><span class="sxs-lookup"><span data-stu-id="67d3f-144">**Resourcing Company**</span></span> | <span data-ttu-id="67d3f-145">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-145">**Quick Create**</span></span> | <span data-ttu-id="67d3f-146">이 비용을 발생시키고 작업을 위한 자원을 제공하는 리소싱 회사 또는 법인입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-146">The resourcing company or legal entity that is incurring this cost and providing the resource to work on it.</span></span> | <span data-ttu-id="67d3f-147">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-147">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="67d3f-148">이 필드는 원가 검색에도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-148">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="67d3f-149">**리소스 조달 단위**</span><span class="sxs-lookup"><span data-stu-id="67d3f-149">**Resourcing Unit**</span></span> | <span data-ttu-id="67d3f-150">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-150">**Quick Create**</span></span> | <span data-ttu-id="67d3f-151">이 비용을 발생시키고 작업할 리소스를 제공하는 리소싱 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-151">The resourcing unit that incurs this cost and provies the resource to work on it.</span></span> | <span data-ttu-id="67d3f-152">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-152">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="67d3f-153">이 필드는 원가 검색에도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-153">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="67d3f-154">**단위 일정**</span><span class="sxs-lookup"><span data-stu-id="67d3f-154">**Unit schedule**</span></span> | <span data-ttu-id="67d3f-155">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-155">**Quick create**</span></span> | <span data-ttu-id="67d3f-156">작업 또는 경비의 단위 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-156">The unit group of the work or expense.</span></span> <span data-ttu-id="67d3f-157">단위는 단위 일정 또는 단위 그룹에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-157">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="67d3f-158">예를 들면 *마일* 과 *킬로미터(Km)* 는 거리를 설명하는 단위 그룹에 속하는 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-158">For example, *miles* and *kilometers (Kms)* are units that belong to a group of units that describe distance.</span></span> | <span data-ttu-id="67d3f-159">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-159">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-160">**단위**</span><span class="sxs-lookup"><span data-stu-id="67d3f-160">**Unit**</span></span> | <span data-ttu-id="67d3f-161">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-161">**Quick Create**</span></span> | <span data-ttu-id="67d3f-162">작업 또는 경비의 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-162">The unit of work or expense.</span></span> | <span data-ttu-id="67d3f-163">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-163">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-164">**수량**</span><span class="sxs-lookup"><span data-stu-id="67d3f-164">**Quantity**</span></span> | <span data-ttu-id="67d3f-165">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-165">**Quick Create**</span></span> | <span data-ttu-id="67d3f-166">작업 또는 경비의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-166">The quantity of work or expense.</span></span> | <span data-ttu-id="67d3f-167">이 필드의 기본값은 자동으로 생성되는 비용에 대한 관련 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-167">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="67d3f-168">**단가**</span><span class="sxs-lookup"><span data-stu-id="67d3f-168">**Unit price**</span></span> | <span data-ttu-id="67d3f-169">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-169">**Quick Create**</span></span> | <span data-ttu-id="67d3f-170">작업을 수행하는 역할의 청구 비율 또는 경비 범주의 판매 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-170">The bill rate of the role that is performing the work or the sales price of the expense category.</span></span> <span data-ttu-id="67d3f-171">이 필드의 기본값은 시작 날짜에 유효한 프로젝트 가격 목록의 역할 및 리소스 단위 조합을 기반으로 하는 **시간** 입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-171">This field defaults for **Time** based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="67d3f-172">경비의 경우 이 필드의 기본값은 시작 날짜에 유효한 프로젝트 가격표의 트랜잭션 범주에 대한 가격 설정에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-172">For expenses, this field's default is from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="67d3f-173">트랜잭션 범주에 대한 가격 책정 방법이 **단위당 가격** 이 아닌 경우 기본값이 없으며 이 필드는 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-173">If the pricing method for the transaction category is not **price-per-unit**, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="67d3f-174">작업을 수행하는 역할의 비용 비율 또는 경비 범주의 단위당 비용입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-174">The cost rate of the role that is performing the work, or the cost per unit of the expense category.</span></span> <span data-ttu-id="67d3f-175">이 필드의 기본값은 **역할에 따른 시간** 및 시작일에 유효한 계약 단위에 첨부된 원가 목록의 역할 가격 라인에 있는 리소싱 단위 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-175">This field defaults for **Time based on the role** and the resourcing unit combination on the role price line of the cost price list attached to the contracting unit effective for the start date.</span></span> <span data-ttu-id="67d3f-176">경비의 경우 이 필드의 기본값은 시작 날짜에 유효한 계약 단위에 첨부된 원가 목록의 범주 가격 라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-176">For expenses, this field's default is based on the category price line of the cost price list attached to the contracting unit that is effective for the start date.</span></span> <span data-ttu-id="67d3f-177">트랜잭션 범주에 대한 가격 책정 방법이 단위당 가격이 아닌 경우 기본값이 없으며 이 필드는 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-177">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="67d3f-178">**예상 세금**</span><span class="sxs-lookup"><span data-stu-id="67d3f-178">**Estimated Tax**</span></span> | <span data-ttu-id="67d3f-179">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-179">**Quick Create**</span></span> | <span data-ttu-id="67d3f-180">사용자가 입력한 이 작업 또는 경비에 대한 예상 세금입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-180">The estimated tax for this work or expense as input by the user.</span></span> | <span data-ttu-id="67d3f-181">사용자가 입력한 이 작업 또는 경비에 대한 예상 세금입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-181">The estimated tax for this work or expense as input by the user.</span></span> |
| <span data-ttu-id="67d3f-182">**금액**</span><span class="sxs-lookup"><span data-stu-id="67d3f-182">**Amount**</span></span> | <span data-ttu-id="67d3f-183">**빨리 만들기**</span><span class="sxs-lookup"><span data-stu-id="67d3f-183">**Quick Create**</span></span> | <span data-ttu-id="67d3f-184">이 필드의 이 값은 **수량** 과 **가격** 필드가 비어 있는 경우 사용자가 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-184">This value in this field can be added by the user if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="67d3f-185">**수량** 과 **가격** 이 채워지면 **금액** 필드는 읽기 전용이며 **(수량 \* 단가) + 세금** 과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-185">If **Quantity** and **Price** are filled, the **Amount** field is read-only and is calculated as **(Quantity \* Unit price) + Tax**.</span></span> | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a><span data-ttu-id="67d3f-186">계약 라인 세부 정보의 가격 업데이트</span><span class="sxs-lookup"><span data-stu-id="67d3f-186">Update prices on contract line details</span></span>

<span data-ttu-id="67d3f-187">계약에 첨부된 프로젝트 가격표 또는 계약 단위의 원가 목록에서 가격을 변경하는 경우 개별 계약 내용 세부 정보의 가격을 새로 고쳐 변경 사항을 반영할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-187">If you change prices on the project price list that is attached to the contract or the cost price list of the contracting unit, you can refresh the prices on the individual contract line details to reflect the change.</span></span> <span data-ttu-id="67d3f-188">**계약** 페이지에서 **다시 계산** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-188">On the **Contract** page, select **Recalculate**.</span></span> <span data-ttu-id="67d3f-189">이 계약의 모든 계약 내용에 대한 가격이 다시 설정되었음을 알리는 경고가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-189">A warning opens to inform you that prices for all contract lines on this contract are reset.</span></span> <span data-ttu-id="67d3f-190">**예** 를 선택하여 판매 및 비용 계약 라인 세부 정보 모두에 대한 가격을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-190">Select **Yes** to refresh prices for both sales and cost contract line details.</span></span>

## <a name="access-contract-line-details-for-cost"></a><span data-ttu-id="67d3f-191">비용에 대한 계약 내용 세부 정보에 액세스</span><span class="sxs-lookup"><span data-stu-id="67d3f-191">Access contract line details for cost</span></span>

<span data-ttu-id="67d3f-192">**계약 내용 세부 정보** 탭에서 그리드의 행을 선택하여 하위 표의 도구 모음에 작업을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-192">On the **Contract Line Details** tab, select a row in the grid to display actions on the toolbar of the subgrid.</span></span> <span data-ttu-id="67d3f-193">하위 표 도구 모음의 첫 번째 작업은 **비용 세부 정보 열기** 입니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-193">The first action on the subgrid tool bar is **Open Cost Detail**.</span></span> <span data-ttu-id="67d3f-194">이 계약 내용 세부 정보에 대한 관련 원가율 및 금액을 보려면 **비용 세부 정보 열기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-194">To see the related cost rate and amount for this contract line detail, select **Open Cost Detail**.</span></span> 

> [!NOTE]
> <span data-ttu-id="67d3f-195">**비용** 에 대한 계약 내용 세부 정보에서 리소싱 회사, 리소싱 단위, 수량, 날짜, 역할 또는 범주 값을 변경하면 **판매** 에 대한 계약 내용 세부 정보에서 해당 값도 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-195">Changing the resourcing company, resourcing unit, quantity, dates, role, or category values on the contract line detail for **Cost** also changes the corresponding values on the contract line detail for **Sales**.</span></span>

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a><span data-ttu-id="67d3f-196">비용 및 판매에 대한 계약 내용 세부 정보의 통화</span><span class="sxs-lookup"><span data-stu-id="67d3f-196">Currency on contract line details for cost and sales</span></span>

<span data-ttu-id="67d3f-197">**판매** 에 대한 계약 내용 세부 정보는 계약 내용 세부 정보의 시작 날짜에 유효한 프로젝트 가격표에서 기본 통화를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-197">The contract line detail for **Sales** sets the default currency from the project price list that is effective for the start date of the contract line detail.</span></span>

<span data-ttu-id="67d3f-198">**비용** 에 대한 계약 내용 세부 정보는 **비용** 에 대한 계약 내용 세부 정보의 시작 날짜에 유효한 계약의 계약 단위의 가격표에서 기본 통화를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-198">The contract line detail for **Cost** sets the default currency from the price list of the contracting unit of the contract that is effective for the start date of the contract line detail for **Cost**.</span></span>

<span data-ttu-id="67d3f-199">수익성 계산은 **비용** 과 **판매** 에 대한 계약 내용 세부 정보의 금액을 계약의 전체 실제 및 예상 마진을 보고하기 위해 환경의 기본 통화로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-199">Profitability calculations convert the amounts for the contract line details for **Cost** and **Sales** into the base currency of the environment to report the overall actual and estimated margins on the contract.</span></span>

> [!NOTE]
> <span data-ttu-id="67d3f-200">날짜 유효 환율이 없기 때문에 통화 반올림 오류 및 변경된 마진이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d3f-200">Currency rounding errors and changed margins could occur because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="67d3f-201">프로젝트 계약에서 이러한 계산을 근사치로만 사용하고, 더 높은 반올림 정밀도와 환율에 대한 날짜 유효성에 대한 인식이 필요한 실제 법정 또는 기타 보고에는 사용하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="67d3f-201">Use these calculations on project contracts only as approximations and not for actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>