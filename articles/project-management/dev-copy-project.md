---
title: 프로젝트 복사로 프로젝트 템플릿 개발
description: 이 항목은 프로젝트 복사 사용자 지정 작업을 사용하여 프로젝트 템플릿을 만드는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005664"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="0f233-103">프로젝트 복사로 프로젝트 템플릿 개발</span><span class="sxs-lookup"><span data-stu-id="0f233-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="0f233-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="0f233-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0f233-105">Dynamics 365 Project Operations는 프로젝트를 복사하고 할당을 역할을 나타내는 일반 리소스로 되돌리는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="0f233-106">고객은 이 기능을 사용하여 기본 프로젝트 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="0f233-107">**프로젝트 복사** 를 선택하면 대상 프로젝트의 상태가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="0f233-108">**상태 설명** 을 사용하여 복사 작업이 완료되는 시기를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="0f233-109">또한 **프로젝트 복사** 를 선택하면 대상 프로젝트 엔터티에서 대상 날짜가 감지되지 않는 경우 프로젝트의 시작 날짜를 현재 시작 날짜로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="0f233-110">프로젝트 사용자 지정 작업 복사</span><span class="sxs-lookup"><span data-stu-id="0f233-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="0f233-111">Name</span><span class="sxs-lookup"><span data-stu-id="0f233-111">Name</span></span> 

<span data-ttu-id="0f233-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="0f233-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="0f233-113">입력 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f233-113">Input parameters</span></span>
<span data-ttu-id="0f233-114">3개의 입력 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-114">There are three input parameters:</span></span>

| <span data-ttu-id="0f233-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f233-115">Parameter</span></span>          | <span data-ttu-id="0f233-116">종류</span><span class="sxs-lookup"><span data-stu-id="0f233-116">Type</span></span>   | <span data-ttu-id="0f233-117">값</span><span class="sxs-lookup"><span data-stu-id="0f233-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="0f233-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="0f233-118">ProjectCopyOption</span></span>  | <span data-ttu-id="0f233-119">String</span><span class="sxs-lookup"><span data-stu-id="0f233-119">String</span></span> | <span data-ttu-id="0f233-120">**{"removeNamedResources":true}** 또는 **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="0f233-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="0f233-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="0f233-121">SourceProject</span></span>      | <span data-ttu-id="0f233-122">엔터티 참조</span><span class="sxs-lookup"><span data-stu-id="0f233-122">Entity Reference</span></span> | <span data-ttu-id="0f233-123">원본 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0f233-123">Source Project</span></span> |
| <span data-ttu-id="0f233-124">대상</span><span class="sxs-lookup"><span data-stu-id="0f233-124">Target</span></span>             | <span data-ttu-id="0f233-125">엔터티 참조</span><span class="sxs-lookup"><span data-stu-id="0f233-125">Entity Reference</span></span> | <span data-ttu-id="0f233-126">대상 프로젝트</span><span class="sxs-lookup"><span data-stu-id="0f233-126">Target Project</span></span> |


- <span data-ttu-id="0f233-127">**{"clearTeamsAndAssignments": true}** : 웹용 프로젝트의 기본 동작이며 모든 할당 및 팀 구성원을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="0f233-128">**{"removeNamedResources": true}** Project Operations의 기본 동작이며 할당을 일반 리소스로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="0f233-129">작업에 대한 자세한 내용은 [웹 API 작업 사용](/powerapps/developer/common-data-service/webapi/use-web-api-actions)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0f233-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="0f233-130">복사할 필드 지정</span><span class="sxs-lookup"><span data-stu-id="0f233-130">Specify fields to copy</span></span> 
<span data-ttu-id="0f233-131">작업이 호출되면 **프로젝트 복사** 는 프로젝트 보기 **프로젝트 열 복사** 를 조회하여 프로젝트를 복사할 때 복사할 필드를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="0f233-132">예제</span><span class="sxs-lookup"><span data-stu-id="0f233-132">Example</span></span>
<span data-ttu-id="0f233-133">다음 예는 **removeNamedResources** 매개 변수 집합이 있는 **CopyProject** 사용자 지정 작업을 호출하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f233-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]