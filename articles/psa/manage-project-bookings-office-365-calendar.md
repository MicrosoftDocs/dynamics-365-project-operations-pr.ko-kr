---
title: Office 365 캘린더에서 프로젝트 및 예약 관리
description: Office 365 캘린더에서 프로젝트 및 예약을 관리하는 방법
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: c575bd3deba5bcde2526ccfc598327917bf91642
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144466"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>귀하의 캘린더에서 프로젝트 및 예약 관리 (Project Service)

> [!Note]
> 단종: 이 기능은 단종되었으며 더 이상 사용할 수 없습니다.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정을 사용하여 개인 약속, 프로젝트 작업 예약 및 현장 서비스 작업 주문 할당을 표시합니다.  
  
 모든 것을 한곳에서 관리하여 하루 일정을 쉽게 관리할 수 있습니다. 모임, 약속, 예약 및 작업이 모두 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정에 제공됩니다.  
  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 사용 중인 경우 Project Service 시간 항목 보기에서 개인 약속을 입력할 수도 있습니다. 이렇게 하면 프로젝트 및 리소스 관리자가 프로젝트에 대한 귀하의 가능 여부를 알 수 있습니다. 시간도 함께 저장되므로 개인 약속에 대한 정보를 두 번 입력하지 않아도 됩니다. 간단하게 일정에서 개인 약속을 Project Service 시간 항목 보기로 가져올 수 있습니다.  
  
 일정은 오늘부터 향후 4주까지의 프로젝트 및 작업 주문 예약을 동기화합니다. 이 설정은 변경할 수 없습니다.  
  
 동기화는 PSA에서 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정으로만 단방향 지원됩니다. 역순으로 동기화할 수 있습니다. 
  
 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정을 사용하는 방법에 대한 자세한 내용은 [비즈니스용 웹상의 Outlook 일정](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)을 참조하십시오.  
  
## <a name="setup"></a>설치  
 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 일정에서 예약을 보고 관리하기 전에 몇 가지를 설정해야 합니다.  
  
- [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 전역 관리자 또는 시스템 관리자 자격 증명이 필요합니다.  
  
- 관리자가 전자 메일 서버 프로필을 구성하고 각 사용자가 자신의 사서함을 구성해야 합니다. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [서버 쪽 동기화를 통해 전자 메일 처리 설정](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>조직에 대한 동기화 켜기(관리자 작업)  
  
1.  메인 메뉴에서 **설정** > **관리** 를 클릭합니다.  
  
2.  **시스템 설정** 을 클릭합니다.  
  
3.  **동기화** 탭을 클릭합니다.  
  
4.  **리소스 예약을 동기화할 수 있는지 여부 선택** 아래의 **Outlook과 리소스 예약 동기화** 를 체크합니다.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>사용자 프로필에 대한 동기화 켜기(사용자 작업)  
  
1.  화면 오른쪽 위에서 **설정** 단추를 클릭합니다.  
  
2.  **옵션** 을 클릭합니다.  
  
3.  **동기화** 탭을 클릭합니다.  
  
4.  **Outlook과 리소스 예약 동기화** 아래의 **Outlook과 리소스 예약 동기화** 를 체크합니다.  
  
## <a name="import-your-personal-appointments-user-task"></a>개인 약속 가져오기(사용자 작업)  
 일정에서 개인 약속을 Project Service Automation 시간 항목 보기로 가져올 수 있습니다.  
  
1. [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]의 일정을 열고 **데이터 가져오기** 를 클릭합니다.  
  
2. 필터 화면에서 **Exchange 약속** 을 선택한 다음 **적용** 을 클릭합니다.  
  
3. 시스템에서는 이번 주에 제안된 항목으로 약속을 시간 항목 보기에 집어 넣습니다. 다른 주에 대한 항목을 추가하려면 **이전** 또는 **다음** 을 클릭합니다.  
  
4. Project Service Automation 시간 항목 보기에 추가할 약속을 선택합니다.  
  
5. **시간 항목** 팝업 상자에서 적절한 옵션을 선택하여 Project Service Automation 시간 항목 보기로 약속을 변환합니다.  
  
6. **저장** 을 클릭합니다.  
  
### <a name="see-also"></a>참고 항목  
 [시간, 비용 및 공동 작업 가이드](../psa/time-expense-collaboration-guide.md)
