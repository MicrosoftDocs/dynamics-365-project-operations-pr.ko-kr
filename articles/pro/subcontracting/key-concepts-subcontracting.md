---
title: 하도급의 핵심 개념
description: 이 항목에서는 Microsoft Dynamics 365 Project Operations의 하도급 계약에 적용되는 몇 가지 주요 개념을 설명합니다.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578119"
---
# <a name="key-concepts-in-subcontracting"></a>하도급의 핵심 개념

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

이 항목에서는 Microsoft Dynamics 365 Project Operations에서 하도급 계약 기능을 사용하기 전에 알아야 할 몇 가지 주요 개념을 설명합니다.

## <a name="contracting-unit-on-the-subcontract"></a>하도급 계약 단위

계약 단위는 최종 프로젝트의 납품을 담당하는 부서 또는 관행을 나타냅니다. 계약 단위는 공급업체와 계약 관계를 맺는 부서이기도 합니다.

## <a name="purchase-currency"></a>구매 통화

Project Operations에서 구매 통화는 하도급 계약이 생성되는 통화입니다. 프로젝트의 하청업체 비용이 기록되는 통화이기도 합니다. 구매 통화는 프로젝트 통화와 다를 수 있으며 프로젝트 통화는 판매 통화와 다를 수 있습니다.

## <a name="billing-methods-on-subcontract-lines"></a>하도급 계약 라인의 청구 방법

프로젝트의 경우 일반적으로 고정 요금 및 소비 기반 계약 모델이 있습니다. Project Operations는 판매 및 구매 컨텍스트에서 이러한 청구 방법을 지원합니다. 구매의 경우 청구 방법은 다음과 같은 방식으로 작동합니다.

- **시간과 재료** – 하도급 계약 라인이 **시간과 재료** 청구 방법을 사용하는 경우, 시간 비용은 하청업체가 해당 프로젝트에 대해 작업하고 시간을 기록할 때 프로젝트에 기록됩니다. 그런 다음 하청업체의 이러한 비용 트랜잭션은 공급업체 송장의 항목과 일치합니다. 이 모델에서 Project Operations를 사용하는 프로젝트 관리자는 기록 및 승인된 하청업체 시간과 공급업체 송장 라인을 일치시키고 확인할 수 있습니다. 검증이 완료되면 승인 후 기록된 비용 실제 값이 취소되고 공급업체 송장을 기반으로 하는 새 비용 실제 값이 프로젝트에 생성됩니다.
- **고정 가격** – 이 고정 요금 계약 모델에서 공급업체 송장은 고정된 중요 시점을 기반으로 합니다. 그러나 하청업체 리소스도 시간을 보고할 수 있습니다. 그런 다음 프로젝트 관리자가 시간을 검토하고 승인합니다. 승인되면 Project Operations에서 프로젝트에 대한 임시 비용 실제 값을 생성합니다. 공급업체가 중요 시점에 대한 송장을 보낸 후 프로젝트 관리자는 중요 시점에 대해 이전에 기록된 비용 실제 값을 일치시킬 수 있습니다. 검증이 완료되면 비용 실제 값이 취소되고 중요 시점 기반 비용이 기록됩니다.

## <a name="project-price-lists-on-subcontracts"></a>하도급 계약에 대한 프로젝트 가격표

프로젝트 가격표는 시간, 경비 및 기타 프로젝트 관련 구성 요소에 대한 구매 가격을 설정하는 데 사용되는 가격표입니다. 여러 가격표가 있을 수 있으며, 각 가격표에는 Project Operations에서 자체 날짜 유효 하도급 계약이 있을 수 있습니다. Project Operations는 하도급 계약의 프로젝트 가격표에 대한 중복 유효 날짜를 지원하지 않습니다.

## <a name="transaction-classes-on-subcontracts"></a>하도급 계약의 트랜잭션 클래스

Project Operations는 네 가지 유형의 트랜잭션 클래스를 지원합니다.

- 시간
- 경비
- 재료
- 티켓

구매 비용은 **시간**, **경비** 및 **재료** 트랜잭션 클래스에서만 추정 및 발생할 수 있습니다. **요금** 은 수익 전용 트랜잭션 클래스이며 구매 콘텐츠에서 사용할 수 없습니다.

## <a name="purchase-pricing-dimensions"></a>구매 가격 책정 차원

가격 책정 차원을 통해 구매 가격 설정 및 정시 트랜잭션 기본값 설정에 사용되는 특성을 결정할 수 있습니다. 구매와 관련하여 Project Operations는 구매 가격 설정 및 기본값 설정을 위한 고정 차원 집합만 지원합니다. 하도급 계약 라인 및 하도급 계약 시간 트랜잭션에 대한 구매 가격 설정 및 기본값 설정의 경우 큭성은 **역할** 및 **예약 가능한 리소스** 입니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
