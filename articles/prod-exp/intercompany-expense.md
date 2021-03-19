---
title: 회사 간 경비
description: 이 토픽은 회사 간 비용을 사용하여 작업이 수행된 법인에 근로자 비용을 할당하는 방법에 대한 정보를 제공합니다.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271541"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="8f85c-103">회사 간 경비</span><span class="sxs-lookup"><span data-stu-id="8f85c-103">Intercompany expenses</span></span>

<span data-ttu-id="8f85c-104">조직의 한 법인에 고용된 근로자는 동일한 조직의 다른 법인을 위해 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="8f85c-105">회사 간 비용을 사용하여 작업자의 비용을 작업이 수행된 법인에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="8f85c-106">근로자를 고용하는 법인을 대출 법인이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="8f85c-107">근로자에게 비용이 발생하는 법인을 차용 법인이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="8f85c-108">근로자가 회사 간 비용을 생성하고 실행하기 전에 회사 간 경비 라인을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="8f85c-109">대출 법인의 **경비 관리 매개 변수** 페이지에서 **회사 간 경비 라인 허용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="8f85c-110">회사간 경비에 대한 세금 전기</span><span class="sxs-lookup"><span data-stu-id="8f85c-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f85c-111">경비 보고서에서 차용(대상) 법인 대신 대출(출처) 법인과 연관된 세금 그룹을 사용하려면 먼저 총계정 원장 판매세 설정에서 기능을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="8f85c-112">**회사 간 세금 전기를 위한 법인** 매개 변수가 **출처** 로 설정되고 **판매세 과세 규칙 적용** 이 **아니요** 로 설정된 경우 대출 법인에 대한 세금 조합이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="8f85c-113">동일한 매개 변수가 **대상** 으로 설정된 경우 차용 법인에 대한 세금 조합이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="8f85c-114">미국 법인의 경우 매개 변수가 **원본** 으로 설정되면 **받을 판매세** 필드도 새 **원장 전기 그룹** 페이지에서 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="8f85c-115">회계 엔진은 이 필드의 정보를 세금 관련 회계 입력에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="8f85c-116">이 동작은 프로젝트 유무에 관계없이 전기된 경비 라인에 대해 일관됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f85c-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]