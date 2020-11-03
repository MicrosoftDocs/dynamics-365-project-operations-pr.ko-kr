---
title: 홈 페이지 업그레이드
description: 이 항목은 Dynamics 365 Project Service Automation에서 새 기능 및 변경된 기능에 대한 중요한 정보와 최신 버전으로 업그레이드하는 프로세스를 확인할 수 있는 위치를 보여줍니다.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080133"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="ced10-103">홈 페이지 업그레이드</span><span class="sxs-lookup"><span data-stu-id="ced10-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="ced10-104">PSA 버전 2.x 또는 1.x에서 버전 3.x로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="ced10-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="ced10-105">새 인스턴스</span><span class="sxs-lookup"><span data-stu-id="ced10-105">New instances</span></span>

<span data-ttu-id="ced10-106">2019년 5월 17일 현재 새 인스턴스 프로비저닝 중에 Project Service Automation이 선택되면 버전 3.x가 기본적으로 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="ced10-107">기존 인스턴스</span><span class="sxs-lookup"><span data-stu-id="ced10-107">Existing instances</span></span>

<span data-ttu-id="ced10-108">이전에는 PSA 버전 2.x의 인스턴스를 가지고 있고 PSA의 통합 클라이언트 인터페이스 기반(UCI) 버전인 버전 3.x로 업그레이드해야 했던 고객은 Microsoft 지원팀에 연락하여 인스턴스의 세부 정보를 제공해야 했습니다. 그러면 지원팀이 버전 3.x로 업그레이드하기 위한 인스턴스를 활성화할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="ced10-109">2020년 3월 1일부터는 PSA 버전 2.x 인스턴스를 가지고 있고 버전 3.x로 업그레이드해야 하는 고객은 Microsoft 지원팀에 문의하지 않고도 관리 포털에서 직접 인스턴스를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="ced10-110">PSA 버전 3.x에는 중요한 변경 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="ced10-111">향상된 사용자 환경을 제공하기 위해 통합 인터페이스 프레임워크를 기반으로 구축되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="ced10-112">재설계된 이 앱은 일관되고 균일한 사용자 인터페이스(UI)를 제공하며, 어떤 화면 크기 또는 기기에서도 최적의 보기를 위한 반응형 디자인 원칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="ced10-113">애플리케이션 전체에 다른 변경 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="ced10-114">변경된 영역 중 일부는 가격 책정, 예약 및 리소스, 시간, 경비 및 결재를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="ced10-115">업그레이드 프로세스를 시작하기 전에 다음 과업을 완료하는 것이 좋습니다:</span><span class="sxs-lookup"><span data-stu-id="ced10-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="ced10-116">식별된 인스턴스에 Dynamics 365 Field Service 및 Project Service Automation이 설치되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="ced10-117">두 솔루션이 모두 설치된 경우, 인스턴스의 정기적인 사용을 다시 시작하기 전에 둘 다 업그레이드하도록 계획해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="ced10-118">다음 항목을 주의 깊게 검토하십시오.</span><span class="sxs-lookup"><span data-stu-id="ced10-118">Carefully review the following topics.</span></span> <span data-ttu-id="ced10-119">버전들 사이의 변경 사항에 대한 인식과 이해는 업그레이드 프로세스에 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="ced10-120">이러한 항목들은 PSA의 주요 변경 사항에 대한 정보와 버전 3.x로의 업그레이드 계획에 대한 고려 사항 및 권장 사항을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="ced10-121">Project Service Automation 버전 3의 새로운 내용 또는 변경 내용</span><span class="sxs-lookup"><span data-stu-id="ced10-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="ced10-122">업그레이드 고려 사항 - Project Service Automation 버전 2.x 또는 1.x에서 버전 3</span><span class="sxs-lookup"><span data-stu-id="ced10-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="ced10-123">생산 인스턴스를 업그레이드하기 전에 샌드박스 인스턴스를 업그레이드하여 구현의 변경 사항을 평가하십시오.</span><span class="sxs-lookup"><span data-stu-id="ced10-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="ced10-124">앞에서 언급한 항목을 검토하고 PSA 버전 3.x 또는 UCI 기반 버전으로 업그레이드할 준비가 된 후 관리 센터에서 업그레이드를 사용할 수 있도록 Microsoft 지원팀에 요청을 제출하십시오.</span><span class="sxs-lookup"><span data-stu-id="ced10-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="ced10-125">요청에서 인스턴스의 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="ced10-126">새로 만든 인스턴스에서 PSA의 이전 버전(PSA 버전 2.x)</span><span class="sxs-lookup"><span data-stu-id="ced10-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="ced10-127">2019년 5월 17일부로 모든 새 인스턴스에 UCI가 기본 클라이언트로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="ced10-128">이러한 변경에 따라 PSA 버전 3.x 및 Field Service 버전 8.x는 UCI 클라이언트에서 작동하도록 설계되었기 때문에 기본적으로 프로비전됩니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="ced10-129">2020년 3월 1일부터 Dynamics PSA 고객은 더 이상 이전 버전의 PSA(예: PSA 버전 2.x 이하)로 새 환경을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="ced10-130">새로운 환경에서는 PSA 버전 3.x만 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="ced10-131">이전 버전의 Field Service 및 PSA 애플리케이션을 사용할 때 최상의 경험을 위해서는 **시스템 설정** 페이지로 이동하여, **새 통합 인터페이스만 사용(권장)** 필드를 위해 **아니요** 를 선택하십시오. 이러한 버전은 UCI에서 올바르게 로드되도록 설계되지 않았기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="ced10-132">UCI를 끄면 이전 웹 클라이언트를 사용하여 이러한 버전의 Field Service 및 PSA를 열고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ced10-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
