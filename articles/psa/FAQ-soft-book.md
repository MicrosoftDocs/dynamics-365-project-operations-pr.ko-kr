---
title: 리소스 가예약하기
description: 이 항목은 프로젝트 팀원을 임시 스케줄링하는 즉 가예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146446"
---
# <a name="soft-book-a-resource"></a><span data-ttu-id="65009-103">리소스 가예약하기</span><span class="sxs-lookup"><span data-stu-id="65009-103">Soft book a resource</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="65009-104">프로젝트 팀에 리소스를 임시로 예약하거나 "가예약"하여 리소스를 프로젝트에 할당할 계획을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-104">You can tentatively schedule or "soft book" a resource onto a project team to show that you plan to assign the resource to the project.</span></span> <span data-ttu-id="65009-105">가예약은 리소스의 사용 가능한 생산 능력을 소모하지 않으며, 가예약된 팀 구성원을 프로젝트 작업에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-105">Soft bookings don’t consume a resource’s available capacity, and you can assign soft-booked team members to project tasks.</span></span> <span data-ttu-id="65009-106">그러나 가예약은 리소스의 생산 능력을 소비하지 않기 때문에 동일한 기간 내에 다른 작업에 대 한 리소스를 "확정 예약"할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-106">However, because soft booking doesn’t consume a resource’s capacity, you can still "hard book" the resource for other tasks within the same period.</span></span> <span data-ttu-id="65009-107">일반 리소스는 가예약할 수 없으며, 가예약은 일반 리소스 요청을 이행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-107">Generic resources can’t be soft booked, nor can a soft booking fulfill a request for a generic resource.</span></span>

<span data-ttu-id="65009-108">가예약된 프로젝트 팀원은 **프로젝트** 페이지의 **팀** 탭에 나열되고, 가예약된 시간은 **명명된 팀원** 보기에서 **가예약된 시간** 열에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-108">Soft-booked project team members are listed on the **Team** tab of the **Project** page, with their soft-booked hours shown in the **Soft Booked Hours** column in the **Named Team Members** view.</span></span> <span data-ttu-id="65009-109">가예약된 된 팀원도 스케줄 게시판에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-109">Soft-booked team members are also listed on the Schedule board.</span></span> <span data-ttu-id="65009-110">그들은 가예약되었으므로 스케줄 게시판은 이러한 리소스에 대한 능력 소비를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-110">Because they are soft booked, the Schedule board doesn't show any consumption of capacity for these resources.</span></span> <span data-ttu-id="65009-111">가예약된 시간은 **조정** 탭에 표시되지 않으며, 스케줄 게시판의 **조정** 탭의 **예약 연장** 필드에도 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-111">Soft-booked time doesn’t show up on the **Reconciliation** tab, nor is it shown in the **Extend Bookings** field in the **Reconciliation** tab of the Schedule board.</span></span> 

<span data-ttu-id="65009-112">스케줄 게시판에서 직접 팀원을 프로젝트에 가예약하거나 또는 **팀** 탭에 팀원을 추가함으로써 가예약하는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-112">There are two ways to soft book a team member onto a project: directly from the Schedule board, or by adding the team member on the **Team** tab.</span></span> 

## <a name="soft-book-from-the-schedule-board"></a><span data-ttu-id="65009-113">스케줄 게시판에서 가예약</span><span class="sxs-lookup"><span data-stu-id="65009-113">Soft book from the Schedule board</span></span>
<span data-ttu-id="65009-114">다음 단계를 완료하여 스케줄 게시판에서 리소스를 가예약합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-114">Complete the following steps to soft book a resource from the Schedule board.</span></span> 

