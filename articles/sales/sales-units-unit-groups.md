---
title: 단위 및 단위 그룹
description: 이 토픽은 Dynamics 365 Project Operations에서 단위 및 단위 그룹을 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277346"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="5a592-103">단위 및 단위 그룹</span><span class="sxs-lookup"><span data-stu-id="5a592-103">Units and unit groups</span></span>

<span data-ttu-id="5a592-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="5a592-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a592-105">단위는 제품 또는 서비스를 판매하는 수량 또는 규격입니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="5a592-106">예를 들어, 정원 소모품을 판매하는 경우 씨앗을 패킷, 박스 또는 팔레트 단위로 판매할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="5a592-107">단위 그룹은 일한 여러 단위의 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="5a592-108">이 항목의 단계를 완료하려면 시스템 관리자 또는 Sales Professional 관리자 역할에 할당되었거나 동등한 권한이 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="5a592-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="5a592-109">단위 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="5a592-109">Create a unit group</span></span>

1. <span data-ttu-id="5a592-110">사이트 맵에서 **단위** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="5a592-111">**신규** 를 선택하고 **단위 그룹 만들기** 대화 상자에 단위 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="5a592-112">**기본 단위** 필드에 제품이 판매되는 가장 낮은 단위를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="5a592-113">예를 들어 "조각" 또는 "온스"를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="5a592-114">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="5a592-115">단위 그룹에 단위 추가</span><span class="sxs-lookup"><span data-stu-id="5a592-115">Add units to a unit group</span></span>

1. <span data-ttu-id="5a592-116">단위 그룹을 열고 **관련** 탭에서 **단위** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="5a592-117">기본 단위가 이미 추가되어 있는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="5a592-118">**새 단취 추가** 를 선택하고 **빠른 만들기: 단위** 페이지에서 **이름** 필드에 단위의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="5a592-119">**수량** 필드에 단위에 포함될 수량을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="5a592-120">예를 들어, 한 박스에 2개가 있으면 "2"를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="5a592-121">**기본 단위** 필드에서 단위에 대한 가장 낮은 측정 단위를 설정할 기본 단위를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="5a592-122">예를 들어 "Piece"를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="5a592-123">**저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a592-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]