---
title: Project Service Automation 업데이트 릴리스 41, V3의 새로운 기능 또는 변경된 기능
description: 이 문서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 41, V3에서 사용할 수 있는 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930556"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Project Service Automation 업데이트 릴리스 41, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation 업데이트 릴리스 41, V3의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.62.162이며 2022년 3월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-41"></a>업데이트 릴리스 41

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**프로젝트 관리**
- 데스크톱 추가 기능에서 만든 프로젝트를 기반으로 하는 템플릿에서 프로젝트를 만들려고 하면 다음 오류가 표시됩니다. "리소스 할당의 계획된 작업 필드 유효성 검사: 각 리소스 할당 시간 조각의 종료 날짜는 시작 날짜보다 이전일 수 없습니다".

**시간 및 경비**
- 시간 항목을 삭제하려고 하면 "ISV 코드에서 예기치 않은 오류가 발생했습니다"라는 오류 메시지가 표시됩니다.

**판매**
- 고정 가격 마일스톤에 대한 송장을 생성하면 **설명** 및 **외부 설명** 필드가 채워지지 않습니다. 
