---
title: 인력 비용 요금 설정 - 라이트
description: 이 항목은 Project Operations에서 인력 비용 요금을 설정하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c7b00d018f20dd79d5a6f8444a25ed4768cc6b220023fd08967eb917e2f4f2b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006119"
---
# <a name="set-up-labor-cost-rates---lite"></a>인력 비용 요금 설정 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

각 가격표에는 가격표의 내용 및 날짜 유효성과 일치하는 인건비 요율(역할 가격) 세트가 있습니다.

1. 가격표를 만들고 **역할 가격** 탭의 하위 표에서 **새 역할** 을 선택합니다.
2. **빨리 만들기** 페이지에서 역할 및 조직 단위를 선택합니다.
3. 기타 필수 필드 정보를 입력합니다.

다음 표에는 비용 가격표에서 인력 요금을 생성할 때 중요한 일부 필드가 포함되어 있습니다.

| 필드 | 위치 | 설명 | 다운스트림 영향 |
| --- | --- | --- | --- |
| 역할 | **일반** 탭 및 **빨리 만들기** 페이지 | 비용 요금을 할당할 역할을 선택합니다. | 들어오는 추정 또는 실제에 대한 역할은 역할 비용을 기본값으로 설정하기 위해 이 라인과 일치시킵니다. |
| 리소스 조달 단위 | **일반** 탭 및 **빨리 만들기** 페이지 | 이 역할이 사용될 회사의 조직 단위 또는 부문을 선택합니다. 예를 들어 Fabrikam India의 Robotics 부문의 개발자 또는 Fabrikam USA의 소프트웨어 부문의 개발자입니다. | 들어오는 추정 또는 실제에 대한 리소싱 단위는 역할 비용을 기본값으로 설정하기 위해 이 라인과 일치시킵니다. |
| 가격 | **일반** 탭 및 **빨리 만들기** 페이지 | 역할, 리소싱 회사 및 리소싱 단위 조합에 대한 비용 요금을 설정합니다. 예를 들어 Fabrikam India의 개발자 비용 1000 INR 또는 Fabrikam USA의 개발자 비용 150 USD입니다. | 가격은 **시간** 트랜잭션 클래스에 대한 들어오는 추정 또는 실제 라인의 단위 비용당 기본 요금입니다. |
| 통화 | **일반** 탭 및 **빨리 만들기** 페이지 | 기본적으로 통화 값은 비용 가격표 헤더의 통화에서 가져오지만 재정의할 수 있습니다. 예를 들어 Fabrikam India의 개발자 비용은 1000 INR입니다. Fabrikam USA의 개발자 비용은 150 USD입니다. | 이 통화의 기본값은 **시간** 트랜잭션 클래스에 대한 들어오는 실제 비용 라인의 단위당 비용입니다. 프로젝트 추정에서 통화 값은 프로젝트 통화로 변환되고 추정의 시간대별 보기에 표시됩니다. |
| 단위 일정 | **일반** 탭 및 **빨리 만들기** 페이지 | 단위 일정은 기본적으로 시간으로 설정되며 시간 단위로 표현 요금이 사용되므로 역할 가격 엔터티에서 변경할 수 없습니다. | 다운스트림에 영향을 주지 않습니다. |
| 단위 | **일반** 탭 및 **빨리 만들기** 페이지 | 기본적으로 값은 비용 가격표 헤더의 **시간 단위** 필드에서 가져옵니다. 값은 재정의할 수 있습니다. 예를 들어 Fabrikam India의 개발자 비용은 **인도 하루** 당 1000 INR입니다. Fabrikam USA의 개발자 비용은 **미국 하루** 당 150 USD입니다. | 시스템은 단위 시스템과 기준 단위 변환을 사용하여 단위당 비용을 계산하여 들어오는 추정 또는 실제 라인에서 단가를 계산합니다. 예를 들어, 인도 개발자의 경우 **인도 하루** 10일 분량의 작업을 추정하고 **인도 하루** 단위는 10시간으로 정의합니다. 해당 추정 라인의 비용을 계산할 때 애플리케이션은 추정에 대한 단위 비용을 다음과 같이 계산합니다. 1000 INR / 10시간 = 시간당 100 INR, 이는 USD로 변환되고 **프로젝트 견적** 페이지에서 단위 비용으로 표시됩니다. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>부문 또는 법인 외부의 리소스에 대한 이전 가격 책정 및 비용

