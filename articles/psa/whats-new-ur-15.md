---
title: Project Service Automation 업데이트 릴리스 15, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 15, V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 189b99c6a4bf18b6063c7b6020dbf1ac372b41e9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280946"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="13e17-103">Project Service Automation 업데이트 릴리스 15, V3</span><span class="sxs-lookup"><span data-stu-id="13e17-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13e17-104">Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="13e17-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="13e17-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13e17-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="13e17-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="13e17-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13e17-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="13e17-109">이 항목에는 PSA V3, 업데이트 릴리스 15에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="13e17-110">이 버전의 빌드 번호는 V3.10.5.28이며 2020년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="13e17-111">업데이트 릴리스 15</span><span class="sxs-lookup"><span data-stu-id="13e17-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="13e17-112">향상된 기능</span><span class="sxs-lookup"><span data-stu-id="13e17-112">Enhancements</span></span>

- <span data-ttu-id="13e17-113">프로젝트 관리</span><span class="sxs-lookup"><span data-stu-id="13e17-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13e17-114">버그 수정</span><span class="sxs-lookup"><span data-stu-id="13e17-114">Bug fixes</span></span>

- <span data-ttu-id="13e17-115">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="13e17-115">Time and Expense</span></span>

  - <span data-ttu-id="13e17-116">수정: 조정 보기에서 부하 시 오류 처리 추가.</span><span class="sxs-lookup"><span data-stu-id="13e17-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="13e17-117">수정: 프로젝트 리소스 허브: 모호성을 줄이기 위해 **금액** 의 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="13e17-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="13e17-118">수정: **시간 항목 열 복사** 보기가 유형을 포함하도록 조정.</span><span class="sxs-lookup"><span data-stu-id="13e17-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="13e17-119">수정: 십진수를 사용하여 표 보기에서 시간 입력 기간을 편집하면 일부 숫자에 알 수 없는 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="13e17-120">프로젝트 관리</span><span class="sxs-lookup"><span data-stu-id="13e17-120">Project Management</span></span>

  - <span data-ttu-id="13e17-121">수정: **추적 보기에서 사용** 드롭다운 메뉴 옵션이 이제 너비에 따라 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="13e17-122">수정: +13 시간대에서 프로젝트를 관리할 때 작업 계산에 부정확한 결과가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="13e17-123">수정: 24시간 달력을 사용할 때 **팀 멤버 종료 시간** 이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="13e17-124">수정: **msdyn_project** 기본 양식의 **BPF** 재활성화.</span><span class="sxs-lookup"><span data-stu-id="13e17-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="13e17-125">수정: 할당 계산이 더 이상 하루를 무시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="13e17-126">수정: 사용자와 프로젝트의 시간대가 다른 경우 새로운 알림 배너가 프로젝트 양식에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="13e17-127">Sales</span><span class="sxs-lookup"><span data-stu-id="13e17-127">Sales</span></span>

  - <span data-ttu-id="13e17-128">수정: 비용 추정 범주 검색을 사용하여 중복 항목을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="13e17-129">수정: **PluginDomain.ExecuteInTryCatchBlock(..)** 의 코드가 더 이상 예외의 출처를 숨기지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="13e17-130">수정: 1000개가 넘는 프로젝트가 있을 때 **견적 라인** 양식의 **프로젝트 조회** 에 더 이상 오류 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="13e17-131">수정: 노동 추정 및 비용 추정에 대한 **추정** 표가 이제 올바른 통화 기호를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="13e17-132">수정: 조직이 업데이트 릴리스 14에서 업데이트 릴리스 15로 PSA를 업데이트하면 더 이상 **프로젝트** 양식에 **일정** 탭이 공백으로 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e17-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]