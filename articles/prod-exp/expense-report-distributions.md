---
title: 경비 보고서 배포
description: 경비 보고서에 경비를 입력하면 조직의 여러 프로젝트, 법인 또는 계정에 경비를 분배할 수 있습니다.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8850a8d3f2efc699bc95d4cb4fc76428badb10f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080209"
---
# <a name="expense-report-distributions"></a><span data-ttu-id="77c77-103">경비 보고서 배포</span><span class="sxs-lookup"><span data-stu-id="77c77-103">Expense report distributions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77c77-104">경비 보고서에 경비를 입력하면 조직의 여러 프로젝트, 재무 차원 또는 계정에 경비를 분배할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="77c77-105">예를 들어 Fabrikam 영업 담당자인 Nancy는 코펜하겐에서 프랑크푸르트로 여행했습니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="77c77-106">프랑크푸르트에서 그녀는 두 조직을 만나 각 조직에 대한 개별 프로젝트를 논의했습니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="77c77-107">Nancy는 프로젝트 A에서 조직 A와 작업하는 데 7일, 프로젝트 B에서 작업하는 데 3일을 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="77c77-108">Nancy는 프랑크푸르트에 있는 동안 두 개의 개별 프로젝트에서 작업했기 때문에 경비 보고서를 입력할 때 그녀는 각 프로젝트에 맞게 경비를 분배합니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="77c77-109">다음 표는 Nancy가 경비를 분배한 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="77c77-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="77c77-110">경비 유형</span><span class="sxs-lookup"><span data-stu-id="77c77-110">Expense type</span></span> | <span data-ttu-id="77c77-111">총 경비 금액</span><span class="sxs-lookup"><span data-stu-id="77c77-111">Total expense amount</span></span>|<span data-ttu-id="77c77-112">프로젝트 A에 분배된 금액</span><span class="sxs-lookup"><span data-stu-id="77c77-112">Amount distributed to project A</span></span>| <span data-ttu-id="77c77-113">프로젝트 B에 분배된 금액</span><span class="sxs-lookup"><span data-stu-id="77c77-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="77c77-114">기차 요금</span><span class="sxs-lookup"><span data-stu-id="77c77-114">Train fare</span></span>   |<span data-ttu-id="77c77-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="77c77-115">DKK 578</span></span>              |<span data-ttu-id="77c77-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="77c77-116">DKK 405</span></span>                        |<span data-ttu-id="77c77-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="77c77-117">DKK 173</span></span>                          |
|<span data-ttu-id="77c77-118">호텔</span><span class="sxs-lookup"><span data-stu-id="77c77-118">Hotel</span></span>         |<span data-ttu-id="77c77-119">EUR 725</span><span class="sxs-lookup"><span data-stu-id="77c77-119">EUR 725</span></span>              |<span data-ttu-id="77c77-120">EUR 557</span><span class="sxs-lookup"><span data-stu-id="77c77-120">EUR 557</span></span>                        |<span data-ttu-id="77c77-121">EUR 168</span><span class="sxs-lookup"><span data-stu-id="77c77-121">EUR 168</span></span>                          |
|<span data-ttu-id="77c77-122">식사</span><span class="sxs-lookup"><span data-stu-id="77c77-122">Meals</span></span>         |<span data-ttu-id="77c77-123">EUR 346</span><span class="sxs-lookup"><span data-stu-id="77c77-123">EUR 346</span></span>              |<span data-ttu-id="77c77-124">EUR 284</span><span class="sxs-lookup"><span data-stu-id="77c77-124">EUR 284</span></span>                        |<span data-ttu-id="77c77-125">EUR 62</span><span class="sxs-lookup"><span data-stu-id="77c77-125">EUR 62</span></span>                           |

