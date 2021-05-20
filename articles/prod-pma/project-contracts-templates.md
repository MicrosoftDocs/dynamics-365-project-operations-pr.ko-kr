---
title: Project Service Automation에서 Finance로 직접 프로젝트 계약 및 프로젝트 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 계약 및 프로젝트를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85722f61a672cc55cd2b511dc80ebfbe4807b957
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950407"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a><span data-ttu-id="3039f-103">Project Service Automation에서 Finance로 직접 프로젝트 계약 및 프로젝트 동기화</span><span class="sxs-lookup"><span data-stu-id="3039f-103">Synchronize project contracts and projects directly from Project Service Automation to Finance</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3039f-104">이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 계약 및 프로젝트를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="3039f-105">Enterprise 버전 7.3.0을 사용하는 경우 KB 4074835를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3039f-106">Project Service Automation에서 Finance까지의 데이터 흐름</span><span class="sxs-lookup"><span data-stu-id="3039f-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="3039f-107">Project Service Automation to Finance 통합 솔루션을 사용하려면 먼저 Dynamics 365 데이터 통합 기능에 익숙해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="3039f-108">Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3039f-109">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 계약, 프로젝트, 프로젝트 계약 내용 및 프로젝트 계약 내용 중요 시점에 대한 데이터 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3039f-110">다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3039f-111">[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="3039f-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3039f-112">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="3039f-112">Templates and tasks</span></span>

<span data-ttu-id="3039f-113">사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-113">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3039f-114">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 계약 및 프로젝트를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="3039f-115">Dynamics 365 Project Service Automation v2.x와 통합</span><span class="sxs-lookup"><span data-stu-id="3039f-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="3039f-116">**데이터 통합의 템플릿 이름:** 프로젝트 및 계약(Project Service Automation에서 Finance로)</span><span class="sxs-lookup"><span data-stu-id="3039f-116">**Name of the template in Data integration:** Projects and contracts (Project Service Automation to Finance)</span></span>
- <span data-ttu-id="3039f-117">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="3039f-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3039f-118">프로젝트 계약 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-118">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-119">프로젝트 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-119">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-120">프로젝트 계약 내용 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-120">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-121">프로젝트 계약 내용 중요 시점 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-121">Project contract line milestones Project Service Automation to Finance</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="3039f-122">Dynamics 365 Project Service Automation v3.x와 통합</span><span class="sxs-lookup"><span data-stu-id="3039f-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="3039f-123">프로젝트 계약 내용 중요 시점 템플릿에 영향을 미치는 Project Service Automation의 스키마 변경이 있으며 Project Service Automation v3.x를 Dynamics 365과 통합하려면 v2 버전의 템플릿을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="3039f-124">**데이터 통합의 템플릿 이름:** 프로젝트 및 계약(Project Service Automation 3.x에서 Finance로) - v2</span><span class="sxs-lookup"><span data-stu-id="3039f-124">**Name of the template in Data integration:** Projects and Contracts (Project Service Automation 3.x to Finance) - v2</span></span>
- <span data-ttu-id="3039f-125">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="3039f-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3039f-126">프로젝트 계약 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-126">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-127">프로젝트 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-127">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-128">프로젝트 계약 내용 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-128">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="3039f-129">프로젝트 계약 내용 중요 시점 Project Service Automation에서 Finance로</span><span class="sxs-lookup"><span data-stu-id="3039f-129">Project contract line milestones Project Service Automation to Finance</span></span>

<span data-ttu-id="3039f-130">프로젝트 계약 및 프로젝트의 동기화가 발생하기 전에 계정을 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="3039f-131">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="3039f-131">Entity set</span></span>

| <span data-ttu-id="3039f-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3039f-132">Project Service Automation</span></span>       | <span data-ttu-id="3039f-133">재무</span><span class="sxs-lookup"><span data-stu-id="3039f-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="3039f-134">주문</span><span class="sxs-lookup"><span data-stu-id="3039f-134">Orders</span></span>                           | <span data-ttu-id="3039f-135">프로젝트 계약을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="3039f-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="3039f-136">프로젝트</span><span class="sxs-lookup"><span data-stu-id="3039f-136">Projects</span></span>                         | <span data-ttu-id="3039f-137">프로젝트를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="3039f-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="3039f-138">주문 라인</span><span class="sxs-lookup"><span data-stu-id="3039f-138">Order lines</span></span>                      | <span data-ttu-id="3039f-139">프로젝트 계약 내용을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="3039f-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="3039f-140">프로젝트 계약 내용 중요 시점</span><span class="sxs-lookup"><span data-stu-id="3039f-140">Project contract line milestones</span></span> | <span data-ttu-id="3039f-141">프로젝트 계약 내용 중요 시점을 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="3039f-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3039f-142">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="3039f-142">Entity flow</span></span>

