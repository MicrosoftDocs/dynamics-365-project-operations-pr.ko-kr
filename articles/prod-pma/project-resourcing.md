---
title: 프로젝트 리소싱 홈 페이지
description: 이 항목은 프로젝트 리소싱에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ecf8ee588de9ec41e0b4f384110f912759ed53f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080038"
---
# <a name="project-resourcing-home-page"></a><span data-ttu-id="74fbe-103">프로젝트 리소싱 홈 페이지</span><span class="sxs-lookup"><span data-stu-id="74fbe-103">Project resourcing home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74fbe-104">이 항목은 프로젝트 리소싱에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="74fbe-105">프로젝트 계획 단계에서 프로젝트 관리자와 리소스 관리자가 겪는 한 가지 과제는 리소스 할당으로, 프로젝트에서 작업할 올바른 리소스를 결정하고 예약해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="74fbe-106">Dynamics 365 Finance에서는 프로젝트에 대한 리소스 기능을 사용하면 특정 참여 또는 참여의 일부를 위해 예약할 수 있는 임시 리소스로 처리되는 역할을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-106">In Dynamics 365 Finance, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="74fbe-107">이러한 유형의 리소싱을 통해 프로젝트 관리자와 리소스 관리자는 다음 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="74fbe-108">리소스를 쉽게 일치시킬 수 있도록 필요한 역량이 있는 역할을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="74fbe-109">역할을 사용하여 예약된 리소스를 기반으로 하는 초기 참여 일정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="74fbe-110">프로젝트에 할당된 역할 및 리소스를 기반으로 비용을 추정하고 초기 예산을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="74fbe-111">역할을 사용하여 각 참여에 필요한 리소스 예약 수를 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="74fbe-112">프로젝트의 전체 수명 주기에 필요한 리소스 수를 추정합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="74fbe-113">초기 리소스 할당을 사용하여 작업 분할 구조(WBS) 초안을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="74fbe-114">[![프로젝트 수명 주기](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="74fbe-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="74fbe-115">프로젝트 계획이 진행됨에 따라 계획된 리소스는 인력이 있는 리소스로 대체될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="74fbe-116">프로젝트 관리자는 모든 프로젝트 단계에서 다시 돌아가 리소스 예약을 업데이트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

<span data-ttu-id="74fbe-117">다음 항목은 리소스 조달 프로젝트에서 작업할 때 완료해야 하는 작업에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="74fbe-117">The following topics provide information about the tasks that need to be completed when you are working on resourcing projects.</span></span>

- [<span data-ttu-id="74fbe-118">프로젝트 리소스 설정</span><span class="sxs-lookup"><span data-stu-id="74fbe-118">Set up project resources</span></span>](set-up-project-resources.md)
- [<span data-ttu-id="74fbe-119">리소스 역량 관리</span><span class="sxs-lookup"><span data-stu-id="74fbe-119">Manage resource competencies</span></span>](manage-resource-competencies.md)
- [<span data-ttu-id="74fbe-120">새 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="74fbe-120">Create a new project</span></span>](create-new-project.md)
- [<span data-ttu-id="74fbe-121">역할 기반 가격 책정 설정</span><span class="sxs-lookup"><span data-stu-id="74fbe-121">Set up role-based pricing</span></span>](set-up-role-based-pricing.md)
- [<span data-ttu-id="74fbe-122">프로젝트 팀 만들기</span><span class="sxs-lookup"><span data-stu-id="74fbe-122">Create a project team</span></span>](create-project-team.md)
- [<span data-ttu-id="74fbe-123">리소스 용량 동기화</span><span class="sxs-lookup"><span data-stu-id="74fbe-123">Synchronize resource capacity</span></span>](synchronize-resource-capacity.md)
- [<span data-ttu-id="74fbe-124">프로젝트 자원 예약 성능</span><span class="sxs-lookup"><span data-stu-id="74fbe-124">Project resource scheduling performance</span></span>](project-scheduling-performance.md)
- [<span data-ttu-id="74fbe-125">작업 분할 구조 템플릿에서 역할 설정</span><span class="sxs-lookup"><span data-stu-id="74fbe-125">Set up roles on Work breakdown structure templates</span></span>](set-up-roles-wbs-template.md)
- [<span data-ttu-id="74fbe-126">계획된 리소스에 대한 리소스 이행</span><span class="sxs-lookup"><span data-stu-id="74fbe-126">Resource fulfillment for planned resources</span></span>](resource-fulfillment-planned-resources.md)
