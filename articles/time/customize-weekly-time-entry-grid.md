---
title: 시간 항목 연장
description: 이 항목은 개발자가 시간 입력 제어를 확장할 수 있는 방법에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930888"
---
# <a name="extending-time-entries"></a><span data-ttu-id="fa323-103">시간 항목 연장</span><span class="sxs-lookup"><span data-stu-id="fa323-103">Extending time entries</span></span>

<span data-ttu-id="fa323-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="fa323-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa323-105">Dynamics 365 Project Operations에는 확장 가능한 시간 항목 사용자 지정 컨트롤이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="fa323-106">이 컨트롤에는 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-106">This control includes the following features:</span></span>

- <span data-ttu-id="fa323-107">1주일 동안 가로로 시간 입력</span><span class="sxs-lookup"><span data-stu-id="fa323-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="fa323-108">일, 행 또는 주별 합계</span><span class="sxs-lookup"><span data-stu-id="fa323-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="fa323-109">행 또는 주 복사</span><span class="sxs-lookup"><span data-stu-id="fa323-109">Copy rows or weeks</span></span>
- <span data-ttu-id="fa323-110">HH:mm 또는 HH.hh를 통한 시간 항목(HH.hh로 자동 변환)</span><span class="sxs-lookup"><span data-stu-id="fa323-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="fa323-111">할당, 예약 또는 약속에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="fa323-111">Import from assignments, bookings or appointments</span></span>

<span data-ttu-id="fa323-112">시간 항목 연장은 다음 두 영역에서 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="fa323-113">자신의 용도에 맞게 사용자 지정 시간 항목 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="fa323-114">주간 시간 항목 컨트롤 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="fa323-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="fa323-115">자신의 용도에 맞게 사용자 지정 시간 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-115">Add custom time entries for your own use.</span></span>

<span data-ttu-id="fa323-116">시간 항목은 여러 시나리오에 사용되도록 설계된 핵심 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-116">Time entries are a core entity that is designed to be used for multiple scenarios.</span></span> <span data-ttu-id="fa323-117">2020년 4월 Wave 1에서 **설정** 엔터티와 새로운 **시간 항목 사용자** 보안 역할을 제공하는 TESA 핵심 솔루션이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-117">In April Wave 1 2020, the TESA core solution was introduced, which provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="fa323-118">**msdyn_duration**과 직접적인 관련이 있는 새로운 필드, **msdyn_start** 및 **msdyn_end**도 포함되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-118">The new fields, **msdyn_start** and **msdyn_end** which have a direct relation to **msdyn_duration**, were also included.</span></span> <span data-ttu-id="fa323-119">새로운 엔터티인 보안 역할 및 필드를 사용하면 여러 제품에서 시간에 대한 보다 통합된 접근 방식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-119">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="fa323-120">시간 원본 엔터티</span><span class="sxs-lookup"><span data-stu-id="fa323-120">Time Source Entity</span></span>
| <span data-ttu-id="fa323-121">필드</span><span class="sxs-lookup"><span data-stu-id="fa323-121">Field</span></span> | <span data-ttu-id="fa323-122">설명</span><span class="sxs-lookup"><span data-stu-id="fa323-122">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="fa323-123">Name</span><span class="sxs-lookup"><span data-stu-id="fa323-123">Name</span></span>  | <span data-ttu-id="fa323-124">시간 항목을 만드는 동안 선택 값으로 사용되는 시간 원본 항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-124">The name of the Time Source entry used as the selection value during time entry creation.</span></span> |
| <span data-ttu-id="fa323-125">기본 시간 원본[시간 원본: isdefault]</span><span class="sxs-lookup"><span data-stu-id="fa323-125">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="fa323-126">기본적으로 하나의 시간 원본만 기본 시간 원본에 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-126">By default, only one Time Source may be marked at the default time source.</span></span> <span data-ttu-id="fa323-127">이 기능을 사용하면 항목이 지정되지 않은 경우 기본적으로 시간 원본을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-127">This capability allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="fa323-128">시간 원본 유형[시간 원본: sourcetype]</span><span class="sxs-lookup"><span data-stu-id="fa323-128">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="fa323-129">원본 유형은 시간 원본을 앱에 연결할 수 있는 옵션(시간 항목 원본 유형)입니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-129">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="fa323-130">추가 애플리케이션이 추가되면 이 옵션 집합에 추가 값이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-130">Additional values will be added to this option set as additional applications are added.</span></span> <span data-ttu-id="fa323-131">Microsoft는 190,000,000보다 큰 값을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-131">Note that Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="fa323-132">시간 항목 및 시간 원본 엔터티</span><span class="sxs-lookup"><span data-stu-id="fa323-132">Time entries and the Time Source Entity</span></span>
<span data-ttu-id="fa323-133">각 시간 항목은 시간 원본 레코드에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="fa323-134">이 레코드는 시간 항목을 처리하는 방법과 애플리케이션을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="fa323-135">시간 항목은 항상 시작, 종료 및 기간이 연결된 하나의 연속된 시간 블록입니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="fa323-136">논리는 다음 상황에서 시간 항목 레코드를 자동으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="fa323-137">다음 세 필드 중 두 개가 제공되면 세 번째 필드가 자동으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-137">If two of the three following fields are provided, the third is calculated automatically</span></span> 

    - <span data-ttu-id="fa323-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="fa323-138">**msdyn_start**</span></span>
    - <span data-ttu-id="fa323-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="fa323-139">**msdyn_end**</span></span>
    - <span data-ttu-id="fa323-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="fa323-140">**msdyn_duration**</span></span>

