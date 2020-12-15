---
title: 보안 모델
description: 이 토픽은 Dynamics 365 Project Operations의 보안 모델에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642911"
---
# <a name="security-model"></a><span data-ttu-id="dd2c9-103">보안 모델</span><span class="sxs-lookup"><span data-stu-id="dd2c9-103">Security Model</span></span>

<span data-ttu-id="dd2c9-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="dd2c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dd2c9-105">Microsoft Dynamics 365 Project Operations는 Microsoft Office 그룹과 협업하는 역할 기반 비즈니스 보안 모델을 허용하는 고유한 보안 모델을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="dd2c9-106">보안 역할</span><span class="sxs-lookup"><span data-stu-id="dd2c9-106">Security roles</span></span>
<span data-ttu-id="dd2c9-107">Project Operations 프런트 엔드 기능에는 다음 역할이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="dd2c9-108">역할</span><span class="sxs-lookup"><span data-stu-id="dd2c9-108">Role</span></span>                          | <span data-ttu-id="dd2c9-109">설명</span><span class="sxs-lookup"><span data-stu-id="dd2c9-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="dd2c9-110">Scope</span><span class="sxs-lookup"><span data-stu-id="dd2c9-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="dd2c9-111">연습 관리자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-111">Practice manager</span></span>              | <span data-ttu-id="dd2c9-112">프로젝트 간 보고를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="dd2c9-113">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-113">Business unit</span></span>              |
| <span data-ttu-id="dd2c9-114">프로젝트 승인자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-114">Project approver</span></span>              | <span data-ttu-id="dd2c9-115">프로젝트에 대한 시간 및 경비를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="dd2c9-116">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-116">Business unit</span></span> |
| <span data-ttu-id="dd2c9-117">프로젝트 청구 관리자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-117">Project billing administrator</span></span> | <span data-ttu-id="dd2c9-118">송장 제안을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="dd2c9-119">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-119">Business unit</span></span> |
| <span data-ttu-id="dd2c9-120">프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-120">Project manager</span></span>               | <span data-ttu-id="dd2c9-121">프로젝트 계획을 작성하고 자원을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="dd2c9-122">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-122">Business unit</span></span> |
| <span data-ttu-id="dd2c9-123">프로젝트 리소스</span><span class="sxs-lookup"><span data-stu-id="dd2c9-123">Project resource</span></span>              | <span data-ttu-id="dd2c9-124">시간을 예약 및 보고할 수 있는 팀 구성원.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="dd2c9-125">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-125">Business unit</span></span>|
| <span data-ttu-id="dd2c9-126">리소스 관리자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-126">Resource manager</span></span>              | <span data-ttu-id="dd2c9-127">리소스 요청 및 예약 이행과 같은 모든 리소스 관리 기능은 하이브리드 프로젝트 관리자 + 리소스 관리자 구성 및 단일 및 중앙 집중식 리소스 관리자 역할을 지원하도록 분리됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="dd2c9-128">사업부</span><span class="sxs-lookup"><span data-stu-id="dd2c9-128">Business unit</span></span> |


