---
title: Project Service Automation 업데이트 릴리스 15, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 15, V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585156"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation 업데이트 릴리스 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 PSA V3, 업데이트 릴리스 15에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.5.28이며 2020년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-15"></a>업데이트 릴리스 15 

### <a name="enhancements"></a>향상된 기능

- 프로젝트 관리

### <a name="bug-fixes"></a>버그 수정

- 시간 및 경비

  - 수정: 조정 보기에서 부하 시 오류 처리 추가.
  - 수정: 프로젝트 리소스 허브: 모호성을 줄이기 위해 **금액** 의 이름 변경.
  - 수정: **시간 항목 열 복사** 보기가 유형을 포함하도록 조정.
  - 수정: 십진수를 사용하여 표 보기에서 시간 입력 기간을 편집하면 일부 숫자에 알 수 없는 오류가 발생합니다.

- 프로젝트 관리

  - 수정: **추적 보기에서 사용** 드롭다운 메뉴 옵션이 이제 너비에 따라 확장됩니다.
  - 수정: +13 시간대에서 프로젝트를 관리할 때 작업 계산에 부정확한 결과가 표시될 수 있습니다.
  - 수정: 24시간 달력을 사용할 때 **팀 멤버 종료 시간** 이 수정되었습니다.
  - 수정: **msdyn_project** 기본 양식의 **BPF** 재활성화.
  - 수정: 할당 계산이 더 이상 하루를 무시하지 않습니다.
  - 수정: 사용자와 프로젝트의 시간대가 다른 경우 새로운 알림 배너가 프로젝트 양식에 추가되었습니다.

- Sales

  - 수정: 비용 추정 범주 검색을 사용하여 중복 항목을 필터링할 수 있습니다.
  - 수정: **PluginDomain.ExecuteInTryCatchBlock(..)** 의 코드가 더 이상 예외의 출처를 숨기지 않습니다.
  - 수정: 1000개가 넘는 프로젝트가 있을 때 **견적 라인** 양식의 **프로젝트 조회** 에 더 이상 오류 메시지가 표시되지 않습니다.
  - 수정: 노동 추정 및 비용 추정에 대한 **추정** 표가 이제 올바른 통화 기호를 표시합니다.
  - 수정: 조직이 업데이트 릴리스 14에서 업데이트 릴리스 15로 PSA를 업데이트하면 더 이상 **프로젝트** 양식에 **일정** 탭이 공백으로 나타나지 않습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
