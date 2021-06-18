---
title: 프로젝트 견적 라인 개요
description: 이 항목은 프로젝트 작업을 위한 프로젝트 견적 라인 사용에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996304"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="09342-103">프로젝트 견적 라인 개요</span><span class="sxs-lookup"><span data-stu-id="09342-103">Project quote lines overview</span></span>

<span data-ttu-id="09342-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="09342-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="09342-105">프로젝트 기반 견적 라인은 계약에 대한 프로젝트 작업을 추정하는 데 도움이 되도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="09342-106">프로젝트 기반 견적 라인의 구조는 다음 개념으로 프로젝트 견적을 위해 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="09342-107">청구 방법</span><span class="sxs-lookup"><span data-stu-id="09342-107">Billing Method</span></span>
- <span data-ttu-id="09342-108">프로젝트 매핑</span><span class="sxs-lookup"><span data-stu-id="09342-108">Project Mapping</span></span>
- <span data-ttu-id="09342-109">포함된 트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="09342-109">Included Transaction classes</span></span>
- <span data-ttu-id="09342-110">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="09342-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="09342-111">청구 가능성 설정</span><span class="sxs-lookup"><span data-stu-id="09342-111">Chargeability setup</span></span>
- <span data-ttu-id="09342-112">견적 라인 세부 정보를 사용한 추정</span><span class="sxs-lookup"><span data-stu-id="09342-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="09342-113">견적 라인 고객</span><span class="sxs-lookup"><span data-stu-id="09342-113">Quote line Customers</span></span>

