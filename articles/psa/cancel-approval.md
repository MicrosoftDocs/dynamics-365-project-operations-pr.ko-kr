---
title: 이전에 승인된 시간 및 경비 항목 취소
description: 이 주제는 승인된 프로젝트 시간 및 경비 처리를 취소하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150586"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>이전에 승인된 시간 또는 경비 항목 취소

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

최신 버전의 Dynamics 365 Project Service Automation에서 결재자는 이전에 승인한 시간 또는 경비 항목을 취소할 수 있습니다.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>이전에 승인된 시간 또는 경비 항목 취소

다음 단계에 따라 이전에 승인한 시간 또는 경비 항목을 취소합니다.

1. **프로젝트** \> **내 작업** \> **결재** 로 이동합니다.
2. **결재** 목록 페이지에서 보기를 **내 과거 결재** 로 변경합니다. 이전에 승인한 시간 및 경비 항목 목록이 표시됩니다.
3. 하나 이상의 항목을 선택한 다음 **승인 취소** 를 선택합니다. 경고 메시지가 나타납니다.
4. **OK** 를 선택하여 승인을 취소합니다.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>시간 또는 경비 항목 승인 취소의 영향 이해

승인이 취소되면 운영상의 영향과 재무적 영향이 있습니다.

### <a name="operational-impact"></a>운영상의 영향

운영 측면에서는 승인이 취소되면 레코드 상태가 **초안** 으로 재설정되고 승인이 **내 과거 결재** 보기에 더 이상 나타나지 않습니다. 그 대신 취소된 승인은 그것이 시간 항목이냐 경비 항목이냐에 따라 **결재 대상 시간 항목** 보기 또는 **결재 대상 경비 항목** 보기에 나타납니다. 또한 관련 시간 또는 경비 항목의 상태가 **제출됨** 으로 변경되어 관련 항목이 **초안** 상태에 있는 결재와 일치합니다.

결재자로서 귀하는 **초안** 상태에 있는 승인 필드 중 일부를 편집할 수 있습니다. 이러한 필드로는 **청구 타입** 과 **시간 항목에 대한 청구 가능 시간** 이 있습니다. 변경한 후 레코드를 다시 승인할 수 있습니다. 또는 항목을 거부할 수 있습니다. 시간 항목의 승인을 거부하면 항목 상태가 **반려됨** 으로 변경됩니다. 경비 항목의 승인을 거부하면 항목 상태가 **거부됨** 으로 변경됩니다. 기능적으로 설명하면, 반려된 항목과 거부된 항목은 **초안** 상태에 있는 항목과 동일하게 기능합니다. 프로젝트 팀원은 항목에 필요한 사항을 변경한 다음 결재를 위해 항목을 다시 제출하거나 항목을 완전히 삭제할 수 있습니다.

### <a name="financial-impact"></a>재무적 영향

승인이 취소되면 프로젝트는 재정적으로도 영향을 받습니다. 첫째, 비용 및 판매에 대한 해당 실제값이 다음과 같은 방식으로 업데이트됩니다:

- 조정 상태가 **조정됨** 으로 설정됩니다.
- 청구 상태가 **취소됨** 으로 설정됩니다.

다음으로 반전 항목이 실제값 표에 만들어집니다. 반전 항목을 만들기 위해 시스템은 원래 실제값의 필드 값을 복사합니다. 복사되지 않는 값은 수량 값뿐입니다. 대신 이러한 값이 반전됩니다. **원가** 및 **미청구 매출액** 의 실제값에 대한 반전된 실제값이 생성됩니다. 반전된 실제값의 **조정 상태** 필드가 **조정 불가능** 으로 설정되고, 청구 상태가 **취소됨** 으로 설정됩니다.

이러한 변경이 이루어지면 프로젝트에 지출된 것으로 기록된 금액과 프로젝트의 수익 백로그가 더 이상 이러한 실제값이 나타내는 금액을 해명하지 못합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]