---
title: 계약의 사전 판매 단계에서 실제 영향
description: 이 항목에서는 계약이 Microsoft Dynamics 365 Project Operations의 사전 판매 단계에 있는 동안 다양한 이벤트에서 실제 테이블에 미치는 영향에 대한 정보를 제공합니다.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577244"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>계약의 사전 판매 단계에서 실제 영향

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

다음 표에는 프로젝트 계약의 사전 판매 단계 동안 다양한 이벤트에서 생성되는 다양한 트랜잭션 유형의 실제 값이 나열되어 있습니다.

| 이벤트 | 비용 실제값 | 예 |
|---|---|---|
| 시간이 생성됩니다. | 해당 없음 | <p>시간당 비용이 100달러(미화 100달러)인 Fabrikam US 조직 구성 단위의 Bob Kozack은 "Adatum에 암 설치"라는 프로젝트를 진행하고 있습니다. 이 프로젝트는 계약 내용의 고정 가격 청구 방법에 매핑됩니다. 다음은 Bob Kozak의 샘플 시간 항목입니다.</p><p>Bob Kozack - 8시간</p> |
| 시간이 제출됩니다. | 해당 없음 | 시간 입력에 대한 비용 분개장 항목이 생성됩니다. 기본 가격과 원가 요율은 분개장에 입력됩니다. |
| 시간 입력은 승인되기 전에 회수됩니다. | 해당 없음 | |
| 시간이 승인됩니다. | 비용 실제 값이 생성됩니다. | <p>생성된 새 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, 8시간, USD 800</li></ul> |
| 시간 승인이 취소됩니다. | <p>원래 비용 실제 값의 조정 상태가 **조정됨** 으로 업데이트됩니다.</p><p>조정 상태가 **조정 불가능** 인 비용 실제 값 취소가 생성됩니다.</p> | <p>업데이트된 기존 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, 8시간, USD 800, *조정됨*</li></ul><p>이전 재무 영향을 취소하기 위해 생성된 신규 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, (8시간), (USD 800), *조정 불가능*</li></ul> |
| 시간 입력은 승인된 후 회수됩니다. | <p>원래 비용 실제 값의 조정 상태가 **조정됨** 으로 업데이트됩니다.</p><p>조정 상태가 **조정 불가능** 인 비용 실제 값 취소가 생성됩니다.</p> | <p>업데이트된 기존 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, 8시간, USD 800, *조정됨*</li></ul><p>이전 재무 영향을 취소하기 위해 생성된 신규 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, (8시간), (USD 800), *조정 불가능*</li></ul> |
| 견적이 성사되고 계약이 생성됩니다. | <p>기존 비용 실제 값의 조정 상태가 **조정됨** 으로 업데이트됩니다.</p><p>조정 상태가 **조정 불가능** 인 비용 실제 값 취소가 생성됩니다.</p><p>계약 규칙을 재평가한 후 새로운 비용 실제 값이 생성됩니다.</p> | <p>업데이트된 기존 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, 8시간, USD 800, *조정됨*</li></ul><p>이전 재무 영향을 취소하기 위해 생성된 신규 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, (8시간), (USD 800), *조정 불가능*</li></ul><p>견적이 성사되고 계약이 생성될 때 재평가된 재무적 영향에 대해 생성되는 신규 실제 값:</p><ul><li>**비용 실제 값:** Bob Kozack, 8시간, USD 800</li><li>**미청구 매출액 실제값**: Bob Kozack, 8시간, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
