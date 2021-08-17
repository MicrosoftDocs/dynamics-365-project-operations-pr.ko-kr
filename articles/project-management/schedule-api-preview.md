---
title: 프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행
description: 이 항목은 프로젝트 일정 API를 사용하기 위한 정보 및 샘플을 제공합니다.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008774"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

> [!IMPORTANT] 
> 이 항목에 언급된 일부 또는 모든 기능은 미리 보기 릴리스의 일부로 사용할 수 있습니다. 내용과 기능은 변경될 수 있습니다. 

## <a name="scheduling-entities"></a>예약 엔터티

프로젝트 일정 API는 **일정 엔터티** 를 사용하여 생성, 업데이트 및 삭제 작업을 수행하는 기능을 제공합니다. 이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다. **예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.

다음 표는 프로젝트 일정 엔터티의 전체 목록을 제공합니다.

| 엔터티 이름  | 엔터티 논리적 이름 |
| --- | --- |
| Project | msdyn_project |
| 프로젝트 작업  | msdyn_projecttask  |
| 프로젝트 작업 종속성  | msdyn_projecttaskdependency  |
| 리소스 할당 | msdyn_resourceassignment |
| 프로젝트 버킷  | msdyn_projectbucket |
| 프로젝트 팀 구성원 | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.

## <a name="project-schedule-apis"></a>프로젝트 일정 API

다음은 현재 프로젝트 일정 API 목록입니다.

- **msdyn_CreateProjectV1**: 이 API를 사용하여 프로젝트를 생성할 수 있습니다. 프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.
- **msdyn_CreateTeamMemberV1**: 이 API를 사용하여 프로젝트 팀 구성원을 만들 수 있습니다. 팀 구성원 레코드가 즉시 생성됩니다.
- **msdyn_CreateOperationSetV1**: 이 API는 트랜잭션 내에서 수행해야 하는 여러 요청을 예약하는 데 사용할 수 있습니다.
- **msdyn_PSSCreateV1**: 이 API는 엔터티를 만드는 데 사용할 수 있습니다. 엔터티는 만들기 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.
- **msdyn_PSSUpdateV1**: 이 API는 엔터티를 업데이트하는 데 사용할 수 있습니다. 엔터티는 업데이트 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.
- **msdyn_PSSDeleteV1**: 이 API는 엔터티를 삭제하는 데 사용할 수 있습니다. 엔터티는 삭제 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다.
- **msdyn_ExecuteOperationSetV1**: 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.

## <a name="using-project-schedule-apis-with-operationset"></a>OperationSet와 함께 프로젝트 일정 API 사용

**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다. 그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.

## <a name="supported-operations"></a>지원되는 작업

| 예약 엔터티 | 만들기 | 엽데이트 | Delete | 중요 사항 |
| --- | --- | --- | --- | --- |
프로젝트 작업 | 네 | 네 | 네 | 없음 |
| 프로젝트 작업 종속성 | 네 | 네 | | 프로젝트 작업 종속성 레코드는 업데이트되지 않습니다. 대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다. |
| 리소스 할당 | 네 | 네 | | **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다. 리소스 할당 레코드는 업데이트되지 않습니다. 대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다. |
| 프로젝트 버킷 | 해당 없음 | 해당 없음 | 해당 없음 | 기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다. |
| 프로젝트 팀원 | 네 | 네 | 네 | 생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다. |
| Project | 네 | 네 | 해당 없음 | **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다. |

이러한 API는 사용자 지정 필드를 포함하는 엔터티 개체를 사용하여 호출할 수 있습니다.

ID 속성은 선택 사항입니다. 제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다. 제공되지 않으면 시스템에서 생성합니다.

## <a name="restricted-fields"></a>제한된 필드

다음 표는 **생성** 및 **편집** 에서 제한되는 필드를 정의합니다.

### <a name="project-task"></a>프로젝트 작업

