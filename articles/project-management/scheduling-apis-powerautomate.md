---
title: Power Automate와 함께 프로젝트 일정 API 사용
description: 이 문서는 프로젝트 일정 API(애플리케이션 인터페이스)를 사용하는 샘플 흐름을 제공합니다.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916342"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Power Automate와 함께 프로젝트 일정 API 사용

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

이 문서에서는 Microsoft Power Automate를 사용하여 전체 프로젝트 계획을 만드는 방법, 작업 집합을 만드는 방법 및 엔터티를 업데이트하는 방법을 보여주는 샘플 흐름에 대해 설명합니다. 이 예는 프로젝트, 프로젝트 팀 구성원, 작업 집합, 프로젝트 작업 및 리소스 할당을 생성하는 방법을 보여줍니다. 이 문서에서는 엔터티를 업데이트하고 작업 집합을 실행하는 방법도 설명합니다.

다음은 이 문서 샘플 흐름에 설명된 단계의 전체 목록입니다.

1. [PowerApps 트리거 만들기](#1)
2. [프로젝트 만들기](#2)
3. [팀원을 위한 변수 초기화](#3)
4. [일반 팀원 만들기](#4)
5. [작업 집합 만들기](#5)
6. [프로젝트 버킷 만들기](#6)
7. [링크 상태를 위한 변수 초기화](#7)
8. [작업 수를 위한 변수 초기화](#8)
9. [프로젝트 작업 ID를 위한 변수 초기화](#9)
10. [기한](#10)
11. [프로젝트 작업 설정](#11)
12. [프로젝트 작업 만들기](#12)
13. [리소스 할당 만들기](#13)
14. [변수 감소](#14)
15. [프로젝트 작업 이름 바꾸기](#15)
16. [작업 집합 실행](#16)

## <a name="assumptions"></a>가정

이 문서에서는 Dataverse 플랫폼, 클라우드 흐름 및 프로젝트 일정 API(응용 프로그래밍 인터페이스)에 대한 기본 지식이 있다고 가정합니다. 자세한 내용은 이 문서의 뒷부분에 나오는 [참조](#references) 섹션을 참조하십시오.

## <a name="create-a-flow"></a>흐름 만들기

### <a name="select-an-environment"></a>환경 선택

사용자 환경에서 Power Automate 흐름을 만들 수 있습니다.

1. <https://flow.microsoft.com>으로 이동하고 관리자 자격 증명을 사용하여 로그인합니다.
2. 오른쪽 상단에서 **환경** 을 선택합니다.
3. 목록에서 Dynamics 365 Project Operations가 설치된 환경을 선택합니다.

### <a name="create-a-solution"></a>솔루션 만들기

다음 단계에 따라 [솔루션 인식 흐름](/power-automate/overview-solution-flows)을 만듭니다. 솔루션 인식 흐름을 만들어 나중에 사용하기 위해 흐름을 더 쉽게 내보낼 수 있습니다.

1. 탐색 창에서 **솔루션** 을 선택합니다.
2. **솔루션** 페이지에서 **새 솔루션** 을 선택합니다.
3. **새 솔루션** 대화 상자에서 필수 필드를 설정한 다음 **만들기** 를 선택합니다.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1단계: PowerApps 만들기 만들기

1. **솔루션** 페이지에서 생성한 솔루션을 선택한 다음 **새로 만들기** 를 선택합니다.
2. 왼쪽 창에서 **클라우드 흐름** \> **자동화** \> **클라우드 흐름** \> **인스턴트** 를 선택합니다.
3. **흐름 이름** 필드에서 **API 데모 흐름 예약** 을 입력합니다.
4. **이 흐름을 트리거하는 방법 선택** 목록에서 **Power Apps** 를 선택합니다. Power Apps 트리거를 만들 때 논리는 작성자에게 달려 있습니다. 이 문서에서는 테스트 목적으로 입력 매개 변수를 비워 둡니다.
5. **만들기** 를 선택합니다.

## <a name="step-2-create-a-project"></a><a id="2"></a>2단계: 프로젝트 만들기

다음 단계에 따라 샘플 프로젝트를 만드십시오.

1. 생성한 흐름에서 **새로운 단계** 를 선택합니다.

    ![새 단계 추가하기.](media/newstep.png)

2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.

    ![작업 선택.](media/chooseactiontab.png)

3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.

![단계 이름 바꾸기.](media/renamestep.png)

4. **프로젝트 만들기** 단계의 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_CreateProjectV1** 을 선택합니다.
6. **msdyn\_subject** 필드에서 **동적 콘텐츠 추가** 를 선택합니다.
7. **식** 탭의 함수 필드에 **Project name - utcNow()** 를 입력합니다.
8. **확인** 을 선택합니다.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3단계: 팀원을 위한 변수 초기화

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 초기화** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **팀원 초기화** 단계 이름을 바꿉니다.
5. **이름** 필드에 **TeamMemberAction** 을 입력합니다.
6. **유형** 필드에서 **문자열** 을 선택합니다.
7. **값** 필드에서 **msdyn\_CreateTeamMemberV1** 을 입력합니다.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4단계: 일반 팀원 만들기

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **팀원 만들기** 단계 이름을 바꿉니다.
5. **작업 이름** 필드의 **동적 콘텐츠** 대화 상자에서 **TeamMemberAction** 을 선택합니다.
6. **작업 매개 변수** 필드에 다음 매개 변수 정보를 입력합니다.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    다음은 매개 변수에 대한 설명입니다.

    - **\@\@odata.type** – 엔터티 이름입니다. 예를 들어 **"Microsoft.Dynamics.CRM.msdyn\_projectteam"** 을 입력합니다.
    - **msdyn\_projectteamid** – 프로젝트 팀 ID의 기본 키입니다. 값은 GUID(Globally Unique Identifier) 식입니다.   ID는 식 탭에서 생성됩니다.

    - **msdyn\_project\@odata.bind** – 소유 프로젝트의 프로젝트 ID입니다. 값은 "프로젝트 만들기" 단계의 응답에서 가져온 동적 콘텐츠입니다. 전체 경로를 입력했는지 확인하고 괄호 사이에 동적 콘텐츠를 추가합니다. 따옴표는 필수 항목입니다. 예를 들어 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"** 를 입력합니다.
    - **msdyn\_name** – 팀원의 표시 이름입니다. 예를 들어 **"ScheduleAPIDemoTM1"** 을 입력합니다.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5단계: 작업 집합 만들기

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **작업 집합 만들기** 단계 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_CreateOperationSetV1** Dataverse 사용자 지정 작업을 선택합니다.
6. **설명** 필드에서 **ScheduleAPIDemoOperationSet** 를 입력합니다.
7. **프로젝트** 필드에서 **/msdyn\_projects(** 를 입력합니다.
8. **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateProjectV1Response ProjectId** 를 선택합니다.
9. **프로젝트** 필드에서 **)** 를 입력합니다.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6단계: 프로젝트 버킷 만들기

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **새 행 추가** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **버킷 만들기** 단계의 이름을 바꿉니다.
5. **테이블 이름** 필드에서 **프로젝트 버킷** 을 선택합니다.
6. **이름** 필드에 **ScheduleAPIDemoBucket1** 을 입력합니다.
7. **프로젝트** 필드의 경우 **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateProjectV1Response ProjectId** 를 선택합니다.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7단계: 링크 상태를 위한 변수 초기화

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 초기화** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **링크 상태 초기화** 단계 이름을 바꿉니다.
5. **이름** 필드에 **linkstatus** 를 입력합니다.
6. **유형** 필드에서 **정수** 를 선택합니다.
7. **값** 필드에 **192350000** 을 입력합니다.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8단계: 작업 수를 위한 변수 초기화

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 초기화** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **작업 수 초기화** 단계 이름을 바꿉니다.
5. **이름** 필드에 **작업 수** 를 입력합니다.
6. **유형** 필드에서 **정수** 를 선택합니다.
7. **값** 필드에 **5** 을 입력합니다.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9단계: 프로젝트 작업 ID를 위한 변수 초기화

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 초기화** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **ProjectTaskID 초기화** 단계 이름을 바꿉니다.
5. **이름** 필드에 **작업 수** 를 입력합니다.
6. **유형** 필드에서 **문자열** 을 선택합니다.
7. **값** 필드의 경우 식 작성기에 **guid()** 를 입력합니다.

## <a name="step-10-do-until"></a><a id="10"></a>10단계: 기한

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **기한** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 조건문의 첫 번째 값을 **동적 콘텐츠** 대화 상자의 **작업 수** 변수로 설정합니다.
4. 조건을 **보다 작거나 같음** 으로 설정합니다.
5. 조건문의 두 번째 값을 **0** 으로 설정합니다.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11단계: 프로젝트 작업 설정

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 설정** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 새 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **프로젝트 작업 설정** 단계 이름을 바꿉니다.
5. **이름** 필드에서 **msdyn\_projecttaskid** 를 선택합니다.
6. **값** 필드의 경우 식 작성기에 **guid()** 를 입력합니다.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12단계: 프로젝트 작업 만들기

다음 단계에 따라 현재 프로젝트 및 생성한 프로젝트 버킷에 속하는 고유 ID가 있는 프로젝트 작업을 생성합니다.

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **프로젝트 작업 만들기** 단계 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_PssCreateV1** 을 선택합니다.
6. **엔터티** 필드에 다음 매개 변수 정보를 입력합니다.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    다음은 매개 변수에 대한 설명입니다.

    - **\@\@odata.type** – 엔터티 이름입니다. 예를 들어 **"Microsoft.Dynamics.CRM.msdyn\_projecttask"** 을 입력합니다.
    - **msdyn\_projecttaskid** – 작업의 고유 ID입니다. 값은 **msdyn\_projecttaskid** 에서 동적 변수로 설정해야 합니다.
    - **msdyn\_project\@odata.bind** – 소유 프로젝트의 프로젝트 ID입니다. 값은 "프로젝트 만들기" 단계의 응답에서 가져온 동적 콘텐츠입니다. 전체 경로를 입력했는지 확인하고 괄호 사이에 동적 콘텐츠를 추가합니다. 따옴표는 필수 항목입니다. 예를 들어 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"** 를 입력합니다.
    - **msdyn\_subject** – 모든 작업 이름입니다.
    - **msdyn\_projectbucket\@odata.bind** – 작업이 포함된 프로젝트 버킷입니다. 값은 "버킷 만들기" 단계의 응답에서 가져온 동적 콘텐츠입니다. 전체 경로를 입력했는지 확인하고 괄호 사이에 동적 콘텐츠를 추가합니다. 따옴표는 필수 항목입니다. 예를 들어 **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"** 를 입력합니다.
    - **msdyn\_start** – 시작 날짜에 대한 동적 콘텐츠입니다. 예를 들어 내일은 **"addDays(utcNow(), 1)"** 과 같이 표시됩니다.
    - **msdyn\_scheduledstart** – 예정된 시작 날짜입니다. 예를 들어 내일은 **"addDays(utcNow(), 1)"** 과 같이 표시됩니다.
    - **msdyn\_scheduleend** – 예정된 종료 날짜입니다. 미래의 날짜를 선택합니다. 예를 들어 **"addDays(utcNow(), 5)"** 를 지정합니다.
    - **msdyn\_LinkStatus** – 링크 상태입니다. 예를 들어 **"192350000"** 을 입력합니다.

7. **OperationSetId** 필드의 경우 **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateOperationSetV1Response** 를 선택합니다.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13단계: 리소스 할당 만들기

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **할당 만들기** 단계의 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_PssCreateV1** 을 선택합니다.
6. **엔터티** 필드에 다음 매개 변수 정보를 입력합니다.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **OperationSetId** 필드의 경우 **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateOperationSetV1Response** 를 선택합니다.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14단계: 변수 감소

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **변수 감소** 를 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. **이름** 필드에 **작업 수** 를 선택합니다.
4. **값** 필드에 **1** 을 입력합니다.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15단계: 프로젝트 작업 이름 바꾸기

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **프로젝트 작업 이름 바꾸기** 단계 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_PssUpdateV1** 을 선택합니다.
6. **엔터티** 필드에 다음 매개 변수 정보를 입력합니다.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **OperationSetId** 필드의 경우 **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateOperationSetV1Response** 를 선택합니다.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16단계: 작업 집합 실행

1. 흐름에서 **새 단계** 를 선택합니다.
2. **작업 선택** 대화 상자의 검색 필드에 **바인딩되지 않은 작업 수행** 을 입력합니다. 그런 다음 **작업** 탭의 결과 목록에서 작업을 선택합니다.
3. 단계에서 줄임표(**...**)를 선택한 다음 **이름 바꾸기** 를 선택합니다.
4. **작업 집합 실행** 단계 이름을 바꿉니다.
5. **작업 이름** 필드에서 **msdyn\_ExecuteOperationSetV1** 을 선택합니다.
6. **OperationSetId** 필드의 경우 **동적 콘텐츠** 대화 상자에서 **msdyn\_CreateOperationSetV1Response OperationSetId** 를 선택합니다.

## <a name="references"></a>참조

- [흐름을 Dataverse - Power Automate와 통합하는 방법에 대한 개요](/power-automate/dataverse/overview?WT.mc_id=email)
- [프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행](schedule-api-preview.md)
- [클라우드 흐름 개요 - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [솔루션 인식 흐름 개요 - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
