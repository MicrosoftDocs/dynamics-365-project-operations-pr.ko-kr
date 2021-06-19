---
title: 프로젝트 계약에 대한 프로젝트 가격표 관리
description: 이 항목은 프로젝트 계약의 프로젝트 가격표 관리에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010389"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="142b7-103">프로젝트 계약에 대한 프로젝트 가격표 관리</span><span class="sxs-lookup"><span data-stu-id="142b7-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="142b7-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="142b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="142b7-105">Dynamics 365 Project Operations의 프로젝트 계약은 계약에서 여러 날짜 유효 판매 가격표를 지원하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="142b7-106">Project Operations에는 **프로젝트 가격표** 라는 새로운 관련 엔터티가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="142b7-107">이 엔터티는 프로젝트 계약에 대해 일대 다 관계를 가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="142b7-108">프로젝트 가격표는 프로젝트에 대한 시간, 재료 및 경비 트랜잭션의 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="142b7-109">계약에 하나 이상의 프로젝트 가격표가 있는 경우 이러한 가격표는 계약 내용을 통해 계약과 연관된 프로젝트의 시간, 재료, 경비 추정 및 실제 가격을 책정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="142b7-110">프로젝트 계약에 프로젝트 가격표가 없으면 프로젝트 가격표가 없으며 기록된 견적, 실제 프로젝트 작업, 재료 및 경비 가격이 책정되지 않는다는 경고 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="142b7-111">판매 가치에 대한 가격은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="142b7-112">프로젝트 계약에서 프로젝트 가격표 연결 또는 연결 해제</span><span class="sxs-lookup"><span data-stu-id="142b7-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="142b7-113">프로젝트 기반 작업, 재료 및 경비를 추정하기 위해 특정 가격표를 생성하거나 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="142b7-114">프로젝트 계약에서 **프로젝트 가격표** 탭을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="142b7-115">하위 표에서 **+ 새 프로젝트 가격표 추가** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="142b7-116">**빨리 만들기** 슬라이더에서 가격표를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="142b7-117">드롭다운 목록에는 컨텍스트가 **영업** 으로 설정된 모든 가격표가 표시됩니다. 여기서 가격표의 통화가 계약의 통화와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="142b7-118">프로젝트 가격표 연결에 대한 설명을 입력하고 **저장** 을 클릭한 다음 **빨리 만들기** 슬라이더를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="142b7-119">프로젝트 가격표 연결이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="142b7-120">1-4 단계를 반복하여 둘 이상의 프로젝트 가격표를 프로젝트 계약에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="142b7-121">연결된 각 프로젝트 가격표에 대해 다른 날짜 유효성이 있는 경우에만 여러 프로젝트 가격표를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="142b7-122">Project Operations는 프로젝트 가격표의 날짜 유효성 중복을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="142b7-123">특정 날짜의 트랜잭션에 대해 여러 프로젝트 가격표가 있는 경우 해당 트랜잭션의 가격은 기본적으로 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="142b7-124">프로젝트 가격표 연결 제거</span><span class="sxs-lookup"><span data-stu-id="142b7-124">Remove a project price list association</span></span>

- <span data-ttu-id="142b7-125">프로젝트 가격표를 선택한 다음 하위 표에서 **계약 프로젝트 가격표 삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="142b7-126">계약의 프로젝트 가격표에서 가격표가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="142b7-127">가격표 자체는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="142b7-128">계약에 대한 연결만 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="142b7-129">계약에서 프로젝트 가격표의 자동 기본값 설정</span><span class="sxs-lookup"><span data-stu-id="142b7-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="142b7-130">프로젝트 가격표를 기본 프로젝트 가격표로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="142b7-131">이 설정은 조직의 모든 계약이 항상 해당 가격 기간에 대한 표준 프로젝트 가격표로 시작되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="142b7-132">프로젝트 가격표에 대한 조직 기본값 설정</span><span class="sxs-lookup"><span data-stu-id="142b7-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="142b7-133">**설정** > **일반** 으로 이동한 다음 **매개 변수** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="142b7-134">**활성 매개 변수** 목록 페이지에서 레코드를 선택하고 두 번 클릭하여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="142b7-135">두 번 클릭하는 동안 하이퍼링크인 필드 값을 클릭하지 않았는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="142b7-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="142b7-136">**활성 매개 변수** 페이지에서 **가격표** 탭을 선택합니다. 하위 표에는 기본 가격표의 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="142b7-137">이것은 표준 비용 및 판매 가격표 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="142b7-138">판매하는 모든 통화에 대해 여기에 연결된 **영업** 가격표는 영업 가격표가 이 통화로 거래하는 고객에 대해 생성하는 모든 계약의 기본값이 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="142b7-139">고객별 프로젝트 가격표 설정</span><span class="sxs-lookup"><span data-stu-id="142b7-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="142b7-140">또한 고객과 마스터 가격 계약을 협상한 경우 고객별 프로젝트 가격표를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="142b7-141">**영업** > **고객** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="142b7-142">활성 거래처 목록에서 특별 가격표가 있는 고객을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="142b7-143">고객 레코드를 선택하여 연 다음 **프로젝트 가격표** 탭을 선택합니다. 하위 표는 이 고객에게 특정한 프로젝트 가격표 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="142b7-144">이 고객에게 특정한 프로젝트 가격표를 포함하려면 여기에 새 가격표 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="142b7-145">프로젝트 계약에 대한 사용자 지정 가격</span><span class="sxs-lookup"><span data-stu-id="142b7-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="142b7-146">조직 및 고객별 기본 프로젝트 가격표가 있으면 이러한 프로젝트 가격표 연결을 사용하여 프로젝트 계약이 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="142b7-147">그러나 프로젝트 계약의 프로젝트 가격표는 항상 날짜와 계약 이름이 추가된 상태로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="142b7-148">그런 다음 거래처 및 프로젝트 관리자는 이러한 사본의 가격을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="142b7-149">변경된 가격은 이 프로젝트 계약에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="142b7-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
