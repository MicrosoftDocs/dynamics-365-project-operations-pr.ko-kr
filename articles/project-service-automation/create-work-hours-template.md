---
title: 작업 시간 템플릿 만들기
description: 작업 시간 템플릿을 만드는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753303"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="bf1fb-103">작업 시간 서식 파일 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="bf1fb-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bf1fb-104">프로젝트 일정을 만들려면 먼저 모든 휴무 일정을 고려하여 일정에 일자별로 제공할 작업 시간을 정의하는 프로젝트 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="bf1fb-105">일별 작업 시간, 휴무일, 기타 휴무 시간에 대한 자세한 정보를 포함하는 작업 시간 템플릿으로 이를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="bf1fb-106">프로젝트를 만들 때 작업 템플릿을 프로젝트 일정에 연결하여 프로젝트에 대한 일정을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="bf1fb-107">두 가지 방법으로 작업 시간 서식 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="bf1fb-108">리소스 일정에 따라 작업 시간 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="bf1fb-109">새 작업 시간 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="bf1fb-110">리소스 일정에 따라 작업 시간 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="bf1fb-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="bf1fb-111">**Project Service > 리소스**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="bf1fb-112">작업 시간을 기준으로 할 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="bf1fb-113">**다른 이름으로 일정 저장**을 클릭하고 작업 시간 템플릿 이름을 입력한 후 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="bf1fb-114">옵션 변경이 완료되면 **저장 후 닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="bf1fb-115">화면 오른쪽 아래 모서리에서 **저장** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="bf1fb-116">새 작업 시간 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="bf1fb-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="bf1fb-117">**Project Service > 작업 시간 템플릿**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="bf1fb-118">**새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="bf1fb-119">작업 시간 템플릿의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="bf1fb-120">작업 시간을 기준으로 할 리소스를 선택한 다음 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1fb-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bf1fb-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bf1fb-121">See Also</span></span>  
 [<span data-ttu-id="bf1fb-122">리소스 설정</span><span class="sxs-lookup"><span data-stu-id="bf1fb-122">Set up resources</span></span>](../project-service/set-up-resources.md)
