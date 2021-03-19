---
title: 리소스 일정 정의
description: 이 항목은 Project Operations에서 리소스에 대한 근무 시간 달력을 정의하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279821"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="6a129-103">리소스 일정 정의</span><span class="sxs-lookup"><span data-stu-id="6a129-103">Define resource calendars</span></span>

<span data-ttu-id="6a129-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="6a129-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a129-105">프로젝트에서 작업하는 예약 가능한 각 리소스에는 가용성을 정의하기 위한 근무 시간 달력이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="6a129-106">리소스의 근무 시간은 두 가지 방법으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="6a129-107">리소스에 대한 개별 일정 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="6a129-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="6a129-108">리소스에 대한 기존 일정 템플릿 적용</span><span class="sxs-lookup"><span data-stu-id="6a129-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="6a129-109">리소스의 근무 시간 정의</span><span class="sxs-lookup"><span data-stu-id="6a129-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="6a129-110">**리소스** 메뉴에서 **리소스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6a129-111">그리드 보기에서 해당하는 **예약 가능한 리소스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="6a129-112">**리소스 세부 정보** 페이지에서 **근무 시간** 탭을 선택합니다. 기본적으로 예약 가능한 리소스 일정은 조직에 대해 정의된 기본 근무 시간 템플릿의 근무 시간으로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="6a129-113">근무 시간을 업데이트하려면 정의할 제안된 일정 규칙의 시작 날짜를 마우스 오른쪽 버튼으로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="6a129-114">일정 규칙 메뉴를 사용하여 특정 날짜, 나머지 시리즈 또는 전체 일정에 대한 일정 규칙을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="6a129-115">옵션을 선택한 후 다음을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="6a129-116">근무 시간이 적용되는 요일.</span><span class="sxs-lookup"><span data-stu-id="6a129-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="6a129-117">매일 근무 시간.</span><span class="sxs-lookup"><span data-stu-id="6a129-117">The working times within each day.</span></span>
    - <span data-ttu-id="6a129-118">일정 규칙의 표준 시간대.</span><span class="sxs-lookup"><span data-stu-id="6a129-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="6a129-119">해당되는 경우 휴무 시간도 규칙에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="6a129-120">리소스에 일정 템플릿 적용</span><span class="sxs-lookup"><span data-stu-id="6a129-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="6a129-121">**리소스** 메뉴에서 **리소스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6a129-122">그리드 보기에서 업데이트할 최대 25개의 **예약 가능한 리소스** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="6a129-123">**일정 설정** 을 선택하면 사용 가능한 근무 시간 템플릿 목록을 묻는 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="6a129-124">사용할 템플릿을 선택한 다음 **적용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6a129-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]