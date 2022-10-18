---
title: Project Service Automation에서 Project Operations로의 프로젝트 일정 전환 프로세스
description: 이 문서에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Project Operations로 변경된 기능에 대한 개요를 제공합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642577"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation에서 Project Operations로의 프로젝트 일정 전환 프로세스

프로젝트가 Microsoft Dynamics 365 Project Service Automation 3.X에서 Dynamics 365 Project Operations Lite로 성공적으로 업그레이드된 후에는 작업 표 WBS(작업 분할 구조)에서 프로젝트 작업을 편집할 수 없습니다. 고객은 작업과 관련된 모든 세부 정보를 제공하기 위해 새 필드가 추가된 추적 그리드에서 WBS를 검토할 수 있습니다. WBS에 대한 편집이 필요한 프로젝트의 경우 적격한 프로젝트를 새로운 Project for the web 일정 환경으로 선택적으로 변환할 수 있습니다.

## <a name="project-conversion-process"></a>프로젝트 변환 프로세스

프로젝트를 변환하려면 다음 단계를 따르세요.

1. 프로젝트의 메인 페이지를 열고 작업 창에서 **변환** 을 선택합니다.
1. 확인 메시지 상자에서 **확인** 을 선택하여 프로젝트 변환을 시작합니다. 다음 작업이 발생합니다.

    1. 프로젝트 메인 페이지에 나타나는 메시지 표시줄에는 "프로젝트 일정이 변환되고 있습니다. 변환이 완료될 때까지 프로젝트를 변경할 수 없습니다."가 표시됩니다
    1. 프로젝트 목록으로 리디렉션됩니다.

    프로젝트 변환이 완료된 후 다음 작업이 발생합니다.

    1. 할당된 프로젝트 관리자는 애플리케이션 오른쪽에서 알림을 받습니다.
    1. 변환이 진행 중임을 나타내는 메시지 표시줄이 제거됩니다.
    1. **일정** 탭은 Project for the Web의 새로운 예약 환경을 보여줍니다. 적절한 라이선스와 보안 역할이 있는 모든 사용자는 WBS를 편집할 수 있습니다.
    1. **예약 엔진** 필드가 **Project for the web** 으로 업데이트되었습니다.
    1. **변환** 버튼이 작업 창에서 제거됩니다.

> [!IMPORTANT]
> 프로젝트의 대량 변환은 허용되지 않습니다. 동시에 많은 양의 프로젝트를 업데이트하려는 모든 시도는 제한됩니다. 이 제한은 모든 고객에게 고성능을 보장하는 데 도움이 됩니다.

## <a name="manual-tasks-vs-automatic-tasks"></a>수동 작업 대 자동 작업

환경이 Project Service Automation에서 Project Operations로 업그레이드되면 WBS의 모든 작업이 자동으로 예약된 것으로 간주됩니다. Project for the web에서는 수동으로 예약된 작업의 개념을 사용할 수 없습니다. 그러나 새 프로젝트를 생성할 때 [예약 모드](/project-management/scheduling-modes.md) 설정을 사용하여 프로젝트에 대한 선호하는 일정 동작을 정의할 수 있습니다.

## <a name="restricted-operations-for-pre-conversion-projects"></a>변환 전 프로젝트의 제한된 작업

이 섹션에서는 프로젝트가 변환되지 않았을 때 예상할 수 있는 기능적 차이점에 대해 간략하게 설명합니다.

### <a name="copy-project"></a>프로젝트 복사

**복사** 작업은 변환된 프로젝트에서만 지원됩니다. 업그레이드된 프로젝트는 변환 전에 복사할 수 없습니다.

### <a name="move-project"></a>프로젝트 이동

프로젝트 시작 날짜를 변경해도 프로젝트가 변환되지 않는 한 작업 시작이 비례적으로 이동하지 않습니다.

## <a name="frequently-asked-questions"></a>자주 묻는 질문

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>변환된 프로젝트와 업그레이드가 완료된 후 생성되는 새 프로젝트의 차이점은 무엇입니까?

환경이 업그레이드된 후 변환된 프로젝트의 경우 일정이 프로젝트 일정만 따르도록 지시하는 플래그가 설정됩니다. 이 동작은 Project Service Automation의 동작과 일치합니다. 그러나 업그레이드 후에 생성된 새 프로젝트에는 플래그가 설정되지 않습니다. 따라서 일정은 작업에 할당된 리소스의 작업 시간을 따릅니다.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>내 프로젝트가 변환되지 않으면 어떻게 해야 합니까?

프로젝트 변환에 실패한 경우 첫 번째 단계는 오류 로그를 검토하여 WBS와 관련된 일반적인 문제를 식별하는 것입니다. 로그에 조치를 취할 수 있는 특정 오류가 표시되지 않으면 고객 지원에 문의하여 케이스를 추가로 검토할 수 있습니다.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Project for the web에서 비즈니스 종료는 어떻게 처리되나요?

Project for the web은 기업이 조직 수준에서 정의하는 비즈니스 종료를 존중하지 않습니다. 그러나 주어진 근무 시간 템플릿에 정의된 다른 유형의 휴무일을 존중합니다.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the web의 제한 사항은 무엇입니까?

[작업 분할 구조 만들기: 프로젝트 제한 사항](/project-management/create-wbs#project-limitations.md)을 참조하십시오.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>비용 및 판매 추정치가 변경될 수 있습니까?

리소스 할당 등고선이 다시 계산되거나 원본 프로젝트와 다른 날짜 경계에 있는 경우는 드물지만 매출과 비용 추정치에 차이가 있을 수 있습니다. 업그레이드 프로세스의 일부로 고객은 잠재적인 일정 변경 사항을 이해할 수 있도록 대표적인 샘플 프로젝트 세트를 테스트해야 합니다.
