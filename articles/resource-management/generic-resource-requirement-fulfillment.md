---
title: 일반 리소스 요구 사항 충족
description: 이 항목은 일반 리소스 요건을 위해 명명된 리소스를 예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279596"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="e83db-103">일반 리소스 요구 사항 충족</span><span class="sxs-lookup"><span data-stu-id="e83db-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="e83db-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="e83db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e83db-105">명명된 리소스를 예약하여 리소스 요건이 있는 일반 리소스를 대체할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="e83db-106">**프로젝트** 페이지에서 **팀** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="e83db-107">목록에서 리소스 요건이 있는 일반 리소스를 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="e83db-108">또는 리소스 요건을 연 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="e83db-109">**스케줄 도우미** 페이지에서 프로젝트 팀에 예약할 명명된 리소스를 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="e83db-110">명명된 리소스에 의해 예약이 완료되고 이행되면 일반 리소스가 명명된 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="e83db-111">스케줄에서의 배정도 명명된 리소스로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="e83db-112">명명된 여러 리소스로 일반 리소스 이행</span><span class="sxs-lookup"><span data-stu-id="e83db-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="e83db-113">일반 리소스를 위한 요건을 여러 명명된 리소스로 충족하는 것은 명명된 단일 리소스를 배정하는 것과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="e83db-114">예컨대, 5일의 기간과 120시간의 노력이 드는 과업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="e83db-115">이 과업은 주 5일에 걸쳐 일반적인 하루 8시간 일하는 하나의 리소스로 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="e83db-116">이 요건은 120시간의 로봇 공학을 위한 것으로서 하루 24시간에 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="e83db-117">이는 일반 리소스 요청을 이행하기 위해 여러 개의 명명된 리소스가 필요한 경우의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="e83db-118">요건을 충족하려면 여러 리소스를 예약해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="e83db-119">이 시나리오의 주요 차이점은 일반 리소스가 과업에 배정된 팀에 남아 있고 예약된 명명된 리소스 팀원이 직위의 일부로 배정되지 않는다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="e83db-120">프로젝트 관리자는 명명된 리소스에 적합한 과업을 배정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="e83db-121">**조정** 보기는 프로젝트 관리자가 여러 리소스에 걸쳐 작업 배정에 대한 예약을 나누는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="e83db-122">요건을 구성하는 작업 번들이 있는 경우와 같이 위의 간단한 예보다 더 복잡한 시나리오에서는 프로젝트 관리자가 배정하려는 방식의 의도를 시스템에서 가정해야 하기 때문에 이 작업은 자동으로 수행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="e83db-123">시스템이 의도를 이해할 수 없기 때문에 가정이 의도한 것과 다를 수 있으며 올바르지 않거나 예측할 수 없는 결과가 발생할 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="e83db-124">프로젝트 관리자가 **조정** 보기의 도움을 받아 의도적으로 배정을 만들 때까지 예측 가능한 결과는 일반 리소스가 배정된 상태로 유지된다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e83db-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]