- <span data-ttu-id="fa323-141">필드, **msdyn_start** 및 **msdyn_end**는 시간대를 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="fa323-142">**msdyn_date** 및 **msdyn_duration**만 지정하여 생성된 시간 항목은 자정에 시작되고 **msdyn_start** 및 **msdyn_end**는 그에 따라 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight, and **msdyn_start** and **msdyn_end** will be updated accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="fa323-143">시간 항목 유형</span><span class="sxs-lookup"><span data-stu-id="fa323-143">Time entry types</span></span>

<span data-ttu-id="fa323-144">시간 항목 레코드에는 관련 애플리케이션에 대한 제출 흐름의 동작을 정의하는 관련 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-144">Time entry records have an associated type that defines behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="fa323-145">레이블</span><span class="sxs-lookup"><span data-stu-id="fa323-145">Label</span></span> | <span data-ttu-id="fa323-146">값</span><span class="sxs-lookup"><span data-stu-id="fa323-146">Value</span></span>|
|-----|-----|
|<span data-ttu-id="fa323-147">휴식 중</span><span class="sxs-lookup"><span data-stu-id="fa323-147">On break</span></span>   |<span data-ttu-id="fa323-148">192,355,000</span><span class="sxs-lookup"><span data-stu-id="fa323-148">192,355,000</span></span>|
|<span data-ttu-id="fa323-149">여행</span><span class="sxs-lookup"><span data-stu-id="fa323-149">Travel</span></span> | <span data-ttu-id="fa323-150">192,355,001</span><span class="sxs-lookup"><span data-stu-id="fa323-150">192,355,001</span></span>|
|<span data-ttu-id="fa323-151">초과 근무</span><span class="sxs-lookup"><span data-stu-id="fa323-151">Overtime</span></span>   | <span data-ttu-id="fa323-152">192,354,320</span><span class="sxs-lookup"><span data-stu-id="fa323-152">192,354,320</span></span>|
|<span data-ttu-id="fa323-153">근무</span><span class="sxs-lookup"><span data-stu-id="fa323-153">Work</span></span>   | <span data-ttu-id="fa323-154">192,350,000</span><span class="sxs-lookup"><span data-stu-id="fa323-154">192,350,000</span></span>|
|<span data-ttu-id="fa323-155">결근</span><span class="sxs-lookup"><span data-stu-id="fa323-155">Absence</span></span>    | <span data-ttu-id="fa323-156">192,350,001</span><span class="sxs-lookup"><span data-stu-id="fa323-156">192,350,001</span></span>|
|<span data-ttu-id="fa323-157">휴가</span><span class="sxs-lookup"><span data-stu-id="fa323-157">Vacation</span></span>   | <span data-ttu-id="fa323-158">192,350,002</span><span class="sxs-lookup"><span data-stu-id="fa323-158">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="fa323-159">주간 시간 항목 컨트롤 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="fa323-159">Customize the weekly Time Entry control</span></span>
<span data-ttu-id="fa323-160">개발자는 다른 엔터티에 추가 필드 및 조회를 추가하고 사용자 지정 비즈니스 규칙을 구현하여 비즈니스 시나리오를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-160">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="fa323-161">다른 엔터티에 조회가 있는 사용자 지정 필드 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-161">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="fa323-162">주간 시간 입력 표에 사용자 지정 필드를 추가하는 세 가지 주요 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-162">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

