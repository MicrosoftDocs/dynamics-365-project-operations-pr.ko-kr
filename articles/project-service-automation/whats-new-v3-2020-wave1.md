---
title: Project Service Automation 버전 3.x 웨이브 1 2020의 새로운 내용 또는 변경 내용
description: 이 항목에서는 Project Service Automation 버전 3 웨이브 1 2020의 새로운 사항과 변경된 내용에 대한 정보를 제공합니다.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753271"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="059a2-103">Project Service Automation 버전 3 웨이브 1 2020의 새로운 내용 또는 변경 내용</span><span class="sxs-lookup"><span data-stu-id="059a2-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="059a2-104">이 항목에서는 PSA(Project Service Automation) 버전 3.x wave 1 2020의 최신 릴리스로 이동할 때 주요 업그레이드 고려 사항을 강조합니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="059a2-105">시간 항목</span><span class="sxs-lookup"><span data-stu-id="059a2-105">Time entry</span></span>
<span data-ttu-id="059a2-106">더 많은 고객 시나리오로 시간 항목을 확장할 수 있는 기능을 제공하기 위해 시간 항목 경험이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="059a2-107">여기에는 필드 스키마 이름 **시간 항목 설정**을 기반으로 **시간 원본**으로 표시되는 특정 동작을 유도하는 항목 유형을 추가하는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="059a2-108">업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="059a2-108">Upgrade consideration</span></span>
<span data-ttu-id="059a2-109">이 기능을 지원하기 위해 PSA 내의 역할이 새로운 권한을 포함하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="059a2-110">이러한 권한은 새로운 엔터티 **시간 항목 설정**에 대한 읽기 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="059a2-111">시간을 기록하는 기능이 필요한 사용자에게는 기존 역할 외에 사용자 역할 **시간 항목 사용자**가 부여되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="059a2-112">이 역할에는 새로운 기능이 포함되며 시간 항목은 계속 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="059a2-113">현재 확장된 시간 항목 변경 사항</span><span class="sxs-lookup"><span data-stu-id="059a2-113">Currently extended time entry changes</span></span>
<span data-ttu-id="059a2-114">현재 시간 항목 사용자에게 미치는 영향을 최소화하기 위해 이 역할 변경은 시간 항목을 계속 사용하는 데 필요한 유일한 핵심 요구 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="059a2-115">사용자 지정 보기나 별도의 시간 항목 경험을 를 작성한 경우 **시간 항목 설정** 필드를 올바른 PSA 값으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a2-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
