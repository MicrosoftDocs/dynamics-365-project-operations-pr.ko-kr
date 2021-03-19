---
title: Finance 환경에서 Project Operations 업데이트
description: 이 항목은 Dynamics 365 Finance 환경에서 Project Operations를 업데이트하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291987"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="72e58-103">Finance 환경에서 Project Operations 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="72e58-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="72e58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="72e58-105">이 항목은 Dynamics 365 Finance  환경에서 Dynamics 365 Project Operations를 업데이트하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="72e58-106">Project Operations를 업데이트 5(UR5)로 업데이트하는 데 필요한 세 가지 절차가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="72e58-107">미리보기 프로젝트로 패키지 가져오기</span><span class="sxs-lookup"><span data-stu-id="72e58-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="72e58-108">업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="72e58-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="72e58-109">Dataverse 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="72e58-110">LCS 프로젝트로 패키지 가져오기</span><span class="sxs-lookup"><span data-stu-id="72e58-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="72e58-111">[Lifecycle Services(LCS)](https://lcs.dynamics.com/)에 프로젝트 담당자 또는 환경 관리자로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="72e58-112">프로젝트 목록에서 LCS 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="72e58-113">**프로젝트** 페이지의 **환경** 그룹에서 업데이트할 환경을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="72e58-114">환경이 실행되고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-114">Verify that the environment is running.</span></span> <span data-ttu-id="72e58-115">시작되지 않은 경우 환경을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="72e58-116">**새 릴리스** 섹션의 **사용 가능한 업데이트** 아래에서 10.0.15에 대한 **업데이트보기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![업데이트 보기 단추](media/view-update.png)

6. <span data-ttu-id="72e58-118">**바이너리 업데이트** 페이지에서 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="72e58-119">**업데이트 검토 및 저장** 페이지에서 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="72e58-120">**자산 라이브러리에 패키지 저장** 창이 열리면 패키지 이름을 입력하고 **패키지 저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="72e58-121">LCS가 패키지 저장을 마치면 **완료** 단추가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="72e58-122">**완료** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-122">Select **Done**.</span></span> <span data-ttu-id="72e58-123">LCS가 패키지를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-123">LCS will verify the package.</span></span> <span data-ttu-id="72e58-124">확인에는 몇 분 또는 최대 1시간이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="72e58-125">패키지 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="72e58-125">Apply the package update</span></span>

1. <span data-ttu-id="72e58-126">LCS의 **환경 세부 정보** 페이지에서 **유지 보수** > **업데이트 적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="72e58-127">목록에서 이전에 저장한 패키지를 선택한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="72e58-128">**예** 를 선택하여 패키지를 배포할지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![패키지 배포 확인 대화 상자](media/confirm-package-deployment.png)

4. <span data-ttu-id="72e58-130">**예** 를 선택하여 응용 프로그램을 업데이트할지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-130">Select **Yes** to confirm that you want to update the application.</span></span>

![응용 프로그램 업데이트 확인 대화 상자](media/confirm-application-update.png)

<span data-ttu-id="72e58-132">배포 및 응용 프로그램 업데이트가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="72e58-133">**환경 세부 정보** 페이지의 오른쪽 상단에서 환경 상태가 **서비스 중** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="72e58-134">약 2시간 후에 업데이트가 완료됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="72e58-135">응용 프로그램 릴리스 정보가 **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** 로 업데이트되고 환경 상태가 **배포됨** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="72e58-136">Dataverse 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="72e58-137">[Power Platform 관리 센터](https://admin.powerplatform.com/)에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="72e58-138">목록에서 Project Operations를 설치하는 데 사용한 환경을 찾아서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="72e58-139">**환경** 페이지에서 **리소스** > **Dynamics 365 앱** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="72e58-140">목록에서 **Microsoft Dynamics 365 Project Operations** 를 찾아 **상태** 열에서 **업데이트 사용 가능** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="72e58-141">**서비스 약관에 동의함** 확인란을 선택한 다음 **업데이트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="72e58-142">최신 버전의 솔루션이 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="72e58-143">설치가 완료되면 버전 4.5.0.134가 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="72e58-144">새 기능 구성</span><span class="sxs-lookup"><span data-stu-id="72e58-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="72e58-145">이중 쓰기 매핑 활성화</span><span class="sxs-lookup"><span data-stu-id="72e58-145">Enable dual-write mapping</span></span>

<span data-ttu-id="72e58-146">Finance 및 Dataverse 환경에 대한 업데이트를 완료한 후 필요한 이중 쓰기 매핑을 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="72e58-147">다음 절차를 완료하여 이중 쓰기 매핑을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="72e58-148">Customer Engagement 환경에서 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="72e58-149">데이터 엔터티 새로 고침</span><span class="sxs-lookup"><span data-stu-id="72e58-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="72e58-150">이중 쓰기 매핑 업데이트 및 실행</span><span class="sxs-lookup"><span data-stu-id="72e58-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="72e58-151">Dataverse 환경에서 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="72e58-152">UR5 업데이트의 일부로 엔티티의 보안 권한에 대한 다음 업데이트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="72e58-153">Dataverse 환경에서 **설정** 으로 이동하고 **시스템** 그룹에서 **보안** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse 환경 설정](media/Picture21.png)

2. <span data-ttu-id="72e58-155">**보안 역할** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="72e58-156">역할 목록에서 **이중 쓰기 앱 사용자** 를 선택하고 **사용자 지정 엔터티** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="72e58-157">역할에 다음에 대한 **읽기** 및 **다른 레코드에 추가** 권한이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="72e58-158">**통화 환율 유형**</span><span class="sxs-lookup"><span data-stu-id="72e58-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="72e58-159">**계정 차트**</span><span class="sxs-lookup"><span data-stu-id="72e58-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="72e58-160">**회계 달력**</span><span class="sxs-lookup"><span data-stu-id="72e58-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="72e58-161">**원장**</span><span class="sxs-lookup"><span data-stu-id="72e58-161">**Ledger**</span></span>

5. <span data-ttu-id="72e58-162">보안 역할이 업데이트되면 **설정** > **보안** > **팀** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="72e58-163">**이중 쓰기 앱 사용자** 역할이 팀에 적용되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="72e58-164">업데이트에서 데이터 엔터티 새로 고침</span><span class="sxs-lookup"><span data-stu-id="72e58-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="72e58-165">Finance 환경에서 **데이터 관리** 작업 영역을 열고 **프레임워크 매개 변수** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="72e58-166">**엔터티 설정** 탭에서 **엔터티 목록 새로 고침** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="72e58-167">**닫기** 를 선택하여 엔터티 새로 고침을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="72e58-168">이 프로세스는 완료하는 데 약 20분 정도 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="72e58-169">새로 고침이 완료되면 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="72e58-170">이중 쓰기 매핑 업데이트</span><span class="sxs-lookup"><span data-stu-id="72e58-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="72e58-171">**데이터 관리** 작업 영역에서 **이중 쓰기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="72e58-172">**솔루션 적용** 을 선택하고 목록에서 두 솔루션을 모두 선택한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="72e58-173">**이중 쓰기** 페이지에서 다음 테이블 맵을 선택한 다음 **중지** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="72e58-174">**Project Operations 통합 실제(msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="72e58-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="72e58-175">**Project Operations 통합 프로젝트 경비 범주(msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="72e58-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="72e58-176">**Project Operations 통합 실제 프로젝트 경비 내보내기 엔터티(msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="72e58-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="72e58-177">**테이블 맵 버전** 페이지에서 새 버전의 맵을 세 항목 각각에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="72e58-178">**이중 쓰기** 페이지에서 실행을 선택하여 맵을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="72e58-179">맵 목록에서 모든 필수 구성 요소가 있는 **원장(msdyn_ledgers)** 을 선택하고 **초기 동기화** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="72e58-180">**초기 동기화를 위한 마스터** 필드에서 **Finance and Operations 앱** 을 선택한 다음 **실행** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="72e58-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![원장 맵 동기화](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]