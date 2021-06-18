---
title: 시간 항목 만들기
description: 이 주제는 시간 항목을 만드는 방법에 대한 정보를 제공합니다.
author: rumant
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
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999274"
---
# <a name="create-time-entries"></a>시간 항목 만들기

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

이전 버전의 Dynamics 365 Project Service Automation에서는 시간 항목이 주별로 입력되었습니다. Project Service Automation의 버전 3에서는 시간 항목이 일별로 입력됩니다. 그러나 소수의 시간 항목을 만든 후 대량으로 만들거나 복사할 수 있습니다.

## <a name="create-a-time-entry"></a>시간 항목 만들기

다음 단계에 따라 시간 항목을 만드십시오.

1. **시간 항목** 페이지에서 **신규** 를 선택합니다.
2. **빠른 만들기: 시간 항목** 대화 상자에서 시간 입력 기간을 분, 시간 또는 일로 입력합니다. 기간은 *x* 분, *x* 시간 또는 *x* 일 형식으로 입력해야 합니다. 시간과 일은 *x.x* 시간 또는 *x.x* 일 같이 소수 자릿수를 사용하여 입력할 수도 있습니다.
3. 시간 항목 타입과 시간 항목을 입력하는 프로젝트를 선택합니다.
4. **프로젝트 과업** 필드에서 이 시간 항목에 대한 과업을 찾습니다.

    > [!NOTE]
    > 사용자에게 할당되지 않은 과업에 대한 시간 항목을 만드는 경우, **프로젝트 과업** 필드에서 **검색** 버튼을 선택하고 **보기 변경** 을 선택한 다음, **모든 활성 프로젝트 과업** 을 선택하면 모든 과업이 열거됩니다.

5. 설명이 요구되는 경우 설명을 입력한 다음 **저장 및 닫기** 를 선택합니다.

시간 항목을 만들고 저장한 후 시간 항목 그리드에서 편집할 수 있습니다. 시간 항목 그리드는 다음 두 형식을 지원합니다:

- 시간 항목을 **hh:mm** 형식으로 입력할 수 있습니다. 그런 다음 이 형식은 시간 및 분수로 변환됩니다.
- 시간과 분수를 직접 입력할 수 있습니다.

한 시간의 분수가 분이 아닙니다. 따라서 1.5시간은 1시간 30분을 나타냅니다. 동일한 규칙이 날의 분수에 적용됩니다. 1일은 24시간, 0.5일은 12시간을 나타냅니다.

## <a name="bulk-create-time-entries"></a>시간 항목 대량 만들기

소수의 시간 항목을 만든 후 대량으로 복사하여 추가 시간 항목을 대량으로 만들 수 있습니다.

1. **시간 항목** 페이지에서 **주 복사** 를 선택합니다.
2. **시작 기간** 필드 그룹의 **시작일** 및 **종료일** 필드에서 시간 항목을 복사할 날짜 범위를 정의합니다.
3. **끝 기간** 필드 그룹의 **시작일** 필드에서 시간 항목을 만들 날짜를 지정합니다.
4. **복사** 를 선택하여 **끝 기간** 필드 그룹에 지정된 요일에 해당하는 시간 항목의 복사본을 만듭니다. 예컨대, 지난 주 월요일의 시간 항목은 **끝 기간** 필드 그룹에 지정된 주의 월요일로 복사됩니다.

## <a name="import-data-for-time-entries"></a>시간 항목에 대한 데이터 가져오기

프로젝트 예약 및 할당에서 데이터를 가져올 수 있습니다. 데이터를 가져올 때 가져올 예약의 날짜 범위를 지정한 다음 **초안** 시간 항목으로 만들어야 하는 예약을 명시적으로 선택할 수 있습니다.

## <a name="group-by-sort-search-and-filter-capabilities"></a>그룹화, 정렬, 검색 및 필터 기능

열에 지정된 차원별로 시간 항목을 그룹화하고 필터링할 수 있습니다. **그룹화** 필드에서 시간 항목을 필터링하는 데 사용할 차원을 선택합니다. 열 표제의 정렬 화살표를 사용하여 오름차순 또는 내림차순으로 시간 항목 레코드를 정렬할 수도 있습니다. 또한 열 표제의 **필터** 버튼을 선택한 다음, **검색** 상자에서 프로젝트 명칭, 프로젝트 과업, 시간 항목 또는 리소스별로 시간 항목을 검색하는 데 사용해야 하는 텍스트를 입력하여 항목을 표시하거나 숨길 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]