---
title: Project Service Automation 업데이트 릴리스 30, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 30, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010434"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="239eb-103">Project Service Automation 업데이트 릴리스 30, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="239eb-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="239eb-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="239eb-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="239eb-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="239eb-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="239eb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="239eb-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="239eb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="239eb-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 30에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="239eb-110">이 버전의 빌드 번호는 V3.10.51.61이며 일반적으로 2021년 4월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="239eb-111">업데이트 릴리스 30</span><span class="sxs-lookup"><span data-stu-id="239eb-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="239eb-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="239eb-112">Bug fixes</span></span>

<span data-ttu-id="239eb-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="239eb-113">**Time and Expense**</span></span>

<span data-ttu-id="239eb-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="239eb-115">**역할** 필드가 제거된 경우 **빨리 만들기** 페이지에서 시간 항목을 만들고 저장할 때 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="239eb-116">시간 입력 필터가 잘못된 필터 연산자를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="239eb-117">복사된 작업표는 시간 입력 제어에서 **주 복사** 선택시 자동으로 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="239eb-118">**리소스 관리**</span><span class="sxs-lookup"><span data-stu-id="239eb-118">**Resource Management**</span></span>

<span data-ttu-id="239eb-119">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="239eb-120">예약을 연장할 때 하드 예약에 지정된 예약 상태가 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="239eb-121">예약 연장은 예약 설정 메타데이터에서 **커밋** 으로 정의된 예약 상태를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="239eb-122">유효한 예약 상태가 지정되지 않은 경우 오류 메시지가 올바르게 현지화되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="239eb-123">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="239eb-123">**Project Management**</span></span>

<span data-ttu-id="239eb-124">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="239eb-125">프로젝트는 하나의 통화로 만들 수 없으며 관련 작업을 다른 통화로 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="239eb-126">**판매**</span><span class="sxs-lookup"><span data-stu-id="239eb-126">**Sales**</span></span>

<span data-ttu-id="239eb-127">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="239eb-128">가격표를 복사하면 가격이 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="239eb-129">원가 세부 정보에 원산지 값이 있으면 견적을 성공으로 마감할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="239eb-130">**프로젝트 작업** 엔터티에서 **추정 비용** 이름이 **계획 비용(기본)** 으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="239eb-131">송장이 생성되거나 삭제될 때 null 참조 예외가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="239eb-131">A null reference exception is generated when invoices are created or deleted.</span></span>
