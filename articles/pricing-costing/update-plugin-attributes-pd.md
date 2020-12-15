---
title: 새 가격 책정 차원을 포함하도록 플러그인 특성 업데이트
description: 이 주제는 가격 책정 차원에 대한 플러그인 특성을 업데이트하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643226"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="66a9f-103">새 가격 책정 차원을 포함하도록 플러그인 특성 업데이트</span><span class="sxs-lookup"><span data-stu-id="66a9f-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="66a9f-104">이 주제는 가격 책정 차원에 대한 플러그인 특성을 업데이트하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="66a9f-105">이 토픽은 Dynamics 365 Project Operations의 견적 및 계약 기능에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66a9f-106">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="66a9f-106">Prerequisites</span></span>
<span data-ttu-id="66a9f-107">이 토픽의 단계를 완료하기 전에 다음 토픽의 절차를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="66a9f-108">맞춤 필드 및 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="66a9f-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="66a9f-109">가격 설정 및 거래 엔터티에 사용자 지정 필드 추가</span><span class="sxs-lookup"><span data-stu-id="66a9f-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="66a9f-110">[가격 책정 차원의 사용자 지정 필드 설정](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="66a9f-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="66a9f-111">이러한 절차를 완료하지 않은 경우 완료한 다음 이 항목으로 돌아오십시오.</span><span class="sxs-lookup"><span data-stu-id="66a9f-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="66a9f-112">플러그 인 등록</span><span class="sxs-lookup"><span data-stu-id="66a9f-112">Register a plug-in</span></span>
<span data-ttu-id="66a9f-113">견적 라인 세부 정보가 생성되면 프로젝트 견적 라인의 **견적 라인** 페이지에서 시스템은 두 개의 견적 라인을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="66a9f-114">한 라인은 견적의 비용 측면이고 다른 라인은 판매 측면입니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="66a9f-115">프로젝트 계약 행에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="66a9f-116">원가 측면에서 수량 또는 필드를 변경하면 해당 변경이 매출액 측에서 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="66a9f-117">이것은 Quotelinedetail 및 contractline 세부 항목의 PreOperation 플러그인이 비용 측면의 특정 속성을 트랜잭션의 판매 측면에 연결하기 때문에 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="66a9f-118">판매 측의 가격 책정 차원 값을 비용 측에서도 변경해야 하는 경우 가격 책정 차원을 변경한 후 다음 플러그인을 다시 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="66a9f-119">다음은 업데이트 및 재등록할 플러그인입니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="66a9f-120">PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction 업데이트**</span><span class="sxs-lookup"><span data-stu-id="66a9f-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="66a9f-121">PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction 업데이트**</span><span class="sxs-lookup"><span data-stu-id="66a9f-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="66a9f-122">플러그인을 업데이트하고 다시 등록하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="66a9f-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="66a9f-123">**PluginRegistrationTool** 을 열고 Project Operations Dataverse 환경에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="66a9f-124">**검색** 을 선택하고 업데이트할 플러그인의 처음 몇 글자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="66a9f-125">플러그인을 찾은 후 플러그인을 선택한 다음 **기본 양식에서 선택** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="66a9f-126">**msdyn_orderlinetransaction 업데이트** 단계를 선택하고 마우스 오른쪽 버튼으로 클릭한 다음, **업데이트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="66a9f-127">**업데이트** 대화 상자 페이지에서 필터링 속성의 타원(**...**)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="66a9f-128">필터링 속성 창이 열리고 엔터티 및 가격 책정 차원의 모든 특성 목록이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="66a9f-129">가격 책정 차원 특성의 선택란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="66a9f-130">**OK** 를 선택하여 페이지를 닫은 다음 **업데이트 단계** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="66a9f-131">두 번째 플러그인 **PreOperationQuoteLineDetail** 에 대해 2-7 단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="66a9f-132">이 플러그인의 경우 **msdyn_quotelinetransaction 업데이트** 단계를 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="66a9f-133">**PluginRegistrationTool** 을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="66a9f-133">Close **PluginRegistrationTool**.</span></span>
