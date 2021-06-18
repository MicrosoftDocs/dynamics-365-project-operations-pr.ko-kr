---
title: 프로젝트 기반 영업 기회 관리
description: 이 항목은 프로젝트와 관련된 영업 기회를 다루는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aebff4d3a94735e76bcb9cafd25a058207dae846
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996349"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="89c27-103">프로젝트 기반 영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="89c27-103">Manage project-based opportunities</span></span>

<span data-ttu-id="89c27-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="89c27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89c27-105">프로젝트 기반 회사는 일반적으로 여러 국가 및 지역에 걸쳐 배포를 위해 운영됩니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="89c27-106">프로젝트 실행 및 제공 비용은 제공을 관리하는 지역 또는 부문에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="89c27-107">결과적으로 이것은 거래의 마진에 영향을 미칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="89c27-108">프로젝트 기반 서비스 제공에는 일반적으로 많은 인적 자원 시간, 상당한 출장 비용, 재료비 및 기타 비용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="89c27-109">Dynamics 365 Project Operations의 프로젝트 기반 영업 기회는 Dynamics 365 Sales에 대한 확장으로 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="89c27-110">이 항목은 프로젝트 기반 기업이 프로젝트 기반 영업 기회를 관리하는 데 필요한 추가 기능에 포함된 다양한 필드 및 비즈니스 로직에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="89c27-111">모든 프로젝트 기반 영업 기회 보기</span><span class="sxs-lookup"><span data-stu-id="89c27-111">View all project-based opportunities</span></span>

