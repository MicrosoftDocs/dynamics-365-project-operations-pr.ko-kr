---
title: 리소스 할당 만들기
description: 이 항목은 일반 및 명명된 리소스 할당 만들기에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079965"
---
# <a name="create-resource-assignments"></a><span data-ttu-id="48759-103">리소스 할당 만들기</span><span class="sxs-lookup"><span data-stu-id="48759-103">Create resource assignments</span></span>

<span data-ttu-id="48759-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="48759-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="48759-105">리소스 할당은 프로젝트 팀 구성원을 리프 노드 작업에 직접 연결하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="48759-105">A resource assignment is the direct association of a project team member to a leaf node task.</span></span> <span data-ttu-id="48759-106">이 항목은 리소스를 할당하는 다른 방법에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-106">This topic provides information about the different ways to assign resources.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="48759-107">작업 할당을 통한 일반 팀원 생성</span><span class="sxs-lookup"><span data-stu-id="48759-107">Create a generic team member through task assignment</span></span>


<span data-ttu-id="48759-108">작업 할당을 통해 일반 팀 구성원을 만들 때 자리 표시자 또는 일반 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48759-108">When you create a generic team member through task assignment, you create a placeholder or generic resource.</span></span> <span data-ttu-id="48759-109">이 일반 리소스는 궁극적으로 작업을 수행하려는 명명된 리소스의 특성을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-109">This generic resource describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="48759-110">그런 다음 명명된 리소스를 검색하고 예약하는 데 사용되는 요건을 생성하거나 요건을 사용하여 요청을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-110">You then generate a requirement, or submit a request using the requirement, that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="48759-111">작업의 일정 그리드에서 **리소스** 셀에 있는 리소스 아이콘을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-111">On the Schedule grid for a task, select the Resource icon in the **Resource** cell.</span></span>
2. <span data-ttu-id="48759-112">자리 표시자 리소스 이름으로 사용할 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-112">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="48759-113">예: 프로그램 관리자.</span><span class="sxs-lookup"><span data-stu-id="48759-113">For example, Program Manager.</span></span>
3. <span data-ttu-id="48759-114">**생성** 을 선택하고 **프로젝트 팀원 빠른 생성** 필드에서 일반 리소스에 대한 역할을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-114">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>
4. <span data-ttu-id="48759-115">작업에 대한 **리소스 선택기** 에서 리소스를 선택하여 필요하면 이 자리 표시자 리소스에 작업을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-115">Assign tasks as needed to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="48759-116">**팀원** 아래에 리소스가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-116">The resources listed under **Team Members**.</span></span>
5. <span data-ttu-id="48759-117">일반 리소스 할당을 마쳤으면 **팀** 탭에서 일반 리소스를 선택하고 **요구 사항 생성** 을 선택하여 일반 리소스에 대한 리소스 요구 사항을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48759-117">When you’re finished assigning the generic resource, on the **Team** tab, select the generic resource, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>
6. <span data-ttu-id="48759-118">일반 리소스에 대해 **예약** 을 선택한 다음 일정 게시판을 사용하여 실제 리소스를 찾고 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-118">Select **Book** for the generic resource and then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="48759-119">리소스 관리자가 이행 요구 사항을 제출할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48759-119">You can also submit the requirement for fulfillment by a resource manager.</span></span>
7. <span data-ttu-id="48759-120">명명된 리소스를 사용하여 일반 리소스가 완전히 충족되면(부분 리소스 요구 사항 충족으로 리소스 할당이 발생하지 않음) 일반 리소스가 팀에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-120">When the generic resource is fully fulfilled (partial resource requirement fulfillment will not result in a resource assignment) with a named resource, the generic resource is removed from the team.</span></span> <span data-ttu-id="48759-121">일반 리소스에 대한 작업 할당은 일반 리소스의 리소스 요구 사항을 충족하는 명명된 리소스에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-121">The task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="48759-122">예약 가능한 모든 리소스 목록에서 명명된 리소스 할당</span><span class="sxs-lookup"><span data-stu-id="48759-122">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="48759-123">**리소스 선택기** 의 검색 상자를 사용하여 예약 가능한 모든 활성 리소스를 검색하고 리프 노드 작업에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48759-123">You can use the search box in the **Resource Picker** to search all active bookable resources and assign them to any leaf node task.</span></span> <span data-ttu-id="48759-124">이 방법으로 할당된 리소스는 예약 없이 팀에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-124">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="48759-125">이는 팀원을 추가하고 **없음** 을 할당 방법으로 선택하는 것과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-125">This is similar to adding a team member and selecting **None** as the allocation method.</span></span> <span data-ttu-id="48759-126">리소스는 **팀** , **리소스 할당** 및 **조정** 탭에 할당 및 예약 부족만 있는 리소스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-126">The resource is displayed on the **Team** , **Resource Assignment** , and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="48759-127">가용성을 사용하려면 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-127">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="48759-128">작업 그리드, 게시판 또는 시간 표시줄에서 **할당 대상** 셀로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-128">From the task grid, board, or timeline, navigate to the **Assigned To** cell.</span></span>
2. <span data-ttu-id="48759-129">검색 상자에 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-129">In the search box, start typing a name.</span></span> <span data-ttu-id="48759-130">이름에 대한 검색 결과는 **리소스 선택기** 의 **기타 리소스** 에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48759-130">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>
3. <span data-ttu-id="48759-131">작업에 할당할 리소스를 선택하거나 **기타 팀 리소스** 아래에서 리소스 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="48759-131">Select the resource that you want to assign to the task or select the name of the resource under **Other Team Resources**.</span></span>
