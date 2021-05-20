---
title: Project Service Automation 업데이트 릴리스 14, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 14 V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949395"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation 업데이트 릴리스 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 PSA V3, 업데이트 릴리스 14에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.4.21이며 다음 일정으로 일반적으로 제공됩니다.

- **일반 가용성(자체 업데이트):** 2020년 1월
- **자동 업데이트:** 2020년 2월

## <a name="update-release-14"></a>업데이트 릴리스 14

### <a name="enhancements"></a>향상된 기능

- Sales

     - 견적이 **성공으로 종료** 로 업데이트될 때 **견적 라인 세부 정보** 의 사용자 지정 필드 값이 **프로젝트 계약 내용 세부 정보** 에 복사됩니다.
     - 확인된 프로젝트가 **실패로 종료** 일 수 있습니다.

- 리소스 관리

     - 예약을 확장하면 예약 결과를 요약하고 예약 유지 링크를 제공하는 확인 대화 상자가 표시됩니다.


### <a name="bug-fixes"></a>버그 수정

- 시간 및 경비

     - 수정: 사용자가 수정할 항목을 선택하지 않은 경우 사용자 환경이 향상되었습니다.

- 리소스 관리

     - 수정: 리소스를 여러 번 예약하면 예약 가능한 리소스 이름이 오버플로됩니다.

- Sales

     - 수정: 사용자가 프로젝트의 비용 견적에 대한 비용 가격을 입력할 때까지 총 판매 가격이 계산되지 않습니다.
     - 수정: 관련 프로젝트 계약이 **초안** 상태가 아닌 경우 견적을 **성공** 으로 종료하는 것에 실패합니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]