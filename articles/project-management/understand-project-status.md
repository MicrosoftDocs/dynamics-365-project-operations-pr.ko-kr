---
title: 프로젝트 상태 이해
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트에 할당된 상태에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079924"
---
# <a name="understand-project-status"></a><span data-ttu-id="ed080-103">프로젝트 상태 이해</span><span class="sxs-lookup"><span data-stu-id="ed080-103">Understand project status</span></span>

<span data-ttu-id="ed080-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="ed080-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ed080-105"> **프로젝트 엔터티** 페이지의 **상태** 섹션은 비용과 노력에 따라 프로젝트 상태에 대한 요약을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="ed080-106">상태 요약 필드</span><span class="sxs-lookup"><span data-stu-id="ed080-106">Status summary fields</span></span>

- <span data-ttu-id="ed080-107"> **전체 프로젝트 상태** 필드는 프로젝트의 전체 상태를 표시하는 편집 가능한 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="ed080-108">이 필드는 녹색, 노란색 및 빨간색과 같은 색상 코딩을 사용하여 위험 증가를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="ed080-109"> **주석** 필드를 사용하면 프로젝트 관리자가 상태에 대한 특정 주석을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="ed080-110"> **상태 업데이트 날짜** 필드는 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="ed080-111">이 필드의 값은 상태가 마지막으로 업데이트된 시기를 나타내는 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="ed080-112"> **일정 성능** 및 **비용 성능** 필드는 추적 그리드부터 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="ed080-113"> **작업량 추적** 보기에서 루트 노드의 일정 및 비용 차이가 양수인 경우 이러한 필드를  **선행** 으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="ed080-114">루트 노드의 일정 및 비용 차이가 음수인 경우 이러한 필드는  **후행** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed080-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
