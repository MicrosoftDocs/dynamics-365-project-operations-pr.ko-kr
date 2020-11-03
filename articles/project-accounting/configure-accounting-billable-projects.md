---
title: 청구 가능한 프로젝트에 대한 회계 구성
description: 이 항목은 청구 가능한 프로젝트의 회계 옵션에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 32031742b1a9580b9ebdbaf6952a998733be5e8f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079966"
---
# <a name="configure-accounting-for-billable-projects"></a>청구 가능한 프로젝트에 대한 회계 구성

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations는 시간 및 자재 및 고정 가격 거래를 포함하는 청구 가능한 프로젝트에 대한 다양한 회계 옵션을 지원합니다.

- **시간 및 자재 트랜잭션** : 이러한 트랜잭션은 프로젝트에 대한 시간, 비용, 항목 또는 수수료의 소비에 따라 작업이 진행됨에 따라 송장이 발행됩니다. 이러한 트랜잭션 비용은 각 트랜잭션의 수익과 일치시킬 수 있으며 작업이 진행됨에 따라 프로젝트에 송장이 발행됩니다. 프로젝트 수익은 트랜잭션이 발생하는 시점에 발생할 수도 있습니다. 송장을 발행하는 동안 수익이 인식되고 해당되는 경우 미지급 수익이 취소됩니다.
- **고정 가격 트랜잭션** : 이러한 트랜잭션은 프로젝트 계약을 기반으로 하는 청구 일정에 따라 청구됩니다. 고정 가격 트랜잭션에 대한 수익은 **완료된 계약** 또는 **완료율** 방법에 따라 송장 발행시 인식되거나 정기적으로 계산 및 전기될 수 있습니다.

프로젝트는 하나 이상의 계약 내용과 연관될 때 청구 가능한 것으로 간주됩니다. 프로젝트 계약 내용은 허용되는 청구 방법 및 트랜잭션 유형을 자체적으로 정의합니다.

예를 들어 Fabrikam Robotics는 장비 최적화를 위해 Adatum Corporation과 프로젝트 계약을 체결했습니다. Adatum은 발생한 프로젝트 비용을 충당하기 위해 고정 금액 $10.000 USD를 지불합니다. 이는 고정 가격 청구 방법입니다. 프로젝트 시간 및 수수료는 사용당 청구됩니다. 이는 시간 및 자재 청구 방법입니다. 모든 작업은 Adatum 장비 최적화라는 단일 프로젝트에서 추적됩니다.

프로젝트 팀원이 Adatum 장비 최적화 프로젝트에 대해 8시간의 작업을 제출합니다. 프로젝트 관리자가 이 시간을 승인하면 시스템은 시간 및 자재 청구 방법을 사용하여 실제 거래, 송장 및 계정을 생성합니다. 이 트랜잭션은 고정 가격 수익 추정 계산에 포함되지 않습니다.

다른 프로젝트 팀원이 Adatum 장비 최적화 프로젝트에 대해 $2000.00 USD의 출장비를 제출합니다. 프로젝트 관리자가 이 제출을 승인하면 시스템은 고정 가격 청구 방법을 사용하여 실제 트랜잭션과 이 프로젝트 비용에 대한 계정을 생성합니다. 이 트랜잭션을 기반으로 고객에게 송장이 발행되지 않습니다. 대신 별도로 구성된 청구 중요 시점을 사용하여 청구됩니다. 이 경비 트랜잭션은 경비 추정치와 함께 고정 고정 가격 수익 추정 계산에 포함되지 않습니다.

프로젝트 트랜잭션에 대한 회계 원칙은 프로젝트 비용 및 수익 프로필에서 정의됩니다. 모든 프로젝트 트랜잭션에 대해 시스템은 구성된 프로젝트 비용 및 수익 프로필 규칙을 사용하여 적절한 프로젝트 비용 및 수익 프로필을 결정합니다.

## <a name="define-project-cost-and-revenue-profiles"></a>프로젝트 비용 및 수익 프로필 정의 

