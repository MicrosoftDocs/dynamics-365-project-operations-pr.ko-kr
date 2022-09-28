---
title: Project Service Automation 업데이트 릴리스 47, V3의 새로운 기능 또는 변경된 기능
description: 이 문서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 47, V3에서 사용할 수 있는 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477238"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Project Service Automation 업데이트 릴리스 47, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation 업데이트 릴리스 45, V3의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.78.8이며 일반적으로 2022년 7월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-47"></a>업데이트 릴리스 47

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**리소스 관리**
- 사용자가 **예약 가능한 리소스** 없이 프로젝트 팀 구성원을 만들려고 할 때 null 참조 예외를 트리거할 수 없도록 유효성 검사가 업데이트되었습니다.
