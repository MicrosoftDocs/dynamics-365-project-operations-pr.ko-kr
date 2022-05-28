---
title: iOS 및 Android의 Microsoft Dynamics 365 Project Timesheet 모바일 앱에 대한 사용자 지정 필드 구현
description: 이 항목은 확장을 사용하여 사용자 지정 필드를 구현하기 위한 공통 패턴을 제공합니다.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 79ef62d6911b393248536e4cc73475f6c35a22e2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682764"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>iOS 및 Android의 Microsoft Dynamics 365 Project Timesheet 모바일 앱에 대한 사용자 지정 필드 구현

[!include [banner](../includes/banner.md)]

이 항목은 확장을 사용하여 사용자 지정 필드를 구현하기 위한 공통 패턴을 제공합니다. 다음 주제를 다룹니다.

- 사용자 지정 필드 프레임워크가 지원하는 다양한 데이터 유형
- 작업 표 항목에 읽기 전용 또는 편집 가능한 필드를 표시하고 사용자가 제공한 값을 다시 데이터베이스에 저장하는 방법
- 작업 표 머리글에 읽기 전용 필드를 표시하는 방법
- 다른 사용자 지정 비즈니스 논리를 통합하여 필드에 기본값을 입력하고 추가 유효성 검사를 수행하는 방법

## <a name="audience"></a>대상

이 항목은 사용자 지정 필드를 Apple iOS 및 Google Android에서 사용할 수 있는 Microsoft Dynamics 365 Project Timesheet 모바일 애플리케이션에 통합하는 개발자를 위한 것입니다. 독자가 X++ 개발 및 프로젝트 타임시트 기능에 익숙하다고 가정합니다.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>데이터 계약 – TSTimesheetCustomField X++ 클래스

**TSTimesheetCustomField** 클래스는 작업 표 기능에 대한 사용자 지정 필드에 대한 정보를 나타내는 X++ 데이터 계약 클래스입니다. 사용자 지정 필드 개체 목록은 TSTimesheetDetails 데이터 계약 및 TSTimesheetEntry 데이터 계약 모두에 전달되어 모바일 앱에 사용자 지정 필드를 표시합니다.

- **TSTimesheetDetails** - 작업 표 헤더 계약입니다.
- **TSTimesheetEntry** - 작업 표 트랜잭션 계약입니다. 동일한 프로젝트 정보 및 **timesheetLineRecId** 값을 가진 이러한 개체 그룹이 선을 구성합니다.

### <a name="fieldbasetype-types"></a>fieldBaseType(유형)

**TsTimesheetCustom** 개체의 **FieldBaseType** 속성은 앱에 표시되는 필드의 유형을 결정합니다. 다음과 같은 **유형** 값이 지원됩니다.

| 유형 값 | 형식              | 메모  |
|-------------|-------------------|-------|
| 0           | 문자열 (및 열거형) | 필드는 텍스트 필드로 나타납니다. |
| 1           | Integer           | 값은 소수점이 없는 숫자로 표시됩니다. |
| 2           | 실수              | 값은 소수점이 있는 숫자로 표시됩니다.<p>앱에서 실제 가치를 통화로 표시하려면 **fieldExtenededType** 속성을 사용합니다. **numberOfDecimals** 속성을 사용하여 표시되는 소수 자릿수를 설정할 수 있습니다.</p> |
| 3           | Date              | 날짜 형식은 **사용자 옵션** 의 **언어 및 국가/지역 기본 설정** 아래에 지정된 사용자의 **날짜, 시간 및 숫자 형식** 설정에 따라 결정됩니다. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- **TSTimesheetCustomField** 개체에서 **stringOptions** 속성이 제공되지 않는 경우 자유 텍스트 필드가 사용자에게 제공됩니다.

    **stringLength** 속성을 사용하여 사용자가 입력할 수 있는 최대 문자열 길이를 설정할 수 있습니다.

