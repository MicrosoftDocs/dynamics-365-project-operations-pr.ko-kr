---
title: 프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정
description: 이 항목은 프로젝트 팀에 명명된 리소스를 예약하는 것과 작업에 배정하는 방법에 대한 정보를 제공합니다.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291447"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="46444-103">프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정</span><span class="sxs-lookup"><span data-stu-id="46444-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="46444-104">명명된 리소스를 팀에 직접 예약하여 프로젝트 팀에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="46444-105">이렇게 하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="46444-106">Project Service Automation에서 **프로젝트** 로 가서, 예약할 프로젝트 열기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="46444-107">**프로젝트** 페이지의 **팀** 탭에서 **신규** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![팀 탭에서 팀원 추가](media/RM-how-to-1.png)

3. <span data-ttu-id="46444-109">**프로젝트 팀원 빠른 생성** 대화 상자에서 예약 가능한 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="46444-110">**역할** 필드가 배정된 경우 리소스의 기본 역할로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="46444-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="46444-111">필요한 경우 역할을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="46444-112">리소스가 필요한 시작 날짜와 끝 날짜를 선택하고 리소스 능력의 배정 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="46444-113">팀원을 프로젝트 결재자로 지정하려면 **프로젝트 결재자** 필드에서 **예** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="46444-114">즉, 팀원이 이 프로젝트를 위해 제출된 시간 및 경비 항목을 결재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="46444-115">**저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-115">Click **Save**.</span></span>

![빠른 생성 양식에 팀원 추가](media/RM-how-to-2.png)


<span data-ttu-id="46444-117">이제 예약된 리소스를 프로젝트의 작업에 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="46444-118">**프로젝트** 페이지에서 **스케줄** 탭을 클릭하여 새 리소스에 작업을 배정합니다.</span><span class="sxs-lookup"><span data-stu-id="46444-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="46444-119">작업 그리드의 **리소스** 필드에서 시작된 리소스 선택기에 선택할 수 있는 팀원들이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46444-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![스케줄 탭의 작업에 팀원 배정](media/RM-how-to-3.png)

<span data-ttu-id="46444-121">Project Service Automation (PSA)의 버전 3에서는 리소스 예약과 작업 배정이 밀접하게 결합되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="46444-122">즉, 스케줄에서 리소스 선택기를 사용할 때 프로젝트에서 예약이 다루는 것보다 더 많은 시간 동안 팀원에게 작업을 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="46444-123">팀원 예약과 배정 사이의 차이점은 **팀** 탭에서 또는 **리소스 조정** 탭에서 확인할 수 있습니다. 또한 리소스에 대한 예약과 배정 사이의 차이를 보다 상세한 수준에서 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![리소스 조정 탭](media/RM-how-to-4.png)

<span data-ttu-id="46444-125">또한 **스케줄** 탭에서 리소스 선택기를 사용하여 아직 프로젝트 팀에 속하지 않은 예약 가능한 리소스를 검색하고 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="46444-126">그들은 리소스 선택기에서 **기타 리소스** 로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46444-126">These are shown in the resource picker as **Other Resources**.</span></span>

![팀원이 아닌 리소스를 작업에 배정](media/RM-how-to-5.png)

<span data-ttu-id="46444-128">이렇게 하면 리소스가 프로젝트 팀에 추가되고 작업에 배정되지만 예약은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![배정되었지만 예약이 없는 팀원](media/RM-how-to-6.png)

<span data-ttu-id="46444-130">**조정** 탭의 확장 예약 기능 또는 **스케줄 게시판** 을 사용하여 프로젝트에 리소스의 능력을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![리소스 조정 탭에서 팀원에 대한 예약 연장](media/RM-how-to-7.png)

<span data-ttu-id="46444-132">프로젝트에 팀원을 예약한 후 예약 정비를 사용하거나 스케줄 게시판을 사용하여 예약을 직접 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46444-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]