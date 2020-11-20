---
title: 추정 및 실제에서 원가 해결 - 라이트
description: 이 항목은 추정 및 실제의 원가를 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176799"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="6efbf-103">추정 및 실제에서 원가 해결 - 라이트</span><span class="sxs-lookup"><span data-stu-id="6efbf-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="6efbf-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="6efbf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6efbf-105">추정 및 실제에 대한 원가 및 비용 가격표를 해결하기 위해 시스템은 관련 프로젝트의 **날짜**, **통화** 및 **계약 단위** 필드의 정보를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="6efbf-106">비용 가격표가 해결된 후 응용 프로그램은 비용 요금을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="6efbf-107">시간에 대한 실제 및 추정 라인의 비용 요금 해결</span><span class="sxs-lookup"><span data-stu-id="6efbf-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="6efbf-108">시간에 대한 추정 라인은 프로젝트의 시간 및 리소스 지정에 대한 견적 및 계약 내용 세부 사항을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="6efbf-109">원가 가격표가 확인된 후 시스템은 시간에 대한 추정 라인의 **역할** 및 **리소스 조달 단위** 필드를 사용하여 가격표의 역할 가격 라인과 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-109">After a cost price list is resolved, the system uses the **Role** and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="6efbf-110">이 일치는 인력 비용에 대해 기본 가격 책정 차원을 사용한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="6efbf-111">대신 또는 추가로 **역할** 및 **리소스 조달 단위** 필드를 일치시키도록 시스템을 구성한 경우 다른 조합을 사용하여 일치하는 역할 가격 라인을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="6efbf-112">응용 프로그램이 **역할** 및 **리소스 조달 단위** 조합에 대한 비용 요금이 있는 역할 가격 라인을 찾은 경우 이것이 기본 비용 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="6efbf-113">응용 프로그램이 **역할** 및 **리소스 조달 단위** 값을 일치시킬 수 없는 경우 역할은 일치하지만 **리소스 조달 단위** 값이 널인 역할 가격 라인을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="6efbf-114">일치하는 역할 가격 레코드가 있으면 해당 레코드에서 비용 요금이 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="6efbf-115">**역할** 및 **리소스 조달 단위** 의 다른 우선 순위를 구성했거나 우선 순위가 더 높은 다른 차원이 있는 경우 이 동작은 그에 따라 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="6efbf-116">시스템은 마지막에 오는 해당 차원에 대해 null 값이 있는 행의 우선 순위에 따라 각 가격 책정 차원 값과 일치하는 값이 있는 역할 가격 레코드를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="6efbf-117">경비에 대한 실제 및 추정 라인의 비용 요금 해결</span><span class="sxs-lookup"><span data-stu-id="6efbf-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="6efbf-118">경비에 대한 추정 라인은 프로젝트의 경비 및 경비 추정 라인에 대한 견적 및 계약 내용 세부 사항을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="6efbf-119">원가 가격표가 확인된 후 시스템은 추정 라인의 **범주** 및 **단위** 필드의 조합을 사용하여 경비를 **범주 가격** 과 일치시킵니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="6efbf-120">시스템이 **범주** 및 **단위** 필드 조합에 대한 비용 요금이 있는 범주 가격 라인을 찾은 경우 이것이 비용 요금이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="6efbf-121">시스템이 **범주** 및 **단위** 값을 일치시킬 수 없거나 또는 일치하는 범주 가격 라인을 찾을 수 있지만 가격 책정 방법이 **단가** 가 아닌 경우 비용 요금은 기본적으로 영(0)으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6efbf-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>
