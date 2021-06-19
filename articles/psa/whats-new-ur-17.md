---
title: Project Service Automation 업데이트 릴리스 17, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 17, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006699"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="f639a-103">Project Service Automation 업데이트 릴리스 17, V3</span><span class="sxs-lookup"><span data-stu-id="f639a-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f639a-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f639a-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="f639a-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f639a-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="f639a-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="f639a-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f639a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f639a-109">이 항목에는 PSA V3, 업데이트 릴리스 17에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="f639a-110">이 버전의 빌드 번호는 V3.10.6.34이며 2020년 3월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="f639a-111">업데이트 릴리스 17</span><span class="sxs-lookup"><span data-stu-id="f639a-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f639a-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="f639a-112">Bug fixes</span></span>

<span data-ttu-id="f639a-113">**일반**</span><span class="sxs-lookup"><span data-stu-id="f639a-113">**General**</span></span>

- <span data-ttu-id="f639a-114">해결: Team Member 라이선스를 시행하도록 Project Service Automation를 업데이트합니다(프로젝트 리소스 허브에는 팀 구성원 서비스 계획 메타데이터 3.x가 포함됨).</span><span class="sxs-lookup"><span data-stu-id="f639a-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="f639a-115">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="f639a-115">**Time and Expense**</span></span>

- <span data-ttu-id="f639a-116">해결: 경비 견적을 0이 아닌 가격에서 0으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="f639a-117">변경은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-117">The change is ignored.</span></span>

<span data-ttu-id="f639a-118">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="f639a-118">**Project Management**</span></span>

- <span data-ttu-id="f639a-119">해결: 팀 구성원의 직위 이름에 null 값 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="f639a-120">해결: **msdyn_resourceassignment** 엔터티의 **msdyn_userresourceid** 필드는 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="f639a-121">해결: 2.x에서 3.x로 업그레이드하면 작업 할당에서 빈 작업량 등고선을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="f639a-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f639a-122">**Sales**</span></span>

- <span data-ttu-id="f639a-123">해결: **Invoice.PreValidateInvoiceUpdate** 는 이제 레코드 소유자를 올바르게 재할당하는 시나리오를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="f639a-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="f639a-124">해결: 트랜잭션 클래스가 **시간** 이면 **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** 및 **ContractLineDetails** 를 포함하여 모든 엔터티에 대해 **UnitGroup** 을 편집할 수 없습니다..</span><span class="sxs-lookup"><span data-stu-id="f639a-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="f639a-125">그러나 **단위** 는 **JournalLine** 과 **InvoiceLineDetails** 의 경우에만 편집할 수 없습니다 .</span><span class="sxs-lookup"><span data-stu-id="f639a-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]