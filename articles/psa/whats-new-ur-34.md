---
title: Project Service Automation 업데이트 릴리스 34, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 34, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323289"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Project Service Automation 업데이트 릴리스 34, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 34에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.55.38이며 일반적으로 2021년 7월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-34"></a>업데이트 릴리스 34

### <a name="bug-fixes"></a>버그 수정
다음과 같은 문제가 해결되었습니다.

**일반**

- 게시자 기반 업데이트는 새로운 최신 승인 워크플로를 활성화하지 않습니다.
- **대상 상태** 및 **작업 유형** 특성이 **승인 집합** 메인 페이지에 누락되었습니다.

**시간 및 경비**

- 최신 승인 흐름을 사용하여 회수 요청을 승인할 수 없습니다.
- 로그인한 사용자와 관련이 없는 항목을 복사할 때 1주일의 시간 항목 복사가 작동하지 않습니다.

**프로젝트 계획**

- Microsoft Project 데스크톱 추가 기능에서 가져올 때 리소스 할당 윤곽이 손상되었습니다.

**리소스 관리**

- Microsoft Project 데스크톱 클라이언트 추가 기능에서 프로젝트를 게시하면 기존 요구 사항의 종료 날짜가 변경됩니다.
- 예약 연장 확인 대화 상자에서 소수점 이하 자릿수가 소수점 이하 두 자리를 초과합니다.

**판매**

- 기존 제품이 있는 제품 기반 라인을 프로젝트 계약에 추가하면 **사전에서 키를 찾을 수 없음** 예외가 표시됩니다.
- 주문 유형이 잠재 고객에서 영업 기회로 매핑되는 경우 잠재 고객을 우량으로 선별할 수 없습니다.
