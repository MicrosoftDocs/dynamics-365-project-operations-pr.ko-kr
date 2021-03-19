---
title: 작업 그리드에서 작업 문제 해결
description: 이 토픽은 작업 그리드에서 작업할 때 필요한 문제 해결 정보를 제공합니다.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286571"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="74b14-103">작업 그리드에서 작업 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74b14-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="74b14-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="74b14-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74b14-105">이 토픽은 비용 관리 작업 중에 발생할 수 있는 문제를 해결하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="74b14-106">쿠키 활성화</span><span class="sxs-lookup"><span data-stu-id="74b14-106">Enable cookies</span></span>

<span data-ttu-id="74b14-107">Project Operations에서는 작업 분할 구조를 렌더링하기 위해 타사 쿠키를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="74b14-108">타사 쿠키가 활성화되지 않은 경우 작업이 표시되는 대신 **프로젝트** 페이지에서 **작업** 탭을 선택하면 빈 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![타사 쿠키가 활성화되지 않은 경우 빈 탭](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="74b14-110">해결 방법</span><span class="sxs-lookup"><span data-stu-id="74b14-110">Workaround</span></span>
<span data-ttu-id="74b14-111">Microsoft Edge 또는 Google Chrome 브라우저의 경우 다음 절차는 타사 쿠키를 사용하도록 브라우저 설정을 업데이트하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="74b14-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="74b14-112">Microsoft Edge</span></span>

1. <span data-ttu-id="74b14-113">Edge 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="74b14-114">오른쪽 상단에서 **줄임표**(...)를 선택한 다음 **설정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="74b14-115">**쿠키 및 사이트 권한** 아래에서 **쿠키 및 사이트 데이터** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="74b14-116">**타사 쿠키 차단** 을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="74b14-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="74b14-117">Google Chrome</span></span>

1. <span data-ttu-id="74b14-118">Chrome 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="74b14-119">오른쪽 상단에서 세 개의 수직 점을 선택한 다음 **설정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="74b14-120">**개인 정보 및 보안** 아래에서 **쿠키 및 기타 사이트 데이터** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="74b14-121">**모든 쿠키 허용** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74b14-122">타사 쿠키를 차단하면 해당 사이트가 예외 목록에서 허용되더라도 다른 사이트의 모든 쿠키 및 사이트 데이터가 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="74b14-123">PEX 끝점</span><span class="sxs-lookup"><span data-stu-id="74b14-123">PEX Endpoint</span></span>

<span data-ttu-id="74b14-124">Project Operations를 위해서는 프로젝트 매개 변수가 PEX 끝점을 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="74b14-125">이 끝점은 작업 분할 구조를 렌더링하는 데 사용되는 서비스와 통신하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="74b14-126">매개 변수가 활성화되지 않은 경우 "프로젝트 매개 변수가 유효하지 않습니다."라는 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="74b14-127">해결 방법</span><span class="sxs-lookup"><span data-stu-id="74b14-127">Workaround</span></span>
 ![프로젝트 매개 변수의 PEX 끝점 필드](media/projectparameter.png)

1. <span data-ttu-id="74b14-129">**PEX 끝점** 필드를 **프로젝트 매개 변수** 페이지에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="74b14-130">다음 값으로 필드를 업데이트합니다: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="74b14-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="74b14-131">**프로젝트 매개 변수** 페이지에서 필드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="74b14-132">웹에 대한 프로젝트 권한</span><span class="sxs-lookup"><span data-stu-id="74b14-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="74b14-133">Project Operations는 외부 일정 서비스에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="74b14-134">이 서비스를 사용하려면 사용자에게 작업 분할 구조와 관련된 엔터티를 읽고 쓰기 위해 할당된 여러 역할이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="74b14-135">이러한 엔터티에는 프로젝트 작업, 리소스 할당 및 작업 종속성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="74b14-136">**작업** 탭으로 이동할 때 사용자가 작업 분할 구조를 렌더링할 수 없는 경우 Project Operations를 위한 프로젝트가 활성화되지 않았기 때문일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="74b14-137">사용자는 보안 역할 오류 또는 액세스 거부와 관련된 오류를 수신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="74b14-138">해결 방법</span><span class="sxs-lookup"><span data-stu-id="74b14-138">Workaround</span></span>

1. <span data-ttu-id="74b14-139">**설정 > 보안 > 사용자 > 응용 프로그램 사용자** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![응용 프로그램 판독기](media/applicationuser.jpg)
   
2. <span data-ttu-id="74b14-141">응용 프로그램 사용자 레코드를 두 번 클릭하여 다음을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="74b14-142">사용자는 프로젝트에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-142">The user has access to the project.</span></span> <span data-ttu-id="74b14-143">이 확인은 일반적으로 사용자가 **프로젝트 관리자** 보안 역할이 있는지 확인하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="74b14-144">Microsoft Project 응용 프로그램 사용자가 존재하고 올바르게 구성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="74b14-145">이 사용자가 없으면 새 사용자 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="74b14-146">**새 사용자** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-146">Select **New Users**.</span></span> <span data-ttu-id="74b14-147">입력 양식을 **응용 프로그램 사용자** 로 변경한 다음 **응용 프로그램 ID** 를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![응용 프로그램 사용자 세부 정보](media/applicationuserdetails.jpg)

4. <span data-ttu-id="74b14-149">사용자에게 올바른 라이선스가 할당되었으며 라이선스의 서비스 계획 세부 정보에서 서비스가 활성화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="74b14-150">사용자가 project.microsoft.com을 열 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="74b14-151">시스템이 올바른 프로젝트 끝점을 가리키고 있는지 프로젝트 매개 변수를 통해 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="74b14-152">프로젝트 응용 프로그램 사용자가 만들어졌는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="74b14-153">사용자에게 다음 보안 역할을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="74b14-154">Dataverse 사용자</span><span class="sxs-lookup"><span data-stu-id="74b14-154">Dataverse User</span></span>
  - <span data-ttu-id="74b14-155">Project Operations 시스템</span><span class="sxs-lookup"><span data-stu-id="74b14-155">Project Operations System</span></span>
  - <span data-ttu-id="74b14-156">프로젝트 시스템</span><span class="sxs-lookup"><span data-stu-id="74b14-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="74b14-157">작업 분할 구조를 업데이트할 때 오류 발생</span><span class="sxs-lookup"><span data-stu-id="74b14-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="74b14-158">작업 분할 구조를 하나 이상 업데이트하면 변경 사항이 결국 실패하고 저장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="74b14-159">일정표에서 "최근 변경 사항을 저장할 수 없습니다."라는 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="74b14-160">해결 방법</span><span class="sxs-lookup"><span data-stu-id="74b14-160">Workaround</span></span>

1. <span data-ttu-id="74b14-161">사용자에게 올바른 라이선스가 할당되었으며 라이선스의 서비스 계획 세부 정보에서 서비스가 활성화되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="74b14-162">사용자가 project.microsoft.com을 열 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="74b14-163">시스템이 올바른 프로젝트 끝점을 가리키고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="74b14-164">프로젝트 응용 프로그램 사용자가 만들어졌는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="74b14-165">사용자에게 다음 보안 역할을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="74b14-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="74b14-166">Dataverse사용자 또는 기본 사용자</span><span class="sxs-lookup"><span data-stu-id="74b14-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="74b14-167">Project Operations 시스템</span><span class="sxs-lookup"><span data-stu-id="74b14-167">Project Operations System</span></span>
  - <span data-ttu-id="74b14-168">프로젝트 시스템</span><span class="sxs-lookup"><span data-stu-id="74b14-168">Project System</span></span>
  - <span data-ttu-id="74b14-169">Project Operations 이중 쓰기 시스템(이 역할은 Project Operations의 리소스/비 재고 기반 시나리오를 배포하는 경우 필요합니다.)</span><span class="sxs-lookup"><span data-stu-id="74b14-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]