---
title: Project Service Automation 버전 3.x 웨이브 1 2020의 새로운 내용 또는 변경 내용
description: 이 항목에서는 Project Service Automation 버전 3 웨이브 1 2020의 새로운 사항과 변경된 내용에 대한 정보를 제공합니다.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079998"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Project Service Automation 버전 3 웨이브 1 2020의 새로운 내용 또는 변경 내용
이 항목에서는 PSA(Project Service Automation) 버전 3.x wave 1 2020의 최신 릴리스로 이동할 때 주요 업그레이드 고려 사항을 강조합니다.

## <a name="time-entry"></a>시간 항목
더 많은 고객 시나리오로 시간 항목을 확장할 수 있는 기능을 제공하기 위해 시간 항목 경험이 확장되었습니다. 여기에는 필드 스키마 이름 **시간 항목 설정** 을 기반으로 **시간 원본** 으로 표시되는 특정 동작을 유도하는 항목 유형을 추가하는 기능이 포함됩니다. 이 기능을 지원하기 위해 시간, 비용, 상태 및 승인(TESA)이라는 새로운 솔루션이 추가되었습니다.

### <a name="upgrade-consideration"></a>업그레이드 고려 사항
이 기능을 지원하기 위해 PSA 내의 역할이 새로운 권한을 포함하도록 업데이트되었습니다. 이러한 권한은 새로운 엔터티 **시간 항목 설정** 에 대한 읽기 액세스 권한을 부여합니다.

시간을 기록하는 기능이 필요한 사용자에게는 기존 역할 외에 사용자 역할 **시간 항목 사용자** 가 부여되어야 합니다. 이 역할에는 새로운 기능이 포함되며 시간 항목은 계속 작동합니다.

또한 시간 입력 엔터티에 대한 모든 양식을 포함하는 사용자 지정 앱 모듈이 있는 경우 모듈에서 **TESA 시간 항목 빨리 만들기 양식** 을 제거해야 합니다.

### <a name="currently-extended-time-entry-changes"></a>현재 확장된 시간 항목 변경 사항
현재 시간 항목 사용자에게 미치는 영향을 최소화하기 위해 이 역할 변경은 시간 항목을 계속 사용하는 데 필요한 유일한 핵심 요구 사항입니다. 사용자 지정 보기나 별도의 시간 항목 경험을 를 작성한 경우 **시간 항목 설정** 필드를 올바른 PSA 값으로 설정해야 합니다.
