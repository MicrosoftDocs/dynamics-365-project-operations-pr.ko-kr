---
title: 카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트
description: 이 항목은 제품 카탈로그의 항목에 대한 비용 및 판매율을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764563"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="026f6-103">카탈로그 제품에 대한 비용 및 판매율 설정 - 라이트</span><span class="sxs-lookup"><span data-stu-id="026f6-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="026f6-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="026f6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="026f6-105">Dynamics 365 Project Operations의 제품 카탈로그 항목에 대한 가격 산정 설정은 Dynamics 365 Sales와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="026f6-106">Project Operations에서는 제품을 추정하거나 프로젝트에 사용할 수 없으므로 견적 및 계약을 위해 제품 카탈로그 가격을 프로젝트 가격 목록에 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="026f6-107">견적, 계약 또는 계정의 **제품 가격** 필드를 사용하여 제품 카탈로그 가격을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="026f6-108">프로젝트 가격 목록에서 제품 카탈로그 가격을 설정하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="026f6-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="026f6-109">프로젝트 가격표는 Project Operations에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="026f6-110">응용 프로그램별 비즈니스 로직은 견적에서 계약으로 가격 목록을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="026f6-111">결과는 계약별 프로젝트 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="026f6-112">견적서의 프로젝트 가격표가 너무 커지면 복사 작업으로 인해 견적 획득 프로세스가 지연될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="026f6-113">제품 가격표는 계약에 대한 사용자 지정 가격표를 만들기 위해 복사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="026f6-114">복사가 필요하지 않기 때문에 견적 프로세스의 성능에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="026f6-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
