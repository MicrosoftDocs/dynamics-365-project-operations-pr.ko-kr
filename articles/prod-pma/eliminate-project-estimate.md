---
title: 프로젝트 추정 제거
description: 이 항목은 완료된 후 프로젝트 추정을 제거하는 방법에 대한 정보를 제공합니다.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080105"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="08314-103">프로젝트 추정 제거</span><span class="sxs-lookup"><span data-stu-id="08314-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08314-104">프로젝트 추산은 프로젝트에 대해 추정되고 스케줄이 잡힌 작업에 대한 재무적인 내용을 볼 수 있게 해 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08314-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="08314-105">프로젝트에 대한 견적 작업을 하려면 프로젝트를 견적 프로젝트에 첨부해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="08314-106">견적 프로젝트는 항상 기존 프로젝트를 기반으로 하지만 여러 프로젝트가 단일 견적 프로젝트를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08314-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="08314-107">프로젝트 견적에는 고정 가격 및 투자 프로젝트만 첨부할 수 있으며 해당 프로젝트는 견적 프로젝트와 동일한 프로젝트 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="08314-108">견적 프로젝트를 제거하려면 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="08314-109">다음 단계는 추정을 제거하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="08314-110">**프로젝트 관리 및 회계** > **모든 프로젝트** 로 이동하고 프로젝트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="08314-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="08314-111">**관리** 탭에서 **추정** 을 선택하고 **추정** 페이지에서 **제거** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="08314-112">**추정 제거** 페이지의 **일반** 탭에서 다음 옵션을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="08314-113">**기간 코드** : 기간 코드를 선택하여 적절한 견적 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="08314-114">**추정 날짜** : 제거를 위한 적절한 추정 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="08314-115">**WIP 경고로 제거** : 진행 중인 작업(WIP)과 연관된 추정이 제거될 때 알림을 제공하려면 이 옵션을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="08314-116">이 옵션을 사용하지 않으면 예상되지 않은 트랜잭션이 있는 경우 제거를 계속할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="08314-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="08314-117">이 옵션은 추정 프로젝트에 제거가 적용된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08314-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="08314-118">주기적 전기를 사용하는 경우 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="08314-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="08314-119">이 설정은 **프로젝트 매개 변수** 페이지의 **추정** 탭, **예상되지 않은 트랜잭션이 있을 때 제거 허용** 필드 그룹에서 설정 작업을 합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="08314-120">**스테이지를 완료로 설정** : 제거를 실행한 후 추정 프로젝트의 스테이지를 **완료됨** 으로 설정하려면 이 옵션을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="08314-121">**추정 목록 인쇄** : 추정 목록 인쇄시 포함할 정보를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="08314-122">**정보 로그 표시** : 정보 로그를 표시하려면 이 옵션을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="08314-123">**전기 날짜** : 추정의 원장 전기 날짜를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="08314-124">**확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-124">Select **OK**.</span></span>
5. <span data-ttu-id="08314-125">제거 프로세스가 완료되면 제거된 추정 프로젝트가 음수 값으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08314-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="08314-126">추정을 제거하지 않으려는 경우 제거된 추정을 선택하고 **역 제거** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="08314-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
