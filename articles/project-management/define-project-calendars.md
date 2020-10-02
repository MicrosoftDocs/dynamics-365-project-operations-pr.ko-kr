---
title: 프로젝트 일정 정의
description: 이 항목은 프로젝트 캘린더를 사용하여 프로젝트 일정을 추적하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897999"
---
# <a name="define-project-calendars"></a><span data-ttu-id="8816c-103">프로젝트 일정 정의</span><span class="sxs-lookup"><span data-stu-id="8816c-103">Define project calendars</span></span>

<span data-ttu-id="8816c-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="8816c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8816c-105">프로젝트 스케줄을 생성하려면 일당 작업 시간 수와 휴무를 정의하는 프로젝트 캘린더 템플릿을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="8816c-106">프로젝트 캘린더 템플릿을 생성하려면 프로젝트를 위한 **Calendar 캘린더 템플릿** 필드와 작업 템플릿을 연계합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="8816c-107">다음 단계에 따라 작업 템플릿을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8816c-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="8816c-108">왼쪽 탐색 창에서 **리소스**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="8816c-109">**리소스** 목록 페이지에서 사용자 레코드를 연 다음 **작업 시간 수 표시**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="8816c-110">브라우저 페이지에서 팝업을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="8816c-111">이렇게 하면 리소스에 대해 설정된 작업 시간 수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="8816c-112">**월별 보기** 탭에서 **설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="8816c-113">세 가지 옵션의 목록이 나타납니다:</span><span class="sxs-lookup"><span data-stu-id="8816c-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="8816c-114">새 주별 일정</span><span class="sxs-lookup"><span data-stu-id="8816c-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="8816c-115">하루 작업 일정</span><span class="sxs-lookup"><span data-stu-id="8816c-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="8816c-116">휴가</span><span class="sxs-lookup"><span data-stu-id="8816c-116">Time Off</span></span>

4. <span data-ttu-id="8816c-117">**새 주별 스케줄**을 선택한 다음 이 리소스 스케줄에 대한 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="8816c-118">되풀이되는 주간 일정, 일일 시간 파라미터, 휴무 등을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="8816c-119">날짜 범위를 설정하고 **저장**을 선택한 다음 **닫기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="8816c-120">**리소스** 목록 페이지로 돌아가서 작업 시간을 설정한 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="8816c-121">**캘린더를 설정**을 선택하여 작업 템플릿을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="8816c-122">**작업 템플릿** 대화 상자에서 작업 템플릿의 명칭을 입력한 다음 **적용**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="8816c-123">이제 작업 템플릿을 프로젝트 스케줄 템플릿과 연계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8816c-123">You can now associate the work template with a project calendar template.</span></span>
