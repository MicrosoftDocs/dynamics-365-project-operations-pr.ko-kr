---
title: 가격 책정 차원으로 예약 가능한 리소스 사용
description: 이 항목은 예약 가능한 리소스를 가격 책정 차원으로 사용하는 것에 대한 정보를 제공합니다.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290952"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>가격 책정 차원으로 예약 가능한 리소스 사용

[!include [banner](../includes/psa-now-project-operations.md)]

이 항목은 예약 가능한 리소스를 가격 책정 차원으로 사용하는 것에 대한 정보를 제공합니다. 시작하기 전에 가격 책정 차원 솔루션을 아직 만들지 않은 경우 새 솔루션을 만들어야 합니다. 가격 차원 솔루션이 이미 있는 경우 해당 솔루션을 변경할 수 있습니다. 조직에 대한 새 가격 책정 차원 솔루션을 만들지 않은 경우 [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities.md) 항목의 절차를 완료하십시오.

## <a name="add-bookable-resource-to-forms-and-views"></a>양식 및 보기에 예약 가능한 리소스 추가
가격 책정 차원 솔루션의 UI에 필드를 표시하려면 주요 Project Service 엔터티의 모든 양식 및 보기를 살펴보고 이러한 필드를 해당 엔터티의 양식 및 보기에 추가해야 합니다.
다음 표는 엔터티별로 나열된 즉시 중단 양식 및 보기의 포괄적인 목록으로서 향후에 업데이트할 필요가 있습니다. 이러한 엔터티의 맞춤화에 추가 보기 또는 양식이 있는 경우 해당 엔터티에 새 필드도 추가하십시오.
가격 차원 솔루션에 대한 솔루션 탐색기를 연 다음 **모든 맞춤화 게시** 를 클릭합니다.


|   엔터티        | 양식   |Views        |
| ------------------------------|---------------------------------|----------------------------------|
|  역할 가격|• 정보 |• 활성 리소스 카테고리 가격<br> • 리소스 카테고리 가격 연계 보기|
|  역할 가격 인상|• 정보|• 활성 역할 가격 인상<br>• 역할 가격 인상 연계 보기|
|  견적 행 내역|• 프로젝트 정보<br>• 프로젝트 빨리 만들기|• 활성 견적 행 내역<br>• 조합된 견적 행 내역<br>• 견적 행 내역 연계 보기|
|  프로젝트 계약 행 내역|• 프로젝트 정보<br>• 프로젝트 빨리 만들기|• 조합된 계약 행 내역<br>• 활성 계약 행 내역<br>• 계약 행 내역 연계 보기|
|  프로젝트 작업|• 정보<br>• 새 양식||
|  프로젝트 팀 구성원|• 정보<br>• 새 양식|• 활성 프로젝트 팀원<br>• 프로젝트 팀원<br>• 프로젝트 팀원 연계 보기|
|  시간 항목|• 정보<br>• 시간 항목 만들기|• 날짜별 내 시간 항목<br>• 금주의 내 시간 항목<br>• 승인을 위한 시간 항목|
|  분개장 항목|• 정보<br>• 빨리 만들기|• 활성 분개장 행<br>• 분개장 행 연계 보기|
|  송장 라인 세부 정보|• 정보<br>• 빨리 만들기|• 활성 청구서 행 내역<br>• 청구 가능 청구서 처리<br>• 무료 청구서 처리<br>• 청구서 행 내역 연계 보기<br>• 청구 불가능한 청구서 처리|
|  실제|• 정보<br>• 활성 실제값|• 실제값 연계 보기|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>가격 책정 차원으로 예약 가능한 리소스 설정

1. 웹 인터페이스에서 **Project Service** > **설정** > **파라미터** 로 이동합니다. **파라미터** 페이지의 **금액 기반 가격 책정 차원** 탭에서 탭의 그리드가 가격 책정 차원 엔터티의 레코드를 보여줌을 인식하십시오. 
2. **예약 가능한 리소스** 를 이 가격 책정 차원 목록에 **msdyn_bookableresource** 로 추가합니다. 
3. 예약 가능한 리소스가 가격 책정 차원으로 기능하는 상황을 표시하고 **원가에 적용** 및 **매출액에 적용** 값을 설정합니다.
4. **차원 타입** 필드에서 **금액 기반** 을 선택합니다. 
5. 예약 가능한 리소스의 원가 및 매출액 우선 순위를 선택합니다. 일반적으로, 가격 책정 차원으로 포함된 경우 예약 가능한 리소스의 우선 순위가 가장 높으므로 이를 **1**(또는 우선 순위를 계수하는 방법에 따라 **0**)로 설정하면 해당 특성이 보장됩니다.

## <a name="set-up-pricing-dimension-field-names"></a>가격 책정 차원 필드 명칭 설정

**역할 가격** 표에서 가격 책정 차원의 필드 명칭이 가격 기본값이 작동해야 하는 다른 엔터티의 필드 명칭과 다른 경우 가격 책정 차원 레코드는 그 다른 이름을 인식하도록 만들어야 합니다.    
예약 가능한 리소스의 경우, **프로젝트 팀원** 엔터티는 **역할 가격** 엔터티에서 불리는 명칭 (**msdyn_bookableresource**)과 약간 다른 필드 명칭(**msdyn_bookableresourceid**)을 갖습니다. **msydn_bookableresource** 를 위한 가격 책정 차원 레코드가 이를 인식하도록 만들어야 합니다. 
1. 이렇게 하려면 **가격 책정 차원** 그리드의 행을 더블클릭하여 **msdyn_bookableresource** 의 차원 페이지를 여십시오.
2. 차원 페이지의 **관련** 탭에서 **가격 책정 차원 필드 명칭** 을 클릭합니다.

 ![가격 책정 차원 필드 명칭 탭](media/PD-fieldname.png)

4. 열리는 연계된 보기에서 **새 가격 책정 차원 필드 명칭 추가** 를 클릭합니다.

 ![새 가격 책정 차원 필드 명칭 추가](media/Add-NewPD-fieldname.png)


그러면 **msdyn_bookableresource** 를 위한 **새 가격 책정 차원 필드 명칭** 페이지가 열립니다. 

5. **msdyn_projectteam** 을 **엔터티 논리 명칭** 필드에 추가하고 **msdyn_bookableresourceid** 를 **필드 명칭** 필드에 추가합니다. 레코드를 저장합니다.

 ![새 가격 책정 차원 필드 명칭 양식](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]