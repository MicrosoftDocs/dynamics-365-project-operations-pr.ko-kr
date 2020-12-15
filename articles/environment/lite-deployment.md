---
title: Project Operations 배포 - 라이트
description: 이 항목은 Project Operations 라이트 배포 - 견적 송장 거래를 설치하는 방법에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642191"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="77096-103">Project Operations 배포 - 라이트</span><span class="sxs-lookup"><span data-stu-id="77096-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="77096-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="77096-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="77096-105">Project Operations는 여러 배포 모델을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77096-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="77096-106">최상의 배포 모델을 결정하려면 [배포 유형](determine-deployment-type.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="77096-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="77096-107">이 배포, 라이트 배포 – 견적 송장 처리 결과 **Project Operations의 Common Data Service 전용 배포** 가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77096-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="77096-108">Project Operations를 새 CDS 환경에 설치</span><span class="sxs-lookup"><span data-stu-id="77096-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="77096-109">기존 CDS 환경에 설치</span><span class="sxs-lookup"><span data-stu-id="77096-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="77096-110">Project Operations를 새 CDS 환경에 설치</span><span class="sxs-lookup"><span data-stu-id="77096-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="77096-111">Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)는 새로운 CDS 환경을 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="77096-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="77096-112">**CDS 데이터베이스** 및 **Dynamics 365 앱** 이 활성화되는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="77096-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="77096-113">자세한 내용은 [Power Platform 관리 센터에서 환경 만들기 및 관리](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="77096-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="77096-114">Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="77096-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="77096-115">Project Operations를 기존 CDS 환경에 설치</span><span class="sxs-lookup"><span data-stu-id="77096-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="77096-116">Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)는 Project Operations를 설치하려는 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에서 환경을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77096-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="77096-117">Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="77096-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="77096-118">자세한 내용은 [Dynamics 365 앱 관리](https://docs.microsoft.com/power-platform/admin/manage-apps)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="77096-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


