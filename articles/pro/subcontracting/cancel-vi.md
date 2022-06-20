---
title: 프로젝트 공급업체 송장 취소
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations에서 프로젝트 공급업체 송장을 취소하는 방법과 프로젝트 공급업체 송장 취소의 재정적 영향에 대해 설명합니다.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911558"
---
# <a name="cancel-a-project-vendor-invoice"></a>프로젝트 공급업체 송장 취소

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

공급업체 송장이 확인된 후에는 편집하거나 삭제할 수 없습니다. 확인된 공급업체 송장에 오류가 있는 경우 취소 작업을 사용하여 공급업체 송장의 영향을 되돌리고 새 공급업체 송장을 생성할 수 있습니다.

공급업체 송장에서 **취소** 를 선택하면 다음 동작이 발생합니다.

1. 공급업체 송장의 상태가 **취소됨** 으로 업데이트됩니다.
2. 취소된 공급업체 송장 및 관련 레코드는 읽기 전용이 되며 편집하거나 삭제할 수 없습니다.
3. 공급업체 송장 확인의 일부로 공급업체 송장 라인을 기반으로 생성된 실제 원가는 취소됩니다.
4. 실제 비용이 일치 프로세스의 일부로 공급업체 송장 라인에 연결된 경우 원래 공급업체 송장 확인에서 이를 취소했습니다. 공급업체 송장을 취소하는 동안 실제 비용이 다시 생성됩니다. 출처는 시간, 비용 또는 재료 사용량 항목을 가리킵니다.
5. 공급업체 송장이 취소된 후 수정 분개장을 다시 생성하고 시간 입력 회수를 처리하고 원래 시간, 비용 또는 실제 자재의 승인을 취소할 수 있습니다.

> [!NOTE]
> 확인된 프로젝트 공급업체 송장만 취소할 수 있습니다. 다른 상태의 공급업체 송장은 취소할 수 없습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
