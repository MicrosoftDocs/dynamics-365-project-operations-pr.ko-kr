---
title: 회사 간 송장 개요
description: 이 토픽은 프로젝트에 대한 회사 간 송장에 대한 정보와 예를 제공합니다.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287336"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="e7861-103">회사 간 송장 개요</span><span class="sxs-lookup"><span data-stu-id="e7861-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="e7861-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e7861-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e7861-105">조직에 프로젝트를 위해 제품과 서비스를 서로 이전하는 여러 부서, 자회사 및 기타 법인이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="e7861-106">서비스 또는 제품을 제공하는 법인을 *대출 법인* 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="e7861-107">서비스 또는 제품을 받는 법인을 *차용 법인* 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="e7861-108">다음 그림은 Contoso Robotics USA(차용 법인)와 Contoso Robotics UK(대출 법인)라는 두 법인이 리소스를 공유하여 고객에게 프로젝트 인 Adventure Works를 제공하는 일반적인 시나리오를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="e7861-109">이 시나리오에서 Contoso Robotics USA는 Adventure Works에 작업을 제공하도록 계약을 맺었습니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![회사 간 송장](./media/IntercompanyScenario.png) 

<span data-ttu-id="e7861-111">Dynamics 365 Project Operations는 다음 흐름을 사용하여 회사 간 트랜잭션을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="e7861-112">대출 법인의 리소스는 차용 법인의 프로젝트에 대한 예약 시간 및 경비를 통해 회사 간 시간 또는 비용 트랜잭션을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="e7861-113">시간 및 경비 비용은 차용 회사의 단위 비용 가격표를 사용하여 대출 회사에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="e7861-114">회사 간 미청구 판매 트랜잭션은 차용 회사의 단위 비용 가격표를 사용하여 대출 회사에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="e7861-115">미 청구 수익은 프로젝트 계약 판매 가격표를 사용하여 차용 회사에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="e7861-116">미 청구 수익이 기록되면 고객에게 청구될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="e7861-117">고객은 회사 간 송장 처리가 완료될 때까지 기다릴 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="e7861-118">회사 간 고객 송장은 대출 회사에서 정기적으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="e7861-119">송장은 수동으로 또는 정기적인 자동화 프로세스를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="e7861-120">각 차용 법인에 대해 단일 송장을 생성하거나 프로젝트별로 별도의 송장을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="e7861-121">회사 간 고객 송장이 대출 법인에 전기되면 해당 보류 공급업체 송장이 차용 법인에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="e7861-122">보류 중인 공급업체 송장의 원가는 송장이 전기될 때 프로젝트 보조 원장에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="e7861-123">다음 다이어그램은 회계 이벤트 및 총계정 원장에 대한 예상 전기와 관련된 회사 간 송장을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7861-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![회사 간 흐름](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="e7861-125">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="e7861-125">Additional resources</span></span>

- [<span data-ttu-id="e7861-126">회사 간 송장 구성</span><span class="sxs-lookup"><span data-stu-id="e7861-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="e7861-127">회사 간 트랜잭션 기록</span><span class="sxs-lookup"><span data-stu-id="e7861-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="e7861-128">회사 간 고객 및 공급업체 송장 만들기</span><span class="sxs-lookup"><span data-stu-id="e7861-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]