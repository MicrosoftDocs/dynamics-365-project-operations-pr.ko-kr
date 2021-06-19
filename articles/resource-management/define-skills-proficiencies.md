---
title: 기술 및 숙련도 정의
description: 이 항목은 리소스를 평가하기 위해 숙련도 모델을 설정하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015339"
---
# <a name="define-skills-and-proficiencies"></a>기술 및 숙련도 정의

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

기능은 Dynamics 365 Project Operations과 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다. 

- Project Operations에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능** 으로 이동하십시오. 

## <a name="use-proficiency-models-to-rate-resources"></a>숙련도 모델을 사용하여 리소스 평가

리소스의 기능은 숙련도 모델에 의해 평가됩니다. 개별 등급은 숙련도 모델에 있습니다. 

1. 숙련도 모델을 만들려면 **리소스** \> **숙련도 모델** 로 이동한 다음 **신규** 를 선택합니다.
2. 새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.
3. **등급 값** 하위 표에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.


이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]