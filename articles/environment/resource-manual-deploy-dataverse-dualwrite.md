---
title: 이중 쓰기를 지원하는 Project Operations Dataverse 앱 수동 배포
description: 이 항목에서는 이중 쓰기를 지원하도록 Project Operations Dataverse 앱을 수동으로 배포하는 방법을 설명합니다.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274016"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="20783-103">이중 쓰기를 지원하는 Project Operations Dataverse 앱 수동 배포</span><span class="sxs-lookup"><span data-stu-id="20783-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="20783-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="20783-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="20783-105">이 항목에서는 이중 쓰기를 지원하도록 Microsoft Dataverse에 Microsoft Dynamics 365 Project Operations을 수동으로 배포하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="20783-106">Project Operations는 환경의 구성을 감지하고 전제 조건이 충족되는 경우 이중 쓰기에 대한 추가 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="20783-107">Microsoft Dynamics LCS(Lifecycle Services)를 통해 배포하는 동안 이 항목의 지침을 따랐다면 Microsoft Power Platform 통합(이전에는 Common Data Service 환경이라고 함) 배포를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20783-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="20783-108">이중 쓰기를 지원하도록 Dataverse에 Project Operations를 배포하는 프로세스는 네 가지 주요 단계로 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="20783-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="20783-109">[이중 쓰기를 지원하는 Dataverse에서 새로운 환경 만들기](#create).</span><span class="sxs-lookup"><span data-stu-id="20783-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="20783-110">[환경에 이중 쓰기 사전 요구 사항 추가](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="20783-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="20783-111">[Project Operations Dataverse 앱 추가](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="20783-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="20783-112">[환경을 연결](#link).</span><span class="sxs-lookup"><span data-stu-id="20783-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="20783-113">이중 쓰기를 지원하는 Dataverse에서 새로운 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="20783-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="20783-114">이 절차를 완료하려면 관리자로 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="20783-115">[Power Platform 관리 센터](https://admin.powerplatform.com)를 열고 관리자로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="20783-116">새 환경을 만들고 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="20783-117">환경 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-117">Select the environment type.</span></span> <span data-ttu-id="20783-118">평가판 제안에 가입한 경우 **평가판(구독 기반)** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="20783-119">배포 지역을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="20783-120">**이 환경에 대한 데이터베이스 만들기** 옵션을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="20783-121">언어를 확인한 다음 통화가 사용자의 Finance and Operations 앱 통화와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="20783-122">**Dynamics 365 앱** 옵션을 활성화하고 **이 앱 자동 배포** 필드가 **없음** 으로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="20783-123">보안 그룹이 필요한 경우 보안 그룹을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="20783-124">**저장** 을 선택하여 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20783-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="20783-125">배포가 완료되고 환경이 **준비** 상태에 도달할 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="20783-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="20783-126">환경에 이중 쓰기 사전 요구 사항 추가</span><span class="sxs-lookup"><span data-stu-id="20783-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="20783-127">이중 쓰기 지원에는 **회사** 엔터티와 같은 주요 엔터티에 추가되는 추가 필드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="20783-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="20783-128">기존 환경에 이중 쓰기 지원을 추가하는 경우 지원을 활성화하려면 데이터를 업데이트해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20783-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="20783-129">데이터를 부트스트랩하는 방법에 대한 자세한 내용은 [회사 데이터 부트스트랩](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="20783-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="20783-130">이중 쓰기에 대한 자세한 내용은 [이중 쓰기 시스템 요구 사항](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="20783-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="20783-131">이중 쓰기 사전 요구 사항을 환경에 추가하려면 이 절차를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="20783-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="20783-132">방금 만든 환경을 열고 **리소스** \> **Dynamics 365 앱** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="20783-133">앱 목록에서 **이중 쓰기 코어 솔루션** 을 선택하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="20783-134">설치가 완료될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="20783-134">Wait until the installation is completed.</span></span> <span data-ttu-id="20783-135">그런 다음 앱 목록에서 **이중 쓰기 애플리케이션 오케스트레이션 솔루션** 을 선택하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="20783-136">Project Operations Dataverse 앱 추가</span><span class="sxs-lookup"><span data-stu-id="20783-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="20783-137">Project Operations를 설치하기 전에 이전 절차를 완료한 경우에만 이 절차를 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20783-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="20783-138">설치하는 동안 시스템은 환경 구성을 분석하고 필요한 경우 이중 쓰기 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="20783-139">이전에 만든 환경을 열고 **리소스** \> **Dynamics 365 앱** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="20783-140">앱 목록에서 **Microsoft Dynamics 365 Project Operations** 를 선택하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="20783-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="20783-141">환경을 연결</span><span class="sxs-lookup"><span data-stu-id="20783-141">Link your environments</span></span>

<span data-ttu-id="20783-142">Dataverse 환경이 배포된 후 Finance and Operations 앱에서 링크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20783-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="20783-143">[이중 쓰기 마법사를 사용하여 환경 연결](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="20783-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
