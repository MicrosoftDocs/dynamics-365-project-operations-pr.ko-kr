---
title: Project Service Automation 업데이트 릴리스 21, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 21, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002335"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="acfdd-103">Project Service Automation 업데이트 릴리스 21, V3</span><span class="sxs-lookup"><span data-stu-id="acfdd-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="acfdd-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="acfdd-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="acfdd-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="acfdd-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="acfdd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="acfdd-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="acfdd-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="acfdd-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 21에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="acfdd-110">이 버전의 빌드 번호는 V 3.10.32.50이며 일반적으로 2020년 6월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="acfdd-111">업데이트 릴리스 21</span><span class="sxs-lookup"><span data-stu-id="acfdd-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="acfdd-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="acfdd-112">Bug fixes</span></span>

<span data-ttu-id="acfdd-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="acfdd-113">**Time and Expense**</span></span>

<span data-ttu-id="acfdd-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="acfdd-115">대시보드에서 **시간 항목 그리드 제어** 를 호스팅할 때 그리드는 대시보드 그리드 컨테이너의 전체 너비를 활용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="acfdd-116">특정 시간대의 경우 **시간 항목** 그리드 컨트롤은 레코드를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="acfdd-117">오후 9시 이후의 시간 항목은 잘못된 날짜에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="acfdd-118">비용 범주, **경비 영수증 필요** 에 값이 없는 경우 사용자는 경비를 제출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="acfdd-119">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="acfdd-119">**Resource Management**</span></span>

<span data-ttu-id="acfdd-120">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="acfdd-121">비활성 예약이 **조정** 보기에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="acfdd-122">일반 리소스 이행에 유효한 예약 상태가 있는지 확인하는 유효성 검사가 누락되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="acfdd-123">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="acfdd-123">**Project Management**</span></span>

<span data-ttu-id="acfdd-124">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="acfdd-125">**프로젝트** 양식 그리드(**리소스 할당**, **작업**, **조정** 보기, **경비 추정**)은 프로젝트가 활성이 아닐 때도 편집 가능한 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="acfdd-126">중복 고객은 확인된 프로젝트 계약에 연결된 고객과 병합할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="acfdd-127">유효한 달력이 없는 리소스가 추가되면 시스템은 사용자에게 친숙한 오류 메시지를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="acfdd-128">프로젝트가 **Microsoft Project 추가 기능** 에 연결되면 작업 그리드의 **작업 추가** 버튼이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="acfdd-129">범주가 있는 작업이 비용 가격이 정의된 역할을 가진 리소스에 할당되면 노력이 통제할 수 없게 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="acfdd-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="acfdd-130">**Sales**</span></span>

<span data-ttu-id="acfdd-131">다음과 같은 기능이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="acfdd-132">**송장 빈도** 및 **청구 시작** 이 **송장 일정** 탭으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="acfdd-133">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="acfdd-134">**역할** 이 0이 아닌 총 판매 가격을 갖더라도 **범주** 에 대한 **총 판매 가격** 이 영(0)입니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="acfdd-135">고객은 다른 사용자 지정 프로세스가 추가 필드를 업데이트할 때 **송장 상태** 필드의 값을 **송장 발부 준비 완료** 로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="acfdd-136">**송장 라인 새로 고침** 버튼을 반복적으로 선택하면 여러 개의 중복된 라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="acfdd-137">**빠른 보기** 양식의 **역할 가격** 하위 그리드에서 **가격 업데이트** 단추가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="acfdd-138">**판매 가격 목록 해결** 논리가 시간대를 부적절하게 처리하여 가격 목록을 잘못 선택하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="acfdd-139">프로젝트의 **총 실제 비용** 은 한 번의 입력이 승인된 후 소수의 금액으로 해제될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="acfdd-140">**가격 해결** 논리는 **검색된 역할 가격** 에서 **'기본 단위'** 및 **'기본 단위의 가격'** 필드에 값이 없는 경우 사용자에게 친숙한 오류 메시지를 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acfdd-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]