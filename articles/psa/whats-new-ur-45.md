---
title: Project Service Automation 업데이트 릴리스 45, V3의 새로운 기능 또는 변경된 기능
description: 이 문서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 45, V3에서 사용할 수 있는 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169161"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Project Service Automation 업데이트 릴리스 45, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation 업데이트 릴리스 45, V3의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.76.168이며 일반적으로 2022년 7월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-45"></a>업데이트 릴리스 45

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**판매**

- 사용자가 페이지의 동일 인스턴스를 보고 있고 새로 고치지 않으면 미청구 매출액 없이 송장을 생성하려고 시도한 후 송장을 성공적으로 생성할 수 없습니다.

**시간 및 경비**

- 최신 승인이 활성화되고 회수된 프로젝트 승인이 승인되면 레코드 스테이지가 **리콜 요청 승인됨** 으로 잘못 업데이트됩니다.
- 최신 승인이 활성화되고 클라우드 흐름이 비활성화되면 승인 프로세스가 성공하지 못하고 제출 또는 승인하는 사용자에게 알림이 전송되지 않습니다.
