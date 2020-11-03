---
title: 연방지원금 지출계획 조회
description: 이 항목은 연방지원금 지출계획 조회에 대한 정보를 제공합니다.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080036"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5a2d4-103">연방지원금 지출계획 조회</span><span class="sxs-lookup"><span data-stu-id="5a2d4-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a2d4-104">관리 예산처 회람 A-133에 따르면, 연방 기금을 받는 기관은 단일 감사라고도 하는 감사 요건의 적용을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="5a2d4-105">감사 프로세스는 연방 지원금의 수입 및 지출을 반복적으로 보고하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="5a2d4-106">단일 감사 보고서에는 SEFA(연방지원금 지출계획)가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="5a2d4-107">연방지원금 지출계획 조회에는 연방 정부 지원 목록(CFDA) 제목과 번호, 보조금 번호, 보조금 연도, 보조금을 제공하는 연방 기관 이름 및 도관 기업(pass-through entity)의 이름이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="5a2d4-108">조회는 특정 기간 동안 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="5a2d4-109">일반적으로 이 기간은 회계 연도인 재무 제표 기간과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="5a2d4-110">조회에는 선택한 날짜 범위의 예상 날짜가 있는 보조금이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="5a2d4-111">조회의 **교부 기관** 열에는 보조금 고객 또는 도관 보조금의 경우 교부 기관이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="5a2d4-112">도관 보조금의 경우 **도관 기관** 열에는 보조금 고객이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="5a2d4-113">보조금이 도관 보조금이 아닌 경우 **도관 기관** 열은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="5a2d4-114">CFDA 클러스터 설정</span><span class="sxs-lookup"><span data-stu-id="5a2d4-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="5a2d4-115">연방지원금 지출계획 조회의 CFDA 번호와 연관될 수 있는 CFDA 클러스터를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="5a2d4-116">**프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 연방 정부 지원 목록 클러스터** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="5a2d4-117">**새로 만들기** 를 선택하여 CFDA 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="5a2d4-118">클러스터 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="5a2d4-119">**저장** 을 선택하여 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="5a2d4-120">CFDA 번호 설정</span><span class="sxs-lookup"><span data-stu-id="5a2d4-120">Set up CFDA numbers</span></span>

<span data-ttu-id="5a2d4-121">보조금에 추가할 수 있는 CFDA 번호를 설정하고 연방지원금 지출계획 조회에 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="5a2d4-122">**프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 연방 정부 지원 목록 번호** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="5a2d4-123">**새로 만들기** 를 선택하여 CFDA 번호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="5a2d4-124">**번호** 열에 CFDA 번호를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="5a2d4-125">**Tab** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="5a2d4-126">**설명** 열에 CFDA 제목을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="5a2d4-127">**Tab** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="5a2d4-128">선택 사항: **프로그램 클러스터** 필드에서 적절한 CFDA 클러스터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="5a2d4-129">**저장** 을 선택하여 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5a2d4-130">연방지원금 지출계획 조회에 대해 보고할 보조금 설정</span><span class="sxs-lookup"><span data-stu-id="5a2d4-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="5a2d4-131">**프로젝트 관리 및 회계 \> 보조금 \> 보조금** 으로 이동하고 기존 보조금을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="5a2d4-132">**설정** 빠른 탭의  **연방 정부 지원 목록** 필드에서 CFDA 번호를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="5a2d4-133">보조금의 CFDA 번호는 보고할 CFDA 클러스터를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="5a2d4-134">**연락처 정보** 빠른 탭에서 다음 단계에 따라 교부 기관 정보를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="5a2d4-135">**보조금 고객** 필드에 보조금을 담당하는 고객을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="5a2d4-136">기존 보조금의 경우 이 정보가 이미 입력되었을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="5a2d4-137">보조금 고객이 자금 제공자인지 여부를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="5a2d4-138">보조금 고객이 자금 제공자인 경우 **도관** 확인란을 선택 취소 상태로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="5a2d4-139">다른 고객이 자금 제공자이고 보조금 고객이 자금 지출 및 추적을 담당하는 경우 **도관** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="5a2d4-140">이전 단계에서 **도관** 확인란을 선택한 경우 **교부 기관** 필드에 보조금을 제공한 고객을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="5a2d4-141">교부 기관과 보조금 고객은 동일한 고객일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="5a2d4-142">다음은 도관 보조금의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="5a2d4-143">연방 정부가 주를 위한 인프라 프로젝트에 자금을 지원했습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="5a2d4-144">연방 정부가 주에 지출할 자금을 제공했습니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="5a2d4-145">이 경우 연방 정부가 교부 기관이고 주가 보조금 고객입니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="5a2d4-146">이 기능을 처음 켜면 보조금에 있는 기존 번호를 사용하여 초기 CFDA 번호가 입력됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="5a2d4-147">보조금 유형에 따라 SEFA 보고에서 보조금 제외</span><span class="sxs-lookup"><span data-stu-id="5a2d4-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="5a2d4-148"> **프로젝트 관리 및 회계 \> 설정 \> 보조금 \> 보조금 유형** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="5a2d4-149"> **기본 정보** 빠른 탭에서  **연방지원금 지출계획에서 제외** 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="5a2d4-150">**저장** 을 선택하여 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5a2d4-151">연방지원금 지출계획 조회 실행</span><span class="sxs-lookup"><span data-stu-id="5a2d4-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="5a2d4-152">**프로젝트 관리 및 회계 \> 조회 및 보고 \> 보조금 조회 \> 연방지원금 지출계획** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="5a2d4-153">**매개 변수** 에서 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="5a2d4-154">**날짜 간격** 필드에서 날짜 간격에 대한 코드를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="5a2d4-155">또는 **시작 날짜** 및 **종료 날짜** 필드에서 날짜 간격을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="5a2d4-156">선택 사항: 청구된 트랜잭션만 조회에 수익으로 포함하려면 **청구된 수익만 포함** 옵션을 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="5a2d4-157">열</span><span class="sxs-lookup"><span data-stu-id="5a2d4-157">Columns</span></span>

<span data-ttu-id="5a2d4-158">연방지원금 지출계획 조회에는 다음 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a2d4-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="5a2d4-159">연방 정부 지원 목록 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="5a2d4-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="5a2d4-160">교부 기관</span><span class="sxs-lookup"><span data-stu-id="5a2d4-160">Grantor agency</span></span>
- <span data-ttu-id="5a2d4-161">도관 기관</span><span class="sxs-lookup"><span data-stu-id="5a2d4-161">Pass-through agency</span></span>
- <span data-ttu-id="5a2d4-162">보조금 이름</span><span class="sxs-lookup"><span data-stu-id="5a2d4-162">Grant name</span></span>
- <span data-ttu-id="5a2d4-163">보조금 ID</span><span class="sxs-lookup"><span data-stu-id="5a2d4-163">Grant ID</span></span>
- <span data-ttu-id="5a2d4-164">보조금 신청 ID</span><span class="sxs-lookup"><span data-stu-id="5a2d4-164">Grant application ID</span></span>
- <span data-ttu-id="5a2d4-165">연방 정부 지원 목록</span><span class="sxs-lookup"><span data-stu-id="5a2d4-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="5a2d4-166">영수증</span><span class="sxs-lookup"><span data-stu-id="5a2d4-166">Receipts</span></span>
- <span data-ttu-id="5a2d4-167">지출</span><span class="sxs-lookup"><span data-stu-id="5a2d4-167">Expenditures</span></span>
