---
title: Project Service Automation 업데이트 릴리스 18, V3의 새로운 기능 또는 변경된 기능
description: 이 문서에는 Project Service Automation 업데이트 릴리스 18, V3에서 사용할 수 있는 기능과 수정 사항이 나와 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918872"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation 업데이트 릴리스 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation V3, 업데이트 릴리스 18의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.8.12이며 일반적으로 2020년 4월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-18"></a>업데이트 릴리스 18

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

- 수정됨: **리콜**, **요청** 및 **승인 취소** 플로우에서 명확하지 않은 오류 메시지와 함께 예외가 발생합니다.
- 수정됨: 비용 때문에 **승인 취소** 가 실패하면 관련 예외 오류가 발생하지 않습니다.
- 수정됨: 10월 일광 절약 시간제(DST) 전환 후 호주의 시간 입력 그리드가 휴무일을 잘못 처리합니다.
- 수정됨: 기본 논리가 잘못되면 경비 제출이 금지됩니다.
- 수정됨: 시간 입력 승인에 실패하면 승인 상태가 **대기 중** 으로 유지됩니다.
- 수정됨: 대량 승인시 SQL 오류(교착 상태/시간 초과).
- 수정됨: 시간 입력을 승인하는 동안 팀 구성원을 업데이트하여 발생하는 사용자 경험의 중요한 성능 문제.

**프로젝트 관리**

- 수정됨: 표준 시간대 알림이 **조정** 보기에서 **프로젝트** 기본 양식으로 이동되었습니다.
- 수정됨: 새 프로젝트 양식을 열 때 일정 템플릿이 기본적으로 올바르게 설정되지 않습니다.
- 수정됨: Chromium 기반 브라우저의 경우 사용자가 삭제할 선행 작업을 쉽게 선택할 수 없습니다.
- 수정됨: **빈 템플릿에서 프로젝트** 작성 또는 복사가 관련 없는 할당을 가져옵니다.
- 수정됨: 특정 에지의 경우 작업 그리드에서 새 할당을 생성하면 중복 레코드가 생성됩니다.
- 수정됨: 수동 모드에서 사용자는 작업 시작 날짜를 현재 저장된 날짜보다 늦게 업데이트 할 수 없습니다.

**리소스 관리**

- 수정됨: **조정** 보기 소계 행이 예약 연장 후 예약 차이를 잘못 계산합니다.
- 수정됨: **조정** 보기가 예약 가능한 리소스에 프로젝트 일정과 일치하지 않는 일정이 있으면 리소스 할당을 잘못 표시합니다.

**Sales**

- 수정됨: 시간 항목이 다시 승인될 때( **승인 > 취소 >** 다시 승인), 청구 가능하지 않은 실제의 사본이 생성됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
