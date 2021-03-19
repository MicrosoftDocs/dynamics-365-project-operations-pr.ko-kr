---
title: 프로젝트 견적에 대한 프로젝트 가격표 관리 - 라이트
description: 이 항목은 견적에 대한 프로젝트 가격표 작업에 대한 정보를 제공합니다. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d48da44f382e329a978a8ceee59c354d009f2114
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273026"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a><span data-ttu-id="0e181-104">프로젝트 견적에 대한 프로젝트 가격표 관리 - 라이트</span><span class="sxs-lookup"><span data-stu-id="0e181-104">Manage project price lists on project quotes - lite</span></span>

<span data-ttu-id="0e181-105">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="0e181-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e181-106">프로젝트 견적은 여러 날짜의 유효 판매 가격표를 지원하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-106">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="0e181-107">Dynamics 365 Project Operations에서 **프로젝트 가격표** 라는 새 관련 엔티티가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-107">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="0e181-108">이 엔터티는 프로젝트 견적과 일대 다 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-108">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="0e181-109">프로젝트 가격표는 프로젝트에 대한 시간 및 비용 트랜잭션의 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-109">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="0e181-110">견적에 하나 이상의 프로젝트 가격표가 있는 경우 이러한 가격표는 견적 라인을 통해 견적과 연관된 프로젝트의 시간 및 비용 추정 및 실제 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-110">When a quote has one or more project price lists, these price lists are used to price time and expense estimates and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="0e181-111">프로젝트 견적에 프로젝트 가격표가 없으면 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-111">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="0e181-112">이 메시지는 프로젝트 가격표가 없기 때문에 추정 및 실제 프로젝트 작업 및 경비가 책정되지 않는다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-112">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="0e181-113">대신 판매 값에 대한 가격이 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-113">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="0e181-114">프로젝트 견적에서 프로젝트 가격표 연결 또는 연결 해제</span><span class="sxs-lookup"><span data-stu-id="0e181-114">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="0e181-115">프로젝트 기반 작업 및 경비를 추정하기 위해 특정 가격표를 작성하거나 선택하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="0e181-115">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="0e181-116">견적에서 **프로젝트 가격** 탭을 선택하고 하위 표에서 **+ 새 프로젝트 가격표 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-116">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="0e181-117">빨리 만들기 페이지에서 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-117">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="0e181-118">드롭다운 목록에는 컨텍스트가 **영업** 으로 설정된 모든 가격표가 표시되고 통화는 견적의 통화와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-118">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="0e181-119">프로젝트 가격표 연결에 대한 설명을 입력하고 **저장 후 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-119">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="0e181-120">프로젝트 가격표 연결이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-120">A project price list association is created.</span></span>

<span data-ttu-id="0e181-121">둘 이상의 프로젝트 가격표를 프로젝트 견적에 연결해야 하는 경우 이 프로세스를 반복할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-121">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="0e181-122">연결된 각 프로젝트 가격펴에 다른 유효 날짜가 있는 경우에만 여러 프로젝트 가격표를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-122">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="0e181-123">Project Operations는 프로젝트 가격표의 중복 날짜 유효성을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-123">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="0e181-124">주어진 날짜의 트랜잭션에 대해 여러 프로젝트 가격표가 있는 경우 해당 트랜잭션의 가격은 기본적으로 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-124">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="0e181-125">프로젝트 가격표 연결을 제거하려면 프로젝트 가격표를 선택한 다음 **견적 프로젝트 가격표 삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-125">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="0e181-126">견적의 프로젝트 가격표에서 가격표가 제거되지만 가격표 자체는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-126">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="0e181-127">견적에 대한 연결만 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-127">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="0e181-128">견적에 기본 프로젝트 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="0e181-128">Set up default project price lists on a quote</span></span>

<span data-ttu-id="0e181-129">프로젝트 가격표는 프로젝트 견적에서 기본값으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-129">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="0e181-130">이렇게 설정하면 조직의 모든 견적이 항상 해당 가격 기간에 대한 표준 가격표로 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-130">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="0e181-131">프로젝트 가격표에 대한 조직 기본값 설정</span><span class="sxs-lookup"><span data-stu-id="0e181-131">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="0e181-132">**설정** > **일반** > **매개 변수** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-132">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="0e181-133">**활성 매개 변수** 목록 페이지에서 레코드를 찾은 다음 두 번 클릭하여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-133">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="0e181-134">**매개 변수** 페이지에서 **가격표** 탭을 선택합니다. 기본 가격표가 표시되는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-134">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="0e181-135">이것은 목록 표준 비용 및 판매 가격표입니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-135">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="0e181-136">판매하는 모든 통화에 대해 여기에 연결된 판매 가격표가 있으면 이 통화로 거래하는 고객에 대해 생성한 견적에 이 판매 가격펴가 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-136">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="0e181-137">고객별 프로젝트 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="0e181-137">Set up customer-specific project price lists</span></span>

<span data-ttu-id="0e181-138">고객과 마스터 가격 계약을 협상한 경우 고객별 프로젝트 가격표를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-138">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="0e181-139">고객별 프로젝트 가격표를 설정하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="0e181-139">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="0e181-140">**영업** 영역에서 **고객** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-140">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="0e181-141">활성 계정 목록에서 특별 가격표가 있는 고객 레코드를 선택하고 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-141">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="0e181-142">**프로젝트 가격표** 탭에서 이 고객에게 특정한 프로젝트 가격표를 포함하도록 새 가격표 연결을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-142">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="0e181-143">프로젝트 견적에 대한 맞춤형 가격 만들기</span><span class="sxs-lookup"><span data-stu-id="0e181-143">Create custom pricing on a project quote</span></span>

<span data-ttu-id="0e181-144">조직 및 고객별 기본 프로젝트 가격표가 있으면 이러한 프로젝트 가격표 연결을 사용하여 프로젝트 견적이 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-144">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="0e181-145">그러나 특정 경우에는 특정 프로젝트 견적에 대한 사용자 지정 가격을 생성해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-145">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="0e181-146">**프로젝트 견적** 의 **프로젝트 가격표** 탭에서 특정 가격표 레코드가 선택되지 않았는지 하위 표에서 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-146">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="0e181-147">**사용자 지정 가격 산정 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-147">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="0e181-148">이렇게 하면 현재 견적에 연결된 모든 표준 가격표의 복사본이 만들어지고 이러한 복사본이 견적에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-148">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="0e181-149">표준 가격표에 대한 기존 연결이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-149">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="0e181-150">그런 다음 영업 사원은 이러한 사본의 가격을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-150">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="0e181-151">변경된 가격은 이 프로젝트 견적에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e181-151">These changed prices will be applicable to this project quote only.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]