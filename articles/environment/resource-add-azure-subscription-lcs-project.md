---
title: LCS 프로젝트에 Azure 구독 추가
description: 이 항목은 Azure 구독을 LCS 프로젝트에 연결하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948961"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="17d6d-103">LCS 프로젝트에 Azure 구독 추가</span><span class="sxs-lookup"><span data-stu-id="17d6d-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="17d6d-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="17d6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="17d6d-105">클라우드 호스팅 환경은 기존 Azure 구독을 사용하여 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="17d6d-106">이 항목은 기존 Azure 구독을 LCS 프로젝트에 연결하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="17d6d-107">관리자 동의 부여</span><span class="sxs-lookup"><span data-stu-id="17d6d-107">Grant admin consent</span></span>

1. <span data-ttu-id="17d6d-108">LCS 프로젝트의 **환경** 섹션에서 **Microsoft Azure 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure 설정](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="17d6d-110">**Azure 커넥터** 탭의 **프로젝트 설정** 페이지에서 **승인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="17d6d-111">이를 통해 이 프로젝트에 환경을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-111">This allows environments to be deployed to this project.</span></span>

![Azure 커넥터](./media/2AzureConnectors.png)

3. <span data-ttu-id="17d6d-113">**승인**을 다시 선택하여 관리자 동의를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-113">Select **Authorize** again to provide admin consent.</span></span>

![관리자 동의 부여](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="17d6d-115">권한 요청을 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-115">Accept the permissions request.</span></span>

![권한 요청 수락](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="17d6d-117">이제 인증이 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-117">The authorization is now complete.</span></span> 

![승인 성공](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="17d6d-119">Azure 구독에 대한 Dynamics 배포 서비스 액세스 제공</span><span class="sxs-lookup"><span data-stu-id="17d6d-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="17d6d-120">[Microsoft Azure 청구](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)로 이동하여 구독을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="17d6d-121">Dynamics Deployment Services는 환경을 배포할 수 있으려면 이 구독에 액세스해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure 구독 세부 정보](./media/6AzureSubscription.png)

2. <span data-ttu-id="17d6d-123">탐색 창에서 **액세스 제어(IAM)** 를 선택한 다음 **역할 할당 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="17d6d-124">오른쪽의 슬라이더에서 **Contributor 역할**을 클릭하고 제공된 목록에서 **Dynamics 배포 서비스**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="17d6d-125">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-125">Select **Save**.</span></span>

![구독 액세스](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="17d6d-127">LCS 프로젝트에 구독 커넥터 추가</span><span class="sxs-lookup"><span data-stu-id="17d6d-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="17d6d-128">LCS 프로젝트의 **Microsoft Azure 설정** 페이지에서 **추가**를 선택하여 새 커넥터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="17d6d-129">Azure 구독 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="17d6d-130">Azure 구독 ID는 [Azure 포털](https://ms.portal.azure.com/)의 **설정** 아래 화면 왼쪽 하단에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="17d6d-131">**Azure Resource Manager를 사용하도록 구성** 필드에서 **예**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="17d6d-132">Azure의 구독 AAD 테넌트 도메인이 사용 중인 도메인 소유 Azure 구독과 일치하는지 확인하고 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="17d6d-133">**Microsoft Azure 설정** 화면에서 **다음**을 선택하여 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="17d6d-134">이 화면에 오류가 표시되면 이 항목의 [Azure 구독에 대한 Dynamics 배포 서비스 액세스 제공](#provide) 섹션으로 돌아가서 모든 단계를 완료했는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="17d6d-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="17d6d-135">컴퓨터의 로컬 폴더에 Azure 관리 인증서를 다운로드한 다음 **설정** > **관리 인증서**로 이동하여 Azure 관리 포털에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="17d6d-136">이 인증서를 사용하면 LCS가 사용자를 대신하여 Azure와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="17d6d-137">사용자에게 구독에 대한 액세스 권한이 있는 경우 이 단계를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="17d6d-138">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-138">Select  **Next**.</span></span>
8. <span data-ttu-id="17d6d-139">배포할 Azure 지역을 선택하고 이 시스템을 사용하려는 위치와 가까운 데이터 센터를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="17d6d-140">**연결**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-140">Select  **Connect**.</span></span>

<span data-ttu-id="17d6d-141">Azure 구독을 성공적으로 연결했습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="17d6d-142">이제 Dynamics 365 Finance 클라우드 호스팅 환경을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d6d-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


