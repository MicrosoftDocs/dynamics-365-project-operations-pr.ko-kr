---
title: Project Service Automation 업데이트 릴리스 26, V3의 새로운 기능 또는 변경된 기능
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643271"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="1be21-102">Project Service Automation 업데이트 릴리스 26, V3</span><span class="sxs-lookup"><span data-stu-id="1be21-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="1be21-103">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1be21-104">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1be21-105">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1be21-106">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="1be21-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1be21-107">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1be21-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1be21-108">이 항목에는 Project Service Automation 업데이트 릴리스 26, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="1be21-109">이 버전의 빌드 번호는 V3.10.44.59이며 일반적으로 2020년 12월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="1be21-110">업데이트 릴리스 26</span><span class="sxs-lookup"><span data-stu-id="1be21-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="1be21-111">버그 수정</span><span class="sxs-lookup"><span data-stu-id="1be21-111">Bug fixes</span></span>

<span data-ttu-id="1be21-112">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="1be21-112">**Time and Expense**</span></span>

<span data-ttu-id="1be21-113">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="1be21-114">사용자는 승인/제출된 시간 항목에서 작업을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="1be21-115">시간 입력을 저장할 때 "개체 참조가 설정되지 않음" 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="1be21-116">리소스 할당에서 시간 항목을 가져 오면 DateTime 값으로 잘못된 시간 항목이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="1be21-117">Project Service Automation 및 Field Service 앱이 모두 설치되면 Field Service 앱의 시간 항목에 대한 **새로 만들기** 단추가 명령 모음에 두 번 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="1be21-118">**허용 단위** 및 **단위 그룹** 셀 업데이트가 이제 **경비 추정** 그리드에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="1be21-119">**업데이트 시간 항목 편집** 양식에는 **타임라인** 이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="1be21-120">비 프로젝트 시간 항목에 대한 시간 승인은 프로젝트 승인자 역할을 검색할 때 시스템을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="1be21-121">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="1be21-121">**Resource Management**</span></span>

<span data-ttu-id="1be21-122">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="1be21-123">**PostProjectCreate** 플러그인에 생성하기 전에 기본 요구 사항을 확인하는 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="1be21-124">**프로젝트 팀 구성원** 빨리 만들기 양식은 양식에서 필드가 제거되는 경우 널 참조 예외가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="1be21-125">1년 동안 12시간에 대한 요구 사항 생성은 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="1be21-126">리소스 요구 사항 생성 중 오류 메시지 null 참조 예외가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="1be21-127">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="1be21-127">**Project Management**</span></span>

<span data-ttu-id="1be21-128">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="1be21-129">**PreProjectUpdate** 플러그인에서 생성된 null 참조 예외를 해결하기 위해 유효성 검사가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="1be21-130">Microsoft Project 데스크톱 추가 기능에서 게시한 프로젝트는 할당되지 않은 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="1be21-131">**PreValidateProjectTaskUpdate** 플러그인에서 Null 참조 예외로 인해 작업의 프로젝트 참조가 유효하지 않은 경우 새 유효성 검사를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="1be21-132">팀 구성원 그리드는 팀 구성원 레코드에 고유한 할당을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="1be21-133">**PreProjectTaskDelete** 플러그인에서 Null 참조 예외로 인한 새 유효성 검사 및 오류 메시지를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="1be21-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1be21-134">**Sales**</span></span>

<span data-ttu-id="1be21-135">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="1be21-136">견적 또는 계약에서 프로젝트 기반 라인을 선택할 때 **제안** 단추는 기존 제품과 연관된 제품 기반 라인을 선택할 때만 표시되어야합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="1be21-137">**Create_Product** 권한을 **Create_ProjectContract** 권한에서 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="1be21-138">송장 라인을 삭제하면 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 에서 Null 참조 실패가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1be21-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>