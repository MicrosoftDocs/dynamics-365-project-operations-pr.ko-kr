---
title: 재구상된 경비 보고서
description: 이 항목은 경비 보고서 항목을 위해 재설계되고 재구상된 환경에 대한 정보를 제공합니다.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 47c1bce0c886897b295a3c1a355f4db843c4b73a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080118"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="921fb-103">재구상된 경비 보고서</span><span class="sxs-lookup"><span data-stu-id="921fb-103">Expense reports reimagined</span></span>

<span data-ttu-id="921fb-104">경비 보고서 항목은 프로세스를 단순화하고 보고서를 완료하는 데 필요한 시간을 줄이기 위해 재설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="921fb-105">다음은 새로운 경비 경험의 주요 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="921fb-106">대리인의 경비에 액세스할 수 있는 새로운 경비 관리 작업 공간.</span><span class="sxs-lookup"><span data-stu-id="921fb-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="921fb-107">헤더 수준 영수증을 더 잘 표시하고 경비 라인에 영수증을 첨부하는 프로세스를 단순화하는 새로운 영수증 일치 환경.</span><span class="sxs-lookup"><span data-stu-id="921fb-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="921fb-108">더 많은 경비 라인과 추가 데이터 열을 볼 수 있는 새로운 읽기 전용 그리드.</span><span class="sxs-lookup"><span data-stu-id="921fb-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="921fb-109">이제 상위 경비와 함께 모든 항목별 및 분할 라인을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="921fb-110">경비 편집을 위한 단순화된 창.</span><span class="sxs-lookup"><span data-stu-id="921fb-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="921fb-111">문제에 대한 올바른 컨텍스트와 이해 및 해결 방법을 제공하기 위해 오류, 경고 및 정책 메시지를 재설계했습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="921fb-112">사용자가 작업을 완료하고 문제를 해결하기 전에 나타난 여러 메시지를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="921fb-113">필수 필드, 선택적 필드 및 포함하지 않아야 하는 필드를 지정하는 새 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="921fb-114">이 페이지는 설정해야 하는 필드 수를 줄이는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="921fb-115">보고서가 더 이상 회계사용으로 설계된 것처럼 보이지 않도록 경비 보고서의 새로운 모양과 느낌.</span><span class="sxs-lookup"><span data-stu-id="921fb-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="921fb-116">새로운 경험을 켜려면 **기능 관리** 작업 영역을 사용하여 **재구상된 경비 보고서** 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined** feature.</span></span> <span data-ttu-id="921fb-117">이 기능을 켜면 다음 동작이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="921fb-118">기존 경비 작업 영역이 새 작업 영역으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="921fb-119">경비 필드 가시성을 위한 새 메뉴 항목이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="921fb-120">경비 보고서(기존 페이지) 또는 경비 보고서 필드에 대한 기존 메뉴 항목이 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="921fb-121">워크플로 및 모든 승인은 여전히 기존 비용 보고서 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="921fb-122">새 사용자를 위한 시작 비디오</span><span class="sxs-lookup"><span data-stu-id="921fb-122">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="921fb-123">[Dynamics 365 for Finance and Operations의 경비 경험](https://youtu.be/Ocy-MsTvEE0) 비디오(위에 표시됨)는 YouTube에서 사용할 수 있는 [Finance and Operations 재생 목록](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)에 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-123">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="921fb-124">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="921fb-124">New features</span></span>

