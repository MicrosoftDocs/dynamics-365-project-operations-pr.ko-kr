---
title: Project Service Automation 업데이트 릴리스 28, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 28, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150631"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Project Service Automation 업데이트 릴리스 28, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 28에 대해 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.이 버전에는 V3.10.46.32의 빌드 번호가 있으며 일반적으로 2021년 1월에 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-28"></a>업데이트 릴리스 28

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- 사용자는 **대량 편집** 을 사용하여 승인 및 제출된 시간 항목을 업데이트할 수 있습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- 작업 GUID가 숫자로 해석되는 경우 **작업 분할 구조** 페이지의 리본에 있는 **작업 편집** 을 사용하여 편집할 작업을 열 수 없습니다.

**Sales**

다음과 같은 문제가 해결되었습니다.

- **GetEstimatesForProject** 플러그인이 호출되면 null 참조 예외가 생성됩니다.
- 중요 시점 그리드의 **송장 발부 준비 완료로 표시** 는 업데이트된 **InvoiceStatus** 특성을 제외하고 특성을 부분적으로만 업데이트합니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]