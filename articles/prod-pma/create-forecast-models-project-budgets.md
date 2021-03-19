---
title: 프로젝트 예산에 대한 예측 모델 만들기
description: 이 항목은 남은 예산에 대한 예측 모델을 만드는 방법을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271046"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="ab78e-103">프로젝트 예산에 대한 예측 모델 만들기</span><span class="sxs-lookup"><span data-stu-id="ab78e-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab78e-104">이 항목은 남은 예산에 대한 예측 모델을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="ab78e-105">예산 통제가 적용되는 프로젝트는 원래 예산과 잔여 예산의 두 가지 유형을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="ab78e-106">프로젝트 예산을 생성할 때 **예측 모델** 페이지에서 생성된 원래 및 잔여 예산 예측 모델을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="ab78e-107">프로젝트 예산을 약정하면 지정된 모델을 기반으로 하는 프로젝트 예산이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="ab78e-108">예산 통제에 사용되는 예측 모델은 하위 모델을 갖거나 하위 모델로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="ab78e-109">**프로젝트 관리 및 회계** > **설정** > **예측**  > **예측 모델** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="ab78e-110">**새로 만들기** 를 선택하여 새 예측 모델을 만든 다음 새 모델의 모델 ID 번호와 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="ab78e-111">**중지됨** 옵션을 **예** 로 설정하여 예측 모델에 대한 예측 라인의 변경을 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="ab78e-112">모델이 연관된 예측 라인이 총계정 원장에서 현금 흐름 예측을 생성해야하는 경우 **현금 흐름 예측에 포함** 을 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="ab78e-113">프로젝트 날짜를 송장 날짜로 사용하려면 **예측 송장 날짜** 를 **예** 로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="ab78e-114">**예산 유형** 필드에서 다음 모델 유형 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="ab78e-115">**원래 예산**: 초기 예산 생성 및 승인시 약정된 최초 예산 금액을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="ab78e-116">**남은 예산**: 프로젝트 기간 동안 남은 예산 금액을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="ab78e-117">이 예측 모델의 잔액은 실제 거래에 의해 감소되고 예산 수정에 의해 증가 또는 감소합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="ab78e-118">**이월**: 프로젝트에 대한 이월 예산 금액을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="ab78e-119">이월은 사용되지 않은 예산 금액을 회계 연도에서 다른 회계 연도로 이전하기 위해 실행할 수 있는 선택적 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="ab78e-120">다음 옵션을 필수로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-120">Set the following options as required:</span></span>

   - <span data-ttu-id="ab78e-121">프로젝트 날짜를 송장 날짜로 사용하려면 **예측 송장 날짜** 를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="ab78e-122">**WIP로 예측** 을 활성화하여 진행 중인 작업(WIP)을 기준으로 예측한 다음 WIP 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="ab78e-123">기본 **예산 유형** 을 **없음** 으로 유지하거나 새 유형을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="ab78e-124">레코드를 변경한 후에는 예산 유형을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="ab78e-125">기본 예산 유형을 변경하면 다른 모든 옵션을 업데이트에 사용할 수 없으며 이 예측 모델을 재사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ab78e-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]