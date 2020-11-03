---
title: Finance and Operations에 전기를 위해 Project Service Automation에서 프로젝트 통합 저널로 프로젝트 실제 데이터를 직접 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Finance and Operations로 직접 프로젝트 실제를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080184"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="50e8d-103">Finance and Operations에 전기를 위해 Project Service Automation에서 프로젝트 통합 저널로 프로젝트 실제 데이터를 직접 동기화</span><span class="sxs-lookup"><span data-stu-id="50e8d-103">Synchronize project actuals directly from Project Service Automation to the project integration journal for posting in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="50e8d-104">이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 실제를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

<span data-ttu-id="50e8d-105">템플릿은 Project Service Automation의 트랜잭션을 Finance의 준비 테이블로 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-105">The template synchronizes transactions from Project Service Automation into a staging table in Finance.</span></span> <span data-ttu-id="50e8d-106">동기화가 완료되면 준비 테이블의 데이터를 통합 저널로 **반드시** 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-106">After synchronization is completed, you **must** import the data from the staging table into the integration journal.</span></span>

> [!NOTE]
> - <span data-ttu-id="50e8d-107">프로젝트 실제 통합은 버전 8.0.1부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-107">Project actuals integration is available starting in version 8.0.1.</span></span>
> - <span data-ttu-id="50e8d-108">KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-108">If you're using Enterprise edition 7.3.0 after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="50e8d-109">회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-109">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="50e8d-110">버전 7.3.0을 사용 중이고 Project Service Automation에서 수수료 거래를 가져오는 경우 프로젝트 송장에 해당 수수료를 포함하려면 KB 4345320를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-110">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="50e8d-111">Project Service Automation에서 시간 또는 경비 트랜잭션에 대한 판매세 금액을 입력하는 경우 Project Service Automation 업데이트 7을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-111">If you're entering sales tax amounts on time or expense transactions in Project Service Automation, you must install Project Service Automation Update 7.</span></span> <span data-ttu-id="50e8d-112">그렇지 않으면 실제 세금이 관련 시간 또는 실제 경비에 연결되지 않고 Finance에 동기화되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-112">Otherwise, the tax actuals won't be linked to the associated time or expense actuals, and they won't be synchronized to Finance.</span></span> <span data-ttu-id="50e8d-113">자세한 내용은 지원 부서에 문의하십시오.</span><span class="sxs-lookup"><span data-stu-id="50e8d-113">For more information, contact Support.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="50e8d-114">Project Service Automation에서 Finance까지의 데이터 흐름</span><span class="sxs-lookup"><span data-stu-id="50e8d-114">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="50e8d-115">Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-115">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="50e8d-116">데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 실제에 대한 데이터 흐름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-116">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance.</span></span>

<span data-ttu-id="50e8d-117">다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-117">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="50e8d-118">[![Project Service Automation과 Finance and Operations 통합을 위한 데이터 흐름](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="50e8d-118">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>

## <a name="project-actuals-from-project-service-automation"></a><span data-ttu-id="50e8d-119">Project Service Automation의 프로젝트 실제</span><span class="sxs-lookup"><span data-stu-id="50e8d-119">Project actuals from Project Service Automation</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="50e8d-120">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="50e8d-120">Template and tasks</span></span>

<span data-ttu-id="50e8d-121">사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-121">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="50e8d-122">다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 실제를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-122">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="50e8d-123">**데이터 통합의 템플릿 이름:** 프로젝트 실제(PSA에서 Fin 및 Ops까지)</span><span class="sxs-lookup"><span data-stu-id="50e8d-123">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="50e8d-124">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="50e8d-124">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="50e8d-125">실제</span><span class="sxs-lookup"><span data-stu-id="50e8d-125">Actuals</span></span>
    - <span data-ttu-id="50e8d-126">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="50e8d-126">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="50e8d-127">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="50e8d-127">Entity set</span></span>

