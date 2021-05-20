---
title: Project Service Automation 업데이트 릴리스 13, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 13, V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949462"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="d8138-103">Project Service Automation 업데이트 릴리스 13, V3</span><span class="sxs-lookup"><span data-stu-id="d8138-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d8138-104">Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d8138-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d8138-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d8138-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="d8138-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d8138-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8138-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d8138-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 13에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d8138-110">이 버전의 빌드 번호는 V3.10.3.18이며 다음 일정으로 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d8138-111">**일반 가용성(자체 업데이트):** 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="d8138-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d8138-112">**자동 업데이트:** 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="d8138-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d8138-113">업데이트 릴리스 13</span><span class="sxs-lookup"><span data-stu-id="d8138-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d8138-114">버그 수정</span><span class="sxs-lookup"><span data-stu-id="d8138-114">Bug fixes</span></span>

- <span data-ttu-id="d8138-115">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="d8138-115">Time and Expense</span></span>

     - <span data-ttu-id="d8138-116">수정: 비용 목적으로 검색할 때 **비용 승인** 페이지의 검색 기능이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d8138-117">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="d8138-117">Resource Management</span></span>

     - <span data-ttu-id="d8138-118">수정: 조정의 숫자가 올바르게 정렬되도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d8138-119">수정: 명명된 리소스를 **일정** 탭을 통해 작업에 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d8138-120">프로젝트 관리</span><span class="sxs-lookup"><span data-stu-id="d8138-120">Project Management</span></span>

     - <span data-ttu-id="d8138-121">수정: 팀 구성원을 할당할 때 **TransactionType** 에 **단위** 및 **기본 그룹** 에 대한 설정 정보가 누락된 경우 Null 참조 예외.</span><span class="sxs-lookup"><span data-stu-id="d8138-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d8138-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d8138-122">Sales</span></span>

     - <span data-ttu-id="d8138-123">수정: 역할 가격 레코드가 작성되면 중복 거래 유형 레코드가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d8138-124">수정: **새 영업 기회**, **견적**, **주문 라인** 및 **제품 추가** 를 위한 추가 단추는 영업 기회, 견적, 제품 주문 및 프로젝트 기반 라인 하위 그리드에 대한 명령에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8138-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]