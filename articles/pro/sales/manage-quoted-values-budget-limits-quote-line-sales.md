---
title: 프로젝트 기반 견적 라인(Pro)
description: 이 항목은 프로젝트 작업에 프로젝트 기반 견적 라인 사용에 대한 정보를 제공합니다. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908343"
---
# <a name="project-based-quote-lines-pro"></a>프로젝트 기반 견적 라인(Pro)

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

프로젝트 기반 견적 라인은 계약에 대한 프로젝트 작업을 추정하는 데 도움이 되도록 설계되었습니다. 프로젝트 기반 견적 라인의 구조는 다음 개념으로 프로젝트 견적을 위해 확장됩니다.

- 청구 방법
- 프로젝트 및 작업 매핑
- 포함된 트랜잭션 클래스
- 초과 안 함 한도
- 청구 가능성 설정
- 견적 라인 세부 정보를 사용한 추정
- 견적 라인 고객

다음 표는 프로젝트 기반 견적 라인의 **일반** 탭의 필드에 대한 정보를 제공합니다. 이 필드는 프로젝트 작업에 대한 상세하고 기초적인 추정을 위한 기초를 설정하는 데 도움이 됩니다.

| **필드** | **관련성, 목적 및 지침** | **다운스트림 영향** |
| --- | --- | --- |
| Name | 예상되는 견적의 개별 구성 요소를 식별하는 데 도움이 되는 견적 라인의 이름입니다. | 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 청구 방법 | 영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 해당 필드에서 복사됩니다. 이 필드에는 Dynamics 365 Project Operations에서 지원하는 두 가지 주요 계약 모델이 포함됩니다.</br>- 고정 가격</br>- 시간 및 재료.| 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| Project | 이 옵션 필드를 사용하여이 계약에 대한 작업을 제공하는 데 사용할 프로젝트를 식별합니다. 프로젝트가 견적 라인에 매핑되면 청구 가능한 작업을 설정하고 견적 라인 세부 정보로 견적 라인에 프로젝트 기반 견적을 가져오는 데 도움이 됩니다. 프로젝트가 프로젝트 기반 견적 라인에 매핑되지 않은 경우 각 견적 라인 세부 정보를 생성하여 견적을 수동으로 생성해야 합니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다.|
| 포함된 작업 | 이 견적 라인이 선택한 프로젝트의 프로젝트 작업 전체 또는 일부에 사용되는지 여부를 나타냅니다. 이 필드에는 다음 가능한 값이 있습니다.</br>- 모든 프로젝트 작업</br>- 선택한 프로젝트 작업만</br>이 필드의 공백 값은 **모든 프로젝트 작업** 옵션과 동일합니다. | 프로젝트 페이지에서 **선택한 프로젝트 작업만**이 선택되면 **작업 청구 설정** 탭을 사용하여 특정 작업을 선택하여 이 견적 라인에 연결할 수 있습니다. 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 시간 포함 | **예**/**아니요** 플래그는 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다. **아니요** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다. **예** 값은 시간 트랜잭션 또는 인건비가 이 견적 라인의 추정에 포함됨을 나타냅니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 경비 포함 | **예**/**아니요** 플래그는 선택한 프로젝트의 경비 비용이 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다. **아니요** 값은 경비 비용이 이 견적 라인의 추정에 포함되는 않음을 나타냅니다. **예** 값은 경비 비용이 이 견적 라인의 추정에 포함됨을 나타냅니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 요금 포함 | **예**/**아니요** 플래그는 선택한 프로젝트의 수수료가 이 견적 라인의 추정에 포함되는지 여부를 나타냅니다. **아니요** 값은 수수료가 이 견적 라인의 추정에 포함되는 않음을 나타냅니다. **예** 값은 수수료가 이 견적 라인의 추정에 포함됨을 나타냅니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 견적 금액 | 이 프로젝트 기반 견적 라인에서 예측된 모든 작업에 대해 고객에게 견적될 금액입니다. 영업 기회에서 견적이 생성되면 이 값은 영업 기회 라인의 **고객 예산** 필드에서 복사됩니다. 프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 금액에서 요약됩니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 예상 세금 | 사용자가 견적 라인에 예상 세액을 추가할 수 있는 편집 가능한 필드입니다. 프로젝트 기반 견적 라인에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 견적 라인 상세 내역의 세액에서 요약됩니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 세금 공제 후 견적 금액 | 이 필드는 세금 공제 후 견적 라인 금액이며 읽기 전용입니다. 이 필드의 금액은 *견적 금액 + 세금*으로 계산됩니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 초과 안 함 한도 | 이 필드는 편집 가능하며 **시간 및 재료** 청구 방법이 있는 프로젝트 기반 견적 라인에서만 사용할 수 있습니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |
| 고객 예산 | 이 필드는 편집 가능하며 영업 기회에서 견적이 생성된 경우 영업 기회 라인의 해당 필드에서 복사됩니다. | 이 필드 값은 견적이 성공하면 이 견적 라인에서 생성된 프로젝트 계약 내용에 복사됩니다. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>프로젝트 기반 견적 라인의 일반 탭에 있는 필드에 대한 유효성 검사 규칙

**규칙 1**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업**으로 설정된 경우 프로젝트가 견적 라인에 포함됩니다.

**규칙 2**: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업**으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 프로젝트 기반 견적 라인 하나에만 포함될 수 있습니다.

**규칙 3**: **포함된 작업** 필드가 **선택한 프로젝트 작업만**으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 견적의 여러 프로젝트 기반 견적 라인에 포함될 수 있습니다.

**규칙 4**: 영업 기회에 여러 견적이 있는 경우 모두 동일한 프로젝트를 참조하고 동일한 트랜잭션 클래스를 포함하는 서로 다른 견적의 견적 라인이 있을 수 있습니다.

**규칙 5**: 견적이 동일한 영업 기회에 속하지 않는 경우 동일한 프로젝트 및 트랜잭션 클래스를 포함할 수 없습니다.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>영업 기회</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>견적</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>견적 라인</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>포함된 작업</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>시간 포함</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>경비 포함</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>포함</strong>
                </p>
                <p>
                    <strong>금액</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>유효/유효하지 않음</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>원인</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
규칙 #2의 위반. P1 프로젝트의 시간, 경비 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
규칙 #2의 위반. P1 프로젝트의 시간 및 요금은 견적 라인 QL1 및 QL2에 포함됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
유효 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1 프로젝트의 시간 및 요금은 QL1에 포함됩니다.
P1 프로젝트의 경비는 QL2에 포함됩니다.
각 견적 라인에 포함되는 내용이 겹치지 않으며 유효합니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
없음 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
위 규칙 #2의 위반. </p>
                <p>
Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.
                </p>
                <p>
QL2에는 전체 프로젝트 P1에 대한 시간, 경비 및 요금이 포함되며 Q1에 포함된 내용과 중복됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
비어 있음 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
유효 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
위 규칙 #3에 따라 </p>
                <p>
Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.
                </p>
                <p>
Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비 및 요금이 포함됩니다.
                </p>
                <p>
유일한 추가 유효성 검사는 QL2의 작업 하위 집합과 다른 QL1의 작업 하위 집합에 대한 것입니다. 이렇게 하면 겹치는 부분이 없습니다. 이것은 작업이 연관될 때 시스템에 의해 수행됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
모든 프로젝트 작업 또는 공백 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" valign="top">
                <p>
유효 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
규칙 #5에 따라 Q1 및 Q2는 동일한 영업 기회에 대한 두 개의 견적이므로 둘 다 프로젝트의 동일한 구성 요소를 추정할 수 있습니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
2분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
모든 프로젝트 작업 또는 공백 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
모든 프로젝트 작업 또는 공백 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" valign="top">
                <p>
유효 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
규칙 #4에 따라 Q1 및 Q2는 다른 영업 기회에 대한 두 개의 견적이므로 같은 프로젝트의 동일한 구성 요소를 추정할 수 없습니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
1분기 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
모든 프로젝트 작업 또는 공백 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="48" valign="top">
                <p>
예 </p>
            </td>
            <td width="42" valign="top">
                <p>
예 </p>
            </td>
            <td width="54" valign="top">
                <p>
유효하지 않음 </p>
            </td>
        </tr>
    </tbody>
</table>

