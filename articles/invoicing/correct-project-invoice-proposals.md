---
title: 프로젝트 송장 제안서 초안에 대한 올바른 회계
description: 이 항목에서는 송장 제안서 초안에서 회계 관련 정보를 조정하는 방법을 설명합니다.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251240"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="ed706-103">프로젝트 송장 제안서 초안에 대한 올바른 회계</span><span class="sxs-lookup"><span data-stu-id="ed706-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="ed706-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ed706-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ed706-105">프로젝트 송장의 *운영 세부 정보* 는 견적 송장에서 프로젝트 관리자가 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="ed706-106">이러한 세부 정보에는 송장을 발행해야 하는 시간, 경비, 재료 또는 이정표, 요율, 선지급 및 유지 금액의 적용에 대한 결정이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="ed706-107">원래 견적 송장을 확인한 후 [수정 견적 송장](../proforma-invoicing/corrective-invoices.md)을 만들고 확인하여 운영 세부정보를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="ed706-108">프로젝트 송장의 *회계 세부 정보* 는 고객 대면 송장 문서에서 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="ed706-109">이러한 세부 정보에는 송장에 적용되는 판매세 계산 및 재무 차원이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="ed706-110">이 항목에서는 초안 프로젝트 송장 제안서에서 이러한 회계 세부 정보를 조정하는 방법에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="ed706-111">판매세 조정</span><span class="sxs-lookup"><span data-stu-id="ed706-111">Adjust sales tax</span></span>

<span data-ttu-id="ed706-112">기본 청구 판매세 그룹 및 품목 판매세 그룹은 송장 제안 문서에서 직접 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="ed706-113">이러한 그룹을 조정하려면 **편집** 을 선택한 다음 각 프로젝트 송장 제안 라인에서 **판매세 그룹** 또는 **품목 판매세 그룹** 필드에 새 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="ed706-114">재무 차원 조정</span><span class="sxs-lookup"><span data-stu-id="ed706-114">Adjust financial dimensions</span></span>

<span data-ttu-id="ed706-115">재무 차원은 프로젝트 송장 제안 라인에서 직접 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="ed706-116">대신 다음 단계에 따라 프로젝트 송장 제안서의 재무 차원을 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="ed706-117">프로젝트 송장 제안서에서 **모두 삭제** 를 선택하여 프로젝트 송장 제안 라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed706-118">**모두 삭제** 버튼은 시스템 관리자가 **기능 관리** 작업 공간에서 **자원 기반/비 재고 시나리오에 대한 Project Operations 사용 시 송장 제안 라인 삭제** 기능을 활성화한 후에만 사용할 수 있습니다. .</span><span class="sxs-lookup"><span data-stu-id="ed706-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="ed706-119">재무 차원 조정:</span><span class="sxs-lookup"><span data-stu-id="ed706-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="ed706-120">**계정입금 거래(청구 중요 시점):** **모든 프로젝트** \> **관리** \> **계정입금 거래** 로 이동하고 조정이 필요한 중요 시점을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="ed706-121">그런 다음 **재무 차원** 탭에서 필요에 따라 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="ed706-122">**시간, 경비 및 자재 거래:** **게시된 프로젝트 트랜잭션** 페이지에서 **회계 조정** 을 선택하여 재무 차원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="ed706-123">재무 차원 값 조정을 완료한 후 **프로젝트 관리 및 회계** \> **주기적** \> **Project Operations 통합** 으로 이동하고 주기적 프로세스를 실행하려면 **준비 테이블에서 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="ed706-124">이 프로세스는 업데이트된 재무 차원 값을 사용하여 프로젝트 송장 제안 라인을 다시 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="ed706-125">업데이트된 값은 프로젝트 송장이 전기될 때 프로젝트 보조원장과 총계정원장에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed706-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
