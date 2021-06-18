---
title: 프로젝트 송장 통합
description: 이 항목에서는 고객 송장에 대한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996574"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="d80a5-103">프로젝트 송장 통합</span><span class="sxs-lookup"><span data-stu-id="d80a5-103">Project invoice integration</span></span>

<span data-ttu-id="d80a5-104">이 항목에서는 고객 송장에 대한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="d80a5-105">Project Operations에서 프로젝트 관리자는 프로젝트 청구 백로그를 관리하고 Microsoft Dataverse에서 고객에 대한 견적 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="d80a5-106">이 견적 송장을 기반으로 수취 계정 담당자 또는 프로젝트 회계사가 고객 대면 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="d80a5-107">이중 쓰기 통합을 통해 견적 송장 세부 정보가 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="d80a5-108">고객 대면 송장이 전기된 후 시스템은 Dataverse의 관련 프로젝트 실적을 회계 세부 사항으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="d80a5-109">다음 그래픽은 이 통합에 대한 개략적인 개념적 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![프로젝트 송장 통합](./media/DW5Invoicing.png)

<span data-ttu-id="d80a5-111">프로젝트 관리자가 Dataverse에서 견적 송장을 확인하면 견적 송장 헤더 정보가 이중 쓰기 테이블 맵인 **프로젝트 송장 제안 V2(송장)** 를 사용하여 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="d80a5-112">Dataverse에서 Finance and Operations 앱으로의 단방향 통합입니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="d80a5-113">Finance and Operations 앱에서 직접 프로젝트 송장 제안을 생성하거나 삭제하는 것은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="d80a5-114">Dataverse의 송장 확인은 비즈니스 로직을 트리거하여 **실제** 엔터티에 청구 관련 레코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="d80a5-115">이러한 레코드는 이중 쓰기 테이블 맵, **Project Operations 통합 실제(msdyn\_actuals)** 를 사용하여 Finance and Operations에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="d80a5-116">자세한 내용은 [프로젝트 추정 및 실제](resource-dual-write-estimates-actuals.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d80a5-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="d80a5-117">프로젝트 송장 제안 라인은 주기적인 프로세스인 **준비에서 가져오기** 에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="d80a5-118">이 프로세스는 **실제 준비** 테이블의 청구된 판매 실제 세부 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d80a5-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="d80a5-119">자세한 내용은 [프로젝트 송장 제안 관리](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d80a5-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
