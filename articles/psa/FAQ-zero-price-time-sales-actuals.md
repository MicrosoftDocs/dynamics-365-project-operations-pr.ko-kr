---
title: 시간 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?
description: 가격이 시간 판매 실제 값에서 기본값이 0인 이유 해결
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: cfb359b4ebd7c1a7a70ffdc2c47cf6291c797566
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285761"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>시간 판매 실제 값에 대한 가격이 기본적으로 0이 되는 이유는 무엇입니까?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

이 FAQ는 트랜잭션 클래스가 시간으로 설정되고 트랜잭션 유형이 미청구된 판매인 실제 값에 적용됩니다. 다음 세 가지 검사를 수행하면 시간 판매 실제 값에 대해 가격(대금 청구 요금)이 기본값 0이 되는 이유를 쉽게 해결할 수 있습니다.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>확인 1: 프로젝트에 대한 판매 가격표 식별

실제 값의 프로젝트 필드에서 프로젝트를 찾아 프로젝트로 페이지로 이동합니다. 그런 다음 영업 탭으로 이동하고 프로젝트 계약 내용 표에서 프로젝트 계약 필드의 링크를 클릭합니다. 프로젝트 계약 페이지가 열립니다. 프로젝트 계약 페이지에서 프로젝트 가격표 탭으로 이동합니다. 여기에 가격표가 하나 이상 첨부되어 있는지 확인합니다. 프로젝트 계약의 프로젝트 가격표 표에 첨부된 가격표가 없는 경우 문제가 해결된 것입니다. 가격표를 프로젝트 가격표 표에 첨부합니다. 여기에 첨부할 수 있는 가격표에는 컨텍스트 필드가 판매로 설정되어 있고 가격표의 통화 필드는 프로젝트 계약의 통화 필드와 일치해야 합니다. 필요한 수정 프로그램을 만든 후에는 시간 항목을 다시 만들고 승인하며 미청구 판매 실제 값이 유효한 가격을 표시하는지 확인합니다. 

프로젝트 계약의 프로젝트 가격표 표에 하나 이상의 가격표가 첨부되어 있는 경우 문서의 다음 확인으로 진행합니다.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>확인 2: 시간 판매 실제 값의 특정 날짜에 대해 위의서 식별된 가격표가 있습니까?

Project Service에서 기본 가격에 대한 가격표를 고려하려면 해당 가격표가 시간 판매 실제 값의 날짜에 적용되어야 합니다. 위에서 확인한 가격표가 적용 가능한 경우 다음을 확인하십시오.
- 첨부된 가격표에 대한 일반 탭에서 시작 날짜와 종료 날짜가 비어 있지 않은지 확인합니다. 위에서 확인한 가격표의 시작 날짜와 종료 날짜가 비어 있으면 문제가 해결된 것입니다. 
- 시간 판매 실제 값에 시작 날짜 필드를 기록해 두고 식별된 가격표가 해당 날짜에 적용되는지 확인합니다. 예를 들어 시간 판매 실제 값의 날짜는 가격표의 시작 날짜와 종료 날짜 내에 있어야 합니다. 
    - 시간 판매 실제 값에 해당 날짜를 포함하는 가격표가 없는 경우 문제가 해결된 것입니다. 가격표가 시간 판매 실제 값의 날짜를 포함하도록 하려면 가격표의 시작 및 종료 날짜를 수정합니다. 
    - 시간 판매 실제 값에 해당 날짜를 포함하는 가격표가 하나 이상 있는 경우 문제가 해결된 것입니다. 시간 판매 실제 값의 날짜를 포함하는 가격표가 하나만 있도록 가격표의 시작 및 종료 날짜를 편집하여 이 문제를 해결할 수 있습니다. 
    - 시간 판매 실제 값의 해당 날짜를 포함하는 가격표가 하나만 있는 경우 확인 3으로 이동합니다.
필요한 수정 프로그램을 만든 후에는 시간 항목을 다시 만들고 승인하며 시간 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>확인 3: 시간 판매 실제 값에 대한 가격 산정 차원에 대한 가격표에 가격이 있습니까?

확인 1 및 확인 2를 성공적으로 완료한 경우 이제 시간 판매 실제 값의 날짜에 적용할 수 있는 가격표가 하나만 있어야 합니다. 이 가격표를 열고 역할 가격 탭으로 이동합니다. 시간 판매 실제 값의 가격 산정 차원에 대한 표에 행이 있는지 확인합니다.

시간 판매 실제 값의 가격 산정 차원에 대한 역할 가격표에 행이 없으면 문제가 해결된 것입니다. 시간 판매 실제 값의 가격 산정 차원에 대한 역할 가격 표에 행을 만듭니다. 작업이 완료되면 시간 항목을 다시 만들고 승인하며 시간 판매 실제 값이 유효한 가격을 표시하는지 확인합니다.

위의 세 가지 확인을 수행한 후에도 시간 판매 실제 값에 유효한 가격이 표시되지 않으면 지원 티켓을 기록해 주십시오. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]