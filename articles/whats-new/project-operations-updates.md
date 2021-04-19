---
title: Project Operations 업데이트
description: 이 토픽은 Dynamics 365 Project Operations의 출시된 버전에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5a1ab3b506ae94bba3a6ca96b164437d3fd3a035
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877543"
---
# <a name="project-operations-updates"></a><span data-ttu-id="87f79-103">Project Operations 업데이트</span><span class="sxs-lookup"><span data-stu-id="87f79-103">Project Operations updates</span></span>

<span data-ttu-id="87f79-104">_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 처리 및 재고/생산 기반 시나리오를 위한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="87f79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, and Project Operations for stocked/production-based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a><span data-ttu-id="87f79-105">Project Operations 구성 요소</span><span class="sxs-lookup"><span data-stu-id="87f79-105">Project Operations components</span></span>

<span data-ttu-id="87f79-106">Dynamics 365 Project Operations는 두 가지 구성 요소로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-106">Dynamics 365 Project Operations consists of two components:</span></span>

- <span data-ttu-id="87f79-107">Dataverse 환경의 Project Operations는 영업 기회에서 견적 송장까지 다양한 기능을 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-107">Project Operations on Dataverse environment covers capabilities from opportunity to proforma invoicing.</span></span> <span data-ttu-id="87f79-108">Dataverse는 Project Operations의 라이트 배포 및 리소스/비 재고 시나리오 배포에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-108">Dataverse is used in the lite deployment and resource/non-stocked scenarios deployment of Project Operations.</span></span>
- <span data-ttu-id="87f79-109">Dynamics 365 Finance 환경의 프로젝트 관리 및 회계에는 경비 관리 기능, 프로젝트 회계 및 수익 인식이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-109">Project management and accounting in the Dynamics 365 Finance environment covers expense management capabilities, project accounting, and revenue recognition.</span></span> <span data-ttu-id="87f79-110">Finance and Operations 앱 환경은 리소스/비 재고 기반 시나리오를 위한 Project Operations 및 재고/생산 기반 시나리오를 위한 Project Operations에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-110">The Finance and Operations app environment is used in Project Operations for resource/non-stocked based scenarios and Project Operations for stocked/production-based scenarios.</span></span>

