---
title: 크레딧 및 수정된 송장
description: 이 항목은 Project Operations에서 수정된 송장에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080163"
---
# <a name="credits-and-corrected-invoices"></a>크레딧 및 수정된 송장

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

확인된 프로젝트 송장을 수정하여 고객 및 프로젝트 관리자와 협상한 대로 변경 또는 대변을 처리할 수 있습니다.

확인된 송장을 편집하려면 확인된 송장을 열고 **이 송장 수정** 을 선택합니다. 

> [!NOTE]
> 이 선택은 프로젝트 송장이 확인되지 않으면 사용할 수 없습니다.

확인된 송장에서 새 송장 초안이 생성됩니다. 이전에 확인된 송장의 모든 송장 라인 상세 내역이 신규 초안에 복사됩니다. 다음은 새로 수정된 송장의 라인 세부 정보에 대해 이해해야 할 몇 가지 핵심 사항입니다.

- 모든 수량이 0으로 업데이트됩니다. 응용 프로그램은 모든 송장 항목이 완전히 입금되었다고 가정합니다. 필요한 경우 차감되는 수량이 아니라 송장이 발행되는 수량을 반영하도록 이러한 수량을 수동으로 업데이트할 수 있습니다. 입력한 수량에 따라 응용 프로그램이 대변 수량을 계산합니다. 이 금액은 수정된 송장이 확인될 때 생성된 실제 금액에 반영됩니다. 세액을 변경하는 경우 공제되는 세액이 아니라 정확한 세액을 입력해야 합니다.
- 이전에 확인된 제품 기반 계약 내용은 복사되지 않습니다. 제품 기반 프로젝트 송장에 대한 수정 처리는 지원되지 않습니다.
- 중요 시점 수정은 항상 전체 크레딧으로 처리됩니다.
- 고객에게 잘못된 금액이 청구된 경우 보유자 또는 선급 금액을 수정할 수 있습니다.
- 이전에 확인된 송장의 요금을 조정하는 데 잘못된 금액이 사용된 경우 보유자 및 선불의 조정을 수정할 수 있습니다.

> [!IMPORTANT]
> 이미 송장이 발행된 다른 비용에 대한 수정인 송장 라인 상세 내역에는 **수정** 필드가 **예** 로 설정되어 있습니다. 송장 라인 상세 내역이 수정된 송장에는 **수정 사항 있음** 필드도 **예** 로 설정되어 있습니다.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>수정 송장 확인시 생성된 실제:

다음은 확인 전에 초안 수정 송장에 대해 수행된 작업을 기반으로 수정 확인시 응용 프로그램에서 생성한 실제 값입니다.

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
            <td width="216" rowspan="4" valign="top">
                <p>
송장 선불 또는 보유자의 수정을 확인합니다.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환. 이 금액은 보유자 또는 선불이 청구될 때 생성된 음수를 취소하기 위한 것이므로 양수입니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
원래 청구된 판매를 취소하기 위해 보유자의 금액에 대해 청구된 판매 취소 실제 값이 생성됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
보유자 또는 선불 기반 수정 송장 라인의 수정된 금액에 대해 신규 청구된 판매 실제 값이 생성됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
조정에 사용되는 보유자 또는 선불 기반 수정된 송장 라인의 음수 금액의 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
이전에 조정된 보유자 또는 선불의 수정 확인.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
조정을 위해 생성된 보유자 또는 선불의 청구되지 않은 매출액 전환. 이 금액은 양수이며 이전 조정이 발생했을 때 생성된 음수를 취소하기 위한 것입니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
이전 송장의 금액에 대한 실제 청구된 판매 취소.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
수정된 송장에 적용되는 수정된 보유자 금액에 대한 신규 청구된 판매 실제 값.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
수정된 잔여 보유자 또는 선불에서 음수 금액이 있고 이후 송장의 조정에 사용되는 미청구된 판매 실제 값.
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
프로젝트 계약 내용의 중요 시점 송장 또는 청구 상태가 **송장 준비** 로 업데이트됩니다.
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
지원되지 않음 </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
이전에 송장을 발행한 제품 기반 계약 내용의 크레딧 및 수정.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
지원되지 않음 </p>
            </td>
        </tr>
    </tbody>
</table>