---
title: 내부 프로젝트에 대한 회계 구성
description: 이 항목은 Project Operations의 내부 프로젝트에 대한 회계 절차를 설정하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012864"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="0d17d-103">내부 프로젝트에 대한 회계 구성</span><span class="sxs-lookup"><span data-stu-id="0d17d-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="0d17d-104">_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0d17d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d17d-105">내부 프로젝트를 통해 회사는 고객에게 청구되지 않는 활동과 관련된 비용을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="0d17d-106">내부 프로젝트의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="0d17d-107">모바일 앱과 같은 제품을 개발하고 개발과 관련된 비용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="0d17d-108">사전 판매 시간 및 비용 관리.</span><span class="sxs-lookup"><span data-stu-id="0d17d-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="0d17d-109">이 사전 판매 내부 프로젝트는 견적이 성사되면 나중에 청구 가능한 프로젝트로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="0d17d-110">Dynamics 365 Project Operations에서 계약과 연관되지 않은 모든 프로젝트는 내부로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="0d17d-111">프로젝트 비용 및 수익 프로필은 프로젝트에 대한 회계 규칙을 결정하는 데 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="0d17d-112">내부 프로젝트 비용은 항상 손익 원칙을 사용하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="0d17d-113">전기를 위한 원장 계정은 **원장 전기 설정** 페이지에서 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="0d17d-114">시간 트랜잭션은 **비용** 계정을 차변 처리하고 **급여 할당** 계정을 대변 처리하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="0d17d-115">경비 트랜잭션은 **비용** 계정을 차변 처리하고 **경비에 대한 상쇄 계정** 계정을 대변 처리하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="0d17d-116">항목 트랜잭션은 **비용** 계정에서 출금하고 **비용 - 품목** 계정에 입금하여 전기됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="0d17d-117">트랜잭션이 프로젝트에 전기된 후 프로젝트가 프로젝트 계약과 연관된 경우 시스템은 누적된 모든 트랜잭션을 취소하고 새로운 청구 가능 트랜잭션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="0d17d-118">청구 가능 트랜잭션은 각 프로젝트 비용 및 수익 프로필에 정의된 회계 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0d17d-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