프로젝트 비용 및 수익 프로필은 프로젝트 트랜잭션에 대한 회계 규칙을 결정합니다. 이러한 프로필은 프로젝트 관리 및 회계에서 구성됩니다. 

새 프로젝트 비용 및 수익 프로필을 생성하려면 다음 단계를 완료하십시오. 

1. **프로젝트 관리 및 회계** > **설정** > **전기** > **프로젝트 비용 및 수익 프로필** 로 이동합니다. 
2. **새로 만들기** 를 선택하여 새로운 프로젝트 비용 및 수익 프로필을 생성합니다.
3. **이름** 필드에 프로필의 이름과 간단한 설명을 입력합니다.
4. **청구 방법** 필드에서 **시간 및 자재** 또는 **고정 가격** 을 선택합니다.
5. **원장** 빠른 탭을 확장합니다. 이 탭의 필드는 Project Operations 통합 분개장을 사용하여 프로젝트 트랜잭션을 분개한 다음 프로젝트 송장 제안을 통해 송장을 발행할 때 사용되는 회계 원칙을 정의합니다.
6. **원장** 빠른 탭의 다음 필드에서 적절한 정보를 선택합니다.

    - **비용 전기 – 시간** :

       - *원장 없음* : Project Operations 통합 분개장이 전기될 때 시간 트랜잭션 비용이 원장에 전기되지 않습니다. 그러나 회계사는 나중에 비용 전기 기능을 사용하여 비용을 전기할 수 있습니다.
       - **잔액** : 시간 트랜잭션 비용은 원장 전기 설정에서 원장 계정 유형 *WIP-비용 값* 으로 차변 처리되고 *급여 할당 계정* 으로 대변 처리됩니다. 회계사는 비용 전기 기능을 사용하여 이 비용을 잔액 계정에서 손익 계정으로 주기적으로 이동합니다.
       - **이익과 손실** : Project Operations 통합 분개장을 전기할 때 시간 트랜잭션 비용이 **원장 전기 설정** 페이지의 **비용** 탭( **프로젝트 관리 및 회계** \>**설정** \>**전기** \>**원장 전기 설정** )에 정의된 원장 계정 유형 *비용* 으로 차변 처리되고 *급여 할당 계정* 으로 대변 처리됩니다. 이것은 시간 및 자재 트랜잭션에 대한 가장 일반적인 설정입니다.
        - *원장 없음* : 시간 트랜잭션에 대한 비용은 원장에 전기되지 않습니다.

    - **비용 전기 – 경비** :

         - **잔액** : Project Operations 통합 분개장을 전기할 때 경비 트랜잭션 비용이 **원장 전기 설정** 의 **비용** 탭에 정의된 대로 원장 계정 유형 *WIP - 비용 값* 으로 차변 처리되고 분개장 항목의 상쇄 계정으로 대변 처리됩니다. 경비에 대한 기본 상쇄 계정은 **프로젝트 관리 및 회계** > **설정** \>**전기** \>**경비에 대한 기본 상쇄 계정** 에 정의됩니다. 회계사는 **비용 전기** 기능을 사용하여 이 비용을 잔액 계정에서 손익 계정으로 주기적으로 이동합니다.
        - **이익과 손실** : Project Operations 통합 분개장을 전기할 때 경비 트랜잭션 비용이 **원장 전기 설정** 의 **비용** 탭에 정의된 대로 원장 계정 유형 *비용* 으로 차변 처리되고 분개장 항목의 상쇄 계정으로 대변 처리됩니다. 경비에 대한 기본 상쇄 계정은 **프로젝트 관리 및 회계** \> **설정** \> **전기** \> **경비에 대한 기본 상쇄 계정** 에 정의됩니다.
       
    - **계정 송장 처리 시** :

        - **잔액** : 프로젝트 송장 제안을 전기할 때 거래처 내 트랜잭션(청구 중요 시점)이 **원장 전기 설정** 페이지의 **수익** 탭에 정의된 대로 원장 계정 유형 *WIP 송장 - 계정* 으로 대변 처리되고 고객 잔액 계정으로 차변 처리됩니다.
         - **이익과 손실** : 프로젝트 송장 제안을 전기할 때 계정 내 트랜잭션(청구 중요 시점)이 **원장 전기 설정** 페이지의 **수익** 탭에 정의된 대로 원장 계정 유형 *송장 발부된 수익 - 계정 내* 로 대변 처리되고 고객 잔액 계정으로 차변 처리됩니다. 고객 잔액 계정은 **외상 매출금** \>**설정** \>**고객 전기 프로필** 에 정의됩니다.

   시간 및 자재 청구 방법에 대한 전기 프로필을 정의할 때 트랜잭션 유형(시간, 경비 및 수수료) 당 수익을 발생시키는 옵션이 있습니다. **수익 발생** 옵션이 **예** 로 설정된 경우 Project Operations 통합 분개장의 청구되지 않은 판매 트랜잭션은 총계정 원장에 기록됩니다. 영업 가치는 **WIP - 영업 가치 계정** 으로 차변 처리되고 **수익** 탭의 **원장 전기 설정** 페이지에서 설정된 **미수 수익 - 영업 가치** 로 대변 처리됩니다. 
  
  > [!NOTE]
  > 옵션 **수익 발생** 은 각 트랜잭션 유형 **비용** 이 손익 계정에 전기될 때만 사용할 수 있습니다.
    
