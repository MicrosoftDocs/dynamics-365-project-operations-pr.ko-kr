---
title: 기본 가격표
description: 이 항목은 Project Operations에서 기본 판매 및 원가 가격표에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd29a3fc9c873d46dd66a05ad100c7515177d6cd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130946"
---
# <a name="default-price-lists"></a><span data-ttu-id="8faa6-103">기본 가격표</span><span class="sxs-lookup"><span data-stu-id="8faa6-103">Default price lists</span></span>

<span data-ttu-id="8faa6-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="8faa6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="sales-price-lists"></a><span data-ttu-id="8faa6-105">판매 가격표</span><span class="sxs-lookup"><span data-stu-id="8faa6-105">Sales price lists</span></span>

<span data-ttu-id="8faa6-106">Dynamics 365 Project Operations의 모든 프로젝트 견적 및 계약에는 기본 판매 가격표가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-106">Every project quote and contract in Dynamics 365 Project Operations contains a default sales price list.</span></span> 

### <a name="price-list-default-on-project-quotes"></a><span data-ttu-id="8faa6-107">프로젝트 견적에 대한 기본 가격표</span><span class="sxs-lookup"><span data-stu-id="8faa6-107">Price list default on project quotes</span></span>
<span data-ttu-id="8faa6-108">시스템은 다음 프로세스를 완료하여 프로젝트 견적에서 기본값으로 사용할 가격표를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-108">The system completes the following process to determine which price list to default on a project quote:</span></span>

1. <span data-ttu-id="8faa6-109">시스템은 계정의 프로젝트 가격표에 첨부된 가격표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-109">The system looks at the price lists that are attached to the account's project price lists.</span></span> 
2. <span data-ttu-id="8faa6-110">계정 레코드에 첨부된 프로젝트 가격표가 있는 경우 시스템은 프로젝트 견적의 통화와 일치하는 프로젝트 매개 변수에 첨부된 판매 가격표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-110">If there are project price lists attached to the account record, the system looks at the sales price lists attached to the project parameters that match the currency of the project quote.</span></span>
3. <span data-ttu-id="8faa6-111">다음으로, 시스템은 프로젝트 견적의 날짜 범위와 일치하는 가격표의 날짜 유효성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-111">Next, the system checks the date effectivity of the price lists that match the date range of the project quote.</span></span> <span data-ttu-id="8faa6-112">특히 견적이 생성된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-112">Specifically, the date the quote was created.</span></span>
4. <span data-ttu-id="8faa6-113">프로젝트 견적 날짜에 유효한 가격표가 여러 개 있는 경우 모든 가격표가 프로젝트 견적에 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-113">If there are multiple price lists that are effective for the date of the project quote, all of the price lists default on the project quote.</span></span>
5. <span data-ttu-id="8faa6-114">프로젝트 견적 날짜에 유효한 가격표가 없는 경우 프로젝트 견적에 기본 프로젝트 가격표가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-114">If no price lists in effect for the date of the project quote, there's no default project price list on the project quote.</span></span> <span data-ttu-id="8faa6-115">프로젝트 견적에 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-115">A warning message will occur on the project quote.</span></span> <span data-ttu-id="8faa6-116">이 메시지는 첨부된 프로젝트 가격표가 없기 때문에 프로젝트에 대한 실제 및 예상 가격이 책정되지 않는다는 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-116">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

### <a name="price-list-default-on-project-contracts"></a><span data-ttu-id="8faa6-117">프로젝트 계약에 대한 기본 가격표</span><span class="sxs-lookup"><span data-stu-id="8faa6-117">Price list default on project contracts</span></span> 
<span data-ttu-id="8faa6-118">시스템은 다음 프로세스를 완료하여 프로젝트 계약에서 기본값으로 사용할 가격표를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-118">The system completes the following process to determine which price list to default on a project contract:</span></span>

