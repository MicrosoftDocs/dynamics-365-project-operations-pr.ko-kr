---
title: 송장 처리 개요
description: 이 토픽은 리소스/비 재고 기반 시나리오에 대해 Project Operations에서 송장 발부 프로세스 개요를 제공합니다.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369024"
---
# <a name="invoicing-process-overview"></a><span data-ttu-id="6b5ed-103">송장 처리 개요</span><span class="sxs-lookup"><span data-stu-id="6b5ed-103">Invoicing process overview</span></span>

<span data-ttu-id="6b5ed-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6b5ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6b5ed-105">리소스/비 재고 기반 시나리오를 위한 Project Operations는 프로젝트 관리자와 쉬치 계정 담당자/프로젝트 회계사 모두의 요구에 맞게 조정된 포괄적인 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-105">Project Operations for resource/non-stocked based scenarios offers comprehensive capabilities tailored to fit the needs of both Project manager and Accounts receivable clerk/project accountant.</span></span> <span data-ttu-id="6b5ed-106">송장 발부 프로세스의 경우 프로젝트 관리자가 프로젝트 청구 백 로그를 관리하고 수취 계정 담당자/프로젝트 회계사는 규정을 준수하고 정확한 고객 대면 송장 문서를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-106">For the invoicing process, the Project manager manages the project billing backlog and the Accounts receivable clerk/project accountant creates a compliant and accurate customer-facing invoice document.</span></span>

![송장 발부 흐름 다이어그램](./media/invoicing-flow.png)

<span data-ttu-id="6b5ed-108">프로젝트 계약 내용은 연관된 프로젝트 트랜잭션에 대한 청구 방법을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-108">The project contract line defines the billing method for associated project transactions.</span></span> <span data-ttu-id="6b5ed-109">프로젝트 관리자가 시간 및 비용 거래를 승인하면 시스템은 **프로젝트 실제** 엔터니에 트랜잭션을 기록하고 Dynamics 365 Finance의 **프로젝트 관리 및 회계** 모듈로 정보를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-109">When the Project manager approves time and expense transactions, the system records the transactions in the **Project Actuals** entity and sends the information to the **Project management and accounting** module in Dynamics 365 Finance.</span></span> <span data-ttu-id="6b5ed-110">그런 다음 프로젝트 회계사는 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 레코드를 검토하고 전기합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-110">The Project accountant then reviews and posts the records using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="6b5ed-111">이 분개장에는 청구, 판매세 그룹, 청구 항목 판매세 그룹 및 재무 차원과 같은 실제 프로젝트에 대한 중요한 회계 세부 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-111">This journal includes important accounting details for project actuals, such as billing, sales tax group, billing item sales tax group, and financial dimensions.</span></span>

<span data-ttu-id="6b5ed-112">프로젝트 관리자는 [시간 및 자재 청구 백 로그](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)에서 시간 및 재료 청구 방법 및 [고정 가격 중요 시점](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)에서 고정 가격 청구를 사용하여 청구되지 않은 판매 거래를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-112">The Project manager can review unbilled sales transactions using the time and material billing method in the [Time and material billing backlog](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) and fixed price billing in [Fixed price milestones](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones).</span></span> <span data-ttu-id="6b5ed-113">이러한 보기를 사용하면 다음 결제 주기에 포함해야 하는 트랜잭션을 필터링하고 선택한 다음 **송장 발부 준비 완료** 로 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-113">These views allow you to filter and select transactions that need to be included in the next billing cycle and then mark them as **Ready to Invoice**.</span></span>

<span data-ttu-id="6b5ed-114">[수동으로 견적 프로젝트 송장을 만들거나](../proforma-invoicing/create-manual-proforma-invoice.md) 또는 [정기적 프로세스](../proforma-invoicing/configure-automated-invoice-creation.md)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-114">You can [manually create a proforma invoice](../proforma-invoicing/create-manual-proforma-invoice.md) or use a [periodic process](../proforma-invoicing/configure-automated-invoice-creation.md).</span></span> <span data-ttu-id="6b5ed-115">프로젝트 관리자는 필요에 따라 [견적 송장 초안을 조정](../proforma-invoicing/manage-proforma-invoice.md)한 다음 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-115">The Project manager can [adjust a draft proforma invoice](../proforma-invoicing/manage-proforma-invoice.md) as needed and then confirm it.</span></span>

<span data-ttu-id="6b5ed-116">확인된 견적 송장은 Finance에서 **프로젝트 관리 및 회계** 모듈로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-116">The confirmed proforma invoice is sent to the **Project management and accounting** module in Finance.</span></span> <span data-ttu-id="6b5ed-117">프로젝트 회계사는 프로젝트 송장 제안서의 서식을 지정하고 업데이트한 다음 문서를 전기하고 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-117">The Project accountant formats and updates the project invoice proposal, and then posts and prints the document.</span></span> <span data-ttu-id="6b5ed-118">전기된 프로젝트 송장은 총계정 원장과 고객 및 프로젝트 보조 원장에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b5ed-118">Posted project invoices are recorded in the General ledger, as well as the Customer and Project subledgers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]