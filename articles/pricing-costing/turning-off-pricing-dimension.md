---
title: 가격 책정 차원 끄기
description: 이 항목은 가격 책정 차원을 끄는 방법에 대한 정보를 제공합니다.
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650057"
---
# <a name="turning-off-a-pricing-dimension"></a>가격 책정 차원 끄기

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

몇 년마다 가격 책정 전략을 검토하고 업데이트해야 할 수 있습니다. 업데이트를 통해 기존 가격 책정 차원을 해제하고 새 것을 만들어야 할 수 있습니다. 예컨대, 이전에는 **역할** 별로 가격이 책정되었을 수 있지만 이제 귀하는 **작업 경험** 별로 가격을 책정하기로 결정했습니다. 이렇게 하려면 가격 책정 차원으로서의 **역할** 을 해제하고 새로운 가격 책정 차원으로서 **작업 경험** 을 만들어야 할 수 있습니다. 

그것이 즉시 사용할 수 있는 것이든 또는 맞춤이든 관계없이, 가격 책정 차원의 **비용에 적용 가능** 및 **판매에 적용 가능** 필드를 **아니오** 로 설정함으로써 가격 책정 차원을 해제할 수 있습니다.

그러나 이렇게 하면 **연관된 가격 레코드가 있는 경우 가격 책정 차원을 업데이트하거나 삭제할 수 없습니다.** 오류 메시지가 표시될 수 있습니다.

![가격 책정 차원을 해제할 때 비즈니스 프로세스 오류 발생 가능성](media/Business-Process-Error.png)

이 오류 메시지는 해제되는 차원에 대해 이전에 설정된 가격 레코드가 있음을 나타냅니다. 차원에 준거하는 모든 **역할 가격** 및 **역할 가격 마크업** 레코드를 삭제해야 차원의 적용 가능성을 **아니오** 로 설정할 수 있습니다. 이 규칙은 즉시 사용 가능한 가격 책정 차원과 생성된 맞춤 가격 책정 차원 모두에 적용됩니다. 이 유효성 검사의 이유는 각 **역할 가격** 레코드는 차원들의 고유한 조합을 가져야 하기 때문입니다. 예컨대, **US Cost Rates 2018** 이라는 가격표에 다음 **역할 가격** 행이 있습니다. 

| 표준 직함         | 조직 단위    |단위   |가격  |통화  |
| -----------------------|-------------|-------|-------|----------|
| 시스템 엔지니어|Contoso US|Hour| 100|USD|
| 선임 시스템 엔지니어|Contoso US|Hour| 150| USD|


가격 책정 차원으로서의 **표준 직함** 을 끄고 가격 책정 엔진이 가격을 검색하면 입력 컨텍스트에서 **조직 단위** 값만 사용됩니다. 입력 컨텍스트의 **조직 단위** 가 "Contoso US"인 경우 두 행이 모두 일치하므로 결과가 결정적이지 않습니다. 이 시나리오를 피하기 위해 **역할 가격** 레코드를 만들 때 시스템은 차원의 조합이 고유한지 확인합니다. **역할 가격** 레코드를 만든 후 차원을 해제하면 이 제약 조건을 위반할 수 있습니다. 따라서 차원을 끄기 전에, 해당 차원 값이 채워진 모든 **역할 가격** 및 **역할 가격 마크업** 행을 삭제할 것이 요구됩니다.
