---
title: 프로젝트 만들기
description: 프로젝트를 만드는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 164dff56bb61f6d9bc4cf0b0678a25e0169a31ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285086"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="7cf7d-103">프로젝트 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="7cf7d-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7cf7d-104">프로젝트 기반 서비스에 대한 영업 기회, 견적 또는 계약을 만들려고 할 경우 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능을 사용하여 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="7cf7d-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능은 영업 기회에서 완료까지 프로젝트 관리를 돕습니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="7cf7d-106">프로젝트를 만들 때 견적, 예상 비용 및 리소스 관리에 영향을 미치는 작업 분할 구조를 만들기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="7cf7d-107">**Project Service > 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="7cf7d-108">**새 프로젝트** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="7cf7d-109">**요약** 영역에 프로젝트 이름을 입력한 후 가능한 한 많은 세부 정보를 기입합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="7cf7d-110">빨간색 별표(\*)로 표시된 항목은 필수 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="7cf7d-111">**저장** 을 클릭하여 프로젝트를 만들면 계속 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="7cf7d-112">다음으로, 프로젝트에 대한 작업 분할 구조를 만들어 프로젝트에 필요한 업무, 타이밍, 리소스 역할을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cf7d-113">예약할 때 Project Service Automation은 적용된 **근무 시간** 템플릿의 표준 시간대를 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="7cf7d-114">그러나 일정 작업을 볼 때 작업 시작 및 종료 날짜는 사용자의 표준 시간대로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="7cf7d-115">이는 **프로젝트** 양식의 다른 시간대별 보기에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="7cf7d-116">사용자의 시간대가 프로젝트에 적용된 근무 시간 템플릿의 시간대와 일치하지 않을 경우 차이를 설명하는 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf7d-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="7cf7d-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7cf7d-117">See Also</span></span>  
 [<span data-ttu-id="7cf7d-118">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="7cf7d-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]