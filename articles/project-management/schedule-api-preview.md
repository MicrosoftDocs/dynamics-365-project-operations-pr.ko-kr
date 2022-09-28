---
title: 프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행
description: 이 문서에서는 프로젝트 일정 API를 사용하기 위한 정보와 샘플을 제공합니다.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541133"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>프로젝트 일정 API를 사용하여 일정 엔터티로 작업 수행

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


**예약 엔터티**

프로젝트 일정 API는 **일정 엔터티** 를 사용하여 생성, 업데이트 및 삭제 작업을 수행하는 기능을 제공합니다. 이러한 엔터티는 웹용 프로젝트에서 예약 엔진을 통해 관리됩니다. **예약 엔터티** 를 사용한 생성, 업데이트 및 삭제 작업은 이전 Dynamics 365 Project Operations 릴리스에서 제한되었습니다.

다음 표는 프로젝트 일정 엔터티의 전체 목록을 제공합니다.

| **엔터티 이름**         | **엔터티 논리적 이름**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| 프로젝트 작업            | msdyn_projecttask           |
| 프로젝트 작업 종속성 | msdyn_projecttaskdependency |
| 리소스 할당     | msdyn_resourceassignment    |
| 프로젝트 버킷          | msdyn_projectbucket         |
| 프로젝트 팀 구성원     | msdyn_projectteam           |
| 프로젝트 검사 목록      | msdyn_projectchecklist      |
| 프로젝트 레이블           | msdyn_projectlabel          |
| 레이블을 지정할 프로젝트 작업   | msdyn_projecttasktolabel    |
| 프로젝트 스프린트          | msdyn_projectsprint         |

**OperationSet**

OperationSet은 일정에 영향을 미치는 여러 요청을 트랜잭션 내에서 처리해야 할 때 사용할 수 있는 작업 단위 패턴입니다.

**프로젝트 일정 API**

다음은 현재 프로젝트 일정 API 목록입니다.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | 이 API는 프로젝트를 생성하는 데 사용됩니다. 프로젝트 및 기본 프로젝트 버킷이 즉시 생성됩니다.                         |
| **msdyn_CreateTeamMemberV1**            | 이 API는 프로젝트 팀원을 생성하는 데 사용됩니다. 팀 구성원 레코드가 즉시 생성됩니다.                                  |
| **msdyn_CreateOperationSetV1**          | 이 API는 트랜잭션 내에서 수행되어야 하는 여러 요청을 예약하는 데 사용됩니다.                                        |
| **msdyn_PssCreateV1**                   | 이 API는 엔터티를 생성하는 데 사용됩니다. 엔터티는 만들기 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다. |
| **msdyn_PssUpdateV1**                   | 이 API는 엔터티를 업데이트하는 데 사용됩니다. 엔터티는 업데이트 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다  |
| **msdyn_PssDeleteV1**                   | 이 API는 엔터티를 삭제하는 데 사용됩니다. 엔터티는 삭제 작업을 지원하는 프로젝트 일정 엔터티 중 하나일 수 있습니다. |
| **msdyn_ExecuteOperationSetV1**         | 이 API는 지정된 작업 집합 내에서 모든 작업을 실행하는 데 사용됩니다.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | 이 API는 자원 할당 계획 작업 윤곽선을 업데이트하는 데 사용됩니다.                                                        |



**OperationSet와 함께 프로젝트 일정 API 사용**

**CreateProjectV1** 및 **CreateTeamMemberV1** 이 모두 있는 레코드가 즉시 생성되기 때문에 이러한 API는 **OperationSet** 에서 직접 사용할 수 없습니다. 그러나 API를 사용하여 필요한 레코드를 만들고 **OperationSet** 을 만든 다음 **OperationSet** 에서 이러한 미리 만들어진 레코드를 사용할 수 있습니다.

**지원되는 작업**

