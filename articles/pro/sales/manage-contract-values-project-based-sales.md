---
title: 프로젝트 기반 계약 내용 개요
description: 이 항목은 프로젝트 기반 계약 내용 작업에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999054"
---
# <a name="project-based-contract-lines-overview"></a>프로젝트 기반 계약 내용 개요

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations의 프로젝트 기반 계약 내용은 계약에 대한 프로젝트 작업의 특정 구성 요소에 대한 추정 및 청구 계약을 유지하도록 설계되었습니다. 프로젝트 기반 계약 내용의 구조는 다음 개념으로 프로젝트 추정 및 청구 시나리오에 대해 확장됩니다.

- 청구 방법
- 프로젝트 및 작업 매핑
- 포함된 트랜잭션 클래스
- 초과 안 함 한도
- 청구 가능성 설정
- 계약 내용 세부 정보를 사용하여 추정
- 계약 내용 고객

다음 표에는 프로젝트 기반 작업에 대한 세부적이고 기초적인 추정 및 청구 약정에 대한 기반을 설정하는 데 도움이 되는 프로젝트 기반 계약 내용의 **일반** 탭에 있는 필드가 포함되어 있습니다.

| 필드 | 설명 | 다운스트림 영향 |
| --- | --- | --- |
| **이름** | 계약 내용의 이름입니다. 이는 추정되는 계약의 개별 구성 요소를 식별합니다. 견적에서 생성된 프로젝트 계약의 경우 이 값은 프로젝트 기반 견적 라인의 해당 값에서 복사됩니다. | 송장이 생성될 때 이 계약 내용에서 생성된 프로젝트 송장 라인에 복사된 이름입니다. |
| **청구 방법** | 견적에서 생성된 프로젝트 계약에서는 이 값은 견적 라인의 해당 값에서 복사됩니다. 이것은 Project Operations에서 지원하는 두 가지 주요 계약 모델을 나타내는 옵션 집합입니다.</br>- **고정 가격**</br>- **시간 및 재료** | 참조된 계약 내용의 청구 방법에 따라 실제 트랜잭션이 처리됩니다. 실제가 참조하는 계약 내용에 시간 및 재료 청구 방법이 있는 경우 비용 및 미청구 판매 실제 레코드가 생성됩니다. 실제가 참조하는 계약 내용에 고정 가격 청구 방법이 있는 경우 실제 비용만 생성됩니다. |
| **Project** | 이 참여에 대한 작업을 제공하는 데 사용될 프로젝트를 식별하려면 이 필드를 사용합니다. | 이 값은 **포함된 작업** 및 **포함된 트랜잭션 클래스** 와 함께 사용되어 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결합니다. |
| **포함된 작업** | 이 계약 내용에 선택한 프로젝트에 대한 모든 프로젝트 작업이 포함되는지 아니면 작업의 하위 집합만 포함되는지 여부를 나타냅니다. 이는 다음과 같은 가능한 값이 있는 옵션 집합입니다.</br>- **모든 프로젝트 작업**</br>- **선택한 프로젝트 작업만**. 이 필드의 빈 값은 **모든 프로젝트 작업** 을 선택하는 것과 같습니다. | **선택한 작업만** 을 선택하면 **프로젝트** 페이지의 **작업 청구 설정** 탭에서 특정 작업을 선택하여 이 계약 라인에 연결할 수 있습니다. 이 값은 **프로젝트** 및 **포함된 트랜잭션** 분류와 함께 사용되어 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결합니다. |
| **시간 포함** | **예**/**아니요** 값은 선택한 프로젝트의 시간 트랜잭션 또는 인건비가 이 계약 내용에 포함되는지 여부를 나타냅니다. **아니요** 값은 시간 트랜잭션 또는 인건비가 이 계약 내용에 포함되지 않음을 나타냅니다. **예** 값은 포함됨을 나타냅니다. | 이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다. |
| **경비 포함** | **예**/**아니요** 값은 선택한 프로젝트의 경비가 이 계약 내용에 포함되는지 여부를 나타냅니다. **아니요** 값은 경비가 이 계약 내용에 포함되지 않음을 나타냅니다. **예** 값은 포함됨을 나타냅니다. | 이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다. |
| **재료 포함** | **예**/**아니요** 값은 선택한 프로젝트의 재료 비용이 계약 내용에 포함되는지 여부를 나타냅니다. **아니요** 값은 재료 비용이 이 계약 내용의 견적에 포함되지 않음을 나타냅니다. **예** 값은 포함됨을 나타냅니다. | 이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다. |
| **요금 포함** | **예**/**아니요** 값은 선택한 프로젝트의 요금이 이 계약 내용에 포함되는지 여부를 나타냅니다. **아니요** 값은 요금이 이 계약 내용에 포함되지 않음을 나타냅니다. **예** 값은 포함됨을 나타냅니다. | 이 값은 실제 또는 추정 라인 레코드에서 계약 내용 참조를 해결하기 위해 프로젝트와 함께 사용됩니다. |
| **계약 금액** | 고정 가격 계약 내용에서 이 금액은 이 계약 내용과 연관된 모든 작업 구성 요소에 대해 고객에게 송장을 발행할 합의된 값입니다. 시간 및 재료 계약 내용에서 이 금액은 이 계약 내용과 연관된 모든 작업 구성 요소에 대해 고객에게 송장을 발행할 추정된 값입니다. 견적에서 생성된 프로젝트 계약에서는 이 값은 견적 라인의 해당 값에서 복사됩니다. 프로젝트 기반 계약 내용에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 계약 내용 상세 내역의 금액에서 요약됩니다. | 계약 내용에 라인 상세 내역이 있는 경우 라인 상세 내역의 금액을 변경하여 이 값을 수정할 수 있습니다. 고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점에 대한 세전 금액을 생성하는 데 사용됩니다. |
| **예상 세금** | 사용자는 이 필드를 편집하여 계약 내용에 예상 세액을 입력할 수 있습니다. 프로젝트 기반 계약 내용에 라인 상세 내역이 있는 경우 이 필드는 편집을 위해 잠기고 계약 내용 상세 내역의 세액에서 요약됩니다. | 계약 내용에 라인 상세 내역이 있는 경우 라인 상세 내역의 세액을 변경하여 이 값을 수정할 수 있습니다. 고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점에 대한 세금을 생성하는 데 사용됩니다. |
| **세금 공제 후 계약 금액** | 세금 공제 후 내용 계약 금액입니다. 이 필드는 읽기 전용이며 **약정 금액 + 세금** 과 같이 계산됩니다. | 고정 가격 계약 내용에서 이 값은 정기 청구 중요 시점을 생성하는 데 사용됩니다. |
| **초과 안 함 한도** | 사용자는 이 필드를 편집할 수 있으며 청구 방법이 시간 및 재료로 설정된 프로젝트 기반 계약 내용에서만 사용할 수 있습니다. | 사용자는 이 필드를 편집할 수 있습니다. 시간 및 재료에 대한 실제가 시간 및 재료에 대해 이 계약 내용을 참조하는 경우 실제 금액은 계약 내용의 초과 안 함 한도에 대해 평가됩니다. 이 평가는 이미 소비되고 약정된 금액이 계산된 후에 완료됩니다. |
| **고객 예산** | 이 필드는 편집 가능하며 견적에서 계약이 생성된 경우 견적 라인의 해당 필드에서 복사됩니다. | 이 필드는 정보용으로만 사용되며 다운 스트림 중요도가 없습니다. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>프로젝트 기반 계약 내용의 일반 탭에 있는 옵션에 대한 검증 규칙

