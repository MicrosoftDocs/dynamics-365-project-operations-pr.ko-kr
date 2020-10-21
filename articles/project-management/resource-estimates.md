---
title: 리소스 추정
description: 이 항목에서는 Project Operations에서 리소스 추정을 계산하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928584"
---
# <a name="resource-estimates"></a>리소스 추정

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

리소스 추정은 적용 가능한 가격 책정 차원과 함께 작업 분할 구조에 정의된 시간별 작업량에서 비롯됩니다. 일반적으로 계산은 **역할 x 시간에 대한 속도/시간**입니다. 각 리소스에 대한 시간대별 작업량은 리소스 할당 레코드에 저장됩니다. 가격은 미리 정의된 가격표에 저장됩니다. 적용 가능한 가격표를 기준으로 단위 변환이 적용됩니다.

![리소스 추정](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>기본 원가 및 비용 통화

원가는 조직 구성 단위에서 기본값으로 설정됩니다.

## <a name="default-bill-rate-and-sales-currency"></a>기본 청구 요금 및 판매 통화

판매 가격은 거래당 한 번 적용됩니다. 판매 가격표 기본값을 위한 계층 구조는 다음과 같습니다.

1. 조직
2. 고객
3. 견적/계약