## <a name="project-operations-release-notes"></a><span data-ttu-id="87f79-111">Project Operations 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="87f79-111">Project Operations release notes</span></span>
- <span data-ttu-id="87f79-112">[리소스/비 재고](whats-new-apr-2021-resource-based.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.</span><span class="sxs-lookup"><span data-stu-id="87f79-112">Project Operations latest release notes for [Resource/non-stocked](whats-new-apr-2021-resource-based.md) scenario.</span></span>
- <span data-ttu-id="87f79-113">[라이트 배포](../pro/whats-new/whats-new-apr-2021-lite.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.</span><span class="sxs-lookup"><span data-stu-id="87f79-113">Project Operations latest release notes for [Lite deployment](../pro/whats-new/whats-new-apr-2021-lite.md) scenario.</span></span>
- <span data-ttu-id="87f79-114">[리소스/생산](../prod-pma/whats-new/whats-new-mar-2021-stocked.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.</span><span class="sxs-lookup"><span data-stu-id="87f79-114">Project Operations latest release notes for [stocked/production](../prod-pma/whats-new/whats-new-mar-2021-stocked.md) scenario.</span></span>

## <a name="project-operations-latest-version"></a><span data-ttu-id="87f79-115">Project Operations 최신 버전</span><span class="sxs-lookup"><span data-stu-id="87f79-115">Project Operations latest version</span></span>

| <span data-ttu-id="87f79-116">Dataverse 환경의 Project Operations</span><span class="sxs-lookup"><span data-stu-id="87f79-116">Project Operations on Dataverse environment</span></span> | <span data-ttu-id="87f79-117">Finance and Operations 앱 환경의 프로젝트 관리 및 회계</span><span class="sxs-lookup"><span data-stu-id="87f79-117">Project management and accounting in Finance and Operations apps environments</span></span> | 
| --- | --- |
| <span data-ttu-id="87f79-118">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-118">4.9.0.221</span></span> | <span data-ttu-id="87f79-119">10.0.17</span><span class="sxs-lookup"><span data-stu-id="87f79-119">10.0.17</span></span> |

<span data-ttu-id="87f79-120">Project Operations 리소스/재고가 없는 시나리오의 경우 Dual Write Orchestration 버전 2.2.2.50 이상을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-120">For Project Operations Resource/non-stocked scenario, we recommend to use Dual Write Orchestration version 2.2.2.50 or higher.</span></span>

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a><span data-ttu-id="87f79-121">Dataverse 환경에서 Project Operations를 위한 릴리스 일정</span><span class="sxs-lookup"><span data-stu-id="87f79-121">Release schedule for Project Operations on Dataverse environment</span></span>

<span data-ttu-id="87f79-122">Dataverse 환경의 Project Operations에 대한 업데이트는 매월 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-122">Updates for Project Operations on Dataverse environment are available monthly.</span></span> 

| <span data-ttu-id="87f79-123">스테이션</span><span class="sxs-lookup"><span data-stu-id="87f79-123">Station</span></span>   | <span data-ttu-id="87f79-124">지역</span><span class="sxs-lookup"><span data-stu-id="87f79-124">Region</span></span>        | <span data-ttu-id="87f79-125">현재 버전</span><span class="sxs-lookup"><span data-stu-id="87f79-125">Current version</span></span> | <span data-ttu-id="87f79-126">다음 버전</span><span class="sxs-lookup"><span data-stu-id="87f79-126">Next version</span></span> | <span data-ttu-id="87f79-127">일반적으로 사용 가능</span><span class="sxs-lookup"><span data-stu-id="87f79-127">Generally available</span></span> |
|-----------|---------------|-----------------|--------------|---------------------|
| <span data-ttu-id="87f79-128">스테이션 1</span><span class="sxs-lookup"><span data-stu-id="87f79-128">Station 1</span></span> |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="87f79-129">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="87f79-129">First Release</span></span> |  <span data-ttu-id="87f79-130">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-130">4.9.0.221</span></span>       | <span data-ttu-id="87f79-131">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-131">TBD</span></span>     | <span data-ttu-id="87f79-132">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-132">23-Apr-21</span></span>           |
| <span data-ttu-id="87f79-133">스테이션 2</span><span class="sxs-lookup"><span data-stu-id="87f79-133">Station 2</span></span> |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="87f79-134">남아메리카</span><span class="sxs-lookup"><span data-stu-id="87f79-134">South America</span></span> |  <span data-ttu-id="87f79-135">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-135">4.9.0.221</span></span>       | <span data-ttu-id="87f79-136">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-136">TBD</span></span>     | <span data-ttu-id="87f79-137">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-137">23-Apr-21</span></span>           |
|    &nbsp; | <span data-ttu-id="87f79-138">캐나다</span><span class="sxs-lookup"><span data-stu-id="87f79-138">Canada</span></span>        |  <span data-ttu-id="87f79-139">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-139">4.9.0.221</span></span>       | <span data-ttu-id="87f79-140">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-140">TBD</span></span>     | <span data-ttu-id="87f79-141">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-141">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-142">인도</span><span class="sxs-lookup"><span data-stu-id="87f79-142">India</span></span>         |  <span data-ttu-id="87f79-143">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-143">4.9.0.221</span></span>       | <span data-ttu-id="87f79-144">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-144">TBD</span></span>     | <span data-ttu-id="87f79-145">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-145">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-146">프랑스</span><span class="sxs-lookup"><span data-stu-id="87f79-146">France</span></span>         |  <span data-ttu-id="87f79-147">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-147">4.9.0.221</span></span>       | <span data-ttu-id="87f79-148">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-148">TBD</span></span>     | <span data-ttu-id="87f79-149">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-149">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-150">아랍에미리트연합국</span><span class="sxs-lookup"><span data-stu-id="87f79-150">United Arab Emirates</span></span>         |  <span data-ttu-id="87f79-151">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-151">4.9.0.221</span></span>       | <span data-ttu-id="87f79-152">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-152">TBD</span></span>     | <span data-ttu-id="87f79-153">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-153">23-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-154">남아프리카 공화국</span><span class="sxs-lookup"><span data-stu-id="87f79-154">South Africa</span></span>         |  <span data-ttu-id="87f79-155">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-155">4.9.0.221</span></span>       | <span data-ttu-id="87f79-156">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-156">TBD</span></span>     | <span data-ttu-id="87f79-157">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-157">23-Apr-21</span></span>           |
| <span data-ttu-id="87f79-158">스테이션 3</span><span class="sxs-lookup"><span data-stu-id="87f79-158">Station 3</span></span>  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="87f79-159">일본</span><span class="sxs-lookup"><span data-stu-id="87f79-159">Japan</span></span>         |  <span data-ttu-id="87f79-160">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-160">4.9.0.221</span></span>       | <span data-ttu-id="87f79-161">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-161">TBD</span></span>     | <span data-ttu-id="87f79-162">2021년 4월 30일</span><span class="sxs-lookup"><span data-stu-id="87f79-162">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-163">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="87f79-163">Asia Pacific</span></span>  |  <span data-ttu-id="87f79-164">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-164">4.9.0.221</span></span>       | <span data-ttu-id="87f79-165">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-165">TBD</span></span>     | <span data-ttu-id="87f79-166">2021년 4월 30일</span><span class="sxs-lookup"><span data-stu-id="87f79-166">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-167">영국</span><span class="sxs-lookup"><span data-stu-id="87f79-167">Great Britain</span></span> |  <span data-ttu-id="87f79-168">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-168">4.9.0.221</span></span>       | <span data-ttu-id="87f79-169">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-169">TBD</span></span>     | <span data-ttu-id="87f79-170">2021년 4월 30일</span><span class="sxs-lookup"><span data-stu-id="87f79-170">30-Apr-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="87f79-171">오세아니아</span><span class="sxs-lookup"><span data-stu-id="87f79-171">Oceania</span></span>       |  <span data-ttu-id="87f79-172">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-172">4.9.0.221</span></span>       | <span data-ttu-id="87f79-173">TBD</span><span class="sxs-lookup"><span data-stu-id="87f79-173">TBD</span></span>     | <span data-ttu-id="87f79-174">2021년 4월 30일</span><span class="sxs-lookup"><span data-stu-id="87f79-174">30-Apr-21</span></span>           |
| <span data-ttu-id="87f79-175">스테이션 4</span><span class="sxs-lookup"><span data-stu-id="87f79-175">Station 4</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="87f79-176">유럽</span><span class="sxs-lookup"><span data-stu-id="87f79-176">Europe</span></span>        |  <span data-ttu-id="87f79-177">4.8.0.92</span><span class="sxs-lookup"><span data-stu-id="87f79-177">4.8.0.92</span></span>       | <span data-ttu-id="87f79-178">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-178">4.9.0.221</span></span>     | <span data-ttu-id="87f79-179">2021년 4월 16일</span><span class="sxs-lookup"><span data-stu-id="87f79-179">16-Apr-21</span></span>           |
| <span data-ttu-id="87f79-180">스테이션 5</span><span class="sxs-lookup"><span data-stu-id="87f79-180">Station 5</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="87f79-181">북아메리카</span><span class="sxs-lookup"><span data-stu-id="87f79-181">North America</span></span> |  <span data-ttu-id="87f79-182">4.8.0.92</span><span class="sxs-lookup"><span data-stu-id="87f79-182">4.8.0.92</span></span>       | <span data-ttu-id="87f79-183">4.9.0.221</span><span class="sxs-lookup"><span data-stu-id="87f79-183">4.9.0.221</span></span>     | <span data-ttu-id="87f79-184">2021년 4월 23일</span><span class="sxs-lookup"><span data-stu-id="87f79-184">23-Apr-21</span></span>           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a><span data-ttu-id="87f79-185">Finance and Operations 앱 환경의 프로젝트 관리 및 회계에 대한 릴리스 일정</span><span class="sxs-lookup"><span data-stu-id="87f79-185">Release schedule for Project management and accounting in the Finance and Operations apps environment</span></span>

<span data-ttu-id="87f79-186">프로젝트 관리 및 회계에 대한 업데이트는 1년에 8번 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-186">Updates for Project management and accounting are released eight times a year.</span></span>

| <span data-ttu-id="87f79-187">지원되는 릴리스</span><span class="sxs-lookup"><span data-stu-id="87f79-187">Supported release</span></span> | <span data-ttu-id="87f79-188">일반적으로 사용 가능(자체 업데이트)</span><span class="sxs-lookup"><span data-stu-id="87f79-188">Generally available (self-update)</span></span> |
| --- | --- |
| <span data-ttu-id="87f79-189">10.0.17</span><span class="sxs-lookup"><span data-stu-id="87f79-189">10.0.17</span></span> | <span data-ttu-id="87f79-190">2021년 3월 19일</span><span class="sxs-lookup"><span data-stu-id="87f79-190">March 19, 2021</span></span> |
| <span data-ttu-id="87f79-191">10.0.16</span><span class="sxs-lookup"><span data-stu-id="87f79-191">10.0.16</span></span> | <span data-ttu-id="87f79-192">2021년 1월 22일</span><span class="sxs-lookup"><span data-stu-id="87f79-192">January 22, 2021</span></span> |


<span data-ttu-id="87f79-193">릴리스 예정일은 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87f79-193">Targeted release dates are subject to change.</span></span> <span data-ttu-id="87f79-194">자세한 내용은 [서비스 업데이트 가용성](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="87f79-194">For more information, see [Service update availability](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json).</span></span>

| <span data-ttu-id="87f79-195">릴리스 예정일</span><span class="sxs-lookup"><span data-stu-id="87f79-195">Targeted release date</span></span> | <span data-ttu-id="87f79-196">일반적으로 사용 가능(자체 업데이트됨)</span><span class="sxs-lookup"><span data-stu-id="87f79-196">Generally available (self- updated)</span></span> |
| --- | --- |
| <span data-ttu-id="87f79-197">10.0.18</span><span class="sxs-lookup"><span data-stu-id="87f79-197">10.0.18</span></span> | <span data-ttu-id="87f79-198">2021년 4월 16일</span><span class="sxs-lookup"><span data-stu-id="87f79-198">April 16, 2021</span></span> |
| <span data-ttu-id="87f79-199">10.0.19</span><span class="sxs-lookup"><span data-stu-id="87f79-199">10.0.19</span></span> | <span data-ttu-id="87f79-200">2021년 6월 18일</span><span class="sxs-lookup"><span data-stu-id="87f79-200">June 18, 2021</span></span> |
| <span data-ttu-id="87f79-201">10.0.20</span><span class="sxs-lookup"><span data-stu-id="87f79-201">10.0.20</span></span> | <span data-ttu-id="87f79-202">2021년 7월 16일</span><span class="sxs-lookup"><span data-stu-id="87f79-202">July 16, 2021</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
