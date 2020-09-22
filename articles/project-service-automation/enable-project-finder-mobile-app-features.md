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
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="707a9-103">Project Finder Mobile 앱 기능 활성화(Project Service)</span><span class="sxs-lookup"><span data-stu-id="707a9-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="707a9-104">리소스가 휴대폰의 Project Finder Mobile 앱을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]와 사용하여 작업할 새 프로젝트를 찾고 기술 집합을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="707a9-105">이 앱은 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] 모바일 및 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="707a9-106">사용자가 프로젝트의 리소스 요구 사항을 확인하고 자신의 기술을 업데이트할 수 있도록 조직 구성 단위에 대한 파라미터 설정에서 몇 가지 옵션을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="707a9-107">Project Finder Mobile 앱은 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]에서만 작동합니다(온-프레미스 설치에서는 작동하지 않음).</span><span class="sxs-lookup"><span data-stu-id="707a9-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="707a9-108">**Project Service > 파라미터**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="707a9-109">Project Finder Mobile 앱 기능을 허용하는 데 사용할 파라미터 설정을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="707a9-110">**일반** 영역에서 **리소스 요구 사항을 리소스에 표시**를 **예**로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="707a9-111">**리소스별 기술 업데이트 허용**을 **예**로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="707a9-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="707a9-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="707a9-113">이는 전역 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-113">This is a global setting.</span></span> <span data-ttu-id="707a9-114">프로젝트 관리자는 개별 프로젝트를 해당 프로젝트의 **프로젝트 팀** 페이지에서 표시할지 여부를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="707a9-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="707a9-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="707a9-116">이메일 알림</span><span class="sxs-lookup"><span data-stu-id="707a9-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="707a9-117">가 다음의 시간에 다음의 받는 사람에게 리소스 요청에 대한 전자 메일을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="707a9-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="707a9-118">받는 사람</span><span class="sxs-lookup"><span data-stu-id="707a9-118">Recipient</span></span>|<span data-ttu-id="707a9-119">이벤트</span><span class="sxs-lookup"><span data-stu-id="707a9-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="707a9-120">프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="707a9-120">Project manager</span></span>|<span data-ttu-id="707a9-121">- 리소스가 Project Finder Mobile 앱을 사용하여 프로젝트에 등록하는 경우.</span><span class="sxs-lookup"><span data-stu-id="707a9-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="707a9-122">리소스</span><span class="sxs-lookup"><span data-stu-id="707a9-122">Resource</span></span>|<span data-ttu-id="707a9-123">- 리소스가 등록한 프로젝트 작업이 이미 다른 리소스에 의해 수행된 경우.</span><span class="sxs-lookup"><span data-stu-id="707a9-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="707a9-124">- 기술 승인 요청이 승인 또는 거부된 경우.</span><span class="sxs-lookup"><span data-stu-id="707a9-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="707a9-125">- 프로젝트 등록 요청이 승인 또는 거부된 경우.</span><span class="sxs-lookup"><span data-stu-id="707a9-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="707a9-126">개인 정보 취급 방침</span><span class="sxs-lookup"><span data-stu-id="707a9-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="707a9-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="707a9-127">See Also</span></span>  
 [<span data-ttu-id="707a9-128">리소스 설정</span><span class="sxs-lookup"><span data-stu-id="707a9-128">Set up resources</span></span>](../project-service/set-up-resources.md)
