---
title: 프로젝트 자원 예약 성능
description: 이 항목은 많은 프로젝트에 대한 리소스 스케줄링 성능을 개선하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080035"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="d710b-103">프로젝트 자원 예약 성능</span><span class="sxs-lookup"><span data-stu-id="d710b-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="d710b-104">리소스 스케줄링과 관련된 성능 문제는 프로젝트 수가 수천 개에 달할 때 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="d710b-105">리소스 예약 성능을 향상시키기 위해 사용자가 리소스 가용성 양식을 시작하는 데 걸리는 시간을 줄일 수 있는 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="d710b-106">특히 이것은 리소스 용량 롤업 동기화 프로세스를 제거하고 **ResProjectResource** 리소스 조회 속도를 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="d710b-107">**ResRollup** 테이블은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d710b-108">리소스 용량 롤업 동기화 프로세스 또는 **ResProjectResource** 테이블에 종속성이 있는 경우 이 기능을 사용하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="d710b-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d710b-109">리소스 스케줄링 성능 향상 활성화</span><span class="sxs-lookup"><span data-stu-id="d710b-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="d710b-110">리소스 스케줄링 성능 향상을 사용하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="d710b-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="d710b-111">**기능 관리** > **모두** 로 이동하고 기능 목록에서 **프로젝트 리소스 스케줄링 성능 향상 기능 사용** 을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d710b-112">**지금 사용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="d710b-113">목록에서 기능을 찾을 수 없는 경우 **업데이트 확인** 을 선택하여 목록을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="d710b-114">브라우저를 새로 고친 다음 **프로젝트 관리 및 회계** > **주기적** > **프로젝트 리소스** > **모든 회사에서 리소스 캘린더 용량 동기화** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="d710b-115">**기존 용량 레코드 제거** 를  **예** 로 설정하여 이전 데이터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d710b-116">증분 데이터를 생성하려면 **아니요** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="d710b-117">**기간 코드** 필드에서 데이터를 생성해야 하는 기간을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d710b-118">기간 코드를 선택하면 시작 날짜와 종료 날짜를 정의할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="d710b-119">**기간 코드** 필드가 비어 있는 경우 데이터를 생성할 특정 시작 및 종료 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="d710b-120">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d710b-121">이것은 일반 데이터를 사용자 환경에 있는 모든 회사의 **ResCalendarCapacity** 테이블로 배포하며 하나의 법인에서만 실행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d710b-122">이 일괄 처리 작업의 데이터는 연관된 달력을 통해 리소스 용량을 계산하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="d710b-123">**프로젝트 관리 및 회계** > **주기적** > **프로젝트 리소스** > **모든 회사의 프로젝트 리소스 채우기** 로 이동한 다음 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="d710b-124">이는 **ResProjectResource** , **ResCalendarDateTimeRange** 및 **ResEffectiveDateTimeRange** 테이블에 있는 일반 데이터를 위한 데이터 업그레이드 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="d710b-125">**PSAPRojSchedRole.RootActivity** 필드의 값도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="d710b-126">이것이 실행되지 않으면 리소스 스케줄링 작업을 실행하려고 할 때 경고를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d710b-127">리소스 스케줄링 성능 향상 끄기</span><span class="sxs-lookup"><span data-stu-id="d710b-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="d710b-128">**기능 관리** > **모두** 로 이동하고 **프로젝트 리소스 스케줄링 성능 향상 기능 사용** 을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d710b-129">기능을 선택한 다음 **비활성화** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="d710b-130">브라우저를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-130">Refresh your browser.</span></span>
4. <span data-ttu-id="d710b-131">**프로젝트 관리 및 회계** > **주기적** > **용량 동기화** > **리소스 용량 롤업 동기화** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="d710b-132">**용량 롤업 동기화** 페이지에서 **기존 용량 레코드 제거** 를 **예** 로 설정하여 이전 데이터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d710b-133">증분 데이터를 생성하려면 **아니요** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="d710b-134">**기간 코드** 필드에서 데이터를 생성해야 하는 기간을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d710b-135">기간 코드를 선택하면 시작 날짜와 종료 날짜를 정의할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="d710b-136">**기간 코드** 필드가 비어 있는 경우 데이터를 생성할 특정 시작 및 종료 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="d710b-137">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d710b-138">이것은 일반 데이터를 사용자 환경에 있는 모든 회사의 **ResRollup** 테이블로 배포하며 하나의 법인에서만 실행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d710b-139">이 일괄 처리 작업은 모든 **리소스 가용성** 보기에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="d710b-140">이 일괄 처리 작업이 실행되지 않으면 **ResRollup** 데이터는 즉석에서 생성되므로 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d710b-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
