---
title: 새 환경 프로비전
description: 이 항목은 새 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642987"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="90e88-103">새 환경 프로비전</span><span class="sxs-lookup"><span data-stu-id="90e88-103">Provision a new environment</span></span>

<span data-ttu-id="90e88-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="90e88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="90e88-105">이 토픽은 리소스/비 재고 기반 시나리오를 위한 새 Dynamics 365 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="90e88-106">LCS 프로젝트에서 Project Operations 자동화 프로비전 활성화</span><span class="sxs-lookup"><span data-stu-id="90e88-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="90e88-107">다음 단계를 사용하여 LCS 프로젝트에 대한 Project Operations 자동화 프로비전 흐름을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="90e88-108">[LCS](https://lcs.dynamics.com/v2)로 이동하고 **미리 보기 기능 관리** 타일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="90e88-109">**미리 보기 기능** 목록에서 **Project Operations 기능** 을 선택하고 **미리 보기 기능 활성화됨** 을 선택하여 Project Operations를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="90e88-110">이 단계는 LCS 프로젝트당 한 번만 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="90e88-111">Project Operations 환경 프로비전</span><span class="sxs-lookup"><span data-stu-id="90e88-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="90e88-112">새로운 Dynamics 365 Finance [데모 환경](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 또는 [샌드박스/프로덕션 환경](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="90e88-113">**환경 프로비전** 마법사를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="90e88-114">선택한 응용 프로그램 버전이 10.0.13 이상인지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="90e88-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="90e88-115">Project Operations를 프로비전하려면 **고급 설정** 에서 **Common Data Service** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="90e88-116">**예** 를 선택하여 **Common Data Service 설정** 을 활성화한 다음 필수 필드에 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="90e88-117">Name</span><span class="sxs-lookup"><span data-stu-id="90e88-117">Name</span></span>
  - <span data-ttu-id="90e88-118">영역</span><span class="sxs-lookup"><span data-stu-id="90e88-118">Region</span></span>
  - <span data-ttu-id="90e88-119">언어</span><span class="sxs-lookup"><span data-stu-id="90e88-119">Language</span></span>
  - <span data-ttu-id="90e88-120">통화</span><span class="sxs-lookup"><span data-stu-id="90e88-120">Currency</span></span>
 
5. <span data-ttu-id="90e88-121">**Common Data Service 템플릿** 필드에서 **Project Operations** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="90e88-122">배포할 환경 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="90e88-123">구독 기반 평가판을 사용하면 30일 동안 CDS 환경을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![배포 설정](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="90e88-125">**수락** 을 선택하여 서비스 약관에 동의한 다음 **완료** 를 선택하여 배포 설정으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![배포 동의](./media/2DeploymentConsent.png)

7. <span data-ttu-id="90e88-127">마법사의 나머지 필수 필드를 완료하고 배포를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="90e88-128">환경 프로비전 시간은 환경 유형에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="90e88-129">프로비전에는 최대 6시간이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="90e88-130">배포가 성공적으로 완료되면 환경이 **배포됨** 으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="90e88-131">환경이 성공적으로 배포되었는지 확인하려면 **로그인** 을 선택하고 확인을 위해 환경에 로그온합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 환경 세부 정보](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="90e88-133">Project Operations Finance 데모 데이터 적용(선택 단계)</span><span class="sxs-lookup"><span data-stu-id="90e88-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="90e88-134">[이 문서](resource-apply-finance-demo-data.md)에 설명된 대로 Project Operations Finance 데모 데이터를 10.0.13 서비스 릴리스 클라우드 호스팅 환경에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="90e88-135">Finance 환경에 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="90e88-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="90e88-136">Project Operations에는 애플리케이션 버전이 **10.0.13(10.0.569.20009)** 이상인 Finance 환경이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="90e88-137">이 버전을 받으려면 Finance 환경에 품질 업데이트를 적용해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="90e88-138">LCS의 **환경 세부 정보** 페이지에서 **사용 가능한 업데이트** 섹션에서 **업데이트 보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![보기 업데이트](./media/5ViewUpdates.png)

2. <span data-ttu-id="90e88-140">**바이너리 업데이트** 페이지에서 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-140">On the **Binary updates** page, select **Save package.**</span></span>

![패키지 저장](./media/6SavePackage.png)

3. <span data-ttu-id="90e88-142">**모두 선택** 을 클릭한 다음 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-142">Click **Select all** and then select **Save package**.</span></span>

![업데이트 검토 및 저장](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="90e88-144">패키지의 이름과 설명을 입력한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="90e88-145">인터넷 연결에 따라 이 과정은 다소 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-145">Depending on the internet connection, this process might take some time.</span></span>

![자산 라이브러리에 패키지 업로드](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="90e88-147">패키지를 저장한 후 **완료** 를 선택하고 이 패키지를 LCS 프로젝트의 자산 라이브러리에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="90e88-148">패키지를 저장하고 유효성을 검사하는 데 15분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="90e88-149">업데이트를 적용하려면 LCS의 **환경 세부 정보** 페이지에서 **유지** > **업데이트 적용** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![환경 유지](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="90e88-151">업데이트 목록에서 생성한 패키지를 선택하고 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-151">In the updates list select the package you created, and select **Apply**.</span></span>

![업데이트 적용](./media/10ApplyUpdates.png)

<span data-ttu-id="90e88-153">환경 서비스는 다소 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-153">Environment servicing will take some time.</span></span> <span data-ttu-id="90e88-154">완료되면 환경이 배포된 상태로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-154">After it is complete, the environment will return to a deployed state.</span></span>

![배포된 환경](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="90e88-156">이중 쓰기 연결 설정</span><span class="sxs-lookup"><span data-stu-id="90e88-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="90e88-157">LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="90e88-158">**Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="90e88-159">링크가 완료된 후 **CDS for Apps에 대한 링크** 를 다시 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="90e88-160">Finance에서 이중 쓰기로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS에 대한 링크](./media/12LinktoCDS.png)

4. <span data-ttu-id="90e88-162">**솔루션 적용** 을 선택하여 통합에 매핑될 엔터티에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![솔루션 적용](./media/13ApplySolutions.png)

5. <span data-ttu-id="90e88-164">두 솔루션 **Dynamics 365 Finance and Operations 이중 쓰기 엔터티 맵** 과 **Dynamics 365 Project Operations 이중 쓰기 엔터티 맵** 을 모두 선택한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![솔루션 확인](./media/14ConfirmSolutions.png)

<span data-ttu-id="90e88-166">솔루션이 적용된 후 이중 쓰기 엔터티가 환경에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![솔루션 적용](./media/15ApplyingSolutions.png)

<span data-ttu-id="90e88-168">엔터티가 적용된 후 사용 가능한 모든 매핑이 환경에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![이중 쓰기 맵](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="90e88-170">업데이트 후 데이터 엔터티 새로 고침</span><span class="sxs-lookup"><span data-stu-id="90e88-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="90e88-171">Finance에서 **데이터 관리** 작업 영역으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-171">In Finance, go to the **Data management** workspace.</span></span>

![데이터 관리 작업 공간](./media/16DataManagement.png)

2. <span data-ttu-id="90e88-173">**프레임워크 매개 변수** 타일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-173">Select the **Framework parameters** tile.</span></span>

![프레임워크 매개 변수](./media/17FrameworkParameters.png)

3. <span data-ttu-id="90e88-175">**엔터티 설정** 페이지에서 **엔터티 목록 새로 고침** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![엔터티 목록 새로 고침](./media/18RefreshEntityList.png)

<span data-ttu-id="90e88-177">새로 고침에는 약 20분이 소요됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="90e88-178">완료되면 알림이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-178">You will receive an alert when it is complete.</span></span>

![새로 고침 확인](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="90e88-180">Project Operations 이중 쓰기 맵 실행</span><span class="sxs-lookup"><span data-stu-id="90e88-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="90e88-181">LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="90e88-182">**Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="90e88-183">링크를 선택하면 매핑의 엔터티 목록으로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="90e88-184">다음 표에 설명된 대로 맵을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="90e88-185">나열된 순서를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="90e88-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="90e88-186">**엔터티 맵**</span><span class="sxs-lookup"><span data-stu-id="90e88-186">**Entity Map**</span></span> | <span data-ttu-id="90e88-187">**엔터티 새로 고침**</span><span class="sxs-lookup"><span data-stu-id="90e88-187">**Refresh entity**</span></span> | <span data-ttu-id="90e88-188">**초기 동기화**</span><span class="sxs-lookup"><span data-stu-id="90e88-188">**Initial sync**</span></span> | <span data-ttu-id="90e88-189">**초기 동기화용 마스터**</span><span class="sxs-lookup"><span data-stu-id="90e88-189">**Master for initial sync**</span></span> | <span data-ttu-id="90e88-190">**필수 구성 요소 실행**</span><span class="sxs-lookup"><span data-stu-id="90e88-190">**Run prerequisites**</span></span> | <span data-ttu-id="90e88-191">**필수 구성 요소 초기 동기화**</span><span class="sxs-lookup"><span data-stu-id="90e88-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="90e88-192">**모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="90e88-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="90e88-193">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-193">No</span></span> | <span data-ttu-id="90e88-194">있음</span><span class="sxs-lookup"><span data-stu-id="90e88-194">Yes</span></span> | <span data-ttu-id="90e88-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90e88-195">Common Data Service</span></span> | <span data-ttu-id="90e88-196">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-196">No</span></span> | <span data-ttu-id="90e88-197">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-197">N\A</span></span> |
| <span data-ttu-id="90e88-198">**법인(cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="90e88-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="90e88-199">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-199">No</span></span> | <span data-ttu-id="90e88-200">있음</span><span class="sxs-lookup"><span data-stu-id="90e88-200">Yes</span></span> | <span data-ttu-id="90e88-201">Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="90e88-201">Finance and Operations apps</span></span> | <span data-ttu-id="90e88-202">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-202">No</span></span> | <span data-ttu-id="90e88-203">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-203">N\A</span></span> |
| <span data-ttu-id="90e88-204">**원장(msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="90e88-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="90e88-205">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-205">No</span></span> | <span data-ttu-id="90e88-206">있음</span><span class="sxs-lookup"><span data-stu-id="90e88-206">Yes</span></span> | <span data-ttu-id="90e88-207">Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="90e88-207">Finance and Operations apps</span></span> | <span data-ttu-id="90e88-208">있음</span><span class="sxs-lookup"><span data-stu-id="90e88-208">Yes</span></span> | <span data-ttu-id="90e88-209">예, Finance and Operations 앱</span><span class="sxs-lookup"><span data-stu-id="90e88-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="90e88-210">**Project Operations 통합 실제(msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="90e88-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="90e88-211">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-211">No</span></span> | <span data-ttu-id="90e88-212">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-212">No</span></span> | <span data-ttu-id="90e88-213">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-213">N\A</span></span> | <span data-ttu-id="90e88-214">예</span><span class="sxs-lookup"><span data-stu-id="90e88-214">Yes</span></span> | <span data-ttu-id="90e88-215">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-215">No</span></span> |
| <span data-ttu-id="90e88-216">**프로젝트 계약 내용(salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="90e88-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="90e88-217">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-217">No</span></span> | <span data-ttu-id="90e88-218">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-218">No</span></span> | <span data-ttu-id="90e88-219">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-219">N\A</span></span> | <span data-ttu-id="90e88-220">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-220">No</span></span> | <span data-ttu-id="90e88-221">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-221">No</span></span> |
| <span data-ttu-id="90e88-222">**프로젝트 트랜잭션 관계를 위한 통합 엔터티(msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="90e88-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="90e88-223">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-223">No</span></span> | <span data-ttu-id="90e88-224">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-224">No</span></span> | <span data-ttu-id="90e88-225">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-225">N\A</span></span> | <span data-ttu-id="90e88-226">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-226">No</span></span> | <span data-ttu-id="90e88-227">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-227">N\A</span></span> |
| <span data-ttu-id="90e88-228">**Project Operations 통합 계약 내용 중요 시점(msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="90e88-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="90e88-229">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-229">No</span></span> | <span data-ttu-id="90e88-230">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-230">No</span></span> | <span data-ttu-id="90e88-231">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-231">N\A</span></span> | <span data-ttu-id="90e88-232">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-232">No</span></span> | <span data-ttu-id="90e88-233">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-233">N\A</span></span> |
| <span data-ttu-id="90e88-234">**경비 추정용 Project Operations 통합 엔터티(msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="90e88-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="90e88-235">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-235">No</span></span> | <span data-ttu-id="90e88-236">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-236">No</span></span> | <span data-ttu-id="90e88-237">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-237">N\A</span></span> | <span data-ttu-id="90e88-238">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-238">No</span></span> | <span data-ttu-id="90e88-239">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-239">N\A</span></span> |
| <span data-ttu-id="90e88-240">**Project Operations 통합 프로젝트 경비 범주 내보내기 엔터티(msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="90e88-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="90e88-241">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-241">No</span></span> | <span data-ttu-id="90e88-242">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-242">No</span></span> | <span data-ttu-id="90e88-243">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-243">N\A</span></span> | <span data-ttu-id="90e88-244">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-244">No</span></span> | <span data-ttu-id="90e88-245">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-245">N\A</span></span> |
| <span data-ttu-id="90e88-246">**Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="90e88-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="90e88-247">예</span><span class="sxs-lookup"><span data-stu-id="90e88-247">Yes</span></span> | <span data-ttu-id="90e88-248">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-248">No</span></span> | <span data-ttu-id="90e88-249">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-249">N\A</span></span> | <span data-ttu-id="90e88-250">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-250">No</span></span> | <span data-ttu-id="90e88-251">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-251">N\A</span></span> |
| <span data-ttu-id="90e88-252">**시간 추정용 Project Operations 통합 엔터티(msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="90e88-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="90e88-253">예</span><span class="sxs-lookup"><span data-stu-id="90e88-253">Yes</span></span> | <span data-ttu-id="90e88-254">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-254">No</span></span> | <span data-ttu-id="90e88-255">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-255">N\A</span></span> | <span data-ttu-id="90e88-256">없음</span><span class="sxs-lookup"><span data-stu-id="90e88-256">No</span></span> | <span data-ttu-id="90e88-257">해당 없음</span><span class="sxs-lookup"><span data-stu-id="90e88-257">N\A</span></span> |


4. <span data-ttu-id="90e88-258">엔터티를 새로 고치려면 맵 이름을 선택한 다음 **엔터티 새로 고침** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![맵 새로 고침](./media/20RefreshMapping.png)

5. <span data-ttu-id="90e88-260">새로 고침이 완료된 후 맵을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="90e88-261">다음 맵을 활성화하기 전에 테이블의 맵이 **실행 중** 상태인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="90e88-262">많은 수의 필수 구성 요소가 있는 맵을 실행하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="90e88-263">필수 구성 요소가 있는 맵을 실행하려면 **관련 엔터티 맵 표시** 토글을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="90e88-264">테이블에 **필수 구성 요소 초기 동기화** 가 **아니요** 로 나타나는 경우 실행하기 전에 모든 필수 구성 요소 맵에서 **초기 동기화** 플래그가 **끄기** 인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![맵 실행](./media/21RunMap.png)

6. <span data-ttu-id="90e88-266">모든 프로젝트 관련 맵이 실행 중 상태인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-266">Validate all project related maps are in the running state.</span></span>

![모든 맵 실행 중](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="90e88-268">Project Operations용 CDS 에 구성 데이터 적용(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="90e88-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="90e88-269">Finance 환경에 데모 데이터를 적용한 경우 [Project Operations에 대해 Common Data Service에서 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md)을 참조하여 CDS 환경에 데모 데이터를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="90e88-270">이제 Project Operations 환경이 프로비전 및 구성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="90e88-270">Your Project Operations environment is now provisioned and configured.</span></span> 
