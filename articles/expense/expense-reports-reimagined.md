---
title: 재구상된 경비 보고서
description: 이 항목은 경비 보고서 입력을 위해 재설계되고 재구상된 경험을 설명합니다.
author: suvaidya
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f8c44f86ff7c00e2d5b927bbe6878be7ab6d7758
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251012"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="f61f4-103">재구상된 경비 보고서</span><span class="sxs-lookup"><span data-stu-id="f61f4-103">Expense reports reimagined</span></span>

<span data-ttu-id="f61f4-104">경비 보고서 항목은 프로세스를 단순화하고 보고서를 완료하는 데 필요한 시간을 줄이기 위해 재설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="f61f4-105">다음은 새로운 경비 경험의 주요 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="f61f4-106">대리인의 경비에 액세스할 수 있는 새로운 경비 관리 작업 공간.</span><span class="sxs-lookup"><span data-stu-id="f61f4-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="f61f4-107">헤더 수준 영수증을 더 잘 표시하고 경비 라인에 영수증을 첨부하는 프로세스를 단순화하는 새로운 영수증 일치 환경.</span><span class="sxs-lookup"><span data-stu-id="f61f4-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="f61f4-108">더 많은 경비 라인과 기타 데이터 열을 볼 수 있는 새로운 읽기 전용 그리드입니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-108">A new read-only grid that lets you view many more expense lines and other columns of data.</span></span> <span data-ttu-id="f61f4-109">이제 상위 경비와 함께 모든 항목별 및 분할 라인을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="f61f4-110">경비 편집을 위한 단순화된 창.</span><span class="sxs-lookup"><span data-stu-id="f61f4-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="f61f4-111">문제에 대한 올바른 컨텍스트와 이해 및 해결 방법을 제공하기 위해 오류, 경고 및 정책 메시지를 재설계했습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="f61f4-112">사용자가 작업을 완료하고 문제를 해결하기 전에 나타난 여러 메시지를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="f61f4-113">필수 필드, 선택적 필드 및 포함하지 않아야 하는 필드를 지정하는 새 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="f61f4-114">이 페이지는 설정해야 하는 필드 수를 줄이는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="f61f4-115">보고서가 더 이상 회계사용으로 설계된 것처럼 보이지 않도록 경비 보고서의 새로운 모양과 느낌.</span><span class="sxs-lookup"><span data-stu-id="f61f4-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="f61f4-116">새 환경을 켜려면 **기능 관리** 작업 공간을 사용하여 **재구상된 경비 보고서 작업 공간** 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined workspace** feature.</span></span> <span data-ttu-id="f61f4-117">이 기능을 켜면 다음 동작이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="f61f4-118">기존 경비 작업 영역이 새 작업 영역으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="f61f4-119">경비 필드 가시성을 위한 새 메뉴 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="f61f4-120">경비 보고서(기존 페이지) 또는 경비 보고서 필드에 대한 기존 메뉴 항목이 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="f61f4-121">워크플로 및 모든 승인은 여전히 기존 비용 보고서 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a><span data-ttu-id="f61f4-122">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f61f4-122">New features</span></span>

