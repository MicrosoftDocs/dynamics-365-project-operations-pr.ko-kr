---
title: 매출액 추산 및 프로젝트
description: 이 항목은 판매 프로세스에서 스케줄과 추산을 활용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283916"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="a9ca6-103">매출액 추산 및 프로젝트</span><span class="sxs-lookup"><span data-stu-id="a9ca6-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a9ca6-104">판매 프로세스 중에 프로젝트를 판매 견적에 연계하여 판매 견적을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="a9ca6-105">이러한 방식으로 프로젝트 스케줄링 및 추산 기능을 활용하기 위해 판매 프로세스 중에 결정적인 추산이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="a9ca6-106">판매가 진행되는 경우 매출액 추산 목적으로 사용된 스케줄을 프로젝트 계획의 추가 구체화를 위한 기초로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="a9ca6-107">프로젝트를 견적 행에 연계</span><span class="sxs-lookup"><span data-stu-id="a9ca6-107">Linking a project to a quote line</span></span>

<span data-ttu-id="a9ca6-108">프로젝트 기반 견적 행을 생성할 때 새 프로젝트를 생성하거나 **견적 행** 페이지의 기존 프로젝트를 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![견적 행 양식](media/project-8.png)
 
<span data-ttu-id="a9ca6-110">견적 행 내역에서 새 프로젝트를 만들 때 프로젝트 템플릿을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="a9ca6-111">프로젝트 템플릿은 조직에서 일반적인 표준 프로젝트 계획 및 재무 예측을 나타내는 모델 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="a9ca6-112">또한 과거 프로젝트의 프로젝트 계획 및 추산의 복사본을 나타낼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![견적 행 내역](media/project-9.png)
  
<span data-ttu-id="a9ca6-114">견적에서 프로젝트를 만들면 프로젝트가 견적 행에 자동으로 연계됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="a9ca6-115">프로젝트의 추산 구성 요소</span><span class="sxs-lookup"><span data-stu-id="a9ca6-115">Components of estimates in a project</span></span>

<span data-ttu-id="a9ca6-116">스케줄을 통해 작업을 과업들로 나누고, 과업 계층 구조를 유지하고, 과업을 완료하는 데 요구되는 리소스를 결정하고, 과업을 완료하는 데 요구되는 노력의 추산을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="a9ca6-117">**프로젝트** 페이지에서 **스케줄** 탭의 필드를 사용하여 작업 노력을 정의하고 추산을 스케줄링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="a9ca6-118">가격표는 프로젝트와 연계되어 있기 때문에 가격표에 정의된 원가 및 판매 가격을 사용하여 재무 추산이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="a9ca6-119">프로젝트에서 견적으로 추산 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9ca6-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="a9ca6-120">프로젝트 견적을 정의한 후 견적 행으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="a9ca6-121">**견적 행 내역** 페이지에서 리본에 있는 **추산에서 가져오기** 를 선택하여 프로젝트 추산을 처리 타입, 역할 또는 과업 수준별로 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ca6-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]