---
title: Project Service Automation 업데이트 릴리스 16, V3의 새로운 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 16, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753272"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="e5399-103">Project Service Automation V3, 업데이트 릴리스 16</span><span class="sxs-lookup"><span data-stu-id="e5399-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="e5399-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e5399-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="e5399-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e5399-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="e5399-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e5399-108">자세한 내용은 [선호 솔루션의 설치, 업데이트](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5399-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="e5399-109">이 항목에는 PSA V3, 업데이트 릴리스 16에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="e5399-110">이 버전의 빌드 번호는 V3.10.6.34이며 2020년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="e5399-111">업데이트 릴리스 16</span><span class="sxs-lookup"><span data-stu-id="e5399-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e5399-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="e5399-112">Bug fixes</span></span>

-   <span data-ttu-id="e5399-113">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="e5399-113">Time and Expense</span></span>

    -   <span data-ttu-id="e5399-114">해결: 승인을 위해 삭제된 시간 및 경비 항목을 제출하려는 사용자는 이제 관련 오류 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="e5399-115">프로젝트 관리</span><span class="sxs-lookup"><span data-stu-id="e5399-115">Project Management</span></span>

    -   <span data-ttu-id="e5399-116">해결: 템플릿에서 팀 구성원에 대해 정의된 리포지토리 단위는 템플릿이 새 프로젝트에 적용되는 것을 존중합니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="e5399-117">해결: 레코드 소유권 재할당 처리 기능이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="e5399-118">해결: 복사가 진행 중인 프로젝트는 모든 복사 작업이 완료될 때까지 복사할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="e5399-119">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="e5399-119">Resource Management</span></span>

    -   <span data-ttu-id="e5399-120">해결: 예약 확장이 이제 짧은 지속 시간을 올바르게 처리하고 더 이상 확장 예약에 대해 0시간을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="e5399-121">해결: 이제 프로젝트 시간대가 +5:30 GMT이고 사용자의 시간이 다를 때 조정 보기가 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="e5399-122">Sales</span><span class="sxs-lookup"><span data-stu-id="e5399-122">Sales</span></span>

    -   <span data-ttu-id="e5399-123">해결: 계약 라인에 매핑된 프로젝트가 제거되고 새 프로젝트가 매핑될 때 계약 라인에 정의된 대금 청구 및 가격 규칙에 따라 새 프로젝트의 실제 레코드가 재평가되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="e5399-124">이 릴리스에서 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-124">This has been fixed in this release.</span></span> <span data-ttu-id="e5399-125">새로 매핑된 프로젝트의 가격 및 실제 레코드는 계약 라인의 가격 및 청구 규칙에 따라 올바르게 되돌려지고 다시 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="e5399-126">매핑되지 않은 프로젝트의 실제 레코드도 결과적으로 다시 평가되고 다시 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="e5399-127">해결: null 값이 유지되지 않도록 추가 유효성 검사가 견적 라인의 **금액** 필드에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="e5399-128">해결: 프로젝트에서 실제가 업데이트되면 사용자가 실제를 다시 동기화할 수 있도록 프로젝트 기본 양식에 새로 고침 단추가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="e5399-129">해결: 사용자가 2.X에서 3.X로 업그레이드할 때 프로젝트 이름에 NULL 값을 가진 프로젝트가 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5399-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

