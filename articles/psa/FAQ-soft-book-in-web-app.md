---
title: 앱 버전 2.x에서 리소스를 "가예약"하는 방법은 무엇입니까?
description: 이 문서에서는 Project Service로 프로젝트 팀 구성원을 가예약하는 방법을 설명합니다.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286031"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="b698e-103">웹 앱(Project Service 앱 v2.x)의 리소스를 "가예약"하는 방법은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="b698e-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b698e-104">프로젝트 팀에 리소스를 임시로 예약하거나 "가예약"하여 리소스를 프로젝트에 할당할 계획을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="b698e-105">가예약은 리소스의 가용 생산 능력을 소모하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="b698e-106">가예약된 팀 구성원은 프로젝트 작업에 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="b698e-107">할당 노력을 충당하기에 충분한 확정 예약 시간이 있다고 가정할 경우, 확정 예약 상태 및 커밋된 커밋 유형을 가진 리소스만 작업에 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="b698e-108">가예약된 프로젝트 팀 구성원은 가예약 열에 표시된 가예약 시간을 사용하여 팀 구성원 표에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="b698e-109">또한 일정 게시판에도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-109">They also show up on the schedule board.</span></span> <span data-ttu-id="b698e-110">다시 말하지만, 가예약은 리소스의 생산 능력을 소비하지 않기 때문에 생산 능력의 소비를 나타내지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="b698e-111">Project Service 버전 2.x를 사용하여 팀 구성원을 프로젝트에 가예약하는 방법은 세 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="b698e-112">일정 게시판을 사용하여 가예약하거나, 예약 정비 기능 또는 일반 리소스를 만들어 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="b698e-113">이러한 방법은 아래에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="b698e-114">일정 게시판으로 가예약</span><span class="sxs-lookup"><span data-stu-id="b698e-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="b698e-115">일정 게시판으로 가예약하려면 다음 절차를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="b698e-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="b698e-116">일정 게시판을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-116">Open the schedule board.</span></span>
2. <span data-ttu-id="b698e-117">일정 게시판 하단의 예약 요구 사항 패널에서 프로젝트 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="b698e-118">리소스를 가예약하려는 프로젝트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="b698e-119">프로젝트가 많을 경우 프로젝트 열 머리글을 클릭한 다음 필터를 사용하여 프로젝트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="b698e-120">프로젝트를 클릭한 다음 리소스의 시간 표로 끌어다 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="b698e-121">그러면 오른쪽에 리소스 예약 만들기 패널이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="b698e-122">시작 및 종료 날짜를 조정하고 예약 상태를 가예약으로 선택하고 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="b698e-123">예약을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-123">Click Book.</span></span>
7. <span data-ttu-id="b698e-124">프로젝트로 돌아가면 이제 리소스가 가예약 열에서 가예약된 시간이 있는 팀 구성원으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="b698e-125">팀에 리소스를 할당하기 위해 확정 예약을 해야 하므로 WBS(작업 분할 구조)의 작업에는 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="b698e-126">예약 정비 기능을 사용하여 가예약</span><span class="sxs-lookup"><span data-stu-id="b698e-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="b698e-127">예산 유지로 가예약하려면 다음 절차를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="b698e-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="b698e-128">팀 구성원 표에서 새로 만들기를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="b698e-129">예약 가능한 리소스, 역할, 시작/종료를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="b698e-130">없음 이외의 할당 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="b698e-131">전체 생산 능력</span><span class="sxs-lookup"><span data-stu-id="b698e-131">Full Capacity</span></span>
- <span data-ttu-id="b698e-132">백분율 생산 능력</span><span class="sxs-lookup"><span data-stu-id="b698e-132">Percentage Capacity</span></span>
- <span data-ttu-id="b698e-133">시간별 균등 분배</span><span class="sxs-lookup"><span data-stu-id="b698e-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="b698e-134">시간별 초기 단계 이익 배분</span><span class="sxs-lookup"><span data-stu-id="b698e-134">By Hours Front Load</span></span>
4. <span data-ttu-id="b698e-135">'저장'을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-135">Click Save.</span></span> <span data-ttu-id="b698e-136">팀 표에 리소스가 표시되고 해당 시간이 확정 예약으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="b698e-137">예약 정비를 클릭하여 리소스의 예약을 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="b698e-138">일정 게시판이 열리면 리소스를 확장하여 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="b698e-139">확정 예약으로 표시된 예약이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="b698e-140">예약을 마우스 오른쪽 단추로 클릭하고 상태 변경에서 가예약을 선택한 다음 가예약을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="b698e-141">이제 예약 상태가 가예약이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="b698e-142">일정 게시판을 닫으면 팀 구성원 표의 리소스에 대한 시간이 확정 예약에서 가예약으로 변경된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="b698e-143">리소스를 팀에 확정 예약한 다음 WBS에서 작업에 이를 할당하는 경우 예약 정비를 사용하여 확정 예약 상태를 가예약으로 변경하면 확정 예약된 리소스만 작업에 할당할 수 있으므로 해당 리소스에 대한 작업의 할당이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="b698e-144">일반 리소스를 만들어 가예약</span><span class="sxs-lookup"><span data-stu-id="b698e-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="b698e-145">일반 리소스 팀 구성원을 생성하고 일정 게시판 또는 리소스 요청을 수행하고 예약하는 동안 유형을 변경하여 가예약을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="b698e-146">이를 수행하려면 다음 절차를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="b698e-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="b698e-147">프로젝트 WBS에서 일반 팀 구성원을 생성하려는 작업에 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="b698e-148">프로젝트 팀 생성을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="b698e-149">프로젝트 팀 구성원 표에서 일반 리소스를 선택하고 예약을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="b698e-150">일정 게시판에서 예약하려는 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="b698e-151">일정 게시판의 리소스 예약 만들기 패널에서 예약 상태를 가예약으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="b698e-152">예약을 클릭하거나 예약 및 끝내기를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="b698e-153">일정 게시판을 닫으면 선택한 리소스가 가예약된 시간 및 할당된 시간으로 팀에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="b698e-154">또한 일반 리소스가 작업을 가예약된 팀 구성원에게 할당되었다는 지표로서 팀에 남아 있는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="b698e-155">가예약된 팀 구성원 리소스를 확정 예약된 팀 구성원으로 변경할 준비가 되면 작업에 할당할 수 있도록 다음을 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="b698e-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="b698e-156">해당 리소스를 선택하고 예약 정비를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="b698e-157">일정 게시판이 열리면 리소스를 확장하여 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="b698e-158">가예약으로 표시된 예약이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="b698e-159">예약을 마우스 오른쪽 단추로 클릭하고 상태 변경에서 확정 예약을 선택한 다음 확정 예약을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="b698e-160">이제 예약 상태가 확정 예약이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="b698e-161">일정 게시판을 닫으면 팀 구성원 표의 리소스에 대한 시간이 가예약에서 확정 예약으로 변경된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="b698e-162">이제 작업에 리소스를 할당할 수 있습니다(확정 예약 시간과 할당을 위한 작업의 작업량 시간 사이에 정렬이 제공됨).</span><span class="sxs-lookup"><span data-stu-id="b698e-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="b698e-163">위의 항목 #3에서 일반 리소스 이행 단계를 수행한 경우 가예약된 예약 가능한 리소스의 상태를 확정 예약으로 변경하면 일반 팀 구성원이 팀에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="b698e-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]