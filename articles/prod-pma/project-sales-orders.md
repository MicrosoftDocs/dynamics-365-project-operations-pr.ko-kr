---
title: 시간 및 자재 프로젝트에 대한 프로젝트 판매 주문
description: 이 항목은 시간 및 자재 프로젝트에 대한 프로젝트 기반 판매 주문을 생성하는 방법을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080037"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="cad17-103">시간 및 자재 프로젝트에 대한 프로젝트 판매 주문</span><span class="sxs-lookup"><span data-stu-id="cad17-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cad17-104">이 항목은 프로젝트에 대한 판매 주문을 생성하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="cad17-105">판매 주문은 **시간 및 재료** 유형의 프로젝트에 대해서만 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="cad17-106">시간 및 자재 프로젝트에 프로젝트 계약의 여러 자금 출처가 있는 경우 **프로젝트 관리 및 회계 매개 변수** 페이지의 **자금 출처가 여러 개인 프로젝트에 대한 판매 주문 허용** 매개 변수를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="cad17-107">여러 자금 출처가 있는 프로젝트 판매 주문에 대한 지원은 애플리케이션 릴리스 10.0.2 이상부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="cad17-108">여러 자금 출처가 있는 프로젝트 판매 주문에 대한 지원을 활성화하는 매개 변수는 2020년 4월 릴리스 웨이브에서 제거되며 그 이후에는 기능이 항상 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="cad17-109">다음 두 가지 방법으로 프로젝트 기반 판매 주문을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="cad17-110">프로젝트로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-110">Go to the project itself.</span></span> <span data-ttu-id="cad17-111">작업 창에서 **관리 > 품목 작업 > 판매 주문** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="cad17-112">프로젝트 정보는 기본적으로 프로젝트의 판매 주문으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="cad17-113">프로젝트 계약에 둘 이상의 자금 출처가 있는 경우 판매 주문에 대한 고객을 설정하려면 자금 출처를 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="cad17-114">프로젝트에 자금 출처가 하나만 있는 경우 고객이 자동으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="cad17-115">**모든 판매 주문** 목록 페이지로 이동하고 새 판매 주문을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="cad17-116">판매 주문에 대한 프로젝트를 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="cad17-117">프로젝트를 선택한 후 고객은 자금 출처에서 설정되거나 프로젝트 계약에 자금 출처가 여러 개인 경우 자금 출처를 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad17-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

