---
title: Project Service Automation 업데이트 릴리스 33, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 33, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334566"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Project Service Automation 업데이트 릴리스 33, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 33에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.54.98이며 일반적으로 2021년 7월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-33"></a>업데이트 릴리스 33

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- 두 개의 잠긴 필드, **msdyn_description** 과 **msdyn_externaldescription** 은 제출 후 수정 가능합니다.
- 프로젝트와 관련이 없는 경비가 생성되면 오류 메시지가 발생합니다.
- 시간 항목이 생성되면 리소스 역할은 기본적으로 비활성 역할로 설정됩니다.
- 회수 및 삭제된 경비와 연결된 분개장 항목은 삭제되지 않습니다.
- **시간 항목 빨리 만들기 양식** 에서 **프로젝트 작업 목록** 보기를 업데이트하여 기본적으로 표시되는 날짜를 작업 시작 날짜로 변경합니다.
- 예약 가능한 리소스의 **관련 항목** 탭에서 시간 항목을 만들 때 상위 예약 가능한 리소스 대신 로그인한 사용자에 대해 시간 항목이 잘못 생성됩니다.
- **일괄 승인 MDD** 대화 상자에 새로운 필드가 추가됩니다.

**프로젝트 계획**

다음과 같은 문제가 해결되었습니다.
- 복잡한 달력과 함께 프로젝트 작업 시간 템플릿을 적용하면 프로젝트 생성 성능이 느려집니다.
- 시작 날짜가 종료 날짜보다 큰 경우 각 필드의 시간 구성 요소가 다르기 때문에 복사 프로젝트 템플릿에 오류가 표시됩니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.
- 리소스 활용 쿼리에 잘못된 매개변수가 사용되어 **리소스 활용** 그리드에 XML이 잘못된 필터 결과를 가져옵니다.
- **예약 연장** 확인에 잘못된 예약 종료 날짜가 표시됩니다.

**판매**

다음과 같은 문제가 해결되었습니다.
- 누락된 값으로 범주 가격을 생성하면 오류 메시지가 발생합니다.
- 주문 라인 없이 계약 내용 중요 시점이 생성되면 오류 메시지가 발생합니다.
