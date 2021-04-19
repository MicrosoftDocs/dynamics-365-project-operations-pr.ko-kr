---
title: Project Service Automation 업데이트 릴리스 29.5, 핫픽스 V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 29.5 핫픽스, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715685"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="4aeed-103">Project Service Automation 업데이트 릴리스 29.5, V3의 새로운 기능 또는 변경된 기능</span><span class="sxs-lookup"><span data-stu-id="4aeed-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="4aeed-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4aeed-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4aeed-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4aeed-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="4aeed-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4aeed-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4aeed-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4aeed-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 29.5에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="4aeed-110">이 버전의 빌드 번호는 V3.10.47.150이며 2021년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="4aeed-111">업데이트 릴리스 29.5</span><span class="sxs-lookup"><span data-stu-id="4aeed-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4aeed-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="4aeed-112">Bug fixes</span></span>


<span data-ttu-id="4aeed-113">**판매**</span><span class="sxs-lookup"><span data-stu-id="4aeed-113">**Sales**</span></span>

<span data-ttu-id="4aeed-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4aeed-115">원가로 견적을 마감하고 견적에 가격표가 없는 경우 **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** 에서 가능한 null 참조 예외가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4aeed-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
