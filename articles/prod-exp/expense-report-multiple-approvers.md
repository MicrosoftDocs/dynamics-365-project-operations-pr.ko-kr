---
title: 경비 보고서에 대한 여러 승인자
description: 이 항목은 여러 사람의 승인이 필요한 경비 보고서에 대한 정보를 제공합니다.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960615"
---
# <a name="multiple-approvers-on-an-expense-report"></a>경비 보고서에 대한 여러 승인자

조직의 경비 승인 정책에 따라 두 명 이상의 사람이 직원이 제출한 경비 보고서를 승인해야 할 수 있습니다. 경비 보고서 승인을 위한 워크플로 프로세스를 설정할 때 하나 이상의 경비 보고서 승인자에 대한 작업 또는 단계를 포함하는 워크플로 요소를 추가할 수 있습니다. 예를 들어, 모든 경비 보고서는 보고서를 제출한 직원의 관리자가 먼저 승인한 다음 채무 코디네이터가 승인하도록 요구할 수 있습니다.

여러 경비 보고서 승인자를 요구하기로 결정한 경우 다음 방법 중 하나로 워크플로 요소를 추가할 수 있습니다.

- 한 단계가 있는 하나의 승인 요소를 추가합니다. 예를 들어 이 단계에서는 경비 보고서를 사용자 그룹에 할당하고 사용자 그룹 구성원의 50 %가 이를 승인해야 할 수 있습니다.
- 여러 단계가 있는 하나의 승인 요소를 추가합니다. 예를 들어 승인 요소에는 다음 단계가 있을 수 있습니다.

    1. 경비 보고서를 제출한 직원의 관리자가 승인합니다.
    2. 미지급금 사무원은 영수증 및 경비 보고서 항목을 확인합니다.
    3. 예산 소유자가 경비 보고서를 승인합니다.

- 각각 하나의 단계가 있는 여러 승인 요소를 추가합니다. 예를 들어 다음 각 단계에 대해 별도의 승인 요소를 추가할 수 있습니다.

    1. 직원의 관리자가 경비 보고서를 승인합니다.
    2. 예산 소유자가 경비 보고서를 승인합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]