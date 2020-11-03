---
title: 프로젝트 계약 확인
description: 이 항목은 Project Operations에서 계약을 확인하는 방법에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080172"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="4c006-103">프로젝트 계약 확인</span><span class="sxs-lookup"><span data-stu-id="4c006-103">Confirm a project contract</span></span>

<span data-ttu-id="4c006-104">_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_</span><span class="sxs-lookup"><span data-stu-id="4c006-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4c006-105">Dynamics 365 Project Operations의 프로젝트 계약은 이유가 **확인됨** 인 경우 활성화되고 이유가 **손실** 인 경우 마감될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="4c006-106">프로젝트 계약을 확인하면 상태가 **초안** 에서 **활성** 으로 업데이트되고 상태 설명은 **확인됨** 이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="4c006-107">활성 또는 마감된 계약은 편집하거나 다시 열 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="4c006-108">프로젝트 계약 확인의 재정적 영향</span><span class="sxs-lookup"><span data-stu-id="4c006-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="4c006-109">프로젝트 계약이 확인되면 응용 프로그램은 이전의 실제 비용을 되돌리고 새로운 실제 비용을 생성하여 비용을 다시 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="4c006-110">그러면 연관된 프로젝트 계약 내용의 청구 방법에 따라 새 실제 비용이 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="4c006-111">실제 비용이 시간 및 재료 계약 내용을 참조하는 경우 응용 프로그램은 해당 청구되지 않은 실제 판매를 자동으로 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="4c006-112">실제 비용이 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 실제 비용 재처리를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="4c006-113">초과하지 않는 한도, 청구 가능성 설정, 실제 항목에 대한 가격 및 비용이 평가되고 확인 프로세스의 일부로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="4c006-114">프로젝트 계약을 손실로 마감</span><span class="sxs-lookup"><span data-stu-id="4c006-114">Close a project contract as lost</span></span>

<span data-ttu-id="4c006-115">프로젝트 계약을 손실로 마감하면 계약 상태가 **마감** 으로 업데이트되고 상태 설명은 **손실** 이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="4c006-116">프로젝트 계약은 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-116">The project contract becomes read-only.</span></span> <span data-ttu-id="4c006-117">마감된 프로젝트 계약을 다시 열 수 없기 때문에 변경이 완료되기 전에 확인 대화 상자가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="4c006-118">손실로 마감된 프로젝트 계약이 해당 라인의 프로젝트를 참조하는 경우 해당 프로젝트도 마감된 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="4c006-119">그 날 이후의 모든 리소스 예약은 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="4c006-120">송장에 아직 없는 프로젝트 계약의 청구되지 않은 실제 판매는 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="4c006-121">Dynamics 365 Project Operations에서 프로젝트 계약을 손실로 마감해도 관련 영업 기회의 상태에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="4c006-122">영업 기회는 열린 상태로 유지되며 수동으로 닫아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c006-122">The opportunity will remain open and must be manually closed.</span></span>
