---
title: 프로젝트 기반 계약 내용에 송장 일정 만들기
description: 이 항목은 계약 내용에 대한 송장 일정 및 중요 시점을 생성하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23378b51c8324a60918ad494e7f659dbbc94e2a8
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080284"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>프로젝트 기반 계약 내용에 송장 일정 만들기 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

프로젝트 기반 계약 내용에 대한 송장 일정을 만들 수 있습니다. 송장 발행은 계약이 성사되고 프로젝트 계약을 생성한 후에만 허용됩니다. 송장 일정을 사용하면 프로젝트 기반 계약 내용에 대한 초안 송장을 자동으로 생성할 수 있습니다. 그러나 수동으로만 송장을 생성하는 경우 계약 내용에서 송장 일정 생성을 건너뛸 수 있습니다.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>계약 내용에 대한 시간 및 재료 송장 일정 생성

프로젝트 기반 계약 내용에 시간 및 재료 청구 방법이 있는 경우 날짜 기반 송장 일정을 생성할 수 있습니다. 날짜 기반 송장 일정을 자동으로 생성하려면 다음 단계를 완료하십시오.

1. **설정** > **송장 빈도** 로 이동하고 송장 빈도를 설정합니다.
2. 프로젝트 계약 레코드로 이동하고 **요약** 탭의 **요청된 배송 날짜** 필드에서 날짜를 선택합니다.
3. 날짜 기반 송장 일정을 생성하는 **시간 및 재료** 계약 내용을 엽니다. 
4. **송장 일정** 탭에서 결제 시작 날짜 및 송장 빈도를 선택합니다.
5. 하위 표에서 **송장 일정 생성** 을 선택합니다. 송장 일정은 다음과 같은 방식으로 설정되는 **송장 실행 날짜** , **트랜잭션 마감일** 및 **실행 상태** 필드를 사용하여 생성됩니다.

    - **송장 실행 날짜** : 이 날짜는 송장 빈도에 따라 지정됩니다.
    - **트랜잭션 마감일** : 송장 실행 날짜의 전날입니다.
    - **실행 상태** : **실행되지 않음** 으로 자동 설정됩니다. 자동 송장 생성 작업이 특정 송장 실행 날짜에 실행되면 이 필드를 **성공적으로 실행** 또는 **실행 실패** 로 업데이트합니다.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>계약 내용에 대한 고정 가격 송장 일정 생성

계약 내용에 고정 결제 방법이 있으면 중요 시점 기반 송장 일정을 생성할 수 있습니다. 

> [!NOTE]
> 계약 내용에 매핑된 프로젝트가 없는 경우 계약 내용에 중요 시점을 생성할 수 없습니다.

달력 기간 동안 균등하게 분배되는 중요 시점의 고정 집합에 대해 중요 시점 송장 일정을 생성하려면 다음 단계를 완료하십시오.

1. **설정** > **송장 빈도** 로 이동하고 송장 빈도를 설정합니다.
2. 프로젝트 계약 레코드로 이동하고 **요약** 탭의 **요청된 배송 날짜** 필드에서 날짜를 선택합니다.
3. 중요 시점 일정을 생성 중인 **고정 가격** 계약 내용을 엽니다. **청구 중요 시점** 탭에서 결제 시작 날짜 및 송장 빈도를 선택합니다. 
4. 하위 표에서 **주기적인 중요 시점 생성** 을 선택합니다. 송장 일정은 **중요 시점 이름** , **중요 시점 날짜** 및 **중요 시점 금액** 필드는 다음과 같이 생성됩니다.

    - **중요 시점 이름** : 이 날짜는 송장 빈도에 따라 지정됩니다.
    - **중요 시점 날짜** : 이 날짜는 송장 빈도에 따라 지정됩니다.
    - **중요 시점 금액** : 이 금액은 계약 내용의 계약 금액을 빈도, 청구 시작 및 요청된 배송 날짜로 지정된 중요 시점 수로 나누어 계산됩니다.

    계약 내용의 **추정 세액** 필드에 값이 있는 경우 이 필드는 주기적 중요 시점을 생성할 때 각 중요 시점에 동일하게 할당됩니다.

청구 중요 시점은 계약 내용의 계약 값과 같아야 합니다. 그렇지 않으면 **계약 내용** 페이지에 오류가 발생합니다. 중요 시점을 생성, 편집 또는 삭제하여 청구 중요 시점이 라인의 계약된 값의 합계인지 확인하여 오류를 수정할 수 있습니다. 변경한 후 페이지를 새로 고쳐 오류를 제거합니다.

### <a name="manually-create-milestones"></a>수동으로 중요 시점 생성

주기적으로 분할되지 않는 경우 고정 가격 중요 시점을 수동으로 생성할 수 있습니다. 중요 시점을 수동으로 생성하려면 다음 단계를 완료하십시오.

1. 중요 시점을 생성할 고정 가격 계약 내용을 열고 **송장 일정** 탭의 하위 표에서 **+ 새 계약 내용 중요 시점 만들기** 를 선택합니다. 
2. **중요 시점 만들기** 페이지에서 다음 표에 따라 필요한 정보를 입력합니다.

| 필드 | 위치 | 관련성, 목적 및 지침 | 다운스트림 영향 |
| --- | --- | --- | --- |
| 이정표 이름 | 빨리 만들기 | 중요 시점 이름의 텍스트 필드입니다. | 이것은 프로젝트 계약 내용 중요 시점 및 송장으로 전달됩니다. |
| 프로젝트 작업 | 빨리 만들기 | 중요 시점이 프로젝트 작업에 연결되어 있는 경우 이 참조를 사용하여 작업 상태에 따라 중요 시점 상태를 설정하는 사용자 지정 논리를 추가합니다. | 애플리케이션은 작업에 대한 이 참조의 다운스트림 영향을 미치지 않습니다. |
| 이정표 날짜 | 빨리 만들기 | 자동 송장 생성 프로세스가 이 중요 시점의 상태를 송장 발행을 위해 고려해야 하는 날짜를 설정합니다. | 이것은 프로젝트 계약 내용 중요 시점 및 송장으로 전달됩니다. |
| 송장 상태 | 빨리 만들기 | 중요 시점이 생성되면 이 상태는 **송장 발부 준비 안 됨** 또는 **시작 안 됨** 으로 설정됩니다. | 이것은 프로젝트 계약 내용 중요 시점 및 송장으로 전달됩니다. |
| 라인 금액 | 빨리 만들기 | 고객에게 청구될 중요 시점의 금액 또는 값입니다. | 이것은 프로젝트 계약 내용 중요 시점 및 송장으로 전달됩니다. |
| 세금 | 빨리 만들기 | 중요 시점에 적용되는 세액입니다. | 이것은 프로젝트 계약 내용 중요 시점 및 송장으로 전달됩니다. |

3. **저장 후 닫기** 를 선택합니다.