<span data-ttu-id="89c27-112">모든 프로젝트 기반 영업 기회의 목록은 **영업 기회** 목록 페이지에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="89c27-113">**영업** > **영업 기회** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="89c27-114">**스위처 보기** 를 사용하여 영업 기회의 다른 필터링된 보기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="89c27-115">이러한 보기 및 탐색 옵션을 구성하기 위해 사용자 지정 필터 기준으로 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="89c27-116">이 목록 페이지 또는 세부 사항 페이지에서 프로젝트 영업 기회를 만들거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="89c27-117">프로젝트 기반 거래의 경우 비즈니스 프로세스 흐름</span><span class="sxs-lookup"><span data-stu-id="89c27-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="89c27-118">Project Operations의 프로젝트 기반 거래에 대해 다음 비즈니스 프로세스 흐름이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="89c27-119">잠재 고객 - 영업 기회 비즈니스 프로세스</span><span class="sxs-lookup"><span data-stu-id="89c27-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="89c27-120">영업 기회 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="89c27-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="89c27-121">잠재 고객 - 영업 기회 비즈니스 프로세스</span><span class="sxs-lookup"><span data-stu-id="89c27-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="89c27-122">잠재 고객 - 영업 기회 비즈니스 프로세스는 다음 스테이지를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="89c27-123">단계</span><span class="sxs-lookup"><span data-stu-id="89c27-123">Stage</span></span> | <span data-ttu-id="89c27-124">매핑된 엔티티</span><span class="sxs-lookup"><span data-stu-id="89c27-124">Mapped entity</span></span> | <span data-ttu-id="89c27-125">기능</span><span class="sxs-lookup"><span data-stu-id="89c27-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="89c27-126">우량으로 선별</span><span class="sxs-lookup"><span data-stu-id="89c27-126">Qualify</span></span> | <span data-ttu-id="89c27-127">잠재 고객</span><span class="sxs-lookup"><span data-stu-id="89c27-127">Lead</span></span> | <span data-ttu-id="89c27-128">잠재 고객을 우량으로 선별하여 거래처, 연락처 및 영업 기회를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="89c27-129">전개</span><span class="sxs-lookup"><span data-stu-id="89c27-129">Develop</span></span> | <span data-ttu-id="89c27-130">영업 기회</span><span class="sxs-lookup"><span data-stu-id="89c27-130">Opportunity</span></span> | <span data-ttu-id="89c27-131">관련된 작업, 주요 이해 관계자 및 경쟁에 대한 더 많은 정보를 추가할 수 있는 영업 기회를 개발하십시오.</span><span class="sxs-lookup"><span data-stu-id="89c27-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="89c27-132">제안</span><span class="sxs-lookup"><span data-stu-id="89c27-132">Propose</span></span> | <span data-ttu-id="89c27-133">영업 기회</span><span class="sxs-lookup"><span data-stu-id="89c27-133">Opportunity</span></span> | <span data-ttu-id="89c27-134">제안서를 개발하고 내부 검토 팀의 승인을 받으십시오.</span><span class="sxs-lookup"><span data-stu-id="89c27-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="89c27-135">종료</span><span class="sxs-lookup"><span data-stu-id="89c27-135">Close</span></span> | <span data-ttu-id="89c27-136">영업 기회</span><span class="sxs-lookup"><span data-stu-id="89c27-136">Opportunity</span></span> | <span data-ttu-id="89c27-137">거래를 성사시킬 수 있는 영업 기회를 얻으십시오.</span><span class="sxs-lookup"><span data-stu-id="89c27-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="89c27-138">영업 기회 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="89c27-138">Opportunity sales process</span></span>
<span data-ttu-id="89c27-139">Project Operations의 영업 기회 영업 프로세스는 Sales 응용 프로그램의 영업 기회 영업 프로세스 비즈니스 흐름에 대한 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="89c27-140">이 비즈니스 프로세스는 프로젝트 기반 영업 기회의 다음 단계를 지원하기 위해 기본적으로 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="89c27-141">단계</span><span class="sxs-lookup"><span data-stu-id="89c27-141">Stage</span></span> | <span data-ttu-id="89c27-142">매핑된 엔티티</span><span class="sxs-lookup"><span data-stu-id="89c27-142">Mapped entity</span></span> | <span data-ttu-id="89c27-143">기능</span><span class="sxs-lookup"><span data-stu-id="89c27-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="89c27-144">우량으로 선별</span><span class="sxs-lookup"><span data-stu-id="89c27-144">Qualify</span></span> | <span data-ttu-id="89c27-145">영업 기회</span><span class="sxs-lookup"><span data-stu-id="89c27-145">Opportunity</span></span> | <span data-ttu-id="89c27-146">잠재 고객을 우량으로 선별하여 거래처, 연락처 및 영업 기회를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="89c27-147">제안</span><span class="sxs-lookup"><span data-stu-id="89c27-147">Propose</span></span> | <span data-ttu-id="89c27-148">견적</span><span class="sxs-lookup"><span data-stu-id="89c27-148">Quote</span></span> | <span data-ttu-id="89c27-149">프로젝트 견적을 사용하여 제안서를 개발하고 내부 검토 팀의 승인을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="89c27-150">계약</span><span class="sxs-lookup"><span data-stu-id="89c27-150">Contract</span></span> | <span data-ttu-id="89c27-151">프로젝트 계약</span><span class="sxs-lookup"><span data-stu-id="89c27-151">Project Contract</span></span> | <span data-ttu-id="89c27-152">견적을 받아 계약을 작성하고 프로젝트 실행 및 납품을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="89c27-153">종료</span><span class="sxs-lookup"><span data-stu-id="89c27-153">Close</span></span> | <span data-ttu-id="89c27-154">프로젝트 계약</span><span class="sxs-lookup"><span data-stu-id="89c27-154">Project Contract</span></span> | <span data-ttu-id="89c27-155">작업을 성공적으로 완료하고 프로젝트 계약을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="89c27-156">프로젝트 기반 거래가 잠재 고객으로 시작된 경우 잠재 고객 비즈니스 프로세스가 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="89c27-157">프로젝트 기반 거래가 영업 기회로 시작된 경우 영업 기회 영업 프로세스가 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="89c27-158">비즈니스 프로세스 흐름 제품을 편집하거나 필요에 따라 영업 프로세스를 추적하는 고유한 비즈니스 프로세스 흐름을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89c27-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="89c27-159">비즈니스 프로세스 흐름에 대한 자세한 내용은 [비즈니스 프로세스 흐름 개요](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="89c27-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]