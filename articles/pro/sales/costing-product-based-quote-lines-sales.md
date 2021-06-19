---
title: 원가 계산 제품 기반 견적 라인
description: 이 항목에서는 제품 기반 견적 라인에 원가를 적용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003459"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="77dd4-103">원가 계산 제품 기반 견적 라인</span><span class="sxs-lookup"><span data-stu-id="77dd4-103">Costing product-based quote lines</span></span>

<span data-ttu-id="77dd4-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="77dd4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="77dd4-105">Dynamics 365 Project Operations의 제품 기반 견적 라인에는 **가격표** 필드도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="77dd4-106">이 필드는 견적 라인에서 제품의 원가를 추적하고 다운스트림 수익성 계산을 위해 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="77dd4-107">카탈로그 제품에 대한 제품 기반 견적 라인이 생성되면 제품 기반 견적 라인의 비용은 기본적으로 제품 카탈로그의 **표준 비용** 필드에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="77dd4-108">제품 카탈로그의 표준 비용 필드는 조직의 기본 통화로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="77dd4-109">제품 기반 견적 라인의 기본 단가는 견적의 판매 통화로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="77dd4-110">제품 기반 견적 라인의 단가</span><span class="sxs-lookup"><span data-stu-id="77dd4-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="77dd4-111">제품 기반 견적 라인에 단가를 지정하는 목적은 각 판매를 위한 제품에 대해 서로 다른 비용을 허용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="77dd4-112">이것은 일반적인 시나리오는 아니지만 때때로 최종 판매 고객에 따라 공급자가 제품 비용을 할인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="77dd4-113">예: </span><span class="sxs-lookup"><span data-stu-id="77dd4-113">For example:</span></span>

<span data-ttu-id="77dd4-114">Fabrikam Robotics는 A Datum Corporation의 조립 라인에 로봇 팔을 설치하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="77dd4-115">Fabrikam은 설치 서비스를 제공하지만 로봇 팔은 Trey 로봇에서 조달합니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="77dd4-116">A Datum Corporation의 로봇 팔 설치로 Trey의 로봇 팔에 대한 새로운 산업 분야가 열리면 Trey는 Fabrikam에 이 거래에 대해 특별 할인을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="77dd4-117">이 경우 Fabrikam은 Robotic Arms에 대한 제품 기반 견적 라인을 만들고이 견적에 대한 특별 단가를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="77dd4-118">이 비용은 Trey Robotic Arms의 표준 비용과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="77dd4-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]