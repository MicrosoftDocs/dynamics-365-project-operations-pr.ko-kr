---
title: Project Service Automation 업데이트 릴리스 23, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 23, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006474"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="ea403-103">Project Service Automation 업데이트 릴리스 23, V3</span><span class="sxs-lookup"><span data-stu-id="ea403-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ea403-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ea403-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ea403-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ea403-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="ea403-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ea403-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea403-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ea403-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 23에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="ea403-110">이 버전의 빌드 번호는 V 3.10.34.30이며 2020년 8월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="ea403-111">업데이트 릴리스 23</span><span class="sxs-lookup"><span data-stu-id="ea403-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ea403-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="ea403-112">Bug fixes</span></span>

<span data-ttu-id="ea403-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="ea403-113">**Time and Expense**</span></span>

<span data-ttu-id="ea403-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="ea403-115">**프로젝트 팀 구성원 삭제** 에서 가장자리 케이스를 처리하여 의미 있는 예외를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="ea403-116">할당 가져오기를 수행하면 빈 제거 화면이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="ea403-117">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="ea403-117">**Resource Management**</span></span>

<span data-ttu-id="ea403-118">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="ea403-119">**리소스 활용 그리드 리소스 카드** 는 시간 척도가 5일 이상인 경우 잘못된 데이터를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="ea403-120">고객이 예약 가능한 리소스를 만들 때 플러그인이 간헐적으로 리소스를 Microsoft Office 365 그룹에 자동으로 추가하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="ea403-121">**조정** 보기의 **주** 또는 **달** 보기에 수동 윤곽이 잘못 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="ea403-122">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="ea403-122">**Project Management**</span></span>

<span data-ttu-id="ea403-123">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="ea403-124">과도한 수의 **사용자 설정에 대한 RetrieveMultiple** 엔터티는 프로젝트 승인 및 기타 작업에 대한 성능 저하를 유발합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="ea403-125">**작업 계획** 그리드 리소스 조회는 프로젝트 팀에서 최대 5명의 팀 구성원만 표시하도록 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="ea403-126">**작업 계획** 그리드 리소스 조회는 비활성 리소스를 필터링하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="ea403-127">프로젝트 계획 작업 분할 구조에서 수동 모드가 예상대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="ea403-128">**작업 계획** 그리드는 **비활성 트랜잭션 범주** 를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="ea403-129">**리소스 할당** 그리드는 작업에 여러 할당이 있는 경우 잘못 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="ea403-130">반올림 값은 단일 작업의 계획 비용과 실제 비용 간에 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="ea403-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ea403-131">**Sales**</span></span>

<span data-ttu-id="ea403-132">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="ea403-133">**모든 트랜잭션 범주 가져 오기** 를 두 번 클릭하면 여러 줄이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea403-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]