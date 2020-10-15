---
title: 리소스 관리 주요 개념
description: 이 항목은 Microsoft Dynamics Project Operations에서 리소스 관리 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897549"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="45c11-103">리소스 관리 주요 개념</span><span class="sxs-lookup"><span data-stu-id="45c11-103">Resource management key concepts</span></span>

<span data-ttu-id="45c11-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="45c11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45c11-105">리소스는 서비스 기반 조직의 가장 중요한 자산입니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="45c11-106">올바른 리소스를 적시에 찾아, 프로젝트에 해당 리소스를 예약하고, 리소스를 활용하는 능력은 조직이 수익 목표와 고객 만족 목표를 달성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="45c11-107">Dynamics 365 Project Operations의 프로젝트 리소싱 기능을 사용하여 다음 작업을 수행할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="45c11-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="45c11-108">사용 가능하고 자격을 갖춘 리소스를 예약하여 프로젝트 팀을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="45c11-109">일반 팀원 레코드를 만들고 해당 역할 및 리소스 구성 단위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="45c11-110">과업 할당에서 일반 팀원에 대한 리소스 요건을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="45c11-111">사용 가능한 리소스 기능에 대해 리소스 수요에 정의된 기능을 식별하여 기능들을 짝맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="45c11-112">대체 리소스.</span><span class="sxs-lookup"><span data-stu-id="45c11-112">Substitute resources.</span></span>
- <span data-ttu-id="45c11-113">프로젝트 스케줄 할당과 리소스 예약을 정렬합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="45c11-114">예약과 할당의 차이를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="45c11-115">사무실 외 상태에 대응하여 리소스 예약을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="45c11-116">프로젝트 관리자와 리소스 관리자 사이에서 공동 작업합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="45c11-117">리소스의 시간이 어떻게 활용되었는가를 세분화하는 것을 포함하여 목표 대비 리소스 활용 이력을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="45c11-118">기능과 숙련도 리포지토리를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="45c11-119">Project Operations에서 일반 또는 명명된 리소스 팀으로 프로젝트를 충원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="45c11-120">다양한 방법을 사용하여 팀원을 추가 및 할당하고 예약 및 할당을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45c11-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
