---
title: Project Operations용 Common Data Service에 구성 데이터 설정 및 적용
description: 이 항목은 Project Operations에서 구성 데이터를 설정하고 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079925"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="01277-103">Project Operations용 Common Data Service에 구성 데이터 설정 및 적용</span><span class="sxs-lookup"><span data-stu-id="01277-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="01277-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="01277-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="01277-105">설정 및 구성 데이터 설치</span><span class="sxs-lookup"><span data-stu-id="01277-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="01277-106">[설정 및 구성 데이터 패키지](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)를 다운로드, 차단 해제 및 압축 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="01277-107">압축이 풀린 폴더로 이동하여 *DataMigrationUtility* 실행 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="01277-108">Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기** 를 선택한 다음 **계속** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![구성 마이그레이션](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="01277-110">CMT 마법사의 2페이지에서 **Microsoft 365** 를 **배포 유형** 으로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="01277-111">**사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="01277-112">테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![구성 로그인](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="01277-114">3 페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="01277-115">4 페이지에서 압축을 푼 폴더에서 zip 파일 *SampleSetupAndConfigData* 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip 파일 선택](./media/3ZipFile.png)

![파일 선택](./media/4SelectAFile.png)

9. <span data-ttu-id="01277-118">Zip 파일을 선택한 후 **데이터 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-118">After the zip file is selected, select **Import Data**.</span></span>

![데이터 가져오기](./media/5ImportData.png)

10. <span data-ttu-id="01277-120">가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="01277-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="01277-121">가져오기가 완료되면 CMT 마법사를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="01277-122">조직에서 다음 19개 항목의 데이터를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="01277-123">통화</span><span class="sxs-lookup"><span data-stu-id="01277-123">Currency</span></span>
  - <span data-ttu-id="01277-124">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="01277-124">Organizational Unit</span></span>
  - <span data-ttu-id="01277-125">연락처</span><span class="sxs-lookup"><span data-stu-id="01277-125">Contact</span></span>
  - <span data-ttu-id="01277-126">세금 그룹</span><span class="sxs-lookup"><span data-stu-id="01277-126">Tax Group</span></span>
  - <span data-ttu-id="01277-127">고객 그룹</span><span class="sxs-lookup"><span data-stu-id="01277-127">Customer Group</span></span>
  - <span data-ttu-id="01277-128">단위</span><span class="sxs-lookup"><span data-stu-id="01277-128">Unit</span></span>
  - <span data-ttu-id="01277-129">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="01277-129">Unit Group</span></span>
  - <span data-ttu-id="01277-130">가격표</span><span class="sxs-lookup"><span data-stu-id="01277-130">Price List</span></span>
  - <span data-ttu-id="01277-131">프로젝트 한도 가격표</span><span class="sxs-lookup"><span data-stu-id="01277-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="01277-132">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="01277-132">Invoice Frequency</span></span>
  - <span data-ttu-id="01277-133">예약 가능한 리소스 범주</span><span class="sxs-lookup"><span data-stu-id="01277-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="01277-134">거래 범주</span><span class="sxs-lookup"><span data-stu-id="01277-134">Transaction Category</span></span>
  - <span data-ttu-id="01277-135">경비 범주</span><span class="sxs-lookup"><span data-stu-id="01277-135">Expense Category</span></span>
  - <span data-ttu-id="01277-136">역할 가격</span><span class="sxs-lookup"><span data-stu-id="01277-136">Role Price</span></span>
  - <span data-ttu-id="01277-137">거래 범주 가격</span><span class="sxs-lookup"><span data-stu-id="01277-137">Transaction Category Price</span></span>
  - <span data-ttu-id="01277-138">특징</span><span class="sxs-lookup"><span data-stu-id="01277-138">Characteristic</span></span>
  - <span data-ttu-id="01277-139">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="01277-139">Bookable Resource</span></span>
  - <span data-ttu-id="01277-140">예약 가능한 리소스 범주 연결</span><span class="sxs-lookup"><span data-stu-id="01277-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="01277-141">예약 가능한 리소스 특징</span><span class="sxs-lookup"><span data-stu-id="01277-141">Bookable Resource Characteristic</span></span>

![가져오기 완료](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="01277-143">Project Operations 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="01277-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="01277-144">CE 환경으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-144">Navigate to the CE environment.</span></span> <span data-ttu-id="01277-145">[Power Platform 관리 센터](https://admin.powerplatform.microsoft.com/environments)를 열고 환경을 선택한 다음 **환경 열기** 를 선택하면 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01277-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![환경 열기](./media/7OpenEnvironment.png)

2. <span data-ttu-id="01277-147">**프로젝트** > **리소스** 로 이동한 다음 **새로 만들기** 를 선택하여 사용자를 위해 예약 가능한 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01277-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![예약 가능한 리소스](./media/8BookableResources.png)

3. <span data-ttu-id="01277-149">**일반** 탭에서 관리 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="01277-150">시간대가 현재 있는 시간대와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-150">Verify that the time zone matches the one you are in.</span></span> 

![새 예약 가능한 리소스](./media/9NewBookableResource.png)

4. <span data-ttu-id="01277-152">**스케줄링** 탭의 **회사** 필드에서 **USPM** 회사를 선택한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![일정 탭](./media/10SchedulingTab.png)

5. <span data-ttu-id="01277-154">**작업 시간** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-154">Select the **Work hours** tab.</span></span>  

![근무 시간](./media/11WorkHours.png)

6. <span data-ttu-id="01277-156">일정에서 값을 두 번 클릭하고 **편집** > **시리즈의 모든 이벤트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![작업 일정](./media/12WorkCalendar.png)

7. <span data-ttu-id="01277-158">근무 시간을 8시간 근무일로 변경하고 주말을 휴무일로 표시하고 시간대가 자신의 시간대와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="01277-159">**저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-159">Select **Save and close**.</span></span>

![일정 업데이트](./media/13UpdateCalendar.png)

9. <span data-ttu-id="01277-161">**설정** > **일정 템플릿** 으로 이동하고 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![일정 템플릿](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="01277-163">이름을 입력하고 생성한 템플릿 리소스를 선택한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![일정 템플릿 저장](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="01277-165">**매개 변수** 로 이동하고 레코드를 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![프로젝트 한도](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="01277-167">다음 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-167">Update the following fields:</span></span>

 - <span data-ttu-id="01277-168">**기본 회사** : USPM</span><span class="sxs-lookup"><span data-stu-id="01277-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="01277-169">**기본 조직 구성 단위** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="01277-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="01277-170">**송장 빈도** : 일곱째 날과 마지막 날</span><span class="sxs-lookup"><span data-stu-id="01277-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="01277-171">**근무 시간 템플릿** : 생성한 템플릿으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="01277-172">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01277-172">Select **Save**.</span></span> 

![업데이트된 프로젝트 매개 변수](./media/17UpdatedProjectParameters.png)
