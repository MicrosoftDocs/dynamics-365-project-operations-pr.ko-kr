---
title: 견적 라인의 청구 가능 구성 요소 구성
description: 이 항목은 프로젝트 기반 견적 라인에서 청구 가능 및 청구 불가능 구성 요소 설정에 대한 정보를 제공합니다.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598404"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>견적 라인의 청구 가능 구성 요소 구성 

_**적용 대상:** 라이트 배포 - 견적 송장 처리, 리소스/비 재고 기반 시나리오를 위한 Project Operations_

프로젝트 기반 견적 라인에는 *포함* 구성 요소 및 *청구 가능* 구성 요소의 개념이 있습니다.

포함된 구성 요소는 다음 항목에 적용됩니다.

  - 청구 방법 및 고객 분할
  - 초과 안 함 한도 
  - 프로젝트 기반 견적 라인에 정의된 송장 빈도 설정

포함 구성 요소의 하위 집합은 **청구 유형** 필드를 사용하여 청구 가능으로 표시할 수 있습니다. **청구 유형** 필드는 견적 라인의 컨텍스트에서 다음 값을 허용하는 옵션 집합입니다.

  - 청구 가능
  - 청구 불가능

청구 가능 구성 요소는 작업, 역할 및 트랜잭션 범주에 정의할 수 있습니다.

청구 가능성은 견적 라인의 작업에 정의되며 해당 라인에 포함된 모든 트랜잭션 클래스에 적용됩니다. **작업 포함** 필드가 **전체 프로젝트** 로 설정되거나 비어 있는 경우 **청구 가능 작업** 탭을 사용할 수 없습니다.

청구 가능성은 견적 라인의 역할에 정의되며 **시간** 트랜잭션 클래스에만 적용됩니다. 프로젝트 견적 라인에서 **시간 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 역할** 탭을 사용할 수 없습니다.

청구 가능성은 견적 라인의 트랜잭션 범주에 정의되며 **경비** 트랜잭션 클래스에만 적용됩니다. 프로젝트 견적 라인에서 **경비 포함** 필드가 **아니요** 로 설정된 경우 **청구 가능 범주** 탭을 사용할 수 없습니다.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>프로젝트 작업을 청구 가능 또는 청구 불가능으로 업데이트

특정 프로젝트 기반 연적 라인의 컨텍스트에서 프로젝트 작업은 청구 가능하거나 청구 불가능할 수 있으므로 다음 설정이 가능합니다.

프로젝트 기반 견적 라인에 **시간** 및 작업 **T1** 이 포함된 경우 작업은 청구 가능으로 견적 라인에 연관됩니다. **경비** 를 포함하는 두 번째 견적 라인이 있는 경우, 견적 라인의 **T1** 작업을 청구 불가능으로 연관시킬 수 있습니다. 결과적으로 작업에 기록된 모든 시간은 청구 가능하며 작업에 기록된 모든 경비는 청구 불가능합니다.

작업의 청구 유형은 **견적 라인 작업** 하위 표에서 **청구 유형** 필드를 업데이트하여 프로젝트 기반 견적 라인의 **청구 가능한 작업** 탭에서 구성할 수 있습니다. 또는 작업과 연결된 견적 라인을 표시하는 프로젝트의 작업 청구 설정에 있는 하위 표의 **청구 유형** 필드에서 프로젝트 작업에 대한 청구 유형을 업데이트 할 수 있습니다.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>역할을 청구 가능 또는 청구 불가능으로 업데이트

특정 프로젝트 기반 견적 라인의 컨텍스트에서 역할은 청구 가능하거나 청구 불가능할 수 있습니다.

역할의 청구 유형은 **청구 가능 역할** 하위 표에서 **청구 유형** 필드를 업데이트하여 견적 라인의 **청구 가능한 역할** 탭에서 구성할 수 있습니다.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>트랜잭션 범주를 청구 가능 또는 청구 불가능으로 업데이트

트랜잭션 범주는 특정 견적 라인에서 청구 가능하거나 청구 불가능할 수 있습니다.

트랜잭션의 청구 유형은 **청구 가능 범주** 하위 표에서 **청구 유형** 필드를 업데이트하여 견적 라인의 **청구 가능한 범주** 탭에서 구성할 수 있습니다.

### <a name="resolve-chargeability"></a>청구 가능성 해결
시간에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.

   - **시간** 은 견적 라인에 포함됩니다.
   - **역할** 은 견적 라인에서 청구 가능으로 구성됩니다.
   - **포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다. 

이 세 가지 사항이 참이면 **작업** 도 청구 가능으로 구성됩니다. 

경비에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다. 

   - **경비** 는 견적 라인에 포함됩니다.
   - **트랜잭션 범주** 는 견적 라인에서 청구 가능으로 구성됩니다.
   - **포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다.

이 세 가지 사항이 참이면 **작업** 도 청구 가능으로 구성됩니다. 

재료에 대해 생성된 추정 또는 실제는 다음 경우에만 청구 가능한 것으로 간주됩니다.

   - **재료** 는 견적 라인에 포함됩니다.
   - **포함된 작업** 은 견적 라인에서 **선택한 작업** 으로 설정됩니다.

이 두 가지 사항이 참이면 **작업** 도 청구 가능으로 구성해야 합니다. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>시간 포함</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>경비 포함</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>재료 포함</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>포함된 작업</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>역할</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>카테고리</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>작업</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>청구 가능성 영향</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: 청구 가능 </p>
                <p>
실제 경비 청구 유형: 청구 가능 </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: 청구 가능 </p>
                <p>
실제 경비 청구 유형: 청구 가능 </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: 청구 가능 </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>청구 불가능</strong>
                </p>
                <p>
실제 재료 청구 유형: <strong>청구 불가능</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>청구 불가능</strong>
                </p>
                <p>
실제 재료 청구 유형: <strong>청구 불가능</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
선택한 작업만 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>청구 불가능</strong>
                </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>청구 가능</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>사용할 수 없음</strong>
                </p>
                <p>
실제 경비 청구 유형: 청구 가능 </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>사용할 수 없음</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>청구 불가능</strong>
                </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="70" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: 청구 가능 </p>
                <p>
실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
네 </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>사용할 수 없음</strong>
                </p>
                <p>
실제 재료 청구 유형: 청구 가능 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="70" valign="top">
                <p>
청구 가능 </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: 청구 가능 </p>
                <p>
실제 경비 청구 유형: 청구 가능 </p>
                <p>
실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
네 </p>
            </td>
            <td width="78" valign="top">
                <p>
네 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>없음</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
전체 프로젝트 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>청구 불가능</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
설정할 수 없음 </p>
            </td>
            <td width="350" valign="top">
                <p>
실제 시간 청구: <strong>청구 불가능</strong>
                </p>
                <p>
실제 경비 청구 유형: <strong>청구 불가능</strong>
                </p>
                <p>
실제 재료 청구 유형: <strong>사용할 수 없음</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