<span data-ttu-id="09342-114">다음 표는 프로젝트 기반 견적 라인의 **일반** 탭의 필드에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="09342-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="09342-115">이 필드는 프로젝트 작업에 대한 상세하고 기초적인 추정을 위한 기초를 설정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="09342-116">**필드**</span><span class="sxs-lookup"><span data-stu-id="09342-116">**Field**</span></span> | <span data-ttu-id="09342-117">**설명**</span><span class="sxs-lookup"><span data-stu-id="09342-117">**Description**</span></span> | <span data-ttu-id="09342-118">**다운스트림 영향**</span><span class="sxs-lookup"><span data-stu-id="09342-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09342-119">Name</span><span class="sxs-lookup"><span data-stu-id="09342-119">Name</span></span> | <span data-ttu-id="09342-120">예상되는 견적의 개별 구성 요소를 식별하는 데 도움이 되는 견적 라인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09342-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="09342-121">견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-122">청구 방법</span><span class="sxs-lookup"><span data-stu-id="09342-122">Billing Method</span></span> | <span data-ttu-id="09342-123">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="09342-124">이 필드에는 Dynamics 365 Project Operations에서 지원하는 두 가지 주요 계약 모델이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="09342-125">- 고정 가격</span><span class="sxs-lookup"><span data-stu-id="09342-125">- Fixed price</span></span></br><span data-ttu-id="09342-126">- 시간 및 재료.</span><span class="sxs-lookup"><span data-stu-id="09342-126">- Time and material.</span></span>| <span data-ttu-id="09342-127">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-128">Project</span><span class="sxs-lookup"><span data-stu-id="09342-128">Project</span></span> | <span data-ttu-id="09342-129">이 옵션 필드를 사용하여이 계약에 대한 작업을 제공하는 데 사용할 프로젝트를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="09342-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="09342-130">프로젝트가 견적 라인에 매핑되면 청구 가능한 작업을 설정하고 견적 라인 세부 정보로 견적 라인에 프로젝트 기반 견적을 가져오는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="09342-131">프로젝트가 프로젝트 기반 견적 라인에 매핑되지 않은 경우 각 견적 라인 세부 정보를 생성하여 견적을 수동으로 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09342-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="09342-132">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-133">시간 포함</span><span class="sxs-lookup"><span data-stu-id="09342-133">Include Time</span></span> | <span data-ttu-id="09342-134">**예**/**아니요** 플래그는 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-135">**아니요** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-136">**예** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="09342-137">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-138">경비 포함</span><span class="sxs-lookup"><span data-stu-id="09342-138">Include Expense</span></span> | <span data-ttu-id="09342-139">**예**/**아니요** 플래그는 선택한 프로젝트의 경비 비용이 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-140">**아니요** 값은 경비 비용이 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-141">**예** 값은 경비 비용이 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="09342-142">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-143">요금 포함</span><span class="sxs-lookup"><span data-stu-id="09342-143">Include Fee</span></span> | <span data-ttu-id="09342-144">**예**/**아니요** 플래그는 선택한 프로젝트의 수수료가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-145">**아니요** 값은 수수료가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="09342-146">**예** 값은 수수료가 이 견적 라인의 추정에 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09342-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="09342-147">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-148">견적 금액</span><span class="sxs-lookup"><span data-stu-id="09342-148">Quoted Amount</span></span> | <span data-ttu-id="09342-149">이 프로젝트 기반 견적 라인에서 예측된 모든 작업에 대해 고객에게 견적될 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="09342-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="09342-150">영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 **고객 예산** 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="09342-151">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 금액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="09342-152">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-153">예상 세금</span><span class="sxs-lookup"><span data-stu-id="09342-153">Estimated Tax</span></span> | <span data-ttu-id="09342-154">사용자가 견적 라인에 예상 세액을 추가할 수 있는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="09342-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="09342-155">프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 세액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="09342-156">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-157">세금 공제 후 견적 금액</span><span class="sxs-lookup"><span data-stu-id="09342-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="09342-158">이 필드는 세금 공제 후 견적 라인 금액이며 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="09342-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="09342-159">이 필드의 금액은 *견적 금액 + 세금* 으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="09342-160">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-161">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="09342-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="09342-162">이 필드는 편집 가능하며 **시간 및 재료** 청구 방법이 있는 프로젝트 기반 견적 라인에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="09342-163">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="09342-164">고객 예산</span><span class="sxs-lookup"><span data-stu-id="09342-164">Customer Budget</span></span> | <span data-ttu-id="09342-165">이 필드는 편집 가능하며 영업 기회에서 견적이 생성된 경우 영업 기회 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="09342-166">이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="09342-167">프로젝트 기반 견적 라인의 일반 탭에 있는 필드에 대한 유효성 검사 규칙</span><span class="sxs-lookup"><span data-stu-id="09342-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="09342-168">**규칙 1**: 선택한 프로젝트의 특정 트랜잭션 분류는 견적의 하나의 프로젝트 기반 견적 라인에만 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="09342-169">**규칙 2**: 영업 기회에 여러 견적이 있는 경우 모두 동일한 프로젝트를 참조하고 동일한 트랜잭션 클래스를 포함하는 서로 다른 견적의 견적 라인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="09342-170">**규칙 3**: 견적이 동일한 영업 기회에 속하지 않는 경우 동일한 프로젝트 및 트랜잭션 클래스를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="09342-171">
                    <strong>영업 기회</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="09342-172">
                    <strong>견적</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="09342-173">
                    <strong>견적 라인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="09342-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="09342-175">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="09342-176">
                    <strong>경비 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="09342-177">
                    <strong>포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="09342-178">
                    <strong>요금</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="09342-179">
                    <strong>유효/유효하지 않음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="09342-180">
                    <strong>원인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09342-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-181">O1</span><span class="sxs-lookup"><span data-stu-id="09342-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-182">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-183">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-184">P1</span><span class="sxs-lookup"><span data-stu-id="09342-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-185">예</span><span class="sxs-lookup"><span data-stu-id="09342-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-186">예</span><span class="sxs-lookup"><span data-stu-id="09342-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-187">예</span><span class="sxs-lookup"><span data-stu-id="09342-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-188">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="09342-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-189">규칙 #1의 위반.</span><span class="sxs-lookup"><span data-stu-id="09342-189">Violation of Rule #1.</span></span> <span data-ttu-id="09342-190">P1 프로젝트의 시간, 경비 및 요금은 견적 라인 QL1 및 QL2 모두에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-191">O1</span><span class="sxs-lookup"><span data-stu-id="09342-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-192">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-193">QL2</span><span class="sxs-lookup"><span data-stu-id="09342-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-194">P1</span><span class="sxs-lookup"><span data-stu-id="09342-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-195">예</span><span class="sxs-lookup"><span data-stu-id="09342-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-196">예</span><span class="sxs-lookup"><span data-stu-id="09342-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-197">예</span><span class="sxs-lookup"><span data-stu-id="09342-197">Yes</span></span> </p>
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
<span data-ttu-id="09342-198">O1</span><span class="sxs-lookup"><span data-stu-id="09342-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-199">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-200">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-201">P1</span><span class="sxs-lookup"><span data-stu-id="09342-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-202">예</span><span class="sxs-lookup"><span data-stu-id="09342-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-203">없음</span><span class="sxs-lookup"><span data-stu-id="09342-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-204">예</span><span class="sxs-lookup"><span data-stu-id="09342-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-205">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="09342-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-206">규칙 #1의 위반.</span><span class="sxs-lookup"><span data-stu-id="09342-206">Violation of Rule #1.</span></span> <span data-ttu-id="09342-207">P1 프로젝트의 시간 및 요금은 견적 라인 QL1 및 QL2 모두에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-208">O1</span><span class="sxs-lookup"><span data-stu-id="09342-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-209">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-210">QL2</span><span class="sxs-lookup"><span data-stu-id="09342-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-211">P1</span><span class="sxs-lookup"><span data-stu-id="09342-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-212">예</span><span class="sxs-lookup"><span data-stu-id="09342-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-213">예</span><span class="sxs-lookup"><span data-stu-id="09342-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-214">예</span><span class="sxs-lookup"><span data-stu-id="09342-214">Yes</span></span> </p>
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
<span data-ttu-id="09342-215">O1</span><span class="sxs-lookup"><span data-stu-id="09342-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-216">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-217">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-218">P1</span><span class="sxs-lookup"><span data-stu-id="09342-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-219">예</span><span class="sxs-lookup"><span data-stu-id="09342-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-220">없음</span><span class="sxs-lookup"><span data-stu-id="09342-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-221">예</span><span class="sxs-lookup"><span data-stu-id="09342-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-222">유효</span><span class="sxs-lookup"><span data-stu-id="09342-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="09342-223">P1 프로젝트의 시간 및 수수료는 QL1에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="09342-224">P1 프로젝트의 경비는 QL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="09342-225">각 견적 라인에 포함되는 내용이 겹치지 않으므로 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="09342-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-226">O1</span><span class="sxs-lookup"><span data-stu-id="09342-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-227">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-228">QL2</span><span class="sxs-lookup"><span data-stu-id="09342-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-229">P1</span><span class="sxs-lookup"><span data-stu-id="09342-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-230">없음</span><span class="sxs-lookup"><span data-stu-id="09342-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-231">예</span><span class="sxs-lookup"><span data-stu-id="09342-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-232">없음</span><span class="sxs-lookup"><span data-stu-id="09342-232">No</span></span> </p>
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
<span data-ttu-id="09342-233">O1</span><span class="sxs-lookup"><span data-stu-id="09342-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-234">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-235">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-236">P1</span><span class="sxs-lookup"><span data-stu-id="09342-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-237">예</span><span class="sxs-lookup"><span data-stu-id="09342-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-238">예</span><span class="sxs-lookup"><span data-stu-id="09342-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-239">예</span><span class="sxs-lookup"><span data-stu-id="09342-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-240">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="09342-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-241">위 규칙 #1의 위반.</span><span class="sxs-lookup"><span data-stu-id="09342-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="09342-242">Q1에는 전체 프로젝트 P1에 대한 시간, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="09342-243">QL2에는 전체 프로젝트 P1에 대한 시간, 경비 및 요금이 포함되며 Q1에 포함된 내용과 중복됩니다.</span><span class="sxs-lookup"><span data-stu-id="09342-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-244">O1</span><span class="sxs-lookup"><span data-stu-id="09342-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-245">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-246">QL2</span><span class="sxs-lookup"><span data-stu-id="09342-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-247">P1</span><span class="sxs-lookup"><span data-stu-id="09342-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-248">예</span><span class="sxs-lookup"><span data-stu-id="09342-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-249">예</span><span class="sxs-lookup"><span data-stu-id="09342-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-250">예</span><span class="sxs-lookup"><span data-stu-id="09342-250">Yes</span></span> </p>
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
<span data-ttu-id="09342-251">O1</span><span class="sxs-lookup"><span data-stu-id="09342-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-252">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-253">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-254">P1</span><span class="sxs-lookup"><span data-stu-id="09342-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-255">예</span><span class="sxs-lookup"><span data-stu-id="09342-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-256">예</span><span class="sxs-lookup"><span data-stu-id="09342-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-257">예</span><span class="sxs-lookup"><span data-stu-id="09342-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="09342-258">유효</span><span class="sxs-lookup"><span data-stu-id="09342-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-259">규칙 #2에 따라 Q1 및 Q2는 동일한 영업 기회에 대한 두 개의 견적이므로 둘 다 프로젝트의 동일한 구성 요소를 추정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-260">O1</span><span class="sxs-lookup"><span data-stu-id="09342-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-261">2분기</span><span class="sxs-lookup"><span data-stu-id="09342-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-262">Q2의 QL1</span><span class="sxs-lookup"><span data-stu-id="09342-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-263">P1</span><span class="sxs-lookup"><span data-stu-id="09342-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-264">예</span><span class="sxs-lookup"><span data-stu-id="09342-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-265">예</span><span class="sxs-lookup"><span data-stu-id="09342-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-266">예</span><span class="sxs-lookup"><span data-stu-id="09342-266">Yes</span></span> </p>
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
<span data-ttu-id="09342-267">O1</span><span class="sxs-lookup"><span data-stu-id="09342-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-268">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-269">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-270">P1</span><span class="sxs-lookup"><span data-stu-id="09342-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-271">예</span><span class="sxs-lookup"><span data-stu-id="09342-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-272">예</span><span class="sxs-lookup"><span data-stu-id="09342-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-273">예</span><span class="sxs-lookup"><span data-stu-id="09342-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="09342-274">유효</span><span class="sxs-lookup"><span data-stu-id="09342-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="09342-275">규칙 #2에 따라 Q1 및 Q2는 다른 영업 기회에 대한 두 개의 견적이므로 같은 프로젝트의 동일한 구성 요소를 추정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="09342-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="09342-276">O2</span><span class="sxs-lookup"><span data-stu-id="09342-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="09342-277">1분기</span><span class="sxs-lookup"><span data-stu-id="09342-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-278">QL1</span><span class="sxs-lookup"><span data-stu-id="09342-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-279">P1</span><span class="sxs-lookup"><span data-stu-id="09342-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-280">예</span><span class="sxs-lookup"><span data-stu-id="09342-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="09342-281">예</span><span class="sxs-lookup"><span data-stu-id="09342-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="09342-282">예</span><span class="sxs-lookup"><span data-stu-id="09342-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="09342-283">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="09342-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
