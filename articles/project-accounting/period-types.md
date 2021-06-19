---
title: 기간 유형
description: 이 토픽은 수익 추정을 위해 기간 유형을 설정하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013494"
---
# <a name="period-types"></a><span data-ttu-id="ebd20-103">기간 유형</span><span class="sxs-lookup"><span data-stu-id="ebd20-103">Period types</span></span>

<span data-ttu-id="ebd20-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ebd20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ebd20-105">기간 유형은 프로젝트 수익이 추정되는 빈도를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="ebd20-106">이 토픽은 수익 추정을 위해 기간 유형을 설정하는 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="ebd20-107">기간 유형 만들기 및 작업</span><span class="sxs-lookup"><span data-stu-id="ebd20-107">Create and work with period types</span></span>
<span data-ttu-id="ebd20-108">기간 유형을 작성하고 작업하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebd20-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="ebd20-109">Dynamics 365 Finance 환경에서 **프로젝트 관리 및 회계** > **설정** > **추정** > **기간 유형** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="ebd20-110">**새로 만들기** 를 선택하여 새 기간 유형을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-110">Select **New** to create new period type.</span></span> <span data-ttu-id="ebd20-111">이름과 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-111">Enter a name and description.</span></span>
3. <span data-ttu-id="ebd20-112">**빈도** 필드에서 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="ebd20-113">**주**, **격주**, **월 2회**, **월**, **일**, **분기** 또는 **년** 을 선택하면 달력은 기간을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="ebd20-114">**원장 기간** 을 선택하면 총계정 원장 구성의 원장 기간이 기간을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="ebd20-115">**제한 없음** 을 선택하면 사용자 정의 기간을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="ebd20-116">기간 유형 레코드를 선택한 다음 **기간 생성** 을 선택하여 기간 유형에 대한 기간을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="ebd20-117">선택한 기간 빈도에 따라 생성할 시작 날짜 또는 기간 수를 지정하는 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="ebd20-118">**기간** 을 선택하여 생성된 기간을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd20-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]