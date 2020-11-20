---
title: 기능 및 숙련도 모델
description: 이 항목은 기능 및 숙련도 모델을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124196"
---
# <a name="skills-and-proficiency-models"></a>기능 및 숙련도 모델

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

기능은 Dynamics 365 Project Service Automation과 존재하는 경우 Dynamics 365 Field Service 사이에 공유되는 리소스 특성입니다. 

Project Service Automation에서 기능 리포지토리를 정비하려면 **리소스** \> **리소스 기능** 으로 이동하십시오. 

> ![리소스 기능](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>숙련도 모델을 사용하여 리소스 평가

리소스의 기능은 숙련도 모델에 의해 평가됩니다. 개별 등급은 숙련도 모델에 있습니다. 

1. 숙련도 모델을 만들려면 **리소스** \> **숙련도 모델** 로 이동한 다음 **신규** 를 선택합니다.
2. 새 등급 모델에서 최소 등급 값, 최대 등급 값 및 등급이 지정되는 엔터티를 지정합니다.
3. **등급 값** 하위 표에서 최소값에서 최대값까지 다른 등급 값을 정의할 수 있습니다.

> ![정의된 최소 및 최대 등급](media/Resource-Management-image85.png)

이러한 등급 값은 **리소스 요건**, **스케줄 게시판** 및 **스케줄 도우미** 필터에 표시됩니다.
