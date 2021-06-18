---
title: 리소스 용량 동기화
description: 이 항목은 일정과 프로젝트에서 리소스의 용량을 동기화하는 방법에 대한 정보를 제공합니다.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997519"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="61768-103">리소스 용량 동기화</span><span class="sxs-lookup"><span data-stu-id="61768-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61768-104">리소스 동기화를 위한 프로세스는 일정 및 기본 일정에 대한 정보가 프로젝트 리소스 스케줄링으로 흘러 들어가는 것을 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="61768-105">일정이 변경되면 프로세스가 프로젝트 리소스 일정에 필요한 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="61768-106">일정의 리소스 정보가 미리 동기화되기 때문에 프로세스는 성능 향상에도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61768-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="61768-107">따라서 리소스 예약 정보에 대한 업데이트가 더 빨리 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="61768-108">프로세스를 한 번에 하나씩이 아닌 일괄 처리로 예약하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="61768-109">그렇지 않으면 정보가 마지막으로 동기화된 포함 날짜를 잊어 버릴 위험이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="61768-110">포함 날짜를 사용하지 않으면 날짜 동기화 중에 간격이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![일정 동기화](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="61768-112">리소스 생산 능력 롤업 동기화</span><span class="sxs-lookup"><span data-stu-id="61768-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="61768-113">동기화 프로세스는 모든 리소스 일정 정보를 동기화하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="61768-114">이 정보에는 프로젝트의 리소스 일정 생산 능력 테이블 변경 사항에 대한 기본 일정 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="61768-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="61768-115">프로젝트에 새 리소스가 추가된 경우 동기화를 통해 업데이트된 일정 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="61768-116">이 동기화는 언제든지 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="61768-117">일괄 처리를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-117">We recommend that you use a batch.</span></span> <span data-ttu-id="61768-118">이 옵션은 용량 예약 동기화 중에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61768-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="61768-119">**프로젝트 관리 및 회계** &gt; **주기적** &gt; **용량 동기화** &gt; **리소스 용량 롤업 동기화** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="61768-120">다음 표에서 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="61768-121">옵션</span><span class="sxs-lookup"><span data-stu-id="61768-121">Option</span></span>      | <span data-ttu-id="61768-122">설명</span><span class="sxs-lookup"><span data-stu-id="61768-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="61768-123">기간 코드</span><span class="sxs-lookup"><span data-stu-id="61768-123">Period code</span></span> | <span data-ttu-id="61768-124">선택적으로 총계정 원장 날짜 간격 코드를 선택하여 리소스 용량 롤업을 위한 동기화 프로세스의 시작 및 종료 날짜를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="61768-125">시작 날짜</span><span class="sxs-lookup"><span data-stu-id="61768-125">Start date</span></span>  | <span data-ttu-id="61768-126">리소스 용량 롤업을 위한 동기화 프로세스의 시작 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="61768-127">종료 날짜</span><span class="sxs-lookup"><span data-stu-id="61768-127">End date</span></span>    | <span data-ttu-id="61768-128">리소스 용량 롤업을 위한 동기화 프로세스의 종료 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="61768-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="61768-129">[![동기화 프로세스](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="61768-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]