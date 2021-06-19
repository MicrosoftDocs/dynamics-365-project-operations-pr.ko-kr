---
title: 기능 및 숙련도 모델
description: 이 항목은 기능 및 숙련도 모델을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008679"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="08b62-103">기능 및 숙련도 모델</span><span class="sxs-lookup"><span data-stu-id="08b62-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="08b62-104">기능은 Dynamics 365 Project Service Automation과 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="08b62-105">Project Service Automation에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능** 으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="08b62-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![리소스 기능](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="08b62-107">숙련도 모델을 사용하여 리소스 평가</span><span class="sxs-lookup"><span data-stu-id="08b62-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="08b62-108">리소스의 기능은 숙련도 모델에 의해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="08b62-109">개별 등급은 숙련도 모델에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="08b62-110">숙련도 모델을 만들려면 **리소스** \> **숙련도 모델** 로 이동한 다음 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="08b62-111">새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="08b62-112">**등급 값** 하위 표에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![정의된 최소 및 최대 등급](media/Resource-Management-image85.png)

<span data-ttu-id="08b62-114">이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08b62-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]