| <span data-ttu-id="50e8d-128">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="50e8d-128">Project Service Automation</span></span> | <span data-ttu-id="50e8d-129">재무</span><span class="sxs-lookup"><span data-stu-id="50e8d-129">Finance</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="50e8d-130">실제</span><span class="sxs-lookup"><span data-stu-id="50e8d-130">Actuals</span></span>                    | <span data-ttu-id="50e8d-131">프로젝트 실제를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="50e8d-131">Integration entity for project actuals</span></span>                   |
| <span data-ttu-id="50e8d-132">거래 연결</span><span class="sxs-lookup"><span data-stu-id="50e8d-132">Transaction Connections</span></span>    | <span data-ttu-id="50e8d-133">프로젝트 트랜잭션 관계를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="50e8d-133">Integration entity for project transaction relationships</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="50e8d-134">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="50e8d-134">Entity flow</span></span>

<span data-ttu-id="50e8d-135">프로젝트 실제는 Project Service Automation에서 관리되며 Finance에서 프로젝트 통합 저널과 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-135">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="50e8d-136">회계는 기본 재무 차원 및 전기 설정을 기반으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-136">The accounting will be applied based on default financial dimensions and the posting setup.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="50e8d-137">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="50e8d-137">Prerequisites</span></span>

<span data-ttu-id="50e8d-138">실제 동기화가 발생하기 전에 Project Service Automation 통합 매개 변수를 구성하고 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-138">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="50e8d-139">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="50e8d-139">Power Query</span></span>

<span data-ttu-id="50e8d-140">프로젝트 실제 템플릿에서 Microsoft Excel용 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-140">In the project actuals template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="50e8d-141">Project Service Automation의 트랜잭션 유형을 Finance의 올바른 트랜잭션 유형으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-141">Transform the transaction type in Project Service Automation to the correct transaction type in Finance.</span></span> <span data-ttu-id="50e8d-142">이 변환은 프로젝트 실제(PSA에서 Fin 및 Ops로) 템플릿에 이미 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-142">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span>
- <span data-ttu-id="50e8d-143">Project Service Automation의 청구 유형을 Finance의 올바른 청구 유형으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-143">Transform the billing type in Project Service Automation to the correct billing type in Finance.</span></span> <span data-ttu-id="50e8d-144">이 변환은 프로젝트 실제(PSA에서 Fin 및 Ops로) 템플릿에 이미 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-144">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="50e8d-145">그런 다음 청구 유형은 **Project Service Automation 통합 매개 변수** 페이지의 구성에 따라 라인 속성에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-145">The billing type is then mapped to the line property, based on the configuration on the **Project Service Automation integration parameters** page.</span></span>
- <span data-ttu-id="50e8d-146">이 템플릿과 동기화해야 하는 특정 리소스 조직 단위로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-146">Filter to specific resource organizational units that must be synchronized with this template.</span></span>
- <span data-ttu-id="50e8d-147">회사 간 시간 또는 회사 간 비용 실제가 Finance에 동기화되는 경우 계약 조직 단위를 Finance의 올바른 법인으로 변환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-147">If intercompany time or intercompany expense actuals will be synchronized to Finance, you must transform the contract organizational unit to the correct legal entity in Finance.</span></span> <span data-ttu-id="50e8d-148">프로젝트 실제(PSA에서 Fin 및 Ops으로) 템플릿에서 조건부 열은 데모 데이터를 기반으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-148">In the Project actuals (PSA to Fin and Ops) template, a conditional column is defined based on demo data.</span></span> <span data-ttu-id="50e8d-149">마지막으로 삽입된 조건부 열을 올바른 법인으로 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-149">You must update the last inserted conditional column to the correct legal entities.</span></span> <span data-ttu-id="50e8d-150">그렇지 않으면 통합 오류가 발생하거나 잘못된 실제 트랜잭션을 Finance로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-150">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>
- <span data-ttu-id="50e8d-151">회사 간 시간 또는 회사 간 경비 실제가 Finance에 동기화되지 않는 경우 템플릿에서 마지막으로 삽입된 조건부 열을 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-151">If intercompany time or intercompany expense actuals won't be synchronized to Finance, you must delete the last inserted conditional column from your template.</span></span> <span data-ttu-id="50e8d-152">그렇지 않으면 통합 오류가 발생하거나 잘못된 실제 트랜잭션을 Finance로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-152">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>