- **TSTimesheetCustomField** 개체에 **stringOptions** 속성이 제공되는 경우 이러한 목록 요소는 사용자가 옵션 단추(라디오 단추)를 사용하여 선택할 수 있는 유일한 값입니다.

    이 경우 문자열 필드는 사용자 입력을 위한 열거형 값 역할을 할 수 있습니다. 값을 열거형으로 데이터베이스에 저장하려면 명령 체인을 사용하여 데이터베이스에 저장하기 전에 문자열 값을 다시 열거형 값에 수동으로 매핑합니다(예를 보려면 이 항목 뒷부분의 "TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 다시 데이터베이스에 저장" 섹션 참조).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

이 속성을 사용하여 실제 값을 통화로 형식화할 수 있습니다. 이 접근 방식은 **fieldBaseType** 값이 **실수** 일 때만 적용됩니다.

- **TSCustomFieldExtendedType:None** – 서식이 적용되지 않습니다.
- **TSCustomFieldExtendedType::Currency** – 값을 통화로 형식화합니다.

    통화 형식이 활성화되면 **stringValue** 필드는 앱에 표시되어야 하는 통화 코드를 전달하는 데 사용할 수 있습니다. 값은 읽기 전용 값입니다.

    **realValue** 필드에는 데이터베이스에 저장해야 하는 금액이 포함됩니다.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

이 속성을 사용하여 앱에서 사용자 지정 필드가 표시되어야 하는 위치를 지정할 수 있습니다.

- **TSCustomFieldSection::Header** – 필드가 앱의 **자세히 보기** 섹션에 나타납니다. 이러한 필드는 항상 읽기 전용입니다.
- **TSCustomFieldSection::Line** – 이 필드는 작업 표 항목의 모든 기본 제공 라인 필드 뒤에 나타납니다. 이러한 필드는 편집 가능하거나 읽기 전용일 수 있습니다.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

이 속성은 앱이 제공하는 값이 데이터베이스에 다시 저장될 때 필드를 식별합니다.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

이 속성은 앱이 제공하는 값이 데이터베이스에 다시 저장될 때 필드를 식별합니다.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

이 속성을 **예** 로 설정하여 작업 표 입력 섹션의 필드를 사용자가 편집할 수 있도록 지정합니다. 필드를 읽기 전용으로 만들려면 속성을  **No** 로 설정합니다.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

이 속성을 **예** 로 설정하여 작업 표 입력 섹션의 필드를 필수로 지정합니다.

### <a name="label-str"></a>label (str)

이 속성은 앱의 필드 옆에 표시되는 레이블을 지정합니다.

### <a name="stringoptions-list-of-strings"></a>stringOptions (문자열 목록)

이 속성은 **fieldBaseType** 이 **String** 으로 설정된 경우에만 적용됩니다. **stringOptions** 이 설정된 경우 옵션 단추(라디오 단추)를 통해 선택할 수 있는 문자열 값은 목록의 문자열로 지정됩니다. 문자열이 제공되지 않으면 문자열 필드에 자유 텍스트 항목이 허용됩니다(예를 보려면 이 항목 뒷부분의 "TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 데이터베이스에 다시 저장" 섹션 참조).

### <a name="stringlength-int"></a>stringLength (int)

이 속성은 문자열 필드의 최대 길이를 지정합니다. **fieldBaseType** 이 **String** 으로 설정된 경우에만 적용됩니다. 

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

이 속성은 실수 필드에 대해 표시되는 소수 자릿수를 지정합니다. **fieldBaseType** 이 **Real** 로 설정된 경우에만 적용됩니다. 

### <a name="ordersequence-int"></a>orderSequence (int)

이 속성은 둘 이상의 사용자 지정 필드가 지정된 경우 사용자 지정 필드가 앱에 표시되는 순서를 제어합니다. 숫자가 더 낮은 필드가 먼저 표시됩니다.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 부울 값을 전달합니다.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 GUID(Globally Unique Identifier) 값을 전달합니다.

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 Int64 값을 전달합니다.

### <a name="intvalue-int"></a>intValue (int)

**Int** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 정수 값을 전달합니다.

### <a name="realvalue-real"></a>realValue (real)

**Real** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 실수 값을 전달합니다.