<span data-ttu-id="3039f-143">프로젝트 계약은 Project Service Automation에서 관리되며 프로젝트 계약으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="3039f-144">통합 템플릿의 일부로 Finance에서 프로젝트 계약에 대한 통합 소스를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="3039f-145">시간과 재료 및 고정 가격 프로젝트는 Project Service Automation에서 관리되고 프로젝트로서 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-145">Time and material and fixed-price projects are managed in Project Service Automation and synchronized to Finance as projects.</span></span> <span data-ttu-id="3039f-146">템플릿 통합의 일부로 Finance에서 프로젝트의 통합 소스를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-146">As part of the template integration, you can set the integration source for the project in Finance.</span></span> <span data-ttu-id="3039f-147">현재 시간과 재료 및 고정 가격 프로젝트만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-147">Currently, only time and material and fixed-price projects are supported.</span></span>


<span data-ttu-id="3039f-148">프로젝트 계약 내용은 Project Service Automation에서 관리되며 프로젝트 계약 청구 규칙으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-148">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="3039f-149">청구 방법이 기본 프로젝트 유형과 다른 경우 동기화는 계약 항목 프로젝트 및 프로젝트 그룹에 대한 프로젝트 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-149">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="3039f-150">프로젝트 계약 내용 중요 시점은 Project Service Automation에서 관리되며 프로젝트 계약 청구 규칙 중요 시점으로 Finance에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-150">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="3039f-151">Project Service Automation에서 Finance 통합 솔루션</span><span class="sxs-lookup"><span data-stu-id="3039f-151">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="3039f-152">**프로젝트 계약 ID** 필드는 **프로젝트 계약** 페이지에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-152">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="3039f-153">이 필드는 통합을 지원하기 위해 자연스럽고 고유한 키로 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-153">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="3039f-154">새 프로젝트 계약이 생성될 때 **프로젝트 계약 ID** 값이 아직 존재하지 않으면 숫자 시퀀스를 사용하여 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-154">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="3039f-155">값은 **ORD** 와 증가하는 숫자 시퀀스 및 6자 접미사가 이어집니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-155">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="3039f-156">예를 들어 다음과 같습니다. **ORD-01022-Z4M9Q0**.</span><span class="sxs-lookup"><span data-stu-id="3039f-156">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="3039f-157">**프로젝트 번호** 필드는 **프로젝트** 페이지에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-157">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="3039f-158">이 필드는 통합을 지원하기 위해 자연스럽고 고유한 키로 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-158">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="3039f-159">새 프로젝트가 생성될 때 **프로젝트 번호** 값이 아직 존재하지 않으면 숫자 시퀀스를 사용하여 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-159">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="3039f-160">값은 **PRJ** 와 증가하는 숫자 시퀀스 및 6자 접미사가 이어집니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-160">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="3039f-161">예를 들어 다음과 같습니다. **PRJ-01049-CCNID0**.</span><span class="sxs-lookup"><span data-stu-id="3039f-161">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="3039f-162">Project Service Automation과 Finance 통합 솔루션이 적용되면 업그레이드 스크립트가 Project Service Automation에서 기존 프로젝트 계약의 **프로젝트 계약 ID** 필드 및 기존 프로젝트의 **프로젝트 번호** 필드를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-162">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3039f-163">필수 조건 및 매핑 설정</span><span class="sxs-lookup"><span data-stu-id="3039f-163">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="3039f-164">프로젝트 계약 및 프로젝트의 동기화가 발생하기 전에 계정을 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-164">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="3039f-165">연결 세트에서 **msdyn\_organizationalunits** 에 대한 통합 키 필드 매핑을 **msdyn\_name \[Name\]** 에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-165">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="3039f-166">먼저 연결 세트에 프로젝트를 추가해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-166">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="3039f-167">자세한 내용은 [앱용 Common Data Service에 데이터 통합](/powerapps/administrator/data-integrator)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="3039f-167">For more information, see [Integrate data into Common Data Service for Apps](/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="3039f-168">연결 세트에서 **msdyn\_projects** 에 대한 통합 키 필드 매핑을 **msdynce\_projectnumber \[Project Number\]** 에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-168">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="3039f-169">먼저 연결 세트에 프로젝트를 추가해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-169">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="3039f-170">자세한 내용은 [앱용 Common Data Service에 데이터 통합](/powerapps/administrator/data-integrator)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="3039f-170">For more information, see [Integrate data into Common Data Service for Apps](/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="3039f-171">프로젝트 계약 및 프로젝트의 **SourceDataID** 는 다른 값으로 업데이트하거나 매핑에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-171">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="3039f-172">기본 템플릿 값은 **Project Service Automation** 입니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-172">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="3039f-173">**PaymentTerms** 매핑은 Finance의 유효한 지불 조건을 반영하도록 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-173">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="3039f-174">프로젝트 작업에서 매핑을 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-174">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="3039f-175">기본값 맵에는 데모 데이터에 대한 기본값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-175">The default value map has default values for demo data.</span></span> <span data-ttu-id="3039f-176">다음 표에는 Project Service Automation의 값이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-176">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="3039f-177">값</span><span class="sxs-lookup"><span data-stu-id="3039f-177">Value</span></span> | <span data-ttu-id="3039f-178">설명</span><span class="sxs-lookup"><span data-stu-id="3039f-178">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="3039f-179">6</span><span class="sxs-lookup"><span data-stu-id="3039f-179">1</span></span>     | <span data-ttu-id="3039f-180">30일</span><span class="sxs-lookup"><span data-stu-id="3039f-180">Net 30</span></span>        |
    | <span data-ttu-id="3039f-181">2</span><span class="sxs-lookup"><span data-stu-id="3039f-181">2</span></span>     | <span data-ttu-id="3039f-182">2% 10일, 30일</span><span class="sxs-lookup"><span data-stu-id="3039f-182">2% 10, Net 30</span></span> |
    | <span data-ttu-id="3039f-183">3</span><span class="sxs-lookup"><span data-stu-id="3039f-183">3</span></span>     | <span data-ttu-id="3039f-184">45일</span><span class="sxs-lookup"><span data-stu-id="3039f-184">Net 45</span></span>        |
    | <span data-ttu-id="3039f-185">4</span><span class="sxs-lookup"><span data-stu-id="3039f-185">4</span></span>     | <span data-ttu-id="3039f-186">60일</span><span class="sxs-lookup"><span data-stu-id="3039f-186">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="3039f-187">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="3039f-187">Power Query</span></span>

<span data-ttu-id="3039f-188">다음 조건이 충족되는 경우 Excel용 Microsoft 파워 쿼리를 사용하여 데이터를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-188">Use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="3039f-189">Dynamics 365 Sales에 판매 주문이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-189">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="3039f-190">Project Service Automation에 여러 조직 단위가 있으며 이러한 조직 단위는 Finance의 여러 법인에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-190">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="3039f-191">파워 쿼리를 사용해야 하는 경우 다음 지침을 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="3039f-191">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="3039f-192">프로젝트 및 계약(PSA에서 Fin 및 Ops까지) 템플릿에는 **작업 항목(msdyn\_ordertype = 192350001)** 유형의 판매 주문만 포함하는 기본 필터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-192">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="3039f-193">이 필터는 Finance에서 판매 주문에 대해 프로젝트 계약이 생성되지 않도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-193">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="3039f-194">고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-194">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="3039f-195">통합 연결 집합의 법인에 동기화되어야 하는 계약 조직만 포함하는 파워 쿼리 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-195">Create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="3039f-196">예를 들어 계약 조직 단위가 Contoso US인 프로젝트 계약은 USSI 법인에 동기화되어야 하지만 계약 조직 단위가 Contoso Global인 프로젝트 계약은 USMF 법인과 동기화되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-196">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="3039f-197">이 필터를 작업 매핑에 추가하지 않으면 모든 프로젝트 계약이 계약 조직 단위에 관계없이 연결 집합에 대해 정의된 법인에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-197">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3039f-198">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="3039f-198">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="3039f-199">**CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** 및 **AddressZipCode** 필드는 프로젝트 계약의 기본 매핑에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-199">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="3039f-200">프로젝트 계약에 대해 이 데이터를 동기화해야 하는 경우 매핑을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-200">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="3039f-201">**Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** 및 **ProjectType** 필드는 프로젝트의 기본 매핑에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-201">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="3039f-202">프로젝트에 대해 이 데이터를 동기화해야 하는 경우 매핑을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-202">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="3039f-203">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-203">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="3039f-204">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3039f-204">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3039f-205">[![프로젝트 계약 템플릿 매핑](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="3039f-205">[![Project contract template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="3039f-206">[![프로젝트 템플릿 매핑](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="3039f-206">[![Project template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="3039f-207">[![프로젝트 계약 내용 템플릿 매핑](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="3039f-207">[![Project contract lines template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="3039f-208">[![프로젝트 계약 내용 중요 시점 템플릿 매핑](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="3039f-208">[![Project contract line milestone template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="3039f-209">프로젝트 및 계약(PSA 3.x에서 Dynamics로) - v2 템플릿의 프로젝트 계약 내용 중요 시점 매핑:</span><span class="sxs-lookup"><span data-stu-id="3039f-209">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="3039f-210">[![두 템플릿 버전이 있는 프로젝트 계약 내용 중요 시점 매핑](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="3039f-210">[![Project contract line milestone mapping with version two template](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]