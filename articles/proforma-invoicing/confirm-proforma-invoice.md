---
title: 견적 송장 확인
description: 이 항목에서는 견적 송장 확인에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079897"
---
# <a name="confirm-a-proforma-invoice"></a>견적 송장 확인

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

견적 송장이 확인되면 프로젝트 송장의 상태가 **확인됨** 으로 업데이트됩니다. 송장이 확인되면 읽기 전용이 됩니다. 앞으로 송장이 지불된 것으로 표시된 경우 고객이 시작한 수정 또는 크레딧이 있는 경우에만 송장을 수정할 수 있습니다.

다음 표는 시스템에서 작성된 실제 값을 나열합니다. 이러한 실제는 확정되기 전에 프로젝트 송장 초안에 대해 특정 작업이 수행될 때 생성됩니다.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>시나리오</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>확정시 생성된 실제</strong>
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
편집된 송장 라인 상세 내역의 시간 및 금액에 대해 청구 가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
편집된 송장 라인 상세 내역의 수정된 수치를 공제한 후 남은 시간 및 금액에 대해 청구 불가능한 신규 청구되지 않은 실제 판매, 청구되지 않은 실제 판매의 매출액 전환 및 이에 상응하는 청구된 실제 판매.
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
최초 경비 승인의 수량 및 금액에 대해 청구된 실제 판매.
                </p>
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
    </tbody>
</table>