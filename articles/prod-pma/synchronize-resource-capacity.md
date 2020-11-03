---
title: 리소스 용량 동기화
description: 이 항목은 일정과 프로젝트에서 리소스의 용량을 동기화하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080030"
---
# <a name="synchronize-resource-capacity"></a>리소스 용량 동기화

[!include [banner](../includes/banner.md)]

리소스 동기화를 위한 프로세스는 일정 및 기본 일정에 대한 정보가 프로젝트 리소스 스케줄링으로 흘러 들어가는 것을 보장합니다. 일정이 변경되면 프로세스가 프로젝트 리소스 일정에 필요한 업데이트를 수행합니다. 일정의 리소스 정보가 미리 동기화되기 때문에 프로세스는 성능 향상에도 도움이 됩니다. 따라서 리소스 예약 정보에 대한 업데이트가 더 빨리 발생합니다. 프로세스를 한 번에 하나씩이 아닌 일괄 처리로 예약하는 것이 좋습니다. 그렇지 않으면 정보가 마지막으로 동기화된 포함 날짜를 잊어 버릴 위험이 있습니다. 포함 날짜를 사용하지 않으면 날짜 동기화 중에 간격이 발생할 수 있습니다.

![일정 동기화](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>리소스 생산 능력 롤업 동기화

동기화 프로세스는 모든 리소스 일정 정보를 동기화하도록 설계되었습니다. 이 정보에는 프로젝트의 리소스 일정 생산 능력 테이블 변경 사항에 대한 기본 일정 정보가 포함됩니다. 프로젝트에 새 리소스가 추가된 경우 동기화를 통해 업데이트된 일정 정보를 사용할 수 있습니다. 이 동기화는 언제든지 수행할 수 있습니다.

일괄 처리를 사용하는 것이 좋습니다. 이 옵션은 용량 예약 동기화 중에 사용할 수 있습니다.

1. **프로젝트 관리 및 회계** &gt; **주기적** &gt; **용량 동기화** &gt; **리소스 용량 롤업 동기화** 를 선택합니다.
2. 다음 표에서 옵션을 설정합니다.

    | 옵션      | 설명 |
    |-------------|-------------|
    | 기간 코드 | 선택적으로 총계정 원장 날짜 간격 코드를 선택하여 리소스 용량 롤업을 위한 동기화 프로세스의 시작 및 종료 날짜를 설정합니다. |
    | 시작 날짜  | 리소스 용량 롤업을 위한 동기화 프로세스의 시작 날짜를 입력합니다. |
    | 종료 날짜    | 리소스 용량 롤업을 위한 동기화 프로세스의 종료 날짜를 입력합니다. |

[![동기화 프로세스](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
