---
title: 기능 및 숙련도 모델
description: 이 항목은 기능 및 숙련도 모델을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73509fda4a715a4131781645736e49cfb02115da2c3650c5a966e35360e7703f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990504"
---
# <a name="skills-and-proficiency-models"></a>기능 및 숙련도 모델

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

기능은 Dynamics 365 Project Service Automation과 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다. 

Project Service Automation에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능** 으로 이동하십시오. 

> ![리소스 기술.](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>숙련도 모델을 사용하여 리소스 평가

리소스의 기능은 숙련도 모델에 의해 평가됩니다. 개별 등급은 숙련도 모델에 있습니다. 

1. 숙련도 모델을 만들려면 **리소스** \> **숙련도 모델** 로 이동한 다음 **신규** 를 선택합니다.
2. 새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.
3. **등급 값** 하위 표에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.

> ![정의된 최소 및 최대 등급.](media/Resource-Management-image85.png)

이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]