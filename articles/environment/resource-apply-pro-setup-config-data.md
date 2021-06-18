---
title: Common Data Service에서 구성 데이터 설정 및 적용
description: 이 항목은 Project Operations에서 구성 데이터를 설정하고 적용하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001299"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="33a8c-103">Common Data Service에서 구성 데이터 설정 및 적용</span><span class="sxs-lookup"><span data-stu-id="33a8c-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="33a8c-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="33a8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="33a8c-105">필수 조건</span><span class="sxs-lookup"><span data-stu-id="33a8c-105">Prerequisites</span></span>

<span data-ttu-id="33a8c-106">Common Data Service(CDS)에서 데이터 구성을 시작하기 전에 다음 전제 조건이 충족되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="33a8c-107">CDS 환경 및 Project Operations을 위한 Dynamics 365 Finance 환경을 프로비저닝합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="33a8c-108">Dynamics 365 Finance의 법인 정보는 CDS 환경에 공유됩니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="33a8c-109">즉 CDS의 **회사** 법인에는 다음과 같은 회사 기록이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="33a8c-110">THPM</span><span class="sxs-lookup"><span data-stu-id="33a8c-110">THPM</span></span>
  - <span data-ttu-id="33a8c-111">USPM</span><span class="sxs-lookup"><span data-stu-id="33a8c-111">USPM</span></span>
  - <span data-ttu-id="33a8c-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="33a8c-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="33a8c-113">설정 및 구성 데이터 설치</span><span class="sxs-lookup"><span data-stu-id="33a8c-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="33a8c-114">[설정 및 구성 데이터 패키지](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)를 다운로드, 차단 해제 및 압축 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="33a8c-115">압축이 풀린 폴더로 이동하여 *DataMigrationUtility* 실행 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="33a8c-116">Common Data Service 구성 마이그레이션(CMT) 마법사의 1 페이지에서 **데이터 가져오기** 를 선택한 다음 **계속** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![구성 마이그레이션](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="33a8c-118">CMT 마법사의 2페이지에서 **Microsoft 365** 를 **배포 유형** 으로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="33a8c-119">**사용 가능한 조직 목록 표시** 및 **고급 표시** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="33a8c-120">테넌트 지역을 선택하고 자격 증명을 입력한 다음 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![구성 로그인](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="33a8c-122">3 페이지의 테넌트의 조직 목록에서 데모 데이터를 가져올 조직을 선택하고 **로그인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="33a8c-123">4 페이지에서 압축을 푼 폴더에서 zip 파일 *SampleSetupAndConfigData* 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip 파일 선택](./media/3ZipFile.png)

![파일 선택](./media/4SelectAFile.png)

9. <span data-ttu-id="33a8c-126">Zip 파일을 선택한 후 **데이터 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-126">After the zip file is selected, select **Import Data**.</span></span>

![데이터 가져오기](./media/5ImportData.png)