7. **추정** 빠른 탭을 확장합니다. 이 탭의 필드는 고정 가격 수익 추정에 대한 계산 설정을 정의합니다. 이 탭의 필드는 청구 방법이 **고정 가격** 인 프로젝트 비용 및 수익 프로필에만 적용됩니다.
8. **추정** 빠른 탭의 다음 필드에서 적절한 정보를 선택합니다.

    - **프로젝트 완료 계산에 사용되는 원칙** :

        - **완료된 계약** : 비용 일치 및 수익 인식은 프로젝트가 끝날 때까지 발생하지 않습니다. 비용은 프로젝트가 완료될 때까지 잔액에 WIP로 반영됩니다.
        - **완료율** : 미수 수익은 프로젝트 완료율을 기준으로 매 기간마다 계산되어 원장에 전기됩니다. 완료율을 계산하는 데 사용할 수 있는 여러 가지 방법이 있습니다. 이러한 방법은 구성에 따라 자동으로 수행되거나 수동으로 수행될 수 있습니다.
        - **WIP 없음** : 이 설정은 기간이 짧고 송장과 비용이 같은 기간에 발생하는 고정 가격 프로젝트에 사용됩니다. 이 경우 **원장** 빠른 탭의 **계정별 인보이스 발행** 필드 값은 송장 발행시 수익이 인식되도록 **이익과 손실** 로 자동 설정됩니다. 이 프로젝트 비용 및 수익 프로필에는 수익 추정 프로세스가 사용되지 않습니다.

    - **일치 원리** : 이 필드는 계산된 판매 값(미수 수익)이 원장에 전기되는 방법을 결정합니다.

        - **영업 가치** 원칙을 사용하여 시스템은 비용과 수익을 일치시킨 다음 단일 금액으로 게시하여 영업 가치를 계산합니다.
        - **생산과 이익** 원칙을 사용하여 시스템은 영업 가치를 실현 비용과 계산된 이익으로 분할합니다. 이들은 별도로 게시됩니다.

    - **비용 템플릿** : 트랜잭션 유형 및 프로젝트 범주를 기반으로 프로젝트 트랜잭션을 그룹화하고 이러한 그룹에 대한 완료율 계산 규칙을 정의할 수 있습니다.
    - **기간 코드** : 주어진 프로젝트 비용 및 수익 프로필에 대해 예상 수익이 계산되는 빈도를 정의합니다.
    - **추정 범주** : 프로젝트 트랜잭션에 대한 영업 가치(미수 수익) 전기에 사용됩니다. 먼저 **수수료** 트랜잭션 유형에 대한 전용 프로젝트 범주를 구성한 다음 이 프로젝트 범주에 대한 **견적** 플래그를 설정합니다. 그런 다음 선택한 일치 원칙에 따라 프로젝트 비용 및 수익 프로필의 **영업** 가치 또는 **이익** 필드에서 이 프로젝트 범주를 선택합니다.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>프로젝트 비용 및 수익 프로필에 대한 샘플 구성