1. <span data-ttu-id="65009-115">스케줄 게시판을 열고, **예약 요건** 패널에서 **프로젝트** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-115">Open the Schedule board, and then in the **Booking Requirements** panel, select the **Project** tab.</span></span>
2. <span data-ttu-id="65009-116">리소스를 가예약하려는 프로젝트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-116">Find the project for which you want to soft book a resource.</span></span> <span data-ttu-id="65009-117">목록에 많은 수의 프로젝트가 있는 경우 **프로젝트** 열 표제를 선택한 다음 필터를 사용하여 하나 이상의 프로젝트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-117">If there are a large number of projects in the list, select the **Project** column header, and then use the filter to search for one or more projects.</span></span>
3. <span data-ttu-id="65009-118">프로젝트를 선택한 다음 리소스의 시간 그리드로 끌어다 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-118">Select the project, and then drag-and-drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="65009-119">**리소스 예약 만들기** 패널에서 시작 및 종료 날짜를 조정하고 **예약 상태** 를 **가예약** 으로 설정한 다음 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-119">In the **Create Resource Booking** panel, adjust the start and end date, set the **Booking Status** to **Soft**, and then set the hours.</span></span> 
6. <span data-ttu-id="65009-120">**예약** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-120">Click **Book**.</span></span> <span data-ttu-id="65009-121">이제 리소스가 프로젝트의 리소스로서 **팀** 탭에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-121">The resource now shows on the **Team** tab as a resource for the project.</span></span> <span data-ttu-id="65009-122">**거명된 팀원** 보기에서 **가예약 시간** 열에 가예약된 시간이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-122">On the **Named Team Member** view you’ll see the soft-booked hours in the **Soft Booked Hours** column.</span></span>

> [!NOTE]
> <span data-ttu-id="65009-123">이제 **스케줄** 탭에서 과업에 가예약을 할당할 수 있습니다. **조정** 탭은 확정 예약만 고려하므로 **조정** 탭에서 리소스는 과업 할당에 상대적인 예약 부족을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65009-123">You can now assign the soft booked to tasks on the **Schedule** tab. On the **Reconciliation** tab, the resource shows a booking deficit relative to the task assignment as the **Reconciliation** tab only considers hard-bookings.</span></span> <span data-ttu-id="65009-124">**예약 연장** 기능을 사용하여 리소스를 확정 예약하여 리소스 할당에 대한 확정 예약의 부족을 없앨 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-124">You can use the **Extend Bookings** feature to hard-book the resource to eliminate the deficit of hard-bookings against the resources assignments.</span></span> <span data-ttu-id="65009-125">**예약 정비** 를 사용하여 리소스에 대한 가예약을 수동으로 취소해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-125">You’ll have to manually cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

## <a name="soft-book-on-the-team-tab"></a><span data-ttu-id="65009-126">팀 탭의 가예약</span><span class="sxs-lookup"><span data-stu-id="65009-126">Soft book on the Team tab</span></span>

<span data-ttu-id="65009-127">**팀** 탭에서 직접 팀원을 추가한 다음 **예약 정비** 를 사용하여 예약 상태를 **확정 예약** 에서 **가예약** 으로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-127">You can add team members directly on the **Team** tab, and then change their booking status from **Hard** to **Soft** with **Maintain Bookings**.</span></span> <span data-ttu-id="65009-128">이러한 방식으로 팀원을 추가하면 할당 방법을 **없음** 으로 선택하지 않는 한 항상 확정 예약이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-128">When you add a team member this way, it will always result in a hard-booking unless you select the allocation method as **None**.</span></span>

<span data-ttu-id="65009-129">이 방법을 사용하려면 다음 단계를 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="65009-129">To use this method, complete the following steps.</span></span>

1. <span data-ttu-id="65009-130">**프로젝트** 페이지의 **팀** 탭에서 **신규** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-130">On the **Project** page, on the **Team** tab, click **New**.</span></span>
2. <span data-ttu-id="65009-131">예약 가능한 리소스, 역할, 시작 및 종료를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-131">Select the bookable resource, the role, and the from and to dates.</span></span>
3. <span data-ttu-id="65009-132">**없음** 이외의 할당 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-132">Select an allocation method other than **None**.</span></span>
4. <span data-ttu-id="65009-133">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-133">Select **Save**.</span></span> <span data-ttu-id="65009-134">표에 리소스가 표시되고 해당 시간이 **확정 예약 시간** 열에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-134">You’ll see the resource on the grid and their hours in the **Hard Booked Hours** column.</span></span>
5. <span data-ttu-id="65009-135">**예약 정비** 를 선택하여 리소스의 예약을 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-135">Maintain the resource’s bookings by selecting **Maintain Bookings**.</span></span>
6. <span data-ttu-id="65009-136">스케줄 게시판이 열리면 리소스를 확장하여 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-136">When the Schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="65009-137">**확정 예약** 으로 표시된 예약이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="65009-137">You will see the booking shown as **Hard**.</span></span>
7. <span data-ttu-id="65009-138">마우스 오른쪽 버튼으로 예약을 클릭하고 **상태 변경** 에서 **가예약하기** \> **가예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-138">Right-click the booking, and under **Change Status**, select **Soft Book** \> **Soft**.</span></span> <span data-ttu-id="65009-139">이제 예약 상태가 **가예약** 이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-139">The booking status is now **Soft**.</span></span>
8. <span data-ttu-id="65009-140">스케줄 게시판을 닫은 후에는 **거명된 팀원** 보기를 볼 때 리소스의 시간이 **팀** 탭 그리드의 **확정 예약된 시간** 열에서 **가예약된 시간** 열로 이동된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-140">After you close the Schedule board, you’ll see that the hours for the resource have moved from the **Hard Booked Hours** column to the **Soft Booked Hours** on the **Team** tab grid, when looking at the **Named Team Members** view.</span></span>

