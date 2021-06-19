---
title: 재무 차원 기본값
description: 이 항목은 재무 차원 기본값을 설정하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013314"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="f9fbf-103">재무 차원 기본값</span><span class="sxs-lookup"><span data-stu-id="f9fbf-103">Financial dimension defaults</span></span>

<span data-ttu-id="f9fbf-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f9fbf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f9fbf-105">Dynamics 365 Project Operations는 Dynamics 365 Finance의 [재무 차원](/dynamics365/finance/general-ledger/financial-dimensions) 프레임 워크를 사용하여 프로젝트 보조 원장 및 총계정 원장 트랜잭션에 대한 추가 통찰력을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="f9fbf-106">기본 재무 차원은 고객, 프로젝트 자금 출처, 중요 시점, 프로젝트 계약 내용 또는 프로젝트에서 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="f9fbf-107">고객에 대한 기본 재무 차원 정의</span><span class="sxs-lookup"><span data-stu-id="f9fbf-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="f9fbf-108">고객 차원 기본값은 Finance에 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="f9fbf-109">차원 기본값을 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="f9fbf-110">**수취 계정** > **고객** > **모든 고객** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="f9fbf-111">**고객** 페이지의 **재무 차원** 탭에서 특정 고객에 대한 재무 차원 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="f9fbf-112">프로젝트 계약에 대한 기본 재무 차원 정의</span><span class="sxs-lookup"><span data-stu-id="f9fbf-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="f9fbf-113">프로젝트 계약은 Common Data Service(CDS)에서 생성되고 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="f9fbf-114">프로젝트 계약에 대한 회계 특성은 Finance의 **프로젝트 관리 및 회계** 모듈에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="f9fbf-115">프로젝트 자금 출처에 대한 재무 차원 설정</span><span class="sxs-lookup"><span data-stu-id="f9fbf-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="f9fbf-116">**프로젝트 관리 및 회계** > **프로젝트** > **프로젝트 계약** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="f9fbf-117">업데이트할 레코드를 선택하고 **프로젝트 계약** 탭에서 **기본 회계 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="f9fbf-118">**관련 정보** 를 확장하고 **자금 출처** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="f9fbf-119">재무 차원 기본값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="f9fbf-120">재무 차원의 기본값은 고객 계정에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="f9fbf-121">프로젝트 계약 내용에 대한 재무 차원 설정</span><span class="sxs-lookup"><span data-stu-id="f9fbf-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="f9fbf-122">**프로젝트 관리 및 회계** > **프로젝트** > **프로젝트 계약** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="f9fbf-123">업데이트할 레코드를 선택하고 **프로젝트 계약** 탭에서 **기본 회계 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="f9fbf-124">**관련 정보** 를 확장하고 **계약 내용** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="f9fbf-125">재무 차원 기본값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="f9fbf-126">재무 차원 기본값이 적용 가능하며 고정 가격(중요 시점) 계약 내용에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="f9fbf-127">이러한 기본값은 관련 프로젝트 미적용 거래 및 송장 라인에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="f9fbf-128">프로젝트에 대한 기본 재무 차원 정의</span><span class="sxs-lookup"><span data-stu-id="f9fbf-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="f9fbf-129">프로젝트는 CDS에서 생성되고 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="f9fbf-130">프로젝트에 대한 회계 특성은 Finance의 **프로젝트 관리 및 회계** 모듈에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="f9fbf-131">**프로젝트 관리 및 회계** > **프로젝트** > **모든 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="f9fbf-132">업데이트할 레코드를 선택하고 **프로젝트** 탭에서 **기본 회계 표시** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="f9fbf-133">**관련 정보** 를 확장하고 **설정** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="f9fbf-134">재무 차원 기본값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="f9fbf-135">재무 차원의 기본값은 고객 계정에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="f9fbf-136">프로젝트가 여러 프로젝트 계약 고객이 있는 계약 내용과 연결된 경우 기본 고객이 재무 차원의 기본값에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="f9fbf-137">프로젝트 기본 재무 차원은 **Project Operations 통합 분개장** 및 관련 프로젝트 송장 라인에서 시간, 경비 및 요금 트랜잭션에 대한 분개장 항목 기본값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9fbf-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]