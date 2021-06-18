---
title: 가격표 비활성화
description: 이 항목은 미사용 또는 이전 가격표를 비활성화하거나 제거하는 방법을 설명합니다.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001344"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="45729-103">가격표 비활성화</span><span class="sxs-lookup"><span data-stu-id="45729-103">Deactivate price lists</span></span> 

<span data-ttu-id="45729-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="45729-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45729-105">Dynamics 365 Project Operations에서 이전 또는 사용되지 않는 가격표를 제거하려면, 완료해야 하는 두 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45729-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="45729-106">특정 페이지에서 가격표를 제거하거나 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="45729-107">**가격표** 페이지의 활성 가격 목록에서 가격표를 비활성화하거나 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="45729-108">가격표를 완전히 제거하려면 두 단계를 모두 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="45729-109">활성 가격표 보기에서 가격표를 직접 삭제하거나 비활성화하는 2단계만 수행하는 것만으로는 충분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45729-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="45729-110">또한 1 단계에서 언급한 모든 위치에서이 가격표의 연결을 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="45729-111">특정 페이지에서 가격표를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="45729-112">Project Operations에서 가격표를 삭제하려면 다음 페이지로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="45729-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="45729-113">**프로젝트 매개 변수** 페이지 > **가격표** 탭</span><span class="sxs-lookup"><span data-stu-id="45729-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="45729-114">**조직 구성 단위** 페이지 >**가격표** 그리드</span><span class="sxs-lookup"><span data-stu-id="45729-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="45729-115">**거래처** 페이지 > **프로젝트 가격표** 그리드</span><span class="sxs-lookup"><span data-stu-id="45729-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="45729-116">**프로젝트 견적** 페이지 >**프로젝트 가격표** 그리드: 모든 활성 프로젝트 견적에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="45729-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="45729-117">**프로젝트 계약** 페이지 >**프로젝트 가격표** 그리드: 모든 활성 프로젝트 계약에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="45729-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="45729-118">각 페이지에 대해 삭제할 가격표를 선택한 다음 **삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="45729-119">가격표 페이지에서 가격표 삭제 또는 비활성화</span><span class="sxs-lookup"><span data-stu-id="45729-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="45729-120">활성 가격표에서 가격표를 삭제하려면 **판매** > **고객** > **가격표** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="45729-121">삭제하려는 가격표룰 선택한 다음 **삭제** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="45729-122">가격표가 기존 트랜잭션에서 참조되는 경우 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="45729-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="45729-123">이 경우 가격표를 비활성화하여 보기에 표시되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45729-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="45729-124">가격표를 비활성화하려면 가격표를 다시 선택한 다음 **비활성화** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="45729-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
