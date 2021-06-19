---
title: 시간 항목 캘린더
description: 이 주제는 시간 항목 캘린더를 사용하드는 방법에 대한 정보를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3efa30f017643cbcf7baa72f8ab964091c9e4f28
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013089"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="eca0a-103">시간 항목 캘린더</span><span class="sxs-lookup"><span data-stu-id="eca0a-103">Time entry calendar</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eca0a-104">**시간 항목** 페이지에서 **표시** \> **캘린더 컨트롤** 을 선택하여 캘린더에서 시간 항목을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="eca0a-105">업데이트된 캘린더 컨트롤</span><span class="sxs-lookup"><span data-stu-id="eca0a-105">Updated calendar control</span></span>

<span data-ttu-id="eca0a-106">Dynamics 365 Project Service Automation은 새롭고 확장 가능한 시간 항목 경험을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="eca0a-107">이 새 환경은 이전 버전에서 사용된 맞춤 캘린더 컨트롤을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="eca0a-108">그러나 통합 인터페이스 프레임워크가 일일, 주간 또는 월별 보기에 대해 제공하는 읽기 전용 캘린더 컨트롤을 통해 시간 항목을 계속 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="eca0a-109">캘린더는 개별 캘린더 항목에 대한 조치를 지원하지 않기 때문에 제출 또는 삭제를 위해 하나 이상의 캘린더 항목을 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="eca0a-110">그 대신, 요구되는 조치를 완료할 수 있는 **시간 항목** 엔터티 페이지를 열려면 캘린더 항목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="eca0a-111">확장성</span><span class="sxs-lookup"><span data-stu-id="eca0a-111">Extensibility</span></span>

<span data-ttu-id="eca0a-112">시간 항목 그리드가 있는 **시간 항목** 페이지에서 맞춤 필드를 추가하고 조회 필드를 설정하고 맞춤 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="eca0a-113">맞춤 필드에 선택되거나 입력된 값을 기반으로 하는 맞춤 비즈니스 논리를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca0a-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]