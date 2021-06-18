---
title: 프로젝트 견적 관리
description: 이 항목은 프로젝트 견적에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8e0b20d4780a14edc3c242e261e22d4905f783a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994819"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="c1574-103">프로젝트 견적 관리</span><span class="sxs-lookup"><span data-stu-id="c1574-103">Manage project quotes</span></span>

<span data-ttu-id="c1574-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="c1574-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c1574-105">Dynamics 365 Project Operations에서 프로젝트 견적은 프로젝트 작업을 위한 제안서를 작성하는 데 도움이 되도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="c1574-106">Project Operations의 프로젝트 견적 구조는 다음 구성 요소를 사용하여 프로젝트 제안을 위해 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="c1574-107">상위 수준 구성 요소로 표시될 작업의 개별 구성 요소를 식별하는 견적 라인입니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="c1574-108">각 상위 수준 구성 요소 또는 견적 라인에 대한 작업을 식별하고 추정하는 견적 라인 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="c1574-109">작업의 일정 또는 날짜 추정과 재정적 측면은 해당 견적 라인에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="c1574-110">계약 모델 및 청구 가능 구성 요소는 각 견적 라인에 대해 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="c1574-111">이 설정은 각 견적 라인과 전체 견적에 대한 수익, 지출 및 수익성의 범위를 추정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="c1574-112">모든 프로젝트 기반 견적 보기</span><span class="sxs-lookup"><span data-stu-id="c1574-112">View all project-based quotes</span></span>

<span data-ttu-id="c1574-113">모든 프로젝트 견적 목록은 **견적** 목록 페이지에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="c1574-114">**영업** > **견적** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="c1574-115">시스템의 모든 프로젝트 견적 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="c1574-116">**보기 전환기** 를 사용하여 견적의 다른 필터링된 보기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="c1574-117">사용자 지정 필터 기준을 사용하여 고유한 보기 및 탐색 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="c1574-118">이 목록 페이지 또는 세부 사항 페이지에서 견적을 작성하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1574-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]