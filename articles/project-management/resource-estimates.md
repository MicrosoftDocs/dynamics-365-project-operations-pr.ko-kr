---
title: 리소스 추정
description: 이 항목에서는 Project Operations에서 리소스 추정을 계산하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928584"
---
# <a name="resource-estimates"></a><span data-ttu-id="14f8e-103">리소스 추정</span><span class="sxs-lookup"><span data-stu-id="14f8e-103">Resource estimates</span></span>

<span data-ttu-id="14f8e-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="14f8e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="14f8e-105">리소스 추정은 적용 가능한 가격 책정 차원과 함께 작업 분할 구조에 정의된 시간별 작업량에서 비롯됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="14f8e-106">일반적으로 계산은 **역할 x 시간에 대한 속도/시간**입니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="14f8e-107">각 리소스에 대한 시간대별 작업량은 리소스 할당 레코드에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="14f8e-108">가격은 미리 정의된 가격표에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="14f8e-109">적용 가능한 가격표를 기준으로 단위 변환이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-109">Unit conversion is applied based on the applicable price list.</span></span>

![리소스 추정](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="14f8e-111">기본 원가 및 비용 통화</span><span class="sxs-lookup"><span data-stu-id="14f8e-111">Default cost price and cost currency</span></span>

<span data-ttu-id="14f8e-112">원가는 조직 구성 단위에서 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="14f8e-113">기본 청구 요금 및 판매 통화</span><span class="sxs-lookup"><span data-stu-id="14f8e-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="14f8e-114">판매 가격은 거래당 한 번 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="14f8e-115">판매 가격표 기본값을 위한 계층 구조는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="14f8e-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="14f8e-116">조직</span><span class="sxs-lookup"><span data-stu-id="14f8e-116">Organization</span></span>
2. <span data-ttu-id="14f8e-117">고객</span><span class="sxs-lookup"><span data-stu-id="14f8e-117">Customer</span></span>
3. <span data-ttu-id="14f8e-118">견적/계약</span><span class="sxs-lookup"><span data-stu-id="14f8e-118">Quote/contract</span></span>
