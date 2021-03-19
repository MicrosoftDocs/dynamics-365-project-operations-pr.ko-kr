---
title: 리소스 관리 FAQ
description: 이 항목은 리소스 관리에 대해 자주 묻는 질문에 대한 답변을 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 20562b98ccc8451ab57dd42fb8c2f9f303811dbe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283151"
---
# <a name="resource-management-faq"></a><span data-ttu-id="e08eb-103">리소스 관리 FAQ</span><span class="sxs-lookup"><span data-stu-id="e08eb-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="e08eb-104">팀원과 리소스 요건 사이의 차이는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="e08eb-105">프로젝트 팀원은 과업에 할당, 예약 또는 초과 예약되거나 결재자로 설정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="e08eb-106">리소스 요건은 수요의 초안으로 프로젝트 팀원 없이도 존재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="e08eb-107">제안된 시간과 가예약된 시간 사이의 차이는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="e08eb-108">제안된 시간과 가예약된 시간은 가시성이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="e08eb-109">제안된 시간은 리소스 요청을 사용하여 요청을 시작한 리소스 관리자와 프로젝트 관리자에게만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="e08eb-110">가예약된 시간은 스케줄 보드에 액세스할 수 있는 모든 사용자가 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="e08eb-111">팀의 리소스에 대한 가예약된 시간을 어떻게 확인할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="e08eb-112">리소스 요건 예약 시, 가예약을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="e08eb-113">프로젝트 팀에서 가예약된 리소스는 가예약된 시간이 있는 팀웜으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="e08eb-114">또한 스케줄 게시판에도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="e08eb-115">예약한 리소스(일반 또는 명명된)에 대해 요구되는 시간과 시작 날짜 및 종료 날짜를 변경하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="e08eb-116">리소스를 예약한 후 요구되는 변경을 하려면 **예약 정비** 를 선택하십시오.</span><span class="sxs-lookup"><span data-stu-id="e08eb-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="e08eb-117">Project Service Automation은 어떤 리소스 타입을 지원합니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="e08eb-118">**사용자** 및 **연락처** 가 Dynamics 365 Project Service Automation에서 지원되는 유일한 리소스 타입입니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="e08eb-119">다른 타입의 리소스(예: **장비** 및 **그룹**)를 만들 수 있지만 종단 간 사용 사례는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="e08eb-120">할당과 예약 사이의 차이는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="e08eb-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="e08eb-121">할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 할당하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="e08eb-122">리소스는 실제 또는 일반 리소스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="e08eb-123">예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="e08eb-124">확정 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="e08eb-125">이상적으로는, 실제 리소스의 경우 예약과 할당이 다르지 않기 때문에 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="e08eb-126">그러나 PSA는 이 일치를 강제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="e08eb-127">조정 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e08eb-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]