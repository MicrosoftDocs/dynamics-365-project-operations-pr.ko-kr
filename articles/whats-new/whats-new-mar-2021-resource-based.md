---
title: 2021년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations의 2021년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500019"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="4f242-103">2021년 3월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f242-103">What's new March 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="4f242-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="4f242-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4f242-105">이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="4f242-106">Dataverse 환경 버전 4.8.0.91의 Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f242-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 
- <span data-ttu-id="4f242-107">Dynamics 365 Finance 환경 버전 10.0.16의 프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="4f242-107">Project management and accounting on Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="4f242-108">품질 업데이트</span><span class="sxs-lookup"><span data-stu-id="4f242-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="4f242-109">Dataverse의 Project Operations</span><span class="sxs-lookup"><span data-stu-id="4f242-109">Project Operations on Dataverse</span></span>


| <span data-ttu-id="4f242-110">**기능 영역**</span><span class="sxs-lookup"><span data-stu-id="4f242-110">**Feature area**</span></span> | <span data-ttu-id="4f242-111">**참조 번호**</span><span class="sxs-lookup"><span data-stu-id="4f242-111">**Reference number**</span></span> | <span data-ttu-id="4f242-112">**품질 업데이트**</span><span class="sxs-lookup"><span data-stu-id="4f242-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4f242-113">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="4f242-113">Billing and pricing</span></span> | <span data-ttu-id="4f242-114">2133873</span><span class="sxs-lookup"><span data-stu-id="4f242-114">2133873</span></span> | <span data-ttu-id="4f242-115">**경비 추정** 그리드의 **단위 판매 가격** 통화 기호의 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-115">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="4f242-116">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="4f242-116">Billing and pricing</span></span> | <span data-ttu-id="4f242-117">2174616</span><span class="sxs-lookup"><span data-stu-id="4f242-117">2174616</span></span> | <span data-ttu-id="4f242-118">견적이 성공되면 견적에서 복사된 계약 내용 세부 사항에서 계약 사용자 정의 가격표가 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-118">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="4f242-119">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="4f242-119">Opportunity Management</span></span> | <span data-ttu-id="4f242-120">2167475</span><span class="sxs-lookup"><span data-stu-id="4f242-120">2167475</span></span> | <span data-ttu-id="4f242-121">청구되지 않은 실제 입력이 발생한 수정 송장의 세액이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-121">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="4f242-122">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="4f242-122">Opportunity Management</span></span> | <span data-ttu-id="4f242-123">2176285</span><span class="sxs-lookup"><span data-stu-id="4f242-123">2176285</span></span> | <span data-ttu-id="4f242-124">판매 계약/견적 라인 상세 내역에서 원가 계약/견적 라인 상세 내역으로 세액을 복사할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-124">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="4f242-125">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="4f242-125">Opportunity Management</span></span> | <span data-ttu-id="4f242-126">2188079</span><span class="sxs-lookup"><span data-stu-id="4f242-126">2188079</span></span> | <span data-ttu-id="4f242-127">작업 기반이 아닌 계약에 대해서는 분할 청구 규칙을 생성하면 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-127">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="4f242-128">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="4f242-128">Planning and Tracking</span></span> | <span data-ttu-id="4f242-129">2125274</span><span class="sxs-lookup"><span data-stu-id="4f242-129">2125274</span></span> | <span data-ttu-id="4f242-130">**프로젝트 시작 날짜 매핑** 의 **프로젝트 이중 쓰기 맵** 특성이 **msdyn\_taskearlieststart** 에서 **msdyn\_actualstart** 로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-130">**Project Dual Write Map** attribute for **Project Start Date Mapping** updated from **msdyn\_taskearlieststart** to **msdyn\_actualstart**.</span></span> |
| <span data-ttu-id="4f242-131">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="4f242-131">Planning and Tracking</span></span> | <span data-ttu-id="4f242-132">2138853</span><span class="sxs-lookup"><span data-stu-id="4f242-132">2138853</span></span> | <span data-ttu-id="4f242-133">참조 작업이 대상 프로젝트에 복사되는 경비 추정 라인을 보장하기 위해 프로젝트 복사 기능이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-133">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="4f242-134">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="4f242-134">Planning and Tracking</span></span> | <span data-ttu-id="4f242-135">2154306</span><span class="sxs-lookup"><span data-stu-id="4f242-135">2154306</span></span> | <span data-ttu-id="4f242-136">Project Operations에서 리소스 기반 시나리오에 대한 경비 추정을 삭제하는 문제를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-136">Fixed issues with deleting expense estimates in Project Operations for resource-based scenarios.</span></span> |
| <span data-ttu-id="4f242-137">계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="4f242-137">Planning and Tracking</span></span> | <span data-ttu-id="4f242-138">2173259</span><span class="sxs-lookup"><span data-stu-id="4f242-138">2173259</span></span> | <span data-ttu-id="4f242-139">특정 시나리오에서 **WBS 복사** 오류 메시지를 표시하지 않도록 프로젝트 복사 기능이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-139">Project copy function updated to ensure it doesn't display **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="4f242-140">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="4f242-140">Time and Expense</span></span> | <span data-ttu-id="4f242-141">2148910</span><span class="sxs-lookup"><span data-stu-id="4f242-141">2148910</span></span> | <span data-ttu-id="4f242-142">**시간 항목** 그리드에서 **항목 편집** 페이지의 표시 문제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-142">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="4f242-143">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="4f242-143">Time and Expense</span></span> | <span data-ttu-id="4f242-144">2159798</span><span class="sxs-lookup"><span data-stu-id="4f242-144">2159798</span></span> | <span data-ttu-id="4f242-145">승인된 경비 항목을 편집할 수 없도록 제어를 강화했습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-145">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="4f242-146">Dynamics 365 Finance에서 프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="4f242-146">Project management and accounting on Dynamics 365 Finance</span></span>

<span data-ttu-id="4f242-147">자세한 내용은 [2021년 1월 새로운 기능 - 리소스/비 재고 기반 시나리오에 대한 Project Operations](whats-new-jan-2021-resource-based.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4f242-147">For more information, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="4f242-148">규제 업데이트</span><span class="sxs-lookup"><span data-stu-id="4f242-148">Regulatory updates</span></span>

<span data-ttu-id="4f242-149">Finance and Operations 앱의 규제 업데이트에 대한 정보는 [규제 업데이트](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4f242-149">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="4f242-150">규제 업데이트에 대해 배우는 또 다른 방법은 LCS에 로그인하고 문제 검색 도구를 사용하여 계획된 규제 업데이트를 보는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-150">Another way to learn about regulatory updates is to sign in to LCS and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="4f242-151">문제 검색을 사용하면 국가, 기능 유형 및 릴리스별로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f242-151">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
