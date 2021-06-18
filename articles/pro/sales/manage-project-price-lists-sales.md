---
title: 프로젝트 견적에 대한 프로젝트 가격표 관리
description: 이 항목은 견적에 대한 프로젝트 가격표 작업에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 926581f877f91e3a351d51cac9c2b1daba035126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994909"
---
# <a name="manage-project-price-lists-on-project-quotes"></a><span data-ttu-id="f6a4f-103">프로젝트 견적에 대한 프로젝트 가격표 관리</span><span class="sxs-lookup"><span data-stu-id="f6a4f-103">Manage project price lists on project quotes</span></span> 

<span data-ttu-id="f6a4f-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="f6a4f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6a4f-105">프로젝트 견적은 여러 날짜의 유효 판매 가격표를 지원하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-105">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="f6a4f-106">Dynamics 365 Project Operations에서 **프로젝트 가격표** 라는 새 관련 엔티티가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-106">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="f6a4f-107">이 엔터티는 프로젝트 견적과 일대 다 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-107">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="f6a4f-108">프로젝트 가격표는 프로젝트에 대한 시간, 재료 및 경비 트랜잭션의 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="f6a4f-109">견적에 하나 이상의 프로젝트 가격표가 있는 경우 이러한 가격표는 견적 라인을 통해 견적과 연관된 프로젝트의 시간, 재료, 경비 추정 및 실제 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-109">When a quote has one or more project price lists, these price lists are used to price time, material, expense estimates, and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="f6a4f-110">프로젝트 견적에 프로젝트 가격표가 없으면 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-110">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="f6a4f-111">이 메시지는 프로젝트 가격표가 없기 때문에 추정 및 실제 프로젝트 작업 및 경비가 책정되지 않는다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-111">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="f6a4f-112">대신 판매 값에 대한 가격이 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-112">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="f6a4f-113">프로젝트 견적에서 프로젝트 가격표 연결 또는 연결 해제</span><span class="sxs-lookup"><span data-stu-id="f6a4f-113">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="f6a4f-114">프로젝트 기반 작업 및 경비를 추정하기 위해 특정 가격표를 작성하거나 선택하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-114">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="f6a4f-115">견적에서 **프로젝트 가격** 탭을 선택하고 하위 표에서 **+ 새 프로젝트 가격표 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-115">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="f6a4f-116">빨리 만들기 페이지에서 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-116">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="f6a4f-117">드롭다운 목록에는 컨텍스트가 **영업** 으로 설정된 모든 가격표가 표시되고 통화는 견적의 통화와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-117">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="f6a4f-118">프로젝트 가격표 연결에 대한 설명을 입력하고 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-118">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="f6a4f-119">프로젝트 가격표 연결이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-119">A project price list association is created.</span></span>

<span data-ttu-id="f6a4f-120">둘 이상의 프로젝트 가격표를 프로젝트 견적에 연결해야 하는 경우 이 프로세스를 반복할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-120">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="f6a4f-121">연결된 각 프로젝트 가격펴에 다른 유효 날짜가 있는 경우에만 여러 프로젝트 가격표를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-121">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="f6a4f-122">Project Operations는 프로젝트 가격표의 중복 날짜 유효성을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-122">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="f6a4f-123">주어진 날짜의 트랜잭션에 대해 여러 프로젝트 가격표가 있는 경우 해당 트랜잭션의 가격은 기본적으로 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-123">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="f6a4f-124">프로젝트 가격표 연결을 제거하려면 프로젝트 가격표를 선택한 다음 **견적 프로젝트 가격표 삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-124">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="f6a4f-125">견적의 프로젝트 가격표에서 가격표가 제거되지만 가격표 자체는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-125">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="f6a4f-126">견적에 대한 연결만 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-126">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="f6a4f-127">견적에 기본 프로젝트 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="f6a4f-127">Set up default project price lists on a quote</span></span>

<span data-ttu-id="f6a4f-128">프로젝트 가격표는 프로젝트 견적에서 기본값으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-128">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="f6a4f-129">이렇게 설정하면 조직의 모든 견적이 항상 해당 가격 기간에 대한 표준 가격표로 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-129">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="f6a4f-130">프로젝트 가격표에 대한 조직 기본값 설정</span><span class="sxs-lookup"><span data-stu-id="f6a4f-130">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="f6a4f-131">**설정** > **일반** > **매개 변수** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-131">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="f6a4f-132">**활성 매개 변수** 목록 페이지에서 레코드를 찾은 다음 두 번 클릭하여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-132">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="f6a4f-133">**매개 변수** 페이지에서 **가격표** 탭을 선택합니다. 기본 가격표가 표시되는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-133">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="f6a4f-134">이것은 목록 표준 비용 및 판매 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-134">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="f6a4f-135">판매하는 모든 통화에 대해 여기에 연결된 판매 가격표가 있으면 이 통화로 거래하는 고객에 대해 생성한 견적에 이 판매 가격펴가 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-135">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="f6a4f-136">고객별 프로젝트 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="f6a4f-136">Set up customer-specific project price lists</span></span>

<span data-ttu-id="f6a4f-137">고객과 마스터 가격 계약을 협상한 경우 고객별 프로젝트 가격표를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-137">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="f6a4f-138">고객별 프로젝트 가격표를 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-138">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="f6a4f-139">**영업** 영역에서 **고객** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-139">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="f6a4f-140">활성 계정 목록에서 특별 가격표가 있는 고객 레코드를 선택하고 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-140">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="f6a4f-141">**프로젝트 가격표** 탭에서 이 고객에게 특정한 프로젝트 가격표를 포함하도록 새 가격표 연결을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-141">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="f6a4f-142">프로젝트 견적에 대한 맞춤형 가격 만들기</span><span class="sxs-lookup"><span data-stu-id="f6a4f-142">Create custom pricing on a project quote</span></span>

<span data-ttu-id="f6a4f-143">조직 및 고객별 기본 프로젝트 가격표가 있으면 이러한 프로젝트 가격표 연결을 사용하여 프로젝트 견적이 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-143">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="f6a4f-144">그러나 특정 경우에는 특정 프로젝트 견적에 대한 사용자 지정 가격을 생성해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-144">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="f6a4f-145">**프로젝트 견적** 의 **프로젝트 가격표** 탭에서 특정 가격표 레코드가 선택되지 않았는지 하위 표에서 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-145">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="f6a4f-146">**사용자 지정 가격 산정 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-146">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="f6a4f-147">이렇게 하면 현재 견적에 연결된 모든 표준 가격표의 복사본이 만들어지고 이러한 복사본이 견적에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-147">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="f6a4f-148">표준 가격표에 대한 기존 연결이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-148">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="f6a4f-149">그런 다음 영업 사원은 이러한 사본의 가격을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-149">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="f6a4f-150">변경된 가격은 이 프로젝트 견적에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-150">These changed prices will be applicable to this project quote only.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
