---
title: 예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다.
description: 이 항목에서는 프로젝트에서 여러 역할을 수행하는 리소스의 가격 책정 및 비용을 지원하기 위해 가격 책정 차원을 사용하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145051"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="d7b6a-103">예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d7b6a-104">프로젝트 기반 회사는 종종 프로젝트에서 여러 역할을 수행하기 위해 하나의 리소스가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="d7b6a-105">이러한 각 역할은 가격이 책정되고 비용이 다르게 책정될 수 있습니다. 즉, 프로젝트에서 동일한 리소스의 시간이 각 역할의 청구서 및 비용 요율에 따라 다른 재무 추정치를 얻을 수 있음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="d7b6a-106">Project Service Automation을 사용하면 명명된 리소스에 대한 팀 구성원 레코드의 값을 설정할 수 있으며 팀 구성원이 할당된 각 작업에 대해 다른 재정의가 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="d7b6a-107">다음 예에서는 이 값의 단순 재정의를 통해 리소스가 비용 및 청구 요율이 다른 프로젝트에서 여러 역할을 가질 수 있는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="d7b6a-108">작업 만들기</span><span class="sxs-lookup"><span data-stu-id="d7b6a-108">Create tasks</span></span>
<span data-ttu-id="d7b6a-109">각각 40시간 동안 두 개의 프로젝트 작업(작업 A 및 작업 B)을 만듭니다. 작업 B의 선행 작업으로 작업 A를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="d7b6a-110">일반 프로젝트 팀 구성원에 대한 역할 및 조직 단위 설정</span><span class="sxs-lookup"><span data-stu-id="d7b6a-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="d7b6a-111">**일정** 페이지에서 작업 A의 **작업** 행을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="d7b6a-112">**리소스** 필드의 드롭다운 목록에서 **만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="d7b6a-113">**팀 구성원 빨리 만들기** 페이지에서 이 작업을 수행할 수 있는 일반 팀 구성원의 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="d7b6a-114">적절한 역할 및 조직 구성 단위를 선택한 다음 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="d7b6a-115">일반 팀 구성원이 생성되고 이 작업에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="d7b6a-116">작업 B에 대해 이러한 단계를 반복하고 작업 B에 대해 생성된 일반 팀 구성원의 역할 및 조직 단위가 작업 A와 다른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="d7b6a-117">프로젝트 작업에 대한 역할 및 조직 구성 단위 설정</span><span class="sxs-lookup"><span data-stu-id="d7b6a-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="d7b6a-118">작업 A를 생성한 후 작업을 선택한 다음 **작업 편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="d7b6a-119">**작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 필드에 이 작업을 수행할 리소스에 필요한 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="d7b6a-120">Project Service Automation 데모 데이터를 사용하여 이 시나리오를 완료하는 경우 **컨설팅 리드** 역할 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="d7b6a-121">작업 B를 선택한 다음, **작업 편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="d7b6a-122">**작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 필드에 이 작업을 수행할 리소스에 필요한 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="d7b6a-123">**역할** 과 **조직 구성 단위** 필드의 값이 작업 A의 값과 작업 B의 값이 다른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="d7b6a-124">Project Service Automation 데모 데이터를 사용하여 이 시나리오를 완료하는 경우 **네트워크 기술자** 역할 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="d7b6a-125">저장 후 **작업 세부 정보** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="d7b6a-126">팀 구성원 및 추정 행동</span><span class="sxs-lookup"><span data-stu-id="d7b6a-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="d7b6a-127">**작업 세부 정보** 페이지의 **팀 구성원** 에서 두 개의 일반 팀 구성원을 선택한 다음 **요구 사항 생성** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="d7b6a-128">**컨설팅 리드** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="d7b6a-129">일정 게시판이 열리고 해당 요구 사항에 대한 리소스가 예약됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="d7b6a-130">**네트워크 기술자** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="d7b6a-131">일정 게시판이 열리고 해당 요구 사항에 대한 동일한 리소스가 예약됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="d7b6a-132">팀 구성원 그리드</span><span class="sxs-lookup"><span data-stu-id="d7b6a-132">Team Member grid</span></span> 
<span data-ttu-id="d7b6a-133">**팀 구성원** 그리드에서 두 개의 일반 팀 구성원 레코드가 삭제되고 하나의 리소스로 대체되었음을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="d7b6a-134">**역할** 및 **조직 구성 단위** 에 대한 기본 값 집합을 보여주는 해당 리소스에 대한 값 집합이 하나 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="d7b6a-135">해당 팀 구성원 레코드의 행을 확장하면 두 작업 모두에 대해 팀 구성원 레코드에서 고유한 할당을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="d7b6a-136">각 할당 행에는 **역할** 및 **조직 구성 단위** 에 대한 작업별 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="d7b6a-137">추정 그리드</span><span class="sxs-lookup"><span data-stu-id="d7b6a-137">Estimates grid</span></span> 
<span data-ttu-id="d7b6a-138">**추정** 그리드로 이동할 때 동일한 리소스에 대한 두 할당의 가격이 다르게 책정됨을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="d7b6a-139">작업 A의 리소스 할당은 **컨설팅 리드** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="d7b6a-140">작업 B의 동일한 리소스 할당은 **네트워크 기술자** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7b6a-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>

