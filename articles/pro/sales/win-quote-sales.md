---
title: 견적 닫기 - 라이트
description: 이 항목은 Project Operations의 견적 종료에 대한 정보를 제공합니다.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175719"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="29302-103">견적 닫기 - 라이트</span><span class="sxs-lookup"><span data-stu-id="29302-103">Close a quote - lite</span></span>

<span data-ttu-id="29302-104">_**적용 대상:** 라이트 배포 - 견적 송장 거래_</span><span class="sxs-lookup"><span data-stu-id="29302-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29302-105">프로젝트 견적은 성공 또는 실패로 마감될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29302-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="29302-106">견적에 대한 활성화 및 수정 작업은 Microsoft Dynamics 365 Project Operations에서 지원되지 않으므로 초안 견적을 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29302-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="29302-107">견적을 성공으로 종료</span><span class="sxs-lookup"><span data-stu-id="29302-107">Close a quote as Won</span></span>

<span data-ttu-id="29302-108">프로젝트 견적을 성공으로 종료하면 상태가 종료됨으로 설정되고 상태 설명이 성공으로 설정된 견적이 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="29302-109">견적을 종료하면 프로젝트 견적이 읽기 전용이 되고 견적 정보가 포함된 프로젝트 계약 초안이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="29302-110">종료된 견적은 확인 대화 상자를 다시 열 수 없습니다. 종료된 견적을 다시 열 수 없고 변경 사항을 되돌릴 수 없기 때문에 변경이 완료되기 전에 확인 대화 상자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29302-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="29302-111">견적이 영업 기회에 첨부된 경우 영업 기회에 대한 다른 프로젝트 견적은 자동으로 실패로 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="29302-112">성공으로 견적 종료의 재정적 영향</span><span class="sxs-lookup"><span data-stu-id="29302-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="29302-113">초안 견적에 첨부되어 있는 동안 프로젝트에 기록된 시간에 대한 실제 값이 있는 경우 시간 또는 경비의 비용만 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="29302-114">견적이 성공으로 종료된 후 응용 프로그램은 이전 실제 비용을 되돌리고 새로운 실제 비용을 다시 생성하여 비용을 리팩토링합니다.</span><span class="sxs-lookup"><span data-stu-id="29302-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="29302-115">응용 프로그램은 연관된 프로젝트 계약 내용의 청구 방법을 기반으로 이러한 실제 비용을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="29302-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="29302-116">실제 비용이 시간 및 재료 계약 내용을 참조하는 경우 시스템은 견적이 종료되고 프로젝트 계약이 생성될 때 해당 미 청구 판매 실적을 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="29302-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="29302-117">실제 비용이 고정 가격 계약 내용을 참조하는 경우 응용 프로그램은 프로젝트 계약 고객에 대한 분할 청구 규칙에 따라 실제 비용 재처리를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="29302-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="29302-118">견적을 실패로 종료:</span><span class="sxs-lookup"><span data-stu-id="29302-118">Closing a quote as lost:</span></span>

<span data-ttu-id="29302-119">프로젝트 견적을 실패로 종료하면 상태가 종료됨으로 설정되고 상태 설명은 실패로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="29302-120">견적을 종료하면 프로젝트 견적이 읽기 전용이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="29302-121">종료된 견적은 다시 열 수 없으므로 견적을 종료하기 전에 확인 대화 상자에서 변경 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="29302-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="29302-122">실패로 종료된 프로젝트 견적에 해당 라인에서 참조된 프로젝트가 있는 경우 해당 프로젝트도 종료됨으로 표시되고 해당 날짜 이후의 모든 리소스 예약이 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="29302-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="29302-123">Project Operations에서 견적을 성공 또는 실패로 종료해도 영업 기회의 해당 상태에 영향을 주지 않으며 수동으로 종료할 때까지 계속 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29302-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
