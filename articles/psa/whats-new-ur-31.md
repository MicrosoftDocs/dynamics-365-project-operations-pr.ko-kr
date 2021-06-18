---
title: Project Service Automation 업데이트 릴리스 31, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 31, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999139"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Project Service Automation 업데이트 릴리스 31, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 31에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.52.77이며 일반적으로 2021년 5월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-31"></a>업데이트 릴리스 31

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- **예약 가능한 리소스** 페이지의 시간 입력 제어 명령 버튼이 혼란스러웠습니다.
- 시간 입력을 승인할 때 **Project.SetTrackingFields** 에서 null 참조 예외가 생성되었습니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.

- **팀 구성원 만들기** 가 **기본 예약 커밋 상태** 에 대한 예약 설정 메타데이터 설정을 올바르게 표시하지 않습니다.
- PSA 1.X에서 3.X로 업그레이드할 때 **UpgradeResourceRequirements** 에서 업그레이드 프로세스가 실패합니다.


**판매**

다음과 같은 문제가 해결되었습니다.

- 실제 수익은 금액을 추적 그리드의 프로젝트 통화로 변환합니다.
- 조직의 기준 통화가 프로젝트 통화와 다른 시나리오에서 분개 라인, 견적 라인 및 계약 내용을 생성할 때 통화 기본값이 명확하지 않습니다.
- **보류 중인 수정 분개장 유효성 검사** 쿼리는 프로젝트별로 필터링되지 않습니다.
- 프로젝트에서 남은 판매가 잘못 계산됩니다.
- 연락처를 기반으로 한 견적은 가격 목록 없이 생성된 경우 실패합니다.
- **송장 확인** 을 선택할 때 처리 스피너가 표시되지 않습니다.
- **송장 만들기** 를 선택할 때 처리 스피너가 표시되지 않습니다.
- 분실로 견적을 닫아도 예약이 취소되지 않습니다.







