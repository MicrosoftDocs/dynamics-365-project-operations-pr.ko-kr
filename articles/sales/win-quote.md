---
title: 견적 닫기
description: 이 항목은 Project Operations의 견적 종료에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124691"
---
# <a name="close-a-quote"></a><span data-ttu-id="48001-103">견적 닫기</span><span class="sxs-lookup"><span data-stu-id="48001-103">Close a quote</span></span>

<span data-ttu-id="48001-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="48001-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48001-105">프로젝트 견적은 성공 또는 실패로 마감될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48001-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="48001-106">Microsoft Dynamics 365 Project Operations의 견적에서는 활성화 및 수정 기능이 지원되지 않으므로 초안 견적을 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48001-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="48001-107">견적을 성공으로 종료</span><span class="sxs-lookup"><span data-stu-id="48001-107">Close a quote as Won</span></span>

<span data-ttu-id="48001-108">프로젝트 견적을 성공으로 종료하면 견적의 상태가 **종료됨** 으로 설정되고 상태 설명이 **성공** 으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="48001-109">견적을 종료하면 읽기 전용이 되고 모든 견적 정보가 포함된 초안 프로젝트 계약이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="48001-110">종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="48001-111">프로젝트 견적에서 생성된 프로젝트 계약은 Project Operations의 프로젝트 관리 및 회계 모듈에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48001-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="48001-112">프로젝트 계약이 해당 라인의 프로젝트에 매핑되지 않은 경우 이 프로젝트 계약은 비활성 프로젝트 계약으로 제공되며 프로젝트가 적어도 하나의 계약 라인에 매핑되는 즉시 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="48001-113">견적이 영업 기회에 첨부된 경우 영업 기회에 대한 다른 프로젝트 견적은 자동으로 실패로 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="48001-114">성공으로 견적 종료의 재정적 영향</span><span class="sxs-lookup"><span data-stu-id="48001-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="48001-115">초안 견적에 첨부되어 있는 동안 프로젝트에 기록된 시간에 대한 실제 값이 있는 경우 시간 또는 경비의 비용만 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="48001-116">견적이 성공으로 종료된 후 응용 프로그램은 이전 실제 비용을 되돌리고 새로운 실제 비용을 다시 생성하여 비용을 리팩토링합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="48001-117">응용 프로그램은 연관된 프로젝트 계약 내용의 청구 방법을 기반으로 이러한 실제 비용을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="48001-118">실제 비용이 시간 및 재료 계약 내용을 참조하는 경우 시스템은 견적이 종료되고 프로젝트 계약이 생성될 때 해당 미 청구 판매 실적을 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="48001-119">실제 비용이 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 프로젝트 계약 고객에 대한 분할 청구 규칙에 따라 실제 비용 재처리를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="48001-120">재처리된 모든 실제 데이터는 프로젝트 관리 및 회계 모듈에서 프로젝트 회계사가 검토, 업데이트 및 총계정 원장에 전기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48001-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="48001-121">견적을 실패로 종료</span><span class="sxs-lookup"><span data-stu-id="48001-121">Close a quote as Lost</span></span>

<span data-ttu-id="48001-122">프로젝트 견적을 실패로 종료하면 상태가 **종료됨** 으로 설정되고 상태 설명은 **실패** 로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="48001-123">견적을 종료하면 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="48001-124">종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="48001-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="48001-125">실패로 종료된 프로젝트 견적에 해당 라인에서 참조된 프로젝트가 있는 경우 해당 프로젝트도 종료됨으로 표시되고 해당 날짜 이후의 모든 리소스 예약이 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="48001-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="48001-126">Project Operations에서 견적을 성공 또는 실패로 종료해도 영업 기회의 해당 상태에 영향을 주지 않으며 수동으로 종료할 때까지 계속 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48001-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
