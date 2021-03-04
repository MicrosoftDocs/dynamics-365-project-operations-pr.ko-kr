---
title: 여행 요청
description: 이 항목은 여행 요청에 대한 정보를 제공합니다.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123746"
---
# <a name="travel-requisitions"></a>여행 요청

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

여행 요청은 여행 목적으로 발생할 경비를 나열합니다. 검토를 위해 여행 요청을 제출하고 경비를 승인하는 데 사용할 수 있습니다.

조직에 청구되는 경비가 발생하기 전에 여행 요청을 제출해야 할 수 있습니다. 이 요구 사항은 회사 신용 카드로 경비를 청구하든, 현금 서비스로 받은 현금을 사용하든, 조직에서 상환할 본인 부담 비용이 발생하든 관계없이 적용됩니다.

여행 요청 및 정책을 사용하여 조직 지출을 관리할 수 있습니다. 예를 들어 조직에서 출장이 필요한 고정 가격 프로젝트를 진행하는 경우 프로젝트 팀 구성원의 출장 경비가 프로젝트 예산에 맞아야 합니다. 출장 경비가 발생하기 전에 승인되도록 요청함으로써 조직은 프로젝트가 예산 내에서 유지되도록 할 수 있습니다.

## <a name="configuration"></a>구성 

경비 관리 매개 변수에서 "여행 사전 승인은 필수" 매개 변수를 활성화하여 여행 요청을 "필수"로 구성할 수 있습니다. 

## <a name="create-and-submit-a-travel-requisition"></a>여행 요청 작성 및 제출

1. **내 경비: 여행 요청** 으로 이동하고 **새로운 여행 요청** 을 선택합니다.
2. 요청의 목적과 목적지를 입력합니다.
3. **여행 설명** 필드에 추가 정보를 입력합니다. 
4. 비행, 식사 또는 렌터카와 같은 예상 경비 각각에 대해 경비 라인 항목을 만듭니다. 각 경비의 예상 날짜, 예상 금액 및 통화를 포함합니다. 
5. 예상 경비 추가를 마쳤으면 **저장** 을 선택합니다.
6. 여행 요청을 제출할 준비가되면 **워크플로** > **제출** 을 선택합니다.

승인된 여행 요청은 **내 경비: 여행 요청** 에서 볼 수 있습니다. 

## <a name="view-available-travel-requisitions"></a>사용 가능한 여행 요청 보기

모든 여행 요청은 **내 경비: 여행 요청** 에서 볼 수 있습니다.

## <a name="approve-travel-requisitions"></a>여행 요청 승인

승인할 여행 요청을 선택한 다음 **워크플로** > **승인** 을 선택합니다.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>승인된 여행 요청을 사용하여 경비 보고서를 제출합니다.

1. 새 경비 보고서를 작성하고 경비 보고서 헤더에서 승인된 여행 요청 목록에서 **여행 요청에 매핑** 을 선택합니다.
2. **여행 요청 금액** 필드는 경비 보고서 헤더에서 자동으로 업데이트됩니다.
3. 여행에 발생한 각 경비를 추가합니다. **사전 승인** 필드가 활성화되면 조정된 금액과 특정 경비 범주에 대한 승인된 금액이 업데이트됩니다.

> [!NOTE]
> 경비 보고서를 승인된 여행 요청에 매핑할 때 트랜잭션 금액은 승인된 금액보다 클 수 없습니다. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]