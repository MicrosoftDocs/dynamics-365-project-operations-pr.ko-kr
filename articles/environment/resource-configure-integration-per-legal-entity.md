---
title: 법인별 프로젝트 Project Operations 통합 구성
description: 이 항목은 Project Operations에서 법인에 의한 통합 설정에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096760"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="b90b6-103">법인별 프로젝트 Project Operations 통합 구성</span><span class="sxs-lookup"><span data-stu-id="b90b6-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="b90b6-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b90b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b90b6-105">이 항목은 법인별로 Dynamics 365 Project Operations를 구성하는 데 필요한 단계를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="b90b6-106">Dynamics 365 Finance에서 기능 키 활성화</span><span class="sxs-lookup"><span data-stu-id="b90b6-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="b90b6-107">필수 기능을 사용하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="b90b6-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="b90b6-108">Dynamics 365 Finance에서 **기능 관리** 작업 영역으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="b90b6-109">**기능 목록** 에서 다음 기능을 찾아 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="b90b6-110">**프로젝트에 대해 여러 계약 내용 활성화**</span><span class="sxs-lookup"><span data-stu-id="b90b6-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="b90b6-111">**Dynamics 365 Customer Engagement에서 Project Operations 활성화**</span><span class="sxs-lookup"><span data-stu-id="b90b6-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="b90b6-112">**기능 키** 가 표시되지 않으면 Finance 버전이 최소 버전 요구 사항(모든 품질 업데이트가 적용된 응용 프로그램 버전 10.0.13 이상)을 충족하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="b90b6-113">**업데이트 확인** 을 선택하여 기능 목록을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="b90b6-114">법인에 대한 Project Operations 배포 시나리오 정의</span><span class="sxs-lookup"><span data-stu-id="b90b6-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="b90b6-115">법인 수준의 Dynamics 365 Customer Engagement에서 Project Operations를 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="b90b6-116">리소스/비 재고 기반 시나리오의 경우 Dynamics 365 Customer Engagement에서 Project Operations를 사용하여 하나의 법인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="b90b6-117">동일한 환경에서 재고/생산 주문 시나리오에 대해 Project Operations를 사용하는 다른 법인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="b90b6-118">Dynamics 365 Finance에서 **프로젝트 관리 및 회계** > **설정** > **전역 프로젝트 관리 및 회계 매개 변수** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="b90b6-119">사용 가능한 법인 목록에서 Dynamics 365 Customer Engagement 기능의 여러 계약 내용 및 Project Operations가 활성화되는 엔터티를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="b90b6-120">재고/생산 주문 시나리오에 대해 Project Operations를 사용할 법인은 선택하지 않은 상태로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="b90b6-121">법인은 기존 프로젝트가 없는 경우에만 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="b90b6-122">프로젝트 관리 및 회계 매개 변수 구성</span><span class="sxs-lookup"><span data-stu-id="b90b6-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="b90b6-123">Dynamics 365 Customer Engagement에서 Project Operations를 사용하는 각 법인은 기본 매개 변수 집합이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="b90b6-124">이러한 매개 변수는 **프로젝트 관리 및 회계 매개 변수** 페이지의 **Project Operations** 탭에 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="b90b6-125">매개 변수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-125">The parameters are:</span></span>

  - <span data-ttu-id="b90b6-126">**결제 유형 기본값** : Project Operations는 라인 속성 Finance에 매핑되어야 하는 고정된 청구 유형 기본값 세트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="b90b6-127">각 청구 유형 **지정하지 않음** , **청구 가능** , **청구 불가능** , **무료** 및 **사용할 수 없음** 에 대한 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="b90b6-128">**프로젝트 범주 기본값** : 각 트랜잭션 유형에 사용할 기본 프로젝트 범주를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="b90b6-129">이러한 기본값은 **Project Operations 통합 분개장** 및 실제 프로젝트에 대해 트랜잭션 범주가 지정되지 않은 추정에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="b90b6-130">**예측** : 시간 및 비용 추정에 사용할 예측 모델을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b6-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
