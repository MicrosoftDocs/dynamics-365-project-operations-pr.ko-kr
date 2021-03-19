---
title: 가격 책정 차원의 Project Operations 필드
description: 이 토픽은 필드를 Dynamics 365 Project Operations의 가격 책정 차원으로 사용하는 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274646"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="a922b-103">가격 책정 차원의 Project Operations 필드</span><span class="sxs-lookup"><span data-stu-id="a922b-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="a922b-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="a922b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a922b-105">**실제** 엔터티에는 리소스 기반 가격 책정에 대한 가격 책정 차원으로 사용할 수 있는 많은 필드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="a922b-106">예를 들어, 하나의 공통 필드가 **예약 가능한 리소스** 입니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a922b-107">청구 가능한 리소스가 20~30개 미만인 소규모 기업은 각 리소스에 특정한 청구서 및 비용 요율을 갖는 것이 더 간단한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a922b-108">그러나 청구 가능한 인력이 증가함에 따라 리소스 보안 요율은 유지하기가 비현실적이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="a922b-109">리소스가 승진하거나 더 많은 경험을 얻거나 다른 기술을 습득함에 따라 리소스 비용 및 청구 요금이 달라지기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="a922b-110">또 다른 예는 처리 카테고리의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-110">Another example is that of transaction category.</span></span> <span data-ttu-id="a922b-111">고객과 구현자는 처리 카테고리를 사용하여 작업을 분류하고 해당 필드를 사용하여 작업의 카테고리에 따라 가격과 비용을 책정하였습니다.</span><span class="sxs-lookup"><span data-stu-id="a922b-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]