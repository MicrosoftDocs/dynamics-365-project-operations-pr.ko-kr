---
title: 프로젝트 단계
description: 이 항목은 프로젝트 단계에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753250"
---
# <a name="project-stages"></a><span data-ttu-id="893db-103">프로젝트 단계</span><span class="sxs-lookup"><span data-stu-id="893db-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="893db-104">프로젝트 단계는 프로젝트가 진행됨에 따라 프로젝트의 상태를 반영하도록 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="893db-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="893db-105">기본 비즈니스 프로세스 흐름은 프로젝트의 일부 단계를 자동으로 업데이트하지만 다른 단계는 프로젝트 관리자가 수동으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="893db-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="893db-106">다음 단계는 기본 BPF에 정의되어 있습니다:</span><span class="sxs-lookup"><span data-stu-id="893db-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="893db-107">신규</span><span class="sxs-lookup"><span data-stu-id="893db-107">New</span></span>
- <span data-ttu-id="893db-108">견적</span><span class="sxs-lookup"><span data-stu-id="893db-108">Quote</span></span>
- <span data-ttu-id="893db-109">계획</span><span class="sxs-lookup"><span data-stu-id="893db-109">Plan</span></span>
- <span data-ttu-id="893db-110">인도</span><span class="sxs-lookup"><span data-stu-id="893db-110">Deliver</span></span>
- <span data-ttu-id="893db-111">완료</span><span class="sxs-lookup"><span data-stu-id="893db-111">Complete</span></span>
- <span data-ttu-id="893db-112">닫기</span><span class="sxs-lookup"><span data-stu-id="893db-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="893db-113">신규</span><span class="sxs-lookup"><span data-stu-id="893db-113">New</span></span>

<span data-ttu-id="893db-114">프로젝트 생성 시 프로젝트 단계는 **신규**로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="893db-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="893db-115">템플릿에서 프로젝트를 만든 경우 스케줄, 추산 및 팀 데이터가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="893db-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="893db-116">그렇지 않으면 그것은 프로젝트의 개요일 뿐이며 나머지 구성 요소를 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="893db-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="893db-117">견적</span><span class="sxs-lookup"><span data-stu-id="893db-117">Quote</span></span>

<span data-ttu-id="893db-118">프로젝트를 견적과 연계하거나 견적에서 프로젝트를 만들 경우, 프로젝트 단계는 **견적**으로 설정되며 예상 시작 및 종료 날짜도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="893db-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="893db-119">프로젝트가 **견적** 단계에 있는 동안 **프로젝트 엔터티** 페이지의 **판매** 탭은 견적 내역을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="893db-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="893db-120">계획</span><span class="sxs-lookup"><span data-stu-id="893db-120">Plan</span></span>

<span data-ttu-id="893db-121">프로젝트와 연계된 견적을 따서 프로젝트가 **계약** 단계로 이동한 경우, 프로젝트 단계는 **계획**으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="893db-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="893db-122">프로젝트가 **계획** 단계에 있는 동안 **프로젝트 엔터티** 페이지는 계약 내역을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="893db-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="893db-123">인도</span><span class="sxs-lookup"><span data-stu-id="893db-123">Deliver</span></span>

<span data-ttu-id="893db-124">프로젝트 계획이 완료되어 귀하가 프로젝트를 시작할 준비가 되면 프로젝트 관리자는 프로젝트 단계를 **인도**로 업데이트하여 프로젝트가 시작되었음을 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="893db-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="893db-125">완료</span><span class="sxs-lookup"><span data-stu-id="893db-125">Complete</span></span> 

<span data-ttu-id="893db-126">프로젝트를 위한 작업이 완료되면 프로젝트 관리자는 그 단계를 **완료**로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="893db-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="893db-127">프로젝트 단계를 **완료**로 업데이트함으로써 프로젝트 관리자는 작업이 100% 완료되었지만 프로젝트가 미결로 유지되어 미결 시간 또는 경비 항목을 기록할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="893db-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="893db-128">닫기</span><span class="sxs-lookup"><span data-stu-id="893db-128">Close</span></span>

<span data-ttu-id="893db-129">모든 처리가 기록되면 프로젝트 관리자는 그 단계를 **종결**로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="893db-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="893db-130">그 시점에서는 처리를 기록할 수 없으며 프로젝트는 읽기 전용으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="893db-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
