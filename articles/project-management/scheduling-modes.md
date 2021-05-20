---
title: 예약 모드
description: 이 주제는 예약 모드에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981443"
---
# <a name="scheduling-modes"></a><span data-ttu-id="c5b38-103">예약 모드</span><span class="sxs-lookup"><span data-stu-id="c5b38-103">Scheduling modes</span></span>

<span data-ttu-id="c5b38-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="c5b38-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c5b38-105">Dynamics 365 Project Operations는 조직이 작업 분할 구조 내에서 작업의 주요 변수에 대한 변경 사항을 관리하는 방법을 정의할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="c5b38-106">조직의 특정 요구 사항에 따라 프로젝트 관리자는 프로젝트가 생성될 때 일정 모드를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="c5b38-107">Project Operations에서 사용할 수 있는 세 가지 예약 모드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="c5b38-108">고정 기간(기본 모드)</span><span class="sxs-lookup"><span data-stu-id="c5b38-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="c5b38-109">작업 고정</span><span class="sxs-lookup"><span data-stu-id="c5b38-109">Fixed work</span></span>
  - <span data-ttu-id="c5b38-110">단위 고정</span><span class="sxs-lookup"><span data-stu-id="c5b38-110">Fixed units</span></span>

<span data-ttu-id="c5b38-111">특정 예약 모드의 정의에 영향을 받는 값은 다음 공식에 의해 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="c5b38-112">작업량(*작업*) = 기간 x 단위</span><span class="sxs-lookup"><span data-stu-id="c5b38-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="c5b38-113">프로젝트의 예약 모드를 정의할 때 이러한 값 중 하나를 설정하는 것이므로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="c5b38-114">이 값을 상수로 유지하면 해당 값에 우선 순위가 지정되어 다른 두 값이 변경될 때 변경되지 않도록 시스템에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="c5b38-115">다음 표는 특정 모드 선택의 영향에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="c5b38-116">**이 작업**</span><span class="sxs-lookup"><span data-stu-id="c5b38-116">**In this task**</span></span>             | <span data-ttu-id="c5b38-117">**단위를 수정하는 경우**</span><span class="sxs-lookup"><span data-stu-id="c5b38-117">**If you revise units**</span></span>   | <span data-ttu-id="c5b38-118">**기간을 수정하는 경우**</span><span class="sxs-lookup"><span data-stu-id="c5b38-118">**If you revise duration**</span></span> | <span data-ttu-id="c5b38-119">**작업량을 수정하는 경우**</span><span class="sxs-lookup"><span data-stu-id="c5b38-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="c5b38-120">고정 단위 작업</span><span class="sxs-lookup"><span data-stu-id="c5b38-120">Fixed units task</span></span>     | <span data-ttu-id="c5b38-121">기간이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-121">Duration is recalculated.</span></span> | <span data-ttu-id="c5b38-122">작업량이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-122">Effort is recalculated.</span></span>    | <span data-ttu-id="c5b38-123">기간이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="c5b38-124">고정된 작업량 작업</span><span class="sxs-lookup"><span data-stu-id="c5b38-124">Fixed effort task</span></span>    | <span data-ttu-id="c5b38-125">기간이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-125">Duration is recalculated.</span></span> | <span data-ttu-id="c5b38-126">단위가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-126">Units are recalculated.</span></span>    | <span data-ttu-id="c5b38-127">기간이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="c5b38-128">고정된 기간 작업</span><span class="sxs-lookup"><span data-stu-id="c5b38-128">Fixed duration task</span></span>  | <span data-ttu-id="c5b38-129">작업량이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-129">Effort is recalculated.</span></span>   | <span data-ttu-id="c5b38-130">작업량이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-130">Effort is recalculated.</span></span>    | <span data-ttu-id="c5b38-131">단위가 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-131">Units are recalculated.</span></span>   |

<span data-ttu-id="c5b38-132">주어진 모드의 의미에 대한 자세한 정보는 [보다 정확한 예약을 위해 작업 유형 변경](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5b38-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="c5b38-133">항목에서 용어 **작업** 대신 **작업량** 이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="c5b38-134">조직의 예약 모드 변경</span><span class="sxs-lookup"><span data-stu-id="c5b38-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="c5b38-135">조직의 예약 모드를 정의하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5b38-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="c5b38-136">**설정** \> **일반** \> **매개 변수** 로 이동한 다음 프로젝트 매개 변수를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="c5b38-137">**프로젝트 매개 변수** 페이지에서 조직의 기본 예약 모드를 선택한 다음 새 프로젝트를 만들 때 프로젝트 관리자가 설정을 재정의 할 수 있는 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="c5b38-138">프로젝트에서 예약 모드 설정 변경</span><span class="sxs-lookup"><span data-stu-id="c5b38-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="c5b38-139">조직에서 프로젝트 관리자가 기본 예약 모드를 재정의하도록 허용하면 프로젝트 관리자는 새 프로젝트를 만들 때 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="c5b38-140">그러나 프로젝트를 저장한 후에는 예약 모드를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="c5b38-141">복사된 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c5b38-141">Copied projects</span></span>

<span data-ttu-id="c5b38-142">프로젝트 복사 작업이 수행될 때 프로젝트가 생성되기 때문에 프로젝트 관리자는 예약 모드를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="c5b38-143">대상 프로젝트는 항상 조직 수준에서 정의된 모드로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="c5b38-144">복사된 작업</span><span class="sxs-lookup"><span data-stu-id="c5b38-144">Copied tasks</span></span>

<span data-ttu-id="c5b38-145">작업이 한 프로젝트에서 다른 프로젝트로 복사되면 작업은 대상 프로젝트의 예약 모드를 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b38-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
