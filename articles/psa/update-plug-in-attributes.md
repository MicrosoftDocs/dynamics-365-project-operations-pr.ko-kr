---
title: 새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트
description: 이 주제는 가격 책정 차원에 대한 플러그인 속성 업데이트에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147076"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="8cc36-103">새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="8cc36-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="8cc36-104">Project Service Automation(PSA)의 견적 및 계약 기능을 사용하지 않는 경우에는 이 주제를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="8cc36-105">이 항목은 귀하가 본 주제의 [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities.md), [가격 설정 및 트랜잭션 엔터티에 맞춤 필드 추가](field-references.md), 및 [가격 책정 차원으로 맞춤 필드 설정](set-up-pricing-dimensions.md) 항목의 절차를 완료했다고 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="8cc36-106">이러한 절차를 완료하지 않은 경우 돌아가서 완료한 다음 이 항목으로 돌아오십시오.</span><span class="sxs-lookup"><span data-stu-id="8cc36-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="8cc36-107">프로젝트 견적 행을 위한 **견적 행** 페이지에 견적 행 내역이 생성되면 시스템은 배경에 두 개의 추산 행(하나는 추산 값의 원가측, 하나는 매출액측)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="8cc36-108">프로젝트 계약 행에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="8cc36-109">원가 측면에서 수량 또는 필드를 변경하면 해당 변경이 매출액 측에 전파됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="8cc36-110">이는 가격 책정 차원을 변경한 후 다시 등록해야 하는 다음 플러그인으로 인해 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="8cc36-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="8cc36-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="8cc36-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="8cc36-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="8cc36-113">다음 단계는 플러그인을 등록하는 프로세스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="8cc36-114">**PluginRegistrationTool** 을 열고 온라인 인스턴스에 접속합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="8cc36-115">**검색** 을 클릭하고 업데이트할 플러그인을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![검색 트리의 스크린샷](media/PRT-1.png)

3. <span data-ttu-id="8cc36-117">플러그인을 찾은 후 플러그인을 선택한 다음 **기본 양식에서 선택** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="8cc36-118">업데이트할 플러그인의 단계를 선택하고 마우스 오른쪽 버튼으로 클릭한 다음 **업데이트** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![업데이트할 플러그인의 스크린샷](media/PRT-2.png)
 
5. <span data-ttu-id="8cc36-120">업데이트 창에서 필터링 속성의 타원(**...**)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![기존 단계 구성 정보 업데이트의 스크린샷](media/PRT-3.png)
 
6. <span data-ttu-id="8cc36-122">가격 책정 속성 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-122">Select the pricing attribute check boxes.</span></span>

 ![가격 속성에 대한 확인란 선택을 보여주는 스크린샷](media/PRT-4.png)

7. <span data-ttu-id="8cc36-124">**OK** 를 클릭하여 페이지를 닫은 다음 **업데이트 단계** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 !["업데이트 단계" 버튼을 보여주는 스크린샷](media/PRT-5.png)
 
8. <span data-ttu-id="8cc36-126">두 번째 플러그인 **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction** 을 위해 이 프로세스를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="8cc36-127">플러그인 등록 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc36-127">Close the plug-in registration tool.</span></span>

