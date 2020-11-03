---
title: Microsoft Project Client 통합
description: 프로젝트 일정을 계획하고 유지하는 것은 복잡할 수 있으므로 프로젝트 관리자는 이 작업을 관리하는 데 도움이 되는 도구를 사용해야 합니다. Microsoft Project Client와의 통합은 프로젝트 작업 분할 구조를 열고 관리할 수 있도록 지원합니다.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080113"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="43457-104">Microsoft Project Client 통합</span><span class="sxs-lookup"><span data-stu-id="43457-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43457-105">프로젝트 일정을 계획하고 유지하는 것은 복잡할 수 있으므로 프로젝트 관리자는 이 작업을 관리하는 데 도움이 되는 도구를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="43457-106">Microsoft Project Client와의 통합은 프로젝트 작업 분할 구조를 열고 관리할 수 있도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="43457-107">프로젝트 관리자는 변경 사항을 Dynamics 365 Finance 프로젝트 작업 분할 구조에 다시 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="43457-108">7월 업데이트(버전 10.0.4)를 사용하는 경우 KB 4054797 및 4055884를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="43457-109">Microsoft Project Client 추가 기능 구성</span><span class="sxs-lookup"><span data-stu-id="43457-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="43457-110">Microsoft Project Client와의 통합을 활성화하려면 Microsoft Dynamics 365 추가 기능은 사용자의 클라이언트 Microsoft Project 애플리케이션에 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="43457-111">이것은 **프로젝트 관리 작업 공간** 을 열어 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="43457-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="43457-112">•    작업 영역의 **연결** > **설정** 섹션에서 **프로젝트 클라이언트 추가 기능 구성** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="43457-113">•   메시지가 표시되면 **열기** 를 클릭한 다음 **실행** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="43457-114">Microsoft Project Client에서 기존 초안 작업 분할 구조를 열고 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="43457-115">Dynamics 365 Finance의 프로젝트에서 작업 분할 구조가 이미 생성된 경우 작업 분할 구조가 초안 상태인 경우 Microsoft Project Client 응용 프로그램에서 작업 분할 구조를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="43457-116">**프로젝트** 페이지에서 열려면 **계획** 탭에서 **Microsoft Project에서 열기** 링크를 클릭합니다. 이 페이지는 **Microsoft Dynamics 365** 탭에서 **열기** 를 클릭하여 Microsoft Project Client 애플리케이션 내에서 열 수도 있습니다. 목록에서 **법인** 과 **계획** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="43457-117">Internet Explorer를 브라우저로 사용하는 경우 **저장** 을 클릭하여 파일을 다운로드한 위치에서 수동으로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="43457-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="43457-118">또는 **저장 후 열기** 를 클릭하여 Microsoft Project Client에서 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="43457-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="43457-119">저장할 때 파일 이름을 바꾸지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="43457-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="43457-120">Microsoft Project Client를 사용하여 파일을 편집하기 전에 체크아웃해야 합니다. **Microsoft Dynamics 365** 탭에서 **체크아웃** 을 클릭합니다. 이렇게 하면 다른 사용자가 Finance 내에서 동시에 작업 분할 구조를 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="43457-121">편집을 완료한 후 작업 분할 구조를 게시하려면 **Microsoft Dynamics 365** 탭에서 **체크인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="43457-122">프로젝트 팀이 이미 Finance의 프로젝트에 추가된 경우 리소스 목록이 팀 구성원으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="43457-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="43457-123">프로젝트 팀이 아직 프로젝트에 추가되지 않은 경우 **Microsoft Dynamics 365** 탭에서 **리소스** 단추를 클릭하여 리소스를 선택하고 Microsoft Project Client 내에서 팀을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="43457-124">다음 데이터는 체크인 프로세스의 일부로 Finance에 다시 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="43457-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="43457-125">•   작업 이름</span><span class="sxs-lookup"><span data-stu-id="43457-125">•   Task name</span></span>

<span data-ttu-id="43457-126">•   시작 날짜</span><span class="sxs-lookup"><span data-stu-id="43457-126">•   Start date</span></span>

<span data-ttu-id="43457-127">•   완료 날짜</span><span class="sxs-lookup"><span data-stu-id="43457-127">•   Finish date</span></span>

<span data-ttu-id="43457-128">•   선행 업무</span><span class="sxs-lookup"><span data-stu-id="43457-128">•   Predecessors</span></span>

<span data-ttu-id="43457-129">•   리소스 이름</span><span class="sxs-lookup"><span data-stu-id="43457-129">•   Resource names</span></span>

<span data-ttu-id="43457-130">•   범주</span><span class="sxs-lookup"><span data-stu-id="43457-130">•   Category</span></span>

<span data-ttu-id="43457-131">•   리소스 범주</span><span class="sxs-lookup"><span data-stu-id="43457-131">•   Resource category</span></span>

<span data-ttu-id="43457-132">•   근무 시간</span><span class="sxs-lookup"><span data-stu-id="43457-132">•   Work hours</span></span>

<span data-ttu-id="43457-133">•   메모</span><span class="sxs-lookup"><span data-stu-id="43457-133">•   Notes</span></span>

<span data-ttu-id="43457-134">•   우선 순위</span><span class="sxs-lookup"><span data-stu-id="43457-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="43457-135">Microsoft Project Client 파일에 다른 열을 추가하면 파일에 저장되지 않으며 파일을 다시 열 때 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="43457-136">Microsoft Project Client를 사용하여 기존 프로젝트에 대한 작업 분할 구조 만들기</span><span class="sxs-lookup"><span data-stu-id="43457-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="43457-137">Microsoft Project Client를 사용하여 새 작업 분할 구조를 만들려면 다음 단계를 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="43457-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="43457-138">Microsoft Project Client를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="43457-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="43457-139">**Microsoft Dynamics 365** 탭에서 **열기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="43457-140">엔터티에 대한 **법인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="43457-141">**프로젝트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="43457-142">**Microsoft Dynamics 365** 탭에서 **체크아웃** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="43457-143">Finance에 게시할 준비가 되면 **Microsoft Dynamics 365** 탭에서 **체크인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="43457-144">Microsoft Project Client를 사용하여 기존 프로젝트에 대한 기존 작업 분할 구조를 대체</span><span class="sxs-lookup"><span data-stu-id="43457-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="43457-145">Microsoft Project Client를 사용하여 새 작업 분할 구조를 만들고 기존 프로젝트의 기존 작업 분할 구조를 바꾸려면 다음 단계를 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="43457-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="43457-146">Microsoft Project Client를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="43457-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="43457-147">Microsoft Project Client에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43457-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="43457-148">**Microsoft Dynamics 365** 탭에서 **변경 사항 저장** > **기존 프로젝트 바꾸기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="43457-149">엔터티에 대한 **법인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="43457-150">**프로젝트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="43457-151">**확인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="43457-152">Microsoft Project Client 내에서 새 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="43457-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="43457-153">Microsoft Project Client를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="43457-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="43457-154">Microsoft Project Client에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43457-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="43457-155">**Microsoft Dynamics 365** 탭에서 **변경 사항 저장** > **새 프로젝트에 저장** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="43457-156">엔터티에 대한 **법인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="43457-157">필요안 경우 **프로젝트 ID** 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="43457-158">**프로젝트 이름** 을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="43457-159">**프로젝트 유형** , **프로젝트 그룹** 그리고 **프로젝트 계약 ID** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="43457-160">또는 **새로 만들기** 를 클릭하여 새 프로젝트 계약을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43457-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="43457-161">리소스 조달에 사용할 **일정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="43457-162">**확인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="43457-162">Click **OK**.</span></span>
