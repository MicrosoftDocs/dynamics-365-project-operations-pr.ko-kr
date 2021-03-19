---
title: 작업 및 프로젝트 팀에 일반 예약 가능한 리소스 할당
description: 이 항목은 작업 및 프로젝트 팀에 일반 리소스를 예약하는 것에 대한 정보를 제공합니다.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291402"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="34c26-103">작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성</span><span class="sxs-lookup"><span data-stu-id="34c26-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="34c26-104">프로젝트에 명명된 리소스 또는 실제 리소스를 예약하고 할당하는 것 외에도 프로젝트 작업에 일반 리소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="34c26-105">이러한 리소스는 프로젝트에 명명된 리소스로 충원할 준비가 될 때까지 명명된 리소스를 위한 자리 표시자 역할을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="34c26-106">Project Service Automation(PSA)에서 **프로젝트** 페이지를 열고 **스케줄** 탭에서 스케줄의 **리소스** 셀에 일반 리소스의 직함을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="34c26-107">또는 셀의 **리소스** 아이콘을 클릭하여 리소스 선택기를 연 다음 만들려는 일반 리소스의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![일반 팀원 생성 및 할당](media/RM-how-to-9.png)

<span data-ttu-id="34c26-109">그러면 **빠른 생성: 프로젝트 팀원** 패널이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="34c26-110">일반 리소스 팀원의 역할 및 조직 단위를 입력한 다음 **저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![일반 팀원 빠른 생성](media/RM-how-to-10.png)

3. <span data-ttu-id="34c26-112">새 일반 리소스 팀원을 만든 후 작업에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="34c26-113">해당 일반 리소스를 작업 스케줄의 다른 작업에 계속 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![기존 일반 팀원을 작업에 할당](media/RM-how-to-11.png)

4. <span data-ttu-id="34c26-115">일반 리소스를 할당한 후 리소스 요건을 생성하고 리소스 관리자에게 리소스 요청을 직접 예약하거나 제출하여 리소스 요건을 충족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![일반 팀원에 대한 요건 생성](media/RM-how-to-12.png)

<span data-ttu-id="34c26-117">팀원 그리드에서 위에서 설명한 대로 리소스 선택기를 사용할 수 있을 뿐만 아니라 일반 리소스를 직접 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="34c26-118">리소스는 **빠른 생성: 프로젝트 팀원** 패널에 지정된 시작/종료 날짜 및 할당 방법에 근거한 리소스 요건과 함께 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="34c26-119">일반 팀원을 직접 추가한 다음 일반 리소스에 요구되는 시간보다 더 많은 작업을 할당하는 경우 차이점을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="34c26-120">**요건 생성** 을 클릭해 요건을 다시 생성하여 요구되는 시간을 할당과 균형을 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="34c26-121">또한 팀 그리드에서 **리소스 요건** 링크를 클릭하여 요건을 열고 기능, 선호 리소스 등을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![리소스 요구 사항](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]