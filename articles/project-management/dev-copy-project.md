---
title: 프로젝트 복사로 프로젝트 템플릿 개발
description: 이 항목은 프로젝트 복사 사용자 지정 작업을 사용하여 프로젝트 템플릿을 만드는 방법에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045017"
---
# <a name="develop-project-templates-with-copy-project"></a>프로젝트 복사로 프로젝트 템플릿 개발

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations는 프로젝트를 복사하고 할당을 역할을 나타내는 일반 리소스로 되돌리는 기능을 지원합니다. 고객은 이 기능을 사용하여 기본 프로젝트 템플릿을 만들 수 있습니다.

**프로젝트 복사** 를 선택하면 대상 프로젝트의 상태가 업데이트됩니다. **상태 설명** 을 사용하여 복사 작업이 완료되는 시기를 결정합니다. 또한 **프로젝트 복사** 를 선택하면 대상 프로젝트 엔터티에서 대상 날짜가 감지되지 않는 경우 프로젝트의 시작 날짜를 현재 시작 날짜로 업데이트합니다.

## <a name="copy-project-custom-action"></a>프로젝트 사용자 지정 작업 복사 

### <a name="name"></a>Name 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>입력 매개 변수
3개의 입력 매개 변수가 있습니다.

| 매개 변수          | 종류   | 값                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** 또는 **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 엔터티 참조 | 원본 프로젝트 |
| 대상             | 엔터티 참조 | 대상 프로젝트 |


- **{"clearTeamsAndAssignments": true}** : 웹용 프로젝트의 기본 동작이며 모든 할당 및 팀 구성원을 제거합니다.
- **{"removeNamedResources": true}** Project Operations의 기본 동작이며 할당을 일반 리소스로 되돌립니다.

작업에 대한 자세한 내용은 [웹 API 작업 사용](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)을 참조하십시오.

## <a name="specify-fields-to-copy"></a>복사할 필드 지정 
작업이 호출되면 **프로젝트 복사** 는 프로젝트 보기 **프로젝트 열 복사** 를 조회하여 프로젝트를 복사할 때 복사할 필드를 결정합니다.


### <a name="example"></a>예제
다음 예는 **removeNamedResources** 매개 변수 집합이 있는 **CopyProject** 사용자 지정 작업을 호출하는 방법을 보여줍니다.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
