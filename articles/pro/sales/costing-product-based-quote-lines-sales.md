---
title: 원가 계산 제품 기반 견적 라인
description: 이 항목에서는 제품 기반 견적 라인에 원가를 적용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273656"
---
# <a name="costing-product-based-quote-lines"></a>원가 계산 제품 기반 견적 라인

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


Dynamics 365 Project Operations의 제품 기반 견적 라인에는 **가격표** 필드도 있습니다. 이 필드는 견적 라인에서 제품의 원가를 추적하고 다운스트림 수익성 계산을 위해 사용됩니다.

카탈로그 제품에 대한 제품 기반 견적 라인이 생성되면 제품 기반 견적 라인의 비용은 기본적으로 제품 카탈로그의 **표준 비용** 필드에서 가져옵니다. 제품 카탈로그의 표준 비용 필드는 조직의 기본 통화로 설정됩니다. 제품 기반 견적 라인의 기본 단가는 견적의 판매 통화로 변환됩니다.

## <a name="unit-cost-on-a-product-based-quote-line"></a>제품 기반 견적 라인의 단가

제품 기반 견적 라인에 단가를 지정하는 목적은 각 판매를 위한 제품에 대해 서로 다른 비용을 허용하는 것입니다. 이것은 일반적인 시나리오는 아니지만 때때로 최종 판매 고객에 따라 공급자가 제품 비용을 할인할 수 있습니다.

예: 

Fabrikam Robotics는 A Datum Corporation의 조립 라인에 로봇 팔을 설치하고 있습니다. Fabrikam은 설치 서비스를 제공하지만 로봇 팔은 Trey 로봇에서 조달합니다. A Datum Corporation의 로봇 팔 설치로 Trey의 로봇 팔에 대한 새로운 산업 분야가 열리면 Trey는 Fabrikam에 이 거래에 대해 특별 할인을 제공할 수 있습니다.

이 경우 Fabrikam은 Robotic Arms에 대한 제품 기반 견적 라인을 만들고이 견적에 대한 특별 단가를 입력합니다. 이 비용은 Trey Robotic Arms의 표준 비용과 다릅니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]