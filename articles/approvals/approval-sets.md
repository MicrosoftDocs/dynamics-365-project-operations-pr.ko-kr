---
title: 승인 집합
description: 이 항목에서는 승인 집합, 요청 및 이러한 작업의 하위 집합을 사용하는 방법을 설명합니다.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323244"
---
# <a name="approval-sets"></a>승인 집합

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

승인 집합은 승인 요청을 더 작은 작업 하위 집합으로 그룹화합니다. 이 그룹화를 통해 프로젝트별로 특정 순서로 승인을 처리하고 재시도 및 순서를 지정할 수 있습니다. 승인 요청을 그룹화하면 대량 승인에 대한 승인 처리의 안정성과 추적 가능성이 향상됩니다.

승인 집합은 관련 레코드의 전체 처리 상태를 나타냅니다. 승인 집합을 사용하여 승인 레코드가 처리되면 레코드가 **제출됨** 에서 **승인됨** 으로 이동하고 더 이상 승인 집합에 연결되지 않습니다. 승인을 위해 제출할 때 레코드가 실패하면 레코드는 **제출됨** 상태로 유지되고 승인 집합은 실패로 표시됩니다. 승인 집합은 실패 오류 메시지를 기록합니다.

## <a name="processing-approvals-and-approval-sets"></a>승인 및 승인 집합 처리
처리 대기 중인 승인은 **승인 처리 중** 보기에 표시됩니다. 시스템은 이전 시도가 실패한 경우 승인을 재시도하는 것을 포함하여 모든 항목을 비동기식으로 여러 번 처리합니다.

**승인 집합 수명** 필드는 실패로 표시되기 전에 집합을 처리하기 위해 남은 시도 횟수를 기록합니다.

## <a name="failed-approvals-and-approval-sets"></a>실패한 승인 및 승인 집합
**승인 실패** 보기에는 사용자 개입이 필요한 모든 승인이 나열됩니다. 연관된 승인 집합 로그를 열어 실패 원인을 식별하십시오.
**재시도** 를 선택하면 승인 집합 수명 수가 추가되고 승인 집합이 다시 **처리 중** 상태로 이동하며 나머지 레코드 처리를 시도합니다.

## <a name="configure-approval-sets"></a>승인 집합 구성

### <a name="enable-the-approval-sets-feature"></a>승인 집합 기능 활성화
승인 집합 기능을 활성화하기 전에 현재 처리 중인 승인이 없는지 확인하십시오.

- **프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 활성화** 를 선택합니다.

### <a name="turn-off-the-approval-sets-feature"></a>승인 집합 기능 끄기
승인 집합 기능을 끄기 전에 현재 처리 중인 승인이 없는지 확인하십시오.

- **프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 비활성화** 를 선택합니다.

### <a name="configuring-the-asynchronous-threshold"></a>비동기 임계값 구성 
승인 집합이 생성될 때 승인을 위해 선택한 레코드 수가 표시된 임계값을 초과하면 처리가 백그라운드로 이동합니다. **비동기 임계값** 필드를 사용하여 승인 처리를 동기 또는 비동기적으로 실행해야 하는 시기를 구성합니다. 다음 값 중 하나를 선택하십시오.

  - 0: 모든 요청이 비동기적으로 처리되어야 합니다. 
  - 0보다 큰 숫자: 제출된 승인 수가 이 값을 초과하는 경우에만 승인이 비동기적으로 처리됩니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]