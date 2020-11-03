---
title: 프로젝트 및 프로젝트 계약에 대한 청구서 백로그 검토
description: 이 항목은 시간, 비용 및 제품 백로그를 검토하는 방법과 청구서를 사용할 준비가 된 것으로 표시하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080261"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>프로젝트 및 프로젝트 계약에 대한 청구서 백로그 검토

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

청구서를 생성 및 처리하도록 트랜잭션이 준비되면 트랜잭션이 **청구서 발행 준비** 로 표시되어야 합니다. 이 항목은 만들 수 있는 트랜잭션의 타입을 설명합니다.

## <a name="review-the-time-and-material-billing-backlog"></a>시간 및 자재 대금 청구 백로그 검토

프로젝트에 대한 시간 또는 비용 항목이 제출되고 승인되면 PSA는 프로젝트 실제값을 생성합니다. 프로젝트와 트랜잭션 클래스의 조합이 시간 및 자재 프로젝트의 계약 행에 매핑되면 항목이 승인될 때 두 개의 실제값이 만들어집니다:

- 비용 실제값 
- 미청구 매출액 실제값

미청구 매출액 실제값은 청구 백로그를 나타내며, 청구 상태를 **청구서 발행 준비** 로 설정해야 합니다. 프로젝트 청구서를 만들 때 **청구서 발행 준비** 로 표시되어 있는 미청구 판매 실제값이 청구서 행 내역으로 복사됩니다.

시간 및 자재에 대한 청구 백로그를 검토하려면 **판매** \> **청구** \> **시간 및 자재 청구 백로그** 로 이동하십시오. 청구서 발행 준비된 미청구 판매 실제값을 모두 선택한 다음, **청구서 발행 준비** 를 선택합니다. 이러한 실제값의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.

![시간 및 자재 대금 청구 백로그](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>제품 대금 청구 백로그 검토

PSA에서는 프로젝트 계약에 제품 기반 계약 행이 있는 경우 해당 행은 프로젝트 계약에 대한 청구서가 작성될 때마다 청구서 발행으로 간주됩니다. **청구서 발행 준비** 로 표시된 계약 행이 있는 제품은 프로젝트 청구서 행으로서 프로젝트 청구서에 복사됩니다.

제품에 대한 청구 백로그를 검토하려면 **판매** \> **청구** \> **제품 대금 청구 백로그** 로 이동하십시오. 청구서 발행 준비된 제품 기반 계약 행을 모두 선택한 다음, **청구서 발행 준비** 를 선택합니다. 이러한 행의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.

![제품 대금 청구 백로그](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>고정 가격 계약의 청구 이정표 검토

고정 가격 청구 방법이 있는 각 프로젝트 계약 행은 계약 이정표를 정의해야 합니다. 이러한 계약 이정표는 **청구서 발행 준비** 로 표시된 경우에만 청구서를 발행할 수 있습니다. 

청구 이정표를 검토하려면 **판매** \> **청구** \> **고정 가격 이정표** 로 이동하십시오. 청구서 발행 준비된 이정표를 선택한 다음, **청구서 발행 준비** 를 선택합니다. 이러한 이정표의 청구 상태가 **청구서 발행 준비** 로 변경됩니다.

![고정 가격 이정표](media/FPBacklog.png)
