---
title: 경비 보고서에 배포
description: 경비 보고서에 경비를 입력하면 조직의 여러 프로젝트, 법인 또는 계정에 경비를 분배할 수 있습니다.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079933"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="7a7b1-103">경비 보고서에 배포</span><span class="sxs-lookup"><span data-stu-id="7a7b1-103">Distributions on an expense report</span></span>

<span data-ttu-id="7a7b1-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7a7b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7a7b1-105">경비 보고서에 경비를 입력하면 조직의 여러 프로젝트, 재무 차원 또는 계정에 경비를 분배할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="7a7b1-106">예를 들어 Fabrikam 영업 담당자인 Nancy는 코펜하겐에서 프랑크푸르트로 여행했습니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="7a7b1-107">프랑크푸르트에서 Nancy는 두 조직을 만나 각 조직에 대한 개별 프로젝트를 논의했습니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="7a7b1-108">Nancy는 프로젝트 A에서 조직 A와 작업하는 데 7일, 프로젝트 B에서 작업하는 데 3일을 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="7a7b1-109">Nancy는 프랑크푸르트에 있는 동안 두 개의 개별 프로젝트에서 작업했기 때문에 경비 보고서를 입력할 때 Nancy는 각 프로젝트에 맞게 경비를 분배합니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="7a7b1-110">다음 표는 Nancy가 경비를 분배한 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="7a7b1-111">경비 유형</span><span class="sxs-lookup"><span data-stu-id="7a7b1-111">Expense type</span></span> | <span data-ttu-id="7a7b1-112">총 경비 금액</span><span class="sxs-lookup"><span data-stu-id="7a7b1-112">Total expense amount</span></span> | <span data-ttu-id="7a7b1-113">프로젝트 A에 분배된 금액</span><span class="sxs-lookup"><span data-stu-id="7a7b1-113">Amount distributed to project A</span></span> | <span data-ttu-id="7a7b1-114">프로젝트 B에 분배된 금액</span><span class="sxs-lookup"><span data-stu-id="7a7b1-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="7a7b1-115">기차 요금</span><span class="sxs-lookup"><span data-stu-id="7a7b1-115">Train fare</span></span>   | <span data-ttu-id="7a7b1-116">DKK 578</span><span class="sxs-lookup"><span data-stu-id="7a7b1-116">DKK 578</span></span>              | <span data-ttu-id="7a7b1-117">DKK 405</span><span class="sxs-lookup"><span data-stu-id="7a7b1-117">DKK 405</span></span>                         | <span data-ttu-id="7a7b1-118">DKK 173</span><span class="sxs-lookup"><span data-stu-id="7a7b1-118">DKK 173</span></span>                         |
| <span data-ttu-id="7a7b1-119">호텔</span><span class="sxs-lookup"><span data-stu-id="7a7b1-119">Hotel</span></span>        | <span data-ttu-id="7a7b1-120">EUR 725</span><span class="sxs-lookup"><span data-stu-id="7a7b1-120">EUR 725</span></span>              | <span data-ttu-id="7a7b1-121">EUR 557</span><span class="sxs-lookup"><span data-stu-id="7a7b1-121">EUR 557</span></span>                         | <span data-ttu-id="7a7b1-122">EUR 168</span><span class="sxs-lookup"><span data-stu-id="7a7b1-122">EUR 168</span></span>                         |
| <span data-ttu-id="7a7b1-123">식사</span><span class="sxs-lookup"><span data-stu-id="7a7b1-123">Meals</span></span>        | <span data-ttu-id="7a7b1-124">EUR 346</span><span class="sxs-lookup"><span data-stu-id="7a7b1-124">EUR 346</span></span>              | <span data-ttu-id="7a7b1-125">EUR 284</span><span class="sxs-lookup"><span data-stu-id="7a7b1-125">EUR 284</span></span>                         | <span data-ttu-id="7a7b1-126">EUR 62</span><span class="sxs-lookup"><span data-stu-id="7a7b1-126">EUR 62</span></span>                          |
