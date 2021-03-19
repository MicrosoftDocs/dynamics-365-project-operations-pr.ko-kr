---
title: Finance Cloud 호스팅 환경에 데모 데이터 적용
description: 이 항목에서는 Project Operations의 데모 데이터를 Dynamics 365 Finance 클라우드 호스팅 환경에 적용하는 방법을 설명합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289872"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="3884b-103">Finance Cloud 호스팅 환경에 데모 데이터 적용</span><span class="sxs-lookup"><span data-stu-id="3884b-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="3884b-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="3884b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3884b-105">이 항목은 Microsoft Dynamics 365 Finance 버전 10.0.13에만 적용되며 클라우드 호스팅 환경에서만 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="3884b-106">환경에 품질 업데이트를 적용하기 **전에** 이 항목의 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="3884b-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="3884b-107">LCS 프로젝트에서 **환경 세부 정보** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="3884b-108">RDP(원격 데스크톱 프로토콜)를 사용하여 환경에 연결하는 데 필요한 세부 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ 환경 세부 정보](./media/1EnvironmentDetails.png)

<span data-ttu-id="3884b-110">강조 표시된 자격 증명의 첫 번째 집합은 로컬 계정 자격 증명이며 원격 데스크톱 연결에 대한 하이퍼링크를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="3884b-111">자격 증명에는 환경 관리자 사용자 이름과 암호가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="3884b-112">두 번째 자격 증명 집합은 이 환경에서 SQL Server에 로그인하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="3884b-113">**로컬 계정** 의 하이퍼링크로 환경에 원격 연결하고 **로컬 계정 자격 증명** 을 사용하여 인증합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="3884b-114">**인터넷 정보 서비스** > **응용 프로그램 풀** > **AOSService** 로 이동하고 서비스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="3884b-115">SQL 데이터베이스를 계속 교체할 수 있도록 이 시점에서 서비스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS 중지](./media/2StopAOS.png)

4. <span data-ttu-id="3884b-117">**서비스** 로 이동하고 다음 두 항목을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="3884b-118">Microsoft Dynamics 365 Unified Operations: 일괄 처리 관리 서비스</span><span class="sxs-lookup"><span data-stu-id="3884b-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="3884b-119">Microsoft Dynamics 365 Unified Operations: 데이터 가져오기 내보내기 프레임워크</span><span class="sxs-lookup"><span data-stu-id="3884b-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![서비스 중지](./media/3StopServices.png)

5. <span data-ttu-id="3884b-121">Microsoft SQL Server Management Studio를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="3884b-122">SQL 서버 자격 증명으로 로그인하고 LCS의 **환경 세부 정보** 페이지에서 axdbadmin 사용자 및 암호를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="3884b-124">개체 탐색기 **데이터베이스** 에서 **AXDB** 를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="3884b-125">데이터베이스를 [다운로드 센터](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)에 있는 새 데이터베이스로 교체합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="3884b-126">원격으로 연결된 VM에 zip 파일을 복사하고 zip 콘텐츠를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="3884b-127">SQL Server Management Studio에서 **AxDB** 를 마우스 오른쪽 단추로 클릭한 다음 **과제** > **복원** > **데이터베이스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![데이터베이스 복원](./media/5RestoreDatabase.png)

9. <span data-ttu-id="3884b-129">**원본 장치** 를 선택하고 복사한 zip에서 추출한 파일로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![원본 장치](./media/6SourceDevice.png)

10. <span data-ttu-id="3884b-131">**옵션** 을 선택한 다음 **기존 데이터베이스 덮어쓰기** 및 **대상 데이터베이스에 대한 기존 연결 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="3884b-132">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-132">Select **OK**.</span></span>

![설정 복원](./media/7RestoreSetting.png)

<span data-ttu-id="3884b-134">AXDB 복원이 성공했다는 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="3884b-135">이 확인을 받은 후 SQL Services Management Studio를 닫을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="3884b-136">**인터넷 정보 서비스** > **응용 프로그램 풀** > **AOSService** 로 다시 이동하고 AOSService를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="3884b-137">**서비스** 로 이동하고 이전에 중지한 두 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="3884b-138">이 VM에서 AdminUserProvisioning 도구를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="3884b-139">K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 아래에서 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="3884b-140">**이메일 주소** 필드에서 사용자 주소를 사용하여 .ext 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="3884b-141">**제출** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-141">Select **Submit**.</span></span>

![관리 사용자 프로비전](./media/8AdminUserProvisioning.png)

<span data-ttu-id="3884b-143">완료하는 데 몇 분 정도 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="3884b-144">관리 사용자가 성공적으로 업데이트되었다는 확인 메시지를 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="3884b-145">마지막으로 관리자 권한으로 명령 프롬프트를 실행하고 iisreset을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS 초기화](./media/9IISReset.png)

18. <span data-ttu-id="3884b-147">원격 데스크톱 세션을 닫고 LCS **환경 세부 정보** 페이지를 사용하여 환경에 로그인하여 예상대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3884b-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]