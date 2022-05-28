---
title: Project Service Automation 업데이트 릴리스 40, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 40, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588652"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Project Service Automation 업데이트 릴리스 40, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 40, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.61.61이며 2022년 2월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-40"></a>업데이트 릴리스 40

### <a name="features"></a>기능
Project Service Automation에서 Project Operations - Lite로의 업그레이드 1단계는 2022년 2월 모든 고객에게 릴리스됩니다. 자격을 확인하려면 [Project Service Automation에서 Project Operations로 업그레이드](upgrade-project-operations-non-stocked.md)를 참조하십시오. 애플리케이션이 Power Platform 관리 센터의 인스턴스에 표시되지 않는 경우 지원에 문의하여 해당 환경에 대해 플라이트를 활성화하도록 요청하십시오. 요청에는 플라이트를 활성화해야 하는 환경 ID 목록이 포함되어야 합니다.

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**시간 및 경비**
- 시간 입력이 거부되거나 취소되면 메모 입력이 누락됩니다. 

**판매**

- 즉시 사용 가능한 플러그인을 사용하여 비용 또는 판매 추정치를 업데이트하는 경우 사용자 인터페이스 외부에서 유효하지 않은 JSON 페이로드를 보내는 것이 잘못 허용됩니다.
- 빠른 보기를 사용하여 견적 라인을 업데이트할 때 견적을 활성화할 수 있습니다.
