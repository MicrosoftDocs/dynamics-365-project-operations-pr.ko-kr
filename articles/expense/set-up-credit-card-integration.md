---
title: 신용 카드 통합 설정
description: 이 항목은 경비 관련 신용 카드 거래를 가져오고 유지하는 방법을 설명합니다.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276176"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="405a4-103">신용 카드 통합 설정</span><span class="sxs-lookup"><span data-stu-id="405a4-103">Set up credit card integration</span></span>

<span data-ttu-id="405a4-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="405a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="405a4-105">경비 관련 신용 카드 거래는 반복되는 일정에 따라 자동으로 가져오도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="405a4-106">또는 필요에 따라 트랜잭션을 수동으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="405a4-107">신용 카드 거래는 신용 카드 거래 데이터 엔터티를 통해 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="405a4-108">신용 카드 거래 가져오기</span><span class="sxs-lookup"><span data-stu-id="405a4-108">Import credit card transactions</span></span>

1. <span data-ttu-id="405a4-109">**신용 카드 거래** 페이지에서 **트랜잭션 가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="405a4-110">처음으로 데이터 관리를 여는 경우 계속하기 전에 시스템에서 데이터 엔터티 목록을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="405a4-111">**이름** 필드에 가져오기 작업의 고유한 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="405a4-112">**소스 데이터 형식** 필드에서 가져올 신용 카드 거래가 포함된 파일 형식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="405a4-113">**업로드** 를 선택한 다음 가져올 파일을 찾아 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="405a4-114">파일이 업로드된 후 타일에서 **지도 보기** 링크를 선택하여 신용 카드 거래 파일과 신용 카드 거래 데이터 항목의 열 매핑을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="405a4-115">매핑 오류가 있거나 매핑을 변경해야 하는 경우 **매핑 시각화** 탭 또는 **매핑 세부 정보** 탭 중 하나에서 매핑을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="405a4-116">신용 카드 거래를 자동화하려면 **반복 데이터 작업 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="405a4-117">그런 다음 신용 카드 거래를 가져와야 하는 빈도를 정의하는 반복을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="405a4-118">완료되면 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="405a4-119">지금 선택한 파일을 가져오려면 **가져오기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="405a4-120">가져오는 동안 오류가 발생하면 실행 로그 또는 스테이징 데이터를 보고 성공적인 가져오기를 보장하기 위해 수정해야 하는 오류를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="405a4-121">둘 이상의 파일 형식을 가져와야 하는 경우 각 형식 유형에 대해 별도의 가져오기 작업을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="405a4-122">퇴직한 직원에 대한 신용 카드 거래 재지정</span><span class="sxs-lookup"><span data-stu-id="405a4-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="405a4-123">직원 레코드가 종료되면 직원의 AD DS(Active Directory 도메인 서비스) 계정이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="405a4-124">그러나 여전히 비용을 지불하고 상환해야 하는 활성 신용 카드 거래가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="405a4-125">**신용 카드 거래** 페이지에서 관련 사원이 종료된 신용 카드 거래에 대해 사원을 재지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="405a4-126">하나 이상의 신용 카드 거래를 선택한 다음 **거래 재지정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="405a4-127">그런 다음 신용 카드 거래를 지정할 다른 사원을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="405a4-128">신용 카드 거래가 재지정된 후 지출 보고서로 선택되고 지출 보고서 상환을 위한 일반적인 프로세스를 통해 지불될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]