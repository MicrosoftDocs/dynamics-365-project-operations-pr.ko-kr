---
title: 프로젝트 복사로 프로젝트 템플릿 개발
description: 이 문서에서는 프로젝트 복사 사용자 지정 작업을 사용하여 프로젝트 템플릿을 만드는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923840"
---
# <a name="develop-project-templates-with-copy-project"></a>프로젝트 복사로 프로젝트 템플릿 개발

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations는 프로젝트를 복사하고 할당을 역할을 나타내는 일반 리소스로 되돌리는 기능을 지원합니다. 고객은 이 기능을 사용하여 기본 프로젝트 템플릿을 만들 수 있습니다.

**프로젝트 복사** 를 선택하면 대상 프로젝트의 상태가 업데이트됩니다. **상태 설명** 을 사용하여 복사 작업이 완료되는 시기를 결정합니다. 또한 **프로젝트 복사** 를 선택하면 대상 프로젝트 엔터티에서 대상 날짜가 감지되지 않는 경우 프로젝트의 시작 날짜를 현재 시작 날짜로 업데이트합니다.

## <a name="copy-project-custom-action"></a>프로젝트 사용자 지정 작업 복사

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>입력 매개 변수

3개의 입력 매개 변수가 있습니다.

- **ReplaceNamedResources** 또는 **ClearTeamsAndAssignments** – 옵션 중 하나만 설정합니다. 둘 다 설정하지 마십시오.

    - **\{"ReplaceNamedResources":true\}** – Project Operations의 기본 동작입니다. 모든 명명된 리소스는 일반 리소스로 대체됩니다.
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web의 기본 동작입니다. 모든 할당 및 팀 구성원이 제거됩니다.

- **SourceProject** – 복사할 원본 프로젝트의 엔터티 참조입니다. 이 매개 변수는 null일 수 없습니다.
- **Target** – 복사할 대상 프로젝트의 엔터티 참조입니다. 이 매개 변수는 null일 수 없습니다.

다음 표는 세 가지 매개 변수에 대한 요약을 제공합니다.

| 매개 변수                | Type             | 값                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | 부울          | **True** 또는 **False** |
| ClearTeamsAndAssignments | 부울          | **True** 또는 **False** |
| SourceProject            | 엔터티 참조 | 소스 프로젝트    |
| Target                   | 엔터티 참조 | 대상 프로젝트    |

작업에 대한 자세한 내용은 [웹 API 작업 사용](/powerapps/developer/common-data-service/webapi/use-web-api-actions)을 참조하십시오.

### <a name="validations"></a>유효성 검사

다음 유효성 검사가 수행됩니다.

1. Null은 소스 및 대상 프로젝트를 확인하고 검색하여 조직에 두 프로젝트가 있는지 확인합니다.
2. 시스템은 다음 조건을 확인하여 대상 프로젝트가 복사에 유효한지 확인합니다.

    - 프로젝트에 대한 이전 활동(**작업** 탭 선택 포함)이 없으며 프로젝트가 새로 생성됩니다.
    - 이전 사본이 없고 이 프로젝트에 요청된 가져오기가 없으며 프로젝트에 **실패** 상태가 없습니다.

3. 작업은 HTTP를 사용하여 호출되지 않습니다.

## <a name="specify-fields-to-copy"></a>복사할 필드 지정

작업이 호출되면 **프로젝트 복사** 는 프로젝트 보기 **프로젝트 열 복사** 를 조회하여 프로젝트를 복사할 때 복사할 필드를 결정합니다.

### <a name="example"></a>예

다음 예는 **removeNamedResources** 매개 변수 집합을 사용하여 **CopyProjectV3** 사용자 지정 작업을 호출하는 방법을 보여줍니다.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
