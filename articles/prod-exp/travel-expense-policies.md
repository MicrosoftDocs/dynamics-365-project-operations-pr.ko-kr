---
title: 경비 정책 설정
description: 작업자가 Microsoft Dynamics 365 Finance에서 경비 보고서 및 출장 요청을 입력하고 제출할 때 따라야 하는 경비 정책을 설정할 수 있습니다.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005754"
---
# <a name="set-up-expense-policies"></a>경비 정책 설정

작업자가 경비 보고서 및 출장 요청을 입력하고 제출할 때 따라야 하는 정책을 정의할 수 있습니다.         
경비 정책을 구현하면 경비를 효과적으로 관리할 수 있습니다.         

예를 들어 1박당 비용이 USD 250을 초과할 수 없음을 나타내는 뉴욕시의 호텔 경비에 대한 정책을 설정할 수 있습니다.       
작업자가 객실 요금이 이 금액을 초과하는 경비 보고서 또는 출장 요청을 제출하면 시스템은        
경비에 대한 정책 금액이 초과되었음을 작업자에게 알립니다. 정책을 정의할 때 작업자가 받을 메시지를 구성할 수        
있습니다.      
        
다음 세 가지 유형의 정책을 정의할 수 있습니다.         
        
- 경고 - 작업자가 경비 보고서 또는 출장 요청서를 제출할 수 있지만 경비는 모든 승인자와 나중에 보고할 수 있도록        
  표시됩니다.        

- 오류 - 경비 보고서 또는 출장 요청서를 제출하기 전에 근로자가 정책을 준수하기 위해 경비를 수정해야 합니다.       
 
 - 정당화 - 경비 보고서 또는 출장 요청서를 제출하기 전에 작업자 또는 관리자가 정책 금액 초과에 대한 사유를 입력해야 합니다.        

## <a name="policy-tips"></a>정책 팁
다음은 경비 관리를 위한 새 정책을 만들 때 도움이 될 수 있는 몇 가지 제안 사항입니다. 
* 정책은 유효 날짜이며 경비가 발생한 날짜 이후의 날짜로 정책을 생성하면 정책이 적용되지 않습니다. 예를 들어, $50의 최대 식사 비용을 적용하기 위해 오늘 새 정책을 생성하는 경우 어제 입력된 기존 비용에는 이 정책이 적용되지 않습니다.
* 항목별로 분류할 수 있는 경비 범주에 대한 정책을 생성할 때 경비 항목 유형에 대한 조건을 추가하는 것이 좋습니다. 영수증을 요구하는 것과 같은 일부 정책은 항목별 라인에 적합하지 않을 수 있으며 헤더 라인 또는 항목화되지 않은 라인에만 적용되어야합니다. 
* 경비 관리 정책은 기본적으로 소스 엔터티에 대해 평가됩니다. 내부 거래 시나리오의 경우 대신 대상 엔터티(차용 엔터티)에 대해 평가되도록 정책을 설정할 수 있습니다. 대상 엔터티에 대해 정책을 실행하려면 **기능 관리** 작업 영역의 "차입 법인에 대한 경비 정책 평가" 기능을 켭니다.

## <a name="when-to-evaluate-policies"></a>정책 평가 시기

경비 관리 매개 변수에서 라인이 저장되거나 경비 보고서가 실행될 때 경비 관리 정책을 평가하는 옵션이 있습니다. 라인이 저장되는 시기를 평가하도록 선택하면 사용자는 경비 보고서를 한 번에 완료하기 위해 수행해야 하는 작업을 미리 파악할 수 있습니다. 그렇지 않으면 워크플로에 제출하는 동안 마지막에 유효성을 검사가 발생하는 경우 정책 평가를 지연하고 시간을 절약할 수 있습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]