| **논리적 이름**                       | **생성 가능** | **편집 가능**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | 아니요             | 아니요               |
| msdyn_actualcost_base                  | 아니요             | 아니요               |
| msdyn_actualend                        | 아니요             | 아니요               |
| msdyn_actualsales                      | 아니요             | 아니요               |
| msdyn_actualsales_base                 | 아니요             | 아니요               |
| msdyn_actualstart                      | 아니요             | 아니요               |
| msdyn_costatcompleteestimate           | 아니요             | 아니요               |
| msdyn_costatcompleteestimate_base      | 아니요             | 아니요               |
| msdyn_costconsumptionpercentage        | 아니요             | 아니요               |
| msdyn_effortcompleted                  | 아니요             | 아니요               |
| msdyn_effortestimateatcomplete         | 아니요             | 아니요               |
| msdyn_iscritical                       | 아니요             | 아니요               |
| msdyn_iscriticalname                   | 아니요             | 아니요               |
| msdyn_ismanual                         | 아니요             | 아니요               |
| msdyn_ismanualname                     | 아니요             | 아니요               |
| msdyn_ismilestone                      | 아니요             | 아니요               |
| msdyn_ismilestonename                  | 아니요             | 아니요               |
| msdyn_LinkStatus                       | 아니요             | 아니요               |
| msdyn_linkstatusname                   | 아니요             | 아니요               |
| msdyn_msprojectclientid                | 아니요             | 아니요               |
| msdyn_plannedcost                      | 아니요             | 아니요               |
| msdyn_plannedcost_base                 | 아니요             | 아니요               |
| msdyn_plannedsales                     | 아니요             | 아니요               |
| msdyn_plannedsales_base                | 아니요             | 아니요               |
| msdyn_pluginprocessingdata             | 아니요             | 아니요               |
| msdyn_progress                         | 아니요             | 아니요(P4W의 경우 예) |
| msdyn_remainingcost                    | 아니요             | 아니요               |
| msdyn_remainingcost_base               | 아니요             | 아니요               |
| msdyn_remainingsales                   | 아니요             | 아니요               |
| msdyn_remainingsales_base              | 아니요             | 아니요               |
| msdyn_requestedhours                   | 아니요             | 아니요               |
| msdyn_resourcecategory                 | 아니요             | 아니요               |
| msdyn_resourcecategoryname             | 아니요             | 아니요               |
| msdyn_resourceorganizationalunitid     | 아니요             | 아니요               |
| msdyn_resourceorganizationalunitidname | 아니요             | 아니요               |
| msdyn_salesconsumptionpercentage       | 아니요             | 아니요               |
| msdyn_salesestimateatcomplete          | 아니요             | 아니요               |
| msdyn_salesestimateatcomplete_base     | 아니요             | 아니요               |
| msdyn_salesvariance                    | 아니요             | 아니요               |
| msdyn_salesvariance_base               | 아니요             | 아니요               |
| msdyn_scheduleddurationminutes         | 아니요             | 아니요               |
| msdyn_scheduledend                     | 아니요             | 아니요               |
| msdyn_scheduledstart                   | 아니요             | 아니요               |
| msdyn_schedulevariance                 | 아니요             | 아니요               |
| msdyn_skipupdateestimateline           | 아니요             | 아니요               |
| msdyn_skipupdateestimatelinename       | 아니요             | 아니요               |
| msdyn_summary                          | 아니요             | 아니요               |
| msdyn_varianceofcost                   | 아니요             | 아니요               |
| msdyn_varianceofcost_base              | 아니요             | 아니요               |

### <a name="project-task-dependency"></a>프로젝트 작업 종속성

| **논리적 이름**              | **생성 가능** | **편집 가능** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | 아니요             | 아니요           |
| msdyn_linktypename            | 아니요             | 아니요           |
| msdyn_predecessortask         | 예            | 아니요           |
| msdyn_predecessortaskname     | 예            | 아니요           |
| msdyn_project                 | 예            | 아니요           |
| msdyn_projectname             | 예            | 아니요           |
| msdyn_projecttaskdependencyid | 예            | 아니요           |
| msdyn_successortask           | 예            | 아니요           |
| msdyn_successortaskname       | 예            | 아니요           |

