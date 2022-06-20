---
title: Project Service Automation에서 Project Operations로 업그레이드
description: 이 문서에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Project Operations로 업그레이드하는 프로세스에 대한 개요를 제공합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912984"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation에서 Project Operations로 업그레이드

Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Project Operations로 업그레이드를 위한 3단계 중 첫 번째 단계를 발표하게 된 것을 기쁘게 생각합니다. 이 문서는 이 흥미진진한 여정을 시작하는 고객을 위한 개요를 제공합니다. 향후 문서에는 개발자 고려 사항 및 기능 향상에 대한 세부 정보가 포함됩니다. Project Operations로의 업그레이드를 준비하는 데 도움이 되는 지침을 제공할 뿐만 아니라 업그레이드 후 기대할 수 있는 사항도 설명합니다.

업그레이드 제공 프로그램은 세 단계로 나뉩니다.

| 업그레이드 전달 | 1단계(2022년 1월) | 2단계(2022년 4월 웨이브) | 3단계  |
|------------------|------------------------|---------------------------|---------------------------|
| 프로젝트의 작업 분할 구조(WBS)에 대한 종속성 없음 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 현재 지원되는 Project Operations 한도 내 WBS | | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client에 대한 지원을 포함하여 현재 지원되는 Project Operations 한도를 벗어난 WBS | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>업그레이드 프로세스 기능 

업그레이드 프로세스의 일부로 관리자가 오류를 보다 쉽게 진단할 수 있도록 사이트 맵에 업그레이드 로그를 추가했습니다. 새 인터페이스 외에도 업그레이드 후 데이터 무결성을 보장하기 위해 새 유효성 검사 규칙이 추가됩니다. 다음 유효성 검사가 업그레이드 프로세스에 추가됩니다.

| 유효성 검사 | 1단계(2022년 1월) | 2단계(2022년 4월 웨이브) | 3단계  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS는 일반적인 데이터 무결성 위반(예: 동일한 상위 작업과 연결되지만 상위 프로젝트가 다른 리소스 할당)에 대해 검증됩니다. | | :heavy_check_mark: | :heavy_check_mark: |
| WBS는 [Project for the Web의 알려진 제한 사항](/project-for-the-web/project-for-the-web-limits-and-boundaries)에 대한 유효성을 검증합니다. | | :heavy_check_mark: | :heavy_check_mark: |
| WBS는 Project Desktop Client의 알려진 제한 사항에 대한 유효성을 검증합니다. | |  | :heavy_check_mark: |
| 예약 가능한 리소스 및 프로젝트 캘린더는 일반적으로 호환되지 않는 캘린더 규칙 예외에 대해 평가됩니다. | | :heavy_check_mark: | :heavy_check_mark: |

2단계에서 Project Operations로 업그레이드하는 고객은 기존 프로젝트를 프로젝트 계획을 위한 읽기 전용 환경으로 업그레이드하게 됩니다. 이 읽기 전용 환경에서는 전체 WBS가 추적 그리드에 표시됩니다. WBS를 편집하기 위해 프로젝트 관리자는 기본 **프로젝트** 페이지에서 **변환** 을 선택할 수 있습니다. 그러면 백그라운드 프로세스가 프로젝트를 업데이트하여 Project for the Web의 새 프로젝트 일정 환경을 지원합니다. 이 단계는 [Project for the Web의 알려진 제한 사항](/project-for-the-web/project-for-the-web-limits-and-boundaries)에 맞는 프로젝트가 있는 고객에게 적합합니다.

3단계에서는 해당 응용 프로그램에서 프로젝트를 계속 편집하려는 고객을 위해 Project Desktop Client에 대한 지원이 추가됩니다. 그러나 기존 프로젝트가 새 Project for the Web 환경으로 변환되는 경우 변환된 각 프로젝트에 대해 추가 기능에 대한 액세스가 비활성화됩니다.

## <a name="prerequisites"></a>필수 항목

1단계 업그레이드 자격을 얻으려면 고객은 다음 기준을 충족해야 합니다.

- 대상 환경은 **msdyn_projecttask** 엔터티의 레코드를 포함하지 않아야 합니다.
- 유효한 Project Operations 라이선스는 고객의 모든 활성 사용자에게 할당되어야 합니다. 
- 고객은 프로덕션 데이터와 일치하는 대표 데이터 세트가 있는 하나 이상의 비프로덕션 환경에서 업그레이드 프로세스를 검증해야 합니다.
- 대상 환경은 Project Service Automation 업데이트 릴리스 41 (3.10.62.162) 이상으로 업데이트해야 합니다.

2단계 및 3단계의 전제 조건은 일반 공급 날짜가 가까워지면 업데이트됩니다.

