---
title: 제품 기반 영업 기회 라인
description: 이 항목에서는 Project Operations의 제품 기반 영업 기회 항목에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079978"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="83854-103">제품 기반 영업 기회 라인</span><span class="sxs-lookup"><span data-stu-id="83854-103">Product-based opportunity lines</span></span>

<span data-ttu-id="83854-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="83854-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="83854-105">제품 기반 영업 기회 라인은 영업 기회의 라인 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="83854-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="83854-106">이러한 라인은 다른 부가가치 서비스 없이 최종 송장의 개별 라인 항목으로 고객에게 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="83854-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="83854-107">관련 지출 및 소비는 관련 프로젝트의 작업에서 추적되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83854-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="83854-108">제품 기반 라인은 카탈로그 항목 또는 기록 제품일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83854-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="83854-109">영업 기회의 제품 기반 라인에 있는 대부분의 기능은 Dynamics 365 Sales 응용 프로그램에서 제공하는 기능을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="83854-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="83854-110">제품 기반 영업 기회 라인에 대한 자세한 내용은 [영업 기회에 제품 추가](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="83854-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="83854-111">프로젝트 기반 영업 기회에 특정한 제품 기반 영업 기회 라인에 대한 한 가지 개념은 **고객 예산** 입니다.</span><span class="sxs-lookup"><span data-stu-id="83854-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="83854-112">이 필드를 사용하여 고객이 광고 항목에 대해 지불할 금액을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="83854-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="83854-113">영업 기회 요약의 수익 방법이 **시스템 계산** 으로 설정된 경우, 제품 및 프로젝트 기반 라인의 고객 예산 값이 요약되어 예상 수익을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="83854-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
