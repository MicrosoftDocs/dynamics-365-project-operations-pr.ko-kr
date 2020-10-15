---
title: 리소스 관리 모드 개요
description: 이 항목은 Dynamics 365 Project Operations에서 리소스 관리 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930099"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="6bc92-103">리소스 관리 모드 개요</span><span class="sxs-lookup"><span data-stu-id="6bc92-103">Resource management modes overview</span></span>

<span data-ttu-id="6bc92-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="6bc92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6bc92-105">Dynamics 365 Project Operations는 전체 예약 흐름을 실행하기 위해 두 가지 모드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="6bc92-106">관리 모드는 프로젝트 매개 변수로 정의되며 비즈니스 변경이 필요한 경우 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="6bc92-107">중앙 모드</span><span class="sxs-lookup"><span data-stu-id="6bc92-107">Central mode</span></span>
<span data-ttu-id="6bc92-108">프로젝트에 대한 리소스 할당을 중앙 집중화하는 조직의 경우 중앙 모드는 프로젝트 관리자가 프로젝트 수준에서 리소스 요구 사항을 정의할 수 있도록 하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="6bc92-109">리소스 요구 사항의 이행은 리소스 관리자에게 위임됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="6bc92-110">프로젝트 관리자는 리소스 관리자가 제안한 리소스를 수락하거나 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![중앙 모드](./media/resource-management-central.png)

<span data-ttu-id="6bc92-112">중앙 모드로 리소스를 관리하려면 다음을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6bc92-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="6bc92-113">작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성</span><span class="sxs-lookup"><span data-stu-id="6bc92-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="6bc92-114">리소스 요건에서 명명된 리소스 예약</span><span class="sxs-lookup"><span data-stu-id="6bc92-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="6bc92-115">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="6bc92-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="6bc92-116">리소스 요청 이행</span><span class="sxs-lookup"><span data-stu-id="6bc92-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="6bc92-117">리소스 요청에서 제안된 프로젝트 리소스를 수락 또는 거부</span><span class="sxs-lookup"><span data-stu-id="6bc92-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="6bc92-118">하이브리드 모델</span><span class="sxs-lookup"><span data-stu-id="6bc92-118">Hybrid mode</span></span>
<span data-ttu-id="6bc92-119">리소스 할당에 유연성이 필요한 조직의 경우 하이브리드 모드를 사용하면 프로젝트 관리자와 리소스 관리자 모두 리소스를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![하이브리드 모드](./media/resource-management-hybrid.png)

<span data-ttu-id="6bc92-121">지원되는 중앙 모드 프로세스 외에도 다음 항목을 참조하여 하이브리드 모드에서 지원되는 다른 모든 예약 흐름을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="6bc92-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="6bc92-122">프로젝트에 리소스를 직접 예약</span><span class="sxs-lookup"><span data-stu-id="6bc92-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="6bc92-123">프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정</span><span class="sxs-lookup"><span data-stu-id="6bc92-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="6bc92-124">리소스 요구 사항에서 리소스 예약:</span><span class="sxs-lookup"><span data-stu-id="6bc92-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="6bc92-125">작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성</span><span class="sxs-lookup"><span data-stu-id="6bc92-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="6bc92-126">리소스 요건에서 명명된 리소스 예약</span><span class="sxs-lookup"><span data-stu-id="6bc92-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
