---
title: 견적 송장 확인 - 라이트
description: 이 항목은 Project Operations에서 견적 송장 확인에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176529"
---
# <a name="confirm-a-proforma-invoice---lite"></a>견적 송장 확인 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_


견적 송장이 확인되면 프로젝트 송장의 상태가 **확인됨** 으로 업데이트됩니다. 송장이 확인되면 읽기 전용이 됩니다. 앞으로 송장이 지불된 것으로 표시된 경우 고객이 시작한 수정 또는 크레딧이 있는 경우에만 송장을 수정할 수 있습니다.

다음 표는 시스템에서 작성된 실제 값을 나열합니다. 이러한 실제는 확정되기 전에 프로젝트 송장 초안에 대해 특정 작업이 수행될 때 생성됩니다.

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
선불 또는 보유자 송장 발행 </p>
            </td>
            <td width="408" valign="top">
                <p>
청구된 실제 판매 유형인 <strong>보유자</strong>는 선불 또는 보유자의 금액에 대해 생성됩니다.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
조정에 사용할 보유자 또는 선불의 음수 금액의 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
송장의 보유자 또는 선불을 완전히 조정한 후.
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
이 송장의 금액에 대한 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
송장의 보유자 또는 선불을 부분 조정한 후.
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
이 송장의 금액에 대한 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
향후 송장의 조정에 사용할 나머지 보유자 또는 선불 금액의 음수 청구되지 않은 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
초안 송장을 편집하지 않고 시간 트랜잭션을 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
최초 시간 승인의 시간 및 금액에 대해 청구된 실제 판매
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
수량을 줄이기 위해 편집된 시간 트랜잭션 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 시간 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
수량을 늘리기 위해 편집된 시간 트랜잭션 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 시간 승인의 시간 및 금액에 대한 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
초안 송장을 편집하지 않고 경비 트랜잭션을 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
최초 경비 승인의 수량 및 금액에 대해 청구된 실제 판매 </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
수량을 줄이기 위해 편집된 경비 트랜잭션 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 수량 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
수량을 늘리기 위해 편집된 경비 트랜잭션 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 경비 승인의 수량 및 금액에 대해 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수량 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
수수료 청구.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
최초 분개장 항목의 수수료 금액에 대한 청구되지 않은 매출액 전환.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
최초 수수료 분개장 항목의 수량 및 금액에 대해 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
중요 시점 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
프로젝트 계약 내용의 원래 중요 시점에 있는 중요 시점 금액에 대해 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
제품 기반 계약 내용 송장 발행.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
제품 기반 계약 내용에서 나오는 수량 및 금액으로 제품 라인에 대해 청구된 실제 판매.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]