- <span data-ttu-id="fa323-163">빠른 만들기 대화 상자에 사용자 지정 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-163">Add the custom field to the quick create dialog box.</span></span>
- <span data-ttu-id="fa323-164">사용자 지정 필드를 표시하도록 표를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-164">Configure the grid to show the custom field.</span></span>
- <span data-ttu-id="fa323-165">행 편집 작업 흐름 또는 셀 편집 작업 흐름에 사용자 지정 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-165">Add the custom field to either the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="fa323-166">또한 새 필드에 행 또는 셀 편집 작업 흐름에 필요한 유효성 검사가 있는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-166">You must also make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="fa323-167">이 단계의 일부로 시간 입력 상태에 따라 필드를 잠가야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-167">As part of this step, you must lock the field based on the time entry status.</span></span>

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="fa323-168">빠른 만들기 대화 상자에 사용자 지정 필드 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-168">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="fa323-169">사용자 지정 필드를 **시간 항목 빠른 만들기** 대화 상자에 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-169">You must add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="fa323-170">사용자는 **새로 만들기**를 선택하여 시간 항목을 추가할 때 값을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-170">Users can then enter a value when they add time entries by selecting **New**.</span></span>

#### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="fa323-171">사용자 지정 필드를 표시하도록 표 구성</span><span class="sxs-lookup"><span data-stu-id="fa323-171">Configure the grid to show the custom field</span></span>
<span data-ttu-id="fa323-172">주간 시간 입력 표에 사용자 지정 필드를 추가하는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-172">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="fa323-173">보기 사용자 지정 및 사용자 지정 필드 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-173">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="fa323-174">새 기본 사용자 지정 시간 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="fa323-174">Create a new default custom time entry</span></span> 


<span data-ttu-id="fa323-175">**보기 사용자 지정 및 사용자 지정 필드 추가**</span><span class="sxs-lookup"><span data-stu-id="fa323-175">**Customize a view and add a custom field**</span></span>

<span data-ttu-id="fa323-176">**내 주간 시간 항목** 보기를 사용자 지정하고 사용자 지정 필드를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-176">You can customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="fa323-177">보기에서 해당 속성을 편집하여 표에서 사용자 지정 필드의 위치와 크기를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-177">You can choose the position and size of the custom field in the grid by editing those properties in the view.</span></span>

<span data-ttu-id="fa323-178">**새 기본 사용자 지정 시간 항목 만들기**</span><span class="sxs-lookup"><span data-stu-id="fa323-178">**Create a new default custom time entry**</span></span> 

