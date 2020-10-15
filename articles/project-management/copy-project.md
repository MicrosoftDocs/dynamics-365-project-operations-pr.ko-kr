---
title: 프로젝트 복사
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트 복사에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908341"
---
# <a name="copy-a-project"></a><span data-ttu-id="6902d-103">프로젝트 복사</span><span class="sxs-lookup"><span data-stu-id="6902d-103">Copy a project</span></span>

<span data-ttu-id="6902d-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="6902d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6902d-105">Dynamics 365 Project Operations를 사용하면 **프로젝트**에서 **프로젝트 복사** 작업을 사용하여 새 프로젝트를 빠르게 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="6902d-106">프로젝트를 복사하려면 프로젝트를 선택한 다음 **복사**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="6902d-107">작업이 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-107">The action will copy:</span></span>

- <span data-ttu-id="6902d-108">프로젝트 속성</span><span class="sxs-lookup"><span data-stu-id="6902d-108">Project properties</span></span>
- <span data-ttu-id="6902d-109">작업 분할 구조</span><span class="sxs-lookup"><span data-stu-id="6902d-109">The Work breakdown structure</span></span>
- <span data-ttu-id="6902d-110">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="6902d-110">Project team members</span></span>
- <span data-ttu-id="6902d-111">프로젝트 추정</span><span class="sxs-lookup"><span data-stu-id="6902d-111">Project estimates</span></span>
- <span data-ttu-id="6902d-112">프로젝트 경비 추정치</span><span class="sxs-lookup"><span data-stu-id="6902d-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="6902d-113">프로젝트 속성</span><span class="sxs-lookup"><span data-stu-id="6902d-113">Project properties</span></span>

<span data-ttu-id="6902d-114">프로젝트가 복사되면 다음 필드의 값이 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="6902d-115">Name</span><span class="sxs-lookup"><span data-stu-id="6902d-115">Name</span></span>
- <span data-ttu-id="6902d-116">설명</span><span class="sxs-lookup"><span data-stu-id="6902d-116">Description</span></span>
- <span data-ttu-id="6902d-117">고객</span><span class="sxs-lookup"><span data-stu-id="6902d-117">Customer</span></span>
- <span data-ttu-id="6902d-118">일정 템플릿</span><span class="sxs-lookup"><span data-stu-id="6902d-118">Calendar Template</span></span>
- <span data-ttu-id="6902d-119">통화</span><span class="sxs-lookup"><span data-stu-id="6902d-119">Currency</span></span>
- <span data-ttu-id="6902d-120">계약 단위</span><span class="sxs-lookup"><span data-stu-id="6902d-120">Contracting Unit</span></span>
- <span data-ttu-id="6902d-121">프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="6902d-121">Project Manager</span></span>
- <span data-ttu-id="6902d-122">상태</span><span class="sxs-lookup"><span data-stu-id="6902d-122">Status</span></span>
- <span data-ttu-id="6902d-123">전체 프로젝트 상태</span><span class="sxs-lookup"><span data-stu-id="6902d-123">Overall Project Status</span></span>
- <span data-ttu-id="6902d-124">메모</span><span class="sxs-lookup"><span data-stu-id="6902d-124">Comments</span></span>
- <span data-ttu-id="6902d-125">추정</span><span class="sxs-lookup"><span data-stu-id="6902d-125">Estimates</span></span>
- <span data-ttu-id="6902d-126">예상 시작 날짜</span><span class="sxs-lookup"><span data-stu-id="6902d-126">Estimated Start Date</span></span>
- <span data-ttu-id="6902d-127">완료 날짜</span><span class="sxs-lookup"><span data-stu-id="6902d-127">Finish Date</span></span>
- <span data-ttu-id="6902d-128">작업량(시간)</span><span class="sxs-lookup"><span data-stu-id="6902d-128">Effort (Hours)</span></span>
- <span data-ttu-id="6902d-129">예상 노동 비용</span><span class="sxs-lookup"><span data-stu-id="6902d-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="6902d-130">예상 경비 비용</span><span class="sxs-lookup"><span data-stu-id="6902d-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="6902d-131">작업 분할 구조</span><span class="sxs-lookup"><span data-stu-id="6902d-131">Work breakdown structure</span></span>

<span data-ttu-id="6902d-132">프로젝트를 복사하면 전체 리소스 로드 작업 분할 구조가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="6902d-133">명명된 리소스가 일반 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="6902d-134">명명된 리소스의 작업 시간이 일반 리소스와 동일하지 않은 경우 일정이 다시 계산되고 작업 기간이 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="6902d-135">프로젝트 팀 구성원</span><span class="sxs-lookup"><span data-stu-id="6902d-135">Project team members</span></span>

<span data-ttu-id="6902d-136">원본 프로젝트에서 프로젝트 팀을 복사하면 일반 리소스가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="6902d-137">일반 리소스 배정은 원본 프로젝트에서와 같이 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="6902d-138">명명된 리소스는 일반 팀 구성원으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="6902d-139">추정</span><span class="sxs-lookup"><span data-stu-id="6902d-139">Estimates</span></span>

<span data-ttu-id="6902d-140">프로젝트가 복사되면 리소스 및 경비 추정 라인이 모두 원본 프로젝트에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="6902d-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>