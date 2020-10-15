---
title: 프로젝트 기반 견적 라인(Pro)
description: 이 항목은 프로젝트 작업에 프로젝트 기반 견적 라인 사용에 대한 정보를 제공합니다. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908343"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="01f6a-104">프로젝트 기반 견적 라인(Pro)</span><span class="sxs-lookup"><span data-stu-id="01f6a-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="01f6a-105">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="01f6a-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="01f6a-106">프로젝트 기반 견적 라인은 계약에 대한 프로젝트 작업을 추정하는 데 도움이 되도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="01f6a-107">프로젝트 기반 견적 라인의 구조는 다음 개념으로 프로젝트 견적을 위해 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="01f6a-108">청구 방법</span><span class="sxs-lookup"><span data-stu-id="01f6a-108">Billing Method</span></span>
- <span data-ttu-id="01f6a-109">프로젝트 및 작업 매핑</span><span class="sxs-lookup"><span data-stu-id="01f6a-109">Project and Task Mapping</span></span>
- <span data-ttu-id="01f6a-110">포함된 트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="01f6a-110">Included Transaction classes</span></span>
- <span data-ttu-id="01f6a-111">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="01f6a-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="01f6a-112">청구 가능성 설정</span><span class="sxs-lookup"><span data-stu-id="01f6a-112">Chargeability setup</span></span>
- <span data-ttu-id="01f6a-113">견적 라인 세부 정보를 사용한 추정</span><span class="sxs-lookup"><span data-stu-id="01f6a-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="01f6a-114">견적 라인 고객</span><span class="sxs-lookup"><span data-stu-id="01f6a-114">Quote line Customers</span></span>

