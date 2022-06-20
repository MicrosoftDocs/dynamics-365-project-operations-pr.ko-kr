---
title: Project Service Automation 업데이트 릴리스 43, V3의 새로운 기능 또는 변경된 기능
description: 이 문서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 43, V3에서 사용할 수 있는 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915330"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Project Service Automation 업데이트 릴리스 43, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation 업데이트 릴리스 43, V3의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.74.200이며 일반적으로 2022년 5월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-43"></a>업데이트 릴리스 43

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.


**시간 및 경비**

- 예약 또는 리소스 할당에서 시간 항목을 가져올 때 예약 가능한 관련 리소스에 대한 참조가 유지되지 않습니다.
- 시간 입력 그리드가 전체 화면으로 확장되면 탭 키로 그리드 탐색이 작동하지 않습니다.
- 다른 사용자가 만든 시간 항목을 제출할 때 **제출자** 필드가 작업표를 만든 사용자로 잘못 채워집니다.
