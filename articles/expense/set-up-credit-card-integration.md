---
title: 신용 카드 통합 설정
description: 이 항목은 경비 관련 신용 카드 트랜잭션을 처리하는 방법을 설명합니다.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001833"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="cb9ba-103">신용 카드 통합 설정</span><span class="sxs-lookup"><span data-stu-id="cb9ba-103">Set up credit card integration</span></span>

<span data-ttu-id="cb9ba-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="cb9ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb9ba-105">경비 관련 신용 카드 거래는 반복되는 일정에 따라 자동으로 가져오도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="cb9ba-106">또는 필요에 따라 트랜잭션을 수동으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="cb9ba-107">신용 카드 거래는 신용 카드 거래 데이터 엔터티를 통해 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="cb9ba-108">신용 카드 거래 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb9ba-108">Import credit card transactions</span></span>

<span data-ttu-id="cb9ba-109">신용 카드 트랜잭션을 가져오려면 다음 단계를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="cb9ba-110">**신용 카드 거래** 페이지에서 **트랜잭션 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="cb9ba-111">처음으로 데이터 관리를 여는 경우 계속하기 전에 시스템에서 데이터 엔터티 목록을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="cb9ba-112">**이름** 필드에서 가져오기 작업에 대한 고유한 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="cb9ba-113">**소스 데이터 형식** 필드에서 가져올 신용 카드 거래가 포함된 파일 형식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="cb9ba-114">**업로드** 를 선택한 다음 가져올 파일을 찾아 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="cb9ba-115">파일이 업로드된 후 타일에서 **지도 보기** 링크를 선택하여 신용 카드 거래 파일과 신용 카드 거래 데이터 항목의 열 매핑을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="cb9ba-116">매핑 오류가 있거나 매핑을 변경해야 하는 경우 **매핑 시각화** 탭 또는 **매핑 세부 정보** 탭 중 하나에서 매핑을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="cb9ba-117">신용 카드 거래를 자동화하려면 **반복 데이터 작업 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="cb9ba-118">그런 다음 신용 카드 거래를 가져와야 하는 빈도를 정의하는 반복을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="cb9ba-119">완료되면 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="cb9ba-120">지금 선택한 파일을 가져오려면 **가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="cb9ba-121">가져오기 중에 오류가 발생하면 실행 로그 또는 스테이징 데이터를 보고 성공적인 가져오기를 위해 수정해야 하는 오류를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="cb9ba-122">둘 이상의 파일 형식을 가져와야 하는 경우 각 형식 유형에 대해 별도의 가져오기 작업을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="cb9ba-123">퇴직한 직원에 대한 신용 카드 거래 재지정</span><span class="sxs-lookup"><span data-stu-id="cb9ba-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="cb9ba-124">직원 레코드가 종료되면 직원의 AD DS(Active Directory 도메인 서비스) 계정이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="cb9ba-125">그러나 여전히 비용을 지불하고 상환해야 하는 활성 신용 카드 거래가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="cb9ba-126">**신용 카드 트랜잭션** 페이지에서 관련 사원이 해고된 신용 카드 트랜잭션에 대해 사원을 재지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="cb9ba-127">하나 이상의 신용 카드 거래를 선택한 다음 **거래 재지정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="cb9ba-128">그런 다음 신용 카드 거래를 지정할 다른 사원을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="cb9ba-129">신용 카드 거래가 재지정된 후 지출 보고서로 선택되고 지출 보고서 상환을 위한 일반적인 프로세스를 통해 지불될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="cb9ba-130">신용 카드 트랜잭션 삭제</span><span class="sxs-lookup"><span data-stu-id="cb9ba-130">Delete credit card transactions</span></span> 

<span data-ttu-id="cb9ba-131">때로는 신용 카드 트랜잭션을 가져온 후 특정 트랜잭션을 삭제해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="cb9ba-132">이는 트랜잭션이 중복되었거나 데이터가 정확하지 않기 때문일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="cb9ba-133">관리자는 **신용 카드 트랜잭션 삭제** 기능을 사용하여 경비 보고서에 **첨부되지 않은** 신용 카드 트랜잭션을 선택하고 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="cb9ba-134">**정기 작업** > **신용 카드 트랜잭션 삭제** 로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="cb9ba-135">**필터** 를 선택하고 포함할 레코드를 식별하기 위한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="cb9ba-136">**확인** 을 선택하여 레코드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ba-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
