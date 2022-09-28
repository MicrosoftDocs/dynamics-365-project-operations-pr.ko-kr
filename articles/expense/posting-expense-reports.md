---
title: 경비 보고서 게시
description: 이 문서에서는 경비 보고서를 게시하는 방법에 대해 설명합니다.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524878"
---
# <a name="post-expense-reports"></a>경비 보고서 게시

경비 보고서가 승인되고 일반 분개장으로 이전된 후 전기할 수 있습니다. 경비 보고서를 전시하면 부가가치세(VAT) 공제 대상 경비가 식별됩니다. VAT 지불 확인 및 복구 작업은 경비 보고서 확인을 담당하는 직원에게 할당됩니다.

경비 보고서의 비용이 직원을 고용한 회사가 아닌 다른 회사에 청구되는 경우 해당 경비를 지불해야 하는 회사와 지불 받아야 하는 회사를 모두 확인해야 합니다. 예를 들어 경비 보고서를 제출한 직원은 DAT 회사에서 근무하지만 DIR 회사에 비용을 청구했습니다. 이 경우 DAT는 경비를 지불해야 하는 회사이고 DIR은 비용을 지불 받아야 하는 회사입니다. 이러한 분개장 항목을 확인한 후 경비 라인을 총계정 원장에 전기할 수 있습니다.

경비 보고서를 전기하려면 **승인된 경비 보고서** 페이지에서 경비 보고서를 선택한 다음 작업 창에서 **경비** 를 선택합니다.

동시에 목록의 모든 경비 보고서를 전기할 수도 있습니다. 모든 경비 보고서를 선택한 다음 **전기** 를 선택합니다.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>현금 결제 방법에 대해 공급업체 통화로 경비 부채를 전기할 수 있는 기능 활성화

**현금 결제 방법에 대해 공급업체 통화로 경비 부채를 전기할 수 있는 기능** 을 사용하면 현금 결제 방법에 대해 공급업체 통화로 경비 보고서를 전기할 수 있습니다.

현재는 현금 경비를 제출하면 경비 보고서가 회계 통화로 전기됩니다. 거래 통화, 회계 통화 및 공급 업체 통화 간의 금액 변환으로 인해 경비의 거래 날짜와 실제 지불 날짜의 환율이 다른 경우 잘못된 금액이 공급 업체에 지급됩니다.

이 기능을 사용하면 경비 보고서가 전기될 때 공급업체 잔액이 공급업체 통화로 기록됩니다.

1. **작업 영역** \> **기능 관리** 로 이동합니다.
2. 목록에서 **현금 결제 방법에 대해 공급업체 통화로 경비 부채를 전기할 수 있는 기능** 을 찾아 선택한 다음 **지금 활성화** 를 선택합니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
