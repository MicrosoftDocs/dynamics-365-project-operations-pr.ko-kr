---
title: 리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334835"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="908ae-103">리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록</span><span class="sxs-lookup"><span data-stu-id="908ae-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="908ae-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="908ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="908ae-105">이 항목에서는 평가판을 구독하고 리소스/비재고 기반 시나리오를 위한 Project Operations 환경을 배포하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="908ae-106">필수 조건</span><span class="sxs-lookup"><span data-stu-id="908ae-106">Prerequisites</span></span>
- <span data-ttu-id="908ae-107">미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="908ae-108">첫 번째 제안 사용 중에 테넌트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="908ae-109">Finance 환경을 배포하려면 환경별로 요금이 청구되는 유효한 Azure 구독이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="908ae-110">조직의 기존 구독을 사용하거나 [Azure 평가판](https://azure.microsoft.com/en-us/free/)을 사용하여 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="908ae-111">CDS 환경은 제한된 30일 동안 무료로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="908ae-112">조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="908ae-113">이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.</span><span class="sxs-lookup"><span data-stu-id="908ae-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="908ae-114">평가판은 테넌트에서 일회용입니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="908ae-115">평가판은 한 번만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-115">You can only run a trial one time.</span></span> <span data-ttu-id="908ae-116">평가판을 위해 새 테넌트를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="908ae-117">Dynamics 365 Project Operations(CE) - 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="908ae-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="908ae-118">시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="908ae-119">첫 번째 제안 코드 **Dynamics 365 Project Operations** 여기[ Project Operations 평가판](https://aka.ms/try-po)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="908ae-120">주문을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-120">Confirm your order.</span></span>

  <span data-ttu-id="908ae-121">확인 제안이 성공적으로 회수되었음을 확인하는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="908ae-122">Dynamics 365 Finance 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="908ae-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="908ae-123">[Dynamics 365 for Finance 미리 보기 평가판](https://aka.ms/trypoche)으로 이동하고 제안의 이전 섹션의 단계를 반복하고 클라우드 호스팅 환경에 가입합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="908ae-124">라이선스 할당</span><span class="sxs-lookup"><span data-stu-id="908ae-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="908ae-125">다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="908ae-126">[Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="908ae-127">**활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="908ae-128">**Dynamics 365 Project Operations** 라이선스가 선택되었는지 확인하고 **변경 사항 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="908ae-129">Finance 평가판 제안은 사용자에게 할당할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="908ae-130">LCS에서 새 프로젝트 시작</span><span class="sxs-lookup"><span data-stu-id="908ae-130">Start a new project in LCS</span></span>

<span data-ttu-id="908ae-131">항목 [LCS에서 새 프로젝트 시작](create-lcs-project.md)에 설명된 대로 새 LCS 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="908ae-132">LCS 프로젝트에 Azure 구독 추가</span><span class="sxs-lookup"><span data-stu-id="908ae-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="908ae-133">이 작업을 완료하려면 항목 [LCS 프로젝트에 Azure 구독 추가](resource-add-azure-subscription-lcs-project.md)의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="908ae-134">리소스/비 재고 시나리오를 위한 Project Operations과 함께 Finance 데모 환경 배포</span><span class="sxs-lookup"><span data-stu-id="908ae-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="908ae-135">항목 [새로운 환경 프로비전](resource-provision-new-environment.md)의 안내를 따라 배포를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="908ae-136">미리 보기를 위한 [데모 환경](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 배포 유형을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="908ae-137">CDS 설정 및 구성 데이터 설치</span><span class="sxs-lookup"><span data-stu-id="908ae-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="908ae-138">항목 [Common Data Service에서 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md)에 설명된 대로 CDS 설정 및 구성 데이터를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="908ae-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="908ae-139">Finance 데모 환경이 배포되고 데모 데이터가 준비된 후에만 이 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="908ae-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
