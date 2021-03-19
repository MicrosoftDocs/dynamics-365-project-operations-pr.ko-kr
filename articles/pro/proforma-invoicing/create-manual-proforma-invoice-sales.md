---
title: 수동 견적 송장 만들기 - 라이트
description: 이 항목은 Project Operations에서 수동 견적 송장 만들기에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274196"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="47dc7-103">수동 견적 송장 만들기 - 라이트</span><span class="sxs-lookup"><span data-stu-id="47dc7-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="47dc7-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="47dc7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47dc7-105">Dynamics 365 Project Operations에서 견적 송장은 필요에 따라 수동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="47dc7-106">**프로젝트 계약** 목록 페이지 또는 **프로젝트 계약** 세부 정보 페이지에서 수동으로 견적 송장을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="47dc7-107">프로젝트 계약 목록 페이지</span><span class="sxs-lookup"><span data-stu-id="47dc7-107">Project Contracts list page</span></span>

<span data-ttu-id="47dc7-108">**프로젝트 계약** 목록 페이지에서 하나 이상의 프로젝트 계약을 선택하고 선택한 모든 레코드에 대한 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="47dc7-109">시스템은 선택한 프로젝트 계약 중 오늘 날짜 이전의 **송장 준비** 백 로그가 있는 계약이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="47dc7-110">이러한 계약에서 시스템은 초안 견적 송장을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="47dc7-111">프로젝트 계약에 여러 고객이 있는 경우 고객당 하나의 송장이 생성되고 프로젝트 계약당 여러 송장이 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="47dc7-112">생성된 모든 프로젝트 송장은 **영업** 영역의 **청구** 섹션에 있는 **송장** 페이지에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="47dc7-113">프로젝트 계약 세부 정보 페이지</span><span class="sxs-lookup"><span data-stu-id="47dc7-113">Project Contract details page</span></span>

<span data-ttu-id="47dc7-114">**프로젝트 계약** 세부 정보 페이지에서도 견적 송장을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="47dc7-115">시스템은 프로젝트 계약에 오늘 날짜 이전의 **송장 발부 준비 완료** 백 로그가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="47dc7-116">이러한 계약에서 시스템은 각 계약 내용의 고객 수를 기반으로 견적 송장 초안을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="47dc7-117">하나의 견적 송장이 생성되면 **송장** 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="47dc7-118">해당 프로젝트 계약에 대해 여러 송장이 생성된 경우 생성된 모든 송장을 표시하는 **송장** 목록 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="47dc7-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]