<span data-ttu-id="fa323-179">이 보기에는 표에 포함하려는 열 외에 **설명** 및 **외부 주석** 필드가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-179">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="fa323-180">보기에서 해당 속성을 편집하여 표에서 사용자 지정 필드의 위치, 크기 및 기본 정렬 순서를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-180">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="fa323-181">**시간 항목 표** 컨트롤이 되도록 이 보기에 대한 사용자 지정 컨트롤을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-181">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="fa323-182">이 컨트롤을 보기에 추가하고 웹, 휴대폰 및 태블릿용으로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-182">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="fa323-183">주간 시간 항목 표에 대한 매개 변수를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-183">Configure the parameters for the weekly time entry grid.</span></span> <span data-ttu-id="fa323-184">**시작 날짜** 필드를 **msdyn_date**로 설정하고 **기간 필드**를 **msdyn_duration**으로 설정하고 **상태** 필드를 **msdyn_entrystatus**로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-184">Set the **Start Date** field to **msdyn_date**, set the **Duration** field to **msdyn_duration**, and set the **Status** field to **msdyn_entrystatus**.</span></span> 
5. <span data-ttu-id="fa323-185">기본 보기의 경우 **읽기 전용 상태 목록** 필드가 **192350002,192350003,192350004**로 설정되어 있으며 **행 편집 작업 흐름** 필드가 **msdyn_timeentryrowedit**으로 설정되고 **셀 편집 작업 흐름** 필드는 **msdyn_timeentryedit**로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-185">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**, the **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**, and the **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
6. <span data-ttu-id="fa323-186">이러한 필드를 사용자 지정하여 읽기 전용 상태를 추가 또는 제거하거나 행 또는 셀 편집에 다른 TBX(작업 기반 환경)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-186">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="fa323-187">이러한 필드는 정적 값에 바인딩되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-187">These fields should be bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="fa323-188">두 옵션 모두 **프로젝트** 및 **프로젝트 작업** 엔터티에서 일부 즉시 필터링을 제거하므로 엔터티에 대한 모든 조회 보기가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-188">Both options will remove some out-of-box filtering on **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="fa323-189">즉시 관련 조회 보기만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-189">Out-of-the-box, only the relevant lookup views are visible.</span></span>
<span data-ttu-id="fa323-190">사용자 지정 필드에 적합한 작업 흐름을 결정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-190">You must determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="fa323-191">대부분의 경우 표에 필드를 추가한 경우 시간 항목의 전체 행에 적용되는 필드에 사용되는 행 편집 작업 흐름으로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-191">Most likely, if you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="fa323-192">사용자 지정 필드에 **끝 시간**에 대한 사용자 지정 필드와 같은 매일 고유한 값이 있는 경우 셀 편집 작업 흐름으로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-192">If the custom field has a unique value every day, such as a custom field for **End time**, it should go in the cell edit task flow.</span></span>

