---
title: 데모 설정 및 구성 데이터 적용
description: 이 항목은 Project Operations에 대해 데모 설정 및 구성 데이터를 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948957"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="1de7e-103">Project Operations Lite 배포를 위한 데모 설정 및 구성 데이터 적용 - 견적 송장 거래</span><span class="sxs-lookup"><span data-stu-id="1de7e-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="1de7e-104">_\*\*Lite 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="1de7e-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="1de7e-105">[마스터 데이터 패키지](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="1de7e-106">*ProjOpsDemoDataSetupAndMaster - Integrated CMT* 폴더로 이동하여 *DataMigrationUtility* 실행 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1de7e-107">Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기**를 선택한 다음 **계속**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![구성 마이그레이션](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1de7e-109">CMT 마법사의 2페이지에서 **Office 365**를 **배포 유형**으로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1de7e-110">**사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1de7e-111">테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![구성 로그인](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1de7e-113">3페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="1de7e-114">4페이지에서 압축을 푼 폴더 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*에서 zip 파일 *MasterAndSetupData*를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![압축 파일](./media/3ZipFile.png)

![파일 선택](./media/4SelectAFile.png)

9. <span data-ttu-id="1de7e-117">Zip 파일을 선택한 후 **데이터 가져오기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-117">After the zip file is selected, select **Import Data**.</span></span>

![데이터 가져오기](./media/5ImportData.png)

10. <span data-ttu-id="1de7e-119">가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1de7e-120">가져오기가 완료되면 CMT 마법사를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1de7e-121">조직에서 다음 20개 항목의 데이터를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1de7e-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="1de7e-122">통화</span><span class="sxs-lookup"><span data-stu-id="1de7e-122">Currency</span></span>
- <span data-ttu-id="1de7e-123">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="1de7e-123">Organizational Unit</span></span>
- <span data-ttu-id="1de7e-124">연락처</span><span class="sxs-lookup"><span data-stu-id="1de7e-124">Contact</span></span>
- <span data-ttu-id="1de7e-125">세금 그룹</span><span class="sxs-lookup"><span data-stu-id="1de7e-125">Tax Group</span></span>
- <span data-ttu-id="1de7e-126">고객 그룹</span><span class="sxs-lookup"><span data-stu-id="1de7e-126">Customer Group</span></span>
- <span data-ttu-id="1de7e-127">단위</span><span class="sxs-lookup"><span data-stu-id="1de7e-127">Unit</span></span>
- <span data-ttu-id="1de7e-128">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="1de7e-128">Unit Group</span></span>
- <span data-ttu-id="1de7e-129">가격표</span><span class="sxs-lookup"><span data-stu-id="1de7e-129">Price List</span></span>
- <span data-ttu-id="1de7e-130">프로젝트 한도 가격표</span><span class="sxs-lookup"><span data-stu-id="1de7e-130">Project Parameter Price List</span></span>
- <span data-ttu-id="1de7e-131">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="1de7e-131">Invoice Frequency</span></span>
- <span data-ttu-id="1de7e-132">송장 빈도 세부 정보</span><span class="sxs-lookup"><span data-stu-id="1de7e-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="1de7e-133">예약 가능한 리소스 범주</span><span class="sxs-lookup"><span data-stu-id="1de7e-133">Bookable Resource Category</span></span>
- <span data-ttu-id="1de7e-134">거래 범주</span><span class="sxs-lookup"><span data-stu-id="1de7e-134">Transaction Category</span></span>
- <span data-ttu-id="1de7e-135">경비 범주</span><span class="sxs-lookup"><span data-stu-id="1de7e-135">Expense Category</span></span>
- <span data-ttu-id="1de7e-136">역할 가격</span><span class="sxs-lookup"><span data-stu-id="1de7e-136">Role Price</span></span>
- <span data-ttu-id="1de7e-137">거래 범주 가격</span><span class="sxs-lookup"><span data-stu-id="1de7e-137">Transaction Category Price</span></span>
- <span data-ttu-id="1de7e-138">특징</span><span class="sxs-lookup"><span data-stu-id="1de7e-138">Characteristic</span></span>
- <span data-ttu-id="1de7e-139">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="1de7e-139">Bookable Resource</span></span>
- <span data-ttu-id="1de7e-140">예약 가능한 리소스 범주 연결</span><span class="sxs-lookup"><span data-stu-id="1de7e-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="1de7e-141">예약 가능한 리소스 특징</span><span class="sxs-lookup"><span data-stu-id="1de7e-141">Bookable Resource Characteristic</span></span>

![가져오기 완료](./media/6CompleteImport.png)
