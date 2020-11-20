---
title: 리소스/비 재고 기반 시나리오에 대한 Project Operations 배포 개요
description: 이 항목은 배포 유형, 리소스/비 재고 기반 시나리오의 Project Operations에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365538"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="f33f2-103">리소스/비 재고 기반 시나리오에 대한 Project Operations 배포 개요</span><span class="sxs-lookup"><span data-stu-id="f33f2-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="f33f2-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f33f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f33f2-105">배포 유형인 리소스/비재고 기반 시나리오에 대한 Dynamics 365 Project Operations에는 프로젝트 기반 회사를 위한 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="f33f2-106">웹용 Microsoft Project를 사용한 프로젝트 계획</span><span class="sxs-lookup"><span data-stu-id="f33f2-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f33f2-107">인건비에 대한 다차원적 가격 책정 및 비용</span><span class="sxs-lookup"><span data-stu-id="f33f2-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="f33f2-108">비용 범주에 대한 범주 기반 가격 책정</span><span class="sxs-lookup"><span data-stu-id="f33f2-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="f33f2-109">Dynamics 365 Sales 기능을 사용한 프로젝트 기반 영업 관리</span><span class="sxs-lookup"><span data-stu-id="f33f2-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="f33f2-110">Dynamics 365 Field Service 및 Dynamics 365 Customer Service 같은 다른 응용 프로그램과 통합되는 Universal Resource Scheduling</span><span class="sxs-lookup"><span data-stu-id="f33f2-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="f33f2-111">프로젝트 진행 및 시간 추적</span><span class="sxs-lookup"><span data-stu-id="f33f2-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="f33f2-112">OCR 기능을 사용하여 영수증 캡처를 포함한 프로젝트 및 비 프로젝트 경비에 대한 기본 및 전체 경비 관리 경험</span><span class="sxs-lookup"><span data-stu-id="f33f2-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="f33f2-113">견적에서 고객 대면으로 확장되고 엔터프라이즈급 판매세 및 날짜 효율적인 환율 시스템으로 뒷받침되는 송장 발행.</span><span class="sxs-lookup"><span data-stu-id="f33f2-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="f33f2-114">진행 중인 작업(WIP) 회계 및 발생에 대한 구성 가능한 프로젝트 비용, 수익 프로필 및 규칙</span><span class="sxs-lookup"><span data-stu-id="f33f2-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="f33f2-115">프로젝트 수익 인식</span><span class="sxs-lookup"><span data-stu-id="f33f2-115">Project revenue recognition</span></span>
- <span data-ttu-id="f33f2-116">Power Platform을 통한 확장성</span><span class="sxs-lookup"><span data-stu-id="f33f2-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="f33f2-117">이 배포 유형은 Dynamics 365 Finance 및 Dynamics 365 Supply Chain Management 응용 프로그램에서 제공하는 기능에 대한 확장을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="f33f2-118">이 배포는 Project Operations가 다음 요구 사항을 포함하는 전체 프로젝트 수명 주기를 사용하는 것으로 예상되므로 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="f33f2-119">Sales 애플리케이션의 기능을 사용하여 다른 유형의 영업으로 프로젝트 기반 영업을 관리하는 기능.</span><span class="sxs-lookup"><span data-stu-id="f33f2-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="f33f2-120">프로젝트 영업에서 회계에 이르기까지 일정 및 재무에 대한 내부 및 청구 가능한 프로젝트를 관리하는 통합 프로젝트 관리 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="f33f2-121">프로젝트 및 비 프로젝트 경비를 추적하기 위한 정책 집행 및 환급을 포함하는 경비 관리 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="f33f2-122">프로젝트에 대한 고객 대면 송장을 생성하는 풍부한 엔터프라이즈급 판매세 및 환율 엔진이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f33f2-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="f33f2-123">IFRS(International Financial Reporting Standards)를 준수하는 프로젝트 회계 및 수익 인식 시스템.</span><span class="sxs-lookup"><span data-stu-id="f33f2-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="f33f2-124">Finance 또는 Supply Chain Management 애플리케이션 및 프로젝트 기반 거래 통합.</span><span class="sxs-lookup"><span data-stu-id="f33f2-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
