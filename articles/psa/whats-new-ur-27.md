---
title: Project Service Automation 업데이트 릴리스 27, V3의 새로운 기능 또는 변경된 기능
description: 이 문서에는 Project Service Automation 업데이트 릴리스 27, V3에서 사용할 수 있는 기능과 수정 사항이 나와 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912938"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Project Service Automation 업데이트 릴리스 27, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 문서에는 Project Service Automation V3, 업데이트 릴리스 27의 새로운 기능과 수정 사항이 나와 있습니다. 이 버전의 빌드 번호는 V3.10.45.98이며 2021년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-27"></a>업데이트 릴리스 27

### <a name="bug-fixes"></a>버그 수정

**일반**

다음과 같은 문제가 해결되었습니다.

- Project Service Automation의 플러그인에서 생성된 로그가 자동 삭제로 설정되지 않았습니다.
- Project Service Automation 솔루션에 레거시 null NavBarArea 및 제목 요소가 포함되어 있으므로 자동 업그레이드가 실패합니다.

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- **시간 입력** 그리드에 **표준 시간대 독립** 날짜 동작에 대해 잘못된 데이터가 표시됩니다.
- **시간 입력** 그리드가 **표준 시간대 독립** 날짜 동작에 대해 잘못된 시간을 생성합니다.
- 작업 조회는 **시간 입력 편집** 페이지에서 선택한 프로젝트로 제한되지 않습니다.
- 시스템이 프로젝트 승인자를 찾고 있기 때문에 비 프로젝트 시간 항목에 대한 시간 승인이 차단됩니다.
- 실제의 올바른 항목은 잘못된 오류 메시지를 표시합니다.
- 작업에 실제 비용에 대한 Null 값이 포함되어 있고 프로젝트 합계가 새로 고쳐지면 "지정된 키가 사전에 없습니다."라는 오류가 발생합니다.
- 특정한 경우에 **프로젝트 추정** 탭의 **그룹화 기준** 필터에 추정 경비가 표시되지 않습니다.
- **일광 절약 시간** 간격이 시간 항목에 대해 올바르지 않습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- **프로젝트** 페이지 로드와 관련된 성능을 향상시키는 캐시 개선.
- 프로젝트 작업이 완료되지 못하게 하는 오래된 비즈니스 규칙.
- Microsoft Project 추가 기능 윤곽이 추가 기능의 일정을 따르지 않아 리소스 요구 사항이 잘못되었습니다.
- 템플릿에서 프로젝트를 만들면 할당 날짜가 잘못 설정되고 리소스 요구 사항을 생성할 수 없습니다.
- 사용자가 키보드를 사용하여 **범주**, **기술**, **상태** 옵션에 액세스할 수 없습니다.
- 프로젝트의 실제 판매액에는 수수료 및 재료 판매액이 포함되어 있지 않습니다.
- 실제 판매와 실제 비용을 집계한 결과, 환율이 서로 다른 경우 잘못된 결과가 발생합니다.
- **기본 근무 시간 템플릿** 의 설명이 오해의 소지가 있습니다.
- 작업을 들여쓰기 해도 새로 고칠 때까지 사용자 인터페이스에서 **범주** 가 제거되지 않습니다.
- 종료일 이후로 프로젝트를 이동하도록 확인하는 누락은 허용되지 않습니다.

**Sales**

다음과 같은 문제가 해결되었습니다.

- 프로젝트가 선택되지 않은 경우 **프로젝트 평가에서 가져오기** 가 표시되므로 프로젝트 견적 라인에서 null 참조 예외가 생성됩니다.
- 견적을 **성공** 으로 마감하면 "개체 참조가 개체의 인스턴스로 설정되지 않았습니다."라는 오류가 발생합니다.
- 계약 내용에서 프로젝트 연결을 해제하는 동안 조정 상태는 실제 취소 중에 설정되지 않습니다.
- Dynamics 365 Field Service 및 Project Service Automation이 모두 설치된 경우 **가격 산정 잠금** 및 **현재 가격 산정 사용** 옵션이 **송장** 페이지에 동시에 표시되지 않습니다.
- 일본어의 경우 다른 달력 기반 페이지와 일치하지 않는 번역이 있습니다.
- **활성화** 및 **비활성화** 가 Project Service Automation에 있는 **가격표 연결** 엔터티에서 제거되었습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
