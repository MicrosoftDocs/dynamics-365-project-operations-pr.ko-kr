---
title: 프로젝트 공급업체 송장 확인
description: 이 항목에서는 Microsoft Dynamics 365 Project Operations에서 프로젝트 공급업체 송장을 확인하는 방법과 프로젝트 공급업체 송장 확인의 재정적 영향에 대해 설명합니다.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595736"
---
# <a name="confirm-a-project-vendor-invoice"></a>프로젝트 공급업체 송장 확인

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Microsoft Dynamics 365 Project Operations에서 공급업체 송장의 모든 라인을 확인한 후 확인 작업을 사용하여 공급업체 송장을 확인할 수 있습니다.

공급업체 송장에서 **확인** 을 선택하면 다음 동작이 발생합니다.

1. 공급업체 송장의 상태가 **확인됨** 으로 업데이트됩니다.
2. 확인된 공급업체 송장 및 관련 레코드는 읽기 전용이 되며 편집하거나 삭제할 수 없습니다.
3. 실제 비용이 일치 프로세스의 일부로 공급업체 송장 라인을 참조하는 경우 참조된 공급업체 송장 라인과 연관된 모든 비용 실제가 취소됩니다.
4. 신규 원가는 공급업체 송장 라인의 정보를 사용하여 생성됩니다.
5. 공급업체 송장이 확정된 후에는 더 이상 수정 분개장을 생성하거나 시간 입력 회수를 처리하거나 취소된 원래 시간, 비용 또는 자재 실제 승인을 취소할 수 없습니다.

> [!NOTE]
> 공급업체 송장의 라인이 **완료** 이외의 확인 상태인 경우 공급업체 송장을 확인할 수 없습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
