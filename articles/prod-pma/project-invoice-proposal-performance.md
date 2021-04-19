---
title: 프로젝트 송장 제안서 성능
description: 이 항목은 프로젝트 송장 제안의 성능 향상에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573567"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="82f7a-103">프로젝트 송장 제안서 성능</span><span class="sxs-lookup"><span data-stu-id="82f7a-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="82f7a-104">새 송장 제안을 생성할 때 프로젝트 및 하위 프로젝트 수가 증가함에 따라 성능 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="82f7a-105">성능을 향상시키기 위해 게시된 프로젝트 트랜잭션에 대한 새 송장 제안을 생성하는 데 필요한 시간을 줄이는 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="82f7a-106">프로젝트 송장 제안 성능 향상 활성화</span><span class="sxs-lookup"><span data-stu-id="82f7a-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="82f7a-107">프로젝트 송장 제안 성능 향상 기능을 사용하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="82f7a-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="82f7a-108">**기능 관리** > **모두** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="82f7a-109">기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="82f7a-110">**지금 사용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="82f7a-111">브라우저를 새로 고친 다음 새 송장 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="82f7a-112">프로젝트 송장 제안 성능 향상 끄기</span><span class="sxs-lookup"><span data-stu-id="82f7a-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="82f7a-113">프로젝트 송장 제안 성능 향상을 끄려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="82f7a-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="82f7a-114">**기능 관리** > **모두** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="82f7a-115">기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="82f7a-116">**사용 안 함** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="82f7a-117">브라우저를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="82f7a-118">청구 규칙이 활성화되어 있거나 일괄 프로세스가 실행 중인 경우 송장 제안 성능을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82f7a-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