<span data-ttu-id="dd2c9-129">웹용 Microsoft Project에는 다음 역할이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="dd2c9-130">역할</span><span class="sxs-lookup"><span data-stu-id="dd2c9-130">Role</span></span>           | <span data-ttu-id="dd2c9-131">설명</span><span class="sxs-lookup"><span data-stu-id="dd2c9-131">Description</span></span>                                                                                                        | <span data-ttu-id="dd2c9-132">Scope</span><span class="sxs-lookup"><span data-stu-id="dd2c9-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="dd2c9-133">프로젝트 사용자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-133">Project user</span></span>   | <span data-ttu-id="dd2c9-134">자신의 프로젝트를 만들고 공유된 프로젝트를 볼 수 있는 Project의 공동 작업 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="dd2c9-135">User</span><span class="sxs-lookup"><span data-stu-id="dd2c9-135">User</span></span>   |
| <span data-ttu-id="dd2c9-136">프로젝트 시스템</span><span class="sxs-lookup"><span data-stu-id="dd2c9-136">Project system</span></span> | <span data-ttu-id="dd2c9-137">애플리케이션 컨텍스트에 사용되는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-137">Role used for application   context.</span></span> <span data-ttu-id="dd2c9-138">고객은 이 시스템 역할을 사용해서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="dd2c9-139">전역</span><span class="sxs-lookup"><span data-stu-id="dd2c9-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="dd2c9-140">보안 적용</span><span class="sxs-lookup"><span data-stu-id="dd2c9-140">Security enforcement</span></span>
<span data-ttu-id="dd2c9-141">프로젝트 수준에서 수행되는 작업은 로그인한 사용자의 컨텍스트에서 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="dd2c9-142">즉, 프로젝트를 생성, 열기 또는 삭제하려면 사용자가 CDS에서 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="dd2c9-143">CDS에서의 액세스는 플랫폼에 포함된 모든 가능한 메커니즘을 통해 부여될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="dd2c9-144">예를 들어, 더 큰 범위의 사용자가 프로젝트에 액세스할 수 있거나 사용자에게 액세스 권한을 부여하는 명시적인 프로젝트 공유 작업이 수행된 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="dd2c9-145">Project Operations에서 프로젝트를 만들 때 이것을 고려하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="dd2c9-146">Project Operations와의 현대적인 그룹 공동 작업</span><span class="sxs-lookup"><span data-stu-id="dd2c9-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="dd2c9-147">웹용 프로젝트 및 Project Operations는 공동 작업을 위한 최신 그룹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="dd2c9-148">그룹을 통해 프로젝트에 추가된 사용자는 프로젝트 계획을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="dd2c9-149">웹용 프로젝트는 할당 시 사용자를 그룹에 자동으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="dd2c9-150">그룹은 프로젝트의 권한을 허용하고 협업 아티팩트를 지원하여 공동으로 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="dd2c9-151">다음 다이어그램은 그룹 할당 프로세스 중에 발생하는 이벤트 및 상태 변경을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="dd2c9-152">Project Operations는 암시적 작업을 통해 그룹을 생성하지 않으며 그룹을 누르는 명시적 작업을 통해서만 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="dd2c9-153">**그룹 관리** 대화 상자의 그룹 구성원 검색은 환경 보안 그룹의 일부로 설정된 사용자로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="dd2c9-154">자세한 내용은 [환경에 대한 사용자 액세스 제어: 보안 그룹 및 라이선스](https://docs.microsoft.com/power-platform/admin/control-user-access)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

![그룹 모드](./media/groupsmode.png)

1. <span data-ttu-id="dd2c9-156">프로젝트는 생성된 사용자가 생성하고 소유합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="dd2c9-157">프로젝트 담당자가 팀으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="dd2c9-158">담당자 팀은 지정되거나 생성된 Office 그룹에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="dd2c9-159">프로젝트의 원래 담당자가 Office 그룹에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="dd2c9-160">배포 권장 사항</span><span class="sxs-lookup"><span data-stu-id="dd2c9-160">Deployment recommendation</span></span>
<span data-ttu-id="dd2c9-161">Office 그룹 공동 작업 모델이 발전함에 따라 시간이 지나면서 보다 세부적인 제어를 제공하는 기능이 추가될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="dd2c9-162">현재 Project Operations를 배포하는 고객은 기존 Microsoft Dynamics 365 보안 모델에 집중하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="dd2c9-163">자세한 내용은 [Common Data Service의 보안](https://docs.microsoft.com/power-platform/admin/wp-security)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-163">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="dd2c9-164">Project Operations 및 Microsoft Dynamics 365 Finance 보안</span><span class="sxs-lookup"><span data-stu-id="dd2c9-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="dd2c9-165">Project Operations에는 다음 역할이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="dd2c9-166">프로젝트 관리자</span><span class="sxs-lookup"><span data-stu-id="dd2c9-166">Project manager</span></span>
- <span data-ttu-id="dd2c9-167">프로젝트 회계사</span><span class="sxs-lookup"><span data-stu-id="dd2c9-167">Project accountant</span></span>

<span data-ttu-id="dd2c9-168">Finance의 보안에 대한 자세한 내용은 [역할 기반 보안](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd2c9-168">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>


