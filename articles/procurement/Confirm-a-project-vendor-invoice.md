---
title: 프로젝트 공급업체 송장 확인
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations에서 프로젝트 공급업체 송장을 확인하는 방법과 프로젝트 공급업체 송장 확인의 재정적 영향에 대해 설명합니다.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475451"
---
# <a name="confirm-project-vendor-invoices"></a>프로젝트 공급업체 송장 확인

_ **적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations

**PM의 수동 확인 필요** 매개 변수가 활성화되면 Microsoft Dataverse에서 생성된 공급업체 송장은 **초안** 상태가 됩니다. 이러한 방식으로 생성된 공급업체 송장은 검토하고 수동으로 확인해야 합니다. **PM의 수동 확인 필요** 매개 변수가 비활성화되면 Dataverse에서 생성된 공급업체 송장이 자동으로 확인됩니다. 추가 작업이 필요하지 않습니다. 

Dynamics 365 Project Operations에서 공급업체 송장의 모든 라인을 확인한 후 **확인** 을 선택하여 공급업체 송장을 확인합니다.

공급업체 송장에서 **확인** 을 선택하면 다음 동작이 발생합니다.

1. 공급업체 송장의 상태가 **확인됨** 으로 업데이트됩니다.
1. 확인된 공급업체 송장 및 관련 레코드는 읽기 전용이 되며 편집하거나 삭제할 수 없습니다.
1. 실제 비용이 일치 프로세스의 일부로 공급업체 송장 라인을 참조하는 경우 참조된 공급업체 송장 라인과 연관된 모든 비용 실제가 취소됩니다.
1. 신규 원가는 공급업체 송장 라인의 정보를 사용하여 생성됩니다.
1. 더 이상 수정 분개장을 생성하거나 시간 입력의 회수를 처리하거나 취소된 원래 시간, 비용 또는 자재 실제 승인을 취소할 수 없습니다.
1. Dynamics 365 Finance에서 프로젝트 통합 저널을 사용하여 **프로젝트 원가** 값이 업데이트되고 프로젝트 통합 분개장이 전기된 후 조달 통합 계정은 *취소* 됩니다.

> [!NOTE]
> 공급업체 송장의 라인이 **완료** 이외의 확인 상태인 경우 공급업체 송장을 확인할 수 없습니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
