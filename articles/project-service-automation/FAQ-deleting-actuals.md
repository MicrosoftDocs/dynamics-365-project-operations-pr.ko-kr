---
title: 실제값 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?
description: 이 항목은 실제값 엔터티에서 레코드를 삭제할 수 없는 이유에 대한 정보를 제공합니다.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753229"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="d0148-103">실제 엔터티에서 레코드를 삭제할 수 없는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="d0148-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d0148-104">Project Service Automation(PSA)에서는 실제값이 총원장 같은 후방 시스템에 재무적 의미를 갖는 처리를 위한 진리원으로 작용하기 때문에 귀하는 실제값을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0148-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="d0148-105">실제값을 삭제할 수 있다면 재무 보고 처리의 무결성에 의문을 제기할 수 있을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d0148-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="d0148-106">감사 추적을 설정하려면 고객은 분개장을 사용하여 보상 처리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0148-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