| <span data-ttu-id="921fb-125">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="921fb-125">New feature</span></span> | <span data-ttu-id="921fb-126">설명</span><span class="sxs-lookup"><span data-stu-id="921fb-126">Description</span></span> |
|---|----|
| <span data-ttu-id="921fb-127">경비 필드 가시성</span><span class="sxs-lookup"><span data-stu-id="921fb-127">Expense field visibility</span></span> | <span data-ttu-id="921fb-128">새로운 설정 페이지를 통해 조직에 대해 비활성화해야 하는 필드, 필수 필드 및 권장되는 필드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-128">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="921fb-129">필수 필드</span><span class="sxs-lookup"><span data-stu-id="921fb-129">Required fields</span></span> | <span data-ttu-id="921fb-130">새로운 간단한 구성을 사용하면 정책 프레임워크를 사용하지 않고도 필요한 일부 필드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-130">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="921fb-131">선택 필드</span><span class="sxs-lookup"><span data-stu-id="921fb-131">Optional fields</span></span> | <span data-ttu-id="921fb-132">선택적 필드에 대한 두 번째 페이지가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-132">A second page for optional fields is added.</span></span> <span data-ttu-id="921fb-133">이런 식으로 직원은 필드를 설정해야 하는 것처럼 느끼지 않지만 필드에 여전히 쉽게 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-133">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="921fb-134">첨부되지 않은 영수증 추가</span><span class="sxs-lookup"><span data-stu-id="921fb-134">Add unattached receipts</span></span> | <span data-ttu-id="921fb-135">첨부되지 않은 영수증을 경비 보고서에 추가하는 기능은 작업 영역과 경비 보고서에서 더 잘 보입니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-135">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="921fb-136">향상된 메시징</span><span class="sxs-lookup"><span data-stu-id="921fb-136">Improved messaging</span></span> | <span data-ttu-id="921fb-137">경고 또는 오류가 있는 경비 라인을 더 잘 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-137">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="921fb-138">메시지 표시줄의 메시지 감소</span><span class="sxs-lookup"><span data-stu-id="921fb-138">Reduction in messages in the message bar</span></span>| <span data-ttu-id="921fb-139">Infolog 메시지의 수가 줄어들고 많은 경우 중복 메시지가 나타나지 않도록 노력했습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-139">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="921fb-140">공통 작업을 함께 그룹화</span><span class="sxs-lookup"><span data-stu-id="921fb-140">Grouped together common actions</span></span> | <span data-ttu-id="921fb-141">인터페이스는 대부분의 일반적인 라인 수준 작업에 대한 새로운 작업 버튼 추가와 헤더 및 기타 덜 빈번한 작업에 대한 줄임표 버튼(...)을 추가하여 정리되었습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-141">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="921fb-142">가시성을 높이기 위한 새로운 작업 영역</span><span class="sxs-lookup"><span data-stu-id="921fb-142">New workspace to increase visibility</span></span> | <span data-ttu-id="921fb-143">새로운 작업 영역은 사용자가 다른 영역으로 이동할 수 있는 기능과 링크를 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-143">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="921fb-144">경비 생성 중 기존 경비 및 영수증 추가</span><span class="sxs-lookup"><span data-stu-id="921fb-144">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="921fb-145">경비 보고서를 작성할 때 모든 또는 선택한 경비 및 영수증을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-145">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="921fb-146">환율 계산기</span><span class="sxs-lookup"><span data-stu-id="921fb-146">Exchange rate calculator</span></span> | <span data-ttu-id="921fb-147">현금 다중 통화 트랜잭션에 대한 환율을 계산할 수 있는 환율 계산기가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-147">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="921fb-148">새 경비 라인 저장 및 추가</span><span class="sxs-lookup"><span data-stu-id="921fb-148">Save and add new expense lines</span></span> | <span data-ttu-id="921fb-149">**저장** 및 **새로 만들기** 버튼은 새 경비를 입력할 때 비용 라인을 빠르게 입력하기 위해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-149">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="921fb-150">분할 및 항목별 라인에 대한 더 나은 가시성</span><span class="sxs-lookup"><span data-stu-id="921fb-150">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="921fb-151">항목별 및 분할 라인이 경비 목록에 직접 추가되어 가시성을 높이고 오류가 있는지 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-151">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="921fb-152">항목화 중 영수증 표시</span><span class="sxs-lookup"><span data-stu-id="921fb-152">Show receipts during itemization</span></span> | <span data-ttu-id="921fb-153">항목화 중 영수증을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-153">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="921fb-154">초기 릴리스는 경비 항목 시나리오에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-154">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="921fb-155">모든 경비 보고서 검토 또는 승인 시나리오는 기존 경비 항목 페이지를 계속 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-155">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="921fb-156">다음 기능은 기존 페이지에 있지만 아직 새 페이지에는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-156">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="921fb-157">이러한 기능은 다음 몇 번의 릴리스에서 다시 도입됩니다.</span><span class="sxs-lookup"><span data-stu-id="921fb-157">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="921fb-158">승인</span><span class="sxs-lookup"><span data-stu-id="921fb-158">Approvals</span></span>
- <span data-ttu-id="921fb-159">지급 계정 승인 및 회계 편집 기능</span><span class="sxs-lookup"><span data-stu-id="921fb-159">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="921fb-160">여러 진입점</span><span class="sxs-lookup"><span data-stu-id="921fb-160">Multiple entry points</span></span>
- <span data-ttu-id="921fb-161">여행 요청 통합</span><span class="sxs-lookup"><span data-stu-id="921fb-161">Travel requisition integration</span></span>
- <span data-ttu-id="921fb-162">경비 필드 가시성을 위한 데이터 엔터티</span><span class="sxs-lookup"><span data-stu-id="921fb-162">Data entity for expense field visibility</span></span>
- <span data-ttu-id="921fb-163">일비 경비 항목</span><span class="sxs-lookup"><span data-stu-id="921fb-163">Entry for per-diem expenses</span></span>
- <span data-ttu-id="921fb-164">라인 수준 워크플로</span><span class="sxs-lookup"><span data-stu-id="921fb-164">Line-level workflow</span></span>
- <span data-ttu-id="921fb-165">임시 승인자 지원</span><span class="sxs-lookup"><span data-stu-id="921fb-165">Interim approver support</span></span>
- <span data-ttu-id="921fb-166">고급 항목화</span><span class="sxs-lookup"><span data-stu-id="921fb-166">Advanced itemization</span></span>
