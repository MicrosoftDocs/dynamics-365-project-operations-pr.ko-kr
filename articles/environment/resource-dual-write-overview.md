---
title: Project Operations 이중 쓰기 통합
description: 이 항목은 Project Operations 이중 쓰기 통합에 대한 개요를 제공합니다.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368439"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="7ab7e-103">Project Operations 이중 쓰기 통합 개요</span><span class="sxs-lookup"><span data-stu-id="7ab7e-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="7ab7e-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7ab7e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7ab7e-105">Project Operations는 [이중 쓰기 기능](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)을 사용하여 Microsoft Dataverse 및 Dynamics 365 Finance를 통해 데이터를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="7ab7e-106">다음 그림은 Dataverse와 Finance 간의 통합의 일부로 데이터가 동기화되는 방식을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations 데이터 흐름 개요](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="7ab7e-108">Dataverse의 Project Operations는 최신 사용자 인터페이스(UI)와 Power Platform 기능을 사용하여 코드가 없는 간편한/낮은 코드 확장성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="7ab7e-109">프로젝트 관리자, 리소스 관리자, 프로젝트 팀 구성원 및 기타 프론트 오피스 페르소나는 Dataverse에서 Project Operations에서 활동을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="7ab7e-110">Finance의 Project Operations는 프로젝트 회계 및 수익 인식 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="7ab7e-111">Project Operations는 판매세 계산, 환율, 재무 차원 보고 등을 위해 Finance의 재무 프레임워크에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="7ab7e-112">프로젝트 회계사 경험은 대부분 Finance를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="7ab7e-113">Project Operations는 다음 구성 요소 통합으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ab7e-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="7ab7e-114">Project Operations 설정 및 구성 데이터 통합</span><span class="sxs-lookup"><span data-stu-id="7ab7e-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="7ab7e-115">프로젝트 추정 및 실제</span><span class="sxs-lookup"><span data-stu-id="7ab7e-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="7ab7e-116">프로젝트 송장</span><span class="sxs-lookup"><span data-stu-id="7ab7e-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="7ab7e-117">경비 관리</span><span class="sxs-lookup"><span data-stu-id="7ab7e-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="7ab7e-118">공급업체 송장</span><span class="sxs-lookup"><span data-stu-id="7ab7e-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
