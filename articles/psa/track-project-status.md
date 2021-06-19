---
title: 프로젝트 상태 추적
description: 프로젝트 상태를 추적하는 방법(Project Service)
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014394"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="925fd-103">프로젝트 상태 추적(Project Service) </span><span class="sxs-lookup"><span data-stu-id="925fd-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="925fd-104">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]를 사용하여 클라이언트의 프로젝트 진행 상황을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="925fd-105">업무 진행 시, 프로젝트 단계가 업무 스테이지를 반영하여 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="925fd-106">**새로 만들기**</span><span class="sxs-lookup"><span data-stu-id="925fd-106">**New**</span></span>    | <span data-ttu-id="925fd-107">프로젝트 생성 시, 스테이지는 **새로 만들기** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="925fd-108">템플릿에서 프로젝트를 만드는 경우, 이 스테이지에서는 프로젝트에 일정, 추정 및 팀 데이터가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="925fd-109">그렇지 않을 경우, 프로젝트 개요가 되며 나머지 프로젝트 구성 요소를 직접 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="925fd-110">**견적**</span><span class="sxs-lookup"><span data-stu-id="925fd-110">**Quote**</span></span>   |      <span data-ttu-id="925fd-111">프로젝트를 견적에 연결하거나 견적에서 프로젝트를 만들 경우, 프로젝트 스테이지가 **견적** 으로 설정되며 예상 시작 및 종료 날짜도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="925fd-112">프로젝트 진행 단계가 견적 스테이지일 경우, 견적 세부 항목이 **프로젝트** 페에지의 **영업** 탭에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="925fd-113">**계획**</span><span class="sxs-lookup"><span data-stu-id="925fd-113">**Plan**</span></span>   |                                     <span data-ttu-id="925fd-114">프로젝트와 연결된 견적에 대한 판매 승인을 받고 업무 진행 상황이 계약서 스테이지인 경우, 프로젝트 스테이지가 **계획** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="925fd-115">계약서 세부 항목은 **프로젝트** 페이지의 **영업** 탭에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="925fd-116">**완료됨**</span><span class="sxs-lookup"><span data-stu-id="925fd-116">**Complete**</span></span> |                    <span data-ttu-id="925fd-117">프로젝트 작업이 완료되면, 스테이지를 **완료됨** 으로 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="925fd-118">프로젝트 스테이지가 완료됨으로 설정되면, 작업이 100% 완료된 것으로 인식되지만 보류 시간 동안 또는 경비 기입이 기록될 때까지 프로젝트가 열려있는 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="925fd-119">**닫기**</span><span class="sxs-lookup"><span data-stu-id="925fd-119">**Close**</span></span>   |           <span data-ttu-id="925fd-120">모든 트랜젝션이 프로젝트에 기록되고 더 이상 기록할 것이 없을 것으로 예상될 경우, 직접 스테이지를 **종료** 로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="925fd-121">프로젝트가 **종료** 로 설정되면, 프로젝트에 대한 추가 트랜잭션을 기록할 수 없고 프로젝트는 일기 전용 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="925fd-122">프로젝트 상태 추적 방법</span><span class="sxs-lookup"><span data-stu-id="925fd-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="925fd-123">**Project Service > 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="925fd-124">작업을 원하는 프로젝트를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="925fd-125">화면 상단 표시줄에서 프로젝트 이름 옆의 아래로 향하는 화살표를 선택한 다음 **프로젝트 추적** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="925fd-126">작업 목록 위 드롭다운 목록에서 **작업량 추적** 또는 **비용 추적** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="925fd-127">편집할 업무를 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-127">Double-click any task to edit it.</span></span> <span data-ttu-id="925fd-128">또한, Gantt 차트의 막대를 움직이거나 크기를 조정하여 시간과 작업 진행 상황을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925fd-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="925fd-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="925fd-129">See Also</span></span>  
 [<span data-ttu-id="925fd-130">프로젝트 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="925fd-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]