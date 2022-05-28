---
title: 트랜잭션 연결 - 서로 다른 트랜잭션 유형의 실제 연결
description: 이 항목에서는 수익성, 청구 백로그, 청구 대 미청구 수익 계산을 추적하는 데 도움이 되도록 다양한 유형의 실제를 연결하는 데 트랜잭션 연결을 사용하는 방법을 설명합니다.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580786"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>트랜잭션 연결 - 서로 다른 트랜잭션 유형의 실제 연결

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

트랜잭션 연결 레코드는 견적 또는 사전 판매 단계에서 계약 단계, 승인 및/또는 회수, 송장 발행, 잠재적 신용 또는 수정 송장 발행으로의 라이프사이클에서 시간, 비용 또는 자재 사용량 이동과 같은 다양한 유형의 실제를 연결하기 위해 생성됩니다.

다음 예는 Project Operations 프로젝트 라이프사이클에서 시간 항목의 일반적인 처리를 보여줍니다.

> ![Project Operations에서 시간 항목을 처리합니다.](media/basic-guide-17.png)

Project Operations 프로젝트 수명 주기의 시간 항목 처리는 다음 단계를 따릅니다. 

1. 시간 항목을 제출하면 비용과 미청구 매출액에 대한 두 개의 분개장 행이 생성됩니다. 
2. 시간 항목을 최종 승인하면 비용과 미청구 매출액에 대한 두 개의 실제값이 생성됩니다. 이 2개의 실제는 트랜잭션 연결을 사용하여 연결됩니다.
3. 사용자가 프로젝트 청구서를 만들면 미청구 매출액 실제값의 데이터를 사용하여 청구서 행 처리가 생성됩니다.
4. 송장이 확인되면 청구되지 않은 판매 취소와 청구된 판매 실제라는 두 개의 새로운 실제가 생성됩니다. 미청구 판매 취소 및 원래 청구되지 않은 실제 판매는 취소 트랜잭션 연결을 사용하여 연결됩니다. 청구된 판매액과 원래 청구되지 않은 실제 판매액도 연결되어 한때 백로그 또는 재공품(WIP) 수익이었던 것과 현재 청구된 수익 사이의 링크를 보여줍니다.   

처리 워크플로의 각 이벤트는 **트랜잭션 연결** 테이블의 레코드 생성을 트리거합니다. 이것은 시간 입력, 분개장 항목, 실제 및 송장 라인 세부 사항에 걸쳐 생성된 레코드 간에 관계의 추적을 구축하는 데 도움이 됩니다.

다음 표는 이전 워크플로에 대한 **트랜잭션 연결** 엔터티의 레코드를 보여줍니다.

|이벤트                   |처리 1                 |처리 1 역할 |처리 1 타입       |처리 2          |처리 2 역할 |처리 2 타입 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|시간 항목 제출   |분개장 행 (매출액) GUID     |미청구 매출액 |msdyn_journalline            |분개장 행 (원가) GUID     |비용            |msdyn_journalline  |
|시간 승인           |미청구 실제값 (매출액) GUID  |미청구 매출액 |msdyn_actual                 |원가 실제값(원가) GUID       |비용            |msdyn_actual       |
|청구서 생성        |청구서 행 내역 GUID      |청구 매출액   |msdyn_invoicelinetransaction |미청구 매출액 실제값 GUID   |미청구 매출액  |msdyn_actual       |
|청구서 확인    |실제값 반전 GUID         |반전      |msdyn_actual                 |원 미청구 매출액 GUID |원본        |msdyn_actual       |
|                        |청구 매출액 GUID             |청구 매출액   |msdyn_actual                 |미청구 매출액 실제값 GUID   |미청구 매출액  |msdyn_actual       |
|청구서 초안 수정 |청구서 행 처리 GUID|교체      |msdyn_invoicelinetransaction |청구 매출액 GUID            |원본        |msdyn_actual       |
|청구서 수정 확인|청구 매출액 반전 GUID  |반전      |msdyn_actual                 |청구 매출액 GUID            |원본        |msdyn_actual       |
|                        |신규 미청구 매출액 GUID |교체            |msdyn_actual                 |청구 매출액 GUID            |원본        |msdyn_actual       |


다음 그림은 Project Operations의 시간 입력 예를 사용하여 다양한 이벤트에서 서로 다른 유형의 실제 사이에 생성된 링크를 보여줍니다.

> ![Project Operations에서 서로 다른 유형의 실제가 서로 연결되는 방식입니다.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
