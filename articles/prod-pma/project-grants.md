---
title: 프로젝트 보조금
description: 이 항목은 보조금을 생성하거나 수정하는 방법을 설명합니다.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289377"
---
# <a name="project-grants"></a><span data-ttu-id="ccfd5-103">프로젝트 권한 부여</span><span class="sxs-lookup"><span data-stu-id="ccfd5-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccfd5-104">보조금은 특정 목적이나 프로젝트를 위한 금전적 선물입니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="ccfd5-105">일반적으로 보조금 사용 방법에는 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="ccfd5-106">프로젝트 관리 및 회계에서 보조금을 입력 및 추적하고 프로젝트 및 프로젝트 계약에 대한 관계를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="ccfd5-107">예를 들어 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="ccfd5-108">**프로젝트** 및 **프로젝트 계약 세부 정보** 페이지의 링크를 통해 보조금을 프로젝트 및 자금 출처와 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="ccfd5-109">한 상태에서 다른 상태로 이동할 때 보조금에 대한 변경 사항을 입력하고 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="ccfd5-110">비용, 요청 금액 및 지급 금액을 입력하고 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="ccfd5-111">마스터 보조금을 만들고 하위 보조금을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="ccfd5-112">새 레코드에 모든 세부 정보를 입력하여 보조금을 만들거나 기존 보조금에서 세부 정보를 복사한 다음 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="ccfd5-113">새 보조금 만들기</span><span class="sxs-lookup"><span data-stu-id="ccfd5-113">Create a new grant</span></span>

1. <span data-ttu-id="ccfd5-114">**프로젝트 관리 및 회계** \> **보조금** \> **보조금** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ccfd5-115">**새로 만들기**\>**보조금** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="ccfd5-116">보조금 세부 정보 페이지의 **일반** 빠른 탭의 **보조금 ID** 필드에 보조금에 대한 영숫자 식별자를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="ccfd5-117">**보조금 이름** 필드에 보조금의 고유 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="ccfd5-118">**설명** 필드에 새 보조금에 대한 세부 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="ccfd5-119">페이지에 있는 대부분의 다른 필드는 선택 사항이며 원하는 만큼 정보를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="ccfd5-120">다음 목록은 보조금 세부 정보 페이지의 각 빠른 탭에 지정된 정보를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="ccfd5-121">**일반** – 보조금 이름, 상태, 설명, 목적 및 금액을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="ccfd5-122">**연락처 정보** – 직원, 보조금을 관리하는 부서, 보조금 고객 또는 보조금의 조직 출처에 대한 세부 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="ccfd5-123">또한 조직이 보조금을 받은 후 다른 받는 사람에게 전달하는 통과 엔터티인지 여부를 나타낼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="ccfd5-124">**추가** 를 선택하여 보조금을 제공하는 조직의 전화 번호 및 이메일 주소와 같은 연락처 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="ccfd5-125">**날짜 및 마감일** – 보조금 및 보조금 신청과 관련된 날짜를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="ccfd5-126">예를 들어 신청 마감일, 제출일 및 보조금 승인 또는 거부 날짜가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="ccfd5-127">**관련 프로젝트 및 프로젝트 계약** – **일반** 빠른 탭의 **보조금 상태** 필드가 **활성** 또는 **부여됨** 으로 설정된 경우에만 이 빠른 탭에 정보를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="ccfd5-128">다음 옵션 중에서 선택하여 관련 작업을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="ccfd5-129">**자금 출처 추가** – 보조금에 대한 새로운 자금 출처를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="ccfd5-130">지금 모든 세부 정보를 입력하거나 기본 정보를 사용한 다음 나중에 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="ccfd5-131">**프로젝트 계약 추가** – 프로젝트 계약 정보를 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="ccfd5-132">**프로젝트 추가** – 프로젝트 세부 정보를 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="ccfd5-133">**설정** –이 정보가 필요한 경우 일치 자금에 대한 세부 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="ccfd5-134">보조금을 수여하는 많은 조직은 수혜자가 보조금으로 수여되는 금액과 일치하도록 자신의 특정 금액이나 자원을 지출하도록 요구합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="ccfd5-135">**로컬 프로젝트 또는 추적 ID** 필드에 프로젝트 식별자와 다른 식별자를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccfd5-136">보조금의 일부가 다른 조직에 수여될 경우 **하위 교부 기관** 옵션을 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="ccfd5-137">미국에서 수여되는 보조금의 경우 보조금이 주 또는 연방 명령에 따라 수여되는지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="ccfd5-138">**드로우다운 세부 정보** – 보조금을 인출, 청구 또는 지출할 수 있는 빈도에 대한 정보를 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="ccfd5-139">사본에서 새 보조금 만들기</span><span class="sxs-lookup"><span data-stu-id="ccfd5-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="ccfd5-140">**프로젝트 관리 및 회계** \> **보조금** \> **보조금** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ccfd5-141">**새로 만들기**\>**보조금에서 복사** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="ccfd5-142">영숫자 식별자와 새 보조금 이름을 입력한 다음 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="ccfd5-143">부여 세부 정보 페이지에서 복사된 부여의 세부 정보를 검토하고 필요한 사항을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="ccfd5-144">페이지에 있는 대부분의 필드는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="ccfd5-145">보조금 세부 정보 보기 또는 수정</span><span class="sxs-lookup"><span data-stu-id="ccfd5-145">View or modify grant details</span></span>

1. <span data-ttu-id="ccfd5-146">**프로젝트 관리 및 회계** \> **보조금** \> **보조금** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ccfd5-147">수정할 보조금을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="ccfd5-148">작업 창의 **보조금** 탭에 있는 **유지 관리** 그룹에서 **편집** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="ccfd5-149">보조금 세부 정보를 검토하고 필요한 사항을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ccfd5-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]