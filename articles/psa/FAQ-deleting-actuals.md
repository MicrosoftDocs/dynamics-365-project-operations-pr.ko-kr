---
title: 실제값 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?
description: 이 항목은 실제값 엔터티에서 레코드를 삭제할 수 없는 이유에 대한 정보를 제공합니다.
author: JPBurrows
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002879"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>실제 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation(PSA)에서는 실제값이 총원장 같은 후방 시스템에 재무적 의미를 갖는 처리를 위한 진리원으로 작용하기 때문에 귀하는 실제값을 삭제할 수 없습니다. 실제값을 삭제할 수 있다면 재무 보고 처리의 무결성에 의문을 제기할 수 있을 것입니다. 감사 추적을 설정하려면 고객은 분개장을 사용하여 보상 처리를 만들어야 합니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]