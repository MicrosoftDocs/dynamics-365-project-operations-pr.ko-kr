---
title: 프로젝트 기반 계약 내용 개요
description: 이 항목은 프로젝트 기반 계약 내용 작업에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858166"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="56901-103">프로젝트 기반 계약 내용 개요</span><span class="sxs-lookup"><span data-stu-id="56901-103">Project-based contract lines overview</span></span>

<span data-ttu-id="56901-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="56901-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="56901-105">Dynamics 365 Project Operations의 프로젝트 기반 계약 내용은 계약에 대한 프로젝트 작업의 특정 구성 요소에 대한 추정 및 청구 계약을 유지하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="56901-106">프로젝트 기반 계약 내용의 구조는 다음 개념으로 프로젝트 추정 및 청구 시나리오에 대해 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="56901-107">청구 방법</span><span class="sxs-lookup"><span data-stu-id="56901-107">Billing method</span></span>
- <span data-ttu-id="56901-108">프로젝트 및 작업 매핑</span><span class="sxs-lookup"><span data-stu-id="56901-108">Project and task mapping</span></span>
- <span data-ttu-id="56901-109">포함된 트랜잭션 클래스</span><span class="sxs-lookup"><span data-stu-id="56901-109">Included transaction classes</span></span>
- <span data-ttu-id="56901-110">초과 안 함 한도</span><span class="sxs-lookup"><span data-stu-id="56901-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="56901-111">청구 가능성 설정</span><span class="sxs-lookup"><span data-stu-id="56901-111">Chargeability setup</span></span>
- <span data-ttu-id="56901-112">계약 내용 세부 정보를 사용하여 추정</span><span class="sxs-lookup"><span data-stu-id="56901-112">Estimates using contract line details</span></span>
- <span data-ttu-id="56901-113">계약 내용 고객</span><span class="sxs-lookup"><span data-stu-id="56901-113">Contract line customers</span></span>