### <a name="stringvalue-str"></a>stringValue (str)

**String** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 문자열 값을 전달합니다. 통화로 형식이 지정된 **Real** 유형의 필드에도 사용됩니다. 이러한 필드의 경우 속성은 통화 코드를 앱에 전달하는 데 사용됩니다.

### <a name="datevalue-date"></a>dateValue (date)

**Date** 유형 필드의 경우 이 속성은 서버와 앱간에 필드의 날짜 값을 전달합니다.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>작업 표 입력 섹션에 사용자 지정 필드 표시 및 저장

아래는 작업 표 항목 생성의 모바일 앱 스크린샷입니다. "두 번째 옵션" 열거형 값이 이미 설정된 "테스트 문자열"이라는 "시간 항목" 섹션의 기본 필드와 사용자 지정 필드가 표시됩니다.

![앱의 테스트 문자열 사용자 지정 필드.](media/timesheet-entry.jpg)



아래는 "테스트 문자열" 사용자 지정 필드에 사용할 수 있는 열거형 옵션 중 하나를 선택하는 사용자의 모바일 앱 스크린샷입니다.  두 가지 옵션은 라디오 단추로 표시된 "첫 번째 옵션"과 "두 번째 옵션"입니다. 두 번째 옵션이 현재 선택되어 있습니다.

