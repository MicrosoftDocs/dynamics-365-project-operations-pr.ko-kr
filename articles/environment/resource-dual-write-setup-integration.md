---
title: Project Operations 설정 및 구성 데이터 통합
description: 이 항목은 Project Operations 이중 쓰기 맵 설정 및 구성에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939012"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a><span data-ttu-id="6c86d-103">Project Operations 설정 및 구성 데이터 통합</span><span class="sxs-lookup"><span data-stu-id="6c86d-103">Project Operations setup and configuration data integration</span></span>

<span data-ttu-id="6c86d-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6c86d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6c86d-105">이 항목은 설정 및 구성 엔터티를 위한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-105">This topic provides information about Project Operations dual-write integration for setup and configuration entities.</span></span>

## <a name="project-contracts-contract-lines-and-projects"></a><span data-ttu-id="6c86d-106">프로젝트 계약, 계약 내용 및 프로젝트</span><span class="sxs-lookup"><span data-stu-id="6c86d-106">Project contracts, contract lines, and projects</span></span>

<span data-ttu-id="6c86d-107">프로젝트 계약, 계약 내용 및 프로젝트는 Dataverse에서 생성되고 추가 회계를 위해 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-107">Project contracts, contract lines, and projects are created in Dataverse and synchronized to Finance and Operations apps for additional accounting.</span></span> <span data-ttu-id="6c86d-108">이러한 엔터티의 레코드는 Dataverse에서만 만들고 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-108">The records in these entities can be created and deleted only in Dataverse.</span></span> <span data-ttu-id="6c86d-109">그러나 판매세 그룹 기본값 및 재무 차원과 같은 회계 속성은 Finance and Operations 앱에서 이러한 레코드에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-109">However, accounting attributes such as sales tax group defaults and financial dimensions can be added to these records in the Finance and Operations apps.</span></span>

  ![프로젝트 계약 통합 개념](./media/1ProjectContract.jpg)

<span data-ttu-id="6c86d-111">판매 활동 잠재 고객, 영업 기회 및 견적은 Dataverse에서 추적되며 이 활동과 관련된 다운스트림 계정이 없기 때문에 Finance and Operations 앱과 동기화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-111">Sales activity leads, opportunities, and quotes are tracked in Dataverse and don't synchronize to Finance and Operations apps because there is no downstream accounting associated with this activity.</span></span>

<span data-ttu-id="6c86d-112">Dataverse의 프로젝트 계약 기능은 **프로젝트 계약 헤더 (salesorders)** 테이블 맵을 사용하여 Finance and Operations 앱에 프로젝트 계약 레코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-112">The project contract functionality in Dataverse creates a project contract record in Finance and Operations apps using the **Project contract headers (salesorders)** table map.</span></span> <span data-ttu-id="6c86d-113">Dataverse에 프로젝트 계약을 저장하면 프로젝트 계약 고객 엔터티 레코드도 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-113">Saving a project contract in Dataverse also starts the creation of a project contract customer entity record.</span></span> <span data-ttu-id="6c86d-114">이 레코드는 **프로젝트 자금 출처(msdyn\_projectcontractssplitbillingrules)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-114">This record is synchronized to Finance and Operations apps using the **Project funding source (msdyn\_projectcontractssplitbillingrules)** table map.</span></span> <span data-ttu-id="6c86d-115">이 맵은 또한 프로젝트 계약 고객 추가, 업데이트 및 삭제를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-115">This map also synchronizes project contract customer additions, updates, and deletions.</span></span> <span data-ttu-id="6c86d-116">프로젝트 계약 고객 간의 분할 청구 비율은 Dataverse에서만 마스터되며 Finance and Operations 앱과 동기화되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-116">Split billing percentages between project contract customers are mastered only in Dataverse and not synchronized to Finance and Operations apps.</span></span>

<span data-ttu-id="6c86d-117">Dataverse에서 프로젝트 계약이 생성되면 프로젝트 회계사는 **프로젝트 관리 및 회계** > **프로젝트 계약** > **설정** > **기본 계정 표시** 로 이동하여 Finance and Operations 앱에서 이 프로젝트 계약의 회계 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-117">After a project contract is created in Dataverse, the project accountant can update the accounting attributes for this project contract in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**.</span></span> <span data-ttu-id="6c86d-118">회계사는 Dataverse에서 관련 프로젝트 계약 기록을 여는 Finance and Operations 앱에서 프로젝트 계약 ID를 선택하여 요청된 납품 날짜 및 계약 금액과 같은 운영 프로젝트 계약 속성을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-118">The accountant can review operational project contract attributes, such as requested delivery date and contract amount by selecting the project contract ID in Finance and Operations apps which opens the related project contract record in Dataverse.</span></span>

