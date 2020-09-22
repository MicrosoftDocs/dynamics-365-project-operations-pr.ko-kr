---
title: 기능 및 숙련도 모델
description: 이 항목은 기능 및 숙련도 모델을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753352"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="7774c-103">기능 및 숙련도 모델</span><span class="sxs-lookup"><span data-stu-id="7774c-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7774c-104">기능은 Dynamics 365 Project Service Automation과 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="7774c-105">Project Service Automation에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능**으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="7774c-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![리소스 기능](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="7774c-107">숙련도 모델을 사용하여 리소스 평가</span><span class="sxs-lookup"><span data-stu-id="7774c-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="7774c-108">리소스의 기능은 숙련도 모델에 의해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="7774c-109">개별 등급은 숙련도 모델에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="7774c-110">숙련도 모델을 만들려면 **리소스** \> **숙련도 모델**로 이동한 다음 **신규**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="7774c-111">새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="7774c-112">**등급 값** 하위 그리드에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![정의된 최소 및 최대 등급](media/Resource-Management-image85.png)

<span data-ttu-id="7774c-114">이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7774c-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
