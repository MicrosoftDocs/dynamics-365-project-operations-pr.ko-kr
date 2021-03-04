---
title: 데모 설정 및 구성 데이터 적용 - 라이트
description: 이 항목은 Project Operations에 대해 데모 설정 및 구성 데이터를 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089127"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="57d93-103">Project Operations의 데모 설정 및 구성 데이터 적용 - 라이트</span><span class="sxs-lookup"><span data-stu-id="57d93-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="57d93-104">_\*\*Lite 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="57d93-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="57d93-105">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="57d93-105">Prerequisites</span></span>

<span data-ttu-id="57d93-106">구성을 시작하기 전에 Dynamics 365 Project Operations용으로 프로비저닝된 Common Data Service(CDS) 환경이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="57d93-107">설명</span><span class="sxs-lookup"><span data-stu-id="57d93-107">Instructions</span></span>

1. <span data-ttu-id="57d93-108">[마스터 데이터 패키지](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="57d93-109">*ProjOpsDemoDataSetupAndMaster - Integrated CMT* 폴더로 이동하여 *DataMigrationUtility* 실행 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="57d93-110">Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기** 를 선택한 다음 **계속** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![구성 마이그레이션](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="57d93-112">CMT 마법사의 2페이지에서 **Microsoft 365** 를 **배포 유형** 으로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="57d93-113">**사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="57d93-114">테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![구성 로그인](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="57d93-116">3페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="57d93-117">4페이지에서 압축을 푼 폴더 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 에서 zip 파일 *MasterAndSetupData* 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![압축 파일](./media/3ZipFile.png)

   ![파일 선택](./media/4SelectAFile.png)

9. <span data-ttu-id="57d93-120">Zip 파일을 선택한 후 **데이터 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-120">After the zip file is selected, select **Import Data**.</span></span>

   ![데이터 가져오기](./media/5ImportData.png)

10. <span data-ttu-id="57d93-122">가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="57d93-123">가져오기가 완료되면 CMT 마법사를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="57d93-124">조직에서 다음 20개 항목의 데이터를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="57d93-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="57d93-125">통화</span><span class="sxs-lookup"><span data-stu-id="57d93-125">Currency</span></span>
    -   <span data-ttu-id="57d93-126">계정</span><span class="sxs-lookup"><span data-stu-id="57d93-126">Account</span></span>
    -   <span data-ttu-id="57d93-127">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="57d93-127">Organizational Unit</span></span>
    -   <span data-ttu-id="57d93-128">연락처</span><span class="sxs-lookup"><span data-stu-id="57d93-128">Contact</span></span>
    -   <span data-ttu-id="57d93-129">단위</span><span class="sxs-lookup"><span data-stu-id="57d93-129">Unit</span></span>
    -   <span data-ttu-id="57d93-130">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="57d93-130">Unit Group</span></span>
    -   <span data-ttu-id="57d93-131">가격표</span><span class="sxs-lookup"><span data-stu-id="57d93-131">Price List</span></span>
    -   <span data-ttu-id="57d93-132">프로젝트 한도 가격표</span><span class="sxs-lookup"><span data-stu-id="57d93-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="57d93-133">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="57d93-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="57d93-134">예약 가능한 리소스 범주</span><span class="sxs-lookup"><span data-stu-id="57d93-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="57d93-135">거래 범주</span><span class="sxs-lookup"><span data-stu-id="57d93-135">Transaction Category</span></span>
    -   <span data-ttu-id="57d93-136">경비 범주</span><span class="sxs-lookup"><span data-stu-id="57d93-136">Expense Category</span></span>
    -   <span data-ttu-id="57d93-137">역할 가격</span><span class="sxs-lookup"><span data-stu-id="57d93-137">Role Price</span></span>
    -   <span data-ttu-id="57d93-138">거래 범주 가격</span><span class="sxs-lookup"><span data-stu-id="57d93-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="57d93-139">특징</span><span class="sxs-lookup"><span data-stu-id="57d93-139">Characteristic</span></span>
    -   <span data-ttu-id="57d93-140">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="57d93-140">Bookable Resource</span></span>
    -   <span data-ttu-id="57d93-141">예약 가능한 리소스 범주 연결</span><span class="sxs-lookup"><span data-stu-id="57d93-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="57d93-142">예약 가능한 리소스 특징</span><span class="sxs-lookup"><span data-stu-id="57d93-142">Bookable Resource Characteristic</span></span>

    ![가져오기 완료](./media/6CompleteImport.png)
