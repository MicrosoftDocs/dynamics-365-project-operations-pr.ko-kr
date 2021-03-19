---
title: 예약 및 할당 비교
description: 이 항목은 리소스 예약과 리소스 할당 간의 차이점에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279911"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="a6170-103">예약 및 할당 비교</span><span class="sxs-lookup"><span data-stu-id="a6170-103">Bookings vs assignments</span></span>

<span data-ttu-id="a6170-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a6170-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6170-105">예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a6170-106">확정 예약은 리소스의 능력을 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="a6170-107">예약은 팀의 조직 개념을 나타내므로 다양한 프로젝트에서 리소스가 사용되는 방식을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="a6170-108">Dynamics 365 Project Operations는 예약을 프로젝트 수준 개념으로 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="a6170-109">예약과 달리 할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 약정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a6170-110">리소스는 이름이 지정되거나 일반이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-110">The resources can be named or generic.</span></span>  <span data-ttu-id="a6170-111">리소스 요구 사항이 프로젝트 작업 할당에서 파생되면 Project Operations는 리소스 할당의 작업량 등고선을 사용하여 리소스 요구 사항 세부 정보의 등고선을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="a6170-112">그러나 리소스 할당에 대한 참조는 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="a6170-113">리소스 요구 사항에서 파생된 예약에 대한 업데이트는 리소스 할당을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="a6170-114">일반적으로 리소스 예약 합계는 하나 이상의 작업에 대한 리소스 할당 합계와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="a6170-115">그러나 Project Operations는 이 계약을 강제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="a6170-116">**조정** 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6170-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]