10. <span data-ttu-id="33a8c-128">가져오기는 네트워크 속도에 따라 약 2~10분 동안 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="33a8c-129">가져오기가 완료되면 CMT 마법사를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="33a8c-130">조직에서 다음 26개 항목의 데이터를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="33a8c-131">통화</span><span class="sxs-lookup"><span data-stu-id="33a8c-131">Currency</span></span>
  - <span data-ttu-id="33a8c-132">계정 차트</span><span class="sxs-lookup"><span data-stu-id="33a8c-132">Chart of Accounts</span></span>
  - <span data-ttu-id="33a8c-133">회계 달력</span><span class="sxs-lookup"><span data-stu-id="33a8c-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="33a8c-134">통화 환율 유형</span><span class="sxs-lookup"><span data-stu-id="33a8c-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="33a8c-135">지불 날짜</span><span class="sxs-lookup"><span data-stu-id="33a8c-135">Payment Day</span></span>
  - <span data-ttu-id="33a8c-136">지불 일정</span><span class="sxs-lookup"><span data-stu-id="33a8c-136">Payment Schedule</span></span>
  - <span data-ttu-id="33a8c-137">지불 조건</span><span class="sxs-lookup"><span data-stu-id="33a8c-137">Payment Term</span></span>
  - <span data-ttu-id="33a8c-138">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="33a8c-138">Organizational Unit</span></span>
  - <span data-ttu-id="33a8c-139">연락처</span><span class="sxs-lookup"><span data-stu-id="33a8c-139">Contact</span></span>
  - <span data-ttu-id="33a8c-140">세금 그룹</span><span class="sxs-lookup"><span data-stu-id="33a8c-140">Tax Group</span></span>
  - <span data-ttu-id="33a8c-141">고객 그룹</span><span class="sxs-lookup"><span data-stu-id="33a8c-141">Customer Group</span></span>
  - <span data-ttu-id="33a8c-142">공급업체 그룹</span><span class="sxs-lookup"><span data-stu-id="33a8c-142">Vendor Group</span></span>
  - <span data-ttu-id="33a8c-143">단위</span><span class="sxs-lookup"><span data-stu-id="33a8c-143">Unit</span></span>
  - <span data-ttu-id="33a8c-144">단위 그룹</span><span class="sxs-lookup"><span data-stu-id="33a8c-144">Unit Group</span></span>
  - <span data-ttu-id="33a8c-145">가격표</span><span class="sxs-lookup"><span data-stu-id="33a8c-145">Price List</span></span>
  - <span data-ttu-id="33a8c-146">프로젝트 한도 가격표</span><span class="sxs-lookup"><span data-stu-id="33a8c-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="33a8c-147">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="33a8c-147">Invoice Frequency</span></span>
  - <span data-ttu-id="33a8c-148">예약 가능한 리소스 범주</span><span class="sxs-lookup"><span data-stu-id="33a8c-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="33a8c-149">거래 범주</span><span class="sxs-lookup"><span data-stu-id="33a8c-149">Transaction Category</span></span>
  - <span data-ttu-id="33a8c-150">경비 범주</span><span class="sxs-lookup"><span data-stu-id="33a8c-150">Expense Category</span></span>
  - <span data-ttu-id="33a8c-151">역할 가격</span><span class="sxs-lookup"><span data-stu-id="33a8c-151">Role Price</span></span>
  - <span data-ttu-id="33a8c-152">거래 범주 가격</span><span class="sxs-lookup"><span data-stu-id="33a8c-152">Transaction Category Price</span></span>
  - <span data-ttu-id="33a8c-153">특징</span><span class="sxs-lookup"><span data-stu-id="33a8c-153">Characteristic</span></span>
  - <span data-ttu-id="33a8c-154">예약 가능한 리소스</span><span class="sxs-lookup"><span data-stu-id="33a8c-154">Bookable Resource</span></span>
  - <span data-ttu-id="33a8c-155">예약 가능한 리소스 범주 연결</span><span class="sxs-lookup"><span data-stu-id="33a8c-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="33a8c-156">예약 가능한 리소스 특징</span><span class="sxs-lookup"><span data-stu-id="33a8c-156">Bookable Resource Characteristic</span></span>

![가져오기 완료](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="33a8c-158">Project Operations 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="33a8c-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="33a8c-159">CE 환경으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-159">Navigate to the CE environment.</span></span> <span data-ttu-id="33a8c-160">[Power Platform 관리 센터](https://admin.powerplatform.microsoft.com/environments)를 열고 환경을 선택한 다음 **환경 열기** 를 선택하면 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![환경 열기](./media/7OpenEnvironment.png)

2. <span data-ttu-id="33a8c-162">**프로젝트** > **리소스** 로 이동한 다음 **새로 만들기** 를 선택하여 사용자를 위해 예약 가능한 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![예약 가능한 리소스](./media/8BookableResources.png)

3. <span data-ttu-id="33a8c-164">**일반** 탭에서 관리 사용자를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="33a8c-165">시간대가 현재 있는 시간대와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-165">Verify that the time zone matches the one you are in.</span></span> 

![새 예약 가능한 리소스](./media/9NewBookableResource.png)

4. <span data-ttu-id="33a8c-167">**스케줄링** 탭의 **회사** 필드에서 **USPM** 회사를 선택한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![일정 탭](./media/10SchedulingTab.png)

5. <span data-ttu-id="33a8c-169">**작업 시간** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-169">Select the **Work hours** tab.</span></span>  

![근무 시간](./media/11WorkHours.png)

6. <span data-ttu-id="33a8c-171">일정에서 값을 두 번 클릭하고 **편집** > **시리즈의 모든 이벤트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![작업 일정](./media/12WorkCalendar.png)

7. <span data-ttu-id="33a8c-173">근무 시간을 8시간 근무일로 변경하고 주말을 휴무일로 표시하고 시간대가 자신의 시간대와 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="33a8c-174">**저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-174">Select **Save and close**.</span></span>

![일정 업데이트](./media/13UpdateCalendar.png)

9. <span data-ttu-id="33a8c-176">**설정** > **일정 템플릿** 으로 이동하고 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![일정 템플릿](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="33a8c-178">이름을 입력하고 생성한 템플릿 리소스를 선택한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![일정 템플릿 저장](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="33a8c-180">**매개 변수** 로 이동하고 레코드를 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![프로젝트 한도](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="33a8c-182">다음 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-182">Update the following fields:</span></span>

 - <span data-ttu-id="33a8c-183">**기본 회사**: USPM</span><span class="sxs-lookup"><span data-stu-id="33a8c-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="33a8c-184">**기본 조직 단위**:Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="33a8c-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="33a8c-185">**송장 빈도**: 일곱째 날과 마지막 날</span><span class="sxs-lookup"><span data-stu-id="33a8c-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="33a8c-186">**근무 시간 템플릿**: 생성한 템플릿으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="33a8c-187">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33a8c-187">Select **Save**.</span></span> 

![업데이트된 프로젝트 매개 변수](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
