---
title: Project Finder Mobile 앱 기능 활성화
description: Project Finder Mobile 앱 기능 활성화(Project Service)
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753210"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Project Finder Mobile 앱 기능 활성화(Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

리소스가 휴대폰의 Project Finder Mobile 앱을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]와 사용하여 작업할 새 프로젝트를 찾고 기술 집합을 업데이트할 수 있습니다.  
  
 이 앱은 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] 모바일 및 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]에서 사용할 수 있습니다.  
  
 사용자가 프로젝트의 리소스 요구 사항을 확인하고 자신의 기술을 업데이트할 수 있도록 조직 구성 단위에 대한 파라미터 설정에서 몇 가지 옵션을 설정해야 합니다.  
  
> [!NOTE]
>  Project Finder Mobile 앱은 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]에서만 작동합니다(온-프레미스 설치에서는 작동하지 않음).  
  
1. **Project Service > 파라미터**로 이동합니다.  
  
2. Project Finder Mobile 앱 기능을 허용하는 데 사용할 파라미터 설정을 클릭합니다.  
  
3. **일반** 영역에서 **리소스 요구 사항을 리소스에 표시**를 **예**로 설정합니다.  
  
4. **리소스별 기술 업데이트 허용**을 **예**로 설정합니다.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   이는 전역 설정입니다. 프로젝트 관리자는 개별 프로젝트를 해당 프로젝트의 **프로젝트 팀** 페이지에서 표시할지 여부를 설정할 수 있습니다.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>이메일 알림  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]가 다음의 시간에 다음의 받는 사람에게 리소스 요청에 대한 전자 메일을 보냅니다.  
  
|받는 사람|이벤트|  
|---------------|-----------|  
|프로젝트 관리자|- 리소스가 Project Finder Mobile 앱을 사용하여 프로젝트에 등록하는 경우.|  
|리소스|- 리소스가 등록한 프로젝트 작업이 이미 다른 리소스에 의해 수행된 경우.<br />- 기술 승인 요청이 승인 또는 거부된 경우.<br />- 프로젝트 등록 요청이 승인 또는 거부된 경우.|  
  
## <a name="privacy-notice"></a>개인 정보 취급 방침  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>참고 항목  
 [리소스 설정](../project-service/set-up-resources.md)
