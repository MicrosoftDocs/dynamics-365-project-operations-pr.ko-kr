---
title: 팀 구성원 유지
description: 이 항목은 프로젝트 팀에 명명된 리소스를 예약하는 것과 작업에 배정하는 것에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286841"
---
# <a name="maintain-team-members"></a><span data-ttu-id="93b20-103">팀 구성원 유지</span><span class="sxs-lookup"><span data-stu-id="93b20-103">Maintain team members</span></span>

<span data-ttu-id="93b20-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="93b20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="93b20-105">명명된 리소스를 팀에 직접 예약하여 프로젝트 팀에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="93b20-106">Dynamics 365 Project Operations에서 **프로젝트** 로 가서, 예약할 프로젝트 열기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="93b20-107">**프로젝트** 페이지의 **팀** 탭에서 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="93b20-108">**프로젝트 팀원 빠른 생성** 대화 상자에서 예약 가능한 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="93b20-109">**역할** 필드가 배정된 경우 리소스의 기본 역할로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="93b20-110">역할은 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-110">You can change the role.</span></span> 
4. <span data-ttu-id="93b20-111">리소스가 필요한 시작 날짜와 끝 날짜를 선택하고 리소스 능력의 배정 방법을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="93b20-112">팀원을 프로젝트 결재자로 지정하려면 **프로젝트 승인자** 필드에서 **예** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="93b20-113">즉, 팀원이 이 프로젝트를 위해 제출된 시간 및 경비 항목을 결재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="93b20-114">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-114">Select **Save**.</span></span>

<span data-ttu-id="93b20-115">이제 예약된 리소스를 프로젝트의 작업에 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="93b20-116">**프로젝트** 페이지의 **일정** 탭에서 새 리소스에 작업을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="93b20-117">작업 그리드의 **리소스** 필드에서 시작된 리소스 선택기에 선택할 수 있는 팀원들이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="93b20-118">Project Operations에서 리소스 예약과 작업 할당은 밀접하게 연결되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="93b20-119">일정에서 리소스 선택기를 사용할 때 프로젝트에서 예약이 다루는 것보다 더 많은 시간 동안 팀원에게 작업을 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="93b20-120">팀 구성원 예약 및 할당 간의 차이점은 **팀** 및 **리소스 조정** 탭에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="93b20-121">리소스에 대한 예약과 할당 간의 차이를 보다 세부적인 수준에서 조정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="93b20-122">**일정** 탭에서 리소스 선택기를 사용하여 아직 프로젝트 팀에 속하지 않은 예약 가능한 리소스를 검색하고 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="93b20-123">이러한 리소스는 리소스 선택기에서 **기타 리소스** 로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="93b20-124">리소스를 선택하면 리소스가 프로젝트 팀에 추가되고 작업에 배정되지만 예약은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="93b20-125">**조정** 탭의 확장 예약 기능 또는 **스케줄 게시판** 을 사용하여 프로젝트에 리소스의 능력을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="93b20-126">프로젝트에 팀원을 예약한 후 **예약 유지** 또는 **일정 게시판** 을 사용하여 예약을 직접 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b20-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]