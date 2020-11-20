---
title: 카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트
description: 이 항목은 제품 카탈로그의 항목에 대한 비용 및 판매율을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176709"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="fa2ee-103">카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트</span><span class="sxs-lookup"><span data-stu-id="fa2ee-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="fa2ee-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="fa2ee-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fa2ee-105">Dynamics 365 Project Operations의 제품 카탈로그 항목에 대한 가격 설정은 Dynamics 365 Sales에서와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="fa2ee-106">Project Operations의 프로젝트에서 제품을 추정하거나 사용할 수 없기 때문에 견적 및 계약을 위해 프로젝트 가격표에 제품 카탈로그 가격을 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="fa2ee-107">제품 카탈로그 가격은 견적, 계약 또는 계정의 **제품 가격** 필드에서 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="fa2ee-108">이러한 엔터티의 프로젝트 가격표에서 제품 카탈로그 가격을 설정하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="fa2ee-109">프로젝트 가격표는 Project Operations에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="fa2ee-110">견적에서 계약으로 가격표를 복사하는 응용 프로그램별 비즈니스 로직이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="fa2ee-111">결과는 계약별 프로젝트 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="fa2ee-112">견적서의 프로젝트 가격표가 너무 커지면 복사 작업으로 인해 견적 획득 프로세스가 지연될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="fa2ee-113">제품 가격표는 계약에 대한 사용자 지정 가격표를 만들기 위해 복사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="fa2ee-114">이는 제품 가격표가 견적 획득 프로세스의 성능에 영향을 미치지 않음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
