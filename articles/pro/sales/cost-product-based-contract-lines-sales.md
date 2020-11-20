---
title: 원가 계산 제품 기반 계약 내용 - 라이트
description: 이 항목은 만들기에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177249"
---
# <a name="cost-product-based-contract-lines---lite"></a>원가 계산 제품 기반 계약 내용 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_


Dynamics 365 Project Operations의 제품 기반 계약 내용에는 다운스트림 수익성 계산을 위해 제품의 원가를 저장하는 **원가** 필드가 포함됩니다.

카탈로그 제품에 대한 제품 기반 계약 내용이 생성되면 제품 기반 계약 내용의 비용은 기본적으로 제품 카탈로그의 **표준 비용** 필드에서 가져옵니다. 제품 카탈로그의 **표준 비용** 필드는 조직의 기본 통화로 설정됩니다. 단가가 계약 내용에서 기본값으로 설정되면 계약의 판매 통화로 변환됩니다.

## <a name="unit-cost-on-a-product-based-contract-line"></a>제품 기반 계약 내용의 단가

제품 기반 계약 내용에 단가가 있으면 단가 판매마다 다른 제품 비용이 허용됩니다. 항상 필요한 것은 아니지만 공급자가 고객을 위해 제품 비용을 할인할 수 있는 특정 시나리오가 있습니다. 다음 시나리오를 살펴 보십시오.

Fabrikam Robotics는 Adatum Corporation의 조립 라인에 로봇 팔을 설치하고 있습니다. Fabrikam은 설치 서비스를 제공하지만 로봇 팔은 Trey Research에서 조달합니다. Adatum Corporation의 로봇 팔 설치로 Trey Research를 위한 새로운 산업 분야가 열리면 Trey는 Fabrikam에 이 거래에 대해 특별 할인을 제공할 수 있습니다. 이 경우 Fabrikam은 Robotic Arms에 대한 제품 기반 계약 내용을 만들고 Trey Research의 로봇 팔 표준 비용과 다른 이 계약의 단위당 비용을 입력합니다.
