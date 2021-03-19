---
title: iOS 및 Android의 Microsoft Dynamics 365 Project Timesheet 모바일 앱에 대한 사용자 지정 필드 구현
description: 이 항목은 확장을 사용하여 사용자 지정 필드를 구현하기 위한 공통 패턴을 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271001"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="03bf3-103">iOS 및 Android의 Microsoft Dynamics 365 Project Timesheet 모바일 앱에 대한 사용자 지정 필드 구현</span><span class="sxs-lookup"><span data-stu-id="03bf3-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03bf3-104">이 항목은 확장을 사용하여 사용자 지정 필드를 구현하기 위한 공통 패턴을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="03bf3-105">다음 주제를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-105">The following topics are covered:</span></span>

- <span data-ttu-id="03bf3-106">사용자 지정 필드 프레임워크가 지원하는 다양한 데이터 유형</span><span class="sxs-lookup"><span data-stu-id="03bf3-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="03bf3-107">작업 표 항목에 읽기 전용 또는 편집 가능한 필드를 표시하고 사용자가 제공한 값을 다시 데이터베이스에 저장하는 방법</span><span class="sxs-lookup"><span data-stu-id="03bf3-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="03bf3-108">작업 표 머리글에 읽기 전용 필드를 표시하는 방법</span><span class="sxs-lookup"><span data-stu-id="03bf3-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="03bf3-109">다른 사용자 지정 비즈니스 논리를 통합하여 필드에 기본값을 입력하고 추가 유효성 검사를 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="03bf3-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="03bf3-110">대상</span><span class="sxs-lookup"><span data-stu-id="03bf3-110">Audience</span></span>

<span data-ttu-id="03bf3-111">이 항목은 사용자 지정 필드를 Apple iOS 및 Google Android에서 사용할 수 있는 Microsoft Dynamics 365 Project Timesheet 모바일 애플리케이션에 통합하는 개발자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="03bf3-112">독자가 X++ 개발 및 프로젝트 타임시트 기능에 익숙하다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="03bf3-113">데이터 계약 – TSTimesheetCustomField X++ 클래스</span><span class="sxs-lookup"><span data-stu-id="03bf3-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="03bf3-114">**TSTimesheetCustomField** 클래스는 작업 표 기능에 대한 사용자 지정 필드에 대한 정보를 나타내는 X++ 데이터 계약 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="03bf3-115">사용자 지정 필드 개체 목록은 TSTimesheetDetails 데이터 계약 및 TSTimesheetEntry 데이터 계약 모두에 전달되어 모바일 앱에 사용자 지정 필드를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="03bf3-116">**TSTimesheetDetails** - 작업 표 헤더 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="03bf3-117">**TSTimesheetEntry** - 작업 표 트랜잭션 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="03bf3-118">동일한 프로젝트 정보 및 **timesheetLineRecId** 값을 가진 이러한 개체 그룹이 선을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="03bf3-119">fieldBaseType(유형)</span><span class="sxs-lookup"><span data-stu-id="03bf3-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="03bf3-120">**TsTimesheetCustom** 개체의 **FieldBaseType** 속성은 앱에 표시되는 필드의 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="03bf3-121">다음과 같은 **유형** 값이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="03bf3-122">유형 값</span><span class="sxs-lookup"><span data-stu-id="03bf3-122">Types value</span></span> | <span data-ttu-id="03bf3-123">형식</span><span class="sxs-lookup"><span data-stu-id="03bf3-123">Type</span></span>              | <span data-ttu-id="03bf3-124">메모 </span><span class="sxs-lookup"><span data-stu-id="03bf3-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="03bf3-125">12</span><span class="sxs-lookup"><span data-stu-id="03bf3-125">0</span></span>           | <span data-ttu-id="03bf3-126">문자열 (및 열거형)</span><span class="sxs-lookup"><span data-stu-id="03bf3-126">String (and Enum)</span></span> | <span data-ttu-id="03bf3-127">필드는 텍스트 필드로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="03bf3-128">6</span><span class="sxs-lookup"><span data-stu-id="03bf3-128">1</span></span>           | <span data-ttu-id="03bf3-129">Integer</span><span class="sxs-lookup"><span data-stu-id="03bf3-129">Integer</span></span>           | <span data-ttu-id="03bf3-130">값은 소수점이 없는 숫자로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="03bf3-131">2</span><span class="sxs-lookup"><span data-stu-id="03bf3-131">2</span></span>           | <span data-ttu-id="03bf3-132">실수</span><span class="sxs-lookup"><span data-stu-id="03bf3-132">Real</span></span>              | <span data-ttu-id="03bf3-133">값은 소수점이 있는 숫자로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="03bf3-134">앱에서 실제 가치를 통화로 표시하려면 **fieldExtenededType** 속성을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="03bf3-135">**numberOfDecimals** 속성을 사용하여 표시되는 소수 자릿수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="03bf3-136">3</span><span class="sxs-lookup"><span data-stu-id="03bf3-136">3</span></span>           | <span data-ttu-id="03bf3-137">Date</span><span class="sxs-lookup"><span data-stu-id="03bf3-137">Date</span></span>              | <span data-ttu-id="03bf3-138">날짜 형식은 **사용자 옵션** 의 **언어 및 국가/지역 기본 설정** 아래에 지정된 사용자의 **날짜, 시간 및 숫자 형식** 설정에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="03bf3-139">4</span><span class="sxs-lookup"><span data-stu-id="03bf3-139">4</span></span>           | <span data-ttu-id="03bf3-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="03bf3-140">Boolean</span></span>           | |
| <span data-ttu-id="03bf3-141">15</span><span class="sxs-lookup"><span data-stu-id="03bf3-141">15</span></span>          | <span data-ttu-id="03bf3-142">GUID</span><span class="sxs-lookup"><span data-stu-id="03bf3-142">GUID</span></span>              | |
| <span data-ttu-id="03bf3-143">16</span><span class="sxs-lookup"><span data-stu-id="03bf3-143">16</span></span>          | <span data-ttu-id="03bf3-144">Int64</span><span class="sxs-lookup"><span data-stu-id="03bf3-144">Int64</span></span>             | |

