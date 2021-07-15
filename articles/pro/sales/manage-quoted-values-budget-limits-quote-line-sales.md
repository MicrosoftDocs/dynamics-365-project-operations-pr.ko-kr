---
title: 프로젝트 기반 견적 라인 개요
description: 이 항목은 프로젝트 작업에 프로젝트 기반 견적 라인 사용에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369879"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="f9149-103">프로젝트 기반 견적 라인 개요</span><span class="sxs-lookup"><span data-stu-id="f9149-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="f9149-104">_**적용 대상:** 라이트 배포 - 견적 송장 처리, 리소스/비 재고 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f9149-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f9149-105">프로젝트 기반 견적 라인은 계약에 대한 프로젝트 작업을 추정하는 데 도움이 되도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="f9149-106">프로젝트 기반 견적 라인의 구조는 다음 개념으로 프로젝트 견적을 위해 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="f9149-107">청구 방법</span><span class="sxs-lookup"><span data-stu-id="f9149-107">Billing Method</span></span>
- <span data-ttu-id="f9149-108">프로젝트 및 작업 매핑</span><span class="sxs-lookup"><span data-stu-id="f9149-108">Project and Task Mapping</span></span>
- <span data-ttu-id="f9149-109">포함된 트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="f9149-109">Included Transaction classes</span></span>
- <span data-ttu-id="f9149-110">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="f9149-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="f9149-111">청구 가능성 설정</span><span class="sxs-lookup"><span data-stu-id="f9149-111">Chargeability setup</span></span>
- <span data-ttu-id="f9149-112">견적 라인 세부 정보를 사용한 추정</span><span class="sxs-lookup"><span data-stu-id="f9149-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="f9149-113">견적 라인 고객</span><span class="sxs-lookup"><span data-stu-id="f9149-113">Quote line Customers</span></span>

