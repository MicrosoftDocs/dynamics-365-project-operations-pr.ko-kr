---
title: 기술 및 숙련도 정의
description: 이 항목은 리소스를 평가하기 위해 숙련도 모델을 설정하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124781"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="3feb9-103">기술 및 숙련도 정의</span><span class="sxs-lookup"><span data-stu-id="3feb9-103">Define skills and proficiencies</span></span>

<span data-ttu-id="3feb9-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="3feb9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3feb9-105">기능은 Dynamics 365 Project Operations와 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="3feb9-106">Project Operations에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능** 으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="3feb9-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="3feb9-107">숙련도 모델을 사용하여 리소스 평가</span><span class="sxs-lookup"><span data-stu-id="3feb9-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="3feb9-108">리소스의 기능은 숙련도 모델에 의해 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="3feb9-109">개별 등급은 숙련도 모델에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="3feb9-110">숙련도 모델을 만들려면 **리소스** \> **숙련도 모델** 로 이동한 다음 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="3feb9-111">새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="3feb9-112">**등급 값** 하위 표에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="3feb9-113">이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3feb9-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
