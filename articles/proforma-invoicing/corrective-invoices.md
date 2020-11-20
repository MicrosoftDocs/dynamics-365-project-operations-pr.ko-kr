---
title: 수정된 송장
description: 이 주제는 수정된 송장에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122396"
---
# <a name="corrected-invoices"></a>수정된 송장

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

확인된 송장을 편집할 수 있습니다. 확인된 송장을 편집하면 임시 수정된 송장이 만들어집니다. 원래 송장의 모든 트랜잭션 및 수량을 되돌리려는 가정이기 때문에 이 수정된 송장에는 원래 송장의 모든 트랜잭션이 포함되며 모든 수량은 0(제로)입니다.

트랜잭션에 수정이 필요하지 않은 경우 초안 수정 송장에서 제거할 수 있습니다. 일부 수량만 되돌리거나 반환하려면 라인 세부 사항에서 수량 필드를 편집할 수 있습니다. 송장 라인 세부 정보를 열면 원래 송장 수량을 볼 수 있습니다. 그런 다음 원래 송장 수량보다 적거나 많은 현재 송장 수량을 편집할 수 있습니다.

수정 송장을 확인할 때 원래 청구된 영업 실제가 반대이며, 새 청구된 영업 실제가 생성됩니다. 수량이 줄어든 경우 그 차이로 인해 실제 청구되지 않은 새 영업도 생성됩니다. 예를 들어 원래 청구된 영업이 8시간이고 수정된 송장 라인 세부 정보가 6시간으로 줄어든 경우 원래 청구된 영업 라인을 반대로 하고 두 개의 새 실제를 만듭니다.

- 6시간 동안 실제 청구된 영업.
- 나머지 2시간 동안 청구되지 않은 영업 실제. 이 거래는 고객과의 협상에 따라 나중에 청구되거나 요금이 부과되지 않는 것으로 표시될 수 있습니다.
