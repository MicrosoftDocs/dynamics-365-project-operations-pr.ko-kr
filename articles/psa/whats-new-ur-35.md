---
title: Project Service Automation 업데이트 릴리스 35, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 35, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574036"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Project Service Automation 업데이트 릴리스 35, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 35, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.56.110이며 일반적으로 2021년 9월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-35"></a>업데이트 릴리스 35

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**시간 및 경비**

- 프로젝트 승인자는 **프로젝트 승인자** 역할을 사용하여 경비 입력을 승인할 때 읽기 권한 오류를 받습니다.
- 프로젝트 승인자는 **프로젝트 승인자** 역할을 사용하여 승인된 시간 입력을 취소할 때 **msdyn_projectapproval** 에서 쓰기 권한 오류를 받습니다.
- 전화기 - 프로젝트 리소스 허브 앱 모듈을 위한 Dynamics 365의 시간 항목에서 **주 복사** 를 선택하면 다음 오류가 발생합합니다. "...\OfficeProductivity_RibbonRules.js.map: HTTP 오류: 상태 코드 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- **다시 시도** 정책은 이전에 거부된 항목을 자동으로 승인합니다.
- **승인 집합** 하위 그리드는 적용할 수 없는 리본 동작을 보여줍니다.
- **시간 입력** 엔터티에 **프로젝트 작업** 및 **리소스 역할** 에 대한 아이콘이 없습니다.
- 리소스 할당을 가져올 때 가져온 시간 항목에는 수동 모드 작업을 통해 생성된 할당에 대한 올바른 기간이 없습니다.
- **삭제** 가 **시간 입력 레코드에 대한 고급 찾기** 페이지에서 누락되었습니다.
- **저장** 이 **시간 입력 정보** 페이지에서 누락되었습니다. 이 문제로 인해 페이지를 닫을 때 변경 사항이 저장되지 않습니다.

**프로젝트 계획**

- **리소스 할당** 및 **리소스 조정** 그리드는 그룹화된 속성을 사전순으로 정렬하지 않습니다.
- 날짜 동작이 **날짜만** 으로 사용자 정의된 경우 작업을 만들 수 없습니다.

**리소스 관리**

- Dynamics 365 Field Service 및 Project Service Automation이 설치된 경우 **리소스 요구 사항 관련 보기** 메인 페이지와 연결되어 있을 때 중첩 문제가 발생합니다.
- **팀 구성원의 빨리 만들기** 대화 상자에서 **저장** 을 두 번 클릭하면 리소스 요구 사항이 생성되지 않습니다.

**판매**

- 상태가 **성공** 인 견적과 연결된 작업을 삭제하면 예외가 발생합니다.
