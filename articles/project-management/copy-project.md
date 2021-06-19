---
title: 프로젝트 복사
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트 복사에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091262"
---
# <a name="copy-a-project"></a><span data-ttu-id="fb474-103">프로젝트 복사</span><span class="sxs-lookup"><span data-stu-id="fb474-103">Copy a project</span></span>

<span data-ttu-id="fb474-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="fb474-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb474-105">Dynamics 365 Project Operations를 사용하면 **프로젝트** 양식에서 **프로젝트 복사** 를 선택하여 새 프로젝트를 빠르게 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="fb474-106">프로젝트를 복사하려면 복사할 프로젝트를 연 다음 **프로젝트 복사** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="fb474-107">이 작업은 다음을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-107">The action will copy the following:</span></span>

- <span data-ttu-id="fb474-108">프로젝트 속성</span><span class="sxs-lookup"><span data-stu-id="fb474-108">Project properties</span></span> 
- <span data-ttu-id="fb474-109">작업 분할 구조</span><span class="sxs-lookup"><span data-stu-id="fb474-109">Work breakdown structure</span></span>
- <span data-ttu-id="fb474-110">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="fb474-110">Project team members</span></span>
- <span data-ttu-id="fb474-111">프로젝트 추정</span><span class="sxs-lookup"><span data-stu-id="fb474-111">Project estimates</span></span>
- <span data-ttu-id="fb474-112">프로젝트 경비 추정치</span><span class="sxs-lookup"><span data-stu-id="fb474-112">Project expense estimates</span></span>
- <span data-ttu-id="fb474-113">프로젝트 재료 추정</span><span class="sxs-lookup"><span data-stu-id="fb474-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="fb474-114">프로젝트 속성</span><span class="sxs-lookup"><span data-stu-id="fb474-114">Project properties</span></span>

<span data-ttu-id="fb474-115">프로젝트가 복사되면 다음 필드의 값이 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="fb474-116">Name</span><span class="sxs-lookup"><span data-stu-id="fb474-116">Name</span></span>
- <span data-ttu-id="fb474-117">설명</span><span class="sxs-lookup"><span data-stu-id="fb474-117">Description</span></span>
- <span data-ttu-id="fb474-118">고객</span><span class="sxs-lookup"><span data-stu-id="fb474-118">Customer</span></span>
- <span data-ttu-id="fb474-119">일정 템플릿</span><span class="sxs-lookup"><span data-stu-id="fb474-119">Calendar Template</span></span>
- <span data-ttu-id="fb474-120">통화</span><span class="sxs-lookup"><span data-stu-id="fb474-120">Currency</span></span>
- <span data-ttu-id="fb474-121">계약 단위</span><span class="sxs-lookup"><span data-stu-id="fb474-121">Contracting Unit</span></span>
- <span data-ttu-id="fb474-122">프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="fb474-122">Project Manager</span></span>
- <span data-ttu-id="fb474-123">상태</span><span class="sxs-lookup"><span data-stu-id="fb474-123">Status</span></span>
- <span data-ttu-id="fb474-124">전체 프로젝트 상태</span><span class="sxs-lookup"><span data-stu-id="fb474-124">Overall Project Status</span></span>
- <span data-ttu-id="fb474-125">댓글</span><span class="sxs-lookup"><span data-stu-id="fb474-125">Comments</span></span>
- <span data-ttu-id="fb474-126">추정</span><span class="sxs-lookup"><span data-stu-id="fb474-126">Estimates</span></span>
- <span data-ttu-id="fb474-127">예상 시작 날짜: 프로젝트가 사본에서 생성된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="fb474-128">예상 완료 날짜: 이 날짜는 복사본에서 만든 새 프로젝트의 시작 날짜를 기준으로 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="fb474-129">작업량(시간)</span><span class="sxs-lookup"><span data-stu-id="fb474-129">Effort (Hours)</span></span>
- <span data-ttu-id="fb474-130">예상 노동 비용</span><span class="sxs-lookup"><span data-stu-id="fb474-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="fb474-131">예상 경비 비용</span><span class="sxs-lookup"><span data-stu-id="fb474-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="fb474-132">예상 재료 비용</span><span class="sxs-lookup"><span data-stu-id="fb474-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="fb474-133">프로젝트 복사는 장기 실행 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-133">Copy project is a long running operation.</span></span> <span data-ttu-id="fb474-134">프로젝트 레코드, 관련 속성 및 많은 관련 엔터티도 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="fb474-135">작업의 장기 실행 특성으로 인해 복사가 시작된 후 복사 작업이 완료될 때까지 편집을 위해 대상 프로젝트 페이지가 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="fb474-136">작업 분할 구조</span><span class="sxs-lookup"><span data-stu-id="fb474-136">Work breakdown structure</span></span>

<span data-ttu-id="fb474-137">프로젝트를 복사하면 전체 리소스 로드 작업 분할 구조가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="fb474-138">명명된 리소스가 일반 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="fb474-139">명명된 리소스의 작업 시간이 일반 리소스와 동일하지 않은 경우 일정이 다시 계산되고 작업 기간이 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="fb474-140">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="fb474-140">Project team members</span></span>

<span data-ttu-id="fb474-141">원본 프로젝트에서 프로젝트 팀을 복사하면 일반 리소스가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="fb474-142">일반 리소스 배정은 원본 프로젝트에서와 같이 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="fb474-143">명명된 리소스는 일반 팀 구성원으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="fb474-144">추정</span><span class="sxs-lookup"><span data-stu-id="fb474-144">Estimates</span></span>

<span data-ttu-id="fb474-145">프로젝트를 복사하면 소스 프로젝트에서 리소스, 경비 및 자재 견적 라인이 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb474-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="fb474-146">프로젝트 복사에 프로그래밍 방식으로 액세스하는 방법에 대한 자세한 내용은 [프로젝트 복사로 프로젝트 템플릿 개발](dev-copy-project.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fb474-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
