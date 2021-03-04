---
title: Project Service Automation 업데이트 릴리스 18, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 18, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147211"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="a268b-103">Project Service Automation 업데이트 릴리스 18, V3</span><span class="sxs-lookup"><span data-stu-id="a268b-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a268b-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a268b-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a268b-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a268b-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="a268b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a268b-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a268b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a268b-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 18에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="a268b-110">이 버전의 빌드 번호는 V3.10.8.12이며 일반적으로 2020년 4월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="a268b-111">업데이트 릴리스 18</span><span class="sxs-lookup"><span data-stu-id="a268b-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a268b-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="a268b-112">Bug fixes</span></span>

<span data-ttu-id="a268b-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="a268b-113">**Time and Expense**</span></span>

- <span data-ttu-id="a268b-114">수정됨: **리콜**, **요청** 및 **승인 취소** 플로우에서 명확하지 않은 오류 메시지와 함께 예외가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="a268b-115">수정됨: 비용 때문에 **승인 취소** 가 실패하면 관련 예외 오류가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="a268b-116">수정됨: 10월 일광 절약 시간제(DST) 전환 후 호주의 시간 입력 그리드가 휴무일을 잘못 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="a268b-117">수정됨: 기본 논리가 잘못되면 경비 제출이 금지됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="a268b-118">수정됨: 시간 입력 승인에 실패하면 승인 상태가 **대기 중** 으로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="a268b-119">수정됨: 대량 승인시 SQL 오류(교착 상태/시간 초과).</span><span class="sxs-lookup"><span data-stu-id="a268b-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="a268b-120">수정됨: 시간 입력을 승인하는 동안 팀 구성원을 업데이트하여 발생하는 사용자 경험의 중요한 성능 문제.</span><span class="sxs-lookup"><span data-stu-id="a268b-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="a268b-121">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="a268b-121">**Project Management**</span></span>

- <span data-ttu-id="a268b-122">수정됨: 표준 시간대 알림이 **조정** 보기에서 **프로젝트** 기본 양식으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="a268b-123">수정됨: 새 프로젝트 양식을 열 때 일정 템플릿이 기본적으로 올바르게 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="a268b-124">수정됨: Chromium 기반 브라우저의 경우 사용자가 삭제할 선행 작업을 쉽게 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="a268b-125">수정됨: **빈 템플릿에서 프로젝트** 작성 또는 복사가 관련 없는 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="a268b-126">수정됨: 특정 에지의 경우 작업 그리드에서 새 할당을 생성하면 중복 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="a268b-127">수정됨: 수동 모드에서 사용자는 작업 시작 날짜를 현재 저장된 날짜보다 늦게 업데이트 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="a268b-128">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="a268b-128">**Resource Management**</span></span>

- <span data-ttu-id="a268b-129">수정됨: **조정** 보기 소계 행이 예약 연장 후 예약 차이를 잘못 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="a268b-130">수정됨: **조정** 보기가 예약 가능한 리소스에 프로젝트 일정과 일치하지 않는 일정이 있으면 리소스 할당을 잘못 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="a268b-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a268b-131">**Sales**</span></span>

- <span data-ttu-id="a268b-132">수정됨: 시간 항목이 다시 승인될 때( **승인 > 취소 >** 다시 승인), 청구 가능하지 않은 실제의 사본이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a268b-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
