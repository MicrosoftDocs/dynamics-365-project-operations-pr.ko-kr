---
title: 프로젝트 스테이지 유형
description: 이 항목은 프로젝트 단계에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008994"
---
# <a name="project-stage-types"></a><span data-ttu-id="a1656-103">프로젝트 스테이지 유형</span><span class="sxs-lookup"><span data-stu-id="a1656-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a1656-104">프로젝트 단계는 프로젝트가 진행됨에 따라 프로젝트의 상태를 반영하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a1656-105">사용자 지정을 사용하여 비즈니스 프로세스 흐름, Power Automate 또는 플러그인 확장으로 단계를 자동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="a1656-106">다음 단계는 기본 BPF에 정의되어 있습니다:</span><span class="sxs-lookup"><span data-stu-id="a1656-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="a1656-107">신규</span><span class="sxs-lookup"><span data-stu-id="a1656-107">New</span></span>
- <span data-ttu-id="a1656-108">견적</span><span class="sxs-lookup"><span data-stu-id="a1656-108">Quote</span></span>
- <span data-ttu-id="a1656-109">계획</span><span class="sxs-lookup"><span data-stu-id="a1656-109">Plan</span></span>
- <span data-ttu-id="a1656-110">인도</span><span class="sxs-lookup"><span data-stu-id="a1656-110">Deliver</span></span>
- <span data-ttu-id="a1656-111">완료</span><span class="sxs-lookup"><span data-stu-id="a1656-111">Complete</span></span>
- <span data-ttu-id="a1656-112">닫기</span><span class="sxs-lookup"><span data-stu-id="a1656-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a1656-113">신규</span><span class="sxs-lookup"><span data-stu-id="a1656-113">New</span></span>

<span data-ttu-id="a1656-114">프로젝트 생성 시 프로젝트 단계는 **신규** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a1656-115">템플릿에서 프로젝트를 만든 경우 스케줄, 추산 및 팀 데이터가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a1656-116">그렇지 않으면 그것은 프로젝트의 개요일 뿐이며 나머지 구성 요소를 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a1656-117">견적</span><span class="sxs-lookup"><span data-stu-id="a1656-117">Quote</span></span>

<span data-ttu-id="a1656-118">프로젝트를 견적과 연계하거나 견적에서 프로젝트를 만들 경우, 프로젝트 단계는 **견적** 으로 설정되며 예상 시작 및 종료 날짜도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a1656-119">프로젝트가 **견적** 단계에 있는 동안 **프로젝트 엔터티** 페이지의 **판매** 탭은 견적 내역을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a1656-120">계획</span><span class="sxs-lookup"><span data-stu-id="a1656-120">Plan</span></span>

<span data-ttu-id="a1656-121">프로젝트와 연계된 견적을 따서 프로젝트가 **계약** 단계로 이동한 경우, 프로젝트 단계는 **계획** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a1656-122">프로젝트가 **계획** 단계에 있는 동안 **프로젝트 엔터티** 페이지는 계약 내역을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a1656-123">인도</span><span class="sxs-lookup"><span data-stu-id="a1656-123">Deliver</span></span>

<span data-ttu-id="a1656-124">프로젝트 계획이 완료되어 귀하가 프로젝트를 시작할 준비가 되면 프로젝트 관리자는 프로젝트 단계를 **인도** 로 업데이트하여 프로젝트가 시작되었음을 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a1656-125">완료</span><span class="sxs-lookup"><span data-stu-id="a1656-125">Complete</span></span> 

<span data-ttu-id="a1656-126">프로젝트를 위한 작업이 완료되면 프로젝트 관리자는 그 단계를 **완료** 로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a1656-127">프로젝트 단계를 **완료** 로 업데이트함으로써 프로젝트 관리자는 작업이 100% 완료되었지만 프로젝트가 미결로 유지되어 미결 시간 또는 경비 항목을 기록할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a1656-128">닫기</span><span class="sxs-lookup"><span data-stu-id="a1656-128">Close</span></span>

<span data-ttu-id="a1656-129">모든 처리가 기록되면 프로젝트 관리자는 그 단계를 **종결** 로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a1656-130">그 시점에서는 처리를 기록할 수 없으며 프로젝트는 읽기 전용으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1656-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]