<span data-ttu-id="6c86d-119">프로젝트 엔터티는 **프로젝트 V2(msdyn\_projects)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-119">The project entity is synchronized to Finance and Operations apps using the **Projects V2 (msdyn\_projects)** table map.</span></span> <span data-ttu-id="6c86d-120">프로젝트 회계사는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-120">The project accountant can:</span></span>

  - <span data-ttu-id="6c86d-121">**프로젝트 관리 및 회계** > **모든 프로젝트** 로 이동하여 Finance and Operations앱에서 프로젝트를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-121">Review projects in Finance and Operations apps by going to **Project management and accounting** > **All projects**.</span></span> 
  - <span data-ttu-id="6c86d-122">**프로젝트 관리 및 회계** > **모든 프로젝트** > **설정** > **기본 계정 표시** 로 이동하여 Finance and Operations 앱에서 프로젝트의 회계 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-122">Update accounting attributes for the project in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Set up** > **Show default accounting**.</span></span>  
  - <span data-ttu-id="6c86d-123">Dataverse에서 관련 프로젝트 레코드를 여는 Finance and Operations앱에서 프로젝트 ID를 선택하여 예상 시작 및 종료 날짜와 같은 운영 프로젝트 속성을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-123">Review operational project attributes, such as estimated start and end dates, by selecting the project ID in Finance and Operations apps which opens the related project record in Dataverse.</span></span>

<span data-ttu-id="6c86d-124">프로젝트는 **프로젝트 계약 내용** 엔터티를 통해 프로젝트 계약과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-124">A project is associated with a project contract through the **Project contract line** entity.</span></span>

<span data-ttu-id="6c86d-125">Dataverse의 프로젝트 계약 내용은 **프로젝트 계약 내용(salesorderdetails)** 테이블 맵을 사용하여 Finance and Operations 앱에서 프로젝트 계약 청구 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-125">Project contract lines in Dataverse creates a project contract billing rule in Finance and Operations apps using the **Project contract lines (salesorderdetails)** table map.</span></span> <span data-ttu-id="6c86d-126">청구 방법은 Finance and Operations 앱에서 프로젝트 계약 청구 규칙 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-126">The billing method defines the project contract billing rule type in Finance and Operations apps:</span></span>

  - <span data-ttu-id="6c86d-127">시간 및 재료 청구 방법이 있는 프로젝트 계약 내용은 시간 및 재료 유형의 청구 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-127">Project contract lines with a billing method of time and material create a billing rule of time and material type.</span></span>
  - <span data-ttu-id="6c86d-128">고정 가격 청구 방법 계약 내용은 중요 시점 청구 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-128">Fixed price billing method contract lines create a milestone billing rule.</span></span>

<span data-ttu-id="6c86d-129">프로젝트 계약 내용은 **프로젝트 관리 및 회계** > **프로젝트 계약** > **설정** > **기본 회계 표시** 로 이동하고 **계약 내용** 탭에서 세부 사항을 검토하여 Finance and Operations 앱에서 프로젝트 회계사가 검토할 수 있습니다. 회계사는 이 탭에서 고정 가격 청구 방법 계약 내용에 대한 기본 재무 차원을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-129">Project contract lines can be reviewed by the project accountant in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**, and reviewing the details on the **Contract lines** tab. The accountant can also set default financial dimensions for the fixed price billing method contract lines on this tab.</span></span>

## <a name="billing-milestones"></a><span data-ttu-id="6c86d-130">청구 이정표</span><span class="sxs-lookup"><span data-stu-id="6c86d-130">Billing milestones</span></span>

<span data-ttu-id="6c86d-131">고정 가격 청구 방법을 사용하는 프로젝트 계약 라인은 청구 이정표를 통해 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-131">Project contract lines using the fixed price billing method are invoiced through billing milestones.</span></span> <span data-ttu-id="6c86d-132">청구 이정표는 **Project Operations 통합 계약 내용 이정표(msdyn\_contractlinescheduleofvalues)** 테이블 맵을 사용하여 Finance and Operations 앱의 프로젝트 계정 트랜잭션에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-132">Billing milestones are synchronized to project on-account transactions in Finance and Operations apps by using the **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** table map.</span></span>

  ![청구 이정표 통합](./media/2Milestones.jpg)

<span data-ttu-id="6c86d-134">회계사는 계정 내 거래를 검토하고 **프로젝트 관리 및 회계** > **프로젝트 계약** > **유지** > **계정 트랜잭션** 또는 **프로젝트 관리 및 회계** > **모든 프로젝트** > **유지** > **계정 트랜잭션** 으로 이동하여 해당 트랜잭션에 대한 회계 속성을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-134">The accountant can review on-account transactions and adjust the accounting attributes for those transactions by going to **Project management and accounting** > **Project contracts** > **Maintain** > **On-account transactions** or **Project management and accounting** > **All projects** > **Maintain** > **On-account transactions**.</span></span>

