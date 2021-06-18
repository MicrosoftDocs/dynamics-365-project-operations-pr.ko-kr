---
title: 보고 홈 페이지
description: 이 주제는 Dynamics 365 Project Service Automation에서의 보고에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 6c35729e51b7439a74446641af3feace5c7751ac
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998104"
---
# <a name="reporting-home-page"></a><span data-ttu-id="5ca33-103">보고 홈 페이지</span><span class="sxs-lookup"><span data-stu-id="5ca33-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5ca33-104">Microsoft Dynamics 365 Project Service Automation을 사용하여 프로젝트 기반 조직이 비즈니스 운영을 효율적으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="5ca33-105">어떤 프로젝트에서든 팀원은 기회를 관리하고, 작업을 견적 및 계획하고, 프로젝트를 리소싱하고, 계획에 따라 작업을 관리하고, 작업에 대한 청구서를 작성하고, 프로젝트를 완료하기 위해 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="5ca33-106">운영에 대한 보고 기능은 조직의 상태를 판단하고 요구되는 시정 조치를 취하는 데 관건입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="5ca33-107">PSA는 모든 보고를 위해 Microsoft Dynamics 365의 보고 방법과 기술을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="5ca33-108">보고 옵션에 대한 자세한 내용은 [Dynamics 365 Customer Engagement (on-premises), 버전 9에 대한 보고서 작성 가이드](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ca33-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="5ca33-109">보고서 마법사</span><span class="sxs-lookup"><span data-stu-id="5ca33-109">Report Wizard</span></span>

<span data-ttu-id="5ca33-110">보고서 마법사를 사용하면 개발자 이외의 사람이 간단한 보고서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="5ca33-111">이 앱은 기존 플랫폼을 기반으로 구축되므로 그 경험은 [보고서 마법사를 사용한 보고서 만들기 또는 편집](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard)에 설명된 경험과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="5ca33-112">그러나 귀하는 Project Service Automation 관련 엔터티를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="5ca33-113">맞춤 SQL Server Reporting Services 보고서</span><span class="sxs-lookup"><span data-stu-id="5ca33-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="5ca33-114">귀하의 비즈니스가 보고서 마법사를 사용하여 만들 수 없는 특정 보고서를 요구하는 경우 맞춤 보고서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="5ca33-115">Microsoft Visual Studio가 설치되고, 해당 Microsoft SQL Server Data Tools 및 Report Authoring Extension이 함께 설치되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="5ca33-116">도구 및 버전에 대한 자세한 설명은 [SQL Server Data Tools를 사용한 보고서 쓰기 환경](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="5ca33-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="5ca33-117">맞춤 보고서를 만드는 방법에 대한 자세한 설명은 [SQL Server Data Tools를 사용한 새 보고서 만들기](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="5ca33-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="5ca33-118">Power BI 인사이트 앱</span><span class="sxs-lookup"><span data-stu-id="5ca33-118">Power BI insights apps</span></span>

<span data-ttu-id="5ca33-119">또한 Microsoft Power BI 및 Dynamics 365는 인사이트 앱의 형태로 귀하의 데이터를 작업할 수 있는 강력한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca33-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="5ca33-120">인사이트 앱의 가용성에 대한 자세한 설명은 [Power BI 인사이트 앱 페이지](https://powerbi.microsoft.com/power-bi-insights-apps/)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="5ca33-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5ca33-121">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="5ca33-121">Additional resources</span></span>
<span data-ttu-id="5ca33-122">PSA에서의 보고에 대한 자세한 설명은 다음 항목들을 참조하십시오:</span><span class="sxs-lookup"><span data-stu-id="5ca33-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="5ca33-123">Project Service 데이터 모델 작업</span><span class="sxs-lookup"><span data-stu-id="5ca33-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="5ca33-124">대시보드</span><span class="sxs-lookup"><span data-stu-id="5ca33-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]