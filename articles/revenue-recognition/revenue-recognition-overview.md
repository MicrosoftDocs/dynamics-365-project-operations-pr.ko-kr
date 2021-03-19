---
title: 수익 인식 개요
description: 이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278876"
---
# <a name="revenue-recognition-overview"></a>수익 인식 개요

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Dynamics 365 Project Operations에서 수익 인식 원칙은 프로젝트 또는 프로젝트 일부에 대해 선택한 청구 방법에 따라 다릅니다. 이 토픽은 Project Operations에서 수익 인식에 대한 정보를 제공합니다.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>시간 및 자재 청구 방법을 사용하여 계산된 트랜잭션

- 비용과 수익 인식이 연결됩니다. 트랜잭션 비용 및 미 청구 판매는 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다.
- 프로젝트 비용 및 수익 프로필은 미 청구 판매 트랜잭션이 총계정 원장에 전기되는지 여부를 결정합니다. **수익 발생** 을 선택하면 전기 중에 **WIP 판매 가치** 및 **발생한 수익 판매 가치** 계정이 사용됩니다. 다음은 이 방법의 예입니다.  

  | 거래 유형 | 차변/대변 | 수량 |
  | --- | --- | --- |
  | WIP 판매 가치 | 차변 | 100 |
  | 발생한 수익 판매 가치 | 대변 | 100 |

- 송장 발행 중에 수익이 인식됩니다. 시스템은 게시하는 동안 **청구된 수익** 계정을 사용합니다. 다음은 이 방법의 예입니다.  

  | 거래 유형 | 차변/대변 | 수량 |
  | --- | --- | --- |
  | 고객 잔액 | 차변 | 120 |
  | 판매세 납부 | 대변 | 20 |
  | 송장 발부된 수익 | 대변 | 100 |

- 미 청구 판매가 전기될 때 수익이 발생한 경우 시스템은 송장 발행시 발생한 수익을 취소합니다.

  | 거래 유형 | 차변/대변 | 수량 |
  | --- | --- | --- |
  | WIP 판매 가치 | 대변 | 100 |
  | 발생한 수익 판매 가치 | 차변 | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>고정 가격 청구 방법을 사용하여 계산된 트랜잭션

- 비용과 수익 인식은 별도입니다. 트랜잭션 비용은 [Project Operations 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 사용하여 전기됩니다. 미 청구 판매 트랜잭션은 생성되지 않습니다.
- 프로젝트 비용 및 수익 프로필에 **프로젝트 완료 계산에 사용되는 원칙** 이 **WIP 없음** 으로 설정된 경우 송장 발행 중에 수익을 인식할 수 있습니다. 이 방법은 단기적이고 간단한 프로젝트에만 사용하십시오.
- 수익은 **완료된 계약** 또는 **완료율 수익 인식** 방법으로 고정 가격 수익 추정치를 사용하여 인식할 수 있습니다.

## <a name="additional-resources"></a>추가 리소스
[청구 가능한 프로젝트에 대한 회계 구성 문서](../project-accounting/configure-accounting-billable-projects.md)

[고정 가격 수익 프로젝트 추정](rev-rec-percentage-completion-method.md)

[수익 추정치 관리](rev-rec-completed-contract-method.md)

[방법을 완료하는 데 드는 비용](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]