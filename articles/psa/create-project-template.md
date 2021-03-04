---
title: 프로젝트 템플릿 만들기
description: 프로젝트 템플릿을 만드는 방법(Project Service)
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149371"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="0311a-103">프로젝트 템플릿 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="0311a-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0311a-104">프로젝트 템플릿을 사용하면 회사가 정기적으로 비슷한 종류의 프로젝트에 입찰 중일 때 시간을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="0311a-105">프로젝트 템플릿은 표준 역할 집합 및 프로젝트의 유형에 대한 예상 시간을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="0311a-106">거래처 관리자와 프로젝트 관리자는 프로젝트 템플릿을 사용하여 프로젝트를 만들거나 템플릿을 복사하여 고유 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="0311a-107">프로젝트 템플릿의 구성 요소</span><span class="sxs-lookup"><span data-stu-id="0311a-107">Components of project template</span></span>
 <span data-ttu-id="0311a-108">프로젝트 템플릿은 세 개의 구성 요소로 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="0311a-109">**작업 분할 구조**: 프로젝트 서식 파일의 작업 분할 구조는 프로젝트와 동일한 요소 집합을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="0311a-110">Gantt에서 작업 계층 구조를 만들고, 작업과 역할을 연결하고, 일정 특성을 정의하고, 모든 데이터의 종속성 및 보기를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="0311a-111">프로젝트 템플릿의 작업 분할 구조는 각 작업에 대한 작업 모드도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="0311a-112">작업 일정을 만들 때 프로젝트 템플릿과 프로젝트는 차이점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="0311a-113">**프로젝트 추정**: 템플릿에서 프로젝트 예상은 프로젝트에서와 동일한 방식으로 작동합니다. 단, 비용 및 판매 가격의 기본 가격표는 항상 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 파라미터에서 정의된 기본 비용 및 판매 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="0311a-114">나머지 기능은 프로젝트에서와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="0311a-115">**프로젝트 팀 구성**: 프로젝트 템플릿에 대한 프로젝트 팀을 구성하는 경우 템플릿의 명명된 리소스를 예약할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="0311a-116">작업 분할 구조에서 **프로젝트 팀 생성** 을 사용하여 일반 리소스의 집합을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="0311a-117">일반 리소스에 대해 필요한 기술 및 숙련도를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="0311a-118">프로젝트 템플릿에서 예약 가능한 자원으로 일반 자원을 대체할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="0311a-119">템플릿에서 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="0311a-119">Create a project from a template</span></span>  
 <span data-ttu-id="0311a-120">다음과 같은 방법으로 템플릿에서 프로젝트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="0311a-121">견적에서 프로젝트를 만들 때 프로젝트 빨리 만들기 양식에서 프로젝트 템플릿을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="0311a-122">**새 프로젝트** 를 클릭하여 프로젝트를 만들 때, 레코드를 저장하기 전에 프로젝트 양식을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="0311a-123">여기에서 **템플릿 선택** 필드를 클릭하여 조직에 미리 정의된 프로젝트 템플릿의 목록에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="0311a-124">**프로젝트 템플릿** 페이지의 **템플릿에서 프로젝트 만들기** 를 클릭하여 템플릿에서 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="0311a-125">프로젝트에 템플릿의 구성 요소 복사</span><span class="sxs-lookup"><span data-stu-id="0311a-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="0311a-126">템플릿의 구성 요소를 프로젝트로 복사할 때 알아야 할 몇 가지 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="0311a-127">**작업 분할 구조 복사**: 프로젝트 템플릿에서 작업 분할 구조를 복사할 때, 프로젝트에 템플릿이 아닌 다른 프로젝트 달력이 있는 경우 프로젝트 달력의 작업 시간이 작업 일정에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="0311a-128">일정이 지원 프로젝트 달력에 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="0311a-129">마찬가지로, 작업 분할 구조에서 첫 번째 작업 계층 구조는 프로젝트의 시작 날짜를 가지며, 작업 계층 구조의 나머지 일정은 템플릿의 작업 분할 구조에 지정된 기간 및 종속성에 따라 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="0311a-130">**프로젝트 예상 복사**: 프로젝트 예상 라인을 복사할 때, 가격표는 비용 가격표에 대한 프로젝트 및 판매 가격표에 대한 고객의 소유 단위에 따라 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="0311a-131">단가 및 판매 가격은 판매 엔터티에 연결된 프로젝트의 해당 가격표에서 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="0311a-132">**프로젝트 팀 복사**: 템플릿에서 프로젝트로 팀 프로젝트를 복사할 때 일반 자원은 템플릿에 정의된 기술 및 숙련도와 함께 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="0311a-133">일반 자원 배정은 프로젝트 템플릿에서와 같이 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="0311a-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0311a-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0311a-134">See Also</span></span>  
 [<span data-ttu-id="0311a-135">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="0311a-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
