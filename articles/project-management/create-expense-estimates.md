---
title: 경비 추정
description: 이 항목은 프로젝트 기반 경비 정의 또는 추정에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908340"
---
# <a name="expense-estimates"></a><span data-ttu-id="0a803-103">경비 추정</span><span class="sxs-lookup"><span data-stu-id="0a803-103">Expense estimates</span></span>
<span data-ttu-id="0a803-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="0a803-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0a803-105">리소스 기반 추정을 정의하는 것과 함께 Dynamics 365 Project Operations를 통해 프로젝트 관리자는 각 프로젝트에 대한 프로젝트 기반 경비를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="0a803-106">각 경비 항목은 특정 프로젝트 작업 또는 경비 범주와 연관될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="0a803-107">경비 범주는 일반적으로 조직 수준에서 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="0a803-108">각 경비 범주의 가격은 일반적으로 다음 계층 구조로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="0a803-109">조직</span><span class="sxs-lookup"><span data-stu-id="0a803-109">Organization</span></span>
- <span data-ttu-id="0a803-110">고객</span><span class="sxs-lookup"><span data-stu-id="0a803-110">Customer</span></span>
- <span data-ttu-id="0a803-111">견적/계약</span><span class="sxs-lookup"><span data-stu-id="0a803-111">Quote/contract</span></span>

<span data-ttu-id="0a803-112">프로젝트 경비를 조회, 추가 또는 삭제하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="0a803-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="0a803-113">**프로젝트**로 이동하고 작업할 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="0a803-114">**프로젝트 추정** 탭을 선택하고 프로젝트 경비 목록을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="0a803-115">**새 경비**를 선택하여 경비를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="0a803-116">또는 삭제할 경비를 선택한 다음 **경비 삭제**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="0a803-117">각 경비 라인 항목에 대해 다음 속성이 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="0a803-118">**범주**: 프로젝트에서 발생한 모든 경비를 설명하는 데 사용되는 공통 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="0a803-119">**시작 날짜**: 경비 발생이 예상되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="0a803-120">**수량**: 특정 범주에 대한 예상 경비 항목 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="0a803-121">**단가 가격**: 경비의 비용을 계산하는 데 사용되는 단가입니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="0a803-122">**단위 판매 가격**: 경비의 판매 가격을 계산하는 데 사용되는 단가입니다.</span><span class="sxs-lookup"><span data-stu-id="0a803-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

