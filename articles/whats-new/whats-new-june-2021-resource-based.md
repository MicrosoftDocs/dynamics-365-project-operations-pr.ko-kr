---
title: 새로운 기능 2021년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 2021년 6월 Project Operations에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293145"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="db93a-103">새로운 기능 2021년 6월 - 리소스/비 재고 기반 시나리오에 대한 Project Operations</span><span class="sxs-lookup"><span data-stu-id="db93a-103">What's new June 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="db93a-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="db93a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="db93a-105">이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="db93a-106">Dynamics 365 Dataverse 환경 버전 4.11.0.156 또는 4.11.0.164의 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="db93a-106">Project Operations on Dynamics 365 Dataverse environment version 4.11.0.156 or 4.11.0.164.</span></span>
- <span data-ttu-id="db93a-107">Finance and Operations 앱 환경 버전 10.0.19의 프로젝트 관리 및 회계.</span><span class="sxs-lookup"><span data-stu-id="db93a-107">Project management and accounting in Finance and Operations apps environments version 10.0.19.</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="db93a-108">이 릴리스에 포함된 기능</span><span class="sxs-lookup"><span data-stu-id="db93a-108">Features included in this release</span></span>

<span data-ttu-id="db93a-109">이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-109">The following features are included in this release:</span></span>

