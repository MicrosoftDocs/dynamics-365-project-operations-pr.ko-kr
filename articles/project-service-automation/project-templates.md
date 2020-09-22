---
title: 프로젝트 템플릿
description: 이 항목은 빠른 프로젝트 설정을 위해 프로젝트 템플릿을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753249"
---
# <a name="project-templates"></a><span data-ttu-id="78937-103">프로젝트 템플릿</span><span class="sxs-lookup"><span data-stu-id="78937-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78937-104">프로젝트 템플릿은 프로젝트를 빠르고 쉽게 시작하는 데 도움이 되는 사전 정의된 틀입니다.</span><span class="sxs-lookup"><span data-stu-id="78937-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="78937-105">사전 정의된 템플릿을 사용하여 한 번의 클릭으로 새 프로젝트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="78937-106">프로젝트의 경우 프로젝트 템플릿의 필수 구성 조건을 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="78937-107">각 프로젝트 템플릿에 대한 프로젝트 스케줄을 정의해야 하며 템플릿의 구성 요소에 유용한 데이터가 있도록 조직에서 역할 및 가격 목록을 사전 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="78937-108">프로젝트 템플릿은 스케줄, 프로젝트 추산 및 프로젝트 팀원의 세 가지 구성 요소로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="78937-109">일정</span><span class="sxs-lookup"><span data-stu-id="78937-109">Schedule</span></span>

<span data-ttu-id="78937-110">프로젝트 템플릿의 스케줄은 프로젝트의 스케줄과 동일한 요소 집합을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="78937-111">귀하는 과업 계층 구조를 만들고, 역할을 과업과 연계하고, 스케줄 속성을 정의하고, 종속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="78937-112">프로젝트 템플릿의 스케줄은 각 과업에 대한 과업 모드도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="78937-113">따라서 그것은 스케줄링 엔진을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="78937-114">프로젝트 캘린더를 프로젝트와 연계해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="78937-115">작업 스케줄을 만들 때 프로젝트 템플릿과 프로젝트 사이에 차이는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="78937-116">프로젝트 추산</span><span class="sxs-lookup"><span data-stu-id="78937-116">Project estimates</span></span>

<span data-ttu-id="78937-117">프로젝트 템플릿에서 프로젝트 추산은 프로젝트에서 프로젝트 추산과 동일한 방식으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="78937-118">그러나 원가 및 판매 가격은 이 파라미터들에 정의된 기본 원가 및 판매 가격 목록에서 가져온 값입니다.</span><span class="sxs-lookup"><span data-stu-id="78937-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="78937-119">템플릿에서 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="78937-119">Creating a project from a template</span></span>
 
<span data-ttu-id="78937-120">프로젝트 템플릿에서 프로젝트를 만드는 방법에는 여러 가지가 있습니다:</span><span class="sxs-lookup"><span data-stu-id="78937-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="78937-121">견적에서 프로젝트를 만들 때, **빠른 생성: 프로젝트** 대화 상자에서 프로젝트 템플릿을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![빠른 생성: 프로젝트 대화 상자](media/project-11.png)

- <span data-ttu-id="78937-123">**새 프로젝트**를 선택하여 프로젝트를 만들 때, **프로젝트** 페이지가 나타나면 레코드를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="78937-124">**템플릿 선택** 필드에서 조직에서 사전 정의된 프로젝트 템플릿 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="78937-125">**템플릿 엔터티** 페이지에서 **템플릿에서 프로젝트 만들기**를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="78937-126">프로젝트에 템플릿의 구성 요소 복사</span><span class="sxs-lookup"><span data-stu-id="78937-126">Copying components of template to project</span></span>

<span data-ttu-id="78937-127">프로젝트 템플릿의 구성 요소를 프로젝트에 복사하면 프로젝트의 설정에 따라 몇 가지 재정의가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="78937-128">스케줄 복사</span><span class="sxs-lookup"><span data-stu-id="78937-128">Copying the schedule</span></span>

<span data-ttu-id="78937-129">프로젝트 템플릿에서 스케줄을 복사할 때, 프로젝트에 템플릿이 아닌 다른 프로젝트 캘린더가 있는 경우, 프로젝트 캘린더의 작업 시간 수가 작업 스케줄에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="78937-130">이런 식으로 스케줄이 지원 프로젝트 캘린더에 일치하도록 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="78937-131">마찬가지로, 스케줄의 첫 번째 과업이 프로젝트의 시작 날짜를 취하며, 나머지 계층의 스케줄은 템플릿에 지정된 기간 및 종속성에 근거하여 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="78937-132">프로젝트 추산 복사</span><span class="sxs-lookup"><span data-stu-id="78937-132">Copying project estimates</span></span> 

<span data-ttu-id="78937-133">프로젝트 추산 행을 복사하면 가격표가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="78937-134">원가표의 경우 이러한 업데이트는 프로젝트의 소유 단위에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="78937-135">판매 가격표의 경우 고객에 근거합니다.</span><span class="sxs-lookup"><span data-stu-id="78937-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="78937-136">판매 엔터티와 연계된 프로젝트의 경우, 단가 및 판매 가격은 해당 가격표에 근거하여 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="78937-137">프로젝트 팀 복사</span><span class="sxs-lookup"><span data-stu-id="78937-137">Copying a project team</span></span>

<span data-ttu-id="78937-138">프로젝트 템플릿에서 프로젝트 팀을 어떤 프로젝트에 복사할 때, 일반 리소스가 템플릿에 정의된 기능 및 숙련도와 함께 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="78937-139">일반 리소스 배정은 프로젝트 템플릿에서와 같이 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="78937-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="78937-140">명명된 리소스는 프로젝트 템플릿에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78937-140">Named resources aren't supported in project templates.</span></span>
