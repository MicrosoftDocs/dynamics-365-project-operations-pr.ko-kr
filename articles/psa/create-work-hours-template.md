---
title: 작업 시간 템플릿 만들기
description: 이 항목에서는 Project Service에서 작업 시간 템플릿을 만드는 방법에 대해 설명합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981263"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="64579-103">작업 시간 서식 파일 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="64579-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="64579-104">프로젝트를 만들고 관리하려면 프로젝트에 일정 템플릿을 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="64579-105">일정 템플릿은 다음 프로젝트 속성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="64579-106">시작 및 종료 시간을 포함한 근무 시간</span><span class="sxs-lookup"><span data-stu-id="64579-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="64579-107">근무일</span><span class="sxs-lookup"><span data-stu-id="64579-107">Working days</span></span>
- <span data-ttu-id="64579-108">휴무일과 같은 일정 예외</span><span class="sxs-lookup"><span data-stu-id="64579-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="64579-109">프로젝트에 적용되는 일정 템플릿은 조직의 설정에 정의된 캘린더 템플릿의 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="64579-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="64579-110">일정 템플릿을 변경하면 해당 변경 사항이 프로젝트의 작업 시간에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64579-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="64579-111">프로젝트의 근무 시간을 변경하려면 새 템플릿을 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="64579-112">조직의 일정 템플릿을 만들려면 두 가지 주요 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64579-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="64579-113">예약 가능한 신규 또는 기존 리소스를 사용하여 템플릿의 원하는 근무 시간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="64579-114">새 일정 템플릿을 만들고 템플릿을 예약 가능한 리소스와 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="64579-115">**템플릿의 근무 시간 정의**</span><span class="sxs-lookup"><span data-stu-id="64579-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="64579-116">**리소스** \> **리소스** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="64579-117">일정 템플릿에서 참조할 새 리소스를 만들거나 기존 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="64579-118">리소스의 **작업 시간** 탭을 선택하고 [리소스에 대한 작업 시간 설정](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)의 지침을 완료하여 일정 규칙을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="64579-119">**새 일정 템플릿 만들기**</span><span class="sxs-lookup"><span data-stu-id="64579-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="64579-120">**설정** \> **일정 템플릿** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="64579-121">**새로 만들기** 를 클릭하고 이름, 설명 및 템플릿 리소스를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="64579-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="64579-122">일정 템플릿에서 리소스가 참조되면 리소스 일정의 복사본이 일정 템플릿과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="64579-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="64579-123">복사된 템플릿의 근무 시간이 변경되면 해당 변경 사항이 일정 템플릿에 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64579-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="64579-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="64579-124">See Also</span></span>  
 [<span data-ttu-id="64579-125">리소스 설정</span><span class="sxs-lookup"><span data-stu-id="64579-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