<span data-ttu-id="fa323-193">작업 흐름에 사용자 지정 필드를 추가하려면 **필드** 요소를 페이지의 적절한 위치로 끌어온 다음 필드 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-193">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="fa323-194">**소스** 속성을 **시간 항목**으로 설정하고 **데이터 필드** 속성을 사용자 지정 필드로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-194">Set the **Source** property to **Time Entry**, and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="fa323-195">**필드** 속성은 TBX 페이지에서 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-195">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="fa323-196">**적용**을 선택하여 변경 사항을 필드에 저장한 다음 **업데이트**를 선택하여 페이지에 대한 변경 사항을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-196">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="fa323-197">대신 새 사용자 지정 TBX 페이지를 사용하려면 새 프로세스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-197">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="fa323-198">범주를 **비즈니스 프로세스 흐름**으로 설정하고, 엔터티를 **시간 항목**으로 설정하고, 비즈니스 프로세스 유형을 **작업 흐름으로 프로세스 실행**으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-198">Set the category to **Business Process Flow**, set the entity to **Time Entry**, and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="fa323-199">**속성**에서 **페이지 이름** 속성은 페이지의 표시 이름 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-199">Under **Properties**, the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="fa323-200">TBX 페이지에 모든 관련 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-200">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="fa323-201">프로세스를 저장하고 활성화한 다음 관련 작업 흐름에 대한 사용자 지정 제어 속성을 프로세스의 **이름** 값으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-201">Save and activate the process, and then update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="fa323-202">새 옵션 집합 값 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-202">Add new option set values</span></span>
<span data-ttu-id="fa323-203">옵션 집합 값을 즉시 입력 필드에 추가하려면 필드의 편집 페이지를 연 다음 **유형**에서 옵션 집합 옆에 **편집**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-203">To add option set values to an out-of-box field, open the editing page for the field, and then, under **Type**, select **Edit** next to the option set.</span></span> <span data-ttu-id="fa323-204">그런 다음 사용자 지정 레이블과 색상이 있는 새 옵션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-204">Next, add a new option that has a custom label and color.</span></span> <span data-ttu-id="fa323-205">새 시간 입력 상태를 추가하려는 경우 즉시 입력 필드라는 이름이**항목 상태**가 아닌 **상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-205">If you want to add a new time entry status, the out-of-box field is named **Entry Status**, not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="fa323-206">새 시간 입력 상태를 읽기 전용으로 지정</span><span class="sxs-lookup"><span data-stu-id="fa323-206">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="fa323-207">새 시간 입력 상태를 읽기 전용으로 지정하려면 새 시간 입력 값을 **읽기 전용 상태 목록** 속성에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-207">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="fa323-208">시간 항목 표의 편집 가능한 부분은 새 상태가 있는 행에 대해 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-208">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="fa323-209">그런 다음 비즈니스 규칙을 추가하여 **시간 항목 행 편집** 및 **시간 항목 편집** TBX 페이지의 모든 필드를 잠금니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-209">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="fa323-210">페이지의 비즈니스 프로세스 흐름 편집기에서 열고 **비즈니스 규칙**을 선택하여 이러한 페이지의 비즈니스 규칙에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-210">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="fa323-211">기존 비즈니스 규칙의 조건에 새 상태를 추가하거나 새 상태에 대한 새 비즈니스 규칙을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-211">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="fa323-212">사용자 지정 유효성 검사 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="fa323-212">Add custom validation rules</span></span>
<span data-ttu-id="fa323-213">주간 시간 입력 표 경험에 대해 추가할 수 있는 두 가지 유형의 유효성 검사 규칙이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-213">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="fa323-214">빨리 만들기 대화 상자 및 TBX 페이지에서 작동하는 클라이언트 측 비즈니스 규칙.</span><span class="sxs-lookup"><span data-stu-id="fa323-214">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="fa323-215">모든 시간 항목 업데이트에 적용되는 서버 측 플러그인 유효성 검사.</span><span class="sxs-lookup"><span data-stu-id="fa323-215">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="fa323-216">비즈니스 규칙</span><span class="sxs-lookup"><span data-stu-id="fa323-216">Business rules</span></span>
<span data-ttu-id="fa323-217">비즈니스 규칙을 사용하여 필드를 잠그고 잠금을 해제하고, 필드에 기본값을 입력하고, 현재 시간 입력 레코드의 정보만 필요한 유효성 검사를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-217">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="fa323-218">페이지의 비즈니스 프로세스 흐름 편집기에서 열고 **비즈니스 규칙**을 선택하여 TBX 페이지의 비즈니스 규칙에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-218">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="fa323-219">그런 다음 기존 비즈니스 규칙을 편집하거나 새 비즈니스 규칙을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-219">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="fa323-220">더 많은 사용자 지정 유효성 검사를 위해 비즈니스 규칙을 사용하여 JavaScript를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-220">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="fa323-221">플러그 인 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="fa323-221">Plug-in validations</span></span>
<span data-ttu-id="fa323-222">단일 시간 항목 레코드에서 사용할 수 있는 것보다 더 많은 컨텍스트가 필요한 유효성 검사 또는 표의 인라인 업데이트에서 실행하려는 유효성 검사에 플러그 인 유효성 검사를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-222">You should use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="fa323-223">유효성 검사를 완료하려면 **시간 항목** 엔터티에 사용자 지정 플러그 인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa323-223">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>