- <span data-ttu-id="db93a-110">[조정 시나리오에 대한 프로젝트 송장 제안 라인](../invoicing/correct-project-invoice-proposals.md) 삭제 기능.</span><span class="sxs-lookup"><span data-stu-id="db93a-110">Ability to delete [Project invoice proposal lines for adjustment scenarios](../invoicing/correct-project-invoice-proposals.md).</span></span>
- <span data-ttu-id="db93a-111">항목별 경비 라인은 경비 보고서 [경비 보고서 재구상된 새로운 기능](../expense/expense-reports-reimagined.md#new-features)의 하위 범주 이름을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-111">Itemized expense lines reflect subcategory names in the expense report [Expense Reports Reimagined-New Features](../expense/expense-reports-reimagined.md#new-features).</span></span>
- <span data-ttu-id="db93a-112">새 경비를 생성할 때 새 경비 창에서 결제 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-112">Payment method is available in the new expense pane when creating a new expense.</span></span>

## <a name="project-operations-dual-write-maps-updates"></a><span data-ttu-id="db93a-113">Project Operations 이중 쓰기 맵 업데이트</span><span class="sxs-lookup"><span data-stu-id="db93a-113">Project Operations dual-write maps updates</span></span>

<span data-ttu-id="db93a-114">이 릴리스에는 Project Operations 이중 쓰기 맵에 대한 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-114">There are no updates for Project Operations dual-write maps in this release.</span></span> 

<span data-ttu-id="db93a-115">Project Operations 이중 쓰기 맵의 현재 목록 및 버전은 [Project Operations 이중 쓰기 맵 버전](../environment/resource-dual-write-maps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="db93a-115">For a current list and versions of Project Operations dual-write maps, see [Project Operations dual-write map versions](../environment/resource-dual-write-maps.md).</span></span>

<span data-ttu-id="db93a-116">Project Operations Dataverse 솔루션 및 Finance and Operations 앱 솔루션 버전을 업데이트할 때 환경에서 맵의 최신 버전을 실행하고 모든 관련 테이블 맵을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-116">Always run the latest version of the map in your environment and enable all related table maps as you update your Project Operations Dataverse solution and Finance and Operations apps solution version.</span></span> <span data-ttu-id="db93a-117">맵의 최신 버전이 활성화되지 않은 경우 특정 기능이 제대로 작동하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-117">Certain features and capabilities might not work correctly if the latest version of the map isn't activated.</span></span> <span data-ttu-id="db93a-118">**버전** 열의 **이중 쓰기** 페이지에서 활성 버전의 맵을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-118">You can see the active version of the map on the **Dual-write** page in the **Version** column.</span></span> <span data-ttu-id="db93a-119">**테이블 맵 버전** 을 선택하고 최신 버전을 선택한 다음 선택한 버전을 저장하여 맵의 새 버전을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-119">Activate a new version of the map by selecting **Table map versions**, selecting the latest version, and then saving the selected version.</span></span> <span data-ttu-id="db93a-120">기본 테이블 맵을 사용자 정의한 경우 변경 사항을 다시 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-120">If you have customized an out-of-the-box table map, reapply the changes.</span></span> <span data-ttu-id="db93a-121">자세한 내용은 [응용 프로그램 수명 주기 관리](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="db93a-121">For more information, see [Application lifecycle management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).</span></span>

<span data-ttu-id="db93a-122">지도를 시작하는 데 문제가 발생하면 이중 쓰기 문제 해결 가이드의 [지도에서 테이블 열 누락 문제](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) 섹션의 지침을 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="db93a-122">If you encounter an issue starting the map, follow the instructions in the [Missing table columns issue on maps](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) section of the Dual-write troubleshooting guide.</span></span>

## <a name="quality-updates"></a><span data-ttu-id="db93a-123">품질 업데이트</span><span class="sxs-lookup"><span data-stu-id="db93a-123">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="db93a-124">Dataverse의 Project Operations</span><span class="sxs-lookup"><span data-stu-id="db93a-124">Project Operations on Dataverse</span></span>

| <span data-ttu-id="db93a-125">**기능 영역**</span><span class="sxs-lookup"><span data-stu-id="db93a-125">**Feature area**</span></span> | <span data-ttu-id="db93a-126">**참조 번호**</span><span class="sxs-lookup"><span data-stu-id="db93a-126">**Reference number**</span></span> | <span data-ttu-id="db93a-127">**품질 업데이트**</span><span class="sxs-lookup"><span data-stu-id="db93a-127">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db93a-128">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="db93a-128">Billing and Pricing</span></span> | <span data-ttu-id="db93a-129">2281417</span><span class="sxs-lookup"><span data-stu-id="db93a-129">2281417</span></span> | <span data-ttu-id="db93a-130">송장 일정을 통한 송장 자동 생성 동작이 실패하는 현상이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-130">Fixed the issue regarding the failure of the automatic invoice creation action through the invoice schedule.</span></span> |
| <span data-ttu-id="db93a-131">청구 및 가격 책정</span><span class="sxs-lookup"><span data-stu-id="db93a-131">Billing and Pricing</span></span> | <span data-ttu-id="db93a-132">2287835</span><span class="sxs-lookup"><span data-stu-id="db93a-132">2287835</span></span> | <span data-ttu-id="db93a-133">송장 확인 성능이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-133">Improved invoice confirmation performance.</span></span> |
| <span data-ttu-id="db93a-134">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="db93a-134">Opportunity Management</span></span> | <span data-ttu-id="db93a-135">2222555</span><span class="sxs-lookup"><span data-stu-id="db93a-135">2222555</span></span> | <span data-ttu-id="db93a-136">자재 견적 청구 가능성에서 **프로젝트 견적에서 가져오기** 를 사용할 때 견적 라인 상세내역에 올바르게 복사해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-136">Material estimates chargeability must be correctly copied to quote line details when using **Import from Project Estimation**.</span></span> |
| <span data-ttu-id="db93a-137">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="db93a-137">Opportunity Management</span></span> | <span data-ttu-id="db93a-138">2223427</span><span class="sxs-lookup"><span data-stu-id="db93a-138">2223427</span></span> | <span data-ttu-id="db93a-139">이제 **GenerateRetainersFromRetainerScheduleOptions** 작업에 대한 사용자 정의가 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-139">Customizations are now allowed for the action, **GenerateRetainersFromRetainerScheduleOptions**.</span></span> |
| <span data-ttu-id="db93a-140">영업 기회 관리</span><span class="sxs-lookup"><span data-stu-id="db93a-140">Opportunity Management</span></span> | <span data-ttu-id="db93a-141">2277528</span><span class="sxs-lookup"><span data-stu-id="db93a-141">2277528</span></span> | <span data-ttu-id="db93a-142">여러 고객이 있는 프로젝트 계약 내용에 대한 고정 청구 중요 시점 값 계산.</span><span class="sxs-lookup"><span data-stu-id="db93a-142">Fixed billing milestone value calculation for project contract lines with multiple customers.</span></span> |
| <span data-ttu-id="db93a-143">프로젝트 계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="db93a-143">Project Planning and Tracking</span></span> | <span data-ttu-id="db93a-144">2226110</span><span class="sxs-lookup"><span data-stu-id="db93a-144">2226110</span></span> | <span data-ttu-id="db93a-145">**프로젝트 팀** 그리드의 **요구사항 생성** 기능과 관련된 간헐적인 문제를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-145">Fixed the intermittent issue with the **Generate Requirement** function in the **Project team** grid.</span></span> |
| <span data-ttu-id="db93a-146">프로젝트 계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="db93a-146">Project Planning and Tracking</span></span> | <span data-ttu-id="db93a-147">2208109</span><span class="sxs-lookup"><span data-stu-id="db93a-147">2208109</span></span> | <span data-ttu-id="db93a-148">사용자는 다른 통화의 관련 작업과 함께 한 통화로 프로젝트를 생성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-148">Users can't create a project in one currency with related tasks in another currency.</span></span> |
| <span data-ttu-id="db93a-149">프로젝트 계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="db93a-149">Project Planning and Tracking</span></span> | <span data-ttu-id="db93a-150">2258228</span><span class="sxs-lookup"><span data-stu-id="db93a-150">2258228</span></span> | <span data-ttu-id="db93a-151">일정 API를 사용하여 **일정** 항목으로 수정할 수 있는 필드 목록이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-151">The list of fields allowed to modify with **Scheduling** entities using the Schedule API has been updated.</span></span> |
| <span data-ttu-id="db93a-152">프로젝트 계획 및 추적</span><span class="sxs-lookup"><span data-stu-id="db93a-152">Project Planning and Tracking</span></span> | <span data-ttu-id="db93a-153">2293989</span><span class="sxs-lookup"><span data-stu-id="db93a-153">2293989</span></span> | <span data-ttu-id="db93a-154">올바른 언어 및 지역 설정이 **프로젝트 작업** 그리드에 전달되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-154">The correct language and regional settings must be passed to the **Project Tasks** grid.</span></span> |
| <span data-ttu-id="db93a-155">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="db93a-155">Resource Management</span></span> | <span data-ttu-id="db93a-156">2220493</span><span class="sxs-lookup"><span data-stu-id="db93a-156">2220493</span></span> | <span data-ttu-id="db93a-157">리소스 요청을 완료로 빠르게 표시할 때 **작업** 그리드의 사용자 경험을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-157">Fixed the user experience in the **Task** grid when quickly marking a resource request as complete.</span></span> |
| <span data-ttu-id="db93a-158">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="db93a-158">Resource Management</span></span> | <span data-ttu-id="db93a-159">2330496</span><span class="sxs-lookup"><span data-stu-id="db93a-159">2330496</span></span> | <span data-ttu-id="db93a-160">**일정 게시판** 로딩 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-160">Fixed the **Schedule Board** loading issue.</span></span> <span data-ttu-id="db93a-161">(품질 업데이트는 4.11.0.164 버전에서 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="db93a-161">(Quality update is available in version 4.11.0.164)</span></span> |
| <span data-ttu-id="db93a-162">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-162">Time and Expense</span></span> | <span data-ttu-id="db93a-163">2194431</span><span class="sxs-lookup"><span data-stu-id="db93a-163">2194431</span></span> | <span data-ttu-id="db93a-164">**시간 항목** 그리드는 **시스템 설정** 에 설정된 그 주의 시작을 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-164">The **Time entry** grid must honor the start of the week as set in the **System settings**.</span></span> |
| <span data-ttu-id="db93a-165">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-165">Time and Expense</span></span> | <span data-ttu-id="db93a-166">2277311</span><span class="sxs-lookup"><span data-stu-id="db93a-166">2277311</span></span> | <span data-ttu-id="db93a-167">**시간 항목** 그리드의 셀에서 값을 삭제한 후에도 커서는 그리드에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-167">After you delete the value in a cell in the **Time entry** grid, the cursor remains in the grid.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="db93a-168">Dynamics 365 Finance에서 프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-168">Project management and accounting on Dynamics 365 Finance</span></span>

| <span data-ttu-id="db93a-169">기능 영역</span><span class="sxs-lookup"><span data-stu-id="db93a-169">Feature area</span></span> | <span data-ttu-id="db93a-170">참조 번호</span><span class="sxs-lookup"><span data-stu-id="db93a-170">Reference number</span></span> | <span data-ttu-id="db93a-171">품질 업데이트</span><span class="sxs-lookup"><span data-stu-id="db93a-171">Quality update</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db93a-172">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-172">Project management and accounting</span></span> | [<span data-ttu-id="db93a-173">552976</span><span class="sxs-lookup"><span data-stu-id="db93a-173">552976</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | <span data-ttu-id="db93a-174">**양식 메모** 및 **양식 설정** 은 Project Operations와 통합된 Finance 법인의 **프로젝트 관리 설정** 아래에 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-174">**Form notes** and **Form setup** isn't visible under **Project management setup** in Finance legal entities that are integrated with Project Operations.</span></span> |
| <span data-ttu-id="db93a-175">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-175">Project management and accounting</span></span> | [<span data-ttu-id="db93a-176">527970</span><span class="sxs-lookup"><span data-stu-id="db93a-176">527970</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | <span data-ttu-id="db93a-177">프로젝트 송장 바우처에 대한 **전기 유형** = **판매세** 인 경우 VAT에 대한 기본 설명은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-177">The default description for VAT is blank when the **Posting type** = **Sales tax** for project invoice vouchers.</span></span> |
| <span data-ttu-id="db93a-178">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-178">Project management and accounting</span></span> | [<span data-ttu-id="db93a-179">565089</span><span class="sxs-lookup"><span data-stu-id="db93a-179">565089</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | <span data-ttu-id="db93a-180">Project Operations 통합과 함께 Dataverse에서 작업 기반 청구가 사용되는 경우 이중 트랜잭션이 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-180">Double transactions are posted when task-based billing is used in Dataverse with Project Operations integration.</span></span> |
| <span data-ttu-id="db93a-181">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-181">Project management and accounting</span></span> | [<span data-ttu-id="db93a-182">566869</span><span class="sxs-lookup"><span data-stu-id="db93a-182">566869</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | <span data-ttu-id="db93a-183">Project Operations 통합을 사용하는 동안 수익 인식 완료율이 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-183">The percentage complete in revenue recognition is incorrect while using Project Operations integration.</span></span> |
| <span data-ttu-id="db93a-184">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-184">Project management and accounting</span></span> | [<span data-ttu-id="db93a-185">568107</span><span class="sxs-lookup"><span data-stu-id="db93a-185">568107</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | <span data-ttu-id="db93a-186">Project Operations 통합 시나리오에서 보류 중인 공급업체 송장에 대해 수익 발생이 두 배가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-186">Revenue accrual is doubled on a pending vendor invoice in a Project Operations integrated scenario.</span></span> |
| <span data-ttu-id="db93a-187">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-187">Project management and accounting</span></span> | [<span data-ttu-id="db93a-188">572370</span><span class="sxs-lookup"><span data-stu-id="db93a-188">572370</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | <span data-ttu-id="db93a-189">수익 프로필 규칙이 **그룹** 설정으로 설정된 경우 통합 저널을 게시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-189">Unable to post the integration journal when the revenue profile rule is set to **Group** setup.</span></span> |
| <span data-ttu-id="db93a-190">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-190">Project management and accounting</span></span> | [<span data-ttu-id="db93a-191">573596</span><span class="sxs-lookup"><span data-stu-id="db93a-191">573596</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | <span data-ttu-id="db93a-192">여러 측정 단위가 있는 라인이 있는 프로젝트 구매 발주에 대해서는 구매 송장을 전기할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-192">A purchase invoice can't be posted for project purchase orders that have lines with multiple units of measure.</span></span> |
| <span data-ttu-id="db93a-193">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-193">Project management and accounting</span></span> | [<span data-ttu-id="db93a-194">573637</span><span class="sxs-lookup"><span data-stu-id="db93a-194">573637</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | <span data-ttu-id="db93a-195">프로젝트의 기본 재무 차원은 프로젝트 **V2** 데이터 항목을 사용하여 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-195">The default financial dimension on a project can't be updated using the projects **V2** data entity.</span></span> |
| <span data-ttu-id="db93a-196">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-196">Project management and accounting</span></span> | [<span data-ttu-id="db93a-197">577211</span><span class="sxs-lookup"><span data-stu-id="db93a-197">577211</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | <span data-ttu-id="db93a-198">프로젝트 견적을 생성하기 위한 일괄 처리 프로세스를 완료하는 데 너무 오래 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-198">The batch process to create project estimates takes too long to complete.</span></span> |
| <span data-ttu-id="db93a-199">프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="db93a-199">Project management and accounting</span></span> | [<span data-ttu-id="db93a-200">582329</span><span class="sxs-lookup"><span data-stu-id="db93a-200">582329</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | <span data-ttu-id="db93a-201">계약을 삭제하면 고객과 연결된 주소도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-201">Deleting a contract also deletes the address associated with the customer.</span></span> |
| <span data-ttu-id="db93a-202">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-202">Travel and expense</span></span> | [<span data-ttu-id="db93a-203">514930</span><span class="sxs-lookup"><span data-stu-id="db93a-203">514930</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | <span data-ttu-id="db93a-204">경비 보고서 승인 워크플로 조건이 올바르게 평가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-204">The expense report approval workflow condition isn't evaluated correctly.</span></span> |
| <span data-ttu-id="db93a-205">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-205">Travel and expense</span></span> | [<span data-ttu-id="db93a-206">519304</span><span class="sxs-lookup"><span data-stu-id="db93a-206">519304</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | <span data-ttu-id="db93a-207">경비 보고서 정책이 프로젝트 ID를 올바르게 평가하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-207">The expense report policy isn't correctly evaluating the project ID.</span></span> |
| <span data-ttu-id="db93a-208">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-208">Travel and expense</span></span> | [<span data-ttu-id="db93a-209">522463</span><span class="sxs-lookup"><span data-stu-id="db93a-209">522463</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | <span data-ttu-id="db93a-210">**본지사 경비 트랜잭션을 위해 개인으로 분할** 작업이 제대로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-210">The action, **Split to personal for intercompany expense transactions** isn't working correctly.</span></span> |
| <span data-ttu-id="db93a-211">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-211">Travel and expense</span></span> | [<span data-ttu-id="db93a-212">534702</span><span class="sxs-lookup"><span data-stu-id="db93a-212">534702</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | <span data-ttu-id="db93a-213">특정 출장 요청이 삭제되면 경비 보고서 라인 근거가 실수로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-213">Expense report line justifications are accidentally deleted when certain travel requisitions are deleted.</span></span> <span data-ttu-id="db93a-214">경비 보고서의 recID와 이동 요청서가 동일한 경우에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-214">This occurs when the recID of the expense report and the travel requisition are the same.</span></span> |
| <span data-ttu-id="db93a-215">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-215">Travel and expense</span></span> | [<span data-ttu-id="db93a-216">544368</span><span class="sxs-lookup"><span data-stu-id="db93a-216">544368</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | <span data-ttu-id="db93a-217">경비 보고서 정책에 **프로젝트 ID** 필드가 필요한 경우 경비 모바일 앱에 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-217">There is an issue in the Expense mobile app when the **Project ID** field is required in expense report policies.</span></span> |
| <span data-ttu-id="db93a-218">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-218">Travel and expense</span></span> | [<span data-ttu-id="db93a-219">545331</span><span class="sxs-lookup"><span data-stu-id="db93a-219">545331</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | <span data-ttu-id="db93a-220">프로젝트와 연결된 본지사 비용은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-220">Intercompany expenses that are associated with a project can't be edited.</span></span> <span data-ttu-id="db93a-221">대신 "개체 참조가 개체의 인스턴스로 설정되지 않았습니다."라는 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-221">Instead, the following error message displays, "Object reference not set to an instance of an object."</span></span> |
| <span data-ttu-id="db93a-222">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-222">Travel and expense</span></span> | [<span data-ttu-id="db93a-223">548659</span><span class="sxs-lookup"><span data-stu-id="db93a-223">548659</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | <span data-ttu-id="db93a-224">경비 보고서가 전기된 후 은행 보조원장에 잘못된 통화와 금액이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-224">After the expense report is posted, the wrong currency and amount is listed in the bank subledger.</span></span> |
| <span data-ttu-id="db93a-225">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-225">Travel and expense</span></span> | [<span data-ttu-id="db93a-226">558336</span><span class="sxs-lookup"><span data-stu-id="db93a-226">558336</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | <span data-ttu-id="db93a-227">*신용카드 트랜잭션 삭제* 기능이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-227">Improvements have been made to the *Delete credit card transactions* feature.</span></span>  |
| <span data-ttu-id="db93a-228">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-228">Travel and expense</span></span> | [<span data-ttu-id="db93a-229">525070</span><span class="sxs-lookup"><span data-stu-id="db93a-229">525070</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | <span data-ttu-id="db93a-230">경비 보고서에 포함된 판매세는 법인에서 다른 보고 통화가 지정된 경우 일관되게 계산되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-230">Sales tax included in an expense report isn't consistently calculated when a different reporting currency is specified in a legal entity.</span></span> |
| <span data-ttu-id="db93a-231">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-231">Travel and expense</span></span> | [<span data-ttu-id="db93a-232">527779</span><span class="sxs-lookup"><span data-stu-id="db93a-232">527779</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | <span data-ttu-id="db93a-233">새로운 현금 여행 경비를 추가하면 성능이 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-233">Performance is impacted when adding a new cash travel expense.</span></span> |
| <span data-ttu-id="db93a-234">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-234">Travel and expense</span></span> | [<span data-ttu-id="db93a-235">537841</span><span class="sxs-lookup"><span data-stu-id="db93a-235">537841</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | <span data-ttu-id="db93a-236">경비 정책 규칙은 경비 보고서에서 트리거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-236">Expense policy rules aren't triggered on an expense report.</span></span> |
| <span data-ttu-id="db93a-237">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-237">Travel and expense</span></span> | [<span data-ttu-id="db93a-238">566386</span><span class="sxs-lookup"><span data-stu-id="db93a-238">566386</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | <span data-ttu-id="db93a-239">데이터 관리 프레임워크를 사용하여 새 공유 범주를 업로드하면 모든 공유 범주에 대한 모든 하위 범주가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-239">Uploading a new shared category by using the Data Management Framework removes all subcategories for all shared categories.</span></span> |
| <span data-ttu-id="db93a-240">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-240">Travel and expense</span></span> | [<span data-ttu-id="db93a-241">574131</span><span class="sxs-lookup"><span data-stu-id="db93a-241">574131</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | <span data-ttu-id="db93a-242">경비 라인을 생성한 다음 범주를 선택하면 "판매세 그룹 DOM과 품목 판매세 그룹 STD의 조합이 유효하지 않습니다."라는 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-242">When you create an expense line and then select a category, the following error message displays, "The combination of Sales tax group DOM and item sales tax group STD is not valid."</span></span> |
| <span data-ttu-id="db93a-243">이동 및 경비</span><span class="sxs-lookup"><span data-stu-id="db93a-243">Travel and expense</span></span> | [<span data-ttu-id="db93a-244">574900</span><span class="sxs-lookup"><span data-stu-id="db93a-244">574900</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | <span data-ttu-id="db93a-245">경비 모바일 애플리케이션에 동기화 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db93a-245">There are synchronization issues in the Expense mobile application.</span></span> |