---
title: 프로젝트 판매 가격표 재정의
description: 이 항목은 맞춤 판매 가격표 생성에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275546"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="08e64-103">프로젝트 판매 가격표 재정의</span><span class="sxs-lookup"><span data-stu-id="08e64-103">Override project sales price lists</span></span>

<span data-ttu-id="08e64-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="08e64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="08e64-105">고객별 프로젝트 가격표</span><span class="sxs-lookup"><span data-stu-id="08e64-105">Customer-specific project price lists</span></span>

<span data-ttu-id="08e64-106">고객별 가격 계약은 Dynamics 365 Project Operations의 거래처 레코드에서 프로젝트 가격표로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="08e64-107">고객별 프로젝트 가격표를 설정하려면 **영업** 영역에서 거래처 레코드로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="08e64-108">**거래처** 목록 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="08e64-109">고객 레코드를 찾아 두 번 클릭하여 **거래처** 세부 정보 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="08e64-110">**프로젝트 가격표** 탭에서 **+ + 새 프로젝트 가격표** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="08e64-111">**새 프로젝트 가격표** 페이지의 드롭다운에서 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="08e64-112">컨텍스트가 **영업** 으로 설정된 가격표만 거래처 통화와 일치하는 통화가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="08e64-113">연결 이름을 입력하고 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="08e64-114">고객별 프로젝트 가격표가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="08e64-115">이 가격표는 견적 또는 프로젝트 계약의 생성 날짜가 가격표의 날짜 유효 기간 내에 있는 이 고객에 대해 생성된 프로젝트 견적 또는 계약의 기본 프로젝트 가격에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="08e64-116">프로젝트 견적에 대한 사용자 지정 가격</span><span class="sxs-lookup"><span data-stu-id="08e64-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="08e64-117">프로젝트 견적에서 고객 또는 프로젝트 매개 변수에서 기본으로 제공되는 기본 표준 가격표로 시작하는 프로젝트 가격을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="08e64-118">특정 견적에 대한 프로젝트 관련 작업에 대한 사용자 지정 가격이 필요한 경우 프로젝트 가격표 관련 엔터티에서 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="08e64-119">견적별 프로젝트 가격을 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="08e64-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="08e64-120">프로젝트 견적을 열고 **프로젝트 가격표** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="08e64-121">하위 표에서 **사용자 지정 가격 책정 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="08e64-122">견적에 첨부된 모든 프로젝트 가격 목록이 새 가격 목록에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="08e64-123">새 가격표의 이름은 이러한 가격표가 생성된 날짜-타임 스탬프와 함께 견적 이름을 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="08e64-124">이러한 각 가격표를 사용하고 인건비(역할 가격) 및 경비(범주 가격) 가격을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="08e64-125">이러한 가격은 이 프로젝트 견적에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="08e64-126">프로젝트 계약의 가격표</span><span class="sxs-lookup"><span data-stu-id="08e64-126">Price lists on a project contract</span></span>

<span data-ttu-id="08e64-127">프로젝트 계약에서 프로젝트 가격은 항상 계약 이름과 이름에 생성된 날짜 타임 스탬프가 추가된 사용자 지정 가격표로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="08e64-128">이는 견적이 성사되었을 때 계약이 생성되었거나 계약이 처음부터 생성되었는지 여부에 관계없이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="08e64-129">필요한 경우 사용자 지정 가격표에서 이 연결을 제거하고 대신 표준 가격표를 프로젝트 계약에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="08e64-130">표준 가격표를 견적 또는 계약의 프로젝트 가격표에 연결하면 가격표의 가격 변경 사항이 가격표를 사용하는 모든 견적 및 계약에 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="08e64-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]