시간 및 자재 – WIP 없음

![비용 및 수익 프로필: 시간 및 자재 - WIP 없음](media/time-material-no-wip.png)

시간 및 자재 – WIP(수익)

![비용 및 수익 프로필: 시간 및 자재 - WIP](media/time-material-with-wip.png)

고정 가격 – WIP 없음

![비용 및 수익 프로필: 고정 가격 - WIP 없음](media/fixed-price-no-wip.png)

고정 가격 – 완료된 계약

![비용 및 수익 프로필: 고정 가격 - 완료된 계약](media/fixed-price-completed-contract.png)

고정 가격 – 완료율

![비용 및 수익 프로필: 고정 가격 - 완료율](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>샘플 프로젝트 비용 및 수익 프로필에 대한 회계 이벤트 예.

| 회계 이벤트                  | 시간 및 자재 - WIP 없음                       | 시간 및 자재 - WIP                                                                                           | 고정 가격 – WIP 없음                                            | 고정 가격 – 완료된 계약                                                                            | 고정 가격 – 완료율                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| 시간 트랜잭션 분개    | 차변 – 비용 <br>대변 – 급여 할당          | 차변 – 비용 <br>대변 – 급여 할당 <br>차변 –WIP 영업 가치 <br>대변 – 미수 수익 영업 가치                | 차변 – 비용 <br>대변 – 급여 할당                         | 차변 – 비용 <br>대변 – 급여 할당                                                                    | 차변 – 비용 <br>대변 – 급여 할당                       |
| 경비 트랜잭션 분개 | 차변 – 비용 <br>대변 – 경비에 대한 상쇄 계정 | 차변 – 비용 <br>대변 – 경비에 대한 상쇄 계정 <br>차변 – WIP 영업 가치 <br>대변 – 미수 수익 영업 가치      | 차변 – 비용 <br>대변 – 경비에 대한 상쇄 계정                 | 차변 – 비용<br> 대변 – 경비에 대한 상쇄 계정                                                            | 차변 – 비용 <br>대변 – 경비에 대한 상쇄 계정               |
| 고객 송장 작성                | 차변 – 고객 잔액 <br>대변 – 송장 발부된 수익 | 차변 – 고객 잔액 <br>대변 – 송장 발부된 수익 <br>대변 – WIP 영업 가치 차변 – 미수 수익 영업 가치 | 차변 – 고객 잔액 <br>대변 – 송장 발부된 수익 - 계정별 | 차변 – 고객 잔액 <br>대변 – WIP – 계정별 송장 발부                                                  | 차변 – 고객 잔액 <br>대변 – WIP – 계정별 송장 발부    |
| 전기 수익 추정             | 해당 없음                                   | 해당 없음                                                                                                    | 해당 없음                                                  | 차변 – WIP 비용 값 <br>대변 – 비용                                                                         | 차변 – WIP - 영업 가치 <br>대변 – 미수 수익 영업 가치 |
| 제거                         | 해당 없음                                   | 해당 없음                                                                                                    | 해당 없음                                                  | 대변 – WIP 비용 값 <br>차변 – 비용 <br>대변 – 미수 수익 - 영업 가치 <br>차변 – WIP 계정별 송장 발부 | 차변 – WIP - 계정별 송장 발부 <br>대변 – WIP 영업 가치     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>프로젝트 비용 및 수익 프로필 규칙 구성

프로젝트 비용 및 수익 프로필 규칙은 청구 가능한 프로젝트 트랜잭션을 처리할 때 사용해야 하는 프로젝트 비용 및 수익 프로필을 결정합니다. **프로젝트 관리 및 회계** \>**설정** \>**전기** \>**프로젝트 비용 및 수익 프로필 규칙** 으로 이동하여 규칙을 정의합니다.

규칙은 프로젝트 계약, 프로젝트 그룹 또는 특정 프로젝트별로 정의할 수 있습니다. 시스템은 항상 가장 높은 세분성 규칙을 먼저 선택합니다.