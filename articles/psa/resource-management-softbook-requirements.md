---
title: 요건 가예약
description: 이 항목은 요건을 가예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147391"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="33569-103">요건 가예약</span><span class="sxs-lookup"><span data-stu-id="33569-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="33569-104">리소스 요건은 확정 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="33569-105">확정 예약은 리소스의 능력을 소비하는 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33569-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="33569-106">그런 다음 제안서가 승인을 위해 요청자에게 다시 발송됩니다.</span><span class="sxs-lookup"><span data-stu-id="33569-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="33569-107">가예약은 프로젝트 팀에 리소스를 임시로 추가하고 스케줄 게시판에 다른 상태를 가지지만 리소스의 능력을 소비하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="33569-108">스케줄 보드에서 리소스를 가예약하려면 **예약 상태** 필드를 **가예약** 으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="33569-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![예약 상태가 가예약으로 설정됨](media/Resource-Management-image77.png)

<span data-ttu-id="33569-110">**명명된 팀원** 보기에 **팀** 탭이 있으면 거기에 리소스가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="33569-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="33569-111">가예약된 시간은 **가예약된 시간** 열에 보고됩니다.</span><span class="sxs-lookup"><span data-stu-id="33569-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![명명된 팀원 보기에서 가예약된 시간](media/Resource-Management-image78.png)

<span data-ttu-id="33569-113">가예약된 팀원은 과업에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-113">Soft-booked team members can be assigned to tasks.</span></span>

![과업에 할당된 가예약된 팀원](media/Resource-Management-image79.png)

<span data-ttu-id="33569-115">**조정** 탭은 확정 예약만 고려하므로 **조정** 탭에는 리소스를 가예약하기 위한 예약이 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![조정 탭에서 예약하지 않고 가예약된 리소스](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="33569-117">일반 팀원으로부터 생성된 요건에서 리소스를 가예약할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="33569-118">스케줄 게시판에서 리소스에 대한 가예약에는 다른 색이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="33569-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![스케줄 게시판에서 가예약](media/Resource-Management-image81.png)

<span data-ttu-id="33569-120">가예약을 확정 예약으로 전환하려면 스케줄 게시판에서 가예약을 마우스 오른쪽 버튼으로 클릭한 다음 **상태 변경** \> **확정 예약** \> **확정** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33569-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![예약 상태를 확정으로 변경](media/Resource-Management-image82.png)

<span data-ttu-id="33569-122">예약이 변경되고 스케줄 게시판에서 상태가 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="33569-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="33569-123">예약 상태가 이제 **확정** 이기 때문에 리소스가 예약됨으로 표시되고 능력 및 가용성이 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="33569-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="33569-124">동일한 방법을 사용하여 스케줄 게시판에서 확정 예약 또는 가예약을 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33569-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="33569-125">가예약된 리소스를 프로젝트의 **팀** 탭에서 확정 예약으로 전환하려면 리소스를 선택한 다음 **확인** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="33569-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![확인 명령](media/Resource-Management-image83.png)