규칙 1: **포함된 작업** 필드가 비어 있거나 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트의 모든 작업이 계약 내용에 포함됩니다.

규칙 2: **포함된 작업** 필드가 비어 있거나 명시적으로 **모든 프로젝트 작업** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 계약의 하나의 프로젝트 기반 계약 내용에만 포함될 수 있습니다.

규칙 3: **포함된 작업** 필드가 **선택한 프로젝트 작업만** 으로 설정된 경우 프로젝트 및 특정 트랜잭션 클래스는 계약의 여러 프로젝트 기반 계약 내용에 포함될 수 있습니다.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>계약</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>계약 내용</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>재료 포함</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>유효/유효하지 않음</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>원인</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
규칙 #2의 위반. P1 프로젝트의 시간, 경비, 재료 및 요금은 견적 라인 CL1 및 QL2 모두에 포함됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
규칙 #2의 위반. P1 프로젝트의 시간, 재료 및 요금은 견적 라인 CL1 및 QL2 모두에 포함됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
유효함 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 프로젝트의 시간, 재료 및 요금은 QL1에 포함됩니다.
                </p>
                <ul>
                    <li>
P1 프로젝트의 경비는 CL2에 포함됩니다.
                    </li>
                </ul>
                <p>
각 계약 내용에 포함되는 내용이 중복되지 않으므로 유효합니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
없음 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
없음 </p>
            </td>
            <td width="42" valign="top">
                <p>
없음 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
유효하지 않음 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
규칙 #2의 위반 </p>
                <p>
Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 재료, 경비 및 요금이 포함됩니다.
                </p>
                <p>
CL2에는 전체 프로젝트 P1에 대한 시간, 재료, 경비 및 요금이 포함되므로 C1에 포함된 내용과 겹칩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
빈 템플릿 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
유효함 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
규칙 3번에 따라 </p>
                <p>
Q1에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비, 재료 및 요금이 포함됩니다.
                </p>
                <p>
Q2에는 프로젝트 P1의 작업 하위 집합에 대한 시간, 경비, 재료 및 요금이 포함됩니다.
                </p>
                <p>
유일한 추가 유효성 검사는 QL2의 작업 하위 집합과 다른 CL1 작업의 하위 집합을 중심으로 중복이 없는지 확인하는 것입니다. 이것은 작업이 연관될 때 시스템에 의해 수행됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="48" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
            <td width="42" valign="top">
                <p>
네 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
