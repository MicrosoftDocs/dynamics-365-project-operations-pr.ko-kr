---
title: 리소스 관리자 가이드
description: 리소스 관리자 가이드(Project Service)
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4a26a384dfaf6b974ed35105434152e655ff6444
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080260"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="d4068-103">리소스 관리자 가이드(Project Service)</span><span class="sxs-lookup"><span data-stu-id="d4068-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d4068-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능은 적절한 프로젝트에 대해 적절한 시간에 적합한 리소스를 찾고 모든 리소스를 효율적으로 활용할 수 있도록 돕습니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="d4068-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 사용하여 회사 컨설턴트를 효율적이며 효과적으로 배치합니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="d4068-106">이 기능은 프로젝트 컨설팅 요구 사항과 일정 및 컨설턴트의 기술과 가용성을 토대로 리소스 일정을 짤 때 필요한 도구를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="d4068-107">프로젝트 작업을 수행할 수 있는 최적격 컨설턴트를 빠르게 찾고 프로젝트별 과정을 진행하는 동안 보다 적절한 일정을 짤 수 있는 방법을 쉽게 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="d4068-108">리소스 일정은 다음을 수행하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="d4068-109">기술 및 숙련도 수준이 프로젝트 리소스 요구 사항과 얼마나 잘 맞는지를 근거로 프로젝트에 리소스 매치</span><span class="sxs-lookup"><span data-stu-id="d4068-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="d4068-110">사용 가능 시간 및 예약된 휴무일에 따라 프로젝트 일정과 리소스의 일정 매치</span><span class="sxs-lookup"><span data-stu-id="d4068-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="d4068-111">색으로 구분된 일정으로 리소스 가용성에 대한 시각적 판단</span><span class="sxs-lookup"><span data-stu-id="d4068-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="d4068-112">컨설턴트별 생산 능력 검토 및 그 생산 능력이 현재 어떻게 사용되는지 확인</span><span class="sxs-lookup"><span data-stu-id="d4068-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="d4068-113">컨설턴트 활용이 미달되거나 초과될 가능성이 있는 곳 또는 컨설턴트가 생산 능력에 맞게 작업 중인지 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="d4068-114">프로젝트에 작업자의 생산 능력에 대한 백분율 또는 구체적인 시간 수 할당</span><span class="sxs-lookup"><span data-stu-id="d4068-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="d4068-115">그룹 리소스 예약</span><span class="sxs-lookup"><span data-stu-id="d4068-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="d4068-116">리소스에 대한 가예약 또는 확정 예약 및 가예약된 시간을 한 번에 확정 예약 시간으로 변환</span><span class="sxs-lookup"><span data-stu-id="d4068-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="d4068-117">자동으로 프로젝트에 대한 작업 분할 구조에 정의된 리소스를 바탕으로 프로젝트 팀 구성</span><span class="sxs-lookup"><span data-stu-id="d4068-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="d4068-118">리소스 요청 처리(예약, 제안, 대체 리소스 찾기)</span><span class="sxs-lookup"><span data-stu-id="d4068-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="d4068-119">중앙(리소스 관리자가 할당) 또는 혼합 모델(리소스 관리자 및 기타 관리자가 할당할 수 있음)에 따라 리소스 할당</span><span class="sxs-lookup"><span data-stu-id="d4068-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="d4068-120">중앙 리소스 관리 모델과 혼합 리소스 관리 모델 설정 간의 차이에 대한 자세한 내용은 [추가 파라미터 구성(Project Service)](../psa/configure-additional-parameters-settings.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d4068-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="d4068-121">프로젝트 전반에 대해 리소스를 효율적으로 관리할 수 있으며 프로젝트에 대해 적절하게 직원 구성을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="d4068-122">다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="d4068-123">[리소스 요청 관리](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="d4068-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="d4068-124">컨설턴트의 기술 및 숙련도를 적절한 프로젝트에 매치</span><span class="sxs-lookup"><span data-stu-id="d4068-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="d4068-125">[리소스 사용 가능 시간 보기](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="d4068-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="d4068-126">일정 보기에서 컨설턴트의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="d4068-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="d4068-127">[리소스 사용률 보기](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="d4068-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="d4068-128">컨설턴트가 현재 예약되어 있는 시간 백분율 확인</span><span class="sxs-lookup"><span data-stu-id="d4068-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="d4068-129">[프로젝트에 리소스 예약](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="d4068-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="d4068-130">프로젝트에 대한 컨설턴트를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="d4068-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="d4068-131">개별 프로젝트에 대한 리소스 요청 제출에 대한 자세한 내용은 [리소스 요청 제출](../psa/submit-resource-requests.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d4068-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d4068-132">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d4068-132">See Also</span></span>  
 <span data-ttu-id="d4068-133">[Project Service 개요](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="d4068-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="d4068-134">[관리자 가이드](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d4068-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="d4068-135">[거래처 관리자 가이드](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d4068-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="d4068-136">[프로젝트 관리자 가이드](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d4068-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="d4068-137">시간, 비용 및 공동 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="d4068-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
