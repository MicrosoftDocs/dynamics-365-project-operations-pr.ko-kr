---
title: 경비 보고서의 개인 경비
description: 이 항목에서는 Microsoft Dynamics 365 Finance에서 작업자의 개인 경비를 처리하는 두 가지 방법을 설명합니다.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6b9d4fa0f69b4b0fe4bd1786958d22e5580a321
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960885"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="56844-103">경비 보고서의 개인 경비</span><span class="sxs-lookup"><span data-stu-id="56844-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="56844-104">여행 중에 작업자는 때때로 회사 신용 카드로 개인 경비를 청구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56844-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="56844-105">개인 경비 처리 프로세스를 정의하지 않으면 작업자가 항목별 경비 보고서를 제출할 때 경비 보고서에 대한 승인 프로세스가 중단될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56844-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="56844-106">작업자의 개인 경비를 처리하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56844-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="56844-107">**직원이 지불** – 조직이 기업 신용 카드 청구서에 표시된 개인 경비를 지불하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56844-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="56844-108">대신 회사 신용 카드로 청구된 회사 경비와 함께 개인 경비를 보여주는 보고서를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="56844-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="56844-109">**회사에서 지불** – 조직이 회사 신용 카드에 대한 전체 청구서를 지불한 다음 개인 경비로 작업자의 계좌에서 인출합니다.</span><span class="sxs-lookup"><span data-stu-id="56844-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="56844-110">**경비 관리 매개 변수** 페이지에서 조직에서 사용하는 방법을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56844-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
