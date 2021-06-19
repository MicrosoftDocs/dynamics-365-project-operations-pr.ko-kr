---
title: 프로젝트 계약 관리
description: 이 항목은 프로젝트 기반 계약 보기에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003099"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="fa555-103">프로젝트 계약 관리</span><span class="sxs-lookup"><span data-stu-id="fa555-103">Manage project contracts</span></span>

<span data-ttu-id="fa555-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="fa555-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa555-105">Dynamics 365 Project Operations의 프로젝트 계약은 프로젝트의 약정 및 청구 세부 정보에 대해 계약상 합의된 내용을 캡처하고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="fa555-106">Project Operations의 프로젝트 계약 구조는 다음 구성 요소를 사용하여 프로젝트 기반 작업에 맞게 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="fa555-107">프로젝트 송장에서 상위 수준 구성 요소로 표시될 작업의 개별 구성 요소를 식별하는 계약 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="fa555-108">각 상위 수준 구성 요소 또는 계약 내용에 대한 작업을 식별하고 추정하는 계약 내용 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="fa555-109">추정에는 계약 내용에 연결된 작업에 대한 일정 및 재정적 측면이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="fa555-110">계약 모델 및 청구 가능 구성 요소는 각 계약 내용 및 전체 계약에 대한 청구 약정을 보유하는 각 계약 내용에 대해 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="fa555-111">모든 프로젝트 기반 계약 보기</span><span class="sxs-lookup"><span data-stu-id="fa555-111">View all project-based contracts</span></span>

<span data-ttu-id="fa555-112">모든 프로젝트 계약 목록은 **견적** 목록 페이지에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="fa555-113">**영업** > **연락처** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="fa555-114">시스템의 모든 프로젝트 계약 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="fa555-115">**보기 전환기**(보기 이름 옆의 드롭다운 화살표)를 선택하여 다른 필터링된 보기를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="fa555-116">사용자 지정 필터 기준을 사용하여 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="fa555-117">이 목록 페이지 또는 세부 사항 페이지에서 계약을 작성하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa555-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]