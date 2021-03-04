---
title: Project Service Automation 업데이트 릴리스 20, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 20, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147121"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="e1346-103">Project Service Automation 업데이트 릴리스 20, V3</span><span class="sxs-lookup"><span data-stu-id="e1346-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e1346-104">Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e1346-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e1346-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e1346-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="e1346-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e1346-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1346-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e1346-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 20에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="e1346-110">이 버전의 빌드 번호는 V 3.10.31.37이며 일반적으로 2020년 6월 자체 업데이트를 통해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="e1346-111">업데이트 릴리스 20</span><span class="sxs-lookup"><span data-stu-id="e1346-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e1346-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="e1346-112">Bug fixes</span></span>

<span data-ttu-id="e1346-113">**프로젝트 관리**</span><span class="sxs-lookup"><span data-stu-id="e1346-113">**Project Management**</span></span>

<span data-ttu-id="e1346-114">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e1346-115">시간이 필요한 할당 방법으로 프로젝트 팀 구성원을 가져오면 지정된 시간이 0일 때 오류 메시지가 명확하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="e1346-116">프로젝트 작업의 **설명** 필드에 최대 문자 수를 입력하면 사용자에게 잘못된 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="e1346-117">사용자의 언어 설정이 일본어로 설정되어 있으면 **Microsoft Dynamics 365 Project Service Automation 추가 기능 다운로드** 페이지가 영어 다운로드 페이지로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="e1346-118">서버 오류가 발생하면 **프로젝트** 양식의 **일정** 탭에 있는 동기화 레이블이 때때로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="e1346-119">작업이 수정되면 중복 작업 업데이트가 서버로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="e1346-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e1346-120">**Sales**</span></span>

<span data-ttu-id="e1346-121">다음과 같은 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="e1346-122">**계약** 양식에서 **송장 만들기** 를 두 번 클릭하면 단일 실제 레코드에 대해 두 개의 송장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="e1346-123">Internet Explorer 11에서 사용자는 비용 항목을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="e1346-124">비용 역분개 및 미청구 판매 실제 금액의 역분개는 연결되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="e1346-125">**계획** 양식의 **실제 새로 고침** 단추가 **작업 실제 시간** 을 새로 고치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="e1346-126">**PreValidateProjectTeamMemberCreate** 플러그인은 특성 **msdyn_isgenericresourceprojectscoped** 가 **False** 로 설정될 때 중복 일반 예약 가능 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="e1346-127">**다시 계산** 은 제품 기반 견적 라인 세부 사항 및 계약 내용 세부 사항의 청구 가능 비용을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="e1346-128">특정 시나리오에서 **PostEstimateLineUpdate** 플러그인은 null 참조 예외 오류를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="e1346-129">**수익성 분석 차트** 의 시간 단계 기간이 견적의 고정 가격 견적 라인 세부 사항의 비용 기간과 일치하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="e1346-130">**계약 내용 세부 사항** 및 **견적 라인 세부 사항** 양식의 비용 범주에 대해 단위 및 단위 그룹 값이 올바른 기본값이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="e1346-131">**조직 단위 원가** 목록은 유효 날짜의 중복을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="e1346-132">사용자는 **조직 단위** 를 변경할 수 없습니다. 주문 유형이 작업 기반이 아닌 경우 null 참조 예외 오류가 발생하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="e1346-133">**견적 라인 세부 사항** 양식에서 탐색하려고 할 때 , **견적** 탭으로 돌아가고 양식이 새로 고쳐지고 **요약** 탭이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1346-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
