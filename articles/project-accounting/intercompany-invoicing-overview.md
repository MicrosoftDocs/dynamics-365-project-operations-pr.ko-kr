---
title: 회사 간 송장 개요
description: 이 토픽은 프로젝트에 대한 회사 간 송장에 대한 정보와 예를 제공합니다.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b7bb4384657c71552390bbc3d60f3c5d0e4136b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586260"
---
# <a name="intercompany-invoicing-overview"></a>회사 간 송장 개요

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

조직에 프로젝트를 위해 제품과 서비스를 서로 이전하는 여러 부서, 자회사 및 기타 법인이 있을 수 있습니다. 서비스 또는 제품을 제공하는 법인을 *대출 법인* 이라고 합니다. 서비스 또는 제품을 받는 법인을 *차용 법인* 이라고 합니다.

다음 그림은 Contoso Robotics USA(차용 법인)와 Contoso Robotics UK(대출 법인)라는 두 법인이 리소스를 공유하여 고객에게 프로젝트 인 Adventure Works를 제공하는 일반적인 시나리오를 보여줍니다. 이 시나리오에서 Contoso Robotics USA는 Adventure Works에 작업을 제공하도록 계약을 맺었습니다.

![회사 간 송장.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations는 다음 흐름을 사용하여 회사 간 트랜잭션을 처리합니다.

1. 대출 법인의 리소스는 차용 법인의 프로젝트에 대한 예약 시간 및 경비를 통해 회사 간 시간 또는 비용 트랜잭션을 기록합니다.
2. 시간 및 경비 비용은 차용 회사의 단위 비용 가격표를 사용하여 대출 회사에 기록됩니다.
3. 회사 간 미청구 판매 트랜잭션은 차용 회사의 단위 비용 가격표를 사용하여 대출 회사에 기록됩니다.
4. 미 청구 수익은 프로젝트 계약 판매 가격표를 사용하여 차용 회사에 기록됩니다. 미 청구 수익이 기록되면 고객에게 청구될 수 있습니다. 고객은 회사 간 송장 처리가 완료될 때까지 기다릴 필요가 없습니다.
5. 회사 간 고객 송장은 대출 회사에서 정기적으로 생성됩니다. 송장은 수동으로 또는 정기적인 자동화 프로세스를 사용하여 생성됩니다. 각 차용 법인에 대해 단일 송장을 생성하거나 프로젝트별로 별도의 송장을 생성할 수 있습니다.
6. 회사 간 고객 송장이 대출 법인에 전기되면 해당 보류 공급업체 송장이 차용 법인에 생성됩니다. 보류 중인 공급업체 송장의 원가는 송장이 전기될 때 프로젝트 보조 원장에 기록됩니다.

다음 다이어그램은 회계 이벤트 및 총계정 원장에 대한 예상 전기와 관련된 회사 간 송장을 보여줍니다.

![회사 간 흐름.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>추가 리소스

- [회사 간 송장 구성](configure-intercompany-invoicing.md)
- [회사 간 트랜잭션 기록](create-intercompany-transactions.md)
- [회사 간 고객 및 공급업체 송장 만들기](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]