## <a name="licensing"></a>라이선싱

Project Service Automation에 대한 활성 라이선스가 있는 경우 Project Service Automation 등의 모든 기능이 포함된 Project Operations를 설치하고 사용할 수 있습니다. 이러한 방식으로 프로덕션에서 Project Service Automation을 계속 사용하면서 Project Operations의 기능을 테스트할 수 있습니다. Project Service Automation 라이선스가 만료되면 Project Operations로 전환해야 합니다. 이 전환을 계획할 때 Project Operations 라이선스에 Project Service Automation 라이선스가 포함되어 있지 않다는 사실을 고려해야 합니다.

## <a name="testing-and-refactoring-customizations"></a>사용자 정의 테스트 및 리팩토링

시작점으로 모든 사용자 지정을 깨끗한 Project Operations(라이트) 환경으로 가져와 가져오기가 성공하고 비즈니스 작업이 예상대로 작동하는지 확인합니다.

다음은 주의해야 할 사항입니다.

- 누락된 종속성으로 인해 가져오기가 실패할 수 있습니다. 즉, 사용자 지정은 Project Operations에서 제거된 필드 또는 기타 구성 요소를 참조합니다. 이 경우 개발 환경에서 이러한 종속성을 제거하십시오.
- 비관리형 및 관리형 솔루션에 사용자 지정되지 않은 구성 요소가 포함된 경우 솔루션에서 해당 구성 요소를 제거합니다. 예를 들어 **프로젝트** 엔터티를 사용자 정의할 때 엔터티 헤더만 솔루션에 추가하십시오. 모든 필드를 추가하지 마십시오. 이전에 모든 하위 구성 요소를 추가한 경우 새 솔루션을 수동으로 만들고 관련 구성 요소를 추가해야 할 수 있습니다.
- 양식과 보기가 예상대로 나타나지 않을 수 있습니다. 어떤 상황에서는 기본 제공되는 양식이나 보기를 사용자 정의한 경우 사용자 정의로 인해 Project Operations의 새 업데이트가 적용되지 않을 수 있습니다. 이러한 문제를 식별하려면 Project Operations의 새로 설치와 사용자 지정이 포함된 Project Operations의 설치를 나란히 검토하는 것이 좋습니다. 귀사의 비즈니스에서 가장 일반적으로 사용되는 양식을 비교하여 귀하의 양식 버전이 여전히 의미가 있고 양식의 깨끗한 버전에서 누락된 것이 없는지 확인하십시오. 사용자 정의한 보기에 대해 동일한 유형의 병렬 검토를 수행하십시오.
- 비즈니스 로직은 런타임에 실패할 수 있습니다. 플러그인의 필드에 대한 참조는 가져올 때 유효성이 검사되지 않기 때문에 더 이상 존재하지 않는 필드에 대한 참조로 인해 비즈니스 로직이 실패할 수 있으며 다음 예와 유사한 오류 메시지가 나타날 수 있습니다. "'프로젝트' 엔티티에 Name = 'msdyn_plannedhours' 및 NameMapping = 'Logical'인 속성이 없습니다." 이 경우 새 필드를 사용하도록 사용자 정의를 수정하십시오. 플러그인 논리에서 자동으로 생성된 프록시 클래스와 강력한 유형 참조를 사용하는 경우 새로 설치에서 해당 프록시를 재생성하는 것이 좋습니다. 이러한 방식으로 플러그인이 더 이상 사용되지 않는 필드에 의존하는 모든 위치를 쉽게 식별할 수 있습니다.

Project Operations를 완전히 가져오기 위해 사용자 지정을 업데이트한 후 다음 단계로 이동합니다.

## <a name="end-to-end-testing-in-development-environments"></a>개발 환경에서 엔드 투 엔드 테스트

### <a name="initiate-upgrade"></a>업그레이드 시작 

1. Power Platform 관리 센터에서 사용자 환경을 찾아 선택합니다. 그런 다음, 응용 프로그램에서 **Dynamics 365 Project Operations** 를 찾아 선택합니다.
2. **설치** 를 선택하여 업그레이드를 시작합니다. Power Platform 관리 센터는 이 설치를 새 설치로 표시합니다. 그러나 이전 버전의 Project Service Automation이 감지되고 기존 설치가 업그레이드됩니다.

    업그레이드가 완료되면 환경에 Project Operations가 설치되어 있고 Project Service Automation이 설치되지 않은 것으로 표시되어야 합니다.

    > [!NOTE]
    > 환경의 데이터 양에 따라 업그레이드에 몇 시간이 걸릴 수 있습니다. 업그레이드를 관리하는 핵심 팀은 그에 따라 계획을 세우고 업무 시간 외 시간에 업그레이드를 실행해야 합니다. 경우에 따라 데이터 볼륨이 크면 주말에 업그레이드를 실행해야 합니다. 스케줄링에 대한 결정은 낮은 환경에서의 테스트 결과를 기반으로 해야 합니다.

