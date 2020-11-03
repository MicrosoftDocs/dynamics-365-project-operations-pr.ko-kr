---
title: 배포 유형 결정
description: 이 항목에서는 회사에 적합한 Project Operations 배포 유형을 결정하는 데 도움이 되는 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080056"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="10e9d-103">배포 유형 결정</span><span class="sxs-lookup"><span data-stu-id="10e9d-103">Determine your deployment type</span></span>

<span data-ttu-id="10e9d-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="10e9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10e9d-105">라이선스를 구매한 후 여기에서 시작하여 [안내식 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="10e9d-106">안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="10e9d-107">설치를 완료하려면 배포 세부 정보를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="10e9d-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="10e9d-108">Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="10e9d-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="10e9d-109">Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="10e9d-110">향후 이러한 고객을 위한 업그레이드 경로가 릴리스될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="10e9d-111">프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="10e9d-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="10e9d-112">프로젝트 관리 및 회계 기능을 사용하는 기존 재무 고객은 그대로 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="10e9d-113">[리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="10e9d-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="10e9d-114">배포 유형</span><span class="sxs-lookup"><span data-stu-id="10e9d-114">Deployment types</span></span>
<span data-ttu-id="10e9d-115">Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="10e9d-116">신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="10e9d-117">[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="10e9d-118">결과는 다음 배포 유형 중 하나로 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="10e9d-119">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="10e9d-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="10e9d-120">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="10e9d-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="10e9d-121">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="10e9d-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="10e9d-122">Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="10e9d-123">예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)에서 재고/생산 주문 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="10e9d-124">Contoso는 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비 재고/리소스 기반 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="10e9d-125">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="10e9d-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="10e9d-126">라이트 배포에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="10e9d-127">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="10e9d-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="10e9d-128">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="10e9d-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="10e9d-129">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="10e9d-129">Unified Resource Management</span></span>
- <span data-ttu-id="10e9d-130">시간 추적</span><span class="sxs-lookup"><span data-stu-id="10e9d-130">Time Tracking</span></span>
- <span data-ttu-id="10e9d-131">기본 경비</span><span class="sxs-lookup"><span data-stu-id="10e9d-131">Basic Expense</span></span>
- <span data-ttu-id="10e9d-132">송장 제안</span><span class="sxs-lookup"><span data-stu-id="10e9d-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="10e9d-133">배포 단계</span><span class="sxs-lookup"><span data-stu-id="10e9d-133">Deployment steps</span></span>
<span data-ttu-id="10e9d-134">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="10e9d-135">이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="10e9d-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="10e9d-136">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="10e9d-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="10e9d-137">리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="10e9d-138">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="10e9d-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="10e9d-139">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="10e9d-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="10e9d-140">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="10e9d-140">Unified Resource Management</span></span>
- <span data-ttu-id="10e9d-141">시간 추적</span><span class="sxs-lookup"><span data-stu-id="10e9d-141">Time Tracking</span></span>
- <span data-ttu-id="10e9d-142">기본 경비</span><span class="sxs-lookup"><span data-stu-id="10e9d-142">Basic Expense</span></span>
- <span data-ttu-id="10e9d-143">전체 경비</span><span class="sxs-lookup"><span data-stu-id="10e9d-143">Full Expense</span></span>
- <span data-ttu-id="10e9d-144">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="10e9d-144">Receipt OCR</span></span>
- <span data-ttu-id="10e9d-145">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="10e9d-145">Full Invoicing</span></span>
- <span data-ttu-id="10e9d-146">수익 인식</span><span class="sxs-lookup"><span data-stu-id="10e9d-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="10e9d-147">배포 단계</span><span class="sxs-lookup"><span data-stu-id="10e9d-147">Deployment steps</span></span>
<span data-ttu-id="10e9d-148">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="10e9d-149">이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="10e9d-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="10e9d-150">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="10e9d-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="10e9d-151">WBS를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="10e9d-151">Project planning using WBS</span></span>
- <span data-ttu-id="10e9d-152">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="10e9d-152">Resource Management</span></span>
- <span data-ttu-id="10e9d-153">시간 추적</span><span class="sxs-lookup"><span data-stu-id="10e9d-153">Time Tracking</span></span>
- <span data-ttu-id="10e9d-154">전체 경비</span><span class="sxs-lookup"><span data-stu-id="10e9d-154">Full Expense</span></span>
- <span data-ttu-id="10e9d-155">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="10e9d-155">Receipt OCR</span></span>
- <span data-ttu-id="10e9d-156">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="10e9d-156">Full Invoicing</span></span>
- <span data-ttu-id="10e9d-157">수익 인식</span><span class="sxs-lookup"><span data-stu-id="10e9d-157">Revenue Recognition</span></span>
- <span data-ttu-id="10e9d-158">생산 주문</span><span class="sxs-lookup"><span data-stu-id="10e9d-158">Production Orders</span></span>
- <span data-ttu-id="10e9d-159">재료 지원</span><span class="sxs-lookup"><span data-stu-id="10e9d-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="10e9d-160">배포 단계</span><span class="sxs-lookup"><span data-stu-id="10e9d-160">Deployment steps</span></span>
<span data-ttu-id="10e9d-161">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="10e9d-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="10e9d-162">이 배포의 경우 [미리 보기 구독 신청](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) 및 [새로운 환경 제공](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="10e9d-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

