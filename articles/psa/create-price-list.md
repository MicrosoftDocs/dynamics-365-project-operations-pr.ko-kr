---
title: 가격표 만들기
description: 가격표를 만드는 방법(Project Service)
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149461"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="c62fc-103">가격표 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="c62fc-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c62fc-104">가격표는 거래처 관리자가 견적 및 프로젝트를 만들고 프로젝트 비용을 수립할 때 사용할 수 있는 템플릿을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="c62fc-105">또한, 가격표는 역할 및 비용의 내용 항목 목록과 각각에 대해 청구할 가격을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="c62fc-106">여러 개의 가격표를 만들어서 제품을 판매하는 지역 또는 판매 채널에 따라 가격 구조를 서로 다르게 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="c62fc-107">고객에게 청구할 모든 통화에 대해 하나 이상의 가격표를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="c62fc-108">납품할 작업에 대한 비용 예상을 만들려면, 모든 프로젝트에 비용 및 영업 가격표가 설정되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="c62fc-109">조직에서 만드는 모든 프로젝트에 적용하는 기본 비용 및 영업 가격표를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="c62fc-110">가격표는 역할 및 경지 범주에 따라 달라지므로, 가격표를 만들기 전에 먼저 가격표 생성 시 사용하려는 역할과 경비 범주를 설정했는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="c62fc-111">**Project Service > 가격표** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="c62fc-112">**새로 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="c62fc-113">**컨텍스트** 에서 **비용**, **구매** 또는 **영업** 중 이 가격표의 용도를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="c62fc-114">**이름** 에서 가격표에 대한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="c62fc-115">**통화** 에서 청구 또는 비용 산출에 사용할 통화를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="c62fc-116">**시간 단위** 에서 날짜, 시간 등과 같이 가격을 적용할 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="c62fc-117">필요에 따라 **시작일**, **종료일**, **설명** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="c62fc-118">**저장** 을 클릭하여 레코드를 만들면 계속 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="c62fc-119">가격표에 역할 가격을 추가하려면 **역할 가격** 아래의 **+** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="c62fc-120">**역할 가격** 창에서 세부 내용을 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c62fc-121">필요에 따라 계속 역할 가격을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="c62fc-122">업을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="c62fc-123">가격표에 경비 범주를 추가하려면 **범주 가격** 아래의 **+** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="c62fc-124">**거래 범주 가격** 창에서 세부 내용을 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c62fc-125">필요에 따라 범주 가격을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="c62fc-126">업을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="c62fc-127">가격표에 가격표 항목을 추가하려면 **가격표 항목** 아래의 **+** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="c62fc-128">**가격표 항목** 창에서 세부 내용을 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c62fc-129">필요에 따라 계속 가격표 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="c62fc-130">업을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="c62fc-131">가격표에 지역 관계를 추가하려면 **지역 관계** 아래의 **+** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="c62fc-132">**새 연결** 창에서 세부 내용을 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c62fc-133">필요에 따라 지역 관계를 계속 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="c62fc-134">업을 마쳤으면, 화면 우측 하단의 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c62fc-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c62fc-135">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c62fc-135">See Also</span></span>  
 [<span data-ttu-id="c62fc-136">Project Service Automation 구성</span><span class="sxs-lookup"><span data-stu-id="c62fc-136">Configure Project Service Automation</span></span>](../psa/configure.md)