3. 사용자 정의 솔루션을 적절하게 업그레이드하십시오. 이 시점에서 이 문서의 [사용자 지정 테스트 및 리팩토링](#testing-and-refactoring-customizations) 섹션에서 사용자 지정에 대한 변경 사항을 배포합니다.
4. **설정** \> **솔루션** 으로 이동하고 **Project Operations에서 사용되지 않는 구성 요소** 솔루션을 제거하도록 선택합니다.

    이 솔루션은 업그레이드 중에 존재하는 기존 데이터 모델 및 구성 요소를 보유하는 임시 솔루션입니다. 이 솔루션을 제거하면 더 이상 사용되지 않는 모든 필드와 구성 요소가 제거됩니다. 이러한 방식으로 인터페이스를 단순화하고 통합 및 확장을 더 쉽게 만들 수 있습니다.
    
### <a name="validate-common-scenarios"></a>일반적인 시나리오 유효성 검사

특정 사용자 지정을 확인할 때 애플리케이션에서 지원되는 비즈니스 프로세스도 검토하는 것이 좋습니다. 이러한 비즈니스 프로세스에는 견적 및 계약과 같은 판매 엔터티 생성, WBS 및 실제 승인을 포함하는 프로젝트 생성이 포함되지만 이에 국한되지 않습니다.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation과 Project Operations 간의 주요 변경 사항

이 섹션에서는 Project Service Automation과 Project Operations 간에 예상할 수 있는 주요 변경 사항에 대한 요약을 제공합니다.

### <a name="project-planning"></a>프로젝트 계획

Project Operations의 프로젝트 계획 기능은 더 이상 클라이언트 측 논리와 서버 측 논리의 조합에 의존하지 않습니다. 대신 Project Operations는 Project for the Web을 일정 엔진으로 사용합니다. 일정 기능의 이러한 변경으로 인해 Board 및 Gantt 보기, 리소스 기반 계획, [작업 체크리스트 항목](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) 및 프로젝트 일정 모드와 같은 몇 가지 새로운 기능이 가능해졌습니다. 새로운 예약 기능은 새로운 [API(응용 프로그래밍 인터페이스)](../project-management/schedule-api-preview.md)의 풍부한 집합에서도 지원됩니다. 이러한 API는 WBS에서 엔터티를 생성, 업데이트 또는 삭제하기 위한 프로그래밍 방식 작업이 일정의 계산된 필드를 손상시키지 않도록 하기 위한 것입니다.

## <a name="billing-and-pricing"></a>청구 및 가격 책정

Project Operations에 대한 지속적인 투자의 일환으로 청구 및 가격 책정에서 몇 가지 새로운 기능을 사용할 수 있습니다. 다음 몇 가지 예를 참조하십시오.

- [프로젝트 및 프로젝트 작업에 대한 재료 사용량 기록](../material/material-usage-log.md)
- [하도급 계약 관리](../pro/subcontracting/managing-subcontracts-overview.md)
- [선급금 및 보유자 기반 계약](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [초과하지 않는 상태 및 유효성 검사 계약](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- 작업 기반 청구

## <a name="frequently-asked-questions"></a>자주 묻는 질문

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>현재 업그레이드가 지원되는 배포 유형은 무엇입니까?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations 라이트 배포                        | 지원됨               |
| Dynamics 365 Finance 프로젝트 관리 및 회계 | Project Operations 라이트 배포                        | 현재 지원되지 않음 |
| Finance 프로젝트 관리 및 회계              | 리소스/비 재고 시나리오에 대한 Project Operations     | 현재 지원되지 않음 |
| Project Service Automation 3.x                         | 리소스/비 재고 시나리오에 대한 Project Operations     | 현재 지원되지 않음 |
| Project for the Web(전용 환경)            | Project Operations 라이트 배포                        | 현재 지원되지 않음 |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>업그레이드 도구를 사용할 수 있기 전에 Project Operations를 설치하려면 어떻게 해야 합니까?

업그레이드 도구를 사용할 수 있기 전에 Project Operations를 설치하는 두 가지 옵션이 있습니다.

- 새 환경 프로비전.
- Project Service Automation이 없는 판매 조직에 Project Operations를 별도로 배포합니다.

> [!NOTE]
> Project Service Automation이 조직에 설치되었지만 사용되지 않은 경우 제거할 수 있습니다. Project Service Automation을 완전히 제거한 후 동일한 조직에 Project Operations를 설치할 수 있습니다.
