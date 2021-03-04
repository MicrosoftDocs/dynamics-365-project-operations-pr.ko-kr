---
title: 프로젝트 설정
description: 이 항목은 프로젝트 관리 설정에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148156"
---
# <a name="project-settings"></a><span data-ttu-id="5b8f8-103">프로젝트 설정</span><span class="sxs-lookup"><span data-stu-id="5b8f8-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5b8f8-104">다음 설정을 사용하여 프로젝트 계획 기능에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="5b8f8-105">작업 템플릿</span><span class="sxs-lookup"><span data-stu-id="5b8f8-105">Work template</span></span>

<span data-ttu-id="5b8f8-106">프로젝트 스케줄을 생성하려면 일당 작업 시간 수와 휴무를 정의하는 프로젝트 캘린더 템플릿을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="5b8f8-107">프로젝트 캘린더 템플릿을 생성하려면 프로젝트를 위한 **Calendar 캘린더 템플릿** 필드와 작업 템플릿을 연계합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="5b8f8-108">다음 단계에 따라 작업 템플릿을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="5b8f8-109">PSA의 왼쪽 탐색 창에서 **리소스** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="5b8f8-110">**리소스** 목록 페이지에서 사용자 레코드를 연 다음 **작업 시간 수 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5b8f8-111">브라우저 페이지에서 팝업을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="5b8f8-112">이렇게 하면 리소스에 대해 설정된 작업 시간 수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="5b8f8-113">**월별 보기** 탭에서 **설정** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="5b8f8-114">세 가지 옵션의 목록이 나타납니다:</span><span class="sxs-lookup"><span data-stu-id="5b8f8-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="5b8f8-115">새 주별 스케줄</span><span class="sxs-lookup"><span data-stu-id="5b8f8-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="5b8f8-116">하루 작업 스케줄</span><span class="sxs-lookup"><span data-stu-id="5b8f8-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="5b8f8-117">휴가</span><span class="sxs-lookup"><span data-stu-id="5b8f8-117">Time Off</span></span>

> ![옵션 설정](media/project-13.png)

4. <span data-ttu-id="5b8f8-119">**새 주별 스케줄** 을 선택한 다음 이 리소스 스케줄에 대한 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="5b8f8-120">되풀이되는 주간 일정, 일일 시간 파라미터, 휴무 등을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="5b8f8-121">날짜 범위를 설정하고 **저장** 을 선택한 다음 **닫기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="5b8f8-122">**리소스** 목록 페이지로 돌아가서 작업 시간을 설정한 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="5b8f8-123">**캘린더를 설정** 을 선택하여 작업 템플릿을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="5b8f8-124">**작업 템플릿** 대화 상자에서 작업 템플릿의 명칭을 입력한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="5b8f8-125">이제 작업 템플릿을 프로젝트 스케줄 템플릿과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="5b8f8-126">리소스 역할</span><span class="sxs-lookup"><span data-stu-id="5b8f8-126">Resource roles</span></span>

<span data-ttu-id="5b8f8-127">*리소스 역할* 이라는 용어는 사람이 프로젝트에서 특정 작업 집합을 수행해야 하는 기능, 역량 및 자격증 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="5b8f8-128">PSA를 사용하면 리소스가 연계된 역할에 근거한 리소스의 시간 비용을 추산하여 청구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="5b8f8-129">모든 조직은 **Project Service** 메뉴에서 왼쪽 탐색을 사용하여 이러한 역할을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="5b8f8-130">모든 조직은 **활성 리소스 카테고리** 페이지에서 이러한 역할을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="5b8f8-131">이 페이지를 열려면 왼쪽 탐색 창에서 **리소스 역할** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="5b8f8-132">가격표</span><span class="sxs-lookup"><span data-stu-id="5b8f8-132">Price lists</span></span>

<span data-ttu-id="5b8f8-133">가격표에서 조직에서의 리소스 역할, 경비 카테고리, 제품 및 기타 요소를 위한 원가와 판매 가격을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="5b8f8-134">프로젝트를 위해 인도해야 하는 작업의 재무 추산을 설정하기 전에 증빙 원가와 판매 가격표를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="5b8f8-135">파라미터 섹션에서 조직에서 만든 모든 프로젝트에 적용되는 기본 원가 및 판매 가격표도 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="5b8f8-136">**활성 프로젝트 파라미터** 페이지에서 기본 원가 및 판매 가격표를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8f8-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
