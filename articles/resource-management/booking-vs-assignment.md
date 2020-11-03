---
title: 예약 및 할당 비교
description: 이 항목은 리소스 예약과 리소스 할당 간의 차이점에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079901"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="33ebd-103">예약 및 할당 비교</span><span class="sxs-lookup"><span data-stu-id="33ebd-103">Bookings vs assignments</span></span>

<span data-ttu-id="33ebd-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="33ebd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33ebd-105">예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="33ebd-106">확정 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="33ebd-107">할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 할당하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="33ebd-108">리소스는 실제 또는 일반 리소스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="33ebd-109">이상적으로는, 실제 리소스의 경우 예약과 할당이 다르지 않기 때문에 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="33ebd-110">그러나 Microsoft Dynamics Project Operations는 이 계약을 강제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="33ebd-111">**조정** 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33ebd-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
