---
title: 완료 시 추정 비용 업데이트
description: 이 항목은 프로젝트에 대한 노력의 예측 업데이트에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127211"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="414ae-103">완료 시 추정 비용 업데이트</span><span class="sxs-lookup"><span data-stu-id="414ae-103">Update estimate at completion</span></span>

<span data-ttu-id="414ae-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="414ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="414ae-105">프로젝트 관리자는 작업에 대한 원래 예상을 수정하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="414ae-106">프로젝트 재추정은 프로젝트의 현재 상태를 고려할 때 프로젝트 관리자의 예상에 대한 인식입니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="414ae-107">하지만, 프로젝트 관리자가 기본 수치를 변경하는 것은 권장하지 않습니다. 프로젝트 기본 수치는 프로젝트의 일정 및 비용에 대해 구비된 실제 자원이며, 모든 프로젝트 이해 관계자가 동의했기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="414ae-108">프로젝트 관리자가 작업에 대한 작업량을 다시 프로젝트할 수 있는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="414ae-109">작업에 실제 남은 작업량의 새 예상값으로 기본 완료 추정 비용(ETC)을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="414ae-110">작업의 실제 진행률의 새 예상값으로 기본 진행률을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="414ae-111">이러한 각 접근 방식은 작업의 ETC, 작업 완료 시 추정 비용(EAC) 및 진행률을 다시 계산하고 작업에 추정된 작업량 차이를 발생하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="414ae-112">요약 작업에 대한 EAC, ETC 및 진행률 비율이 다시 계산되고 작업량 차이의 새로운 추정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="414ae-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
