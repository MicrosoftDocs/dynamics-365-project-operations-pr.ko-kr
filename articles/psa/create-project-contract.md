---
title: 프로젝트 계약 만들기
description: 프로젝트 계약을 만드는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7a626da271a4c4e1751870323b56ce54743bb891
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080066"
---
# <a name="create-a-project-contract-project-service"></a><span data-ttu-id="dc88f-103">프로젝트 계약서 만들기(Project Service)</span><span class="sxs-lookup"><span data-stu-id="dc88f-103">Create a project contract (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dc88f-104">프로젝트에 대한 견적이 완성되면 계약서를 만들어 고객과 공식 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-104">Now that you’ve won the quote for your project, it’s time to create a contract with your customer and make it official.</span></span> <span data-ttu-id="dc88f-105">각 견적에 대해 여러 계약서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-105">You can create one or more contracts for each quote.</span></span> <span data-ttu-id="dc88f-106">프로젝트의 **계약** 단계에서 계약서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-106">When you’re creating a contract, you’re in the **Contract** phase of your project.</span></span>  
  
1. <span data-ttu-id="dc88f-107">이전 단계의 **프로젝트 계약** 화면에서 **요약** 영역의 필요한 정보를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-107">In the **Project Contract** screen from the previous step, change any information as necessary in the **Summary** area.</span></span>  
  
2. <span data-ttu-id="dc88f-108">계약 대상 제품을 추가하려면 **계약 내용** 영역의 **제품 기반 내용** 아래에 있는 **새로 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-108">To add a product to the contract, click **New** under **Product-based Lines** in the **Contract Lines** area.</span></span> <span data-ttu-id="dc88f-109">**제품 이름** 아래 항목을 선택한 다음 수량, 영업 가격 및 계약 총액을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-109">Select an item under **Product Name** , and then specify the quantity, sales price, and contracted amount.</span></span>  
  
3. <span data-ttu-id="dc88f-110">계약서에 프로젝트 기반 내용을 추가하려면 **계약 내용** 영역의 **프로젝트 기반 내용** 아래에 있는 **+** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-110">To add a project-based line to the contract, click **+** under **Project-based Lines** in the **Contract Lines** area.</span></span> <span data-ttu-id="dc88f-111">가능한 경우 이름, 예산 총액 및 프로젝트를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-111">Enter the name, budget amount, and project, if available.</span></span> <span data-ttu-id="dc88f-112">작업 분할 구조로 프로젝트를 만들어 예상을 생성해야 할 경우 [프로젝트 만들기](../psa/create-project.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="dc88f-112">If you need to create a project with a work breakdown structure to come up with an estimate, see [Create a project](../psa/create-project.md).</span></span>  
  
4. <span data-ttu-id="dc88f-113">편집을 마쳤으면, 화면 우측 하단의 **저장** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-113">When you’re done editing, click the **Save** button at the bottom right of the screen.</span></span>  
  
5. <span data-ttu-id="dc88f-114">계약서를 고객에게 보낼 준비가 되면 **더 보기** (...)를 클릭하고 **보고서 실행** 을 클릭한 다음 **주문** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-114">When you’re ready to send the contract to your customer, click **More** (…), click **Run Report** , and then click **Order**.</span></span> <span data-ttu-id="dc88f-115">[!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] 문서로 보고서를 저장하고 필요한 경우 편집한 다음 계약서를 고객에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-115">Save the report as a [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] document, edit as necessary, and then send the contract to your customer.</span></span>  
  
6. <span data-ttu-id="dc88f-116">고객이 계약 내용을 승인할 경우, **프로젝트 계약** 화면 상단의 **승인** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-116">If your customer confirms your contract, click **Confirm** at the top of the **Project Contract** screen.</span></span> <span data-ttu-id="dc88f-117">고객이 항목 변경을 원할 경우 새 계약서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-117">If your customer wants you to change some items, create a new contract.</span></span> <span data-ttu-id="dc88f-118">고객이 지금 서비스를 사용하지 않기로 결정할 경우, **프로젝트 계약** 화면 상단의 **실패로 종료** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88f-118">If your customer decides not to use your services at this time, click **Close as Lost** at the top of the **Project Contract** screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dc88f-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dc88f-119">See Also</span></span>  
 [<span data-ttu-id="dc88f-120">거래처 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="dc88f-120">Account Manager Guide</span></span>](../psa/account-manager-guide.md)
