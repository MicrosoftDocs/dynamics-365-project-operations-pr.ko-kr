---
title: 프로젝트에 리소스 예약
description: 프로젝트에 대한 리소스 일정을 예약하는 방법(Project Service)
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282656"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="4cae5-103">프로젝트에 대한 리소스 일정 예약(Project Service)</span><span class="sxs-lookup"><span data-stu-id="4cae5-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4cae5-104">리소스 사용 가능 여부를 확인하여 예약된 리소스 상태를 전부 보거나, 보기를 기술, 팀, 위치 및 기타 옵션으로 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="4cae5-105">일정 게시판에는 리소스 및 사용 가능 여부에 대한 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="4cae5-106">**시간**, **일**, **주**, 또는 **월** 로 사용 가능성을 표시하도록 보기 모드를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="4cae5-107">일정 게시판을 사용하기 전에 설정하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="4cae5-108">자세한 내용은 [일정 보드 구성(Field Service 또는 Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cae5-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="4cae5-109">이전 버전을 사용 중인 경우 리소스 사용 가능 시간에 대해 [리소스 사용 가능한 시간 보기](../psa/view-resource-availability.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cae5-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="4cae5-110">일정 게시판 예약 기능, 지역 코드 입력, 위치 서비스를 사용하려면 지도를 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="4cae5-111">메인 메뉴에서 **리소스 예약** > **관리** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="4cae5-112">**예약 파라미터** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="4cae5-113">레코드를 열고 **Resource Scheduling Optimization** 섹션으로 아래로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="4cae5-114">**지도에 연결** 필드에서 **예** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="4cae5-115">약관에 동의하고 레코드를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="4cae5-116">메인 메뉴에서 **Project Service** > **일정 게시판** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="4cae5-117">여기에서 예약 요구 사항을 수동으로 예약하는 방법이 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="4cae5-118">사용자에게 맞는 방법을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="4cae5-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="4cae5-119">사용 가능한 리소스 찾기</span><span class="sxs-lookup"><span data-stu-id="4cae5-119">Find available resources</span></span>

1.  <span data-ttu-id="4cae5-120">**예약 요구 사항** 목록에서 예약되지 않은 예약을 마우스 오른쪽 단추로 클릭하고 다음 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="4cae5-121">**사용 가능성 찾기 - 현재 리소스** 를 선택하여 일정 게시판의 목록에서 사용 가능한 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="4cae5-122">**사용 가능성 찾기 - 모든 리소스** 를 선택하여 시스템의 리소스 목록에서 사용 가능한 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="4cae5-123">이렇게 하면 필터링을 통해 선택한 예약 요구 사항에 대한 옵션이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="4cae5-124">일정 게시판에서 타임 슬롯 중 사용 가능한 슬롯을 마우스 오른쪽 단추로 클릭하고 **여기에서 예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="4cae5-125">또는 예약 요구 사항을 사용 가능한 시간 슬롯에 끌어 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="4cae5-126">일별 보기를 사용하여 리소스를 예약하고 예약이 덜 된 리소스 찾기</span><span class="sxs-lookup"><span data-stu-id="4cae5-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="4cae5-127">일정 게시판에서 **보기 모드** 를 선택하고 **일** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="4cae5-128">리소스가 하루에 몇 시간 예약됐는지 그리고 여유 있는 날짜를 나타내는 표 보기가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="4cae5-129">예약을 원하는 리소스를 누른 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="4cae5-130">**리소스 예약(만들기)** 대화 상자에서 리소스를 예약하고자 하는 프로젝트와 예약 방법, 시작 및 종료 시각을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="4cae5-131">완료되면 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="4cae5-132">일정 게시판 보기</span><span class="sxs-lookup"><span data-stu-id="4cae5-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="4cae5-133">하단의 목록에서 예약되지 않은 예약 요구 사항을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="4cae5-134">예약 보드의 사용 가능한 리소스/시간 슬롯으로 예약 요구 사항을 끌어 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="4cae5-135">완료되면 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4cae5-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="4cae5-136">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="4cae5-136">Additional resources</span></span>  
 [<span data-ttu-id="4cae5-137">리소스 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="4cae5-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]