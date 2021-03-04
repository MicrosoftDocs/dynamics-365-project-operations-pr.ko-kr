---
title: 프로젝트 리소싱 홈 페이지
description: 이 항목은 Dynamics 365용 Project Service Automation(PSA)에서 리소스 관리 능력에 대한 정보를 제공합니다.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6d62baf0d5a535d118df507edaba3059d44fd4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147436"
---
# <a name="resourcing-projects-home-page"></a><span data-ttu-id="ce661-103">프로젝트 리소싱 홈 페이지</span><span class="sxs-lookup"><span data-stu-id="ce661-103">Resourcing projects home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ce661-104">리소스는 서비스 기반 조직의 가장 중요한 자산입니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-104">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="ce661-105">올바른 리소스를 적시에 찾아, 프로젝트에 해당 리소스를 예약하고, 리소스를 활용하는 능력은 조직이 수익 목표와 고객 만족 목표를 달성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-105">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="ce661-106">Project Service Automation(PSA)의 프로젝트 리소싱 기능을 사용하여 다음을 수행할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="ce661-106">You can use the project resourcing functionality in Project Service Automation (PSA) to do the following:</span></span>

- <span data-ttu-id="ce661-107">사용 가능하고 자격을 갖춘 리소스를 예약하여 프로젝트 팀을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-107">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="ce661-108">일반 팀원 레코드를 만들고 해당 역할 및 리소스 구성 단위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-108">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="ce661-109">과업 할당에서 일반 팀원에 대한 리소스 요건을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-109">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="ce661-110">사용 가능한 리소스 기능에 대해 리소스 수요에 정의된 기능을 식별하여 기능들을 짝맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-110">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="ce661-111">대체 리소스.</span><span class="sxs-lookup"><span data-stu-id="ce661-111">Substitute resources.</span></span>
- <span data-ttu-id="ce661-112">프로젝트 스케줄 할당과 리소스 예약을 정렬합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-112">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="ce661-113">예약과 할당의 차이를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-113">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="ce661-114">사무실 외 상태에 대응하여 리소스 예약을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-114">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="ce661-115">프로젝트 관리자와 리소스 관리자 사이에서 공동 작업합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-115">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="ce661-116">리소스의 시간이 어떻게 활용되었는가를 세분화하는 것을 포함하여 목표 대비 리소스 활용 이력을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-116">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="ce661-117">기능과 숙련도 리포지토리를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-117">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="ce661-118">PSA에서 일반 또는 명명된 리소스 팀으로 프로젝트를 충원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-118">You can staff your project with a team of generic or named resources in PSA.</span></span> <span data-ttu-id="ce661-119">다양한 방법을 사용하여 팀원을 추가 및 할당하고 예약 및 할당을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce661-119">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> <span data-ttu-id="ce661-120">자세한 내용은 다음 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ce661-120">For additional information, see the following topics:</span></span>

- [<span data-ttu-id="ce661-121">프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 과업 할당</span><span class="sxs-lookup"><span data-stu-id="ce661-121">Book named bookable resources to a project team and assigning them tasks</span></span>](assign-named-bookable-resource.md)
- [<span data-ttu-id="ce661-122">작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성</span><span class="sxs-lookup"><span data-stu-id="ce661-122">Assign generic bookable resources to a task and generate resource requirements</span></span>](assign-generic-bookable-resource.md)
- [<span data-ttu-id="ce661-123">리소스 요건에서 명명된 리소스 예약</span><span class="sxs-lookup"><span data-stu-id="ce661-123">Book named resources from resource requirements</span></span>](book-named-resource.md)
- [<span data-ttu-id="ce661-124">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="ce661-124">Submit a resource request</span></span>](submit-resource-request.md)
- [<span data-ttu-id="ce661-125">리소스 요청에서 제안된 프로젝트 리소스를 수락 또는 거부</span><span class="sxs-lookup"><span data-stu-id="ce661-125">Accept or reject a proposed project resource from a resource request</span></span>](accept-reject-proposed-resource.md)
