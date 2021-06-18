---
title: 보류 중인 공급업체 송장을 사용하여 비 재고 재료 구매
description: 이 항목에서는 보류 중인 공급업체 송장을 기록하는 방법을 설명합니다.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993809"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="2a643-103">보류 중인 공급업체 송장을 사용하여 비 재고 재료 구매</span><span class="sxs-lookup"><span data-stu-id="2a643-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="2a643-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2a643-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2a643-105">회사가 프로젝트를 위해 비축 재료를 조달하면 프로젝트에 대해 비용을 즉시 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="2a643-106">예를 들면 Contoso Robotics US는 장비 갱신 프로젝트를 수행하고 있으며 소프트웨어 라이선스가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="2a643-107">이러한 라이선스는 타사 공급업체에서 조달합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="2a643-108">Dynamics 365 Finance를 사용하여 지급 계정 사무원은 보류 중인 공급업체 송장 문서를 기록하고 장비 갱신 프로젝트에 직접 라이선스 비용을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2a643-109">이 항목에 설명된 기능을 사용하기 전에 필요한 구성을 검토하고 적용하십시오.</span><span class="sxs-lookup"><span data-stu-id="2a643-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="2a643-110">자세한 내용은 [비 재고 재료 및 보류 중인 공급업체 송장 활성화](configure-materials-nonstocked.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="2a643-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="2a643-111">프로젝트 관련 보류 중인 공급업체 송장 전기</span><span class="sxs-lookup"><span data-stu-id="2a643-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="2a643-112">보류 중인 공급업체 송장은 **보류 중인 공급업체 송장** 페이지 (**지급 계정** > **송장** > **보류 중인 공급업체 송장**)에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="2a643-113">프로젝트 관련 보류 중인 공급업체 송장을 전기하려면 다음 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="2a643-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="2a643-114">**지급 계정** > **송장** 으로 이동하고 **새로 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="2a643-115">**송장 계정** 필드에서 공급업체를 선택하고 **번호** 필드에 공급업체 송장 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="2a643-116">공급업체 송장에 라인을 추가하고 **품목 번호** 필드에서 공급업체로부터 구매한 비 재고 품목을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a643-117">조달 범주를 기반으로 하는 공급업체 송장 라인은 프로젝트에 대해 기록할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="2a643-118">구매한 수량을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-118">Add the quantity purchased.</span></span> <span data-ttu-id="2a643-119">시스템은 비 재고 품목 가격 구성을 기반으로 단가를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="2a643-120">라인에서 총액 및 기타 필수 세부 사항을 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="2a643-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="2a643-121">라인 세부 정보의 **프로젝트** 탭에서 이 항목이 기록될 프로젝트의 ID를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="2a643-122">선택적으로 활동 번호를 선택하고 프로젝트 범주 및 라인 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="2a643-123">보류 중인 공급업체 송장을 전기합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-123">Post pending vendor invoice.</span></span> <span data-ttu-id="2a643-124">송장이 전기되면 시스템은 다음을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="2a643-125">공급업체 잔액.</span><span class="sxs-lookup"><span data-stu-id="2a643-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="2a643-126">판매세 금액.</span><span class="sxs-lookup"><span data-stu-id="2a643-126">The sales tax amount.</span></span>
    - <span data-ttu-id="2a643-127">프로젝트에 대한 비용은 조달 통합 계정에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="2a643-128">Dataverse에서 프로젝트 실제 트랜잭션.</span><span class="sxs-lookup"><span data-stu-id="2a643-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="2a643-129">이 트랜잭션은 [Project Operations 통합 저널](../project-accounting/project-operations-integration-journal.md)을 사용하여 추가 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2a643-130">이 분개장을 전기하면 금액이 조달 통합 계정에서 프로젝트 원가 계정으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="2a643-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
