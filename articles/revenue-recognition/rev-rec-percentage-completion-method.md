---
title: 고정 가격 수익 프로젝트 추정
description: 이 토픽은 프로젝트에서 고정 가격 수익에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278921"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="4e312-103">고정 가격 수익 프로젝트 추정</span><span class="sxs-lookup"><span data-stu-id="4e312-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="4e312-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="4e312-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4e312-105">Microsoft Dataverse의 Dynamics 365 Project Operations에서 다음 특성을 사용하여 프로젝트 계약 내용을 생성할 때 시스템은 고정 가격 수익 추정 프로젝트를 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="4e312-106">이 프로젝트의 정보는 다음을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="4e312-107">고정 가격 청구 방법.</span><span class="sxs-lookup"><span data-stu-id="4e312-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="4e312-108">관련 프로젝트.</span><span class="sxs-lookup"><span data-stu-id="4e312-108">An associated project.</span></span>
  - <span data-ttu-id="4e312-109">**프로젝트 계약 내용** 페이지의 **송장 일정** 탭에 정의된 하나 이상의 중요 시점.</span><span class="sxs-lookup"><span data-stu-id="4e312-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="4e312-110">고정 가격 수익 추정 프로젝트 검토</span><span class="sxs-lookup"><span data-stu-id="4e312-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="4e312-111">고정 가격 수익 추정 프로젝트를 검토하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="4e312-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="4e312-112">Dynamics 365 Finance 환경에서 **프로젝트 관리 및 회계** > **프로젝트** > **고정 가격 수익 추정 프로젝트** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="4e312-113">보려는 프로젝트를 선택하고 **추정 프로젝트 ID** 를 두 번 클릭하여 레코드를 열고 프로젝트의 세부 사항을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="4e312-114">**프로젝트** 탭을 확장합니다. **선택한 프로젝트** 그리드에 하나의 프로젝트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="4e312-115">시스템은 프로젝트 계약 내용과 연관된 프로젝트이므로 이를 기본 프로젝트로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="4e312-116">연결을 변경하려면 추가 프로젝트를 선택하고 **선택한 프로젝트** 그리드에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="4e312-117">이 그리드에서 여러 프로젝트를 선택한 경우 선택한 모든 프로젝트에 대해 프로젝트 완료율 및 예상 수익이 함께 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="4e312-118">프로젝트 비용, 수익 프로필, 비용 템플릿 및 기간 코드는 수동으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="4e312-119">수동으로 설정하지 않은 경우 프로젝트 비용 및 수익 프로필에 대해 구성된 규칙을 사용하여 프로젝트에 대한 첫 번째 추정 계산 중에 값이 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e312-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]