<span data-ttu-id="56901-114">다음 표에는 프로젝트 기반 작업에 대한 세부적이고 기초적인 추정 및 청구 약정에 대한 기반을 설정하는 데 도움이 되는 프로젝트 기반 계약 내용의 **일반** 탭에 있는 필드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="56901-115">필드</span><span class="sxs-lookup"><span data-stu-id="56901-115">Field</span></span> | <span data-ttu-id="56901-116">설명</span><span class="sxs-lookup"><span data-stu-id="56901-116">Description</span></span> | <span data-ttu-id="56901-117">다운스트림 영향</span><span class="sxs-lookup"><span data-stu-id="56901-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="56901-118">**이름**</span><span class="sxs-lookup"><span data-stu-id="56901-118">**Name**</span></span> | <span data-ttu-id="56901-119">계약 내용의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-119">Name of the contract line.</span></span> <span data-ttu-id="56901-120">이는 추정되는 계약의 개별 구성 요소를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="56901-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="56901-121">견적에서 생성된 프로젝트 계약의 경우 이 값은 프로젝트 기반 견적 라인의 해당 값에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="56901-122">송장이 생성될 때 이 계약 내용에서 생성된 프로젝트 송장 라인에 복사된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="56901-123">**청구 방법**</span><span class="sxs-lookup"><span data-stu-id="56901-123">**Billing Method**</span></span> | <span data-ttu-id="56901-124">견적에서 생성된 프로젝트 계약에서는 이 값은 견적 라인의 해당 값에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="56901-125">이것은 Project Operations에서 지원하는 두 가지 주요 계약 모델을 나타내는 옵션 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="56901-126">- **고정 가격**</span><span class="sxs-lookup"><span data-stu-id="56901-126">- **Fixed Price**</span></span></br><span data-ttu-id="56901-127">- **시간 및 재료**</span><span class="sxs-lookup"><span data-stu-id="56901-127">- **Time and Material**</span></span> | <span data-ttu-id="56901-128">참조된 계약 내용의 청구 방법에 따라 실제 트랜잭션이 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="56901-129">실제가 참조하는 계약 내용에 시간 및 재료 청구 방법이 있는 경우 비용 및 미청구 판매 실제 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="56901-130">실제가 참조하는 계약 내용에 고정 가격 청구 방법이 있는 경우 실제 비용만 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="56901-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="56901-131">**Project**</span></span> | <span data-ttu-id="56901-132">이 참여에 대한 작업을 제공하는 데 사용될 프로젝트를 식별하려면 이 필드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="56901-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="56901-133">이 값은 **포함된 작업** 및 **포함된 트랜잭션 클래스** 와 함께 사용되어 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="56901-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="56901-134">**포함된 작업**</span><span class="sxs-lookup"><span data-stu-id="56901-134">**Included Tasks**</span></span> | <span data-ttu-id="56901-135">이 계약 내용에 선택한 프로젝트에 대한 모든 프로젝트 작업이 포함되는지 아니면 작업의 하위 집합만 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="56901-136">이는 다음과 같은 가능한 값이 있는 옵션 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="56901-137">- **모든 프로젝트 작업**</span><span class="sxs-lookup"><span data-stu-id="56901-137">- **All Project Tasks**</span></span></br><span data-ttu-id="56901-138">- **선택한 프로젝트 작업만**.</span><span class="sxs-lookup"><span data-stu-id="56901-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="56901-139">이 필드의 빈 값은 **모든 프로젝트 작업** 을 선택하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="56901-140">**선택한 작업만** 을 선택하면 **프로젝트** 페이지의 **작업 청구 설정** 탭에서 특정 작업을 선택하여 이 계약 라인에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="56901-141">이 값은 **프로젝트** 및 **포함된 트랜잭션** 분류와 함께 사용되어 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="56901-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="56901-142">**시간 포함**</span><span class="sxs-lookup"><span data-stu-id="56901-142">**Include Time**</span></span> | <span data-ttu-id="56901-143">**예**/**아니요** 값은 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 계약 내용에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="56901-144">**아니요** 값은 시간 트랜잭션 또는 인건비가 이 계약 내용에 포함되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="56901-145">**예** 값은 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="56901-146">이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="56901-147">**경비 포함**</span><span class="sxs-lookup"><span data-stu-id="56901-147">**Include Expense**</span></span> | <span data-ttu-id="56901-148">**예**/**아니요** 값은 선택한 프로젝트의 경비가 이 계약 내용에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="56901-149">**아니요** 값은 경비가 이 계약 내용에 포함되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="56901-150">**예** 값은 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="56901-151">이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="56901-152">**재료 포함**</span><span class="sxs-lookup"><span data-stu-id="56901-152">**Include Materials**</span></span> | <span data-ttu-id="56901-153">**예**/**아니요** 값은 선택한 프로젝트의 재료 비용이 계약 내용에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="56901-154">**아니요** 값은 재료 비용이 이 계약 내용의 견적에 포함되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="56901-155">**예** 값은 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="56901-156">이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="56901-157">**요금 포함**</span><span class="sxs-lookup"><span data-stu-id="56901-157">**Include Fee**</span></span> | <span data-ttu-id="56901-158">**예**/**아니요** 값은 선택한 프로젝트의 요금이 이 계약 내용에 포함되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="56901-159">**아니요** 값은 요금이 이 계약 내용에 포함되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="56901-160">**예** 값은 포함됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56901-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="56901-161">이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="56901-162">**계약 금액**</span><span class="sxs-lookup"><span data-stu-id="56901-162">**Contracted Amount**</span></span> | <span data-ttu-id="56901-163">고정 가격 계약 내용에서 이 금액은 이 계약 내용과 연관된 모든 작업 구성 요소에 대해 고객에게 송장을 발행할 합의된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="56901-164">시간 및 재료 계약 내용에서 이 금액은 이 계약 내용과 연관된 모든 작업 구성 요소에 대해 고객에게 송장을 발행할 추정된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="56901-165">견적에서 생성된 프로젝트 계약에서는 이 값은 견적 라인의 해당 값에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="56901-166">프로젝트 기반 계약 내용에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 계약 내용 상세 내역의 금액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="56901-167">계약 내용에 라인 상세 내역이 있는 경우 라인 상세 내역의 금액을 변경하여 이 값을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="56901-168">고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점에 대한 세전 금액을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="56901-169">**예상 세금**</span><span class="sxs-lookup"><span data-stu-id="56901-169">**Estimated Tax**</span></span> | <span data-ttu-id="56901-170">사용자는 이 필드를 편집하여 계약 내용에 예상 세액을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="56901-171">프로젝트 기반 계약 내용에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 계약 내용 상세 내역의 세액에서 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="56901-172">계약 내용에 라인 상세 내역이 있는 경우 라인 상세 내역의 세액을 변경하여 이 값을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="56901-173">고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점에 대한 세금을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="56901-174">**세금 공제 후 계약 금액**</span><span class="sxs-lookup"><span data-stu-id="56901-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="56901-175">세금 공제 후 내용 계약 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-175">The contract line amount after tax.</span></span> <span data-ttu-id="56901-176">이 필드는 읽기 전용이며 **약정 금액 + 세금** 과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="56901-177">고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="56901-178">**초과 안 함 한도**</span><span class="sxs-lookup"><span data-stu-id="56901-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="56901-179">사용자는 이 필드를 편집할 수 있으며 청구 방법이 시간 및 재료로 설정된 프로젝트 기반 계약 내용에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="56901-180">사용자는 이 필드를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-180">The user can edit this field.</span></span> <span data-ttu-id="56901-181">시간 및 재료에 대한 실제가 시간 및 재료에 대해 이 계약 내용을 참조하는 경우 실제 금액은 계약 내용의 초과 안 함 한도에 대해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="56901-182">이 평가는 이미 소비되고 약정된 금액이 계산된 후에 완료됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="56901-183">**고객 예산**</span><span class="sxs-lookup"><span data-stu-id="56901-183">**Customer Budget**</span></span> | <span data-ttu-id="56901-184">이 필드는 편집 가능하며 견적에서 계약이 생성된 경우 견적 라인의 해당 필드에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="56901-185">이 필드는 정보용으로만 사용되며 다운 스트림 중요도가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="56901-186">프로젝트 기반 계약 내용의 일반 탭에 있는 옵션에 대한 검증 규칙</span><span class="sxs-lookup"><span data-stu-id="56901-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="56901-187">규칙 1: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트의 모든 작업이 계약 내용에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="56901-188">규칙 2: **포함된 작업** 필드가 비어 있거나 명시적으로 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 계약의 하나의 프로젝트 기반 계약 내용에만 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="56901-189">규칙 3: **포함된 작업** 필드가 **선택한 프로젝트 작업만** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 계약의 여러 프로젝트 기반 계약 내용에 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56901-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="56901-190">
                    <strong>계약</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="56901-191">
                    <strong>계약 내용</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56901-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="56901-193">
                    <strong>포함된 작업</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="56901-194">
                    <strong>시간 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="56901-195">
                    <strong>경비 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56901-196">
                    <strong>재료 포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56901-197">
                    <strong>포함</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="56901-198">
                    <strong>금액</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="56901-199">
                    <strong>유효/유효하지 않음</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="56901-200">
                    <strong>원인</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56901-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-201">C1</span><span class="sxs-lookup"><span data-stu-id="56901-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-202">CL1</span><span class="sxs-lookup"><span data-stu-id="56901-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-203">P1</span><span class="sxs-lookup"><span data-stu-id="56901-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-204">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-205">네</span><span class="sxs-lookup"><span data-stu-id="56901-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-206">네</span><span class="sxs-lookup"><span data-stu-id="56901-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-207">네</span><span class="sxs-lookup"><span data-stu-id="56901-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-208">네</span><span class="sxs-lookup"><span data-stu-id="56901-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-209">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="56901-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-210">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="56901-210">Violation of Rule #2.</span></span> <span data-ttu-id="56901-211">P1 프로젝트의 시간, 경비, 재료 및 요금은 견적 라인 CL1 및 QL2 모두에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-212">C1</span><span class="sxs-lookup"><span data-stu-id="56901-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-213">CL2</span><span class="sxs-lookup"><span data-stu-id="56901-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-214">P1</span><span class="sxs-lookup"><span data-stu-id="56901-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-215">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-216">네</span><span class="sxs-lookup"><span data-stu-id="56901-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-217">네</span><span class="sxs-lookup"><span data-stu-id="56901-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-218">네</span><span class="sxs-lookup"><span data-stu-id="56901-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-219">네</span><span class="sxs-lookup"><span data-stu-id="56901-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-220">C1</span><span class="sxs-lookup"><span data-stu-id="56901-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-221">CL1</span><span class="sxs-lookup"><span data-stu-id="56901-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-222">P1</span><span class="sxs-lookup"><span data-stu-id="56901-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-223">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-224">네</span><span class="sxs-lookup"><span data-stu-id="56901-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-225">없음</span><span class="sxs-lookup"><span data-stu-id="56901-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-226">네</span><span class="sxs-lookup"><span data-stu-id="56901-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-227">네</span><span class="sxs-lookup"><span data-stu-id="56901-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-228">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="56901-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-229">규칙 #2의 위반.</span><span class="sxs-lookup"><span data-stu-id="56901-229">Violation of Rule #2.</span></span> <span data-ttu-id="56901-230">P1 프로젝트의 시간, 재료 및 요금은 견적 라인 CL1 및 QL2 모두에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-231">C1</span><span class="sxs-lookup"><span data-stu-id="56901-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-232">CL2</span><span class="sxs-lookup"><span data-stu-id="56901-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-233">P1</span><span class="sxs-lookup"><span data-stu-id="56901-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-234">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-235">네</span><span class="sxs-lookup"><span data-stu-id="56901-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-236">네</span><span class="sxs-lookup"><span data-stu-id="56901-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-237">네</span><span class="sxs-lookup"><span data-stu-id="56901-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-238">네</span><span class="sxs-lookup"><span data-stu-id="56901-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-239">C1</span><span class="sxs-lookup"><span data-stu-id="56901-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-240">CL1</span><span class="sxs-lookup"><span data-stu-id="56901-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-241">P1</span><span class="sxs-lookup"><span data-stu-id="56901-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-242">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-243">네</span><span class="sxs-lookup"><span data-stu-id="56901-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-244">없음</span><span class="sxs-lookup"><span data-stu-id="56901-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-245">네</span><span class="sxs-lookup"><span data-stu-id="56901-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-246">네</span><span class="sxs-lookup"><span data-stu-id="56901-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-247">유효함</span><span class="sxs-lookup"><span data-stu-id="56901-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-248">P1 프로젝트의 시간, 재료 및 요금은 QL1에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="56901-249">P1 프로젝트의 경비는 CL2에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="56901-250">각 계약 내용에 포함되는 내용이 중복되지 않으므로 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="56901-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-251">C1</span><span class="sxs-lookup"><span data-stu-id="56901-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-252">CL2</span><span class="sxs-lookup"><span data-stu-id="56901-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-253">P1</span><span class="sxs-lookup"><span data-stu-id="56901-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-254">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-255">없음</span><span class="sxs-lookup"><span data-stu-id="56901-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-256">네</span><span class="sxs-lookup"><span data-stu-id="56901-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-257">없음</span><span class="sxs-lookup"><span data-stu-id="56901-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-258">없음</span><span class="sxs-lookup"><span data-stu-id="56901-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-259">C1</span><span class="sxs-lookup"><span data-stu-id="56901-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-260">CL1</span><span class="sxs-lookup"><span data-stu-id="56901-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-261">P1</span><span class="sxs-lookup"><span data-stu-id="56901-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-262">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="56901-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-263">네</span><span class="sxs-lookup"><span data-stu-id="56901-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-264">네</span><span class="sxs-lookup"><span data-stu-id="56901-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-265">네</span><span class="sxs-lookup"><span data-stu-id="56901-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-266">네</span><span class="sxs-lookup"><span data-stu-id="56901-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-267">유효하지 않음</span><span class="sxs-lookup"><span data-stu-id="56901-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-268">규칙 #2의 위반</span><span class="sxs-lookup"><span data-stu-id="56901-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="56901-269">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 재료, 경비 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56901-270">CL2에는 전체 프로젝트 P1에 대한 시간, 재료, 경비 및 요금이 포함되므로 C1에 포함된 내용과 겹칩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-271">C1</span><span class="sxs-lookup"><span data-stu-id="56901-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-272">CL2</span><span class="sxs-lookup"><span data-stu-id="56901-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-273">P1</span><span class="sxs-lookup"><span data-stu-id="56901-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-274">빈 템플릿</span><span class="sxs-lookup"><span data-stu-id="56901-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-275">네</span><span class="sxs-lookup"><span data-stu-id="56901-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-276">네</span><span class="sxs-lookup"><span data-stu-id="56901-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-277">네</span><span class="sxs-lookup"><span data-stu-id="56901-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-278">네</span><span class="sxs-lookup"><span data-stu-id="56901-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-279">C1</span><span class="sxs-lookup"><span data-stu-id="56901-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-280">CL1</span><span class="sxs-lookup"><span data-stu-id="56901-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-281">P1</span><span class="sxs-lookup"><span data-stu-id="56901-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-282">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="56901-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-283">네</span><span class="sxs-lookup"><span data-stu-id="56901-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-284">네</span><span class="sxs-lookup"><span data-stu-id="56901-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-285">네</span><span class="sxs-lookup"><span data-stu-id="56901-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-286">네</span><span class="sxs-lookup"><span data-stu-id="56901-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-287">유효함</span><span class="sxs-lookup"><span data-stu-id="56901-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56901-288">규칙 3번에 따라</span><span class="sxs-lookup"><span data-stu-id="56901-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="56901-289">Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비, 재료 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56901-290">Q2에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비, 재료 및 요금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56901-291">유일한 추가 유효성 검사는 QL2의 작업 하위 집합과 다른 CL1 작업의 하위 집합을 중심으로 중복이 없는지 확인하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="56901-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="56901-292">이것은 작업이 연관될 때 시스템에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="56901-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="56901-293">C1</span><span class="sxs-lookup"><span data-stu-id="56901-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="56901-294">CL2</span><span class="sxs-lookup"><span data-stu-id="56901-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-295">P1</span><span class="sxs-lookup"><span data-stu-id="56901-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="56901-296">선택한 작업만</span><span class="sxs-lookup"><span data-stu-id="56901-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-297">네</span><span class="sxs-lookup"><span data-stu-id="56901-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56901-298">네</span><span class="sxs-lookup"><span data-stu-id="56901-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-299">네</span><span class="sxs-lookup"><span data-stu-id="56901-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56901-300">네</span><span class="sxs-lookup"><span data-stu-id="56901-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
