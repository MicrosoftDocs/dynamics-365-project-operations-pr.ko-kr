---
title: Office 365 캘린더에서 프로젝트 및 예약 관리
description: Office 365 캘린더에서 프로젝트 및 예약을 관리하는 방법
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 575f3c94f886d12717496445d0e6357fdc01246b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000399"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="d2fcd-103">귀하의 캘린더에서 프로젝트 및 예약 관리 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d2fcd-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="d2fcd-104">단종: 이 기능은 단종되었으며 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="d2fcd-105">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정을 사용하여 개인 약속, 프로젝트 작업 예약 및 현장 서비스 작업 주문 할당을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="d2fcd-106">모든 것을 한곳에서 관리하여 하루 일정을 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="d2fcd-107">모임, 약속, 예약 및 작업이 모두 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="d2fcd-108">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 사용 중인 경우 Project Service 시간 항목 보기에서 개인 약속을 입력할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="d2fcd-109">이렇게 하면 프로젝트 및 리소스 관리자가 프로젝트에 대한 귀하의 가능 여부를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="d2fcd-110">시간도 함께 저장되므로 개인 약속에 대한 정보를 두 번 입력하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="d2fcd-111">간단하게 일정에서 개인 약속을 Project Service 시간 항목 보기로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="d2fcd-112">일정은 오늘부터 향후 4주까지의 프로젝트 및 작업 주문 예약을 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="d2fcd-113">이 설정은 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="d2fcd-114">동기화는 PSA에서 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정으로만 단방향 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="d2fcd-115">역순으로 동기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="d2fcd-116">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정을 사용하는 방법에 대한 자세한 내용은 [비즈니스용 웹상의 Outlook 일정](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="d2fcd-117">설치</span><span class="sxs-lookup"><span data-stu-id="d2fcd-117">Setup</span></span>  
 <span data-ttu-id="d2fcd-118">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정에서 예약을 보고 관리하기 전에 몇 가지를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="d2fcd-119">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 전역 관리자 또는 시스템 관리자 자격 증명이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="d2fcd-120">관리자가 전자 메일 서버 프로필을 구성하고 각 사용자가 자신의 사서함을 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d2fcd-121">[서버 쪽 동기화를 통해 전자 메일 처리 설정](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="d2fcd-121">[Set up email processing through server-side synchronization](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="d2fcd-122">조직에 대한 동기화 켜기(관리자 작업)</span><span class="sxs-lookup"><span data-stu-id="d2fcd-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="d2fcd-123">메인 메뉴에서 **설정** > **관리** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="d2fcd-124">**시스템 설정** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="d2fcd-125">**동기화** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="d2fcd-126">**리소스 예약을 동기화할 수 있는지 여부 선택** 아래의 **Outlook과 리소스 예약 동기화** 를 체크합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="d2fcd-127">사용자 프로필에 대한 동기화 켜기(사용자 작업)</span><span class="sxs-lookup"><span data-stu-id="d2fcd-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="d2fcd-128">화면 오른쪽 위에서 **설정** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="d2fcd-129">**옵션** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="d2fcd-130">**동기화** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="d2fcd-131">**Outlook과 리소스 예약 동기화** 아래의 **Outlook과 리소스 예약 동기화** 를 체크합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="d2fcd-132">개인 약속 가져오기(사용자 작업)</span><span class="sxs-lookup"><span data-stu-id="d2fcd-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="d2fcd-133">일정에서 개인 약속을 Project Service Automation 시간 항목 보기로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="d2fcd-134">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]의 일정을 열고 **데이터 가져오기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="d2fcd-135">필터 화면에서 **Exchange 약속** 을 선택한 다음 **적용** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="d2fcd-136">시스템에서는 이번 주에 제안된 항목으로 약속을 시간 항목 보기에 집어 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="d2fcd-137">다른 주에 대한 항목을 추가하려면 **이전** 또는 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="d2fcd-138">Project Service Automation 시간 항목 보기에 추가할 약속을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="d2fcd-139">**시간 항목** 팝업 상자에서 적절한 옵션을 선택하여 Project Service Automation 시간 항목 보기로 약속을 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="d2fcd-140">**저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fcd-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d2fcd-141">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d2fcd-141">See Also</span></span>  
 [<span data-ttu-id="d2fcd-142">시간, 비용 및 공동 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="d2fcd-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]