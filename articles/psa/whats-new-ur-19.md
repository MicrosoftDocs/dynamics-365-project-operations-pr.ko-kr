---
title: Project Service Automation 업데이트 릴리스 19, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 19, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080005"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="fa41c-103">Project Service Automation 업데이트 릴리스 19, V3</span><span class="sxs-lookup"><span data-stu-id="fa41c-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="fa41c-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fa41c-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fa41c-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fa41c-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="fa41c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fa41c-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa41c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fa41c-109">이 항목에는 PSA V3, 업데이트 릴리스 19에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="fa41c-110">이 버전의 빌드 번호는 V3.10.30.41이며 일반적으로 2020년 5월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="fa41c-111">업데이트 릴리스 19</span><span class="sxs-lookup"><span data-stu-id="fa41c-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fa41c-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="fa41c-112">Bug fixes</span></span>

<span data-ttu-id="fa41c-113">**시간 및 경비**</span><span class="sxs-lookup"><span data-stu-id="fa41c-113">**Time and Expense**</span></span>

<span data-ttu-id="fa41c-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="fa41c-115">시간 항목 가져 오기에서 파생된 오류가 올바르게 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="fa41c-116">시간 입력 그리드는 **날짜만** 필드 동작을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="fa41c-117">프로젝트 리소스가 프로젝트 비용을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="fa41c-118">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="fa41c-118">**Project Management**</span></span>

<span data-ttu-id="fa41c-119">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="fa41c-120">최하위 작업은 완료(EAC) 계산 중에 잘못된 노력 추정치를 유발합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="fa41c-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fa41c-121">**Sales**</span></span>

<span data-ttu-id="fa41c-122">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="fa41c-123">**다시 계산** 작업은 비용 계약 내용 세부 사항 또는 견적 라인 세부 사항과 함께 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="fa41c-124">**가격 업데이트** 에 비용 추정치가 누락되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="fa41c-125">고객이 **프로젝트 계약** 페이지에서 사용자 지정 계약 상태 설명을 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="fa41c-126">고객은 견적에서 사용자 정의 가격표를 작성할 때 성능 저하를 경험합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="fa41c-127">고객이 **견적 라인 세부 사항** 및 **계약 내용 세부 사항** 페이지에서 **단위** 기본값의 불일치를 경험합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="fa41c-128">청구 불가능한 거래 범주 항목을 청구 가능 계약 내용에 추가하면 거래 범주의 **청구 불가능한** 청구 유형이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="fa41c-129">고객은 이전에 생성된 계약에서 새로 추가된 역할 및 범주를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="fa41c-130">고객이 PreValidateProjectTeamMemberUpdate.cs의 불필요한 검색에서 성능 저하를 경험합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="fa41c-131">**리소스 범주** 목록에서 청구 불가능으로 설정된 역할은 프로젝트의 계약 내용에서 **청구 가능한 역할** 탭에 **청구 불가능** 으로 추가되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="fa41c-132">**GetBookableResourceIdFromUser** 는 기본 ID 대신 예약 가능한 리소스의 모든 열을 검색하기 때문에 프로젝트를 만들 때 고객이 성능 저하를 경험할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="fa41c-133">**TransactionType** 엔터티에 사용자가 트랜잭션 유형에 유효하지 않은 **단위** 및 **단위 그룹** 을 입력하지 못하도록 사전 유효성 검사 업데이트 플러그인이 누락되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="fa41c-134">시간 항목 가져오기에 **제거** 단계가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa41c-134">The **Remove** step does not work for time entry import.</span></span>