> [!NOTE]
> <span data-ttu-id="65009-141">**예약 정비** 를 사용하여 상태를 **확정 예약** 에서 **가예약** 으로 변경할 때, 리소스를 팀에 확정 예약한 다음 리소스에 과업을 할당하는 경우, 해당 리소스에 대한 과업 할당이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-141">When you use **Maintain Bookings** to change the status from **Hard** to **Soft**, if you hard-book a resource onto the team and then assign tasks to the resource, the task assignments for the resource are retained.</span></span> <span data-ttu-id="65009-142">그러나 **조정** 탭에서는 예약과 할당을 조정할 때 확정 예약만 고려되기 때문에 리소스 예약이 부족합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-142">However, on the **Reconciliation** tab, the resource will have a booking deficiency because only hard-bookings are considered when reconciling bookings versus assignments.</span></span> <span data-ttu-id="65009-143">**조정** 탭의 **예약 연장** 기능을 사용하여 리소스를 확정 예약하여 리소스 할당에 대한 확정 예약의 부족을 없앨 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-143">You can use the **Extend Bookings** feature on the **Reconciliation** tab to hard-book the resource to eliminate the deficit of hard bookings against the resources assignments.</span></span> <span data-ttu-id="65009-144">**예약 정비** 를 사용하여 리소스에 대한 가예약을 취소해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-144">You’ll have to cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

<span data-ttu-id="65009-145">가예약된 팀 구성원 리소스를 확정 예약된 팀 구성원으로 변경할 준비가 되면 다음을 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="65009-145">When you’re ready to change a soft-booked team member resource to a hard-booked team member, do the following:</span></span>

1. <span data-ttu-id="65009-146">스케줄 게시판에서 리소스를 연장하여 해당 예약을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-146">On the Schedule board, expand the resource to show their bookings.</span></span> <span data-ttu-id="65009-147">**가예약** 으로 표시된 예약이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="65009-147">You’ll see the booking shown as **Soft**.</span></span>
2. <span data-ttu-id="65009-148">예약을 마우스 오른쪽 버튼으로 클릭하고 **상태 변경** 에서 **확정 예약** \> **확정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="65009-148">Right-click the booking, and under **Change Status**, select **Hard Book** \> **Hard**.</span></span> <span data-ttu-id="65009-149">이제 예약 상태가 **확정** 이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65009-149">The booking status is now **Hard**.</span></span>
3. <span data-ttu-id="65009-150">스케줄 게시판을 닫고 프로젝트로 돌아가 **팀** 탭을 연 후에 **거명된 팀원** 보기에서 리소스의 시간이 **팀** 탭의 **가예약된 시간** 열에서 **확정 예약된 시간** 열로 이동된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-150">After you close the Schedule board, return to the project, and open the **Team** tab, you’ll see that the hours for the resource have moved from the **Soft Booked Hours** column to the **Hard Booked Hours** column on the **Team** tab when in the **Named Team Members** view.</span></span> <span data-ttu-id="65009-151">리소스가 작업에 할당된 경우 이제 예약이 확정 예약이므로 **조정** 탭에 더 이상 예약 부족이 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65009-151">If the resource was assigned to tasks, they’ll no longer show a booking deficit on the **Reconciliation** tab as their bookings are now hard.</span></span>