- <span data-ttu-id="03bf3-145">**TSTimesheetCustomField** 개체에서 **stringOptions** 속성이 제공되지 않는 경우 자유 텍스트 필드가 사용자에게 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="03bf3-146">**stringLength** 속성을 사용하여 사용자가 입력할 수 있는 최대 문자열 길이를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="03bf3-147">**TSTimesheetCustomField** 개체에 **stringOptions** 속성이 제공되는 경우 이러한 목록 요소는 사용자가 옵션 단추(라디오 단추)를 사용하여 선택할 수 있는 유일한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="03bf3-148">이 경우 문자열 필드는 사용자 입력을 위한 열거형 값 역할을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="03bf3-149">값을 열거형으로 데이터베이스에 저장하려면 명령 체인을 사용하여 데이터베이스에 저장하기 전에 문자열 값을 다시 열거형 값에 수동으로 매핑합니다(예를 보려면 이 항목 뒷부분의 "TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 다시 데이터베이스에 저장" 섹션 참조).</span><span class="sxs-lookup"><span data-stu-id="03bf3-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="03bf3-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="03bf3-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="03bf3-151">이 속성을 사용하여 실제 값을 통화로 형식화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="03bf3-152">이 접근 방식은 **fieldBaseType** 값이 **실수** 일 때만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="03bf3-153">**TSCustomFieldExtendedType:None** – 서식이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="03bf3-154">**TSCustomFieldExtendedType::Currency** – 값을 통화로 형식화합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="03bf3-155">통화 형식이 활성화되면 **stringValue** 필드는 앱에 표시되어야 하는 통화 코드를 전달하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="03bf3-156">값은 읽기 전용 값입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-156">The value is a read-only value.</span></span>

    <span data-ttu-id="03bf3-157">**realValue** 필드에는 데이터베이스에 저장해야 하는 금액이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="03bf3-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="03bf3-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="03bf3-159">이 속성을 사용하여 앱에서 사용자 지정 필드가 표시되어야 하는 위치를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="03bf3-160">**TSCustomFieldSection::Header** – 필드가 앱의 **자세히 보기** 섹션에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="03bf3-161">이러한 필드는 항상 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-161">These fields are always read-only.</span></span>
