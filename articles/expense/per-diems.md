---
title: 일비
description: 이 항목은 경비 관리에 사용되는 일비 규칙에 대한 정보를 제공합니다.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276311"
---
# <a name="per-diems"></a>일비

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_


일비는 업무를 위해 여행하는 근로자에게 지급되는 수당입니다. 경비 관리에서는 다양한 여행 상황에 대한 일당 규칙을 만들 수 있습니다. 일비 요율은 연중 시간, 여행 위치 또는 둘 다를 기반으로 할 수 있습니다. 일비 규칙을 만들 때 근로자가 무료 급식 또는 서비스를 받는 경우 일비 비율의 일정 비율이 보류되도록 지정할 수 있습니다. 일비 요율이 근로자의 출장에 적용될 수 있는 최소 및 최대 시간을 설정할 수도 있습니다.

## <a name="configuration"></a>구성 

1. 일비 위치를 추가하려면 **설정** > **계산 및 코드** > **일비 위치** 으로 이동합니다.
2. 위에 추가된 각 위치에 대해 호텔, 식사 및 기타 비용에 대해 특정 시작 날짜와 종료 날짜 사이에 유효한 일비 요율 및 통화를 선택합니다. 일비 요율 및 통화는 **설정** > **계산 및 코드** > **일비** 아래 구성됩니다.
3. **일비 위치** 페이지에서 일비 요율 계층을 구성합니다. 일비 요율 계층을 사용하면 호텔, 식사 및 기타 비용에 대한 일비 수당의 비율 분할을 정의할 수 있습니다. 
4. 아침, 점심 또는 저녁 식사에 대한 식사 비율 감소를 지정하려면 **일비** 탭의 **경비 관리 매개 변수** 페이지에서 필드를 업데이트합니다. 
    
## <a name="submit-expenses-using-per-diem"></a>일비를 사용하여 경비 제출
일비를 활용한 경비를 제출하려면 **일비** 경비 보고서를 생성할 때 경비 범주를 사용합니다. **일비 시작 날짜**,**일비 종료 날짜** 및 **일비 위치** 를 입력합니다. 금액은 선택한 위치의 일비 요율을 기준으로 계산되며, 식비 감소는 일비 요율 등급에 따라 계산됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]