---
title: 스케줄 게시판에서 프로젝트 예약을 만들기
description: 이 항목은 스케줄 게시판에서 프로젝트 예약을 만드는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286121"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="19c4c-103">스케줄 게시판에서 프로젝트 예약을 만들기</span><span class="sxs-lookup"><span data-stu-id="19c4c-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="19c4c-104">프로젝트의 **팀** 탭에서 직접 리소스를 예약하거나 일반 팀원 할당에서 리소스 요건을 생성한 다음 프로젝트 팀원과 함께 생성된 요건을 이행하는 방법으로 리소스를 프로젝트에 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="19c4c-105">스케줄 게시판에서 직접 프로젝트에 리소스를 예약할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="19c4c-106">방법은 세 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-106">There are three ways to do this:</span></span>

- <span data-ttu-id="19c4c-107">**생성된 리소스 요건에서 예약:** 일반 리소스를 만들고 프로젝트 내에서 작업을 할당한 후 리소스 요건을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="19c4c-108">**기본 요건에서 예약**: 기본 요건은 **프로젝트** 탭의 스케줄 게시판에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="19c4c-109">**새 리소스 요건에서 예약:** 리소스 요건을 처음부터 만들어 프로젝트와 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="19c4c-110">스케줄 게시판에서 리소스 요건은 **요건 열기** 탭에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="19c4c-111">생성된 리소스 요구 사항에서 예약</span><span class="sxs-lookup"><span data-stu-id="19c4c-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="19c4c-112">일반 리소스를 만들고 프로젝트 내에서 한 개 이상의 과업을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="19c4c-113">그런 다음 일반 팀원에서 리소스 요건을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="19c4c-114">스케줄 게시판에서 이 리소스는 **요건 열기** 탭에 표시됩니다. 열려 있는 요건이 많은 경우 표에서 열 필터를 사용해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="19c4c-115">![일정 게시판의 요구 사항 열기 탭](media/FAQ-Project-Booking-Schedule-Board-1.png "예약 및 할당 테이블의 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="19c4c-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="19c4c-116">요구 사항을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-116">Select the requirement.</span></span> <span data-ttu-id="19c4c-117">선택된 행의 맨 위에 **가용성 찾기** 탭이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="19c4c-118">이 탭을 선택하면 스케줄 게시판의 일정 도우미 모드가 시작되고 리소스 요건을 충족하는 사용 가능한 리소스가 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="19c4c-119">그 후에 리소스를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="19c4c-120">스케줄 게시판 아래쪽에서 선택된 행을 위에 있는 그리드의 리소스 셀로 끌어다 놓을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="19c4c-121">끌어다 놓으면 오른쪽에 **리소스 예약 만들기** 패널이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="19c4c-122">**예약** 을 선택하면 프로젝트 팀에 리소스가 예약됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-122">Selecting **Book** books the resource onto the project team.</span></span>

![리소스 예약 패널 만들기](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="19c4c-124">기본 요구 사항에서 예약</span><span class="sxs-lookup"><span data-stu-id="19c4c-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="19c4c-125">Project Service에서 프로젝트를 만들면 기본 요구 사항이라는 리소스 요구 사항이 자동으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="19c4c-126">이는 요건을 생성하거나 처음부터 만들지 않고 스케줄 게시판으로 리소스를 신속하게 예약하는 데 사용되는 빈 요건입니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="19c4c-127">요건이 비어 있으므로 할당 방법과 시간(해당되는 경우) 뿐만 아니라 날짜를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="19c4c-128">기본 요건으로 리소스를 예약하려면 스케줄 게시판에서 **프로젝트** 탭을 선택하십시오. 프로젝트가 많은 경우 **프로젝트** 열의 열 필터를 사용해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="19c4c-129">![일정 게시판의 열 필터](media/FAQ-Project-Booking-Schedule-Board-2.png "예약 및 할당 테이블의 스크린샷")</span><span class="sxs-lookup"><span data-stu-id="19c4c-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="19c4c-130">이름으로서 프로젝트 이름만 가지고 있고 지속 시간이 제로(0)인 요건을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="19c4c-131">행에 나타나는 **사용 가능성 찾기** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="19c4c-132">그러면 스케줄 도우미 모드에 스케줄 게시판이 배치되고 프로젝트에 예약할 수 있는 사용 가능한 리소스가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="19c4c-133">**기본 요건** 이 기간이 제로(0)인 빈 요건이므로 리소스를 선택하고 예약할 때 **리소스 예약 만들기** 패널에서 기간을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="19c4c-134">또한 스케줄 게시판의 맨 아래에 있는 **프로젝트 기본 요건** 을 선택하여 리소스에 끌어다 놓아 예약할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="19c4c-135">**기본 요건** 이 기간이 제로(0)인 빈 요건이므로 리소스를 선택하고 예약할 때 **리소스 예약 만들기** 패널에서 기간을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="19c4c-136">스케줄 게시판의 **기본 요건** 을 통해 리소스를 예약하면 할당 없이 프로젝트 팀에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="19c4c-137">새로운 리소스 요구 사항에서 예약</span><span class="sxs-lookup"><span data-stu-id="19c4c-137">Book from a new resource requirement</span></span>
<span data-ttu-id="19c4c-138">그 다음 단계를 완료하여 새 리소스 요건에서 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="19c4c-139">**리소스 요건** 으로 이동하고 **신규** 를 선택하여 새 리소스 요건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="19c4c-140">**프로젝트** 탭에서 프로젝트에 요건을 연계할 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="19c4c-141">스케줄 게시판에서 이 새 요건은 귀하가 이행할 수 있는 **요건 열기** 로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="19c4c-142">리소스를 예약하여 프로젝트 팀에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="19c4c-143">이제 리소스를 예약했으므로 과업을 수동으로 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c4c-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]