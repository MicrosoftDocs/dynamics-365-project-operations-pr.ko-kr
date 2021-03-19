---
title: 프로젝트 범주 구성
description: 이 항목에서는 프로젝트 범주 설정에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287516"
---
# <a name="configure-project-categories"></a><span data-ttu-id="e3030-103">프로젝트 범주 구성</span><span class="sxs-lookup"><span data-stu-id="e3030-103">Configure project categories</span></span>

<span data-ttu-id="e3030-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e3030-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e3030-105">Project Operations는 프로젝트의 수익과 경비를 분류하는 강력한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="e3030-106">범주는 프로젝트 트랜잭션을 보고 및 분석하고 총계정 원장에 전기하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="e3030-107">다음 다이어그램은 트랜잭션 범주, 공유 범주 및 프로젝트 범주 간의 상관 관계를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="e3030-108">트랜잭션 범주는 프로젝트 트랜잭션의 기본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="e3030-109">해당 그룹 내에는 응용 프로그램과 모듈간에 공유할 수 있는 공유 범주 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="e3030-110">더 자세히 살펴보면 프로젝트 범주는 가장 세분화된 범주 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="e3030-111">프로젝트 범주는 법인, 모듈 및 응용 프로그램에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-111">Project categories are specific to legal entity, module, and application.</span></span>

![트랜잭션 범주, 공유 범주 및 프로젝트 범주 간의 상관 관계](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="e3030-113">트랜잭션 범주</span><span class="sxs-lookup"><span data-stu-id="e3030-113">Transaction categories</span></span>

<span data-ttu-id="e3030-114">트랜잭션 범주는 프로젝트 트랜잭션에 대한 기본 그룹을 나타내며 회사 또는 트랜잭션 유형과 관련이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="e3030-115">예를 들어 Contoso Robotics는 디자인, 여행, 설치 및 서비스 트랜잭션 범주를 사용하여 프로젝트 트랜잭션을 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="e3030-116">트랜잭션 범주는 Project Operations 모듈에서 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="e3030-117">**설정** \>**트랜잭션 범주** 로 이동하여 양식을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="e3030-118">**새로 만들기** 를 선택하거나 **Excel에서 가져오기** 를 선택하여 새 트랜잭션 범주를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="e3030-119">공유 범주</span><span class="sxs-lookup"><span data-stu-id="e3030-119">Shared categories</span></span>

<span data-ttu-id="e3030-120">Dynamics 365는 공유 범주 개념을 사용하여 Dynamics 365 Finance, Dynamics 365 Supply Chain 및 Dynamics 365 Project Operations와 같은 다양한 응용 프로그램에서 비용을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="e3030-121">생성된 각 트랜잭션 범주에 대해 Project Operations는 시간, 경비, 요금 및 품목의 네 가지 관련 공유 범주를 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="e3030-122">**프로젝트 관리 및 회계** \> **설정** \> **범주** \> **공유 범주** 로 이동하여 공유 범주를 검토하고 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="e3030-123">프로젝트 범주</span><span class="sxs-lookup"><span data-stu-id="e3030-123">Project categories</span></span>

<span data-ttu-id="e3030-124">프로젝트 범주는 가장 세분화된 범주 구성 수준을 나타내며 프로젝트 회계사가 각 회사에 대해 별도로 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="e3030-125">**프로젝트 관리 및 회계** \> **설정** \> **범주** \> **프로젝트 범주** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="e3030-126">**새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-126">Select **New**.</span></span>
3. <span data-ttu-id="e3030-127">이전 섹션에서 만든 공유 범주의 **범주 ID** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="e3030-128">Project Operations에서는 트랜잭션 범주와 연관된 공유 범주만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="e3030-129">범주 그룹을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="e3030-130">범주 그룹</span><span class="sxs-lookup"><span data-stu-id="e3030-130">Category groups</span></span>

<span data-ttu-id="e3030-131">범주 그룹은 관련 프로젝트 범주 간에 속성(주로 프로필 게시)을 공유하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="e3030-132">각 트랜잭션 유형에 대해 하나 이상의 범주 그룹이 있어야 하며 각 프로젝트 범주에는 그룹이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="e3030-133">Project Operations의 전기 사양은 프로젝트 비용 및 수익 프로필 규칙, 프로젝트 범주 및 범주 그룹에 의해 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="e3030-134">**프로젝트 관리 및 회계** \> **설정** \> **범주** \> **범주 그룹** 으로 이동하여 범주 그룹을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3030-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]