<span data-ttu-id="f9149-114">다음 표는 프로젝트 기반 견적 라인의 **일반** 탭의 필드에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="f9149-115">이 필드는 프로젝트 작업에 대한 상세하고 기초적인 추정을 위한 기초를 설정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="f9149-116">**필드**</span><span class="sxs-lookup"><span data-stu-id="f9149-116">**Field**</span></span> | <span data-ttu-id="f9149-117">**설명**</span><span class="sxs-lookup"><span data-stu-id="f9149-117">**Description**</span></span> | <span data-ttu-id="f9149-118">**다운스트림 영향**</span><span class="sxs-lookup"><span data-stu-id="f9149-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9149-119">이름</span><span class="sxs-lookup"><span data-stu-id="f9149-119">Name</span></span> | <span data-ttu-id="f9149-120">추정되는 견적의 개별 구성 요소를 식별하는 데 도움이 되는 견적 라인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="f9149-121">견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-122">청구 방법</span><span class="sxs-lookup"><span data-stu-id="f9149-122">Billing Method</span></span> | <span data-ttu-id="f9149-123">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="f9149-124">이 필드에는 Dynamics 365 Project Operations에서 지원하는 두 가지 주요 계약 모델이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="f9149-125">- 고정 가격</span><span class="sxs-lookup"><span data-stu-id="f9149-125">- Fixed price</span></span></br><span data-ttu-id="f9149-126">- 시간 및 재료.</span><span class="sxs-lookup"><span data-stu-id="f9149-126">- Time and material.</span></span>| <span data-ttu-id="f9149-127">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-128">Project</span><span class="sxs-lookup"><span data-stu-id="f9149-128">Project</span></span> | <span data-ttu-id="f9149-129">이 옵션 필드를 사용하여이 계약에 대한 작업을 제공하는 데 사용할 프로젝트를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="f9149-130">프로젝트가 견적 라인에 매핑되면 청구 가능한 작업을 설정하고 견적 라인 세부 정보로 견적 라인에 프로젝트 기반 견적을 가져오는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="f9149-131">프로젝트가 프로젝트 기반 견적 라인에 매핑되지 않은 경우 각 견적 라인 세부 정보를 생성하여 견적을 수동으로 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="f9149-132">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="f9149-133">포함된 작업</span><span class="sxs-lookup"><span data-stu-id="f9149-133">Included Tasks</span></span> | <span data-ttu-id="f9149-134">이 견적 라인이 선택한 프로젝트의 프로젝트 작업 전체 또는 일부에 사용되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="f9149-135">이 필드에는 다음 가능한 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-135">This field has the following possible values:</span></span></br><span data-ttu-id="f9149-136">- 모든 프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="f9149-136">- All project tasks</span></span></br><span data-ttu-id="f9149-137">- 선택한 프로젝트 작업만</span><span class="sxs-lookup"><span data-stu-id="f9149-137">- Selected project tasks only</span></span></br><span data-ttu-id="f9149-138">이 필드의 공백 값은 **모든 프로젝트 작업** 옵션과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="f9149-139">프로젝트 페이지에서 **선택한 프로젝트 작업만** 선택하면 **작업 청구 설정** 탭을 사용하면 특정 작업을 선택하여 이 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="f9149-140">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-141">시간 포함</span><span class="sxs-lookup"><span data-stu-id="f9149-141">Include Time</span></span> | <span data-ttu-id="f9149-142">**예**/**아니요** 값은 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 견적 라인의 견적에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-143">**아니요** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-144">**예** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f9149-145">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-146">경비 포함</span><span class="sxs-lookup"><span data-stu-id="f9149-146">Include Expense</span></span> | <span data-ttu-id="f9149-147">**예**/**아니요** 값은 선택한 프로젝트의 경비가 이 견적 라인의 견적에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-148">**아니요** 값은 경비 비용이 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-149">**예** 값은 경비 비용이 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f9149-150">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-151">재료 포함</span><span class="sxs-lookup"><span data-stu-id="f9149-151">Include Material</span></span> | <span data-ttu-id="f9149-152">**예**/**아니요** 값은 선택한 프로젝트의 재료 비용이 이 견적 라인의 견적에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-153">**아니요** 값은 재료 비용이 이 견적 라인의 견적에 포함되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-154">**예** 값은 재료 비용이 이 견적 라인의 견적에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f9149-155">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-156">요금 포함</span><span class="sxs-lookup"><span data-stu-id="f9149-156">Include Fee</span></span> | <span data-ttu-id="f9149-157">**예**/**아니요** 값은 선택한 프로젝트의 수수료가 이 견적 라인의 견적에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-158">**아니요** 값은 수수료가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f9149-159">**예** 값은 수수료가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f9149-160">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-161">견적 금액</span><span class="sxs-lookup"><span data-stu-id="f9149-161">Quoted Amount</span></span> | <span data-ttu-id="f9149-162">이 프로젝트 기반 견적 라인에서 예측된 모든 작업에 대해 고객에게 견적될 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="f9149-163">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 **고객 예산** 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="f9149-164">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 금액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="f9149-165">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-166">예상 세금</span><span class="sxs-lookup"><span data-stu-id="f9149-166">Estimated Tax</span></span> | <span data-ttu-id="f9149-167">사용자가 견적 라인에 예상 세액을 추가할 수 있는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="f9149-168">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 세액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="f9149-169">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-170">세금 공제 후 견적 금액</span><span class="sxs-lookup"><span data-stu-id="f9149-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="f9149-171">이 필드는 세금 공제 후 견적 라인 금액이며 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="f9149-172">이 필드의 금액은 *견적 금액 + 세금* 으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="f9149-173">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-174">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="f9149-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="f9149-175">이 필드는 편집 가능하며 **시간 및 재료** 청구 방법이 있는 프로젝트 기반 견적 라인에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="f9149-176">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f9149-177">고객 예산</span><span class="sxs-lookup"><span data-stu-id="f9149-177">Customer Budget</span></span> | <span data-ttu-id="f9149-178">이 필드는 편집 가능하며 영업 기회에서 견적이 생성된 경우 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="f9149-179">이 값은 견적이 성사될 때 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="f9149-180">프로젝트 기반 견적 라인의 일반 탭에 있는 필드에 대한 유효성 검사 규칙</span><span class="sxs-lookup"><span data-stu-id="f9149-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="f9149-181">**규칙 1**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트가 견적 라인에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="f9149-182">**규칙 2**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 프로젝트 기반 견적 라인 하나에만 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="f9149-183">**규칙 3**: **포함된 작업** 필드가 **선택한 프로젝트 작업만** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 여러 프로젝트 기반 견적 라인에 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="f9149-184">**규칙 4**: 영업 기회에 여러 견적이 있는 경우 모두 동일한 프로젝트를 참조하고 동일한 트랜잭션 클래스를 포함하는 서로 다른 견적의 견적 라인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="f9149-185">**규칙 5**: 견적이 동일한 영업 기회에 속하지 않는 경우 동일한 프로젝트 및 트랜잭션 클래스를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="f9149-186">
                    <strong>영업 기회</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="f9149-187">
                    <strong>견적</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="f9149-188">
                    <strong>견적 라인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="f9149-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="f9149-190">
                    <strong>포함된 작업</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="f9149-191">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="f9149-192">
                    <strong>경비 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="f9149-193">
                    <strong>재료 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="f9149-194">
                    <strong>포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="f9149-195">
                    <strong>금액</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="f9149-196">
                    <strong>유효/유효하지 않음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="f9149-197">
                    <strong>원인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9149-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-198">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-199">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-200">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-201">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-202">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-203">네</span><span class="sxs-lookup"><span data-stu-id="f9149-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-204">네</span><span class="sxs-lookup"><span data-stu-id="f9149-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-205">네</span><span class="sxs-lookup"><span data-stu-id="f9149-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-206">네</span><span class="sxs-lookup"><span data-stu-id="f9149-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-207">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="f9149-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-208">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="f9149-208">Violation of Rule #2.</span></span> <span data-ttu-id="f9149-209">P1 프로젝트의 시간, 경비 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-210">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-211">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-212">QL2</span><span class="sxs-lookup"><span data-stu-id="f9149-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-213">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-214">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-215">네</span><span class="sxs-lookup"><span data-stu-id="f9149-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-216">네</span><span class="sxs-lookup"><span data-stu-id="f9149-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-217">네</span><span class="sxs-lookup"><span data-stu-id="f9149-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-218">네</span><span class="sxs-lookup"><span data-stu-id="f9149-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-219">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-220">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-221">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-222">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-223">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-224">네</span><span class="sxs-lookup"><span data-stu-id="f9149-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-225">없음</span><span class="sxs-lookup"><span data-stu-id="f9149-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-226">네</span><span class="sxs-lookup"><span data-stu-id="f9149-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-227">네</span><span class="sxs-lookup"><span data-stu-id="f9149-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-228">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="f9149-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-229">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="f9149-229">Violation of Rule #2.</span></span> <span data-ttu-id="f9149-230">P1 프로젝트의 시간, 재료 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-231">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-232">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-233">QL2</span><span class="sxs-lookup"><span data-stu-id="f9149-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-234">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-235">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-236">네</span><span class="sxs-lookup"><span data-stu-id="f9149-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-237">네</span><span class="sxs-lookup"><span data-stu-id="f9149-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-238">네</span><span class="sxs-lookup"><span data-stu-id="f9149-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-239">네</span><span class="sxs-lookup"><span data-stu-id="f9149-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-240">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-241">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-242">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-243">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-244">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-245">네</span><span class="sxs-lookup"><span data-stu-id="f9149-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-246">없음</span><span class="sxs-lookup"><span data-stu-id="f9149-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-247">네</span><span class="sxs-lookup"><span data-stu-id="f9149-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-248">네</span><span class="sxs-lookup"><span data-stu-id="f9149-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-249">유효함</span><span class="sxs-lookup"><span data-stu-id="f9149-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-250">P1 프로젝트의 시간, 재료 및 요금은 QL1에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="f9149-251">P1 프로젝트의 경비는 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="f9149-252">각 견적 라인에 포함되는 내용이 중복되지 않으므로 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-253">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-254">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-255">QL2</span><span class="sxs-lookup"><span data-stu-id="f9149-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-256">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-257">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-258">없음</span><span class="sxs-lookup"><span data-stu-id="f9149-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-259">네</span><span class="sxs-lookup"><span data-stu-id="f9149-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-260">없음</span><span class="sxs-lookup"><span data-stu-id="f9149-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-261">없음</span><span class="sxs-lookup"><span data-stu-id="f9149-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-262">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-263">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-264">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-265">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-266">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="f9149-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-267">네</span><span class="sxs-lookup"><span data-stu-id="f9149-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-268">네</span><span class="sxs-lookup"><span data-stu-id="f9149-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-269">네</span><span class="sxs-lookup"><span data-stu-id="f9149-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-270">네</span><span class="sxs-lookup"><span data-stu-id="f9149-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-271">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="f9149-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-272">규칙 #2의 위반</span><span class="sxs-lookup"><span data-stu-id="f9149-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="f9149-273">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 재료, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="f9149-274">CL2에는 전체 프로젝트 P1에 대한 시간, 경비 및 요금이 포함되므로 C1에 포함된 내용과 겹칩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-275">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-276">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-277">QL2</span><span class="sxs-lookup"><span data-stu-id="f9149-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-278">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-279">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="f9149-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-280">네</span><span class="sxs-lookup"><span data-stu-id="f9149-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-281">네</span><span class="sxs-lookup"><span data-stu-id="f9149-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-282">네</span><span class="sxs-lookup"><span data-stu-id="f9149-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-283">네</span><span class="sxs-lookup"><span data-stu-id="f9149-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-284">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-285">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-286">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-287">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-288">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="f9149-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-289">네</span><span class="sxs-lookup"><span data-stu-id="f9149-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-290">네</span><span class="sxs-lookup"><span data-stu-id="f9149-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-291">네</span><span class="sxs-lookup"><span data-stu-id="f9149-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-292">네</span><span class="sxs-lookup"><span data-stu-id="f9149-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-293">유효함</span><span class="sxs-lookup"><span data-stu-id="f9149-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-294">규칙 3번에 따라</span><span class="sxs-lookup"><span data-stu-id="f9149-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="f9149-295">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 재료, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f9149-296">Q2에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 재료, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f9149-297">유일한 추가 유효성 검사는 QL2의 작업 하위 집합과 다른 QL1 작업의 하위 집합을 중심으로 중복이 없는지 확인하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="f9149-298">이것은 작업이 연관될 때 시스템에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-299">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-300">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-301">QL2</span><span class="sxs-lookup"><span data-stu-id="f9149-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-302">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-303">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="f9149-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-304">네</span><span class="sxs-lookup"><span data-stu-id="f9149-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-305">네</span><span class="sxs-lookup"><span data-stu-id="f9149-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-306">네</span><span class="sxs-lookup"><span data-stu-id="f9149-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-307">네</span><span class="sxs-lookup"><span data-stu-id="f9149-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-308">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-309">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-310">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-311">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-312">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="f9149-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-313">네</span><span class="sxs-lookup"><span data-stu-id="f9149-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-314">네</span><span class="sxs-lookup"><span data-stu-id="f9149-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-315">네</span><span class="sxs-lookup"><span data-stu-id="f9149-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-316">네</span><span class="sxs-lookup"><span data-stu-id="f9149-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-317">유효함</span><span class="sxs-lookup"><span data-stu-id="f9149-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-318">규칙 5번에 따라 Q1 및 Q2는 동일한 영업 기회에 대한 두 개의 견적이므로 둘 다 프로젝트의 동일한 구성 요소를 추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-319">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-320">2분기</span><span class="sxs-lookup"><span data-stu-id="f9149-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-321">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-322">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-323">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="f9149-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-324">네</span><span class="sxs-lookup"><span data-stu-id="f9149-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-325">네</span><span class="sxs-lookup"><span data-stu-id="f9149-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-326">네</span><span class="sxs-lookup"><span data-stu-id="f9149-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-327">네</span><span class="sxs-lookup"><span data-stu-id="f9149-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-328">O1</span><span class="sxs-lookup"><span data-stu-id="f9149-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-329">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-330">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-331">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-332">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="f9149-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-333">네</span><span class="sxs-lookup"><span data-stu-id="f9149-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-334">네</span><span class="sxs-lookup"><span data-stu-id="f9149-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-335">네</span><span class="sxs-lookup"><span data-stu-id="f9149-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-336">네</span><span class="sxs-lookup"><span data-stu-id="f9149-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-337">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="f9149-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9149-338">규칙 4번에 따라 Q1 및 Q2는 다른 영업 기회에 대한 두 개의 견적이므로 동일한 프로젝트의 동일한 구성 요소를 추정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f9149-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="f9149-339">O2</span><span class="sxs-lookup"><span data-stu-id="f9149-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="f9149-340">1분기</span><span class="sxs-lookup"><span data-stu-id="f9149-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="f9149-341">QL1</span><span class="sxs-lookup"><span data-stu-id="f9149-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-342">P1</span><span class="sxs-lookup"><span data-stu-id="f9149-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="f9149-343">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="f9149-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="f9149-344">네</span><span class="sxs-lookup"><span data-stu-id="f9149-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="f9149-345">네</span><span class="sxs-lookup"><span data-stu-id="f9149-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f9149-346">네</span><span class="sxs-lookup"><span data-stu-id="f9149-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f9149-347">네</span><span class="sxs-lookup"><span data-stu-id="f9149-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
