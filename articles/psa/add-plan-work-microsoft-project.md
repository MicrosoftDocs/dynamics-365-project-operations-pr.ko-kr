---
title: Project Service 추가 기능을 사용하여 Microsoft Project의 작업 계획 | MicrosoftDocs
description: 이 항목은 Microsoft Project Service를 위한 Microsoft Project 추가 기능을 추가, 구성 및 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129686"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="03384-103">Project Service Automation 추가 기능을 사용하여 Microsoft Project의 작업 계획</span><span class="sxs-lookup"><span data-stu-id="03384-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="03384-104">으로 쉽게 예상을 비롯한 프로젝트 계획을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="03384-105">작업을 정의하여 최종 제안서를 제출할 때 비용, 노력 및 영업 가치를 명확하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="03384-106">이제 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]을 설치하여 익숙한 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 환경에서 작업을 계획할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="03384-107">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]의 강력한 계획 및 관리 기능을 사용한 다음 Project Service Automation에서 프로젝트 계획을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="03384-108">SharePoint 문서 관리를 사용하여 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트의 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일을 저장하려면 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 관리자가 문서 관리를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="03384-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]은 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional 에디션과만 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="03384-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="03384-110">추가 기능 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="03384-110">Download and install the add-in</span></span>  
 <span data-ttu-id="03384-111">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 로그인 정보를 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="03384-112">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]로 연결하기 위해 이 정보가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="03384-113">다운로드 센터에서 지원되는 Project Service 버전 [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) 또는 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)를 위한 추가 기능을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="03384-114">다운로드 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-114">Click the download link.</span></span>  

3.  <span data-ttu-id="03384-115">다운로드가 완료되면 **예** 를 클릭하여 추가 기능을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="03384-116">추가 기능 구성</span><span class="sxs-lookup"><span data-stu-id="03384-116">Configure the add-in</span></span>  

