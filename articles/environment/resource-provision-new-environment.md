---
title: 새 환경 프로비전
description: 이 항목은 새 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950542"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="bb26f-103">새 환경 프로비전</span><span class="sxs-lookup"><span data-stu-id="bb26f-103">Provision a new environment</span></span>

<span data-ttu-id="bb26f-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bb26f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bb26f-105">이 토픽은 리소스/비 재고 기반 시나리오를 위한 새 Dynamics 365 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="bb26f-106">LCS 프로젝트에서 Project Operations 자동화 프로비전 활성화</span><span class="sxs-lookup"><span data-stu-id="bb26f-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="bb26f-107">다음 단계를 사용하여 LCS 프로젝트에 대한 Project Operations 자동화 프로비전 흐름을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="bb26f-108">[LCS](https://lcs.dynamics.com/v2)로 이동하고 **미리 보기 기능 관리** 타일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="bb26f-109">**미리 보기 기능** 목록에서 **Project Operations 기능** 을 선택하고 **미리 보기 기능 활성화됨** 을 선택하여 Project Operations를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="bb26f-110">이 단계는 LCS 프로젝트당 한 번만 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="bb26f-111">Project Operations 환경 프로비전</span><span class="sxs-lookup"><span data-stu-id="bb26f-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="bb26f-112">새로운 Dynamics 365 Finance [데모 환경](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 또는 [샌드박스/프로덕션 환경](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="bb26f-113">**환경 프로비전** 마법사를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="bb26f-114">선택한 응용 프로그램 버전이 10.0.13 이상인지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="bb26f-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="bb26f-115">Project Operations를 프로비전하려면 **고급 설정** 에서 **Common Data Service** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="bb26f-116">**예** 를 선택하여 **Common Data Service 설정** 을 활성화한 다음 필수 필드에 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="bb26f-117">Name</span><span class="sxs-lookup"><span data-stu-id="bb26f-117">Name</span></span>
  - <span data-ttu-id="bb26f-118">영역</span><span class="sxs-lookup"><span data-stu-id="bb26f-118">Region</span></span>
  - <span data-ttu-id="bb26f-119">언어</span><span class="sxs-lookup"><span data-stu-id="bb26f-119">Language</span></span>
  - <span data-ttu-id="bb26f-120">통화</span><span class="sxs-lookup"><span data-stu-id="bb26f-120">Currency</span></span>
 
5. <span data-ttu-id="bb26f-121">**Common Data Service 템플릿** 필드에서 **Project Operations** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="bb26f-122">배포할 환경 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="bb26f-123">구독 기반 평가판을 사용하면 30일 동안 CDS 환경을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![배포 설정](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="bb26f-125">**수락** 을 선택하여 서비스 약관에 동의한 다음 **완료** 를 선택하여 배포 설정으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![배포 동의](./media/2DeploymentConsent.png)

7. <span data-ttu-id="bb26f-127">선택 사항 - 환경에 데모 데이터를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="bb26f-128">**고급 설정** 으로 이동하고 **SQL 데이터베이스 구성 사용자 지정** 을 선택하고 **응용 프로그램 데이터베이스에 대한 데이터 세트 지정** 을 **데모** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="bb26f-129">마법사의 나머지 필수 필드를 완료하고 배포를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="bb26f-130">환경 프로비저닝 시간은 환경 유형에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="bb26f-131">프로비전에는 최대 6시간이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="bb26f-132">배포가 성공적으로 완료되면 환경이 **배포됨** 으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="bb26f-133">환경이 성공적으로 배포되었는지 확인하려면 **로그인** 을 선택하고 확인을 위해 환경에 로그온합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 환경 세부 정보](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="bb26f-135">Finance 환경에 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="bb26f-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="bb26f-136">Project Operations에는 애플리케이션 버전이 **10.0.13(10.0.569.20009)** 이상인 Finance 환경이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="bb26f-137">이 버전을 받으려면 Finance 환경에 품질 업데이트를 적용해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="bb26f-138">LCS의 **환경 세부 정보** 페이지에서 **사용 가능한 업데이트** 섹션에서 **업데이트 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![보기 업데이트](./media/5ViewUpdates.png)

2. <span data-ttu-id="bb26f-140">**바이너리 업데이트** 페이지에서 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-140">On the **Binary updates** page, select **Save package.**</span></span>

![패키지 저장](./media/6SavePackage.png)

3. <span data-ttu-id="bb26f-142">**모두 선택** 을 클릭한 다음 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-142">Click **Select all** and then select **Save package**.</span></span>

![업데이트 검토 및 저장](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="bb26f-144">패키지의 이름과 설명을 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="bb26f-145">인터넷 연결에 따라 이 과정은 다소 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-145">Depending on the internet connection, this process might take some time.</span></span>

![자산 라이브러리에 패키지 업로드](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="bb26f-147">패키지를 저장한 후 **완료** 를 선택하고 이 패키지를 LCS 프로젝트의 자산 라이브러리에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="bb26f-148">패키지를 저장하고 유효성을 검사하는 데 15분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="bb26f-149">업데이트를 적용하려면 LCS의 **환경 세부 정보** 페이지에서 **유지** > **업데이트 적용** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![환경 유지](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="bb26f-151">업데이트 목록에서 생성한 패키지를 선택하고 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-151">In the updates list select the package you created, and select **Apply**.</span></span>

![업데이트 적용](./media/10ApplyUpdates.png)

<span data-ttu-id="bb26f-153">환경 서비스는 다소 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-153">Environment servicing will take some time.</span></span> <span data-ttu-id="bb26f-154">완료되면 환경이 배포된 상태로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-154">After it is complete, the environment will return to a deployed state.</span></span>

![배포된 환경](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="bb26f-156">이중 쓰기 연결 설정</span><span class="sxs-lookup"><span data-stu-id="bb26f-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="bb26f-157">LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="bb26f-158">**Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="bb26f-159">링크가 완료된 후 **CDS for Apps에 대한 링크** 를 다시 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="bb26f-160">Finance에서 이중 쓰기로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS에 대한 링크](./media/12LinktoCDS.png)

4. <span data-ttu-id="bb26f-162">**솔루션 적용** 을 선택하여 통합에 매핑될 엔터티에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![솔루션 적용](./media/13ApplySolutions.png)

5. <span data-ttu-id="bb26f-164">두 솔루션 **Dynamics 365 Finance and Operations 이중 쓰기 엔터티 맵** 과 **Dynamics 365 Project Operations 이중 쓰기 엔터티 맵** 을 모두 선택한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![솔루션 확인](./media/14ConfirmSolutions.png)

<span data-ttu-id="bb26f-166">솔루션이 적용된 후 이중 쓰기 엔터티가 환경에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![솔루션 적용](./media/15ApplyingSolutions.png)

<span data-ttu-id="bb26f-168">엔터티가 적용된 후 사용 가능한 모든 매핑이 환경에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![이중 쓰기 맵](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="bb26f-170">업데이트 후 데이터 엔터티 새로 고침</span><span class="sxs-lookup"><span data-stu-id="bb26f-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="bb26f-171">Finance에서 **데이터 관리** 작업 영역으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-171">In Finance, go to the **Data management** workspace.</span></span>

![데이터 관리 작업 공간](./media/16DataManagement.png)

2. <span data-ttu-id="bb26f-173">**프레임워크 매개 변수** 타일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-173">Select the **Framework parameters** tile.</span></span>

![프레임워크 매개 변수](./media/17FrameworkParameters.png)

3. <span data-ttu-id="bb26f-175">**엔터티 설정** 페이지에서 **엔터티 목록 새로 고침** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![엔터티 목록 새로 고침](./media/18RefreshEntityList.png)

<span data-ttu-id="bb26f-177">새로 고침에는 약 20분이 소요됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="bb26f-178">완료되면 알림이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-178">You will receive an alert when it is complete.</span></span>

![새로 고침 확인](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="bb26f-180">Dataverse에서 Project Operations에 대한 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="bb26f-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="bb26f-181">Dataverse 환경에서 Project Operations로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="bb26f-182">**설정** > **보안** > **보안 역할** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="bb26f-183">**보안 역할** 페이지의 역할 목록에서 **이중 쓰기 앱 사용자** 를 선택하고 **사용자 지정 엔터티** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="bb26f-184">역할에 다음에 대한 **읽기** 및 **다른 레코드에 추가** 권한이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="bb26f-185">**통화 환율 유형**</span><span class="sxs-lookup"><span data-stu-id="bb26f-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="bb26f-186">**계정 차트**</span><span class="sxs-lookup"><span data-stu-id="bb26f-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="bb26f-187">**회계 달력**</span><span class="sxs-lookup"><span data-stu-id="bb26f-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="bb26f-188">**원장**</span><span class="sxs-lookup"><span data-stu-id="bb26f-188">**Ledger**</span></span>

5. <span data-ttu-id="bb26f-189">보안 역할이 업데이트되면 **설정** > **보안** > **팀** 으로 이동하고 **로컬 비즈니스 담당자** 팀 보기에서 기본 팀을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="bb26f-190">**역할 관리** 를 선택하고 **이중 쓰기 앱 사용자** 보안 권한이 이 팀에 적용되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="bb26f-191">Project Operations 이중 쓰기 맵 실행</span><span class="sxs-lookup"><span data-stu-id="bb26f-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="bb26f-192">LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="bb26f-193">**Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="bb26f-194">링크를 선택하면 매핑의 엔터티 목록으로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="bb26f-195">다음 표에 설명된 대로 맵을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="bb26f-196">나열된 순서를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="bb26f-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="bb26f-197">**엔터티 맵**</span><span class="sxs-lookup"><span data-stu-id="bb26f-197">**Entity Map**</span></span> | <span data-ttu-id="bb26f-198">**엔터티 새로 고침**</span><span class="sxs-lookup"><span data-stu-id="bb26f-198">**Refresh entity**</span></span> | <span data-ttu-id="bb26f-199">**초기 동기화**</span><span class="sxs-lookup"><span data-stu-id="bb26f-199">**Initial sync**</span></span> | <span data-ttu-id="bb26f-200">**초기 동기화용 마스터**</span><span class="sxs-lookup"><span data-stu-id="bb26f-200">**Master for initial sync**</span></span> | <span data-ttu-id="bb26f-201">**필수 구성 요소 실행**</span><span class="sxs-lookup"><span data-stu-id="bb26f-201">**Run prerequisites**</span></span> | <span data-ttu-id="bb26f-202">**필수 구성 요소 초기 동기화**</span><span class="sxs-lookup"><span data-stu-id="bb26f-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="bb26f-203">**모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="bb26f-204">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-204">No</span></span> | <span data-ttu-id="bb26f-205">있음</span><span class="sxs-lookup"><span data-stu-id="bb26f-205">Yes</span></span> | <span data-ttu-id="bb26f-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="bb26f-206">Common Data Service</span></span> | <span data-ttu-id="bb26f-207">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-207">No</span></span> | <span data-ttu-id="bb26f-208">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-208">N\A</span></span> |
| <span data-ttu-id="bb26f-209">**법인(cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="bb26f-210">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-210">No</span></span> | <span data-ttu-id="bb26f-211">있음</span><span class="sxs-lookup"><span data-stu-id="bb26f-211">Yes</span></span> | <span data-ttu-id="bb26f-212">Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="bb26f-212">Finance and Operations apps</span></span> | <span data-ttu-id="bb26f-213">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-213">No</span></span> | <span data-ttu-id="bb26f-214">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-214">N\A</span></span> |
| <span data-ttu-id="bb26f-215">**원장(msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="bb26f-216">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-216">No</span></span> | <span data-ttu-id="bb26f-217">있음</span><span class="sxs-lookup"><span data-stu-id="bb26f-217">Yes</span></span> | <span data-ttu-id="bb26f-218">Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="bb26f-218">Finance and Operations apps</span></span> | <span data-ttu-id="bb26f-219">있음</span><span class="sxs-lookup"><span data-stu-id="bb26f-219">Yes</span></span> | <span data-ttu-id="bb26f-220">예, Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="bb26f-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="bb26f-221">**Project Operations 통합 실제(msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="bb26f-222">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-222">No</span></span> | <span data-ttu-id="bb26f-223">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-223">No</span></span> | <span data-ttu-id="bb26f-224">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-224">N\A</span></span> | <span data-ttu-id="bb26f-225">예</span><span class="sxs-lookup"><span data-stu-id="bb26f-225">Yes</span></span> | <span data-ttu-id="bb26f-226">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-226">No</span></span> |
| <span data-ttu-id="bb26f-227">**프로젝트 계약 내용(salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="bb26f-228">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-228">No</span></span> | <span data-ttu-id="bb26f-229">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-229">No</span></span> | <span data-ttu-id="bb26f-230">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-230">N\A</span></span> | <span data-ttu-id="bb26f-231">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-231">No</span></span> | <span data-ttu-id="bb26f-232">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-232">No</span></span> |
| <span data-ttu-id="bb26f-233">**프로젝트 트랜잭션 관계를 위한 통합 엔터티(msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="bb26f-234">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-234">No</span></span> | <span data-ttu-id="bb26f-235">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-235">No</span></span> | <span data-ttu-id="bb26f-236">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-236">N\A</span></span> | <span data-ttu-id="bb26f-237">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-237">No</span></span> | <span data-ttu-id="bb26f-238">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-238">N\A</span></span> |
| <span data-ttu-id="bb26f-239">**Project Operations 통합 계약 내용 중요 시점(msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="bb26f-240">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-240">No</span></span> | <span data-ttu-id="bb26f-241">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-241">No</span></span> | <span data-ttu-id="bb26f-242">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-242">N\A</span></span> | <span data-ttu-id="bb26f-243">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-243">No</span></span> | <span data-ttu-id="bb26f-244">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-244">N\A</span></span> |
| <span data-ttu-id="bb26f-245">**경비 추정용 Project Operations 통합 엔터티(msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="bb26f-246">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-246">No</span></span> | <span data-ttu-id="bb26f-247">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-247">No</span></span> | <span data-ttu-id="bb26f-248">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-248">N\A</span></span> | <span data-ttu-id="bb26f-249">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-249">No</span></span> | <span data-ttu-id="bb26f-250">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-250">N\A</span></span> |
| <span data-ttu-id="bb26f-251">**Project Operations 통합 프로젝트 경비 범주 내보내기 엔터티(msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="bb26f-252">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-252">No</span></span> | <span data-ttu-id="bb26f-253">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-253">No</span></span> | <span data-ttu-id="bb26f-254">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-254">N\A</span></span> | <span data-ttu-id="bb26f-255">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-255">No</span></span> | <span data-ttu-id="bb26f-256">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-256">N\A</span></span> |
| <span data-ttu-id="bb26f-257">**Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="bb26f-258">예</span><span class="sxs-lookup"><span data-stu-id="bb26f-258">Yes</span></span> | <span data-ttu-id="bb26f-259">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-259">No</span></span> | <span data-ttu-id="bb26f-260">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-260">N\A</span></span> | <span data-ttu-id="bb26f-261">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-261">No</span></span> | <span data-ttu-id="bb26f-262">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-262">N\A</span></span> |
| <span data-ttu-id="bb26f-263">**시간 추정용 Project Operations 통합 엔터티(msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="bb26f-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="bb26f-264">예</span><span class="sxs-lookup"><span data-stu-id="bb26f-264">Yes</span></span> | <span data-ttu-id="bb26f-265">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-265">No</span></span> | <span data-ttu-id="bb26f-266">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-266">N\A</span></span> | <span data-ttu-id="bb26f-267">없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-267">No</span></span> | <span data-ttu-id="bb26f-268">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bb26f-268">N\A</span></span> |


4. <span data-ttu-id="bb26f-269">엔터티를 새로 고치려면 맵 이름을 선택한 다음 **엔터티 새로 고침** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![맵 새로 고침](./media/20RefreshMapping.png)

5. <span data-ttu-id="bb26f-271">새로 고침이 완료된 후 맵을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="bb26f-272">다음 맵을 활성화하기 전에 테이블의 맵이 **실행 중** 상태인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="bb26f-273">많은 수의 필수 구성 요소가 있는 맵을 실행하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="bb26f-274">필수 구성 요소가 있는 맵을 실행하려면 **관련 엔터티 맵 표시** 토글을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="bb26f-275">테이블에 **필수 구성 요소 초기 동기화** 가 **아니요** 로 나타나는 경우 실행하기 전에 모든 필수 구성 요소 맵에서 **초기 동기화** 플래그가 **끄기** 인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![맵 실행](./media/21RunMap.png)

6. <span data-ttu-id="bb26f-277">모든 프로젝트 관련 맵이 실행 중 상태인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-277">Validate all project related maps are in the running state.</span></span>

![모든 맵 실행 중](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="bb26f-279">Project Operations용 CDS 에 구성 데이터 적용(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="bb26f-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="bb26f-280">Finance 환경에 데모 데이터를 적용한 경우 [Project Operations에 대해 Common Data Service에서 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md)을 참조하여 CDS 환경에 데모 데이터를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="bb26f-281">이제 Project Operations 환경이 프로비전 및 구성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bb26f-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]