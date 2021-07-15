---
title: 리소스 사용률 개요
description: 이 항목은 Project Operations에서 리소스 활용도에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367944"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="91991-103">리소스 사용률 개요</span><span class="sxs-lookup"><span data-stu-id="91991-103">Resource utilization overview</span></span>

<span data-ttu-id="91991-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="91991-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91991-105">리소스는 목표 청구 가능 활용도를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91991-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="91991-106">이 목표 활용도는 리소스의 기본 역할에 대한 특성으로 정의되거나 개별 예약 가능 리소스의 레코드에 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="91991-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="91991-107">활용도 계산은 승인된 시간 항목을 사용하여 리소스가 보고한 실제 시간을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="91991-108">활용도를 계산하는 데 다음 공식이 사용됩니다:</span><span class="sxs-lookup"><span data-stu-id="91991-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="91991-109">청구 가능 활용도 = 청구 가능 실제값 시간 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="91991-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="91991-110">청구 가능 활용도 = 청구 타입 ID가 있는 실제값 시간 = 비청구, 보완 또는 사용할 수 없음 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="91991-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="91991-111">내부 = 판매 계약이 없는 실제 시간 ÷ 리소스 능력</span><span class="sxs-lookup"><span data-stu-id="91991-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="91991-112">리소스 능력 = 리소스 작업 시간 – 업무 외 – 휴무일</span><span class="sxs-lookup"><span data-stu-id="91991-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="91991-113">**리소스** 창에서 **리소스 활용도** 보기를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91991-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="91991-114">그리드의 각 셀은 일, 주 또는 월과 같은 기간 동안 리소스의 청구 가능 활용도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91991-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="91991-115">셀을 컬러링하는 데 다음 공식이 사용됩니다:</span><span class="sxs-lookup"><span data-stu-id="91991-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="91991-116">**녹색**: 청구 가능한 사용률 >= 리소스 대상 사용률</span><span class="sxs-lookup"><span data-stu-id="91991-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="91991-117">**노랑**: 대상 사용률 – 20 <= 청구 가능 사용률 < 대상 사용률</span><span class="sxs-lookup"><span data-stu-id="91991-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="91991-118">**빨강**: 청구 가능한 사용률 < 대상 사용률 – 20</span><span class="sxs-lookup"><span data-stu-id="91991-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="91991-119">**리소스 활용도** 보기는 스케줄 보드를 기반으로 하므로 스케줄 보드의 필터링 기능을 사용하여 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91991-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="91991-120">그리드는 귀하가 역할 또는 개별 리소스에 대한 목표 활용도를 설정할 것을 요구합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="91991-121">이 설정을 하려면 **리소스** > **리소스 역할** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="91991-122">또한 기본 역할은 각 예약 가능한 리소스에 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="91991-123">**리소스** > **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="91991-124">**Project Service** 탭에서 리소스 역할이 정의되어 있는지, 리소스 역할에 대한 **기본값임** 이 **예** 로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="91991-125">**기본값임** = **아니요** 인 추가 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91991-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="91991-126">해당 역할의 목표 대비 리소스의 활용도를 평가하기 위해 **기본값임** = **예** 인 역할이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91991-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="91991-127">**Project Service** 탭에서 리소스에 대한 개별 목표 활용도를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91991-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="91991-128">그런 다음 활용도 계산은 해당 목표 활용도를 사용하여 리소스의 기본 역할 목표 대신 리소스의 목표를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="91991-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="91991-129">해당 리소스가 그리드에 표시되는 기간 동안 승인된 청구 가능 시간인 경우에만 리소스에 대한 활용도가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91991-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]