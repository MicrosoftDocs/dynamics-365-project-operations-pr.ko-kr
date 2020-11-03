---
title: 프로젝트 관리자 가이드
description: 프로젝트 관리자 가이드(Project Service)
author: ruhercul
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
ms.openlocfilehash: 89e33ae67f5d4134bf8c6f6c517fd4460c6879dd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080022"
---
# <a name="project-manager-guide-project-service"></a><span data-ttu-id="4d0a0-103">프로젝트 관리자 가이드(Project Service)</span><span class="sxs-lookup"><span data-stu-id="4d0a0-103">Project manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]<span data-ttu-id="4d0a0-104">의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능은 프로젝트 견적 및 계약 만들기와 계약 체결 후 클라이언트를 위한 프로젝트 만들기 및 관리를 돕습니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-104">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you create project quotes and contracts, and create and manage projects for your clients after you’ve won the contract.</span></span> <span data-ttu-id="4d0a0-105">또한, 적절하고 수익성 있는 프로젝트로 만들기 위한 분석 역시 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-105">They also provides analytics to help you ensure projects are feasible and profitable.</span></span> <span data-ttu-id="4d0a0-106">시간 및 자재 또는 고정 가격을 기반으로 프로젝트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-106">You can set up projects on a time and materials or fixed-price basis.</span></span>  
  
 <span data-ttu-id="4d0a0-107">프로젝트 관리 도구를 사용하면 다음을 수행하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-107">Project management tools help you to:</span></span>  
  
-   <span data-ttu-id="4d0a0-108">효과적으로 작업 예측</span><span class="sxs-lookup"><span data-stu-id="4d0a0-108">Effectively estimate work</span></span>  
  
-   <span data-ttu-id="4d0a0-109">프로젝트가 파이프라인에 있을 때 리소스 요구 사항 예측</span><span class="sxs-lookup"><span data-stu-id="4d0a0-109">Forecast resource requirements when projects are in the pipeline</span></span>  
  
-   <span data-ttu-id="4d0a0-110">팀원들이 프로젝트에 대해 협업하고 항상 현재의 정확한 프로젝트 상태 유지</span><span class="sxs-lookup"><span data-stu-id="4d0a0-110">Enable team members to collaborate on projects and maintain current and accurate project status at all times</span></span>  
  
-   <span data-ttu-id="4d0a0-111">매 업무의 성공에 대한 잠재적인 위협을 사전에 파악하여 해결</span><span class="sxs-lookup"><span data-stu-id="4d0a0-111">Proactively identify and resolve potential threats to the success of each and every engagement.</span></span>  
  
<span data-ttu-id="4d0a0-112">이 가이드에서는 프로젝트를 만들고 관리하는 데 필요한 정보에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-112">This guide provides information you need to create and manage projects:</span></span>  
  
-   [<span data-ttu-id="4d0a0-113">영업 프로세스 중에 프로젝트에 대한 작업 추정 제공</span><span class="sxs-lookup"><span data-stu-id="4d0a0-113">Provide work estimates for a project during the sales process</span></span>](../psa/provide-estimates-project-during-sales-process.md)  
  
