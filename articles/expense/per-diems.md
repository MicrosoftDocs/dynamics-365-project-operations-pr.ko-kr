---
title: 일비
description: 이 항목은 경비 관리에 사용되는 일비 규칙에 대한 정보를 제공합니다.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995269"
---
# <a name="per-diems"></a><span data-ttu-id="eac9e-103">일비</span><span class="sxs-lookup"><span data-stu-id="eac9e-103">Per diems</span></span>

<span data-ttu-id="eac9e-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="eac9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="eac9e-105">일비는 업무를 위해 여행하는 근로자에게 지급되는 수당입니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="eac9e-106">경비 관리에서는 다양한 여행 상황에 대한 일당 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="eac9e-107">일비 요율은 연중 시간, 여행 위치 또는 둘 다를 기반으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="eac9e-108">일비 규칙을 만들 때 근로자가 무료 급식 또는 서비스를 받는 경우 일비 비율의 일정 비율이 보류되도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="eac9e-109">일비 요율이 근로자의 출장에 적용될 수 있는 최소 및 최대 시간을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="eac9e-110">구성</span><span class="sxs-lookup"><span data-stu-id="eac9e-110">Configuration</span></span> 

1. <span data-ttu-id="eac9e-111">일비 위치를 추가하려면 **설정** > **계산 및 코드** > **일비 위치** 으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="eac9e-112">위에 추가된 각 위치에 대해 호텔, 식사 및 기타 비용에 대해 특정 시작 날짜와 종료 날짜 사이에 유효한 일비 요율 및 통화를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="eac9e-113">일비 요율 및 통화는 **설정** > **계산 및 코드** > **일비** 아래 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="eac9e-114">**일비 위치** 페이지에서 일비 요율 계층을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="eac9e-115">일비 요율 계층을 사용하면 호텔, 식사 및 기타 비용에 대한 일비 수당의 비율 분할을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="eac9e-116">아침, 점심 또는 저녁 식사에 대한 식사 비율 감소를 지정하려면 **일비** 탭의 **경비 관리 매개 변수** 페이지에서 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="eac9e-117">일비를 사용하여 경비 제출</span><span class="sxs-lookup"><span data-stu-id="eac9e-117">Submit expenses using per diem</span></span>
<span data-ttu-id="eac9e-118">일비를 활용한 경비를 제출하려면 **일비** 경비 보고서를 생성할 때 경비 범주를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="eac9e-119">**일비 시작 날짜**,**일비 종료 날짜** 및 **일비 위치** 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="eac9e-120">금액은 선택한 위치의 일비 요율을 기준으로 계산되며, 식비 감소는 일비 요율 등급에 따라 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="eac9e-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]