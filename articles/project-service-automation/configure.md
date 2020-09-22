---
title: Project Service Automation 구성
description: Project Service 구성 단계
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753259"
---
# <a name="configure-project-service"></a><span data-ttu-id="bef4b-103">Project Service 구성</span><span class="sxs-lookup"><span data-stu-id="bef4b-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bef4b-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]에서 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 자동화 기능을 사용하여 거래처, 프로젝트 및 리소스를 관리하려면, 먼저 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 솔루션이 조직의 요구 사항에 맞게 몇 가지 구성 단계를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="bef4b-105">이 단계에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-105">These steps include:</span></span>  
  
-   <span data-ttu-id="bef4b-106">[시간 단위 설정](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="bef4b-107">프로젝트 일정 및 결제에 기본으로 사용할 프로젝트 카탈로그의 시간 단위를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="bef4b-108">[통화 및 환율 설정](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="bef4b-109">프로젝트에 사용할 통화를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="bef4b-110">[조직 구성 단위 만들기](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="bef4b-111">지역, 비즈니스 기능 또는 기타 논리 부분 등, 비즈니스를 구분하는 데 사용하는 그룹을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="bef4b-112">[송장 빈도 설정](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="bef4b-113">고객에게 비용을 청구하는 데 사용하려는 기간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="bef4b-114">[거래 범주 구성](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="bef4b-115">컨설턴트가 지불 가능 및 지불 불가능 비용을 청구할 수 있는 거래 카테고리를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="bef4b-116">[경비 범주 구성](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="bef4b-117">컨설턴트가 지불 가능 및 지불 불가능 비용을 청구할 수 있는 카테고리를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="bef4b-118">[제품 카탈로그 항목 만들기](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="bef4b-119">제품 카탈로그에 소프트웨어 라이선스 등의 판매 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="bef4b-120">[가격표 만들기](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="bef4b-121">프로젝트에 필요한 각 역할에 대해 고객에게 청구하려는 금액에 따라 다양한 가격표를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="bef4b-122">[리소스 설정](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="bef4b-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="bef4b-123">프로젝트에 필요한 기술, 숙련도, 리소스 역할 및 기타 리소스 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bef4b-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bef4b-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bef4b-124">See Also</span></span>  
 <span data-ttu-id="bef4b-125">[Project Service Automation 개요](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="bef4b-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="bef4b-126">[Project Service Automation 구성](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="bef4b-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="bef4b-127">[거래처 관리자 가이드](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bef4b-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="bef4b-128">[프로젝트 관리자 가이드](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bef4b-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="bef4b-129">[리소스 관리자 가이드](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bef4b-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="bef4b-130">시간, 비용 및 공동 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="bef4b-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
