---
title: 리소스/생산 기반 시나리오에 대한 Project Operations 배포 개요
description: 이 항목은 배포 유형, 재고/생산 기반 시나리오의 Project Operations에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ffbcb326e5cd86c49b3b3b27ce7d68404a6842b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289242"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="144d0-103">리소스/생산 기반 시나리오에 대한 Project Operations 배포 개요</span><span class="sxs-lookup"><span data-stu-id="144d0-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="144d0-104">_**적용 대상:** 리소스/생산 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="144d0-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="144d0-105">이 배포 유형에는 프로젝트 기반 회사에 대해 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="144d0-106">[작업 분할 구조](work-breakdown-structures.md)를 사용하는 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="144d0-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="144d0-107">프로젝트를 위한 재고 재고 인벤토리 확보 및 소비</span><span class="sxs-lookup"><span data-stu-id="144d0-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="144d0-108">Dynamics 365 Finance and Operations 앱의 **판매 및 마케팅** 모듈을 사용한 프로젝트 기반 영업 관리</span><span class="sxs-lookup"><span data-stu-id="144d0-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="144d0-109">Finance and Operations 앱의 비용 요율 및 청구 요율 구성을 사용한 프로젝트 가격 및 비용</span><span class="sxs-lookup"><span data-stu-id="144d0-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="144d0-110">Finance and Operations 앱에서 프로젝트에 대한 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="144d0-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="144d0-111">Finance and Operations 앱에서 프로젝트 진행 및 시간 추적</span><span class="sxs-lookup"><span data-stu-id="144d0-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="144d0-112">OCR 기능을 사용하여 영수증 캡처를 통해 프로젝트 및 비 프로젝트 경비에 대한 경비 관리 경험</span><span class="sxs-lookup"><span data-stu-id="144d0-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="144d0-113">엔터프라이즈급 판매세 및 날짜 효율적인 환율 시스템을 사용하여 송장 발행</span><span class="sxs-lookup"><span data-stu-id="144d0-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="144d0-114">WIP 회계 및 발생에 대한 구성 가능한 프로젝트 그룹</span><span class="sxs-lookup"><span data-stu-id="144d0-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="144d0-115">프로젝트 수익 인식</span><span class="sxs-lookup"><span data-stu-id="144d0-115">Project revenue recognition</span></span>

<span data-ttu-id="144d0-116">이 배포 유형은 또한 Dynamics 365 Finance 및 Dynamics 365 Supply Chain Management 응용 프로그램에서 제공하는 기능에 대한 확장을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="144d0-117">다음 주요 요구 사항을 포함하여 전체 프로젝트 수명 주기에 Dynamics 365 Project Operations를 사용하려면 이 배포 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="144d0-118">일정 및 재무에 대해 내부 및 청구 가능한 프로젝트에 대한 재고 항목 및 작업/생산 주문 비용을 관리하는 광범위한 프로젝트 관리 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="144d0-119">조직은 이미 Dynamics 365 Finance 또는 Dynamics 365 공급망 및 제조 앱과 프로젝트 기반 트랜잭션을 통합하면 데이터 액세스 및 보고 요구 사항이 간소화됩니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="144d0-120">프로젝트 및 비 프로젝트 경비를 추적하기 위한 정책 집행 및 환급을 포함하는 완전한 기능의 경비 관리 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="144d0-121">프로젝트에 대한 고객 대면 송장을 생성하는 엔터프라이즈급 판매세 및 환율 엔진입니다.</span><span class="sxs-lookup"><span data-stu-id="144d0-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="144d0-122">IFRS(International Financial Reporting Standards)를 준수하는 프로젝트 회계 및 수익 인식 시스템.</span><span class="sxs-lookup"><span data-stu-id="144d0-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]