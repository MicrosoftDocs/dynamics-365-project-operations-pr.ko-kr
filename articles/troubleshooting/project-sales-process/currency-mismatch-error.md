---
title: 통화 불일치 오류
description: 이 토픽에서는 특정 레코드 유형을 저장할 때 발생하는 통화 불일치 오류에 대한 문제 해결 정보를 제공합니다.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589756"
---
# <a name="currency-mismatch-error"></a>통화 불일치 오류 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

프로젝트, 계약, 견적 또는 예약 가능한 리소스를 저장할 때 **소유 회사 통화가 계약 단위 통화와 일치하지 않음 오류가 수신될 수 있습니다. 계속하려면 다른 소유 회사 또는 계약 단위를 선택하십시오.** 이는 레코드의 계약 단위 통화와 소유 회사 통화 사이에 통화 불일치가 있기 때문입니다.


## <a name="resolution"></a>해상도

문제를 해결하려면 다음을 수행합니다.
- 이 레코드에 대한 계약 단위의 통화를 확인하십시오. 조직 단위 레코드를 열고 **통화** 필드의 **일반** 탭에서 값을 확인하여 통화를 볼 수 있습니다.
- 소유 회사의 통화를 확인합니다. 회사 기록의 **관련 항목** > **원장** 으로 이동하면 통화를 볼 수 있습니다. 회사와 연결된 원장 레코드를 두 번 클릭하고 **회계 통화** 필드의 **일반** 탭에서 값을 확인합니다.

계약 단위에 설정된 통화와 원장 레코드가 일치하지 않는 경우 레코드를 저장할 때 구성을 조정하거나 다른 값을 선택하십시오. 회사 간 송장 발행 흐름이 올바른지 확인하려면 시스템에서 이러한 레코드가 일치해야 합니다. 회사 간 구성에 대한 자세한 내용은 [회사 간 트랜잭션 만들기](../../project-accounting/create-intercompany-transactions.md)를 참조하십시오..

회사 레코드에 연결된 원장 레코드가 없는 경우 환경을 설정할 때 구성이 누락되었음을 나타냅니다. 시스템 관리자가 구성을 수정해야 합니다. 시스템 관리자는 **이중 쓰기 구성** 으로 이동하여 이 맵의 초기 동기화 및 전제 조건과 함께 **원장 이중 쓰기 맵** 을 중지했다가 다시 시작해야 합니다. 자세한 내용은 [Project Operations 이중 쓰기 맵 버전](../../environment/resource-dual-write-maps.md)을 참조하십시오.