-   [<span data-ttu-id="4d0a0-114">프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-114">Create a project</span></span>](../psa/create-project.md)  
  
-   [<span data-ttu-id="4d0a0-115">Project Service Automation 추가 기능을 사용하여 Microsoft Project의 작업 계획</span><span class="sxs-lookup"><span data-stu-id="4d0a0-115">Use the Project Service Automation add-in to plan your work in Microsoft Project</span></span>](../psa/add-plan-work-microsoft-project.md)  
  
-   [<span data-ttu-id="4d0a0-116">작업 분할 구조로 프로젝트 일정 짜기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-116">Schedule a project with a work breakdown structure</span></span>](../psa/schedule-project-work-breakdown-structure.md)  
  
-   [<span data-ttu-id="4d0a0-117">프로젝트 비용 및 수익 추정치 판단</span><span class="sxs-lookup"><span data-stu-id="4d0a0-117">Determine project cost and revenue estimates</span></span>](../psa/determine-project-cost-revenue-estimates.md)  
  
-   [<span data-ttu-id="4d0a0-118">프로젝트 진행률 및 비용 추적</span><span class="sxs-lookup"><span data-stu-id="4d0a0-118">Track project progress and cost</span></span>](../psa/track-project-progress-cost.md)  
  
-   [<span data-ttu-id="4d0a0-119">프로젝트 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-119">Create a project template</span></span>](../psa/create-project-template.md)  
  
-   [<span data-ttu-id="4d0a0-120">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="4d0a0-120">Submit resource requests</span></span>](../psa/submit-resource-requests.md)  
  
-   [<span data-ttu-id="4d0a0-121">프로젝트용 Office 365 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-121">Create an Office 365 Group for a project</span></span>](../psa/create-office-365-group-project.md)  
  
-   [<span data-ttu-id="4d0a0-122">프로젝트에 문서 추가</span><span class="sxs-lookup"><span data-stu-id="4d0a0-122">Add documents to a project</span></span>](../psa/add-documents-project.md)  
  
-   [<span data-ttu-id="4d0a0-123">프로젝트 상태 추적</span><span class="sxs-lookup"><span data-stu-id="4d0a0-123">Track a project’s status</span></span>](../psa/track-project-status.md)  
  
-   [<span data-ttu-id="4d0a0-124">프로젝트 팀 구성원 보기 및 예약 관리</span><span class="sxs-lookup"><span data-stu-id="4d0a0-124">View project team members and manage bookings</span></span>](../psa/view-project-team-members-manage-bookings.md)  
  
-   [<span data-ttu-id="4d0a0-125">프로젝트 예상 보기 및 편집</span><span class="sxs-lookup"><span data-stu-id="4d0a0-125">View and edit project estimates</span></span>](../psa/view-edit-project-estimates.md)  
  
-   [<span data-ttu-id="4d0a0-126">시간 및 비용 승인</span><span class="sxs-lookup"><span data-stu-id="4d0a0-126">Approve time and expenses</span></span>](../psa/approve-time-expenses.md)  
  
-   [<span data-ttu-id="4d0a0-127">프로젝트 실제 검토</span><span class="sxs-lookup"><span data-stu-id="4d0a0-127">Review project actuals</span></span>](../psa/review-project-actuals.md)  
  
-   [<span data-ttu-id="4d0a0-128">송장 보기 및 보내기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-128">View and send invoices</span></span>](../psa/view-send-invoices.md)  
  
-   [<span data-ttu-id="4d0a0-129">대시보드 및 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="4d0a0-129">View dashboards and reports</span></span>](../psa/view-dashboards-reports.md)  
  
## <a name="prerequisites"></a><span data-ttu-id="4d0a0-130">필수 조건</span><span class="sxs-lookup"><span data-stu-id="4d0a0-130">Prerequisites</span></span>  
 <span data-ttu-id="4d0a0-131">아직 하지 않았을 경우, 다음 항목을 완료해야 프로젝트 만들기를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-131">If you haven't already, you’ll need to complete the following items before you can start creating projects:</span></span>  
  
-   <span data-ttu-id="4d0a0-132">[작업 시간 템플릿 만들기](../psa/create-work-hours-template.md).</span><span class="sxs-lookup"><span data-stu-id="4d0a0-132">[Create a work hours template](../psa/create-work-hours-template.md).</span></span> <span data-ttu-id="4d0a0-133">모든 휴무 일정을 고려하여 일정에 일자별로 제공할 작업 시간을 정의하는 프로젝트 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-133">Set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span>  
  
-   <span data-ttu-id="4d0a0-134">[가격표 만들기](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="4d0a0-134">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="4d0a0-135">조직에서의 리소스 역할과 비용 및 제품 등의 여타 카테고리에 대한 비용과 판매 가격을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-135">Set cost and sales prices for resource roles in your organization, as well as for other categories like expenses and products.</span></span>  
  
-   <span data-ttu-id="4d0a0-136">[리소스 역할 추가](../psa/add-resource-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d0a0-136">[Add resource roles](../psa/add-resource-roles.md).</span></span> <span data-ttu-id="4d0a0-137">리소스 요구 사항과 프로젝트 비용을 결정할 수 있도록 역할을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4d0a0-137">Define roles to help determine resource requirements and project costs.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4d0a0-138">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4d0a0-138">See Also</span></span>  
 <span data-ttu-id="4d0a0-139">[Project Service 개요](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="4d0a0-139">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="4d0a0-140">[관리자 가이드](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4d0a0-140">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="4d0a0-141">[거래처 관리자 가이드](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4d0a0-141">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="4d0a0-142">[리소스 관리자 가이드](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4d0a0-142">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="4d0a0-143">시간, 비용 및 공동 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="4d0a0-143">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)

