---
title: 프로젝트 업데이트
description: 이 항목은 Project Operations의 프로젝트 업데이트에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079907"
---
# <a name="update-a-project"></a><span data-ttu-id="a0e16-103">프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a0e16-103">Update a project</span></span>

<span data-ttu-id="a0e16-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a0e16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a0e16-105">다음은 프로젝트가 생성된 후 업데이트될 수 있는 필드와 업데이트의 적용 가능한 의미에 대한 요약입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="a0e16-106">프로젝트 세부 사항 필드</span><span class="sxs-lookup"><span data-stu-id="a0e16-106">Project detail fields</span></span>

- <span data-ttu-id="a0e16-107">**이름** : 프로젝트의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="a0e16-108">**설명** : 프로젝트의 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="a0e16-109">**고객** : 프로젝트를 전달할 회사입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="a0e16-110">**일정 템플릿** : 프로젝트의 작업 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="a0e16-111">필드가 변경되면 전체 일정이 다시 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="a0e16-112">**통화** : 프로젝트의 통화입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="a0e16-113">이 필드의 기본값은 계약 단위에 정의된 통화를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="a0e16-114">계약 단위가 업데이트되면 필드도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="a0e16-115">**계약 단위** : 판매에 성공하고 고객에게 작업 및 서비스 제공을 관리하는 책임이 있는 회사 그룹 또는 부서를 대표하는 조직 구성 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="a0e16-116">**프로젝트 관리자** : 시간 항목 및 경비를 검토하고 승인할 권한이 있는 프로젝트 팀 구성원입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="a0e16-117">추정 필드</span><span class="sxs-lookup"><span data-stu-id="a0e16-117">Estimate fields</span></span>

- <span data-ttu-id="a0e16-118">**예상 시작 날짜** : 프로젝트가 시작되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="a0e16-119">이 필드가 업데이트되면 프로젝트의 모든 작업이 새 시작 날짜에 비례하여 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="a0e16-120">**종료 날짜** : 프로젝트 종료 예정 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="a0e16-121">**작업량** : 프로젝트의 예상 작업량입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="a0e16-122">프로젝트에 작업이 추가되면 이 필드는 더 이상 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="a0e16-123">**예상 노동 비용** : 프로젝트의 예상 노동 비용입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="a0e16-124">프로젝트에 노동 비용이 추가되면 이 필드는 더 이상 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="a0e16-125">**예상 경비** : 프로젝트의 예상 경비입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="a0e16-126">프로젝트에 경비가 추가되면 이 필드는 더 이상 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="a0e16-127">프로젝트 실제 필드</span><span class="sxs-lookup"><span data-stu-id="a0e16-127">Project actual fields</span></span>
- <span data-ttu-id="a0e16-128">**실제 시작** : 프로젝트가 시작된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="a0e16-129">**실제 종료** : 프로젝트가 완료되면 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="a0e16-130">프로젝트 상태 필드</span><span class="sxs-lookup"><span data-stu-id="a0e16-130">Project status fields</span></span>

- <span data-ttu-id="a0e16-131">**전체 프로젝트 상태** : 프로젝트 관리자가 제공한 전체 프로젝트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="a0e16-132">**댓글** : 프로젝트 관리자가 제공한 프로젝트의 현재 상태에 대한 댓글입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e16-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

