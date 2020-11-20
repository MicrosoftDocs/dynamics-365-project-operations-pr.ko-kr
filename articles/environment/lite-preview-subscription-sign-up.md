---
title: 미리 보기 구독 신청 - 라이트
description: 이 항목은 Project Operations 라이트 배포 - 견적 송장 거래를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175899"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="503fc-103">미리 보기 구독 신청 - 라이트</span><span class="sxs-lookup"><span data-stu-id="503fc-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="503fc-104">이 항목에서는 미리보기 파트너 제안을 구독하고 Dynamics 365 Project Operations 라이트 배포 - 견적 송장 처리를 배포하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="503fc-105">이 프로세스는 Project Operations의 향후 릴리스에서 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="503fc-106">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="503fc-106">Prerequisites</span></span>

- <span data-ttu-id="503fc-107">미리 보기에 참여하도록 초대하는 이메일을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="503fc-108">[Project Operations 웹 사이트](https://dynamics.microsoft.com/en-us/project-operations/overview/)에서 미리 보기를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="503fc-109">미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="503fc-110">모든 이용 약관을 검토하십시오.</span><span class="sxs-lookup"><span data-stu-id="503fc-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="503fc-111">구독</span><span class="sxs-lookup"><span data-stu-id="503fc-111">Subscribe</span></span>

<span data-ttu-id="503fc-112">[미리 보기 요청](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) 승인을 받으면 이메일로 Microsoft로부터 두 가지 제안을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="503fc-113">이러한 제안을 통해 Project Operations 미리 보기를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="503fc-114">Dynamics 365 Project Operations(CRM) – 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="503fc-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="503fc-115">Office 365 Project Operations - 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="503fc-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="503fc-116">조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="503fc-117">이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.</span><span class="sxs-lookup"><span data-stu-id="503fc-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="503fc-118">Dynamics 365 Project Operations(CRM) – 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="503fc-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="503fc-119">시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="503fc-120">브라우저 URL에 붙여 넣어 첫 번째 제안 코드 **Dynamics 365 Project Operations(CRM) - 평가판 미리 보기** 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![초대 제안](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="503fc-122">주문을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-122">Confirm your order.</span></span>
<span data-ttu-id="503fc-123">![주문 확인](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="503fc-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="503fc-124">확인 제안이 성공적으로 회수되었음을 확인하는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-124">You'll see confirmation offer was successfully redeemed.</span></span>

![확인](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="503fc-126">Office 365 Project Operations - 평가판 미리 보기</span><span class="sxs-lookup"><span data-stu-id="503fc-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="503fc-127">첫 번째 제안 코드와 동일한 단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="503fc-128">첫 번째 제안 코드에 사용된 것과 동일한 사용자 계정을 사용하여 두 번째 제안 코드를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="503fc-129">라이선스 할당</span><span class="sxs-lookup"><span data-stu-id="503fc-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="503fc-130">다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="503fc-131">[Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![관리 센터 홈 페이지](./media/14AdminPortal.png)

2. <span data-ttu-id="503fc-133">**활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![라이선스 할당](./media/15AssignLicenses.png)

3. <span data-ttu-id="503fc-135">**Dynamics 365 Project Operations(CRM) 미리 보기** 및 **Office 365 Project Operations - 미리 보기** 라이선스가 선택되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="503fc-136">**변경 내용 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="503fc-137">새 CDS 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="503fc-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="503fc-138">항목 [CDS 배포 모델](lite-deployment.md)의 지침에 따라 새 Project Operations CDS 배포 환경을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="503fc-139">환경 유형을 선택할 때 **평가판(구독 기반)** 을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="503fc-140">![새 환경](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="503fc-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="503fc-141">**Dynamics 365 앱 사용** 설정을 선택하고 **이러한 앱 자동 배포** 를 비워둡니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="503fc-142">**저장** 을 선택하여 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-142">Select **Save** to create the environment.</span></span>

![데이터베이스 추가](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="503fc-144">환경이 생성된 후 **Microsoft Dynamics 365 Project Operations** 솔루션을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![솔루션 설치](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="503fc-146">CDS 구성 설치 및 데모 데이터 설정</span><span class="sxs-lookup"><span data-stu-id="503fc-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="503fc-147">항목 [데모 설정 및 구성 데이터 적용](lite-apply-demo-setup-config-data.md)의 지침에 따라 CDS 구성을 설치하고 데모 데이터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="503fc-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>
