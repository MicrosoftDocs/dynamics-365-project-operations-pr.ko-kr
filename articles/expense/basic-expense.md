---
title: 경비 항목(라이트)
description: 이 문서에서는 라이트 배포에서 경비 입력을 사용하는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917952"
---
# <a name="expense-entry-lite"></a>경비 항목(라이트)

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

기본 또는 라이트 경비 관리는 간단한 경비를 기록하는 기능입니다. 프로젝트에 대한 경비를 기록할 수 있으며 프로젝트 승인자가 이를 검토하고 승인합니다.

Dynamics 365 Project Operations에서 경비 기능에 대한 자세한 내용은[경비 개요](expense-overview.md)를 참조하십시오.

## <a name="capture-a-basic-expense"></a>기본 경비 캡처

승인자에게 제출할 수 있도록 경비를 캡처할 수 있습니다.

1. **경비** 로 이동하고 **새로 만들기** 를 선택합니다.
2. **새 경비** 페이지에서 필요한 경비 정보를 입력하고 **저장** 을 선택합니다.

## <a name="submit-a-basic-expense"></a>기본 경비 제출

모든 경비 수집을 완료하고 승인을 받을 준비가 되었으면 이를 제출해야 합니다.

1. **경비** 로 이동하고 경비를 선택합니다. 또는 헤더의 확인란을 사용하여 모든 경비를 선택합니다.
2. **제출** 을 선택합니다. 시스템은 선택한 항목을 처리한 다음 경비 승인 요청을 생성합니다.

## <a name="add-an-attachment"></a>첨부 파일 추가

승인자에게 경비에 대한 추가 문서를 제공해야 할 수 있습니다. 경비 항목의 타임라인에 영수증을 첨부할 수 있습니다. **편집** 을 선택하고 **타임라인** 섹션을 선택한 다음 종이 클립 아이콘을 선택하여 영수증을 첨부합니다.

## <a name="recall-a-basic-expense"></a>기본 경비 회수

실수로 경비를 제출하면 회수할 수 있습니다. 경비 항목을 회수하는 데 필요한 시간은 승인 스테이지에 따라 다릅니다.  승인자가 아직 항목을 승인하지 않은 경우 즉시 회수할 수 있습니다. 그러나 입력이 이미 승인된 경우 승인자는 회수를 승인하고 트랜잭션을 취소하도록 요청합니다.

1. **경비** 로 이동한 다음 경비 목록에서 회수할 경비를 선택합니다.
2. **철회** 를 선택합니다. 경비 입력이 아직 승인되지 않은 경우 시스템은 즉시 이를 회수합니다. 경비 항목이 이미 승인된 경우 승인자에게 경비를 취소할 것임을 알리는 회수 요청이 생성됩니다. 그런 다음 승인자는 취소를 수행할 수 있는지 확인하고 항목이 반환됩니다.

## <a name="delete-a-basic-expense"></a>기본 경비 삭제

아직 제출되지 않은 경비는 삭제할 수 있습니다. 이미 제출된 경비를 삭제하려면 먼저 회수해야 합니다.

## <a name="see-also"></a>참조

- [승인 개요](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]