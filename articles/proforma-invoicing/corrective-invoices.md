---
title: 수정된 송장
description: 이 주제는 수정된 송장에 대한 정보를 제공합니다.
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
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287831"
---
# <a name="corrected-invoices"></a><span data-ttu-id="9bed0-103">수정된 송장</span><span class="sxs-lookup"><span data-stu-id="9bed0-103">Corrected invoices</span></span>

<span data-ttu-id="9bed0-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="9bed0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9bed0-105">확인된 송장을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="9bed0-106">확인된 송장을 편집하면 임시 수정된 송장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="9bed0-107">원래 송장의 모든 트랜잭션 및 수량을 되돌리려는 가정이기 때문에 이 수정된 송장에는 원래 송장의 모든 트랜잭션이 포함되며 모든 수량은 0(제로)입니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="9bed0-108">트랜잭션에 수정이 필요하지 않은 경우 초안 수정 송장에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="9bed0-109">일부 수량만 되돌리거나 반환하려면 라인 세부 사항에서 수량 필드를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="9bed0-110">송장 라인 세부 정보를 열면 원래 송장 수량을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="9bed0-111">그런 다음 원래 송장 수량보다 적거나 많은 현재 송장 수량을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="9bed0-112">수정 송장을 확인할 때 원래 청구된 영업 실제가 반대이며, 새 청구된 영업 실제가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="9bed0-113">수량이 줄어든 경우 그 차이로 인해 실제 청구되지 않은 새 영업도 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="9bed0-114">예를 들어 원래 청구된 영업이 8시간이고 수정된 송장 라인 세부 정보가 6시간으로 줄어든 경우 원래 청구된 영업 라인을 반대로 하고 두 개의 새 실제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="9bed0-115">6시간 동안 실제 청구된 영업.</span><span class="sxs-lookup"><span data-stu-id="9bed0-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="9bed0-116">나머지 2시간 동안 청구되지 않은 영업 실제.</span><span class="sxs-lookup"><span data-stu-id="9bed0-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="9bed0-117">이 거래는 고객과의 협상에 따라 나중에 청구되거나 요금이 부과되지 않는 것으로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bed0-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]