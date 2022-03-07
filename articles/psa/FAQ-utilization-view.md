---
title: 청구 가능한 리소스 활용도 보기
description: 이 항목은 리소스 활용도 보기에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32dba5acd95c1d192556153240ebd51343112be53aa3db93e5e6f127c2d960e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007154"
---
# <a name="view-chargeable-utilization-for-resources"></a>청구 가능한 리소스 활용도 보기

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Project Service 리소스 활용도** 페이지의 **활용도 보기** 는 예약 가능한 각 리소스에 대한 청구 가능한 활용도를 표시합니다. 보기는 스케줄 게시판에 근거하므로 같은 기능 대부분을 찾을 수 있습니다.

> ![사용률 보기의 스크린샷.](media/FAQ-utilization-1.png)
 

청구 가능한 사용률 계산은 다음과 같이 작동합니다.

   청구 가능한 활용도 = (청구 가능한 실제값 시간) / (리소스 능력)

셀은 선택한 기간(일, 주 또는 월) 동안의 계산된 청구 가능한 활용도를 나타냅니다.

각 셀의 색은 대상의 사용 가능한 사용률과 비교한 리소스에 대한 청구 가능한 사용률을 보여줍니다. 

목표 활용도를 기본 역할 또는 개별 리소스 자체에서 설정할 수 있습니다. 계산은 먼저 대상의 개인을 찾은 다음 리소스의 기본 역할을 찾습니다.

## <a name="set-target-on-a-resource"></a>리소스에 대한 목표 설정

1. **리소스** \> **리소스** 로 이동합니다. 
2. 리소스를 선택하여 레코드를 엽니다. 
3. **Project Service** 탭에서 리소스의 목표 활용도를 설정할 수 있습니다.

> ![Project Service 탭을 사용하여 대상 사용률을 설정하는 스크린샷.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>역할에 대한 목표 활용도 설정

1. **리소스** \> **리소스 역할** 로 이동합니다. 
2. 역할을 선택하여 레코드를 엽니다. 
3. 역할에 대한 대상 사용률을 설정합니다.

> ![리소스 역할을 사용하여 대상 사용률을 설정하는 스크린샷.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>리소스에 대한 청구 가능한 활용도 계산

리소스에 대한 청구 가능한 활용도를 계산하려면 일부 전제조건을 완료해야 합니다. 

### <a name="set-default-role-for-individual-resource"></a>개별 리소스에 대한 기본 역할 설정

먼저, 개별 리소스에 대한 또는 리소스 역할에 대한 목표 활용도를 설정해야 합니다. 대상에 대한 리소스 역할을 사용하는 경우 각 개별 리소스에 기본 역할이 있어야 합니다. 

1. 이를 설정하려면 **리소스** \> **리소스** 로 이동합니다. 
2. 리소스를 선택하고 레코드를 연 다음 **Project Service** 탭을 선택합니다. 
3. **리소스** 역할 그리드에서 리소스에 대한 역할이 하나 있고 **기본값임** 이 **예** 로 설정되어 있는지 확인합니다.
 
### <a name="change-billing-type-for-resource-role"></a>리소스 역할을 위한 대금 청구 타입 변경

리소스 역할은 청구 타입이 **청구 가능** 으로 설정되어 있어야 합니다. 

1. **리소스** \> **리소스 역할** 로 이동합니다. 
2. 업데이트하려는 레코드를 연 다음 청구 타입 기본값을 **청구 가능** 으로 설정합니다.

### <a name="set-working-hours-for-resource-role"></a>리소스 역할을 위한 작업 시간 설정
 
리소스에는 생산 능력 계산을 위한 작업 시간이 있어야 합니다. 

1. **리소스** \> **리소스** 로 이동합니다. 
2. 리소스를 선택하여 레코드를 연 다음 **작업 시간 표시** 를 선택합니다. 
3. **리소스 목록** 보기에서 **작업 시간 템플릿** 을 적용함으로써 리소스 목록을 대량 업데이트할 수 있습니다.

## <a name="troubleshooting-chargeable-actual-hours"></a>청구 가능한 실제값 시간 문제 해결

청구 가능한 실제값 시간은 **실제값** 엔터티에서 구합니다. 청구 타입이 **청구 가능** 인 실제값이 계산에 포함되며 이러한 이유로 청구 가능한 실제값이 있는 프로젝트가 있어야 합니다.

청구 가능한 사용률이 표시되지 않는 경우 다음을 확인할 수 있습니다.

- 리소스에는 생산 능력에 대한 근무 시간이 정의되었습니다.
- 리소스에 개별적으로 정의된 사용률 대상이 있거나 기본 역할이 할당되어 있습니다. 역할에 대해 정의된 사용률 대상이 있습니다.
- 실제값은 활용도 계산을 예상하는 기간에 대해 **청구 가능** 인 청구 타입을 갖습니다. 청구 가능 이외의 청구 타입을 갖는 실제값이 보이는 경우 다음을 체크하십시오:

  - 실제에 사용되는 역할에는 청구 가능 이외의 기본 청구 유형이 있습니다.
  - 프로젝트를 백업하는 프로젝트 계약 내용에 대한 역할이 청구 가능 아님으로 설정되었습니다.
  - 프로젝트에 연결된 계약 라인이 없습니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]