---
title: 일정 도우미 보기
description: 이 항목은 일정 도우미를 사용하여 리소스를 예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014124"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="62beb-103">일정 도우미 보기</span><span class="sxs-lookup"><span data-stu-id="62beb-103">Schedule assistant overview</span></span>

<span data-ttu-id="62beb-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="62beb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62beb-105">일정 도우미는 프로젝트 관리자가 정의한 요구 사항에 따라 리소스를 예약하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="62beb-106">일정 도우미는 리소스 요구 사항에 제공된 매개 변수를 사용하여 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="62beb-107">일정 도우미는 필요한 시간 창이나 기술과 같은 관련 요구 사항과 일치하는 리소스를 추천합니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="62beb-108">적절한 리소스가 식별되면 리소스 또는 프로젝트 관리자가 리소스를 작업에 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="62beb-109">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="62beb-109">Prerequisites</span></span>

<span data-ttu-id="62beb-110">일정 도우미는 Universal Resource Scheduling 솔루션의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="62beb-111">이 솔루션은 Dynamics 365 Project Operations, Dynamics 365 Field Service 및 Dynamics 365 Customer Service에 포함되며 함께 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="62beb-112">일치하는 요구 사항 및 리소스</span><span class="sxs-lookup"><span data-stu-id="62beb-112">Matching requirements and resources</span></span>

<span data-ttu-id="62beb-113">생성된 리소스 요구 사항은 다음과 같은 세부 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="62beb-114">특징</span><span class="sxs-lookup"><span data-stu-id="62beb-114">Characteristics</span></span>
-   <span data-ttu-id="62beb-115">역할</span><span class="sxs-lookup"><span data-stu-id="62beb-115">Roles</span></span>
-   <span data-ttu-id="62beb-116">사업부</span><span class="sxs-lookup"><span data-stu-id="62beb-116">Business units</span></span>
-   <span data-ttu-id="62beb-117">리소스 선호 설정</span><span class="sxs-lookup"><span data-stu-id="62beb-117">Resource preferences</span></span>
-   <span data-ttu-id="62beb-118">작업량 윤곽</span><span class="sxs-lookup"><span data-stu-id="62beb-118">Effort contours</span></span>
-   <span data-ttu-id="62beb-119">표준 시간대</span><span class="sxs-lookup"><span data-stu-id="62beb-119">Time zone</span></span>

<span data-ttu-id="62beb-120">일정 도우미는 이러한 세부 정보를 사용하여 리소스를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="62beb-121">일정 도우미 시작</span><span class="sxs-lookup"><span data-stu-id="62beb-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="62beb-122">일정 도우미를 시작하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="62beb-123">하이브리드 모드를 사용하는 경우 팀 구성원 표에서 충족되지 않은 리소스 요구 사항이 있는 팀 구성원을 선택한 다음 **예약** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="62beb-124">중앙 모드를 사용하는 경우 리소스 관리자가 리소스를 찾아 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="62beb-125">일정 도우미 필터</span><span class="sxs-lookup"><span data-stu-id="62beb-125">Schedule assistant filters</span></span>

<span data-ttu-id="62beb-126">일정 도우미가 실행된 후 리소스 요구 사항의 세부 정보가 왼쪽 창에 필터링된 값으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="62beb-127">리소스 관리자 또는 프로젝트 관리자는 일정 요구 사항을 충족하도록 필터를 조정하여 결과를 미세 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="62beb-128">필터 창에는 다음과 같은 작업 관련 옵션이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62beb-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="62beb-129">작업 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="62beb-129">Work start and end</span></span>
-   <span data-ttu-id="62beb-130">특징</span><span class="sxs-lookup"><span data-stu-id="62beb-130">Characteristics</span></span>
-   <span data-ttu-id="62beb-131">역할</span><span class="sxs-lookup"><span data-stu-id="62beb-131">Roles</span></span>
-   <span data-ttu-id="62beb-132">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="62beb-132">Organizational units</span></span>
-   <span data-ttu-id="62beb-133">리소싱 회사</span><span class="sxs-lookup"><span data-stu-id="62beb-133">Resourcing company</span></span>
-   <span data-ttu-id="62beb-134">리소스 유형</span><span class="sxs-lookup"><span data-stu-id="62beb-134">Resource types</span></span>
-   <span data-ttu-id="62beb-135">선호 리소스</span><span class="sxs-lookup"><span data-stu-id="62beb-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]