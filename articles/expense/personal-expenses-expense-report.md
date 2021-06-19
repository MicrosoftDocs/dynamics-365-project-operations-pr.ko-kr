---
title: 경비 보고서의 개인 경비에 대한 작업
description: 이 토픽은 업무 목적으로 여행하는 동안 직원이 발생하는 개인 경비를 처리하는 방법에 대한 정보를 제공합니다.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025692"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>경비 보고서의 개인 경비에 대한 작업

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

출장 중 직원은 회사 신용 카드로 개인 경비를 청구할 수 있습니다. 개인 경비 처리를 위한 프로세스가 정의되지 않은 경우 직원이 항목별 경비 보고서를 제출할 때 경비 보고서 승인 프로세스가 중단될 수 있습니다.

직원의 개인 경비를 처리하는 데 사용할 수 있는 두 가지 방법이 있습니다.

  - **직원이 지불**: 조직이 기업 신용 카드 청구서에 표시된 개인 경비를 지불하지 않습니다. 대신 직원이 경비를 신용 카드 공급업체에 직접 지불합니다. 
  - **회사에서 지불**: 조직에서 회사 신용 카드에 대한 전체 청구액을 지불한 다음 개인 경비로 근로자의 계좌에서 인출합니다.

**경비 관리 매개 변수** 페이지에서 조직에서 사용하는 방법을 선택할 수 있습니다.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>개인 금액 필드에 값이 정의된 경우 경비 분할 기능 활성화

**개인 금액 필드에 값이 정의된 경우 경비 분할 기능 활성화** 기능은 라인 수준 워크플로를 사용하여 승인된 경비 보고서에만 적용됩니다. 보고서는 **경비 보고서 처리** > **나에게 할당된 경비 보고서** > **경비 보고서 열기** 로 이동하여 승인됩니다. 

이 기능을 활성화하려면 **작업 영역** > **기능 관리** 로 이동하여 **개인 금액 필드에 값이 정의된 경우 경비 분할 기능 활성화** 를 선택한 다음 **지금 활성화** 를 선택합니다. 

이 기능이 활성화되면 이 기능을 사용하는 경비 라인은 보고서가 실행될 때 두 라인을 생성합니다. 승인자가 각 라인을 개별적으로 승인할 수 있도록 두 개의 라인이 생성됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
