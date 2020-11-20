---
title: 실제값 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?
description: 이 항목은 실제값 엔터티에서 레코드를 삭제할 수 없는 이유에 대한 정보를 제공합니다.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127166"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="517eb-103">실제 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="517eb-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="517eb-104">Project Service Automation(PSA)에서는 실제값이 총원장 같은 후방 시스템에 재무적 의미를 갖는 처리를 위한 진리원으로 작용하기 때문에 귀하는 실제값을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="517eb-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="517eb-105">실제값을 삭제할 수 있다면 재무 보고 처리의 무결성에 의문을 제기할 수 있을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="517eb-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="517eb-106">감사 추적을 설정하려면 고객은 분개장을 사용하여 보상 처리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="517eb-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

