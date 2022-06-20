---
title: 최신 승인을 위한 업그레이드 고려 사항
description: 이 문서에서는 관리자가 최신 승인 기능을 활성화할 때 고려해야 할 사항을 다룹니다.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931752"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>최신 승인을 위한 업그레이드 고려 사항 

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

2022년 4월 웨이브 1 릴리스의 일부로 최신 승인 기능이 기본적으로 활성화됩니다. 이 기능은 승인 논리의 신뢰성을 향상시키고 승인 논리가 실패한 경우 원인을 확인할 수 있도록 합니다.

이 변경의 일부로 프로젝트 승인에 대한 상태 변경이 업데이트됩니다. 이제 상태가 **제출됨** 에서 **승인됨** 으로 바로 변경됩니다. **보류 중** 은 더 이상 승인 상태가 아닙니다. 승인이 보류 중인지 확인하려면 승인이 승인 집합의 일부인지 확인하고 연결된 승인 집합의 상태를 검토합니다.

## <a name="before-you-upgrade"></a>업그레이드하기 전에

최신 승인으로 업그레이드하기 전에 보류 중인 승인이 없는지 확인하십시오. 최신 승인은 **보류 중** 상태를 사용하지 않습니다. 따라서 업그레이드 후에도 **보류 중** 으로 표시된 승인은 처리되지 않습니다.

## <a name="after-you-upgrade"></a>업그레이드 사후 작업

최신 승인으로 업그레이드한 후 관리자는 승인을 처리하는 클라우드 흐름이 활성화되었는지 확인해야 합니다.

1. [flow.microsoft.com](https://flow.microsoft.com)에 로그인합니다.
2. 페이지 오른쪽 상단에서 환경을 업그레이드한 환경으로 전환합니다.
3. **솔루션** 을 선택하여 환경에 설치된 솔루션을 나열합니다.
4. 솔루션 목록에서 **Project Operations** 또는 **Project Service** 를 선택합니다.
5. 필터를 **모두** 에서 **클라우드 흐름** 으로 변경합니다.
6. **Project Service – 프로젝트 승인 집합을 주기적으로 예약** 옵션이 **켜기** 로 설정되어 있는지 확인합니다. 그렇지 않은 경우 흐름을 선택한 다음 **켜기** 를 선택합니다.
7. **설정** 영역의 **시스템 작업** 목록을 검토하여 처리가 5분마다 발생하는지 확인합니다.

## <a name="short-term-rollback"></a>단기 롤백

변경 사항을 적용할 수 없거나 이 기능에 심각한 문제가 발생한 경우 다음 단계를 수행하여 일시적으로 원래 승인 흐름으로 되돌릴 수 있습니다.
1. 환경에 로그인하고 보류 중인 승인이 없는지 확인합니다.
2. **설정** > **프로젝트 매개 변수** 로 이동합니다.
3. **기능 제어** 를 선택한 다음 **최신 승인** 을 선택하여 기능을 끕니다.

## <a name="removing-the-feature-flag"></a>기능 플래그 제거

2022년 10월 웨이브 2 업데이트에서 이 기능을 끄는 기능이 제거됩니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