프로젝트 기반 회사에서는 프로젝트에 다른 법인 또는 부문의 직원을 사용하는 것이 일반적입니다. 프로젝트는 하나의 법인에 의해 실행될 수 있지만, 프로젝트에 참여하는 직원 또는 컨설턴트는 동일한 법인 또는 다른 법인에서 올 수 있거나 둘 다의 조합이 있을 수 있습니다. Dynamics 365 Project Operations에서 프로젝트 배달을 담당하는 법인은 **담당 회사** 이고 배달을 담당하는 부서는 **계약 단위** 입니다. 리소스를 제공하는 다른 법인은 **리소싱 회사** 이고 리소스를 제공하는 부문은 **리소싱 단위** 입니다. 대부분의 국가에서 기업은 리소스를 조달하는 법인 또는 부문이 리소스 사용에 대해 담당 회사와 계약 단위에 비용을 청구하도록 해야 합니다.

예를 들어 Fabrikam 회사는 Fabrikam India-Robotics가 Fabrikam US-Robotics 또는 Fabrikam UK-Robotics와 비용 요금 카드를 협상했는지 확인해야 합니다.

Fabrikam India-Robotic의 개발자는 Fabrikam US-Robotics에 빌려줄 때 $100를 청구하고 Fabrikam U-Robotics에 빌려줄 때 $150를 청구합니다.

### <a name="set-up-costs-for-outside-resources"></a>외부 리소스에 대한 비용 설정

1. *Fabrikam US-Robotics 비용 요금* 이라는 비용 가격표를 만들고 날짜 유효 범위를 설정합니다.
2. 비용 가격표에서 다음 표의 정보를 사용하여 요금을 설정합니다. 

| 역할 | 리소싱 회사 | 리소스 조달 단위 | 비용 요금 |
| --- | --- | --- | --- |
| 디벨로퍼 | Fabrikam India | Fabrikam India-Robotics | $100 |
| 디벨로퍼 | Fabrikam Philippines | Fabrikam Philippines-Robotics | $90 |
| 디벨로퍼 | Fabrikam US | Fabrikam US-Robotics | $150 |

3. 이 비용 가격표를 Fabrikam US-Robotics 조직 단위에 연결합니다.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>적절한 통화로 리소스에 대한 이전 가격을 설정합니다. 

Project Operations에서 리소스 가격 책정은 모든 통화로 설정할 수 있습니다. 통화는 기본적으로 가격표 헤더에 있지만 변경할 수 있습니다.

이전 가격 설정 예제를 사용하면 정보를 다음과 같이 변경할 수 있습니다.

Fabrikam 회사는 Fabrikam India-Robotics가 Fabrikam US-Robotics 또는 Fabrikam UK-Robotics와 비용 요금을 협상했는지 확인해야 합니다.

Fabrikam India-Robotic의 개발자는 Fabrikam US-Robotics에 빌려줄 때 $100의 비용이 들고 Fabrikam U-Robotics에 빌려줄 때 $150의 비용이 듭니다.

Fabrikam US-Robotics의 비용 가격표에서 비용 요금은 다음과 같이 표현할 수 있습니다.

| 역할 | 리소싱 회사 | 비용 |
| --- | --- | --- |
| 디벨로퍼 | Fabrikam India | 5000 INR |
| 디벨로퍼 | Fabrikam US | 115 USD |

Fabrikam UK-Robotics의 비용 가격표에서 비용 요금은 다음과 같이 표현할 수 있습니다.

| 역할 | 리소싱 회사 | 비용 |
| --- | --- | --- |
| 디벨로퍼 | Fabrikam India | 5500 INR |
| 디벨로퍼 | Fabrikam UK | 115 GBP |

비용 가격표는 여러 통화로 인력 요금을 제공할 수 있습니다. 프로젝트에 대한 비용 견적을 생성할 때 Project Operations는 이러한 비용을 프로젝트 통화로 변환하여 사용자에게 표시합니다. 시간 항목이 승인되고 실제 비용이 생성되면 실제 비용은 비용 가격펴에서 해당 역할 가격 라인의 통화로 가격이 책정됩니다. 단일 프로젝트의 시간에 대한 실제 비용은 여러 통화로 기록될 수 있습니다. 그러나 프로젝트 수준에서 실제 인력 비용을 롤업하거나 요약할 때 Project Operations는 모든 인력 비용 금액을 사용자가 볼 수 있는 프로젝트 통화로 변환합니다.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]