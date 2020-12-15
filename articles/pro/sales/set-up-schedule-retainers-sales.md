---
title: 보유자 일정 설정
description: 이 항목은 Project Operations에서 보유자 일정을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596380"
---
# <a name="set-up-a-retainer-schedule"></a><span data-ttu-id="de8ad-103">보유자 일정 설정</span><span class="sxs-lookup"><span data-stu-id="de8ad-103">Set up a retainer schedule</span></span>

<span data-ttu-id="de8ad-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="de8ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de8ad-105">보유자 일정은 Dynamics 365 Project Operations의 **프로젝트 계약** 페이지에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-105">Retainer schedules are set up on the **Project Contract** page in Dynamics 365 Project Operations.</span></span>

1. <span data-ttu-id="de8ad-106">**프로젝트 계약** 페이지의 **선불금 및 보유자** 탭에서 **보유자 일정 설정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-106">On the **Project Contract** page, on the **Advances and Retainers** tab, select **Set up retainer schedule**.</span></span>
2. <span data-ttu-id="de8ad-107">열리는 대화 페이지에 다음 표에 나열된 필드가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-107">On the dialog page that opens, the fields listed in the following table are shown.</span></span> <span data-ttu-id="de8ad-108">이 표는 입력된 값이 생성될 보유자 일정에 어떤 영향을 미치는지에 대한 아이디어를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-108">The table gives an idea on how the entered values impact or influence the retainer schedule that will be created.</span></span>

| <span data-ttu-id="de8ad-109">필드</span><span class="sxs-lookup"><span data-stu-id="de8ad-109">Field</span></span> | <span data-ttu-id="de8ad-110">설명</span><span class="sxs-lookup"><span data-stu-id="de8ad-110">Description</span></span> | <span data-ttu-id="de8ad-111">다운스트림 영향</span><span class="sxs-lookup"><span data-stu-id="de8ad-111">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="de8ad-112">프로젝트 계약 고객</span><span class="sxs-lookup"><span data-stu-id="de8ad-112">Project Contract Customer</span></span> | <span data-ttu-id="de8ad-113">이 보유자 또는 선불금에 대해 청구될 계약상의 고객입니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-113">The customer on the contract who will be invoiced for this retainer or advance.</span></span> | <span data-ttu-id="de8ad-114">계약에 여러 고객이 있고 각 고객에게 특정 보유자 또는 선불금에 대해 송장을 발행해야 하는 경우 각 고객에 대해 하나의 송장을 수동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-114">If you have multiple customers on the contract, and if you need to invoice each of them for a specific retainer or advance amount, manually create one invoice for each customer.</span></span> |
| <span data-ttu-id="de8ad-115">보유자 일정 시작</span><span class="sxs-lookup"><span data-stu-id="de8ad-115">Retainer Schedule Start</span></span> | <span data-ttu-id="de8ad-116">보유자 일정의 시작 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-116">Enter the start date of the retainer schedule.</span></span> | <span data-ttu-id="de8ad-117">이 날짜는 최초 보유자 또는 선불금이 생성된 날짜가 아닐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-117">This date may not be the date on which the first retainer or advance is created.</span></span> <span data-ttu-id="de8ad-118">첫 번째 보유자 또는 선불금이 생성된 날짜도 송장 빈도의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-118">The date on which the first retainer or advance is created, is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="de8ad-119">보유자 일정 종료</span><span class="sxs-lookup"><span data-stu-id="de8ad-119">Retainer Schedule End</span></span> | <span data-ttu-id="de8ad-120">보유자 일정의 종료 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-120">Enter the end date of the retainer schedule.</span></span> | <span data-ttu-id="de8ad-121">이 날짜는 마지막 보유자 또는 선불금이 생성된 날짜가 아닐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-121">This date may not be the date on which the last retainer or advance is created.</span></span> <span data-ttu-id="de8ad-122">마지막 보유자 또는 선불금이 생성된 날짜도 송장 빈도의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-122">The date on which the last retainer or advance is created is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="de8ad-123">만들 보유자 수</span><span class="sxs-lookup"><span data-stu-id="de8ad-123">Number of Retainers to Create</span></span> | <span data-ttu-id="de8ad-124">생성할 보유자 수를 입력하면 시스템은 시작 날짜와 빈도를 사용하여 이 필드에 번호를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-124">When you enter the number of retainers to create, the system uses the start date and frequency to create the number in this field.</span></span> | <span data-ttu-id="de8ad-125">이 필드를 수동으로 업데이트하면 시스템은 **보류자 일정 종료** 필드의 값을 무시하고 대신 특정 수의 보유자 또는 선불금을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-125">When this field is manually updated, the system ignores the value in the **Retainer Schedule End** field and instead creates the specific number of retainers or advances.</span></span> |
| <span data-ttu-id="de8ad-126">송장 빈도</span><span class="sxs-lookup"><span data-stu-id="de8ad-126">Invoice Frequency</span></span> | <span data-ttu-id="de8ad-127">애플리케이션이 보유자와 선불금을 생성하는 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-127">How often the application will create retainers and advances.</span></span> | <span data-ttu-id="de8ad-128">이 값은 보유자 및 선불금 수와 생성 날짜에 직접적인 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-128">This value directly influences the number of retainers and advances and the created dates.</span></span> |
| <span data-ttu-id="de8ad-129">총 금액</span><span class="sxs-lookup"><span data-stu-id="de8ad-129">Total Amount</span></span> | <span data-ttu-id="de8ad-130">총 금액은 개별 보유자 또는 선불금으로 분할되는 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-130">The total amount is the amount that is split into the individual retainer or advance payments that will be created.</span></span> | <span data-ttu-id="de8ad-131">이 필드에 대한 다운스트림 영향은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="de8ad-131">There's no downstream impact for this field.</span></span> |