<span data-ttu-id="01f6a-115">다음 표는 프로젝트 기반 견적 라인의 **일반** 탭의 필드에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="01f6a-116">이 필드는 프로젝트 작업에 대한 상세하고 기초적인 추정을 위한 기초를 설정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="01f6a-117">**필드**</span><span class="sxs-lookup"><span data-stu-id="01f6a-117">**Field**</span></span> | <span data-ttu-id="01f6a-118">**관련성, 목적 및 지침**</span><span class="sxs-lookup"><span data-stu-id="01f6a-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="01f6a-119">**다운스트림 영향**</span><span class="sxs-lookup"><span data-stu-id="01f6a-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="01f6a-120">Name</span><span class="sxs-lookup"><span data-stu-id="01f6a-120">Name</span></span> | <span data-ttu-id="01f6a-121">예상되는 견적의 개별 구성 요소를 식별하는 데 도움이 되는 견적 라인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="01f6a-122">견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-123">청구 방법</span><span class="sxs-lookup"><span data-stu-id="01f6a-123">Billing Method</span></span> | <span data-ttu-id="01f6a-124">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="01f6a-125">이 필드에는 Dynamics 365 Project Operations에서 지원하는 두 가지 주요 계약 모델이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="01f6a-126">- 고정 가격</span><span class="sxs-lookup"><span data-stu-id="01f6a-126">- Fixed price</span></span></br><span data-ttu-id="01f6a-127">- 시간 및 재료.</span><span class="sxs-lookup"><span data-stu-id="01f6a-127">- Time and material.</span></span>| <span data-ttu-id="01f6a-128">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-129">Project</span><span class="sxs-lookup"><span data-stu-id="01f6a-129">Project</span></span> | <span data-ttu-id="01f6a-130">이 옵션 필드를 사용하여이 계약에 대한 작업을 제공하는 데 사용할 프로젝트를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="01f6a-131">프로젝트가 견적 라인에 매핑되면 청구 가능한 작업을 설정하고 견적 라인 세부 정보로 견적 라인에 프로젝트 기반 견적을 가져오는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="01f6a-132">프로젝트가 프로젝트 기반 견적 라인에 매핑되지 않은 경우 각 견적 라인 세부 정보를 생성하여 견적을 수동으로 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="01f6a-133">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="01f6a-134">포함된 작업</span><span class="sxs-lookup"><span data-stu-id="01f6a-134">Included Tasks</span></span> | <span data-ttu-id="01f6a-135">이 견적 라인이 선택한 프로젝트의 프로젝트 작업 전체 또는 일부에 사용되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="01f6a-136">이 필드에는 다음 가능한 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-136">This field has the following possible values:</span></span></br><span data-ttu-id="01f6a-137">- 모든 프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="01f6a-137">- All project tasks</span></span></br><span data-ttu-id="01f6a-138">- 선택한 프로젝트 작업만</span><span class="sxs-lookup"><span data-stu-id="01f6a-138">- Selected project tasks only</span></span></br><span data-ttu-id="01f6a-139">이 필드의 공백 값은 **모든 프로젝트 작업** 옵션과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="01f6a-140">프로젝트 페이지에서 **선택한 프로젝트 작업만**이 선택되면 **작업 청구 설정** 탭을 사용하여 특정 작업을 선택하여 이 견적 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="01f6a-141">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-142">시간 포함</span><span class="sxs-lookup"><span data-stu-id="01f6a-142">Include Time</span></span> | <span data-ttu-id="01f6a-143">**예**/**아니요** 플래그는 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-144">**아니요** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-145">**예** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="01f6a-146">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-147">경비 포함</span><span class="sxs-lookup"><span data-stu-id="01f6a-147">Include Expense</span></span> | <span data-ttu-id="01f6a-148">**예**/**아니요** 플래그는 선택한 프로젝트의 경비 비용이 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-149">**아니요** 값은 경비 비용이 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-150">**예** 값은 경비 비용이 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="01f6a-151">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-152">요금 포함</span><span class="sxs-lookup"><span data-stu-id="01f6a-152">Include Fee</span></span> | <span data-ttu-id="01f6a-153">**예**/**아니요** 플래그는 선택한 프로젝트의 수수료가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-154">**아니요** 값은 수수료가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="01f6a-155">**예** 값은 수수료가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="01f6a-156">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-157">견적 금액</span><span class="sxs-lookup"><span data-stu-id="01f6a-157">Quoted Amount</span></span> | <span data-ttu-id="01f6a-158">이 프로젝트 기반 견적 라인에서 예측된 모든 작업에 대해 고객에게 견적될 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="01f6a-159">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 **고객 예산** 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="01f6a-160">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 금액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="01f6a-161">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-162">예상 세금</span><span class="sxs-lookup"><span data-stu-id="01f6a-162">Estimated Tax</span></span> | <span data-ttu-id="01f6a-163">사용자가 견적 라인에 예상 세액을 추가할 수 있는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="01f6a-164">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 세액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="01f6a-165">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-166">세금 공제 후 견적 금액</span><span class="sxs-lookup"><span data-stu-id="01f6a-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="01f6a-167">이 필드는 세금 공제 후 견적 라인 금액이며 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="01f6a-168">이 필드의 금액은 *견적 금액 + 세금*으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="01f6a-169">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-170">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="01f6a-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="01f6a-171">이 필드는 편집 가능하며 **시간 및 재료** 청구 방법이 있는 프로젝트 기반 견적 라인에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="01f6a-172">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="01f6a-173">고객 예산</span><span class="sxs-lookup"><span data-stu-id="01f6a-173">Customer Budget</span></span> | <span data-ttu-id="01f6a-174">이 필드는 편집 가능하며 영업 기회에서 견적이 생성된 경우 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="01f6a-175">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="01f6a-176">프로젝트 기반 견적 라인의 일반 탭에 있는 필드에 대한 유효성 검사 규칙</span><span class="sxs-lookup"><span data-stu-id="01f6a-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="01f6a-177">**규칙 1**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업**으로 설정된 경우 프로젝트가 견적 라인에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="01f6a-178">**규칙 2**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업**으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 프로젝트 기반 견적 라인 하나에만 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="01f6a-179">**규칙 3**: **포함된 작업** 필드가 **선택한 프로젝트 작업만**으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 여러 프로젝트 기반 견적 라인에 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="01f6a-180">**규칙 4**: 영업 기회에 여러 견적이 있는 경우 모두 동일한 프로젝트를 참조하고 동일한 트랜잭션 클래스를 포함하는 서로 다른 견적의 견적 라인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="01f6a-181">**규칙 5**: 견적이 동일한 영업 기회에 속하지 않는 경우 동일한 프로젝트 및 트랜잭션 클래스를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="01f6a-182">
                    <strong>영업 기회</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="01f6a-183">
                    <strong>견적</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="01f6a-184">
                    <strong>견적 라인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="01f6a-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="01f6a-186">
                    <strong>포함된 작업</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="01f6a-187">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="01f6a-188">
                    <strong>경비 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="01f6a-189">
                    <strong>포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="01f6a-190">
                    <strong>금액</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="01f6a-191">
                    <strong>유효/유효하지 않음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="01f6a-192">
                    <strong>원인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="01f6a-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-193">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-194">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-195">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-196">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-197">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-198">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-199">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-200">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-201">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="01f6a-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-202">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="01f6a-202">Violation of Rule #2.</span></span> <span data-ttu-id="01f6a-203">P1 프로젝트의 시간, 경비 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-204">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-205">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-206">QL2</span><span class="sxs-lookup"><span data-stu-id="01f6a-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-207">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-208">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-209">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-210">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-211">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-212">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-213">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-214">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-215">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-216">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-217">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-218">없음</span><span class="sxs-lookup"><span data-stu-id="01f6a-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-219">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-220">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="01f6a-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-221">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="01f6a-221">Violation of Rule #2.</span></span> <span data-ttu-id="01f6a-222">P1 프로젝트의 시간 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-223">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-224">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-225">QL2</span><span class="sxs-lookup"><span data-stu-id="01f6a-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-226">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-227">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-228">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-229">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-230">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-231">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-232">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-233">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-234">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-235">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-236">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-237">없음</span><span class="sxs-lookup"><span data-stu-id="01f6a-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-238">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-239">유효</span><span class="sxs-lookup"><span data-stu-id="01f6a-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="01f6a-240">P1 프로젝트의 시간 및 요금은 QL1에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="01f6a-241">P1 프로젝트의 경비는 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="01f6a-242">각 견적 라인에 포함되는 내용이 겹치지 않으며 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-243">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-244">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-245">QL2</span><span class="sxs-lookup"><span data-stu-id="01f6a-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-246">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-247">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-248">없음</span><span class="sxs-lookup"><span data-stu-id="01f6a-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-249">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-250">없음</span><span class="sxs-lookup"><span data-stu-id="01f6a-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-251">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-252">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-253">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-254">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-255">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="01f6a-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-256">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-257">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-258">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-259">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="01f6a-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-260">위 규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="01f6a-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="01f6a-261">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="01f6a-262">QL2에는 전체 프로젝트 P1에 대한 시간, 경비 및 요금이 포함되며 Q1에 포함된 내용과 중복됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-263">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-264">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-265">QL2</span><span class="sxs-lookup"><span data-stu-id="01f6a-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-266">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-267">비어 있음</span><span class="sxs-lookup"><span data-stu-id="01f6a-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-268">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-269">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-270">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-271">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-272">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-273">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-274">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-275">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="01f6a-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-276">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-277">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-278">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-279">유효</span><span class="sxs-lookup"><span data-stu-id="01f6a-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-280">위 규칙 #3에 따라</span><span class="sxs-lookup"><span data-stu-id="01f6a-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="01f6a-281">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="01f6a-282">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="01f6a-283">유일한 추가 유효성 검사는 QL2의 작업 하위 집합과 다른 QL1의 작업 하위 집합에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="01f6a-284">이렇게 하면 겹치는 부분이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="01f6a-285">이것은 작업이 연관될 때 시스템에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-286">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-287">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-288">QL2</span><span class="sxs-lookup"><span data-stu-id="01f6a-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-289">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-290">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="01f6a-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-291">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-292">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-293">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-294">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-295">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-296">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-297">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-298">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="01f6a-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-299">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-300">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-301">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="01f6a-302">유효</span><span class="sxs-lookup"><span data-stu-id="01f6a-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-303">규칙 #5에 따라 Q1 및 Q2는 동일한 영업 기회에 대한 두 개의 견적이므로 둘 다 프로젝트의 동일한 구성 요소를 추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-304">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-305">2분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-306">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-307">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-308">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="01f6a-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-309">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-310">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-311">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-312">O1</span><span class="sxs-lookup"><span data-stu-id="01f6a-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-313">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-314">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-315">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-316">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="01f6a-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-317">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-318">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-319">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="01f6a-320">유효</span><span class="sxs-lookup"><span data-stu-id="01f6a-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="01f6a-321">규칙 #4에 따라 Q1 및 Q2는 다른 영업 기회에 대한 두 개의 견적이므로 같은 프로젝트의 동일한 구성 요소를 추정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="01f6a-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="01f6a-322">O2</span><span class="sxs-lookup"><span data-stu-id="01f6a-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="01f6a-323">1분기</span><span class="sxs-lookup"><span data-stu-id="01f6a-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-324">QL1</span><span class="sxs-lookup"><span data-stu-id="01f6a-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-325">P1</span><span class="sxs-lookup"><span data-stu-id="01f6a-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="01f6a-326">모든 프로젝트 작업 또는 공백</span><span class="sxs-lookup"><span data-stu-id="01f6a-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-327">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="01f6a-328">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="01f6a-329">예</span><span class="sxs-lookup"><span data-stu-id="01f6a-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="01f6a-330">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="01f6a-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