### <a name="resource-assignment"></a>리소스 할당

| **논리적 이름**             | **생성 가능** | **편집 가능** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | 예            | 아니요           |
| msdyn_bookableresourceidname | 예            | 아니요           |
| msdyn_bookingstatusid        | 아니요             | 아니요           |
| msdyn_bookingstatusidname    | 아니요             | 아니요           |
| msdyn_committype             | 아니요             | 아니요           |
| msdyn_committypename         | 아니요             | 아니요           |
| msdyn_effort                 | 아니요             | 아니요           |
| msdyn_effortcompleted        | 아니요             | 아니요           |
| msdyn_effortremaining        | 아니요             | 아니요           |
| msdyn_finish                 | 아니요             | 아니요           |
| msdyn_plannedcost            | 아니요             | 아니요           |
| msdyn_plannedcost_base       | 아니요             | 아니요           |
| msdyn_plannedcostcontour     | 아니요             | 아니요           |
| msdyn_plannedsales           | 아니요             | 아니요           |
| msdyn_plannedsales_base      | 아니요             | 아니요           |
| msdyn_plannedsalescontour    | 아니요             | 아니요           |
| msdyn_plannedwork            | 아니요             | 아니요           |
| msdyn_projectid              | 예            | 아니요           |
| msdyn_projectidname          | 아니요             | 아니요           |
| msdyn_projectteamid          | 아니요             | 아니요           |
| msdyn_projectteamidname      | 아니요             | 아니요           |
| msdyn_start                  | 아니요             | 아니요           |
| msdyn_taskid                 | 아니요             | 아니요           |
| msdyn_taskidname             | 아니요             | 아니요           |
| msdyn_userresourceid         | 아니요             | 아니요           |

### <a name="project-team-member"></a>프로젝트 팀원

| **논리적 이름**                                 | **생성 가능** | **편집 가능** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | 아니요             | 아니요           |
| msdyn_creategenericteammemberwithrequirementname | 아니요             | 아니요           |
| msdyn_deletestatus                               | 아니요             | 아니요           |
| msdyn_deletestatusname                           | 아니요             | 아니요           |
| msdyn_effort                                     | 아니요             | 아니요           |
| msdyn_effortcompleted                            | 아니요             | 아니요           |
| msdyn_effortremaining                            | 아니요             | 아니요           |
| msdyn_finish                                     | 아니요             | 아니요           |
| msdyn_hardbookedhours                            | 아니요             | 아니요           |
| msdyn_hours                                      | 아니요             | 아니요           |
| msdyn_markedfordeletiontimer                     | 아니요             | 아니요           |
| msdyn_markedfordeletiontimestamp                 | 아니요             | 아니요           |
| msdyn_msprojectclientid                          | 아니요             | 아니요           |
| msdyn_percentage                                 | 아니요             | 아니요           |
| msdyn_requiredhours                              | 아니요             | 아니요           |
| msdyn_softbookedhours                            | 아니요             | 아니요           |
| msdyn_start                                      | 아니요             | 아니요           |

### <a name="project"></a>Project

