---
title: 경비 보고서 전기
description: 이 항목은 총계정 원장에 경비 보고서를 전기하는 방법을 설명합니다.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080198"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="d244c-103">경비 보고서 전기</span><span class="sxs-lookup"><span data-stu-id="d244c-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d244c-104">경비 보고서가 승인되고 일반 분개장으로 이전된 후 총계정 원장에 전기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="d244c-105">경비 보고서를 전시하면 부가가치세(VAT) 공제 대상 경비가 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="d244c-106">VAT 지불 확인 및 복구 작업은 경비 보고서 확인을 담당하는 직원에게 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="d244c-107">경비 보고서의 비용이 직원을 고용한 회사가 아닌 다른 회사에 청구되는 경우 해당 경비를 지불해야 하는 회사와 경비를 지불 받아야 하는 회사를 모두 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="d244c-108">예를 들어 경비 보고서를 제출한 직원은 DAT 회사에서 근무하지만 DIR 회사에 비용을 청구했습니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="d244c-109">이 경우 DAT는 경비를 지불해야 하는 회사이고 DIR은 비용을 지불 받아야 하는 회사입니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="d244c-110">이러한 분개장 항목을 확인한 후 경비 라인을 총계정 원장에 전기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="d244c-111">경비 보고서를 전기하려면 **승인된 경비 보고서** 페이지에서 경비 보고서를 선택한 다음 작업 창에서 **경비** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="d244c-112">동시에 목록의 모든 경비 보고서를 전기할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="d244c-113">모든 경비 보고서를 선택한 다음 **전기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d244c-113">Select all the expense reports, and then select **Post**.</span></span>
