---
title: 프로젝트 송장 제안서 성능
description: 이 항목은 프로젝트 송장 제안의 성능 향상에 대한 정보를 제공합니다.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269798"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="98ccf-103">프로젝트 송장 제안서 성능</span><span class="sxs-lookup"><span data-stu-id="98ccf-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98ccf-104">새 송장 제안을 생성할 때 프로젝트 및 하위 프로젝트 수가 증가함에 따라 성능 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="98ccf-105">성능을 향상시키기 위해 게시된 프로젝트 트랜잭션에 대한 새 송장 제안을 생성하는 데 필요한 시간을 줄이는 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="98ccf-106">프로젝트 송장 제안 성능 향상 활성화</span><span class="sxs-lookup"><span data-stu-id="98ccf-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="98ccf-107">프로젝트 송장 제안 성능 향상 기능을 사용하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="98ccf-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="98ccf-108">**기능 관리** > **모두** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="98ccf-109">기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="98ccf-110">**지금 사용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="98ccf-111">브라우저를 새로 고친 다음 새 송장 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="98ccf-112">프로젝트 송장 제안 성능 향상 끄기</span><span class="sxs-lookup"><span data-stu-id="98ccf-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="98ccf-113">프로젝트 송장 제안 성능 향상을 끄려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="98ccf-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="98ccf-114">**기능 관리** > **모두** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="98ccf-115">기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="98ccf-116">**사용 안 함** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="98ccf-117">브라우저를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="98ccf-118">청구 규칙이 활성화된 경우 송장 제안 성능을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="98ccf-119">송장 제안을 생성하기 위한 배치 프로세스 동안 하위 작업의 수는 입력한 내용에 관계없이 송장 가능한 트랜잭션이 있는 계약 수를 기반으로 작업을 최대 수로 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="98ccf-120">예를 들어 **3** 을 입력하면 일괄 송장 제안 생성을 위한 하위 작업의 수에 대해 송장 가능한 트랜잭션이 있는 두 개의 계약만 있고 두 개의 하위 작업만 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="98ccf-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
