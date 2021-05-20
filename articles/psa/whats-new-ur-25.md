---
title: Project Service Automation 업데이트 릴리스 25, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 25, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948879"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="c5abb-103">Project Service Automation 업데이트 릴리스 25, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="c5abb-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c5abb-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c5abb-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c5abb-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c5abb-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5abb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c5abb-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c5abb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c5abb-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 25에 대해 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.이 버전에는 V 3.10.43.76의 빌드 번호가 있으며 일반적으로 2020년 10월에 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="c5abb-110">업데이트 릴리스 25</span><span class="sxs-lookup"><span data-stu-id="c5abb-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c5abb-111">버그 수정</span><span class="sxs-lookup"><span data-stu-id="c5abb-111">Bug fixes</span></span>

<span data-ttu-id="c5abb-112">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="c5abb-112">**Time and Expense**</span></span>

<span data-ttu-id="c5abb-113">다음 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="c5abb-114">검색되는 너무 큰 간격을 기반으로 추가 데이터를 표시하는 시간 입력 차트.</span><span class="sxs-lookup"><span data-stu-id="c5abb-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="c5abb-115">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="c5abb-115">**Resource Management**</span></span>

<span data-ttu-id="c5abb-116">다음 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="c5abb-117">Package Deployer 코드를 추가하여 더 높은 버전의 패치가 이미 있는 경우 Universal Resource Scheduling 패치 가져오기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="c5abb-118">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="c5abb-118">**Project Management**</span></span>

<span data-ttu-id="c5abb-119">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="c5abb-120">반올림 및 환율 불일치를 수정하여 프로젝트 추적 그리드에서 계획된 비용이 잘못되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="c5abb-121">**프로젝트** 양식에서 두 개 이상의 반응 그리드를 표시하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="c5abb-122">달력 종료 날짜가 지난 작업을 할당할 수 있는 기능을 해결하기 위한 유효성 검사를 제공하여 리소스 할당이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="c5abb-123">다음에서 생성된 Null 참조 예외를 해결하기 위해 오류 처리가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="c5abb-124">**PreValidateProjectTeamMemberCreate** 플러그인</span><span class="sxs-lookup"><span data-stu-id="c5abb-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="c5abb-125">연결된 프로젝트 없이 프로젝트 작업이 생성될 때 **PreValidateProjectTaskCreate**</span><span class="sxs-lookup"><span data-stu-id="c5abb-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="c5abb-126">**PreProjectTeamMemberCreate** 플러그인</span><span class="sxs-lookup"><span data-stu-id="c5abb-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="c5abb-127">**PostProjectTeamMemberDelete** 플러그인</span><span class="sxs-lookup"><span data-stu-id="c5abb-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="c5abb-128">**PreValidateProjectTaskDelete** 플러그인</span><span class="sxs-lookup"><span data-stu-id="c5abb-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="c5abb-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c5abb-129">**Sales**</span></span>

<span data-ttu-id="c5abb-130">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="c5abb-131">**프로젝트 복사: 도우미 리소스 관리 추정** 에서 생성된 Null 참조 예외를 해결하기 위해 오류 처리가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="c5abb-132">**시간 및 재료 청구 백로그** 의 **송장 발부 준비 안 됨** 이 청구 상태를 지우지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="c5abb-133">**역할 가격** 및 **카탈로그 항목** 탭의 잘못된 라벨 **가격** 단추가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5abb-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]