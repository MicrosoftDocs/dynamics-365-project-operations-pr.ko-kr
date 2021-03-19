---
title: 견적 닫기 - 라이트
description: 이 항목은 Project Operations의 견적 종료에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272287"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="3672c-103">견적 닫기 - 라이트</span><span class="sxs-lookup"><span data-stu-id="3672c-103">Close a quote - lite</span></span>

<span data-ttu-id="3672c-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="3672c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3672c-105">프로젝트 견적은 성공 또는 실패로 마감될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="3672c-106">견적에 대한 활성화 및 수정 작업이 Microsoft Dynamics 365 Project Operations에서 지원되지 않기 때문에 초안 견적을 마감할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="3672c-107">견적을 성공으로 종료</span><span class="sxs-lookup"><span data-stu-id="3672c-107">Close a quote as Won</span></span>

<span data-ttu-id="3672c-108">프로젝트 견적을 성공으로 마감하면 상태는 마감으로 설정되고 상태 설명은 성공이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="3672c-109">견적을 종료하면 프로젝트 견적이 읽기 전용이 되고 견적 정보가 포함된 프로젝트 계약 초안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="3672c-110">마감된 견적은 다시 열 수 없기 때문에 확인 대화 상자에서 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3672c-111">견적이 영업 기회에 첨부된 경우 영업 기회에 대한 다른 프로젝트 견적은 자동으로 실패로 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="3672c-112">성공으로 견적 종료의 재정적 영향</span><span class="sxs-lookup"><span data-stu-id="3672c-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="3672c-113">초안 견적에 첨부되어 있는 동안 프로젝트의 시간에 대한 실제가 있는 경우 시간 또는 경비의 비용만 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="3672c-114">견적이 성공으로 종료된 후 응용 프로그램은 이전 실제 비용을 되돌리고 새로운 실제 비용을 다시 생성하여 비용을 리팩토링합니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="3672c-115">응용 프로그램은 연관된 프로젝트 계약 내용의 청구 방법을 기반으로 이러한 실제 비용을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="3672c-116">실제 원가가 시간 및 재료 계약 내용을 참조하는 경우 견적이 마감되고 프로젝트 계약이 생성될 때 해당 미청구 판매 실제가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="3672c-117">실제 원가가 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 프로젝트 계약 고객에 대한 분할 청구 규칙을 기반으로 하는 실제 원가 재처리를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="3672c-118">견적을 실패로 종료:</span><span class="sxs-lookup"><span data-stu-id="3672c-118">Closing a quote as lost:</span></span>

<span data-ttu-id="3672c-119">프로젝트 견적을 실패로 마감하면 상태는 마감으로 설정되고 상태 설명은 실패가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="3672c-120">견적을 종료하면 프로젝트 견적이 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="3672c-121">종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3672c-122">실패로 마감된 프로젝트 견적이 해당 라인의 프로젝트를 참조하는 경우 해당 프로젝트도 마감됨으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="3672c-123">그 날 이후의 모든 리소스 예약은 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="3672c-124">Project Operations에서 견적을 성공 또는 실패로 종료해도 영업 기회의 해당 상태에 영향을 주지 않으며 수동으로 종료할 때까지 계속 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3672c-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]