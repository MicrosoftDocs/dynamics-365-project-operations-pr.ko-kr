---
title: Project Service Automation 업데이트 릴리스 31, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 31, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999139"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="bd742-103">Project Service Automation 업데이트 릴리스 31, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="bd742-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bd742-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bd742-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bd742-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bd742-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd742-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bd742-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd742-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bd742-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 31에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="bd742-110">이 버전의 빌드 번호는 V3.10.52.77이며 일반적으로 2021년 5월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="bd742-111">업데이트 릴리스 31</span><span class="sxs-lookup"><span data-stu-id="bd742-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bd742-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="bd742-112">Bug fixes</span></span>

<span data-ttu-id="bd742-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="bd742-113">**Time and Expense**</span></span>

<span data-ttu-id="bd742-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd742-115">**예약 가능한 리소스** 페이지의 시간 입력 제어 명령 버튼이 혼란스러웠습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="bd742-116">시간 입력을 승인할 때 **Project.SetTrackingFields** 에서 null 참조 예외가 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="bd742-117">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="bd742-117">**Resource Management**</span></span>

<span data-ttu-id="bd742-118">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd742-119">**팀 구성원 만들기** 가 **기본 예약 커밋 상태** 에 대한 예약 설정 메타데이터 설정을 올바르게 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="bd742-120">PSA 1.X에서 3.X로 업그레이드할 때 **UpgradeResourceRequirements** 에서 업그레이드 프로세스가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="bd742-121">**판매**</span><span class="sxs-lookup"><span data-stu-id="bd742-121">**Sales**</span></span>

<span data-ttu-id="bd742-122">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd742-123">실제 수익은 금액을 추적 그리드의 프로젝트 통화로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="bd742-124">조직의 기준 통화가 프로젝트 통화와 다른 시나리오에서 분개 라인, 견적 라인 및 계약 내용을 생성할 때 통화 기본값이 명확하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="bd742-125">**보류 중인 수정 분개장 유효성 검사** 쿼리는 프로젝트별로 필터링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="bd742-126">프로젝트에서 남은 판매가 잘못 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="bd742-127">연락처를 기반으로 한 견적은 가격 목록 없이 생성된 경우 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="bd742-128">**송장 확인** 을 선택할 때 처리 스피너가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="bd742-129">**송장 만들기** 를 선택할 때 처리 스피너가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="bd742-130">분실로 견적을 닫아도 예약이 취소되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd742-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