![테스트 문자열 사용자 지정 필드에 대한 옵션 단추(라디오 단추).](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>사용자 지정 필드를 갖도록 TSTimesheetLine 테이블 확장

일반적인 시나리오에서는 작업 표 입력 섹션의 사용자 지정 필드에 대한 데이터가 TSTimesheetLine 테이블에 저장될 수 있습니다. 그러나 제공된 TSTimesheetTrans 레코드를 기반으로 데이터를 검색할 수 있거나 특정 레코드 컨텍스트가 없는 경우(예: 필드가 프로젝트 매개 변수에서 읽기 전용으로 설정된 경우) 다른 테이블을 사용할 수 있습니다.

사용자 지정 필드에는 백업 데이터베이스 레코드가 필요하지 않습니다. X++ 로직을 기반으로 동적으로 생성될 수 있습니다. 이 접근 방식은 읽기 전용 시나리오에서 유용할 수 있습니다(동적으로 생성된 사용자 지정 필드 값의 예는 "TSTimesheetDetails 클래스의 명령 체인, buildCustomFieldListForHeader 메서드를 사용하여 작업 표 세부 정보 채우기"섹션 참조).

아래는 Visual Studio 응용 프로그램 개체 트리의 스크린샷입니다. TestLineString 필드가 사용자 지정 필드로 추가된 TSTimesheetLine 테이블의 확장을 보여줍니다.

![라인 문자열.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>TSTimesheetSettings 클래스의 buildCustomFieldList 메서드에서 명령 체인을 사용하여 작업 표 입력 섹션에 필드를 표시합니다.

이 코드는 앱의 필드에 대한 표시 설정을 제어합니다. 예를 들어, 필드 유형, 레이블, 필드가 필수인지 여부 및 필드가 표시되는 섹션을 제어합니다.

다음 예제는 시간 항목에 대한 문자열 필드를 보여줍니다. 이 필드에는 옵션 단추(라디오 단추)를 통해 사용할 수 있는 **첫 번째 옵션** 및 **두 번째 옵션** 의 두 가지 옵션이 있습니다. 앱의 필드는 TSTimesheetLine 테이블에 추가되는 **TestLineString** 필드와 연결됩니다.

**TSTimesheetCustomField::newFromMetatdata()** 메서드를 사용하여 사용자 지정 필드 속성 **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** 및 **numberOfDecimals** 의 초기화를 단순화합니다. 원하는 대로 이러한 매개 변수를 수동으로 설정할 수도 있습니다.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>TSTimesheetEntry 클래스의 buildCustomFieldListForEntry 메서드에서 명령 체인을 사용하여 작업 표 항목에 값을 입력합니다.

**buildCustomFieldListForEntry** 메서드는 모바일 앱에서 저장된 작업 표 줄에 값을 입력하는 데 사용됩니다. TSTimesheetTrans 레코드를 매개 변수로 사용합니다. 해당 레코드의 필드를 사용하여 앱에서 사용자 지정 필드 값을 채울 수 있습니다.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>TSTimesheetEntryService 클래스에서 명령 체인을 사용하여 앱의 작업 표 항목을 다시 데이터베이스에 저장합니다.

일반적인 사용에서 사용자 지정 필드를 데이터베이스에 다시 저장하려면 여러 메서드를 확장해야 합니다.

- **timesheetLineNeedsUpdating** 메서드는 앱에서 사용자가 라인 레코드를 변경했는지 여부를 확인하는 데 사용되며 데이터베이스에 저장해야 합니다. 성능이 중요하지 않은 경우 이 메서드를 단순화하여 항상 **true** 를 반환합니다.
- **populateTimesheetLineFromEntryDuringCreate** 및 **populateTimesheetLineFromEntryDuringUpdate** 메서드는 제공되는 TSTimesheetEntry 데이터 계약 레코드의 TSTimesheetLine 데이터베이스 레코드에 값을 입력하도록 확장할 수 있습니다. 다음 예에서는 데이터베이스 필드와 입력 필드 간의 매핑이 X++ 코드를 통해 수동으로 수행되는 방식을 확인합니다.
- **populateTimesheetWeekFromEntry** 메서드는 **TSTimesheetEntry** 개체에 매핑된 사용자 지정 필드를 TSTimesheetLineweek 데이터베이스 테이블에 다시 써야하는 경우 확장될 수도 있습니다.

> [!NOTE]
> 다음 예제는 사용자가 데이터베이스에 대해 원시 문자열 값으로 선택하는 **firstOption** 또는 **secondOption** 값입니다. 데이터베이스 필드가 **열거형** 유형의 필드인 경우 이러한 값을 수동으로 열거형 값에 매핑한 다음 데이터베이스 테이블의 열거 형 필드에 저장할 수 있습니다.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>작업 표 헤더 섹션에 사용자 지정 필드 표시

아래는 작업 표를 보고 있는 사용자의 모바일 앱 스크린샷입니다. "추가 정보 보기" 옵션을 표시하기 위해 오른쪽 상단 모서리에서 "추가 정보" 단추가 선택되었습니다.  

![추가 정보 보기 명령.](media/show-more.png)

아래는 작업 표의 "자세히" 섹션을 보여주는 모바일 앱의 스크린샷입니다. "이 작업 표의 활용률(계산된 사용자 지정 필드)"이라는 사용자 지정 필드가 작업 표 헤더 섹션에 추가되었습니다. 사용자 지정 필드에 "0.667"의 읽기 전용 값이 설정됩니다.

![자세히 섹션.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>사용자 지정 필드를 갖도록 TSTimesheetTable 테이블 확장

일반적인 시나리오에서는 헤더 섹션의 사용자 지정 필드에 대한 데이터가 TSTimesheetHeader 테이블에 가져올 수 있습니다. 그러나 제공된 TSTimesheetTable 레코드를 기반으로 데이터를 검색할 수 있거나 특정 레코드 컨텍스트가 없는 경우(예: 필드가 프로젝트 매개 변수에서 읽기 전용으로 설정된 경우) 다른 테이블을 사용할 수 있습니다.

사용자 지정 필드에는 백업 데이터베이스 레코드가 필요하지 않습니다. X++ 로직을 기반으로 동적으로 생성될 수 있습니다. 다음 예제는 이 접근 방식을 보여줍니다.

헤더 섹션의 필드는 앱에서 항상 읽기 전용입니다.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>TSTimesheetSettings 클래스의 buildCustomFieldList 메서드에서 명령 체인을 사용하여 헤더 섹션에 필드를 표시합니다.

이 코드는 앱의 필드에 대한 표시 설정을 제어합니다. 예를 들어, 필드 유형, 레이블, 필드가 필수인지 여부 및 필드가 표시되는 섹션을 제어합니다.

다음 예제는 앱의 헤더 섹션에 계산된 값을 보여줍니다.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>TSTimesheetDetails 클래스의 buildCustomFieldListForHeader 메서드에서 명령 체인을 사용하여 작업 표 세부 정보를 채웁니다.

**buildCustomFieldListForHeader** 메서드는 모바일 앱에서 작업 표 세부 정보를 채우는 데 사용됩니다. TSTimesheetTable 레코드를 매개 변수로 사용합니다. 해당 레코드의 필드를 사용하여 앱에서 사용자 지정 필드 값을 채울 수 있습니다. 다음 예제는 데이터베이스에서 값을 읽지 않습니다. 대신 X++ 논리를 사용하여 앱에 표시되는 계산된 값을 생성합니다.


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

## <a name="other-configurabilityextensibility-opportunities"></a>기타 구성 가능성/확장 가능성 기회

### <a name="adding-additional-validation-for-the-app"></a>앱에 대한 추가 유효성 검사 추가

데이터베이스 수준의 작업 표 기능에 대한 기존 논리는 여전히 예상대로 작동합니다. 저장 또는 제출 작업 완료를 중단하고 특정 오류 메시지를 표시하려면 **throw 오류("사용자에 대한 메시지")** 를 일련의 명령 확장을 통해 코드에 추가할 수 있습니다. 다음은 유용한 확장 가능한 메서드의 세 가지 예입니다.

- 작업 표 라인에 대한 저장 작업 중에 TSTimesheetLine 테이블의 **validateWrite** 이 **false** 를 반환하는 경우 모바일 앱에 오류 메시지가 표시됩니다.
- 앱에서 작업 표 제출 중에 TSTimesheetTable 테이블의 **validateSubmit** 이 **false** 를 반환하는 경우 사용자에게 오류 메시지가 표시됩니다.
- TSTimesheetLine 테이블에서 **삽입** 메서드 동안 필드를 채우는 논리(예: **라인 속성**)는 계속 실행됩니다.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>구성을 통해 기본 제공 필드 숨기기 및 읽기 전용으로 표시

프로젝트 매개 변수에서 기본 필드를 읽기 전용으로 만들거나 모바일 앱에서 숨길 수 있습니다. **프로젝트 관리 및 회계 매개 변수** 페이지의 **시간표** 탭의 **모바일 시간표** 섹션에서 옵션을 설정합니다.

![프로젝트 매개 변수.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>확장을 통해 선택할 수 있는 활동 변경

프로젝트에 대해 선택할 수 있는 활동은 **TsTimesheetProjectService** 클래스에서 **getActivitiesForProject()** 및 **getActivityQuery()** 메서드를 통해 채워집니다. 명령 체인을 사용하여 특정 프로젝트에 대해 선택할 수 있는 활동에 대한 비즈니스 시나리오와 일치하도록 이 동작을 변경할 수 있습니다.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>작업 표 항목에 기본 프로젝트 범주 입력

작업 표 항목에 대한 기본 프로젝트 범주 항목은 세 가지 수준에서 발생합니다. 명령 체인을 사용하여 이러한 수준의 일부 또는 전체에서 동작을 확장하여 원하는 동작을 얻을 수 있습니다. 다음 계층 구조가 사용됩니다.

1. 앱은 프로젝트 리소스에서 기본 범주를 넣으려고 합니다. 이 기본 범주는 **TSTimesheetSettingsService** 클래스에서 **getCurrentUserResource** 및 **getDelegatedResourcesForCurrentUser** 메서드에서 설정됩니다.
2. 프로젝트 리소스 수준에서 기본 범주가 제공되지 않으면 앱은 프로젝트 활동에서 이를 가져오려고 합니다. 이 기본 범주는 **TSTimesheetProjectService** 클래스에서 **getActivitiesForProject** 메서드에 설정됩니다.
3. 프로젝트 활동 수준에서 기본 범주가 제공되지 않으면 기본 범주는 프로젝트 매개 변수에서 가져옵니다. 이 기본 범주는 **TSTimesheetProjectService** 클래스에서 **getProjectDetailsbyRule** 메서드에 설정됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]