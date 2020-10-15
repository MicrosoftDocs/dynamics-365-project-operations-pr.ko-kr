---
title: 배포 유형
description: 이 항목에서는 회사에 적합한 Project Operations 배포 유형을 결정하는 데 도움이 되는 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948958"
---
# <a name="deployment-types"></a><span data-ttu-id="cea16-103">배포 유형</span><span class="sxs-lookup"><span data-stu-id="cea16-103">Deployment types</span></span>

<span data-ttu-id="cea16-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="cea16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cea16-105">라이선스를 구매한 후 여기에서 시작하여 [안내식 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="cea16-106">안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="cea16-107">설치를 완료하려면 아래 배포 세부 정보를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cea16-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="cea16-108">Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="cea16-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="cea16-109">Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="cea16-110">향후 이러한 고객을 위한 업그레이드 경로가 릴리스될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="cea16-111">프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객</span><span class="sxs-lookup"><span data-stu-id="cea16-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="cea16-112">프로젝트 관리 및 회계 기능을 사용하는 기존 재무 고객은 그대로 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="cea16-113">[리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cea16-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="cea16-114">Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="cea16-115">신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="cea16-116">[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="cea16-117">결과는 다음 배포 유형 중 하나로 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="cea16-118">라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="cea16-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="cea16-119">리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="cea16-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="cea16-120">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="cea16-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="cea16-121">Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="cea16-122">예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)의 재고/생산 주문 기능과 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비재고/리소스 기반 기능을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="cea16-123"><a name="lite"><a/>라이트 배포 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="cea16-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="cea16-124">라이트 배포에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="cea16-125">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="cea16-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="cea16-126">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="cea16-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="cea16-127">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="cea16-127">Unified Resource Management</span></span>
- <span data-ttu-id="cea16-128">시간 추적</span><span class="sxs-lookup"><span data-stu-id="cea16-128">Time Tracking</span></span>
- <span data-ttu-id="cea16-129">기본 경비</span><span class="sxs-lookup"><span data-stu-id="cea16-129">Basic Expense</span></span>
- <span data-ttu-id="cea16-130">송장 제안</span><span class="sxs-lookup"><span data-stu-id="cea16-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="cea16-131">배포 단계:</span><span class="sxs-lookup"><span data-stu-id="cea16-131">Deployment steps:</span></span>
<span data-ttu-id="cea16-132">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cea16-133">이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cea16-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="cea16-134"><a name="integrated"><a/>리소스/비 재고 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="cea16-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="cea16-135">리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="cea16-136">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="cea16-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="cea16-137">다차원 가격 책정</span><span class="sxs-lookup"><span data-stu-id="cea16-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="cea16-138">통합 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="cea16-138">Unified Resource Management</span></span>
- <span data-ttu-id="cea16-139">시간 추적</span><span class="sxs-lookup"><span data-stu-id="cea16-139">Time Tracking</span></span>
- <span data-ttu-id="cea16-140">기본 경비</span><span class="sxs-lookup"><span data-stu-id="cea16-140">Basic Expense</span></span>
- <span data-ttu-id="cea16-141">전체 경비</span><span class="sxs-lookup"><span data-stu-id="cea16-141">Full Expense</span></span>
- <span data-ttu-id="cea16-142">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="cea16-142">Receipt OCR</span></span>
- <span data-ttu-id="cea16-143">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="cea16-143">Full Invoicing</span></span>
- <span data-ttu-id="cea16-144">수익 인식</span><span class="sxs-lookup"><span data-stu-id="cea16-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="cea16-145">배포 단계:</span><span class="sxs-lookup"><span data-stu-id="cea16-145">Deployment steps:</span></span>
<span data-ttu-id="cea16-146">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cea16-147">이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cea16-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="cea16-148">리소스/생산 주문 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="cea16-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="cea16-149">WBS를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="cea16-149">Project planning using WBS</span></span>
- <span data-ttu-id="cea16-150">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="cea16-150">Resource Management</span></span>
- <span data-ttu-id="cea16-151">시간 추적</span><span class="sxs-lookup"><span data-stu-id="cea16-151">Time Tracking</span></span>
- <span data-ttu-id="cea16-152">전체 경비</span><span class="sxs-lookup"><span data-stu-id="cea16-152">Full Expense</span></span>
- <span data-ttu-id="cea16-153">OCR 영수증</span><span class="sxs-lookup"><span data-stu-id="cea16-153">Receipt OCR</span></span>
- <span data-ttu-id="cea16-154">전체 송장 발행</span><span class="sxs-lookup"><span data-stu-id="cea16-154">Full Invoicing</span></span>
- <span data-ttu-id="cea16-155">수익 인식</span><span class="sxs-lookup"><span data-stu-id="cea16-155">Revenue Recognition</span></span>
- <span data-ttu-id="cea16-156">생산 주문</span><span class="sxs-lookup"><span data-stu-id="cea16-156">Production Orders</span></span>
- <span data-ttu-id="cea16-157">재료 지원</span><span class="sxs-lookup"><span data-stu-id="cea16-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="cea16-158">배포 단계:</span><span class="sxs-lookup"><span data-stu-id="cea16-158">Deployment steps:</span></span>
<span data-ttu-id="cea16-159">[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="cea16-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cea16-160">이 배포의 경우 [미리 보기 구독 신청](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) 및 [새로운 환경 제공](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cea16-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



