---
title: 영업 프로세스 중에 프로젝트에 대한 작업 추정 제공
description: 영업 프로세스 중에 프로젝트에 대한 추정을 제공하는 방법(Project Service)
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147976"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="11961-103">영업 프로세스 중에 프로젝트에 대한 작업 추정 제공(Project Service)</span><span class="sxs-lookup"><span data-stu-id="11961-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="11961-104">영업 과정 중에 견적 내용으로 처음부터 영업 예상을 산출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]<span data-ttu-id="11961-105">의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능은 작업 분할 구조에서 프로젝트에 대한 추정에 기여하는 작업 항목 분할 및 관련 특성 연결을 통해 영업 예상 결과를 보다 과학적이고 확실하게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11961-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="11961-106">영업에 성공하면, 프로젝트의 성공적인 완료에 필요한 대로 변경하여 관련 작업 분할 구조를 프로젝트 계획에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="11961-107">프로젝트를 견적 내용에 연결</span><span class="sxs-lookup"><span data-stu-id="11961-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="11961-108">프로젝트 기반 견적 내용을 만들 때, 견적 내용에서 새 프로젝트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="11961-109">그런 다음, 미리 구성된 표준 프로젝트 계획 및 조직에서 일반적으로 사용되는 경비 추정 또는 과거 프로젝트에서 산출한 프로젝트 계획 및 추정 사본인 프로젝트 템플릿을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="11961-110">프로젝트를 만들 때, 프로젝트 템플릿을 선택하여 프로젝트 계획, 추정, 역할 요구 사항을 변경하는 기준을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="11961-111">견적에서 프로젝트를 만들면 프로젝트가 견적 내용에 자동으로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="11961-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="11961-112">프로젝트 추정 구성 요소</span><span class="sxs-lookup"><span data-stu-id="11961-112">Project estimate components</span></span>  
 <span data-ttu-id="11961-113">프로젝트의 작업 분할 구조는 작업을 업무 단위로 나누고, 업무의 계층 구조를 관리하며, 각 업무 완료에 필요한 예상 작업량을 할당하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11961-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="11961-114">또한 업무에 역할을 연결하여 업무 및 일정 완료에 필요한 리소스 유형 추정을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="11961-115">작업 분할 구조를 사용하면 작업량을 정하고 예상 일정을 짜는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11961-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="11961-116">기본적으로 프로젝트는 앞서 정의한 기본 가격표를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="11961-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="11961-117">가격표에 정의된 비용 및 영업 가격은 프로젝트 작업 분할에 대한 예상 비용을 정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11961-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="11961-118">프로젝트가 견적에 연결되고 견적의 가격표가 기본과 다를 경우, 견적의 가격표가 재무 추정에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="11961-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="11961-119">프로젝트에서 견적으로 추정 가져오기</span><span class="sxs-lookup"><span data-stu-id="11961-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="11961-120">프로젝트에서 프로젝트 추정을 확보하면 이것을 견적 내용으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="11961-121">**견적 내용 상세** 에서 **추정에서 가져오기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="11961-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="11961-122">거래 유형, 역할 또는 작업 분할 구조 노드 수준별로 요약된 프로젝트 추정을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11961-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="11961-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="11961-123">See Also</span></span>  
 [<span data-ttu-id="11961-124">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="11961-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
