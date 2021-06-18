---
title: 가격표 비활성화
description: 이 항목은 미사용 또는 이전 가격표를 비활성화하거나 제거하는 방법을 설명합니다.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001344"
---
# <a name="deactivate-price-lists"></a>가격표 비활성화 

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations에서 이전 또는 사용되지 않는 가격표를 제거하려면, 완료해야 하는 두 단계가 있습니다. 

1. 특정 페이지에서 가격표를 제거하거나 삭제합니다.
2. **가격표** 페이지의 활성 가격 목록에서 가격표를 비활성화하거나 삭제합니다.

>[!IMPORTANT]
> 가격표를 완전히 제거하려면 두 단계를 모두 완료해야 합니다. 활성 가격표 보기에서 가격표를 직접 삭제하거나 비활성화하는 2단계만 수행하는 것만으로는 충분하지 않습니다. 또한 1 단계에서 언급한 모든 위치에서이 가격표의 연결을 삭제해야 합니다.

## <a name="delete-the-price-list-from-specific-pages"></a>특정 페이지에서 가격표를 삭제합니다.
1. Project Operations에서 가격표를 삭제하려면 다음 페이지로 이동하십시오.  

      - **프로젝트 매개 변수** 페이지 > **가격표** 탭
      - **조직 구성 단위** 페이지 >**가격표** 그리드
      - **거래처** 페이지 > **프로젝트 가격표** 그리드
      - **프로젝트 견적** 페이지 >**프로젝트 가격표** 그리드: 모든 활성 프로젝트 견적에 적용됩니다.
      - **프로젝트 계약** 페이지 >**프로젝트 가격표** 그리드: 모든 활성 프로젝트 계약에 적용됩니다.

 2. 각 페이지에 대해 삭제할 가격표를 선택한 다음 **삭제** 를 선택합니다. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>가격표 페이지에서 가격표 삭제 또는 비활성화
 
1. 활성 가격표에서 가격표를 삭제하려면 **판매** > **고객** > **가격표** 로 이동합니다. 
2. 삭제하려는 가격표룰 선택한 다음 **삭제** 를 선택합니다. 가격표가 기존 트랜잭션에서 참조되는 경우 삭제할 수 없습니다. 이 경우 가격표를 비활성화하여 보기에 표시되지 않도록 할 수 있습니다. 
3. 가격표를 비활성화하려면 가격표를 다시 선택한 다음 **비활성화** 를 선택합니다.   