- <span data-ttu-id="03bf3-162">**TSCustomFieldSection::Line** – 이 필드는 작업 표 항목의 모든 기본 제공 라인 필드 뒤에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="03bf3-163">이러한 필드는 편집 가능하거나 읽기 전용일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="03bf3-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="03bf3-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="03bf3-165">이 속성은 앱이 제공하는 값이 데이터베이스에 다시 저장될 때 필드를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="03bf3-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="03bf3-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="03bf3-167">이 속성은 앱이 제공하는 값이 데이터베이스에 다시 저장될 때 필드를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="03bf3-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="03bf3-168">isEditable (NoYes)</span></span>

<span data-ttu-id="03bf3-169">이 속성을 **예** 로 설정하여 작업 표 입력 섹션의 필드를 사용자가 편집할 수 있도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="03bf3-170">필드를 읽기 전용으로 만들려면 속성을  **No** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="03bf3-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="03bf3-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="03bf3-172">이 속성을 **예** 로 설정하여 작업 표 입력 섹션의 필드를 필수로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="03bf3-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="03bf3-173">label (str)</span></span>

<span data-ttu-id="03bf3-174">이 속성은 앱의 필드 옆에 표시되는 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="03bf3-175">stringOptions (문자열 목록)</span><span class="sxs-lookup"><span data-stu-id="03bf3-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="03bf3-176">이 속성은 **fieldBaseType** 이 **String** 으로 설정된 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="03bf3-177">**stringOptions** 이 설정된 경우 옵션 단추(라디오 단추)를 통해 선택할 수 있는 문자열 값은 목록의 문자열로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="03bf3-178">문자열이 제공되지 않으면 문자열 필드에 자유 텍스트 항목이 허용됩니다(예를 보려면 이 항목 뒷부분의 "TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 데이터베이스에 다시 저장" 섹션 참조).</span><span class="sxs-lookup"><span data-stu-id="03bf3-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="03bf3-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="03bf3-179">stringLength (int)</span></span>

<span data-ttu-id="03bf3-180">이 속성은 문자열 필드의 최대 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="03bf3-181">**fieldBaseType** 이 **String** 으로 설정된 경우에만 적용됩니다. </span><span class="sxs-lookup"><span data-stu-id="03bf3-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="03bf3-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="03bf3-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="03bf3-183">이 속성은 실수 필드에 대해 표시되는 소수 자릿수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="03bf3-184">**fieldBaseType** 이 **Real** 로 설정된 경우에만 적용됩니다. </span><span class="sxs-lookup"><span data-stu-id="03bf3-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="03bf3-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="03bf3-185">orderSequence (int)</span></span>

<span data-ttu-id="03bf3-186">이 속성은 둘 이상의 사용자 지정 필드가 지정된 경우 사용자 지정 필드가 앱에 표시되는 순서를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="03bf3-187">숫자가 더 낮은 필드가 먼저 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="03bf3-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="03bf3-188">booleanValue (boolean)</span></span>

<span data-ttu-id="03bf3-189">**Boolean** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 부울 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="03bf3-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="03bf3-190">guidValue (guid)</span></span>

<span data-ttu-id="03bf3-191">**GUID** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 GUID(Globally Unique Identifier) 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="03bf3-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="03bf3-192">int64Value (int64)</span></span>

<span data-ttu-id="03bf3-193">**Int64** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 Int64 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="03bf3-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="03bf3-194">intValue (int)</span></span>

<span data-ttu-id="03bf3-195">**Int** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 정수 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="03bf3-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="03bf3-196">realValue (real)</span></span>

<span data-ttu-id="03bf3-197">**Real** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 실수 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="03bf3-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="03bf3-198">stringValue (str)</span></span>

<span data-ttu-id="03bf3-199">**String** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 문자열 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="03bf3-200">통화로 형식이 지정된 **Real** 유형의 필드에도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="03bf3-201">이러한 필드의 경우 속성은 통화 코드를 앱에 전달하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="03bf3-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="03bf3-202">dateValue (date)</span></span>

