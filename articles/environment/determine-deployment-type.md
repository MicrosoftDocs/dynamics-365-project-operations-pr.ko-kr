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
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479572"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="1f69c-103">배포 유형 결정</span><span class="sxs-lookup"><span data-stu-id="1f69c-103">Determine your deployment type</span></span>

<span data-ttu-id="1f69c-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="1f69c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f69c-105">라이선스를 구입한 후 여기에서 시작하여 [안내 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적의 배포 모델을 결정하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="1f69c-106">안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="1f69c-107">설치를 완료하려면 배포 세부 정보를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="1f69c-108">Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="1f69c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="1f69c-109">Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="1f69c-110">2021년 릴리스 웨이브 1에서 이러한 고객을 위한 업그레이드 경로가 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="1f69c-111">프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="1f69c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="1f69c-112">프로젝트 관리 및 회계 기능을 사용하는 기존 Finance 고객은 그대로 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="1f69c-113">[리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="1f69c-114">배포 지역</span><span class="sxs-lookup"><span data-stu-id="1f69c-114">Deployment regions</span></span>
<span data-ttu-id="1f69c-115">Project Operations 배포를 지원하는 지역을 확인하려면 [Dynamics 365 및 Power Platform의 지리적 가용성 보고서](https://dynamics.microsoft.com/en-us/geographic-availability/)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="1f69c-116">**보고서 보기** 를 선택하고 **Dynamics 365 > 운영 앱 > Dynamics 365 Project Operations** 를 확장하고 지원되는 지역을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="1f69c-117">배포 유형</span><span class="sxs-lookup"><span data-stu-id="1f69c-117">Deployment types</span></span>
<span data-ttu-id="1f69c-118">Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="1f69c-119">신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="1f69c-120">[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="1f69c-121">결과는 다음 배포 유형 중 하나로 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="1f69c-122">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="1f69c-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="1f69c-123">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f69c-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="1f69c-124">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f69c-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="1f69c-125">Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="1f69c-126">예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)에서 재고/생산 주문 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="1f69c-127">Contoso는 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비 재고/리소스 기반 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="1f69c-128">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="1f69c-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="1f69c-129">라이트 배포에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="1f69c-130">Dynamics 365 Sales 애플리케이션 경험을 확장하는 프로젝트의 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="1f69c-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="1f69c-131">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="1f69c-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1f69c-132">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="1f69c-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1f69c-133">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="1f69c-133">Unified resource management</span></span>
- <span data-ttu-id="1f69c-134">시간 추적</span><span class="sxs-lookup"><span data-stu-id="1f69c-134">Time tracking</span></span>
- <span data-ttu-id="1f69c-135">기본 경비</span><span class="sxs-lookup"><span data-stu-id="1f69c-135">Basic expense</span></span>
- <span data-ttu-id="1f69c-136">견적 및 고객 대면 송장 발행</span><span class="sxs-lookup"><span data-stu-id="1f69c-136">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="1f69c-137">배포 단계</span><span class="sxs-lookup"><span data-stu-id="1f69c-137">Deployment steps</span></span>
<span data-ttu-id="1f69c-138">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1f69c-139">이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="1f69c-140">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f69c-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="1f69c-141">리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="1f69c-142">Dynamics 365 Sales 애플리케이션을 확장하는 프로젝트의 영업 프로세스</span><span class="sxs-lookup"><span data-stu-id="1f69c-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="1f69c-143">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="1f69c-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1f69c-144">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="1f69c-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1f69c-145">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="1f69c-145">Unified resource management</span></span>
- <span data-ttu-id="1f69c-146">시간 추적</span><span class="sxs-lookup"><span data-stu-id="1f69c-146">Time tracking</span></span>
- <span data-ttu-id="1f69c-147">기본 경비</span><span class="sxs-lookup"><span data-stu-id="1f69c-147">Basic expense</span></span>
- <span data-ttu-id="1f69c-148">전체 경비</span><span class="sxs-lookup"><span data-stu-id="1f69c-148">Full expense</span></span>
- <span data-ttu-id="1f69c-149">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="1f69c-149">Receipt OCR</span></span>
- <span data-ttu-id="1f69c-150">견적 및 고객 대면 송장 발행</span><span class="sxs-lookup"><span data-stu-id="1f69c-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="1f69c-151">프로젝트의 수익 인식</span><span class="sxs-lookup"><span data-stu-id="1f69c-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="1f69c-152">배포 단계</span><span class="sxs-lookup"><span data-stu-id="1f69c-152">Deployment steps</span></span>
<span data-ttu-id="1f69c-153">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1f69c-154">이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="1f69c-155">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f69c-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="1f69c-156">WBS를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="1f69c-156">Project planning using WBS</span></span>
- <span data-ttu-id="1f69c-157">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="1f69c-157">Resource Management</span></span>
- <span data-ttu-id="1f69c-158">시간 추적</span><span class="sxs-lookup"><span data-stu-id="1f69c-158">Time Tracking</span></span>
- <span data-ttu-id="1f69c-159">전체 경비</span><span class="sxs-lookup"><span data-stu-id="1f69c-159">Full Expense</span></span>
- <span data-ttu-id="1f69c-160">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="1f69c-160">Receipt OCR</span></span>
- <span data-ttu-id="1f69c-161">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="1f69c-161">Full Invoicing</span></span>
- <span data-ttu-id="1f69c-162">수익 인식</span><span class="sxs-lookup"><span data-stu-id="1f69c-162">Revenue Recognition</span></span>
- <span data-ttu-id="1f69c-163">생산 주문</span><span class="sxs-lookup"><span data-stu-id="1f69c-163">Production Orders</span></span>
- <span data-ttu-id="1f69c-164">재료 지원</span><span class="sxs-lookup"><span data-stu-id="1f69c-164">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="1f69c-165">배포 단계</span><span class="sxs-lookup"><span data-stu-id="1f69c-165">Deployment steps</span></span>
<span data-ttu-id="1f69c-166">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f69c-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1f69c-167">이 배포의 경우 [미리 보기 구독 신청](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) 및 [새로운 환경 제공](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1f69c-167">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
