---
title: 작업 시간 템플릿 만들기
description: 이 문서에서는 Project Service에서 근무 시간 템플릿을 만드는 방법을 설명합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916066"
---
# <a name="create-a-work-hours-template-project-service"></a>작업 시간 서식 파일 만들기(Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

프로젝트를 만들고 관리하려면 프로젝트에 일정 템플릿을 적용해야 합니다. 일정 템플릿은 다음 프로젝트 속성을 정의합니다.

- 시작 및 종료 시간을 포함한 근무 시간
- 근무일
- 휴무일과 같은 일정 예외

프로젝트에 적용되는 일정 템플릿은 조직의 설정에 정의된 캘린더 템플릿의 복사본입니다.

> [!NOTE]
> 일정 템플릿을 변경하면 해당 변경 사항이 프로젝트의 작업 시간에 적용되지 않습니다. 프로젝트의 근무 시간을 변경하려면 새 템플릿을 적용해야 합니다.

조직의 일정 템플릿을 만들려면 두 가지 주요 요구 사항이 있습니다.

- 예약 가능한 신규 또는 기존 리소스를 사용하여 템플릿의 원하는 근무 시간을 정의합니다.
- 새 일정 템플릿을 만들고 템플릿을 예약 가능한 리소스와 연결합니다.

**템플릿의 근무 시간 정의**

1. **리소스** \> **리소스** 로 이동합니다.
2. 일정 템플릿에서 참조할 새 리소스를 만들거나 기존 리소스를 선택합니다.
3. 리소스의 **작업 시간** 탭을 선택하고 [리소스에 대한 작업 시간 설정](/dynamics365/field-service/set-work-hours-resource)의 지침을 완료하여 일정 규칙을 구성합니다.

**새 일정 템플릿 만들기**

1. **설정** \> **일정 템플릿** 으로 이동합니다.
2. **새로 만들기** 를 클릭하고 이름, 설명 및 템플릿 리소스를 입력합니다.


> [!NOTE]
> 일정 템플릿에서 리소스가 참조되면 리소스 일정의 복사본이 일정 템플릿과 연결됩니다. 복사된 템플릿의 근무 시간이 변경되면 해당 변경 사항이 일정 템플릿에 적용되지 않습니다.


### <a name="see-also"></a>참고 항목  
 [리소스 설정](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
