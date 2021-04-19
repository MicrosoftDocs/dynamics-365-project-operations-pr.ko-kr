---
title: 수정 프로젝트 기반 송장
description: 이 항목은 Project Operations에서 수정 프로젝트 기반 송장을 만들고 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867049"
---
# <a name="corrective-project-based-invoices"></a>수정 프로젝트 기반 송장

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

확인된 프로젝트 송장을 수정하여 고객 및 프로젝트 관리자와 협상한 대로 변경 또는 대변을 처리할 수 있습니다.

확인된 송장을 편집하려면 확인된 송장을 열고 **이 송장 수정** 을 선택합니다. 

> [!NOTE]
> 이 선택 사항은 프로젝트 송장이 확인되거나 프로젝트 기반 송장에 선금 또는 보유자 또는 대출 또는 보유자의 조정이 있는 경우에만 사용할 수 있습니다.

확인된 송장에서 새 송장 초안이 생성됩니다. 이전에 확인된 송장의 모든 송장 라인 상세 내역이 신규 초안에 복사됩니다. 다음은 새로 수정된 송장의 라인 세부 정보에 대해 이해해야 할 몇 가지 핵심 사항입니다.

- 모든 수량이 0으로 업데이트됩니다. Dynamics 365 Project Operations에서는 모든 송장 항목이 완전히 입금되었다고 가정합니다. 필요한 경우 차감되는 수량이 아니라 송장이 발행되는 수량을 반영하도록 이러한 수량을 수동으로 업데이트할 수 있습니다. 입력한 수량에 따라 응용 프로그램이 대변 수량을 계산합니다. 이 금액은 수정된 송장이 확인될 때 생성된 실제 금액에 반영됩니다. 세액을 변경하는 경우 공제되는 세액이 아니라 정확한 세액을 입력해야 합니다.
- 중요 시점 수정은 항상 전체 크레딧으로 처리됩니다.


> [!IMPORTANT]
> 이미 송장이 발행된 다른 경비에 대한 수정인 송장 라인 상세 내역에는 **수정** 필드가 **예** 로 설정되어 있습니다. 송장 라인 세부 정보가 수정된 송장의 경우 **수정 사항 있음** 필드가 **예** 로 설정됩니다.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>수정 송장 확인시 생성된 실제

다음 표에는 수정 송장이 확인될 때 생성되는 실제 항목이 나열되어 있습니다.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>시나리오</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>확정시 생성된 실제</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
이전에 청구된 시간 트랜잭션의 전체 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
시간에 대한 최초 송장 라인 상세 내역의 시간 및 금액에 대한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
시간 트랜잭션에 대한 부분 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
시간에 대한 최초 송장 라인 상세 내역의 시간 및 송장 발행된 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
이전에 청구된 경비 트랜잭션의 전체 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
경비에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
이전에 청구된 경비 트랜잭션의 부분 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
경비에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
수정된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
이전에 송장을 발행한 재료 트랜잭션의 전체 대변 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
재료에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 판매 취소.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
재료에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 실제 신규 미청구 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
재료 트랜잭션에 대한 부분 신용 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
재료에 대한 최초 송장 라인 상세 내역의 송장 발부된 수량 및 금액에 대한 청구된 판매 취소.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 미청구 판매 실제, 이것의 취소 및 이에 상응하는 청구된 판매 실제.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
송장 라인 상세 내역에서 수정된 수치를 차감한 후 남은 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
이전에 청구된 요금 트랜잭션의 전체 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
요금에 대한 최초 송장 라인 상세 내역의 수량 및 금액에 대한 신규 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
이전에 청구된 요금 트랜잭션의 부분 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
요금에 대한 최초 송장 라인 상세 내역의 수량 및 송장 발행된 금액에 대한 청구된 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 수정 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 이것의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
이전에 청구된 중요 시점의 전체 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
중요 시점에 대한 최초 송장 라인 상세 내역의 금액에 대한 청구된 매출액 전환.
                </p>
                <p>
이정표의 송장 상태는 <b>고객 송장 게시됨</b>에서 <b>송장 발부 준비 완료</b>로 업데이트됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
이전에 청구된 중요 시점의 부분 크레딧 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
이 시나리오는 지원되지 않습니다.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
