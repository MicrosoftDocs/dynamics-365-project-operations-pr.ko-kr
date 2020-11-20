---
title: Project Service Automation 업데이트 릴리스 12, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 12, V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: fc92a5dcc111688159f9be5b2839b7c040404a3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119966"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="49085-103">Project Service Automation 업데이트 릴리스 12, V3</span><span class="sxs-lookup"><span data-stu-id="49085-103">Project Service Automation Update Release 12, V3</span></span>
<span data-ttu-id="49085-104">Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="49085-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="49085-105">이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="49085-106">이 릴리스는 Dynamics 365 9.x와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="49085-107">이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오.</span><span class="sxs-lookup"><span data-stu-id="49085-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="49085-108">자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49085-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="49085-109">이 항목에는 Project Service Automation V3, 업데이트 릴리스 12에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="49085-110">이 버전의 빌드 번호는 V3.10.2.34이며 2019년 10월에 자체 업데이트를 통해 일반적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="49085-111">업데이트 릴리스 12</span><span class="sxs-lookup"><span data-stu-id="49085-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="49085-112">버그 수정</span><span class="sxs-lookup"><span data-stu-id="49085-112">Bug fixes</span></span>

- <span data-ttu-id="49085-113">시간 및 경비</span><span class="sxs-lookup"><span data-stu-id="49085-113">Time and Expense</span></span>

    - <span data-ttu-id="49085-114">수정: 시간 항목 오류 메시지가 더 관련성이 높은 컨텍스트로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="49085-115">수정: 필요할 때 시간 항목 표 및 일정이 세로 스크롤 막대를 올바르게 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="49085-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="49085-116">수정: 제출된 비용 및 시간 항목을 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="49085-117">수정: 승인 상태가 **승인됨** 에서 **제출됨** 으로 변경될 때 승인 확인 취소 대화 상자 메시지가 승인 상태를 반영하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="49085-118">수정: **가격**, **단위**, **수량** 필드는 승인된 후에 비용 레코드에서 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="49085-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="49085-119">프로젝트 관리</span><span class="sxs-lookup"><span data-stu-id="49085-119">Project Management</span></span>

    - <span data-ttu-id="49085-120">수정: **팀 구성원** 기본 양식에서 **새로 만들기** 작업이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="49085-121">수정: 리소스 할당이 부정확한 반올림 오류를 반영하도록 업데이트되어 작업 종료 날짜가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="49085-122">수정: 작업 표에서 관련 서버 측 오류가 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="49085-123">수정: 이제 작업 인물 선택기에 팀원 이름이 직책 이름 대신 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="49085-124">리소스 관리</span><span class="sxs-lookup"><span data-stu-id="49085-124">Resource Management</span></span>

    - <span data-ttu-id="49085-125">수정: 템플릿에서 생성된 프로젝트에 대한 리소스 요구 사항 세부 정보가 이제 프로젝트 일정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="49085-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="49085-126">수정: 기술 및 역량이 이제 역할 마스터 데이터에서 해당 역할에 대해 생성된 리소스 요구 사항으로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="49085-127">Sales</span><span class="sxs-lookup"><span data-stu-id="49085-127">Sales</span></span>

    - <span data-ttu-id="49085-128">수정: 중복 개체 ID가 **계약 기본** 양식에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="49085-129">수정: **견적 분석** 탭이 표시되어 탭의 메타데이터 설정이 표시되도록 논리가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49085-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="49085-130">수정: 실제 레코드의 회계 날짜는 이제 승인 날짜가 아닌 시간/비용 항목 날짜로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49085-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
