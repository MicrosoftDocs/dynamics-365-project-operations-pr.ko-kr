---
title: 실제 값
description: 이 문서는 Microsoft Dynamics 365 Project Operations에서 실제 값으로 작업하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924806"
---
# <a name="actuals"></a>실제 값

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

실제는 프로젝트에 대한 검토 및 승인된 재무 및 일정 진행 상황을 나타냅니다. 시간, 비용 및 자재 사용량 항목, 분개장 항목 및 송장이 승인될 때 생성됩니다.

> [!IMPORTANT]
> 실제를 편집하거나 시스템에서 삭제해서는 안 됩니다. 그렇지 않으면 재무 건전성과 다른 재무 및 회계 시스템과의 통합이 부정적인 영향을 받을 수 있습니다. Microsoft Dynamics 365 Project Operations를 사용하면 프로젝트의 비즈니스 프로세스 수명 주기의 다양한 지점에서 실제 값을 편집하고 반전을 사용할 수 있습니다.

## <a name="recording-actuals-based-on-project-events"></a>프로젝트 이벤트에 근거한 실제값 기록

Project Operations는 프로젝트 참여 수명 주기 동안 발생한 금융 거래를 실제 거래로 기록합니다. 수명 주기의 다양한 이벤트에서 실제 생성은 프로젝트 계약이 시간 및 자재 청구 모델을 사용하는지 아니면 고정 가격 청구 모델을 사용하는지, 그리고 사전 판매 단계에 있는지 아니면 내부 프로젝트인지에 따라 다릅니다.

다음 문서에서는 다양한 변형에 대한 다양한 이벤트에서 실제 테이블에 미치는 영향에 대해 설명합니다.

- [시간 및 자재 계약의 실제 값 영향](ActualsonTM.md)
- [고정 가격 계약의 실제 값 영향](ActualonFP.md)
- [계약의 사전 판매 단계에서 실제 영향](ActualonPreSales.md)
- [내부 프로젝트에 대한 실제 영향](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
