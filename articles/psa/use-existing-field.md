---
title: Project Service의 기존 필드를 가격 책정 차원으로 사용
description: 이 항목은 가격 책정 차원으로서 기존 Project Service 필드를 사용하는 것에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281576"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="0694c-103">Project Service의 기존 필드를 가격 책정 차원으로 사용</span><span class="sxs-lookup"><span data-stu-id="0694c-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0694c-104">Project Service Automation(PSA)의 **실제값** 엔터티에는 프로젝트 조직에서 리소스 기반 가격 책정을 위한 가격 책정 차원으로 사용할 수 있는 많은 필드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="0694c-105">예를 들어, 하나의 공통 필드가 **예약 가능한 리소스** 입니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="0694c-106">청구 가능한 리소스가 20~30개 미만인 소규모 기업은 각 리소스에 특정한 청구서 및 비용 요율을 갖는 것이 더 간단한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="0694c-107">그러나 청구 가능한 인력이 증가함에 따라 리소스가 승격되거나 더 많은 경험을 얻거나 다른 기능 집합을 습득함에 따라 리소스 비용과 청구 요금이 달라지기 시작하면서 특정 비율을 유지하는 것이 비현실적일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="0694c-108">이 방법은 여전히 특정 크기의 회사에서 작동하므로, 어떻게 기존 Project Service 필드를 가격 책정 차원으로 사용할 수 있는지를 이해하려면 [예약 가능한 리소스를 가격 책정 차원으로 사용](bookable-resource-pricing-dimension.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0694c-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="0694c-109">또 다른 예는 처리 카테고리의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-109">Another example is that of transaction category.</span></span> <span data-ttu-id="0694c-110">고객과 구현자는 PSA의 처리 카테고리를 사용하여 작업을 분류하고 해당 필드를 사용하여 작업의 카테고리에 따라 가격과 비용을 책정하였습니다.</span><span class="sxs-lookup"><span data-stu-id="0694c-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="0694c-111">자세한 설명은 [처리 카테고리 를 가격 책정 차원으로 사용](transaction-category-pricing-dimension.md) 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0694c-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]