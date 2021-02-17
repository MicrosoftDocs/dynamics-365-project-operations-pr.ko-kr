---
title: 방법을 완료하는 데 드는 비용
description: 이 토픽은 프로젝트 완료 비용을 계산하는 데 사용되는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531484"
---
# <a name="cost-to-complete-methods"></a><span data-ttu-id="b63f7-103">방법을 완료하는 데 드는 비용</span><span class="sxs-lookup"><span data-stu-id="b63f7-103">Cost to complete methods</span></span>

<span data-ttu-id="b63f7-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b63f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b63f7-105">이 토픽은 프로젝트 완료 비용을 계산하는 데 사용되는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-105">This topic provides information about the methods used to calculate the cost to complete a project.</span></span> <span data-ttu-id="b63f7-106">프로젝트 완료 비용을 계산하는 데 사용할 수 있는 여러 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-106">There are multiple methods you can use to calculate the cost to complete a project.</span></span> 

<span data-ttu-id="b63f7-107">프로젝트에 대한 견적을 생성할 때 **추정 만들기** 페이지에서 **방법을 완료하는 데 드는 비용** 필드에서 다음 비용 중 하나를 선택하여 방법을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-107">When you create an estimate for a project, on the **Create estimate** page, in the **Cost to complete method** field, you can select one of the following cost to complete methods.</span></span>

| <span data-ttu-id="b63f7-108">방법을 완료하는 데 드는 비용</span><span class="sxs-lookup"><span data-stu-id="b63f7-108">Cost to complete method</span></span>    | <span data-ttu-id="b63f7-109">설명</span><span class="sxs-lookup"><span data-stu-id="b63f7-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b63f7-110">총 비용-실제</span><span class="sxs-lookup"><span data-stu-id="b63f7-110">Total cost-actual</span></span>            | <span data-ttu-id="b63f7-111">**추정 페이지** 의 **비용 추정** 단추를 사용하여 **총 비용** 또는 **총 수량** 필드에 추정 비용을 수동으로 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-111">Enter estimate costs manually in the **Total cost** or **Total quantity** fields using the **Cost estimate** button on the **Estimate page**.</span></span> <span data-ttu-id="b63f7-112">시스템은 입력한 합계에서 실제 비용을 뺍니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-112">The system subtracts the actual costs from the totals you entered.</span></span> <span data-ttu-id="b63f7-113">총액은 프로젝트를 완료하는 데 드는 비용입니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-113">The total is the cost to complete the project.</span></span> <span data-ttu-id="b63f7-114">이 방법은 Microsoft Dataverse 내에서 Project Operations에 입력된 경비 추정 및 리소스 할당을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-114">This method doesn't use the expense estimates and resources assignments entered in Project Operations built within Microsoft Dataverse.</span></span> <span data-ttu-id="b63f7-115">총 비용 또는 총 수량은 필요에 따라 수동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-115">The total cost or total quantity can be updated manually as needed.</span></span>  |
| <span data-ttu-id="b63f7-116">총 예측-실제</span><span class="sxs-lookup"><span data-stu-id="b63f7-116">Total forecast-actual</span></span>        | <span data-ttu-id="b63f7-117">리소스 할당 및 경비 추정은 총 프로젝트 예측 금액을 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-117">Resource assignments and expense estimates are used to determine the total project forecast amount.</span></span> <span data-ttu-id="b63f7-118">완료 비용을 계산하기 위해 실제 비용을 이 예측과 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-118">Actual costs are compared against this forecast to calculate the cost to complete.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b63f7-119">이전 추정치로</span><span class="sxs-lookup"><span data-stu-id="b63f7-119">As previous estimate</span></span>         | <span data-ttu-id="b63f7-120">이전 기간에 사용된 것과 동일한 추정 방법이 여기에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-120">The same estimate methods that was used in the previous period is used here.</span></span> <span data-ttu-id="b63f7-121">이 방법에는 이전 기간에 예측 모델이 필요했던 경우 예측 모델이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-121">This method requires a forecast model if the previous period required a forecast model.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b63f7-122">완료 비용을 0으로 설정</span><span class="sxs-lookup"><span data-stu-id="b63f7-122">Set cost to complete to zero</span></span> | <span data-ttu-id="b63f7-123">일반적으로 추정 프로젝트가 제거되기 전에 사용되는 이 방법은 총 추정치를 전기된 실제 트랜잭션과 일치시키고 **완료 비용** 열을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-123">Typically used before the estimate project is eliminated, this method matches total estimates with posted actual transactions and clears the **Cost to complete** column.</span></span> <span data-ttu-id="b63f7-124">완료되면 결과는 항상 100%입니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-124">When complete, the result is always 100 percent.</span></span> <span data-ttu-id="b63f7-125">생성하는 각 비용 라인에 대해 **예측** 확인란이 선택 취소되고 총 추정이 이전 비용 추정에서 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-125">For each cost line that you create, the **Forecasting** check box is cleared and the total estimate is copied from the previous cost estimate.</span></span> <span data-ttu-id="b63f7-126">추정 기간의 실제 소비는 프로젝트 완료 비용에서 공제됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-126">The actual consumption for the estimate period is deducted from the cost to complete the project.</span></span>              |
| <span data-ttu-id="b63f7-127">비용 템플릿에서</span><span class="sxs-lookup"><span data-stu-id="b63f7-127">From cost template</span></span>           | <span data-ttu-id="b63f7-128">선택한 견적 프로젝트와 연결된 비용 템플릿에 설정된 완료 비용 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b63f7-128">The cost to complete method that is set up in the cost template that's associated with the selected estimate project.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |