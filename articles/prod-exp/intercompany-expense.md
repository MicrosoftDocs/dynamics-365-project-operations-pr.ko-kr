---
title: 회사 간 경비
description: 조직의 한 법인에 고용된 근로자는 동일한 조직의 다른 법인을 위해 작업을 수행할 수 있습니다. 이 상황에서 회사 간 경비 기능을 사용하여 작업자 경비를 작업이 수행된 법인에 할당할 수 있습니다.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080203"
---
# <a name="intercompany-expenses"></a>회사 간 경비

[!include [banner](../includes/banner.md)]

조직의 한 법인에 고용된 근로자는 동일한 조직의 다른 법인을 위해 작업을 수행할 수 있습니다. 이 상황에서 회사 간 경비 기능을 사용하여 작업자 경비를 작업이 수행된 법인에 할당할 수 있습니다. 근로자를 고용하는 법인을 대출 법인이라고 합니다. 근로자에게 비용이 발생하는 법인을 차용 법인이라고 합니다. 

근로자가 다른 법인을 위해 수행된 작업에 대한 경비를 생성하고 제출하기 전에 대출 법인의 **경비 관리 매개 변수** 페이지에서 **회사간 경비 라인 허용** 옵션을 선택합니다. 

## <a name="tax-posting-for-intercompany-expenses"></a>회사간 경비에 대한 세금 전기

[!include [banner](../includes/banner.md)]

경비 보고서에서 차용(대상) 법인 대신 대출(원본) 법인과 연관된 세금 그룹을 사용하려면 총계정 원장 판매세 설정에서 이를 구성해야 합니다. 총계정 원장 매개 변수, **회사간 세금 전기를 위한 법인** 이 **원본** 으로 설정되고 **판매세 과세 규칙 적용** 이 **아니요** 로 설정되면 대출 법인의 세금 조합이 사용됩니다. 동일한 매개 변수가 **대상** 으로 설정된 경우 차용 법인에 대한 세금 조합이 사용됩니다. 미국 법인의 경우 매개 변수가 **원본** 으로 설정되면 **받을 판매세** 필드도 새 **원장 전기 그룹** 페이지에서 구성해야 합니다. 회계 엔진은 이 필드의 정보를 세금 관련 회계 입력에 사용합니다.   
이 동작은 프로젝트 유무에 관계없이 전기된 경비 라인에 대해 일관됩니다.  