#### <a name="contract-organizational-unit"></a><span data-ttu-id="50e8d-153">연락처 조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="50e8d-153">Contract organizational unit</span></span>
<span data-ttu-id="50e8d-154">템플릿에서 삽입된 조건부 열을 업데이트하려면 **매핑** 화살표를 클릭하여 매핑을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-154">To update the inserted conditional column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="50e8d-155">**고급 쿼리 및 필터링** 링크를 선택하여 파워 쿼리를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-155">Select the **Advanced Query and Filtering** link to open Power Query.</span></span>

- <span data-ttu-id="50e8d-156">기본 프로젝트 실제(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 파워 쿼리의 **적용 단계** 섹션에서 마지막 **삽입된 조건** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-156">If you're using the default Project actuals (PSA to Fin and Ops) template, in Power Query, select the last **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="50e8d-157">**함수** 항목에서 **USSI** 를 통합과 함께 사용해야 하는 법인의 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-157">In the **Function** entry, replace **USSI** with the name of the legal entity that should be used with the integration.</span></span> <span data-ttu-id="50e8d-158">필요에 따라 추가 조건을 **함수** 항목에 추가하고 **USMF** 의 **else** 조건을 올바른 법인으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-158">Add additional conditions to the **Function** entry as you require, and update the **else** condition from **USMF** to the correct legal entity.</span></span>
- <span data-ttu-id="50e8d-159">새 템플릿을 만드는 경우 회사 간 시간 및 경비를 지원하기 위해 열을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-159">If you're creating a new template, you must add the column to support intercompany time and expenses.</span></span> <span data-ttu-id="50e8d-160">**조건 열 추가** 를 선택하고 열의 이름(예: **LegalEntity** )을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-160">Select **Add Conditional Column** , and enter a name for the column, such as **LegalEntity**.</span></span> <span data-ttu-id="50e8d-161">열에 대한 조건을 입력합니다. 여기서 **msdyn\_contractorganizationalunitid.msdyn\_name** 이 \<organizational unit\>인 경우 \<enter the legal entity\>, 그렇지 않으면 null입니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-161">Enter a condition for the column, where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="50e8d-162">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="50e8d-162">Template mapping in Data integration</span></span>

<span data-ttu-id="50e8d-163">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-163">The following illustrations show an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="50e8d-164">매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-164">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="50e8d-165">[![템플릿 매핑 - 실제](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="50e8d-165">[![Template mapping - Actuals](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="50e8d-166">[![템플릿 매핑 - 트랜잭션 연결](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="50e8d-166">[![Template mapping - Transaction connections](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a><span data-ttu-id="50e8d-167">Project Service Automation에서 통합한 후 준비 테이블에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="50e8d-167">Import from staging table after integration from Project Service Automation</span></span>

<span data-ttu-id="50e8d-168">Project Service Automation에서 Finance로 실제 데이터를 동기화한 후 준비 테이블에서 가져오기 주기적 프로세스를 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-168">The Import from staging table periodic process must be run after the synchronization of actuals from Project Service Automation to Finance.</span></span> <span data-ttu-id="50e8d-169">이 프로세스는 준비 테이블에서 Project Service Automation 통합 저널로 프로젝트 트랜잭션을 가져오며 여기에서 회계가 적용되고 가져온 트랜잭션을 전기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-169">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="50e8d-170">이 프로세스를 배치 모드로 실행하는 것이 좋습니다. 반복 배치로 실행되도록 선택적으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-170">We recommend that you run this process in batch mode; it can optionally be set up to run as a recurring batch.</span></span>

## <a name="update-actuals-from-finance"></a><span data-ttu-id="50e8d-171">Finance에서 실제 업데이트</span><span class="sxs-lookup"><span data-stu-id="50e8d-171">Update actuals from Finance</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="50e8d-172">템플릿 및 작업</span><span class="sxs-lookup"><span data-stu-id="50e8d-172">Template and tasks</span></span>

<span data-ttu-id="50e8d-173">다음 템플릿 및 기본 작업은 Finance에서 Project Service Automation으로 전기된 프로젝트 트랜잭션에 대한 바우처 번호 및 판매세를 동기화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-173">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="50e8d-174">**데이터 통합의 템플릿 이름:** 프로젝트 실제 업데이트(Fin Ops에서 PSA로)</span><span class="sxs-lookup"><span data-stu-id="50e8d-174">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
- <span data-ttu-id="50e8d-175">**프로젝트에서 작업의 이름:**</span><span class="sxs-lookup"><span data-stu-id="50e8d-175">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="50e8d-176">실제</span><span class="sxs-lookup"><span data-stu-id="50e8d-176">Actuals</span></span> 
    - <span data-ttu-id="50e8d-177">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="50e8d-177">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="50e8d-178">엔터티 집합</span><span class="sxs-lookup"><span data-stu-id="50e8d-178">Entity set</span></span>

| <span data-ttu-id="50e8d-179">재무</span><span class="sxs-lookup"><span data-stu-id="50e8d-179">Finance</span></span>                                                  | <span data-ttu-id="50e8d-180">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="50e8d-180">Project Service Automation</span></span> |
|----------------------------------------------------------|----------------------------|
| <span data-ttu-id="50e8d-181">프로젝트 실제를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="50e8d-181">Integration entity for project actuals</span></span>                   | <span data-ttu-id="50e8d-182">실제</span><span class="sxs-lookup"><span data-stu-id="50e8d-182">Actuals</span></span>                    |
| <span data-ttu-id="50e8d-183">프로젝트 트랜잭션 관계를 위한 통합 엔터티</span><span class="sxs-lookup"><span data-stu-id="50e8d-183">Integration entity for project transaction relationships</span></span> | <span data-ttu-id="50e8d-184">거래 연결</span><span class="sxs-lookup"><span data-stu-id="50e8d-184">Transaction Connections</span></span>    |

### <a name="entity-flow"></a><span data-ttu-id="50e8d-185">엔터티 흐름</span><span class="sxs-lookup"><span data-stu-id="50e8d-185">Entity flow</span></span>

<span data-ttu-id="50e8d-186">프로젝트 실제는 Project Service Automation에서 관리되며 Finance에서 프로젝트 통합 저널과 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-186">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="50e8d-187">실제 값이 Finance에 전기된 후 Finance의 바우처 번호로 Project Service Automation에서 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-187">After actuals are posted in Finance, they are updated in Project Service Automation with the voucher number from Finance.</span></span> <span data-ttu-id="50e8d-188">Finance에 판매세가 추가된 경우 Project Service Automation에서 새 실제 세금이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-188">If sales taxes were added in Finance, new tax actuals are created in Project Service Automation.</span></span>

### <a name="power-query"></a><span data-ttu-id="50e8d-189">파워 쿼리</span><span class="sxs-lookup"><span data-stu-id="50e8d-189">Power Query</span></span>

<span data-ttu-id="50e8d-190">프로젝트 실제 업데이트 템플릿에서 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-190">In the project actuals update template, you must use Power Query to complete these tasks:</span></span>

- <span data-ttu-id="50e8d-191">Finance의 트랜잭션 유형을 Project Service Automation의 올바른 트랜잭션 유형으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-191">Transform the transaction type in Finance to the correct transaction type in Project Service Automation.</span></span> <span data-ttu-id="50e8d-192">이 변환은 프로젝트 실제 업데이트(Ops에서 PSA로) 템플릿에 이미 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-192">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>
- <span data-ttu-id="50e8d-193">Finance의 청구 유형을 Project Service Automation의 올바른 청구 유형으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-193">Transform the billing type in Finance to the correct billing type in Project Service Automation.</span></span> <span data-ttu-id="50e8d-194">이 변환은 프로젝트 실제 업데이트(Ops에서 PSA로) 템플릿에 이미 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-194">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="50e8d-195">데이터 통합의 템플릿 매핑</span><span class="sxs-lookup"><span data-stu-id="50e8d-195">Template mapping in Data integration</span></span>

<span data-ttu-id="50e8d-196">다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-196">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="50e8d-197">매핑은 Finance에서 Project Service Automation으로 동기화될 필드 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50e8d-197">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="50e8d-198">[![템플릿 매핑 - 실제 업데이트](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="50e8d-198">[![Template mapping - Actuals update](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="50e8d-199">[![템플릿 매핑 - 트랜잭션 업데이트](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="50e8d-199">[![Template mapping - Transaction update](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>