1. <span data-ttu-id="8faa6-119">견적에서 계약이 생성된 경우 견적의 프로젝트 가격표가 별도로 복사되어 프로젝트 계약에 첨부됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-119">If the contract is created from a quote, the project price lists on the quote are copied over separately and attached to the project contract.</span></span>
2. <span data-ttu-id="8faa6-120">계약이 처음부터 생성된 경우 시스템은 계정의 프로젝트 가격표에 첨부된 가격표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-120">If the contract is created from scratch, the system looks at the price lists that are attached to the project price lists of the account.</span></span> <span data-ttu-id="8faa6-121">계정 레코드에 첨부된 프로젝트 가격표가 없는 경우 시스템은 프로젝트 계약의 통화와 일치하는 프로젝트 매개 변수에 첨부된 판매 가격표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-121">If there aren't project price lists attached to the account record, the system looks for sales price lists attached to the project parameters that match the currency of the project contract.</span></span>
4. <span data-ttu-id="8faa6-122">다음으로, 시스템은 프로젝트 계약의 날짜 범위와 일치하는 가격표의 날짜 유효성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-122">Next, the system checks the date effectivity of the price lists that match the date range of the project contract.</span></span> <span data-ttu-id="8faa6-123">특히 계약이 생성된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-123">Specifically, the date the contract was created.</span></span>
5. <span data-ttu-id="8faa6-124">계약 날짜에 유효한 가격표가 여러 개 있는 경우 모든 가격표가 프로젝트 계약에 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-124">If there are multiple price lists that are effective for the date of the contract, all of the price lists default on the contract.</span></span>
6. <span data-ttu-id="8faa6-125">계약 날짜에 유효한 가격표가 없는 경우 계약에 기본 프로젝트 가격표가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-125">If there are no price lists in effect for the date of the contract, no project price lists default to the contract.</span></span> <span data-ttu-id="8faa6-126">프로젝트 계약에 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-126">A warning message will occur on the project contract.</span></span> <span data-ttu-id="8faa6-127">이 메시지는 첨부된 프로젝트 가격표가 없기 때문에 프로젝트에 대한 실제 및 예상 가격이 책정되지 않는다는 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-127">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

## <a name="cost-price-lists"></a><span data-ttu-id="8faa6-128">원가표</span><span class="sxs-lookup"><span data-stu-id="8faa6-128">Cost price lists</span></span>

<span data-ttu-id="8faa6-129">원가표는 Project Operations의 엔터티로 기본 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-129">Cost price lists don't default to any entity in Project Operations.</span></span> <span data-ttu-id="8faa6-130">프로젝트 비용에 사용할 원가표를 결정하는 것은 항상 즉시 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-130">Determining the cost price list to use for project costs is always done in the moment.</span></span> <span data-ttu-id="8faa6-131">시스템은 다음 프로세스를 완료하여 프로젝트 비용에 사용할 가격표를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-131">The system completes the following process to determine which price list to use for project costs:</span></span>

1. <span data-ttu-id="8faa6-132">시스템은 먼저 프로젝트의 계약 조직 단위에 첨부된 가격표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-132">The system first looks at the price lists that are attached to the contracting organization unit of the project.</span></span>
2. <span data-ttu-id="8faa6-133">그런 다음 시스템은 들어오는 추정 또는 실제 라인의 날짜와 일치하는 가격표의 날짜 유효성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-133">The system then looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> <span data-ttu-id="8faa6-134">이러한 상황에서 *추정 라인* 은 Project Operations에서 추정의 세 가지 컨텍스트를 모두 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-134">In this situation, *estimate line* refers to all three contexts of estimation in Project Operations:</span></span>

    - <span data-ttu-id="8faa6-135">프로젝트 추정 라인</span><span class="sxs-lookup"><span data-stu-id="8faa6-135">Project estimate line</span></span>
    - <span data-ttu-id="8faa6-136">견적 라인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="8faa6-136">Quote line detail</span></span>
    - <span data-ttu-id="8faa6-137">계약 라인 상세 내역</span><span class="sxs-lookup"><span data-stu-id="8faa6-137">Contract line detail</span></span>
  
3. <span data-ttu-id="8faa6-138">들어오는 추정 또는 실제 날짜에 유효한 가격표가 여러 개 있는 경우 가장 최근에 생성된 가격표가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-138">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
4. <span data-ttu-id="8faa6-139">프로젝트의 계약 조직 단위에 첨부된 가격표가 없는 경우 시스템은 프로젝트 통화와 일치하는 프로젝트 매개 변수에 첨부된 원가표를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-139">If there no price lists attached to the contracting organization unit of the project, the system looks at cost price lists attached to project parameters that match the currency of the project.</span></span>
5. <span data-ttu-id="8faa6-140">그런 다음 시스템은 들어오는 추정 또는 실제 라인의 날짜와 일치하는 가격표의 날짜 유효성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-140">Next the system looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> 
6. <span data-ttu-id="8faa6-141">들어오는 추정 또는 실제 날짜에 유효한 가격표가 여러 개 있는 경우 가장 최근에 생성된 가격표가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-141">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
7. <span data-ttu-id="8faa6-142">통화 및 유효 날짜와 일치하는 프로젝트 매개 변수에 첨부된 원가표가 없는 경우 시스템은 들어오는 추정 또는 실제 라인에서 비용 요금을 기본적으로 0으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8faa6-142">If there are no cost price lists attached to the project parameters that match the currency and effective date, the system defaults the cost rate to zero (0) on the incoming estimate or actual line.</span></span>
