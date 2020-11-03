---
title: 프로젝트 견적 분석
description: 이 항목은 프로젝트 견적 분석에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080168"
---
# <a name="analysis-of-project-quotes"></a>프로젝트 견적 분석

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation은 프로젝트 견적을 분석하여 수익성을 추산합니다. 또한 견적이 인도일 또는 완료일에 대한 고객의 기대와 예산에 얼마나 잘 부합하는지를 분석합니다.

## <a name="profitability-analysis"></a>수익성 분석

Project Service Automation은 총 마진과 조정된 총 마진을 사용하여 수익성을 분석합니다.

- 총 마진은 다음 공식을 사용하여 계산됩니다:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- 조정된 총 마진은 다음 공식을 사용하여 계산됩니다:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

총 마진과 조정된 총 마진의 값들이 큰 폭으로 다른 경우, 견적에서 작업의 대부분은 청구 불가능으로 분류됩니다.

## <a name="analysis-of-customer-expectations"></a>고객 기대 분석

다음 필드에 값을 입력하면 견적을 분석하고 스케줄 및 예산에 대한 고객 기대에 대한 차트를 생성할 수 있습니다:

- 견적 표제의 **요청된 인도일** 필드.
- 각 견적 행에 대한 **고객 예산** 필드(프로젝트 기반 행 및 제품 기반 행의 경우).

스케줄에 대한 고객 기대 분석은 견적 행 내역의 가장 늦은 종료 날짜와 요청된 인도일을 비교하여 수행됩니다.

예산에 대한 고객 기대 분석은 총 고객 예산의 합과 모든 견적 행의 견적 금액을 비교하여 수행됩니다.
