---
title: Project Service Automation 업데이트 릴리스 14, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 14 V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080010"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="c1405-103">Project Service Automation 업데이트 릴리스 14, V3</span><span class="sxs-lookup"><span data-stu-id="c1405-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="c1405-104">Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="c1405-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c1405-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c1405-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="c1405-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="c1405-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1405-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c1405-109">이 항목에는 PSA V3, 업데이트 릴리스 14에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="c1405-110">이 버전의 빌드 번호는 V3.10.4.21이며 다음 일정으로 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="c1405-111">**일반 가용성(자체 업데이트):** 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="c1405-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="c1405-112">**자동 업데이트:** 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="c1405-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="c1405-113">업데이트 릴리스 14</span><span class="sxs-lookup"><span data-stu-id="c1405-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="c1405-114">향상된 기능</span><span class="sxs-lookup"><span data-stu-id="c1405-114">Enhancements</span></span>

- <span data-ttu-id="c1405-115">Sales</span><span class="sxs-lookup"><span data-stu-id="c1405-115">Sales</span></span>

     - <span data-ttu-id="c1405-116">견적이 **성공으로 종료** 로 업데이트될 때 **견적 라인 세부 정보** 의 사용자 지정 필드 값이 **프로젝트 계약 내용 세부 정보** 에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="c1405-117">확인된 프로젝트가 **실패로 종료** 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="c1405-118">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="c1405-118">Resource Management</span></span>

     - <span data-ttu-id="c1405-119">예약을 확장하면 예약 결과를 요약하고 예약 유지 링크를 제공하는 확인 대화 상자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="c1405-120">버그 수정</span><span class="sxs-lookup"><span data-stu-id="c1405-120">Bug fixes</span></span>

- <span data-ttu-id="c1405-121">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="c1405-121">Time and Expense</span></span>

     - <span data-ttu-id="c1405-122">수정: 사용자가 수정할 항목을 선택하지 않은 경우 사용자 환경이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="c1405-123">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="c1405-123">Resource Management</span></span>

     - <span data-ttu-id="c1405-124">수정: 리소스를 여러 번 예약하면 예약 가능한 리소스 이름이 오버플로됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="c1405-125">Sales</span><span class="sxs-lookup"><span data-stu-id="c1405-125">Sales</span></span>

     - <span data-ttu-id="c1405-126">수정: 사용자가 프로젝트의 비용 견적에 대한 비용 가격을 입력할 때까지 총 판매 가격이 계산되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="c1405-127">수정: 관련 프로젝트 계약이 **초안** 상태가 아닌 경우 견적을 **성공** 으로 종료하는 것에 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="c1405-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

