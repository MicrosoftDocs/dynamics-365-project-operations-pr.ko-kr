---
title: Project Service Automation 업데이트 릴리스 37, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 37, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593482"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Project Service Automation 업데이트 릴리스 37, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 37, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.58.120이며 2021년 11월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-37"></a>업데이트 릴리스 37

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**시간 및 경비**
- 사용자는 셀을 지워서 시간 항목을 삭제할 수 없습니다.
- **내 승인 실패** 보기에는 **제출됨** 상태의 프로젝트 승인만 포함됩니다.

**프로젝트 관리**
- 프로젝트 팀 구성원의 위치 이름이 비어 있는 경우 사용자가 Microsoft 데스크톱 추가 기능에서 프로젝트를 열 때 null 참조 예외 오류를 수신합니다.
- **프로젝트 작업** 페이지에 **저장** 버튼이 없으므로 사용자가 작업 레코드에 대한 변경 사항을 저장할 수 없습니다.
- 사용자는 **성공** 상태의 견적과 연결된 작업이 있는 프로젝트를 삭제할 수 없습니다.

**판매**
- **프로젝트** 페이지의 **통화** 필드는 적용된 템플릿의 통화와 일치하도록 업데이트됩니다.
- 여러 통화가 있는 작업에서 비용이 잘못 계산됩니다.