1. <span data-ttu-id="03384-117">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 열고 **Project Service** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="03384-118">**연결** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="03384-119">로그인 정보를 입력하고 **로그인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="03384-120">이제 이 추가 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="03384-121">템플릿에서 읽기</span><span class="sxs-lookup"><span data-stu-id="03384-121">Read from a template</span></span>  
 <span data-ttu-id="03384-122">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 만든 템플릿에서 읽어와 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]로 복사하여 프로젝트 계획을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="03384-123">[프로젝트 템플릿 만들기(Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="03384-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="03384-124">**Project Service** 탭에서 **읽기** > **Project Service Automation 프로젝트 템플릿** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="03384-125">목록에서 프로젝트 템플릿을 선택하고 **열기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="03384-126">기본적으로 템플릿에서 Project로 복사하는 작업은 수동으로 예약하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03384-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="03384-127">프로젝트 리소스에 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 역할 할당</span><span class="sxs-lookup"><span data-stu-id="03384-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="03384-128">프로젝트를 열고 **작업** 리본을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="03384-129">**Gantt 차트** 메뉴를 클릭한 후 **리소스 시트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="03384-130">리소스 시트에서 **Project Service 리소스 역할** 드롭다운 메뉴를 클릭하고 Project Service Automation 역할을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="03384-131">리소스를 사용하여 프로젝트 팀 구성</span><span class="sxs-lookup"><span data-stu-id="03384-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="03384-132">Project Service 탭에서 행을 선택하고 **리소스 찾기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="03384-133">**리소스 예약** 화면에서 프로젝트에 사용할 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="03384-134">**예약** 을 클릭한 후 **확인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="03384-135">프로젝트 게시</span><span class="sxs-lookup"><span data-stu-id="03384-135">Publish your project</span></span>  
<span data-ttu-id="03384-136">프로젝트 계획이 완료되면 다음 단계는 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 프로젝트를 가져와 게시하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="03384-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="03384-137">프로젝트는 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03384-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="03384-138">가격 산정 및 팀 생성 프로세스가 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03384-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="03384-139">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 프로젝트를 열어 팀, 프로젝트 추정, 작업 분할 구조가 생성된 것을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="03384-140">다음 표에서는 결과를 찾을 수 있는 위치를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03384-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="03384-141">**Gantt 차트**</span><span class="sxs-lookup"><span data-stu-id="03384-141">**Gantt Chart**</span></span>   | <span data-ttu-id="03384-142">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **작업 분할 구조 화면** 으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03384-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="03384-143">**리소스 시트**</span><span class="sxs-lookup"><span data-stu-id="03384-143">**Resource Sheet**</span></span> |   <span data-ttu-id="03384-144">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **프로젝트 팀 구성원** 화면으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03384-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="03384-145">**사용 용도**</span><span class="sxs-lookup"><span data-stu-id="03384-145">**Use Usage**</span></span>    |    <span data-ttu-id="03384-146">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **프로젝트 추정** 화면으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03384-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="03384-147">**프로젝트를 가져오고 게시하려면**</span><span class="sxs-lookup"><span data-stu-id="03384-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="03384-148">**Project Service** 탭에서 **게시** > **새 Project Service Automation 프로젝트** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="03384-149">**Project Service에 새 프로젝트로 게시** 대화 상자에 **프로젝트 이름** 을 입력하고 **고객** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="03384-150">추가적으로 **Project Service Automation에 프로젝트 계획 연결** 을 체크하여 계획 Project 파일을 Project Service Automation에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="03384-151">**게시** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-151">Click **Publish**.</span></span>  

   <span data-ttu-id="03384-152">Project 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결하면 Project 파일이 마스터 파일이 되고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 작업 분할 구조가 읽기 전용으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03384-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="03384-153">프로젝트 계획을 수정하려면 이를 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만들고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 업데이트로 게시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="03384-154">가져온 프로젝트 편집</span><span class="sxs-lookup"><span data-stu-id="03384-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="03384-155">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]으로 가져온 프로젝트 계획 변경은 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="03384-156">마스터 파일을 열고 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="03384-157">파일 연결을 해제하고 Project Service에서 바로 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="03384-158">기본적으로 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 업로드된 프로젝트는 잠겨있으므로 Project에서만 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="03384-159">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 파일을 편집하려면 파일의 연결을 해제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="03384-160">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 편집</span><span class="sxs-lookup"><span data-stu-id="03384-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="03384-161">메인 메뉴에서 **Project Service** > **프로젝트** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="03384-162">프로젝트 목록에서 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만든 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="03384-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="03384-163">리본 메뉴에서 **MS Project에서 열기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="03384-164">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 연결된 마스터 파일이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="03384-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="03384-165">파일 연결을 해제하고 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service에서 편집</span><span class="sxs-lookup"><span data-stu-id="03384-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="03384-166">메인 메뉴에서 **Project Service** > **프로젝트** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="03384-167">프로젝트 목록에서 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만든 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="03384-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="03384-168">리본 메뉴에서 **MS Project에서 연결 해제** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="03384-169">Project 파일을 SharePoint 또는 Office 그룹에 업로드</span><span class="sxs-lookup"><span data-stu-id="03384-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="03384-170">Project 파일을 SharePoint에 업로드하면 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트의 관련 문서에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="03384-171">관리자가 SharePoint 문서 관리를 구성하고 프로젝트 엔터티에 대해 이를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="03384-172">또한 Office 그룹을 설정한 경우 Project 파일을 [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="03384-173">SharePoint용 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="03384-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="03384-174">메인 메뉴에서 **Project Service** > **업로드** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="03384-175">**Project Service Automation 프로젝트 문서에** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="03384-176">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기 허용** 대화에서 **예** 또는 **아니요** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="03384-177">**예** 를 클릭하면 Project Service Automation에서 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 버튼을 선택하여 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 시작하고 SharePoint 문서 라이브러리에서 프로젝트 파일을 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="03384-178">**아니요** 를 클릭하면 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 단추 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="03384-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일은 특정 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트에 대해 **문서** 아래의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="03384-180">Office 그룹에 대해 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="03384-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="03384-181">메인 메뉴에서 **Project Service** > **업로드** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="03384-182">**Project Service Automation 프로젝트 문서에** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="03384-183">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기 허용** 대화에서 **예** 또는 **아니요** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="03384-184">**예** 를 클릭하면 Project Service Automation에서 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 버튼을 선택하여 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]를 시작하고 SharePoint 문서 라이브러리에서 프로젝트 파일을 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="03384-185">**아니요** 를 클릭하면 **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 열기** 단추 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="03384-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 파일은 특정 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 프로젝트에 대해 **문서** 아래의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="03384-187">프로젝트를 템플릿으로 게시</span><span class="sxs-lookup"><span data-stu-id="03384-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="03384-188">프로젝트를 저장한 다음 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 프로젝트 템플릿으로 저장하여 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03384-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="03384-189">프로젝트 템플릿은 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에서 다시 사용할 수 있는 프로젝트 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="03384-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="03384-190">[프로젝트 템플릿 만들기(Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="03384-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="03384-191">**Project Service** 탭에서 **게시** > **새 Project Service Automation 프로젝트 템플릿** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="03384-192">**Project Service 템플릿에 새 프로젝트로 게시** 대화 상자에 **프로젝트 템플릿 이름** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="03384-193">추가적으로 **Project Service Automation에 프로젝트 계획 연결** 을 체크하여 프로젝트 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="03384-194">**게시** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-194">Click **Publish**.</span></span>  

<span data-ttu-id="03384-195">Project 파일을 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 연결하면 Project 파일이 마스터 파일이 되고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 템플릿에서 작업 분할 구조가 읽기 전용으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03384-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="03384-196">프로젝트 계획을 수정하려면 이를 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]에서 만들고 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]에 업데이트로 게시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03384-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="03384-197">참고 항목</span><span class="sxs-lookup"><span data-stu-id="03384-197">See Also</span></span>  
 [<span data-ttu-id="03384-198">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="03384-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
