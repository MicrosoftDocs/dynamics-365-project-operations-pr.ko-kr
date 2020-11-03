---
title: 시간 항목 만들기
description: 이 주제는 시간 항목을 만드는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080143"
---
# <a name="create-time-entries"></a><span data-ttu-id="0f484-103">시간 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="0f484-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0f484-104">이전 버전의 Dynamics 365 Project Service Automation에서는 시간 항목이 주별로 입력되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="0f484-105">Project Service Automation의 버전 3에서는 시간 항목이 일별로 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="0f484-106">그러나 소수의 시간 항목을 만든 후 대량으로 만들거나 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="0f484-107">시간 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="0f484-107">Create a time entry</span></span>

<span data-ttu-id="0f484-108">다음 단계에 따라 시간 항목을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0f484-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="0f484-109">**시간 항목** 페이지에서 **신규** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="0f484-110">**빠른 만들기: 시간 항목** 대화 상자에서 시간 입력 기간을 분, 시간 또는 일로 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="0f484-111">기간은 *x* 분, *x* 시간 또는 *x* 일 형식으로 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="0f484-112">시간과 일은 *x.x* 시간 또는 *x.x* 일 같이 소수 자릿수를 사용하여 입력할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="0f484-113">시간 항목 타입과 시간 항목을 입력하는 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="0f484-114">**프로젝트 과업** 필드에서 이 시간 항목에 대한 과업을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f484-115">사용자에게 할당되지 않은 과업에 대한 시간 항목을 만드는 경우, **프로젝트 과업** 필드에서 **검색** 버튼을 선택하고 **보기 변경** 을 선택한 다음, **모든 활성 프로젝트 과업** 을 선택하면 모든 과업이 열거됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="0f484-116">설명이 요구되는 경우 설명을 입력한 다음 **저장 및 닫기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="0f484-117">시간 항목을 만들고 저장한 후 시간 항목 그리드에서 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="0f484-118">시간 항목 그리드는 다음 두 형식을 지원합니다:</span><span class="sxs-lookup"><span data-stu-id="0f484-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="0f484-119">시간 항목을 **hh:mm** 형식으로 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="0f484-120">그런 다음 이 형식은 시간 및 분수로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="0f484-121">시간과 분수를 직접 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="0f484-122">한 시간의 분수가 분이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="0f484-123">따라서 1.5시간은 1시간 30분을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="0f484-124">동일한 규칙이 날의 분수에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="0f484-125">1일은 24시간, 0.5일은 12시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="0f484-126">시간 항목 대량 만들기</span><span class="sxs-lookup"><span data-stu-id="0f484-126">Bulk create time entries</span></span>

<span data-ttu-id="0f484-127">소수의 시간 항목을 만든 후 대량으로 복사하여 추가 시간 항목을 대량으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="0f484-128">**시간 항목** 페이지에서 **주 복사** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="0f484-129">**시작 기간** 필드 그룹의 **시작일** 및 **종료일** 필드에서 시간 항목을 복사할 날짜 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="0f484-130">**끝 기간** 필드 그룹의 **시작일** 필드에서 시간 항목을 만들 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="0f484-131">**복사** 를 선택하여 **끝 기간** 필드 그룹에 지정된 요일에 해당하는 시간 항목의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="0f484-132">예컨대, 지난 주 월요일의 시간 항목은 **끝 기간** 필드 그룹에 지정된 주의 월요일로 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="0f484-133">시간 항목에 대한 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0f484-133">Import data for time entries</span></span>

<span data-ttu-id="0f484-134">프로젝트 예약 및 할당에서 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="0f484-135">데이터를 가져올 때 가져올 예약의 날짜 범위를 지정한 다음 **초안** 시간 항목으로 만들어야 하는 예약을 명시적으로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="0f484-136">그룹화, 정렬, 검색 및 필터 기능</span><span class="sxs-lookup"><span data-stu-id="0f484-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="0f484-137">열에 지정된 차원별로 시간 항목을 그룹화하고 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="0f484-138">**그룹화** 필드에서 시간 항목을 필터링하는 데 사용할 차원을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="0f484-139">열 표제의 정렬 화살표를 사용하여 오름차순 또는 내림차순으로 시간 항목 레코드를 정렬할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="0f484-140">또한 열 표제의 **필터** 버튼을 선택한 다음, **검색** 상자에서 프로젝트 명칭, 프로젝트 과업, 시간 항목 또는 리소스별로 시간 항목을 검색하는 데 사용해야 하는 텍스트를 입력하여 항목을 표시하거나 숨길 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f484-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
