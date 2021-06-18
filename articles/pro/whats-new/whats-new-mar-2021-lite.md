---
title: 2021년 3월의 새로운 기능 - Project Operations 라이트 배포
description: 이 항목은 Project Operations 라이트 배포의 2021년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993874"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="58322-103">2021년 3월의 새로운 기능 - Project Operations 라이트 배포</span><span class="sxs-lookup"><span data-stu-id="58322-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="58322-104">_적용 대상: 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="58322-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="58322-105">이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="58322-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="58322-106">Dataverse 환경 버전 4.8.0.91의 Project Operations</span><span class="sxs-lookup"><span data-stu-id="58322-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="58322-107">품질 업데이트</span><span class="sxs-lookup"><span data-stu-id="58322-107">Quality updates</span></span>

| <span data-ttu-id="58322-108">**기능 영역**</span><span class="sxs-lookup"><span data-stu-id="58322-108">**Feature area**</span></span> | <span data-ttu-id="58322-109">**참조 번호**</span><span class="sxs-lookup"><span data-stu-id="58322-109">**Reference number**</span></span> | <span data-ttu-id="58322-110">**품질 업데이트**</span><span class="sxs-lookup"><span data-stu-id="58322-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="58322-111">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="58322-111">Billing and pricing</span></span> | <span data-ttu-id="58322-112">2133873</span><span class="sxs-lookup"><span data-stu-id="58322-112">2133873</span></span> | <span data-ttu-id="58322-113">**경비 추정** 그리드의 **단위 판매 가격** 통화 기호의 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="58322-114">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="58322-114">Billing and pricing</span></span> | <span data-ttu-id="58322-115">2174616</span><span class="sxs-lookup"><span data-stu-id="58322-115">2174616</span></span> | <span data-ttu-id="58322-116">견적이 성공되면 견적에서 복사된 계약 내용 세부 사항에서 계약 사용자 정의 가격표가 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="58322-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="58322-117">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="58322-117">Opportunity Management</span></span> | <span data-ttu-id="58322-118">2167475</span><span class="sxs-lookup"><span data-stu-id="58322-118">2167475</span></span> | <span data-ttu-id="58322-119">청구되지 않은 실제 입력이 발생한 수정 송장의 세액이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="58322-120">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="58322-120">Opportunity Management</span></span> | <span data-ttu-id="58322-121">2176285</span><span class="sxs-lookup"><span data-stu-id="58322-121">2176285</span></span> | <span data-ttu-id="58322-122">판매 계약/견적 라인 상세 내역에서 원가 계약/견적 라인 상세 내역으로 세액을 복사할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="58322-123">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="58322-123">Opportunity Management</span></span> | <span data-ttu-id="58322-124">2188079</span><span class="sxs-lookup"><span data-stu-id="58322-124">2188079</span></span> | <span data-ttu-id="58322-125">작업 기반이 아닌 계약에 대해서는 분할 청구 규칙을 생성하면 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="58322-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="58322-126">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="58322-126">Planning and Tracking</span></span> | <span data-ttu-id="58322-127">2138853</span><span class="sxs-lookup"><span data-stu-id="58322-127">2138853</span></span> | <span data-ttu-id="58322-128">참조 작업이 대상 프로젝트에 복사되는 경비 추정 라인을 보장하기 위해 프로젝트 복사 기능이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="58322-129">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="58322-129">Planning and Tracking</span></span> | <span data-ttu-id="58322-130">2173259</span><span class="sxs-lookup"><span data-stu-id="58322-130">2173259</span></span> | <span data-ttu-id="58322-131">특정 시나리오에서 **WBS 복사** 오류 메시지를 표시하지 않도록 프로젝트 복사 기능이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="58322-132">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="58322-132">Time and Expense</span></span> | <span data-ttu-id="58322-133">2148910</span><span class="sxs-lookup"><span data-stu-id="58322-133">2148910</span></span> | <span data-ttu-id="58322-134">**시간 항목** 그리드에서 **항목 편집** 페이지의 표시 문제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="58322-135">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="58322-135">Time and Expense</span></span> | <span data-ttu-id="58322-136">2159798</span><span class="sxs-lookup"><span data-stu-id="58322-136">2159798</span></span> | <span data-ttu-id="58322-137">승인된 경비 항목을 편집할 수 없도록 제어를 강화했습니다.</span><span class="sxs-lookup"><span data-stu-id="58322-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