| **예약 엔터티**   | **만들기** | **Update** | **Delete** | **중요 사항**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 프로젝트 작업            | 네        | 네        | 네        | **Progress**, **EffortCompleted** 및 **EffortRemaining** 필드는 Project for the Web에서 편집할 수 있지만 Project Operations에서는 편집할 수 없습니다.                                                                                                                                                                                             |
| 프로젝트 작업 종속성 | 네        | 없음         | 네        | 프로젝트 작업 종속성 레코드는 업데이트되지 않습니다. 대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다.                                                                                                                                                                                                                                 |
| 리소스 할당     | 네        | 네\*      | 네        | **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** 및 **PlannedWork** 필드를 사용한 작업은 지원되지 않습니다. 리소스 할당 레코드는 업데이트되지 않습니다. 대신 이전 레코드를 삭제하고 새 레코드를 만들 수 있습니다. 자원 할당 윤곽선을 업데이트하기 위해 별도의 API가 제공되었습니다. |
| 프로젝트 버킷          | 네        | 네        | 네        | 기본 버킷은 **CreateProjectV1** API를 사용하여 생성됩니다. 프로젝트 버킷 생성 및 삭제에 대한 지원이 업데이트 릴리스 16에 추가되었습니다.                                                                                                                                                                                                   |
| 프로젝트 팀원     | 네        | 네        | 네        | 생성 작업의 경우 **CreateTeamMemberV1** API를 사용합니다.                                                                                                                                                                                                                                                                                           |
| Project                 | 네        | 네        |            | **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** 및 **Duration** 필드를 사용한 작업은 지원되지 않습니다.                                                                                       |
| 프로젝트 검사 목록      | 네        | 네        | 네        |                                                                                                                                                                                                                                                                                                                                                         |
| 프로젝트 레이블           | 없음         | 네        | 없음         | 레이블 이름은 변경할 수 있습니다. 이 기능은 Project for the Web에서만 사용할 수 있습니다                                                                                                                                                                                                                                                                      |
| 레이블을 지정할 프로젝트 작업   | 네        | 없음         | 네        | 이 기능은 Project for the Web에서만 사용할 수 있습니다                                                                                                                                                                                                                                                                                                  |
| 프로젝트 스프린트          | 네        | 네        | 네        | **시작** 필드의 날짜는 **완료** 필드보다 이전이어야 합니다. 동일한 프로젝트의 스프린트는 서로 겹칠 수 없습니다. 이 기능은 Project for the Web에서만 사용할 수 있습니다                                                                                                                                                                    |




ID 속성은 선택 사항입니다. 제공되는 경우 시스템은 이를 사용하려고 시도하고 사용할 수 없는 경우 예외를 발생시킵니다. 제공되지 않으면 시스템에서 생성합니다.

**제한 사항 및 알려진 문제**

다음은 제한 사항 및 알려진 문제 목록입니다.

-   프로젝트 일정 API는 **Microsoft Project 라이선스가 있는 사용자** 만 사용할 수 있습니다. 다음 사용자는 사용할 수 없습니다.
    -   응용 프로그램 사용자
    -   시스템 사용자
    -   통합 사용자
    -   필요한 라이선스가 없는 다른 사용자
-   각 **OperationSet** 는 최대 100개의 작업만 가질 수 있습니다.
-   각 사용자는 최대 10개의 열린 **OperationSet** 만 가질수 있습니다.
-   Project Operations는 현재 프로젝트에서 최대 500개의 총 작업을 지원합니다.
-   각 업데이트 리소스 할당 윤곽선 작업은 단일 작업으로 계산됩니다.
-   업데이트된 등고선의 각 목록에는 최대 100개의 타임 슬라이스가 포함될 수 있습니다.
-   **OperationSet** 실패 상태 및 실패 로그는 현재 사용할 수 없습니다.
-   프로젝트당 최대 400개의 스프린트가 있습니다.
-   [프로젝트 및 작업에 대한 한도 및 경계](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   레이블은 현재 Project for the Web에서만 사용할 수 있습니다.

**오류 처리**

-   작업 세트에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **작업 세트** 로 이동합니다.
-   프로젝트 일정 서비스에서 생성된 오류를 검토하려면 **설정** \> **일정 통합** \> **PSS 오류 로그** 로 이동합니다.

**리소스 할당 윤곽선 편집**

엔터티를 업데이트하는 다른 모든 프로젝트 일정 API와 달리 자원 할당 윤곽 API는 단일 엔터티 msydn_resourceassignment에서 단일 필드 msdyn_plannedwork에 대한 업데이트를 단독으로 담당합니다.

주어진 일정 모드는 다음과 같습니다.

-   **고정 단위**
-   프로젝트 일정은 월, 화, 목, 금요일 태평양 표준시 9-5시(수요일 휴무)
-   리소스 캘린더는 태평양 표준시 월~금 9-1시

이 할당은 1주일 동안 하루 4시간입니다. 리소스 일정이 9-1 태평양 표준시 또는 하루 4시간이기 때문입니다.

| &nbsp;     | 작업 | 시작 날짜 | 종료 날짜  | 수량 | 2022년 6월 13일 | 2022년 6월 14일 | 2022년 6월 15일 | 2022년 6월 16일 | 2022년 6월 17일 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1시 작업자 |  T1  | 2022년 6월 13일  | 2022년 6월 17일 | 20       | 4         | 4         | 4         | 4         | 4         |

예를 들어, 작업자가 이번 주에 매일 3시간만 일하고 다른 작업에는 1시간을 허용하도록 하려는 경우입니다.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours 샘플 페이로드 선택:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

컨투어 일정 API 업데이트가 실행된 후의 할당입니다.

| &nbsp;     | 작업 | 시작 날짜 | 종료 날짜  | 수량 | 2022년 6월 13일 | 2022년 6월 14일 | 2022년 6월 15일 | 2022년 6월 16일 | 2022년 6월 17일 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1시 작업자 | T1   | 2022년 6월 13일  | 2022년 6월 17일 | 15       | 3         | 3         | 3         | 3         | 3         |


**샘플 시나리오**

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

** 추가 샘플

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
