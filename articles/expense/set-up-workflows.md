---
title: 경비 관리를 위한 워크플로 설정
description: 출장 및 경비 문서를 검토하고 승인하는 데 사용되는 워크플로 프로세스를 설정할 수 있습니다.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127706"
---
# <a name="set-up-workflows-for-expense-management"></a>경비 관리를 위한 워크플로 설정

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

출장 및 경비 문서를 검토하고 승인하는 워크플로 프로세스를 설정할 수 있습니다. 경비 보고서, 출장 요청 및 현금 서비스 요청에 대한 워크플로를 정의할 수 있습니다.

워크플로는 비즈니스 프로세스를 나타내며 문서가 시스템을 통과하는 방식을 정의합니다. 워크플로는 또한 작업을 완료하거나 문서를 승인해야 하는 사람을 나타냅니다. 조직에서 워크플로 시스템을 사용하면 다음과 같은 몇 가지 이점이 있습니다.

- **일관된 프로세스**: 구매 요청, 경비 보고서 등 특정 문서에 대한 승인 프로세스를 정의할 수 있습니다. 워크플로 시스템을 사용하면 문서를 일관되고 효율적인 방식으로 처리하고 승인할 수 있습니다.
- **프로세스 가시성**: 특정 워크플로 인스턴스의 상태, 기록 및 성능 메트릭을 추적할 수 있습니다. 이를 통해 효율성 향상을 위해 워크플로를 변경해야 하는지 여부를 결정할 수 있습니다.
- **중앙 집중식 작업 목록**: 사용자는 중앙 집중식 작업 목록을 보고 자신에게 할당된 워크플로 작업 및 승인을 볼 수 있습니다. 

## <a name="workflow-types"></a>워크플로 유형

다음 표에는 **경비 관리** 에서 만들 수 있는 워크플로 유형이 나열되어 있습니다.


|              <strong>유형</strong>              |                   <strong>이 유형 사용</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>경비 보고서 자동 승인</strong> |            경비 보고서에 대한 승인 워크플로를 만듭니다.             |
|  <strong>경비 보고서 자동 게시</strong>   |        경비 보고서에 대한 자동 게시 워크플로를 만듭니다.        |
|       <strong>경비 라인 항목</strong>        |     경비 보고서에 라인 항목에 대한 승인 워크플로를 만듭니다.      |
| <strong>경비 라인 항목 자동 게시</strong> | 경비 보고서에 라인 항목에 대한 자동 게시 워크플로를 만듭니다. |
|       <strong>여행 요청</strong>       |          여행 요청에 대한 승인 워크플로를 만듭니다.           |
|      <strong>현금 서비스 요청</strong>      |         현금 서비스 요청에 대한 승인 워크플로를 만듭니다.          |
|        <strong>VAT 세금 회수</strong>        | 부가가치세(VAT) 회수를 위한 승인 워크플로를 만듭니다.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]