---
title: Project Service Automation 업데이트 릴리스 28, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 28, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150631"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d154b-103">Project Service Automation 업데이트 릴리스 28, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="d154b-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d154b-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d154b-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d154b-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d154b-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="d154b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d154b-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d154b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d154b-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 28에 대해 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.이 버전에는 V3.10.46.32의 빌드 번호가 있으며 일반적으로 2021년 1월에 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d154b-110">업데이트 릴리스 28</span><span class="sxs-lookup"><span data-stu-id="d154b-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d154b-111">버그 수정</span><span class="sxs-lookup"><span data-stu-id="d154b-111">Bug fixes</span></span>

<span data-ttu-id="d154b-112">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="d154b-112">**Time and Expense**</span></span>

<span data-ttu-id="d154b-113">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d154b-114">사용자는 **대량 편집** 을 사용하여 승인 및 제출된 시간 항목을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d154b-115">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="d154b-115">**Project Management**</span></span>

<span data-ttu-id="d154b-116">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d154b-117">작업 GUID가 숫자로 해석되는 경우 **작업 분할 구조** 페이지의 리본에 있는 **작업 편집** 을 사용하여 편집할 작업을 열 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d154b-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d154b-118">**Sales**</span></span>

<span data-ttu-id="d154b-119">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d154b-120">**GetEstimatesForProject** 플러그인이 호출되면 null 참조 예외가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d154b-121">중요 시점 그리드의 **송장 발부 준비 완료로 표시** 는 업데이트된 **InvoiceStatus** 특성을 제외하고 특성을 부분적으로만 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d154b-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

