---
title: Project Service Automation 업데이트 릴리스 29, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 29, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499679"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Project Service Automation 업데이트 릴리스 29, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 29에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.45.98이며 2021년 2월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-29"></a>업데이트 릴리스 29

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- 사용자는 시간 입력 그리드에서 휴무일에 기록된 근무 시간을 볼 수 없습니다.
- 승인된 경비 항목은 그리드에서 편집할 수 있습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- 리소스 할당 작업 시간을 보장하기 위한 검증 로직이 누락되어도 음수일 수 없습니다.
- 사용자 지정 작업 **AssignResourcesForTask** 는 변경된 필드 대신 모든 필드를 업데이트합니다.
- 플러그인 또는 워크플로가 있는 환경에서 프로젝트를 복사할 때 **CreateProject** 이벤트, **msdyn_bulkgenerationstatus** 특성은 **CopyWBSToProject** 가 실패하면 업데이트되지 않습니다.
- 프로젝트 달력을 확장하면 작업일이 오름차순으로 정렬되지 않아 일부 프로젝트 작업 업데이트가 실패합니다.
- 기존 프로젝트에서 프로젝트 관리자를 변경하면 조직 단위 기본값 논리가 트리거됩니다.

**판매**

다음과 같은 문제가 해결되었습니다.

- 계약 내용이 없는 경우 초기화 중에 **계약** 페이지의 **계약 성능** 탭이 자동으로 실패합니다.
