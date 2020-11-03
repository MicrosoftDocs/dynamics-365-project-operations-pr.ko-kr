---
title: 실제값 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?
description: 이 항목은 실제값 엔터티에서 레코드를 삭제할 수 없는 이유에 대한 정보를 제공합니다.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080178"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>실제 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation(PSA)에서는 실제값이 총원장 같은 후방 시스템에 재무적 의미를 갖는 처리를 위한 진리원으로 작용하기 때문에 귀하는 실제값을 삭제할 수 없습니다. 실제값을 삭제할 수 있다면 재무 보고 처리의 무결성에 의문을 제기할 수 있을 것입니다. 감사 추적을 설정하려면 고객은 분개장을 사용하여 보상 처리를 만들어야 합니다.