| <span data-ttu-id="f61f4-123">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f61f4-123">New feature</span></span> | <span data-ttu-id="f61f4-124">설명</span><span class="sxs-lookup"><span data-stu-id="f61f4-124">Description</span></span> |
|---|----|
| <span data-ttu-id="f61f4-125">경비 필드 가시성</span><span class="sxs-lookup"><span data-stu-id="f61f4-125">Expense field visibility</span></span> | <span data-ttu-id="f61f4-126">새 설정 페이지에서 조직에 대해 비활성화해야 하는 필드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-126">A new setup page lets you specify which fields should be disabled for an organization.</span></span> <span data-ttu-id="f61f4-127">필수 필드와 권장 필드를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-127">You can also specify which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="f61f4-128">필수 필드</span><span class="sxs-lookup"><span data-stu-id="f61f4-128">Required fields</span></span> | <span data-ttu-id="f61f4-129">새로운 간단한 구성을 사용하면 정책 프레임워크를 사용하지 않고도 필요한 일부 필드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-129">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="f61f4-130">선택 필드</span><span class="sxs-lookup"><span data-stu-id="f61f4-130">Optional fields</span></span> | <span data-ttu-id="f61f4-131">선택적 필드에 대한 두 번째 페이지가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-131">A second page for optional fields is added.</span></span> <span data-ttu-id="f61f4-132">이런 식으로 직원은 필드를 설정해야 하는 것처럼 느끼지 않지만 필드에 여전히 쉽게 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-132">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="f61f4-133">첨부되지 않은 영수증 추가</span><span class="sxs-lookup"><span data-stu-id="f61f4-133">Add unattached receipts</span></span> | <span data-ttu-id="f61f4-134">첨부되지 않은 영수증을 경비 보고서에 추가하는 기능은 작업 영역과 경비 보고서에서 더 잘 보입니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-134">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="f61f4-135">향상된 메시징</span><span class="sxs-lookup"><span data-stu-id="f61f4-135">Improved messaging</span></span> | <span data-ttu-id="f61f4-136">경고 또는 오류가 있는 경비 라인을 더 잘 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-136">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="f61f4-137">메시지 표시줄의 메시지 감소</span><span class="sxs-lookup"><span data-stu-id="f61f4-137">Reduction in messages in the message bar</span></span>| <span data-ttu-id="f61f4-138">Infolog 메시지의 수가 줄어들고 많은 경우 중복 메시지가 나타나지 않도록 노력했습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-138">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="f61f4-139">공통 작업을 함께 그룹화</span><span class="sxs-lookup"><span data-stu-id="f61f4-139">Grouped together common actions</span></span> | <span data-ttu-id="f61f4-140">인터페이스는 대부분의 일반적인 라인 수준 작업에 대한 새로운 작업 버튼 추가와 헤더 및 기타 덜 빈번한 작업에 대한 줄임표 버튼(...)을 추가하여 정리되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-140">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="f61f4-141">가시성을 높이기 위한 새로운 작업 영역</span><span class="sxs-lookup"><span data-stu-id="f61f4-141">New workspace to increase visibility</span></span> | <span data-ttu-id="f61f4-142">새로운 작업 영역은 사용자가 다른 영역으로 이동할 수 있는 기능과 링크를 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-142">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="f61f4-143">경비 생성 중 기존 경비 및 영수증 추가</span><span class="sxs-lookup"><span data-stu-id="f61f4-143">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="f61f4-144">경비 보고서를 작성할 때 모든 경비를 추가하거나 첨부되지 않은 경비를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-144">When you create expense reports, you can add all expenses, or select unattached expenses.</span></span> <span data-ttu-id="f61f4-145">첨부되지 않은 경비는 회사 신용 카드 피드에서 가져온 경비 또는 사용자가 수동으로 생성했지만 경비 보고서에 첨부되지 않은 경비입니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-145">Unattached expenses are expenses that were imported from the corporate credit card feed or expenses that were manually created by the user but haven't been attached to an expense report.</span></span>|
| <span data-ttu-id="f61f4-146">환율 계산기</span><span class="sxs-lookup"><span data-stu-id="f61f4-146">Exchange rate calculator</span></span> | <span data-ttu-id="f61f4-147">현금 다중 통화 트랜잭션에 대한 환율을 계산할 수 있는 환율 계산기가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-147">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="f61f4-148">새 경비 라인 저장 및 추가</span><span class="sxs-lookup"><span data-stu-id="f61f4-148">Save and add new expense lines</span></span> | <span data-ttu-id="f61f4-149">**저장** 및 **새로 만들기** 버튼은 새 경비를 입력할 때 비용 라인을 빠르게 입력하기 위해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-149">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="f61f4-150">분할 및 항목별 라인에 대한 더 나은 가시성</span><span class="sxs-lookup"><span data-stu-id="f61f4-150">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="f61f4-151">항목별 및 분할 라인이 경비 목록에 직접 추가되어 가시성을 높이고 오류가 있는지 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-151">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="f61f4-152">항목별 라인에서 하위 범주 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f61f4-152">View subcategory details in itemized lines</span></span> | <span data-ttu-id="f61f4-153">상위 비용의 항목별 행은 경비 보고서의 하위 범주 레이블을 표시하므로 세부적인 세부 정보를 한 눈에 검토하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-153">Itemized lines of a parent expense show the subcategory labels in the expense report, which helps you to review the granular details at a glance.</span></span>|
| <span data-ttu-id="f61f4-154">항목화 중 영수증 표시</span><span class="sxs-lookup"><span data-stu-id="f61f4-154">Show receipts during itemization</span></span> | <span data-ttu-id="f61f4-155">항목화 중 영수증을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-155">Receipts can be shown during itemization.</span></span> |
| <span data-ttu-id="f61f4-156">현금 서비스 선택</span><span class="sxs-lookup"><span data-stu-id="f61f4-156">Cash advance selection</span></span> | <span data-ttu-id="f61f4-157">단일 경비 트랜잭션을 이행하기 위해 하나 이상의 현금 서비스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-157">Select one or more cash advances for fulfilling a single expense transaction.</span></span> |
| <span data-ttu-id="f61f4-158">현금 서비스 잔액</span><span class="sxs-lookup"><span data-stu-id="f61f4-158">Cash advance balance</span></span> | <span data-ttu-id="f61f4-159">승인 및 지급된 현금 서비스에 대한 경비 항목을 생성할 때 실시간으로 현금 서비스 잔액을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-159">Review the cash advance balance in real time when you create an expense entry against approved and paid cash advances.</span></span> |

<span data-ttu-id="f61f4-160">초기 릴리스는 경비 항목 시나리오에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-160">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="f61f4-161">모든 경비 보고서 검토 또는 승인 시나리오는 기존 경비 항목 페이지를 계속 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-161">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="f61f4-162">다음 기능은 재구상된 경비 보고서 작업 영역에서 지원되지 않지만 향후 릴리스에 대해 계획되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61f4-162">The following features aren't supported on the Expense reports reimagined workspace, but are planned for future releases:</span></span> 

- <span data-ttu-id="f61f4-163">여행 요청 통합</span><span class="sxs-lookup"><span data-stu-id="f61f4-163">Travel requisition integration</span></span>
- <span data-ttu-id="f61f4-164">일당 경비 입력</span><span class="sxs-lookup"><span data-stu-id="f61f4-164">Per diem expense entry</span></span>
- <span data-ttu-id="f61f4-165">임시 승인자 지원</span><span class="sxs-lookup"><span data-stu-id="f61f4-165">Interim approver support</span></span>
- <span data-ttu-id="f61f4-166">워크플로 기록을 보는 기능</span><span class="sxs-lookup"><span data-stu-id="f61f4-166">Ability to view workflow history</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
