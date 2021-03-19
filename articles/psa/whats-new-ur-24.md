---
title: Project Service Automation 업데이트 릴리스 24, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 24, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280496"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="6c71b-103">Project Service Automation 업데이트 릴리스 24, V3</span><span class="sxs-lookup"><span data-stu-id="6c71b-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6c71b-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6c71b-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6c71b-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6c71b-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="6c71b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6c71b-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6c71b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6c71b-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 24에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="6c71b-110">이 버전의 빌드 번호는 V 3.10.42.43이며 2020년 10월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="6c71b-111">업데이트 릴리스 24</span><span class="sxs-lookup"><span data-stu-id="6c71b-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6c71b-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="6c71b-112">Bug fixes</span></span>

<span data-ttu-id="6c71b-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6c71b-113">**Sales**</span></span>

<span data-ttu-id="6c71b-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c71b-115">제품의 기본 가격 목록을 설정하는 동안 문제가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="6c71b-116">포함된 가격표 및 역할 가격 레코드 사본으로 인해 견적 받기의 성능이 느립니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="6c71b-117">**프로젝트 계약/판매 허브** > **제품 라인 항목/주문 라인 수량** 은 가장 가까운 정수로 자동 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="6c71b-118">가격표를 읽을 때 시스템 권한으로 승격하십시오.</span><span class="sxs-lookup"><span data-stu-id="6c71b-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="6c71b-119">고객 주소 필드 **address1_freighttermscode** 및 **address1_shippingmethodcode** 를 견적/주문으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="6c71b-120">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="6c71b-120">**Time and Expense**</span></span>

<span data-ttu-id="6c71b-121">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c71b-122">**시간 항목 그리드** 는 **날짜만** 시간 동작을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="6c71b-123">**시간 항목** 은 자동으로 새로 고침되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="6c71b-124">수동 새로 고침이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-124">A manual refresh is required.</span></span>
- <span data-ttu-id="6c71b-125">리소스 할당에 휴식(0 시간)이 있는 경우 할당에서 시간 항목을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="6c71b-126">시간 항목을 만들 때 시작을 **msdyn_date** 와 동일하게 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="6c71b-127">시간 항목에 대한 대량 편집을 다시 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="6c71b-128">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="6c71b-128">**Resource Management**</span></span>

<span data-ttu-id="6c71b-129">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c71b-130">요구 사항 없이 당일 예약 상태를 업데이트하려고 하면 null-ref 예외가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="6c71b-131">**조정 보기** 로드 중 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="6c71b-132">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="6c71b-132">**Project Management**</span></span>

<span data-ttu-id="6c71b-133">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c71b-134">**프로젝트 일정** 에서 **수동** 에서 **자동** 으로 변경하면 자동 저장이 완료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="6c71b-135">경비 비용은 **프로젝트 추적 그리드** 의 차이로 계산해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="6c71b-136">로드 중 **추정 태그** 열의 일관되지 않은 동작과 **시간 위상** 유형 변경을 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="6c71b-137">프로젝트의 실제 비용은 **실제** 의 총액을 반영하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="6c71b-138">**요약** 탭의 **예상 완료 날짜** 가 **WBS 일정** 과 일치하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="6c71b-139">내어쓰기의 **실제 시간 업데이트** 가 제대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="6c71b-140">루트 **BU** 외부의 프로젝트 관리자가 프로젝트를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="6c71b-141">**경비 추정** 의 작업 또는 범주 변경이 지속되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="6c71b-142">**계약 사본** 이 송장 일정 및 실행 상태를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="6c71b-143">**실적 새로 고침** 단추가 요약 작업을 잘못 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="6c71b-144">Microsoft Project 추가 기능: 팀 구성원이 빈 리소스 단위를 가진 경우 null 참조 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c71b-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]