---
title: 미리 보기 구독 신청 - 라이트
description: 이 항목은 Project Operations 라이트 배포 - 견적 송장 거래를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334790"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="429a7-103">미리 보기 구독 신청 - 라이트</span><span class="sxs-lookup"><span data-stu-id="429a7-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="429a7-104">이 항목에서는 평가판을 구독하고 Dynamics 365 Project Operations 라이트 배포를 배포하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="429a7-105">이 프로세스는 Project Operations의 향후 릴리스에서 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="429a7-106">필수 조건</span><span class="sxs-lookup"><span data-stu-id="429a7-106">Prerequisites</span></span>
- <span data-ttu-id="429a7-107">미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="429a7-108">첫 번째 제안 사용 중에 테넌트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="429a7-109">조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="429a7-110">이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.</span><span class="sxs-lookup"><span data-stu-id="429a7-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="429a7-111">평가판은 테넌트에서 일회용입니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="429a7-112">평가판은 한 번만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-112">You can only run a trial one time.</span></span> <span data-ttu-id="429a7-113">평가판을 위해 새 테넌트를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="429a7-114">Dynamics 365 Project Operations 평가판</span><span class="sxs-lookup"><span data-stu-id="429a7-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="429a7-115">시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="429a7-116">[Project Operations 평가판](https://aka.ms/try-po)으로 이동하여 첫 번째 제안 코드인 **Dynamics 365 Project Operations** 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="429a7-117">주문을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-117">Confirm your order.</span></span>

  <span data-ttu-id="429a7-118">확인 제안이 성공적으로 사용되었음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="429a7-119">라이선스 할당</span><span class="sxs-lookup"><span data-stu-id="429a7-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="429a7-120">다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="429a7-121">[Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="429a7-122">**활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="429a7-123">**Dynamics 365 Project Operations** 라이선스가 선택되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="429a7-124">**변경 내용 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="429a7-125">새 Dataverse 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="429a7-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="429a7-126">항목 [Dataverse 배포 모델](lite-deployment.md)의 지침에 따라 새 Project Operations Dataverse 배포 환경을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="429a7-127">환경 유형을 선택할 때 **평가판(구독 기반)** 을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![새 환경](./media/19CreateEnvironment.png)

2. <span data-ttu-id="429a7-129">**Dynamics 365 앱 사용** 설정을 선택하고 **이러한 앱 자동 배포** 를 비워둡니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="429a7-130">**저장** 을 선택하여 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-130">Select **Save** to create the environment.</span></span>

  ![데이터베이스 추가](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="429a7-132">환경이 생성된 후 **Microsoft Dynamics 365 Project Operations** 솔루션을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![솔루션 설치](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="429a7-134">CDS 구성 설치 및 데모 데이터 설정</span><span class="sxs-lookup"><span data-stu-id="429a7-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="429a7-135">항목 [데모 설정 및 구성 데이터 적용](lite-apply-demo-setup-config-data.md)의 지침에 따라 CDS 구성을 설치하고 데모 데이터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="429a7-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
