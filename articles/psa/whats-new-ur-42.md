---
title: Project Service Automation 업데이트 릴리스 42, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 42, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589204"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Project Service Automation 업데이트 릴리스 42, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 42, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.73.61이며 일반적으로 2022년 4월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-42"></a>업데이트 릴리스 42

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**시간 및 경비**

- 타임시트가 거부되면 거부한 사용자가 **시스템** 으로 잘못 식별됩니다.
- 시간 항목을 가져올 때 **리소스 범주** 값이 누락되었습니다.
- 프로젝트 승인자는 권한이 특별히 **승인 가능** 으로 설정되지 않은 경우 제출된 프로젝트를 승인할 수 있습니다.

**판매**

- 루트가 아닌 작업에 실제가 기록되면 실제 비용이 잘못 집계됩니다.
