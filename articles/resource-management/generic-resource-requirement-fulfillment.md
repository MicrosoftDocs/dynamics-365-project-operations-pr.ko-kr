---
title: 일반 리소스 요구 사항 충족
description: 이 항목은 일반 리소스 요건을 위해 명명된 리소스를 예약하는 것에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897594"
---
# <a name="generic-resource-requirement-fulfillment"></a>일반 리소스 요구 사항 충족

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

명명된 리소스를 예약하여 리소스 요건이 있는 일반 리소스를 대체할 수 있습니다.

1. **프로젝트** 페이지에서 **팀** 탭을 선택합니다.
2. 목록에서 리소스 요건이 있는 일반 리소스를 선택한 다음**예약**을 선택합니다. 또는 리소스 요건을 연 다음 **예약**을 선택합니다.
3. **스케줄 도우미** 페이지에서 프로젝트 팀에 예약할 명명된 리소스를 선택한 다음 **예약**을 선택합니다.

명명된 리소스에 의해 예약이 완료되고 이행되면 일반 리소스가 명명된 리소스로 대체됩니다.

스케줄에서의 배정도 명명된 리소스로 업데이트됩니다.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>명명된 여러 리소스로 일반 리소스 이행
일반 리소스를 위한 요건을 여러 명명된 리소스로 충족하는 것은 명명된 단일 리소스를 배정하는 것과 유사합니다. 예컨대, 5일의 기간과 120시간의 노력이 드는 과업이 있습니다. 이 과업은 주 5일에 걸쳐 일반적인 하루 8시간 일하는 하나의 리소스로 완료할 수 없습니다. 

이 요건은 120시간의 로봇 공학을 위한 것으로서 하루 24시간에 해당됩니다.

이는 일반 리소스 요청을 이행하기 위해 여러 개의 명명된 리소스가 필요한 경우의 예입니다. 요건을 충족하려면 여러 리소스를 예약해야 합니다.

이 시나리오의 주요 차이점은 일반 리소스가 과업에 배정된 팀에 남아 있고 예약된 명명된 리소스 팀원이 직위의 일부로 배정되지 않는다는 것입니다. 프로젝트 관리자는 명명된 리소스에 적합한 과업을 배정할 수 있습니다. **조정** 보기는 프로젝트 관리자가 여러 리소스에 걸쳐 작업 배정에 대한 예약을 나누는 데 도움이 될 수 있습니다. 요건을 구성하는 작업 번들이 있는 경우와 같이 위의 간단한 예보다 더 복잡한 시나리오에서는 프로젝트 관리자가 배정하려는 방식의 의도를 시스템에서 가정해야 하기 때문에 이 작업은 자동으로 수행되지 않습니다. 시스템이 의도를 이해할 수 없기 때문에 가정이 의도한 것과 다를 수 있으며 올바르지 않거나 예측할 수 없는 결과가 발생할 가능성이 있습니다. 프로젝트 관리자가 **조정** 보기의 도움을 받아 의도적으로 배정을 만들 때까지 예측 가능한 결과는 일반 리소스가 배정된 상태로 유지된다는 것입니다.


