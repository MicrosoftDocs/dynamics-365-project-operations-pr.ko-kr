---
title: 표준 시간대 관리
description: 프로젝트가 생성될 때 시간대는 적용된 근무 시간 템플릿에 정의된 시간대를 기반으로 합니다.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997744"
---
# <a name="manage-time-zones"></a><span data-ttu-id="c3182-103">표준 시간대 관리</span><span class="sxs-lookup"><span data-stu-id="c3182-103">Manage time zones</span></span>

<span data-ttu-id="c3182-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="c3182-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="c3182-105">프로젝트</span><span class="sxs-lookup"><span data-stu-id="c3182-105">Projects</span></span>

<span data-ttu-id="c3182-106">프로젝트가 생성될 때 시간대는 적용된 근무 시간 템플릿에 정의된 시간대를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="c3182-107">**프로젝트** 에서 날짜는 항상 **작업** 탭을 제외하고 각 탭에 로그인한 사용자의 표준 시간대를 기준으로 합니다. 작업 분할 구조를 볼 때 날짜는 항상 프로젝트의 시간대로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="c3182-108">작업</span><span class="sxs-lookup"><span data-stu-id="c3182-108">Tasks</span></span>

<span data-ttu-id="c3182-109">작업이 생성되면 시작 시간, 종료 시간 및 시간/일은 프로젝트의 작업 시간에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="c3182-110">예를 들어 시간대가 -8 PST이고 근무 시간이 월요일 ~ 금요일 오전 9시 ~ 오후 5시인 프로젝트로 작업이 생성된 경우 할당없이 생성된 모든 작업은 시작 시간과 프로젝트 일정의 종료 시간을 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="c3182-111">표준 시간대로 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="c3182-111">Manage resources with time zones</span></span>

<span data-ttu-id="c3182-112">**예약 연장** 사용시 정확하고 예측 가능한 결과를 위해 충족해야 하는 두 가지 주요 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="c3182-113">사용자는 시스템의 **개인화 설정** 에 정의된 표준 시간대와 일치하도록 장치의 시간대를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Windows 10의 시간대 설정](media/reconcile-assignments-03.png)

  ![개인 맞춤 설정의 시간대 설정](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="c3182-116">예약 가능한 리소스에는 요청된 확장을 정의하는 데 사용되는 배분과 겹치는 최소 1분의 작업 시간이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="c3182-117">예를 들어 근무 시간이 오전 9시에서 오후 7시 사이인 다음 리소스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![리소스 배분 비교](media/reconcile-assignments-05.png)

<span data-ttu-id="c3182-119">아래 표는 다음을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-119">The following table shows:</span></span>

- <span data-ttu-id="c3182-120">프로젝트 일정 템플릿</span><span class="sxs-lookup"><span data-stu-id="c3182-120">A project calendar template</span></span>
- <span data-ttu-id="c3182-121">리소스 A :이 리소스는 일정이 같고 프로젝트와 동일한 시간대에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="c3182-122">예약 시작 시간은 오전 9시입니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="c3182-123">리소스 B: 이 리소스는 프로젝트와 다른 표준 시간대에 있으며 해당 표준 시간대의 오전 7시에 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="c3182-124">그러나 예약은 할당 배분의 가장 빠른 시작 시간이므로 오전 9시에 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="c3182-125">리소스 C 및 D: 리소스는 둘 모두 프로젝트와 서로 다른 표준 시간대에 있으며 예약은 사용 가능한 시작 시간보다 일찍 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="c3182-126">엔터티</span><span class="sxs-lookup"><span data-stu-id="c3182-126">Entity</span></span>  |<span data-ttu-id="c3182-127">달력</span><span class="sxs-lookup"><span data-stu-id="c3182-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="c3182-128">프로젝트 일정 템플릿</span><span class="sxs-lookup"><span data-stu-id="c3182-128">Project calendar template</span></span>   | ![프로젝트 일정](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c3182-130">리소스 A</span><span class="sxs-lookup"><span data-stu-id="c3182-130">Resource A</span></span>  | ![리소스 A 일정](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c3182-132">리소스 B</span><span class="sxs-lookup"><span data-stu-id="c3182-132">Resource B</span></span>  |  ![리소스 B 일정](media/reconcile-assignments-07.png) |
|<span data-ttu-id="c3182-134">리소스 C</span><span class="sxs-lookup"><span data-stu-id="c3182-134">Resource C</span></span>  |  ![리소스 C 일정](media/reconcile-assignments-08.png) |
|<span data-ttu-id="c3182-136">리소스 D</span><span class="sxs-lookup"><span data-stu-id="c3182-136">Resource D</span></span>  | ![리소스 D 일정](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="c3182-138">**조정** 보기로 이동할 때 리소스 할당 및 연관된 예약 부족이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![확장 전 조정 보기](media/reconcile-assignments-10.png)

<span data-ttu-id="c3182-140">각 리소스에 대해 예약 연장 기능이 사용된 후 각 리소스의 작업 시간이 부족의 윤곽과 겹치기 때문에 각 리소스에 대한 예약이 성공적으로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![예약 확장 후 조정 보기](media/reconcile-assignments-11.png) 

<span data-ttu-id="c3182-142">예약 세부 정보를 자세히 살펴보면 예약 시작 시간에 차이가 있음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="c3182-143">예약은 할당 윤곽의 시작 시간 이전에 시작되지 않고 리소스의 사용 가능한 시작 시간 이전에 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3182-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![일정 게시판에서 리소스의 새로운 예약](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]