| **논리적 이름**                       | **생성 가능** | **편집 가능** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | 아니요             | 아니요           |
| msdyn_actualexpensecost_base           | 아니요             | 아니요           |
| msdyn_actuallaborcost                  | 아니요             | 아니요           |
| msdyn_actuallaborcost_base             | 아니요             | 아니요           |
| msdyn_actualsales                      | 아니요             | 아니요           |
| msdyn_actualsales_base                 | 아니요             | 아니요           |
| msdyn_contractlineproject              | 예            | 아니요           |
| msdyn_contractorganizationalunitid     | 예            | 아니요           |
| msdyn_contractorganizationalunitidname | 예            | 아니요           |
| msdyn_costconsumption                  | 아니요             | 아니요           |
| msdyn_costestimateatcomplete           | 아니요             | 아니요           |
| msdyn_costestimateatcomplete_base      | 아니요             | 아니요           |
| msdyn_costvariance                     | 아니요             | 아니요           |
| msdyn_costvariance_base                | 아니요             | 아니요           |
| msdyn_duration                         | 아니요             | 아니요           |
| msdyn_effort                           | 아니요             | 아니요           |
| msdyn_effortcompleted                  | 아니요             | 아니요           |
| msdyn_effortestimateatcompleteeac      | 아니요             | 아니요           |
| msdyn_effortremaining                  | 아니요             | 아니요           |
| msdyn_finish                           | 예            | 예          |
| msdyn_globalrevisiontoken              | 아니요             | 아니요           |
| msdyn_islinkedtomsprojectclient        | 아니요             | 아니요           |
| msdyn_islinkedtomsprojectclientname    | 아니요             | 아니요           |
| msdyn_linkeddocumenturl                | 아니요             | 아니요           |
| msdyn_msprojectdocument                | 아니요             | 아니요           |
| msdyn_msprojectdocumentname            | 아니요             | 아니요           |
| msdyn_plannedexpensecost               | 아니요             | 아니요           |
| msdyn_plannedexpensecost_base          | 아니요             | 아니요           |
| msdyn_plannedlaborcost                 | 아니요             | 아니요           |
| msdyn_plannedlaborcost_base            | 아니요             | 아니요           |
| msdyn_plannedsales                     | 아니요             | 아니요           |
| msdyn_plannedsales_base                | 아니요             | 아니요           |
| msdyn_progress                         | 아니요             | 아니요           |
| msdyn_remainingcost                    | 아니요             | 아니요           |
| msdyn_remainingcost_base               | 아니요             | 아니요           |
| msdyn_remainingsales                   | 아니요             | 아니요           |
| msdyn_remainingsales_base              | 아니요             | 아니요           |
| msdyn_replaylogheader                  | 아니요             | 아니요           |
| msdyn_salesconsumption                 | 아니요             | 아니요           |
| msdyn_salesestimateatcompleteeac       | 아니요             | 아니요           |
| msdyn_salesestimateatcompleteeac_base  | 아니요             | 아니요           |
| msdyn_salesvariance                    | 아니요             | 아니요           |
| msdyn_salesvariance_base               | 아니요             | 아니요           |
| msdyn_scheduleperformance              | 아니요             | 아니요           |
| msdyn_scheduleperformancename          | 아니요             | 아니요           |
| msdyn_schedulevariance                 | 아니요             | 아니요           |
| msdyn_taskearlieststart                | 아니요             | 아니요           |
| msdyn_teamsize                         | 아니요             | 아니요           |
| msdyn_teamsize_date                    | 아니요             | 아니요           |
| msdyn_teamsize_state                   | 아니요             | 아니요           |
| msdyn_totalactualcost                  | 아니요             | 아니요           |
| msdyn_totalactualcost_base             | 아니요             | 아니요           |
| msdyn_totalplannedcost                 | 아니요             | 아니요           |
| msdyn_totalplannedcost_base            | 아니요             | 아니요           |


## <a name="limitations-and-known-issues"></a>제한 사항 및 알려진 문제
다음은 제한 사항 및 알려진 문제 목록입니다.

- 프로젝트 일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다. 다음 사용자는 사용할 수 없습니다.
    - 응용 프로그램 사용자
    - 시스템 사용자
    - 통합 사용자
    - 필요한 라이선스가 없는 다른 사용자
- 각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.
- 각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.
- Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.
- **OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.
- [프로젝트 및 작업에 대한 제한 및 경계](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>오류 처리

   - 작업 세트에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **작업 세트** 로 이동합니다.
   - 프로젝트 일정 서비스에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **PSS 오류 로그** 로 이동합니다.

## <a name="sample-scenario"></a>샘플 시나리오

이 시나리오에서는 프로젝트, 팀 구성원, 4개의 작업 및 2개의 리소스 할당을 만듭니다. 다음으로 하나의 작업을 업데이트하고, 프로젝트를 업데이트하고, 하나의 작업을 삭제하고, 하나의 리소스 할당을 삭제하고, 작업 종속성을 만듭니다.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>추가 샘플

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
