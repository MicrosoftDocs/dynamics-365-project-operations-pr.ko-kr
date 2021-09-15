---
title: Project Service Automation의 승인 집합
description: 이 항목은 승인 집합, 요청 및 해당 작업의 하위 집합에 대한 정보를 제공합니다.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323559"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation의 승인 집합

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

승인 집합은 승인 요청을 더 작은 작업 하위 집합으로 그룹화합니다. 이 그룹화를 사용하면 프로젝트별로 승인을 순서대로 처리할 수 있으며 재시도 및 순서 지정이 가능합니다. 그룹화는 대량 승인에 대한 승인 처리의 신뢰성과 추적성을 향상시킵니다.

승인 집합은 관련 레코드의 전체 처리 상태를 나타냅니다. 승인 집합을 사용하여 승인 레코드를 처리하면 레코드가 **제출됨** 에서 **승인됨** 으로 이동하며 승인 집합에서 연결 해제됩니다. 승인을 위해 제출할 때 레코드가 실패하면 레코드는 **제출됨** 상태로 유지되고 승인 집합은 실패로 표시됩니다. 승인 집합은 실패 오류 메시지를 기록합니다.

## <a name="processing-approvals-and-approval-sets"></a>승인 및 승인 집합 처리
처리 대기 중인 승인은 **승인 처리 중** 보기에 표시됩니다. 시스템은 이전 시도가 실패한 경우 승인 재시도를 포함하여 모든 항목을 비동기적으로 여러 번 처리하려고 합니다.

**승인 집합 수명** 필드는 실패로 표시되기 전에 집합을 처리하기 위해 남은 시도 횟수를 기록합니다.

## <a name="failed-approvals-and-approval-sets"></a>실패한 승인 및 승인 집합
**실패한 승인** 보기는 사용자 개입이 필요한 모든 승인을 나열합니다. 연관된 승인 집합 로그를 열어 실패 원인을 식별하십시오.
**재시도** 를 선택하면 승인 집합 수명 수가 추가되고 승인 집합이 다시 **처리 중** 상태로 이동하며 나머지 레코드 처리를 시도합니다.

## <a name="configure-approval-sets"></a>승인 집합 구성

###  <a name="enable-the-approval-sets-feature"></a>승인 집합 기능 활성화
승인 집합 기능을 활성화하기 전에 현재 처리 중인 승인이 없는지 확인하십시오.

- **프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 활성화** 를 선택합니다.

### <a name="turn-off-the-approval-sets-feature"></a>승인 집합 기능 끄기
승인 집합 기능을 끄기 전에 현재 처리 중인 승인이 없는지 확인하십시오.

- **프로젝트 매개 변수** 페이지로 이동하고 **기능 제어** > **최신 승인 비활성화** 를 선택합니다.

### <a name="configuring-the-asynchronous-threshold"></a>비동기 임계값 구성 
승인 집합이 생성될 때 승인을 위해 선택한 레코드 수가 표시된 임계값을 초과하면 처리가 백그라운드로 이동합니다. **비동기 임계값** 필드를 사용하여 승인 처리를 동기 또는 비동기적으로 실행해야 하는 시기를 구성합니다.
유효한 값:

  - 0: 모든 요청이 비동기적으로 처리되어야 합니다. 
  - 0보다 큰 숫자: 제출된 승인 수가 이 값을 초과하는 경우에만 승인이 비동기적으로 처리됩니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
