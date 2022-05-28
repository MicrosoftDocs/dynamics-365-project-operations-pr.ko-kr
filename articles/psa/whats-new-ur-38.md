---
title: Project Service Automation 업데이트 릴리스 38, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 38, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598726"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation 업데이트 릴리스 38, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 38, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.59.117이며 일반적으로 2021년 12월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-38"></a>업데이트 릴리스 38

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**시간 및 경비**

- 승인 집합 로그의 길이가 100,000 레코드를 초과하는 경우 예외가 발생합니다.
- 사용자는 **시간 항목** 기본 페이지에서 **시간 항목** 그리드에 액세스할 수 없습니다.
- 가져올 수 있는 항목이 없으면 **시간 항목 가져오기** 대화 상자에 텍스트가 표시되지 않습니다.
- 사용자는 **대상 상태** 필드가 **알 수 없음** 으로 설정된 승인 집합을 생성할 수 있습니다.

**프로젝트 관리**

- 일광 절약 시간제가 시작될 때 UTC(+09:30) 및 UTC(+10:00)에 대한 리소스 할당에 윤곽선이 올바르게 표시되지 않습니다.
- 작업 분할 구조에 대한 **추가 열** 필드는 일부 로케일에서 숨겨져 있습니다.
- **프로젝트 작업** 그리드의 달력 컨트롤에 대한 날짜 선택기가 중국어로 올바르게 지역화되지 않았습니다.

**판매**

- 계약 단위 및 통화가 다른 예약 가능한 자원이 시간 항목을 제출할 때 **계약 성과** 및 **프로젝트 실제 비용** 값이 일치하지 않습니다.
- 송장을 관리형 솔루션로 가져올 때 송장을 자동으로 확인하는 사용자 지정 워크플로가 실패합니다. 다음 메시지가 표시됩니다. "Microsoft.Xrm.Sdk.InvalidPluginExecutionException 메시지: 잘못된 송장 상태입니다."
- **루트** 가 요약 옵션으로 선택되고 프로젝트에 혼합된 트랜잭션 클래스의 견적(예: 시간, 비용 및 자재 견적의 조합)이 있는 경우 시스템은 트랜잭션 클래스 전체를 단일 수수료 라인으로 요약합니다.
- 계약 내용이 프로젝트와 연결되기 전에 경비 라인이 추가되는 시나리오에서는 **가격 업데이트** 필드에 올바른 가격이 기본값으로 입력되지 않습니다.
- 음수 판매 금액은 **프로젝트** 및 **작업** 엔터티에 허용되지 않습니다.
