---
title: 프로젝트 및 프로젝트 계약에 대한 청구서 백로그 검토
description: 이 항목은 시간, 비용 및 제품 백로그를 검토하는 방법과 청구서를 사용할 준비가 된 것으로 표시하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008544"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="5e8f8-103">프로젝트 및 프로젝트 계약에 대한 청구서 백로그 검토</span><span class="sxs-lookup"><span data-stu-id="5e8f8-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5e8f8-104">청구서를 생성 및 처리하도록 트랜잭션이 준비되면 트랜잭션이 **청구서 발행 준비** 로 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="5e8f8-105">이 항목은 만들 수 있는 트랜잭션의 타입을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="5e8f8-106">시간 및 자재 대금 청구 백로그 검토</span><span class="sxs-lookup"><span data-stu-id="5e8f8-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="5e8f8-107">프로젝트에 대한 시간 또는 비용 항목이 제출되고 승인되면 PSA는 프로젝트 실제값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="5e8f8-108">프로젝트와 트랜잭션 클래스의 조합이 시간 및 자재 프로젝트의 계약 행에 매핑되면 항목이 승인될 때 두 개의 실제값이 만들어집니다:</span><span class="sxs-lookup"><span data-stu-id="5e8f8-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="5e8f8-109">비용 실제값</span><span class="sxs-lookup"><span data-stu-id="5e8f8-109">Cost actual</span></span> 
- <span data-ttu-id="5e8f8-110">미청구 매출액 실제값</span><span class="sxs-lookup"><span data-stu-id="5e8f8-110">Unbilled sales actual</span></span>

<span data-ttu-id="5e8f8-111">미청구 매출액 실제값은 청구 백로그를 나타내며, 청구 상태를 **청구서 발행 준비** 로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="5e8f8-112">프로젝트 청구서를 만들 때 **청구서 발행 준비** 로 표시되어 있는 미청구 판매 실제값이 청구서 행 내역으로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="5e8f8-113">시간 및 자재에 대한 청구 백로그를 검토하려면 **판매** \> **청구** \> **시간 및 자재 청구 백로그** 로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="5e8f8-114">청구서 발행 준비된 미청구 판매 실제값을 모두 선택한 다음, **청구서 발행 준비** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="5e8f8-115">이러한 실제값의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![시간 및 자재 대금 청구 백로그](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="5e8f8-117">제품 대금 청구 백로그 검토</span><span class="sxs-lookup"><span data-stu-id="5e8f8-117">Review the product billing backlog</span></span>

<span data-ttu-id="5e8f8-118">PSA에서는 프로젝트 계약에 제품 기반 계약 행이 있는 경우 해당 행은 프로젝트 계약에 대한 청구서가 작성될 때마다 청구서 발행으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="5e8f8-119">**청구서 발행 준비** 로 표시된 계약 행이 있는 제품은 프로젝트 청구서 행으로서 프로젝트 청구서에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="5e8f8-120">제품에 대한 청구 백로그를 검토하려면 **판매** \> **청구** \> **제품 대금 청구 백로그** 로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="5e8f8-121">청구서 발행 준비된 제품 기반 계약 행을 모두 선택한 다음, **청구서 발행 준비** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="5e8f8-122">이러한 행의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![제품 대금 청구 백로그](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="5e8f8-124">고정 가격 계약의 청구 이정표 검토</span><span class="sxs-lookup"><span data-stu-id="5e8f8-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="5e8f8-125">고정 가격 청구 방법이 있는 각 프로젝트 계약 행은 계약 이정표를 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="5e8f8-126">이러한 계약 이정표는 **청구서 발행 준비** 로 표시된 경우에만 청구서를 발행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="5e8f8-127">청구 이정표를 검토하려면 **판매** \> **청구** \> **고정 가격 이정표** 로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="5e8f8-128">청구서 발행 준비된 이정표를 선택한 다음, **청구서 발행 준비** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="5e8f8-129">이러한 이정표의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e8f8-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![고정 가격 이정표](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]