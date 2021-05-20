---
title: 프로젝트 일정 정의
description: 이 항목은 프로젝트 일정을 추적하기 위해 캘린더 템플릿을 프로젝트에 적용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981308"
---
# <a name="define-project-calendars"></a><span data-ttu-id="7eba4-103">프로젝트 일정 정의</span><span class="sxs-lookup"><span data-stu-id="7eba4-103">Define project calendars</span></span>

<span data-ttu-id="7eba4-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="7eba4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7eba4-105">프로젝트를 만들고 관리하려면 프로젝트에 일정 템플릿을 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="7eba4-106">일정 템플릿은 다음 프로젝트 속성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="7eba4-107">시작 및 종료 시간을 포함한 근무 시간</span><span class="sxs-lookup"><span data-stu-id="7eba4-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="7eba4-108">근무일</span><span class="sxs-lookup"><span data-stu-id="7eba4-108">Working days</span></span>
- <span data-ttu-id="7eba4-109">휴무일과 같은 일정 예외</span><span class="sxs-lookup"><span data-stu-id="7eba4-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="7eba4-110">프로젝트에 적용되는 일정 템플릿은 조직의 설정에 정의된 캘린더 템플릿의 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="7eba4-111">일정 템플릿을 변경하면 해당 변경 사항이 프로젝트의 작업 시간에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="7eba4-112">프로젝트의 근무 시간을 변경하려면 새 템플릿을 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="7eba4-113">조직의 일정 템플릿을 만들려면 두 가지 주요 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="7eba4-114">예약 가능한 신규 또는 기존 리소스를 사용하여 템플릿의 원하는 근무 시간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="7eba4-115">새 일정 템플릿을 만들고 템플릿을 예약 가능한 리소스와 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="7eba4-116">**템플릿의 근무 시간 정의**</span><span class="sxs-lookup"><span data-stu-id="7eba4-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="7eba4-117">**리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="7eba4-118">일정 템플릿에서 참조할 새 리소스를 만들거나 기존 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="7eba4-119">리소스의 **작업 시간** 탭을 선택하고 [리소스에 대한 작업 시간 설정](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)의 지침을 완료하여 일정 규칙을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="7eba4-120">**새 일정 템플릿 만들기**</span><span class="sxs-lookup"><span data-stu-id="7eba4-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="7eba4-121">**설정** \> **일정 템플릿** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="7eba4-122">**새로 만들기** 를 클릭하고 이름, 설명 및 템플릿 리소스를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="7eba4-123">일정 템플릿에서 리소스가 참조되면 리소스 일정의 복사본이 일정 템플릿과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="7eba4-124">복사된 템플릿의 근무 시간이 변경되면 해당 변경 사항이 일정 템플릿에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="7eba4-125">이제 작업 템플릿을 프로젝트 스케줄 템플릿과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eba4-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

