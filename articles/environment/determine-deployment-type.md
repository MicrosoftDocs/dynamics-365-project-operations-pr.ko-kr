---
title: 배포 유형 결정
description: 이 항목에서는 회사에 적합한 Project Operations 배포 유형을 결정하는 데 도움이 되는 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401226"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="0b037-103">배포 유형 결정</span><span class="sxs-lookup"><span data-stu-id="0b037-103">Determine your deployment type</span></span>

<span data-ttu-id="0b037-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="0b037-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b037-105">라이선스를 구매한 후 여기에서 시작하여 [안내식 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="0b037-106">안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="0b037-107">설치를 완료하려면 배포 세부 정보를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0b037-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="0b037-108">Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="0b037-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="0b037-109">Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="0b037-110">2021년 릴리스 웨이브 1에서 이러한 고객을 위한 업그레이드 경로가 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="0b037-111">프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="0b037-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="0b037-112">프로젝트 관리 및 회계 기능을 사용하는 기존 Finance 고객은 그대로 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="0b037-113">[리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0b037-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="0b037-114">배포 유형</span><span class="sxs-lookup"><span data-stu-id="0b037-114">Deployment types</span></span>
<span data-ttu-id="0b037-115">Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="0b037-116">신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="0b037-117">[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="0b037-118">결과는 다음 배포 유형 중 하나로 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="0b037-119">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="0b037-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="0b037-120">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0b037-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="0b037-121">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0b037-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="0b037-122">Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="0b037-123">예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)에서 재고/생산 주문 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="0b037-124">Contoso는 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비 재고/리소스 기반 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="0b037-125">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="0b037-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="0b037-126">라이트 배포에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="0b037-127">Dynamics 365 Sales 애플리케이션 경험을 확장하는 프로젝트의 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="0b037-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="0b037-128">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="0b037-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0b037-129">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="0b037-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0b037-130">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="0b037-130">Unified resource management</span></span>
- <span data-ttu-id="0b037-131">시간 추적</span><span class="sxs-lookup"><span data-stu-id="0b037-131">Time tracking</span></span>
- <span data-ttu-id="0b037-132">기본 경비</span><span class="sxs-lookup"><span data-stu-id="0b037-132">Basic expense</span></span>
- <span data-ttu-id="0b037-133">견적 및 고객 대면 송장 발행</span><span class="sxs-lookup"><span data-stu-id="0b037-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="0b037-134">배포 단계</span><span class="sxs-lookup"><span data-stu-id="0b037-134">Deployment steps</span></span>
<span data-ttu-id="0b037-135">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0b037-136">이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0b037-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="0b037-137">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0b037-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="0b037-138">리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="0b037-139">Dynamics 365 Sales 애플리케이션을 확장하는 프로젝트의 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="0b037-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="0b037-140">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="0b037-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0b037-141">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="0b037-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0b037-142">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="0b037-142">Unified resource management</span></span>
- <span data-ttu-id="0b037-143">시간 추적</span><span class="sxs-lookup"><span data-stu-id="0b037-143">Time tracking</span></span>
- <span data-ttu-id="0b037-144">기본 경비</span><span class="sxs-lookup"><span data-stu-id="0b037-144">Basic expense</span></span>
- <span data-ttu-id="0b037-145">전체 경비</span><span class="sxs-lookup"><span data-stu-id="0b037-145">Full expense</span></span>
- <span data-ttu-id="0b037-146">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="0b037-146">Receipt OCR</span></span>
- <span data-ttu-id="0b037-147">견적 및 고객 대면 송장 발행</span><span class="sxs-lookup"><span data-stu-id="0b037-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="0b037-148">프로젝트의 수익 인식</span><span class="sxs-lookup"><span data-stu-id="0b037-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="0b037-149">배포 단계</span><span class="sxs-lookup"><span data-stu-id="0b037-149">Deployment steps</span></span>
<span data-ttu-id="0b037-150">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0b037-151">이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0b037-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="0b037-152">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0b037-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="0b037-153">WBS를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="0b037-153">Project planning using WBS</span></span>
- <span data-ttu-id="0b037-154">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="0b037-154">Resource Management</span></span>
- <span data-ttu-id="0b037-155">시간 추적</span><span class="sxs-lookup"><span data-stu-id="0b037-155">Time Tracking</span></span>
- <span data-ttu-id="0b037-156">전체 경비</span><span class="sxs-lookup"><span data-stu-id="0b037-156">Full Expense</span></span>
- <span data-ttu-id="0b037-157">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="0b037-157">Receipt OCR</span></span>
- <span data-ttu-id="0b037-158">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="0b037-158">Full Invoicing</span></span>
- <span data-ttu-id="0b037-159">수익 인식</span><span class="sxs-lookup"><span data-stu-id="0b037-159">Revenue Recognition</span></span>
- <span data-ttu-id="0b037-160">생산 주문</span><span class="sxs-lookup"><span data-stu-id="0b037-160">Production Orders</span></span>
- <span data-ttu-id="0b037-161">재료 지원</span><span class="sxs-lookup"><span data-stu-id="0b037-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="0b037-162">배포 단계</span><span class="sxs-lookup"><span data-stu-id="0b037-162">Deployment steps</span></span>
<span data-ttu-id="0b037-163">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b037-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0b037-164">이 배포의 경우 [미리 보기 구독 신청](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) 및 [새로운 환경 제공](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0b037-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

