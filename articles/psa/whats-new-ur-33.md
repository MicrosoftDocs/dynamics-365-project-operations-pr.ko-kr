---
title: Project Service Automation 업데이트 릴리스 33, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 33, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334566"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="85962-103">Project Service Automation 업데이트 릴리스 33, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="85962-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="85962-104">Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="85962-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="85962-106">Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="85962-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="85962-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="85962-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="85962-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="85962-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 33에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="85962-110">이 버전의 빌드 번호는 V3.10.54.98이며 일반적으로 2021년 7월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="85962-111">업데이트 릴리스 33</span><span class="sxs-lookup"><span data-stu-id="85962-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="85962-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="85962-112">Bug fixes</span></span>

<span data-ttu-id="85962-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="85962-113">**Time and Expense**</span></span>

<span data-ttu-id="85962-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="85962-115">두 개의 잠긴 필드, **msdyn_description** 과 **msdyn_externaldescription** 은 제출 후 수정 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="85962-116">프로젝트와 관련이 없는 경비가 생성되면 오류 메시지가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="85962-117">시간 항목이 생성되면 리소스 역할은 기본적으로 비활성 역할로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="85962-118">회수 및 삭제된 경비와 연결된 분개장 항목은 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="85962-119">**시간 항목 빨리 만들기 양식** 에서 **프로젝트 작업 목록** 보기를 업데이트하여 기본적으로 표시되는 날짜를 작업 시작 날짜로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="85962-120">예약 가능한 리소스의 **관련 항목** 탭에서 시간 항목을 만들 때 상위 예약 가능한 리소스 대신 로그인한 사용자에 대해 시간 항목이 잘못 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="85962-121">**일괄 승인 MDD** 대화 상자에 새로운 필드가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="85962-122">**프로젝트 계획**</span><span class="sxs-lookup"><span data-stu-id="85962-122">**Project planning**</span></span>

<span data-ttu-id="85962-123">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="85962-124">복잡한 달력과 함께 프로젝트 작업 시간 템플릿을 적용하면 프로젝트 생성 성능이 느려집니다.</span><span class="sxs-lookup"><span data-stu-id="85962-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="85962-125">시작 날짜가 종료 날짜보다 큰 경우 각 필드의 시간 구성 요소가 다르기 때문에 복사 프로젝트 템플릿에 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="85962-126">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="85962-126">**Resource management**</span></span>

<span data-ttu-id="85962-127">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="85962-128">리소스 활용 쿼리에 잘못된 매개변수가 사용되어 **리소스 활용** 그리드에 XML이 잘못된 필터 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85962-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="85962-129">**예약 연장** 확인에 잘못된 예약 종료 날짜가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85962-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="85962-130">**판매**</span><span class="sxs-lookup"><span data-stu-id="85962-130">**Sales**</span></span>

<span data-ttu-id="85962-131">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="85962-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="85962-132">누락된 값으로 범주 가격을 생성하면 오류 메시지가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="85962-133">주문 라인 없이 계약 내용 중요 시점이 생성되면 오류 메시지가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="85962-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
