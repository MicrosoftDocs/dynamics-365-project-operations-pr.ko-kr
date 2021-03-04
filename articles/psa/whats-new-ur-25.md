---
title: Project Service Automation 업데이트 릴리스 25, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 25, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143767"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation 업데이트 릴리스 25, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 25에 대해 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.이 버전에는 V 3.10.43.76의 빌드 번호가 있으며 일반적으로 2020년 10월에 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-25"></a>업데이트 릴리스 25

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음 문제가 해결되었습니다.

- 검색되는 너무 큰 간격을 기반으로 추가 데이터를 표시하는 시간 입력 차트.

**리소스 관리**

다음 문제가 해결되었습니다.

- Package Deployer 코드를 추가하여 더 높은 버전의 패치가 이미 있는 경우 Universal Resource Scheduling 패치 가져오기를 건너뜁니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- 반올림 및 환율 불일치를 수정하여 프로젝트 추적 그리드에서 계획된 비용이 잘못되었습니다.
- **프로젝트** 양식에서 두 개 이상의 반응 그리드를 표시하는 기능을 지원합니다.
- 달력 종료 날짜가 지난 작업을 할당할 수 있는 기능을 해결하기 위한 유효성 검사를 제공하여 리소스 할당이 실패했습니다.
- 다음에서 생성된 Null 참조 예외를 해결하기 위해 오류 처리가 개선되었습니다.

    - **PreValidateProjectTeamMemberCreate** 플러그인
    - 연결된 프로젝트 없이 프로젝트 작업이 생성될 때 **PreValidateProjectTaskCreate**
    - **PreProjectTeamMemberCreate** 플러그인
    - **PostProjectTeamMemberDelete** 플러그인
    - **PreValidateProjectTaskDelete** 플러그인

**Sales**

다음과 같은 문제가 해결되었습니다.

- **프로젝트 복사: 도우미 리소스 관리 추정** 에서 생성된 Null 참조 예외를 해결하기 위해 오류 처리가 개선되었습니다.
- **시간 및 재료 청구 백로그** 의 **송장 발부 준비 안 됨** 이 청구 상태를 지우지 않습니다.
- **역할 가격** 및 **카탈로그 항목** 탭의 잘못된 라벨 **가격** 단추가 해결되었습니다.
