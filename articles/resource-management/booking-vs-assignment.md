---
title: 예약 및 할당 비교
description: 이 항목은 리소스 예약과 리소스 할당 간의 차이점에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130226"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="8730d-103">예약 및 할당 비교</span><span class="sxs-lookup"><span data-stu-id="8730d-103">Bookings vs assignments</span></span>

<span data-ttu-id="8730d-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="8730d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8730d-105">예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="8730d-106">확정 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="8730d-107">예약은 팀의 조직 개념을 나타내므로 다양한 프로젝트에서 리소스가 사용되는 방식을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="8730d-108">Dynamics 365 Project Operations는 예약을 프로젝트 수준 개념으로 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="8730d-109">예약과 달리 할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 약정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="8730d-110">리소스는 이름이 지정되거나 일반이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="8730d-111">일반적으로 리소스 예약 합계는 하나 이상의 작업에 대한 리소스 할당 합계와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="8730d-112">그러나 Project Operations는 이 계약을 강제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="8730d-113">**조정** 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8730d-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