<span data-ttu-id="6c86d-135">주어진 프로젝트 계약 내용에 대한 청구 이정표를 처음 생성하면 시스템은 이 계약 내용과 연관된 프로젝트에 대한 고정 가격 수익 추정 프로젝트를 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-135">When you first create a billing milestone for a given project contract line, the system automatically creates a fixed price revenue estimate project for the project associated with this contract line.</span></span> <span data-ttu-id="6c86d-136">고정 가격 수익 추정 프로젝트는 **프로젝트 관리 및 회계** > **고정 가격 수익 추정 프로젝트** 로 이동하여 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-136">Fixed-price revenue estimate projects can be reviewed by going to **Project management and accounting** > **Fixed-price revenue estimate projects**.</span></span>

### <a name="project-tasks"></a><span data-ttu-id="6c86d-137">프로젝트 작업</span><span class="sxs-lookup"><span data-stu-id="6c86d-137">Project tasks</span></span>

<span data-ttu-id="6c86d-138">프로젝트 작업은 참조 목적으로만 **프로젝트 작업(msdyn\_projecttasks)** 테이블 맵을 통해 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-138">Project tasks are synchronized to Finance and Operations apps through the **Project tasks (msdyn\_projecttasks)** table map for reference purposes only.</span></span> <span data-ttu-id="6c86d-139">Finance and Operations 앱에서는 작업 생성, 업데이트 및 삭제가 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-139">Creating, updating, and deleting operations isn't supported through Finance and Operations apps.</span></span>

  ![프로젝트 작업 통합](./media/3Tasks.jpg)

## <a name="project-resources"></a><span data-ttu-id="6c86d-141">프로젝트 리소스</span><span class="sxs-lookup"><span data-stu-id="6c86d-141">Project resources</span></span>

<span data-ttu-id="6c86d-142">**프로젝트 리소스 역할** 엔터티는 참조 목적으로만 **모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-142">The **Project resource roles** entity is synchronized to Finance and Operations apps using the **Project resource roles for all companies (bookableresourcecategories)** table map for reference purposes only.</span></span> <span data-ttu-id="6c86d-143">Dataverse의 리소스 역할은 회사별로 다르기 때문에 시스템은 이중 쓰기 통합 범위에 포함된 모든 법인에 대해 자동으로 Finance and Operations 앱에 각 회사별 리소스 역할 레코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-143">Because resource roles in Dataverse are not company-specific, the system automatically creates respective company-specific resource roles records in Finance and Operations apps automatically for all legal entities included into dual-write integration scope.</span></span>

![리소스 역할 통합](./media/5Resources.jpg)

<span data-ttu-id="6c86d-145">Project Operations의 프로젝트 리소스는 Dataverse에서 유지되며 Finance and Operations 앱과 동기화되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-145">Project resources in Project Operations are maintained in Dataverse and aren't synchronized to Finance and Operations apps.</span></span>

### <a name="transaction-categories"></a><span data-ttu-id="6c86d-146">트랜잭션 범주</span><span class="sxs-lookup"><span data-stu-id="6c86d-146">Transaction categories</span></span>

<span data-ttu-id="6c86d-147">트랜잭션 범주는 Dataverse에서 유지되며 **프로젝트 트랜잭션 범주(msdyn\_transactioncategories)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-147">Transaction categories are maintained in Dataverse and synchronized to Finance and Operations apps using the **Project transaction categories (msdyn\_transactioncategories)** table map.</span></span> <span data-ttu-id="6c86d-148">트랜잭션 범주 레코드가 동기화된 후 시스템은 4개의 공유 범주 레코드를 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-148">After the transaction category record is synchronized, the system automatically creates four shared category records.</span></span> <span data-ttu-id="6c86d-149">각 레코드는 Finance and Operations 앱의 트랜잭션 유형에 해당하며 이를 트랜잭션 범주 레코드에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-149">Each record corresponds to a transaction type in Finance and Operations apps and links them to the transaction category record.</span></span>

![트랜잭션 범주 통합](./media/4TransactionCategories.jpg)

<span data-ttu-id="6c86d-151">견적 및 실제에 대해 트랜잭션 범주를 사용하려면 프로젝트 회계사 또는 시스템 관리자가 모든 법인에서 해당 프로젝트 범주를 만들어야합니다.</span><span class="sxs-lookup"><span data-stu-id="6c86d-151">Using transaction categories for estimates and actuals requires the project accountant or system administrator to create corresponding project categories in every legal entity.</span></span> <span data-ttu-id="6c86d-152">자세한 내용은 [프로젝트 범주 구성](../project-accounting/configure-project-categories.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6c86d-152">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md).</span></span>
