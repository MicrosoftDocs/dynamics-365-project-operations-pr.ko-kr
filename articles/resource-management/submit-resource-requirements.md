---
title: 리소스 요청 제출
description: 생성된 리소스 요건을 리소스 요청으로 제출할 수 있습니다. 그러면 요청이 이행을 위해 리소스 관리자에게 발송됩니다.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128831"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="28602-104">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="28602-104">Submit a resource request</span></span>

<span data-ttu-id="28602-105">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="28602-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28602-106">생성된 리소스 요건을 리소스 요청으로 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28602-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="28602-107">그러면 요청이 이행을 위해 리소스 관리자에게 발송됩니다.</span><span class="sxs-lookup"><span data-stu-id="28602-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="28602-108">Dynamics 365 Project Operations의 **프로젝트** 페이지에서 **팀** 탭을 선택하여 예약 가능한 리소스의 목록을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="28602-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="28602-109">목록에서 리소스 요건이 있는 일반 리소스를 선택한 다음 **요청 제출** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="28602-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="28602-110">일반 팀원의 요청 상태가 **제출됨** 으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="28602-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="28602-111">요청을 이행한 후 리소스 관리자가 명명된 리소스의 예약으로 요청을 이행하면 일반 리소스가 명명된 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="28602-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="28602-112">그렇지 않고 리소스 관리자가 명명된 리소스를 제안한 경우 일반 리소스가 팀에 남아 있고 요청 상태가 **검토 필요** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="28602-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
