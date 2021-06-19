---
title: Project Service Automation 업데이트 릴리스 32, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 32, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129674"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="cfd88-103">Project Service Automation 업데이트 릴리스 32, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="cfd88-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cfd88-104">Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="cfd88-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cfd88-106">Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cfd88-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="cfd88-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="cfd88-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cfd88-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cfd88-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 32에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="cfd88-110">이 버전의 빌드 번호는 V3.10.53.108이며 일반적으로 2021년 6월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="cfd88-111">업데이트 릴리스 32</span><span class="sxs-lookup"><span data-stu-id="cfd88-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cfd88-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="cfd88-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="cfd88-113">일반</span><span class="sxs-lookup"><span data-stu-id="cfd88-113">General</span></span>

- <span data-ttu-id="cfd88-114">주요 업그레이드가 실패하면 공유 엔터티에 계속 액세스할 수 있도록 기본 응용 프로그램 진입점만 차단해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="cfd88-115">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="cfd88-115">Time and Expense</span></span>

<span data-ttu-id="cfd88-116">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfd88-117">**TimeEntriesImportFromResourceAssignment** 는 리소스 할당 등고선 슬라이스의 시작 및 종료 시간을 유지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="cfd88-118">**시간 항목** 에서 **항목 열기** 를 선택하면 다른 양식을 선택하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="cfd88-119">시간 항목에 할당을 가져오는 동안 클라이언트 코드 쿼리는 쿼리에 실패하는 긴 URL을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="cfd88-120">**시간 항목** 그리드에서 값이 셀에서 삭제된 후 포커스가 그리드에 남아 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="cfd88-121">최신 승인의 경우 **승인 처리 중** 보기에서 **거부** 버튼이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="cfd88-122">시간 항목 대량 승인의 안정성과 성능은 교착 상태 및 **시간 항목** 엔터티와 관련된 사용자 지정을 적절하게 처리하지 못하는 경우 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="cfd88-123">프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="cfd88-123">Project Planning</span></span>

- <span data-ttu-id="cfd88-124">**계약 단위** 필드에 null 값이 있는 프로젝트를 업데이트하면 null 참조 예외가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="cfd88-125">**프로젝트 합계 새로 고침** 이 프로젝트의 남은 비용과 남은 매출을 잘못 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="cfd88-126">중복 가격 계산은 리소스 할당 윤곽의 업데이트와 관련된 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="cfd88-127">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="cfd88-127">Resource Management</span></span>

<span data-ttu-id="cfd88-128">다음 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="cfd88-129">예약 가능한 리소스의 달력 용량이 1보다 크면 Project Service Automation에서 용량을 0(영)으로 잘못 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="cfd88-130">따라서 일정 보기에서 무한 루프가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="cfd88-131">판매</span><span class="sxs-lookup"><span data-stu-id="cfd88-131">Sales</span></span>

<span data-ttu-id="cfd88-132">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="cfd88-133">사용자 지정 트랜잭션 유형이 있는 분개장 항목이 생성되면 다음과 같은 null 참조 예외가 발생합니다.*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="cfd88-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="cfd88-134">견적을 복사하기 전에 비활성화된 역할 및 범주는 새로 복사된 견적의 청구 가능한 역할 및 범주에 추가하면 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="cfd88-135">증빙 날짜 및 회계 날짜가 초안 송장에 직접 생성된 송장 라인 세부 정보에 제공된 시작 날짜와 일치하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="cfd88-136">견적을 복사하기 전에 역할 및 범주 비활성화와 관련된 시나리오에서 Null 참조 예외가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="cfd88-137">**프로젝트** 페이지의 **가격 업데이트** 작업이 비용 견적 및 재료 견적을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfd88-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
