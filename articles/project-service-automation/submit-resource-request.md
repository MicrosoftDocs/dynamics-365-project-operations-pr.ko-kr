---
title: 리소스 요청 제출
description: 이 항목은 프로젝트 리소스에 대한 요청을 제출하는 방법에 대한 정보를 제공합니다.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753321"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="d7756-103">리소스 요청 제출</span><span class="sxs-lookup"><span data-stu-id="d7756-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7756-104">생성된 리소스 요건을 리소스 요청으로 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="d7756-105">그러면 요청이 이행을 위해 리소스 관리자에게 발송됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="d7756-106">Project Service Automation(PSA)의 **프로젝트** 페이지에서 **팀** 탭을 클릭하여 예약 가능한 리소스의 목록을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="d7756-107">목록에서 리소스 요건이 있는 일반 리소스를 선택한 다음**요청 제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![리소스 요청 제출](media/RM-how-to-18.png)

<span data-ttu-id="d7756-109">일반 팀원의 요청 상태가 **제출됨**으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="d7756-110">리소스 관리자가 요청을 이행한 후 리소스 관리자가 명명된 리소스의 예약으로 요청을 이행하면 일반 리소스가 명명된 리소스로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="d7756-111">그렇지 않으면 일반 리소스가 팀에 남아 있고 리소스 관리자가 명명된 리소스를 제안한 경우 요청 상태가 **검토 필요**로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7756-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
