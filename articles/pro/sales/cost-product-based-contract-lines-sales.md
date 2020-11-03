---
title: 원가 계산 제품 기반 계약 내용
description: 이 항목은 만들기에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080283"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="9b2d7-103">원가 계산 제품 기반 계약 내용</span><span class="sxs-lookup"><span data-stu-id="9b2d7-103">Costing product-based contract lines</span></span>

<span data-ttu-id="9b2d7-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="9b2d7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9b2d7-105">Dynamics 365 Project Operations의 제품 기반 계약 내용에는 다운스트림 수익성 계산을 위해 제품의 원가를 저장하는 **원가** 필드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="9b2d7-106">카탈로그 제품에 대한 제품 기반 계약 내용이 생성되면 제품 기반 계약 내용의 비용은 기본적으로 제품 카탈로그의 **표준 비용** 필드에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="9b2d7-107">제품 카탈로그의 **표준 비용** 필드는 조직의 기본 통화로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="9b2d7-108">단가가 계약 내용에서 기본값으로 설정되면 계약의 판매 통화로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="9b2d7-109">제품 기반 계약 내용의 단가</span><span class="sxs-lookup"><span data-stu-id="9b2d7-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="9b2d7-110">제품 기반 계약 내용에 단가가 있으면 단가 판매마다 다른 제품 비용이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="9b2d7-111">항상 필요한 것은 아니지만 공급자가 고객을 위해 제품 비용을 할인할 수 있는 특정 시나리오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="9b2d7-112">다음 시나리오를 살펴 보십시오.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-112">Consider the following scenario:</span></span>

<span data-ttu-id="9b2d7-113">Fabrikam Robotics는 Adatum Corporation의 조립 라인에 로봇 팔을 설치하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="9b2d7-114">Fabrikam은 설치 서비스를 제공하지만 로봇 팔은 Trey Research에서 조달합니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="9b2d7-115">Adatum Corporation의 로봇 팔 설치로 Trey Research를 위한 새로운 산업 분야가 열리면 Trey는 Fabrikam에 이 거래에 대해 특별 할인을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="9b2d7-116">이 경우 Fabrikam은 Robotic Arms에 대한 제품 기반 계약 내용을 만들고 Trey Research의 로봇 팔 표준 비용과 다른 이 계약의 단위당 비용을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
