---
title: 회사 간 경비
description: 이 문서에서는 회사 간 경비를 사용하여 작업이 수행된 법인에 근로자 경비를 할당하는 방법에 대한 정보를 제공합니다.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932396"
---
# <a name="intercompany-expenses"></a>회사 간 경비

조직의 한 법인에 고용된 근로자는 동일한 조직의 다른 법인을 위해 작업을 수행할 수 있습니다. 회사 간 비용을 사용하여 작업자의 비용을 작업이 수행된 법인에 할당할 수 있습니다. 근로자를 고용하는 법인을 대출 법인이라고 합니다. 근로자에게 비용이 발생하는 법인을 차용 법인이라고 합니다. 

근로자가 회사 간 비용을 생성하고 실행하기 전에 회사 간 경비 라인을 활성화해야 합니다. 대출 법인의 **경비 관리 매개 변수** 페이지에서 **회사 간 경비 라인 허용** 을 선택합니다. 

## <a name="tax-posting-for-intercompany-expenses"></a>회사간 경비에 대한 세금 전기

[!include [banner](../includes/banner.md)]

경비 보고서에서 차용(대상) 법인 대신 대출(출처) 법인과 연관된 세금 그룹을 사용하려면 먼저 총계정 원장 판매세 설정에서 기능을 활성화해야 합니다. **회사 간 세금 전기를 위한 법인** 매개 변수가 **출처** 로 설정되고 **판매세 과세 규칙 적용** 이 **아니요** 로 설정된 경우 대출 법인에 대한 세금 조합이 사용됩니다. 동일한 매개 변수가 **대상** 으로 설정된 경우 차용 법인에 대한 세금 조합이 사용됩니다. 미국 법인의 경우 매개 변수가 **원본** 으로 설정되면 **받을 판매세** 필드도 새 **원장 전기 그룹** 페이지에서 구성해야 합니다. 회계 엔진은 이 필드의 정보를 세금 관련 회계 입력에 사용합니다.   
이 동작은 프로젝트 유무에 관계없이 전기된 경비 라인에 대해 일관됩니다.  

## <a name="new-expense-expression-builder"></a>새로운 경비 식 작성기

새로운 경비 식 작성기는 프로젝트를 사용하는 회사 간 경비 시나리오의 문제를 해결합니다. 이 기능을 사용하면 본지사 경비를 생성할 때 경비 라인에서 선택한 프로젝트에 대해 경비 정책이 올바르게 검증되고 경비 보고서가 성공적으로 제출될 수 있습니다.

경비 식 작성기 기능이 작동하려면 켜져 있어야 합니다. 또한 프로젝트 ID가 있는 경비 정책을 설정해야 합니다.

경비 라인에서 프로젝트 ID를 확인하는 정책을 이미 구성한 경우 해당 정책은 폐기되어야 합니다. 그런 다음 기능을 켜고 정책을 재구성할 수 있습니다.

이 기능을 켜려면 다음 단계를 따르십시오.

1. **작업 영역** \> **기능 관리** 로 이동합니다.
2. 목록에서 **프로젝트를 사용하는 회사 간 경비 시나리오의 문제를 해결하기 위한 새로운 경비 식 작성기** 를 선택합니다. 그런 다음 **지금 활성화** 를 선택합니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
