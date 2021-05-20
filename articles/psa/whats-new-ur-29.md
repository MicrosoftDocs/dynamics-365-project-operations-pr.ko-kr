---
title: Project Service Automation 업데이트 릴리스 29, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 29, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948656"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="8ed28-103">Project Service Automation 업데이트 릴리스 29, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="8ed28-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8ed28-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8ed28-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8ed28-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8ed28-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ed28-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8ed28-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8ed28-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8ed28-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 29에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="8ed28-110">이 버전의 빌드 번호는 V3.10.47.7이며 2021년 2월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="8ed28-111">업데이트 릴리스 29</span><span class="sxs-lookup"><span data-stu-id="8ed28-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8ed28-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="8ed28-112">Bug fixes</span></span>

<span data-ttu-id="8ed28-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="8ed28-113">**Time and Expense**</span></span>

<span data-ttu-id="8ed28-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ed28-115">사용자는 시간 입력 그리드에서 휴무일에 기록된 근무 시간을 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="8ed28-116">승인된 경비 항목은 그리드에서 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="8ed28-117">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="8ed28-117">**Project Management**</span></span>

<span data-ttu-id="8ed28-118">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ed28-119">리소스 할당 작업 시간을 보장하기 위한 검증 로직이 누락되어도 음수일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="8ed28-120">사용자 지정 작업 **AssignResourcesForTask** 는 변경된 필드 대신 모든 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="8ed28-121">플러그인 또는 워크플로가 있는 환경에서 프로젝트를 복사할 때 **CreateProject** 이벤트, **msdyn_bulkgenerationstatus** 특성은 **CopyWBSToProject** 가 실패하면 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="8ed28-122">프로젝트 달력을 확장하면 작업일이 오름차순으로 정렬되지 않아 일부 프로젝트 작업 업데이트가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="8ed28-123">기존 프로젝트에서 프로젝트 관리자를 변경하면 조직 단위 기본값 논리가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="8ed28-124">**판매**</span><span class="sxs-lookup"><span data-stu-id="8ed28-124">**Sales**</span></span>

<span data-ttu-id="8ed28-125">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ed28-126">계약 내용이 없는 경우 초기화 중에 **계약** 페이지의 **계약 성능** 탭이 자동으로 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed28-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>