<span data-ttu-id="03bf3-203">**Date** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 날짜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="03bf3-204">작업 표 입력 섹션에 사용자 지정 필드 표시 및 저장</span><span class="sxs-lookup"><span data-stu-id="03bf3-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="03bf3-205">아래는 작업 표 항목 생성의 모바일 앱 스크린샷입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="03bf3-206">"두 번째 옵션" 열거형 값이 이미 설정된 "테스트 문자열"이라는 "시간 항목" 섹션의 기본 필드와 사용자 지정 필드가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![앱의 테스트 문자열 사용자 지정 필드](media/timesheet-entry.jpg)



<span data-ttu-id="03bf3-208">아래는 "테스트 문자열" 사용자 지정 필드에 사용할 수 있는 열거형 옵션 중 하나를 선택하는 사용자의 모바일 앱 스크린샷입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="03bf3-209">두 가지 옵션은 라디오 단추로 표시된 "첫 번째 옵션"과 "두 번째 옵션"입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="03bf3-210">두 번째 옵션이 현재 선택되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-210">The second option is currently selected.</span></span>

![테스트 문자열 사용자 지정 필드에 대한 옵션 단추(라디오 단추)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="03bf3-212">사용자 지정 필드를 갖도록 TSTimesheetLine 테이블 확장</span><span class="sxs-lookup"><span data-stu-id="03bf3-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="03bf3-213">일반적인 시나리오에서는 작업 표 입력 섹션의 사용자 지정 필드에 대한 데이터가 TSTimesheetLine 테이블에 저장될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="03bf3-214">그러나 제공된 TSTimesheetTrans 레코드를 기반으로 데이터를 검색할 수 있거나 특정 레코드 컨텍스트가 없는 경우(예: 필드가 프로젝트 매개 변수에서 읽기 전용으로 설정된 경우) 다른 테이블을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="03bf3-215">사용자 지정 필드에는 백업 데이터베이스 레코드가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="03bf3-216">X++ 로직을 기반으로 동적으로 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="03bf3-217">이 접근 방식은 읽기 전용 시나리오에서 유용할 수 있습니다(동적으로 생성된 사용자 지정 필드 값의 예는 "TSTimesheetDetails 클래스의 명령 체인, buildCustomFieldListForHeader 메서드를 사용하여 작업 표 세부 정보 채우기"섹션 참조).</span><span class="sxs-lookup"><span data-stu-id="03bf3-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="03bf3-218">아래는 Visual Studio 응용 프로그램 개체 트리의 스크린샷입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="03bf3-219">TestLineString 필드가 사용자 지정 필드로 추가된 TSTimesheetLine 테이블의 확장을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![라인 문자열](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="03bf3-221">TSTimesheetSettings 클래스의 buildCustomFieldList 메서드에서 명령 체인을 사용하여 작업 표 입력 섹션에 필드를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="03bf3-222">이 코드는 앱의 필드에 대한 표시 설정을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="03bf3-223">예를 들어, 필드 유형, 레이블, 필드가 필수인지 여부 및 필드가 표시되는 섹션을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="03bf3-224">다음 예제는 시간 항목에 대한 문자열 필드를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="03bf3-225">이 필드에는 옵션 단추(라디오 단추)를 통해 사용할 수 있는 **첫 번째 옵션** 및 **두 번째 옵션** 의 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="03bf3-226">앱의 필드는 TSTimesheetLine 테이블에 추가되는 **TestLineString** 필드와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="03bf3-227">**TSTimesheetCustomField::newFromMetatdata()** 메서드를 사용하여 사용자 지정 필드 속성 **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** 및 **numberOfDecimals** 의 초기화를 단순화합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="03bf3-228">원하는 대로 이러한 매개 변수를 수동으로 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="03bf3-229">TSTimesheetEntry 클래스의 buildCustomFieldListForEntry 메서드에서 명령 체인을 사용하여 작업 표 항목에 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="03bf3-230">**buildCustomFieldListForEntry** 메서드는 모바일 앱에서 저장된 작업 표 줄에 값을 입력하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="03bf3-231">TSTimesheetTrans 레코드를 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="03bf3-232">해당 레코드의 필드를 사용하여 앱에서 사용자 지정 필드 값을 채울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="03bf3-233">TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 다시 데이터베이스에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="03bf3-234">일반적인 사용에서 사용자 지정 필드를 데이터베이스에 다시 저장하려면 여러 메서드를 확장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="03bf3-235">**timesheetLineNeedsUpdating** 메서드는 앱에서 사용자가 라인 레코드를 변경했는지 여부를 확인하는 데 사용되며 데이터베이스에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="03bf3-236">성능이 중요하지 않은 경우 이 메서드를 단순화하여 항상 **true** 를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="03bf3-237">**populateTimesheetLineFromEntryDuringCreate** 및 **populateTimesheetLineFromEntryDuringUpdate** 메서드는 제공되는 TSTimesheetEntry 데이터 계약 레코드의 TSTimesheetLine 데이터베이스 레코드에 값을 입력하도록 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="03bf3-238">다음 예에서는 데이터베이스 필드와 입력 필드 간의 매핑이 X++ 코드를 통해 수동으로 수행되는 방식을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="03bf3-239">**populateTimesheetWeekFromEntry** 메서드는 **TSTimesheetEntry** 개체에 매핑된 사용자 지정 필드를 TSTimesheetLineweek 데이터베이스 테이블에 다시 써야하는 경우 확장될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="03bf3-240">다음 예제는 사용자가 데이터베이스에 대해 원시 문자열 값으로 선택하는 **firstOption** 또는 **secondOption** 값입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="03bf3-241">데이터베이스 필드가 **열거형** 유형의 필드인 경우 이러한 값을 수동으로 열거형 값에 매핑한 다음 데이터베이스 테이블의 열거 형 필드에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="03bf3-242">작업 표 헤더 섹션에 사용자 지정 필드 표시</span><span class="sxs-lookup"><span data-stu-id="03bf3-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="03bf3-243">아래는 작업 표를 보고 있는 사용자의 모바일 앱 스크린샷입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="03bf3-244">"추가 정보 보기" 옵션을 표시하기 위해 오른쪽 상단 모서리에서 "추가 정보" 단추가 선택되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![추가 정보 보기 명령](media/show-more.png)

<span data-ttu-id="03bf3-246">아래는 작업 표의 "자세히" 섹션을 보여주는 모바일 앱의 스크린샷입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="03bf3-247">"이 작업 표의 활용률(계산된 사용자 지정 필드)"이라는 사용자 지정 필드가 작업 표 헤더 섹션에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="03bf3-248">사용자 지정 필드에 "0.667"의 읽기 전용 값이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-248">A read-only value of "0.667" is set on the custom field.</span></span>

![자세히 섹션](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="03bf3-250">사용자 지정 필드를 갖도록 TSTimesheetTable 테이블 확장</span><span class="sxs-lookup"><span data-stu-id="03bf3-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="03bf3-251">일반적인 시나리오에서는 헤더 섹션의 사용자 지정 필드에 대한 데이터가 TSTimesheetHeader 테이블에 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="03bf3-252">그러나 제공된 TSTimesheetTable 레코드를 기반으로 데이터를 검색할 수 있거나 특정 레코드 컨텍스트가 없는 경우(예: 필드가 프로젝트 매개 변수에서 읽기 전용으로 설정된 경우) 다른 테이블을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="03bf3-253">사용자 지정 필드에는 백업 데이터베이스 레코드가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="03bf3-254">X++ 로직을 기반으로 동적으로 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="03bf3-255">다음 예제는 이 접근 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="03bf3-256">헤더 섹션의 필드는 앱에서 항상 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="03bf3-257">TSTimesheetSettings 클래스의 buildCustomFieldList 메서드에서 명령 체인을 사용하여 헤더 섹션에 필드를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="03bf3-258">이 코드는 앱의 필드에 대한 표시 설정을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="03bf3-259">예를 들어, 필드 유형, 레이블, 필드가 필수인지 여부 및 필드가 표시되는 섹션을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="03bf3-260">다음 예제는 앱의 헤더 섹션에 계산된 값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="03bf3-261">TSTimesheetDetails 클래스의 buildCustomFieldListForHeader 메서드에서 명령 체인을 사용하여 작업 표 세부 정보를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="03bf3-262">**buildCustomFieldListForHeader** 메서드는 모바일 앱에서 작업 표 세부 정보를 채우는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="03bf3-263">TSTimesheetTable 레코드를 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="03bf3-264">해당 레코드의 필드를 사용하여 앱에서 사용자 지정 필드 값을 채울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="03bf3-265">다음 예제는 데이터베이스에서 값을 읽지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="03bf3-266">대신 X++ 논리를 사용하여 앱에 표시되는 계산된 값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="03bf3-267">기타 구성 가능성/확장 가능성 기회</span><span class="sxs-lookup"><span data-stu-id="03bf3-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="03bf3-268">앱에 대한 추가 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="03bf3-268">Adding additional validation for the app</span></span>

<span data-ttu-id="03bf3-269">데이터베이스 수준의 작업 표 기능에 대한 기존 논리는 여전히 예상대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="03bf3-270">저장 또는 제출 작업 완료를 중단하고 특정 오류 메시지를 표시하려면 **throw 오류("사용자에 대한 메시지")** 를 일련의 명령 확장을 통해 코드에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="03bf3-271">다음은 유용한 확장 가능한 메서드의 세 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="03bf3-272">작업 표 라인에 대한 저장 작업 중에 TSTimesheetLine 테이블의 **validateWrite** 이 **false** 를 반환하는 경우 모바일 앱에 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="03bf3-273">앱에서 작업 표 제출 중에 TSTimesheetTable 테이블의 **validateSubmit** 이 **false** 를 반환하는 경우 사용자에게 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="03bf3-274">TSTimesheetLine 테이블에서 **삽입** 메서드 동안 필드를 채우는 논리(예: **라인 속성**)는 계속 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="03bf3-275">구성을 통해 기본 제공 필드 숨기기 및 읽기 전용으로 표시</span><span class="sxs-lookup"><span data-stu-id="03bf3-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="03bf3-276">프로젝트 매개 변수에서 기본 필드를 읽기 전용으로 만들거나 모바일 앱에서 숨길 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="03bf3-277">**프로젝트 관리 및 회계 매개 변수** 페이지의 **시간표** 탭의 **모바일 시간표** 섹션에서 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![프로젝트 매개 변수](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="03bf3-279">확장을 통해 선택할 수 있는 활동 변경</span><span class="sxs-lookup"><span data-stu-id="03bf3-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="03bf3-280">프로젝트에 대해 선택할 수 있는 활동은 **TsTimesheetProjectService** 클래스에서 **getActivitiesForProject()** 및 **getActivityQuery()** 메서드를 통해 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="03bf3-281">명령 체인을 사용하여 특정 프로젝트에 대해 선택할 수 있는 활동에 대한 비즈니스 시나리오와 일치하도록 이 동작을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="03bf3-282">작업 표 항목에 기본 프로젝트 범주 입력</span><span class="sxs-lookup"><span data-stu-id="03bf3-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="03bf3-283">작업 표 항목에 대한 기본 프로젝트 범주 항목은 세 가지 수준에서 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="03bf3-284">명령 체인을 사용하여 이러한 수준의 일부 또는 전체에서 동작을 확장하여 원하는 동작을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="03bf3-285">다음 계층 구조가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="03bf3-286">앱은 프로젝트 리소스에서 기본 범주를 넣으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="03bf3-287">이 기본 범주는 **TSTimesheetSettingsService** 클래스에서 **getCurrentUserResource** 및 **getDelegatedResourcesForCurrentUser** 메서드에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="03bf3-288">프로젝트 리소스 수준에서 기본 범주가 제공되지 않으면 앱은 프로젝트 활동에서 이를 가져오려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="03bf3-289">이 기본 범주는 **TSTimesheetProjectService** 클래스에서 **getActivitiesForProject** 메서드에 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="03bf3-290">프로젝트 활동 수준에서 기본 범주가 제공되지 않으면 기본 범주는 프로젝트 매개 변수에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="03bf3-291">이 기본 범주는 **TSTimesheetProjectService** 클래스에서 **getProjectDetailsbyRule** 메서드에 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03bf3-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]