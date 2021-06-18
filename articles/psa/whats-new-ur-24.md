---
title: Project Service Automation 업데이트 릴리스 24, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 24, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000264"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation 업데이트 릴리스 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 24에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V 3.10.42.43이며 2020년 10월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-24"></a>업데이트 릴리스 24

### <a name="bug-fixes"></a>버그 수정

**Sales**

다음과 같은 문제가 해결되었습니다.

- 제품의 기본 가격 목록을 설정하는 동안 문제가 발생했습니다.
- 포함된 가격표 및 역할 가격 레코드 사본으로 인해 견적 받기의 성능이 느립니다.
- **프로젝트 계약/판매 허브** > **제품 라인 항목/주문 라인 수량** 은 가장 가까운 정수로 자동 반올림됩니다.
- 가격표를 읽을 때 시스템 권한으로 승격하십시오.
- 고객 주소 필드 **address1_freighttermscode** 및 **address1_shippingmethodcode** 를 견적/주문으로 복사합니다. 


**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- **시간 항목 그리드** 는 **날짜만** 시간 동작을 지원하지 않습니다.
- **시간 항목** 은 자동으로 새로 고침되지 않습니다. 수동 새로 고침이 필요합니다.
- 리소스 할당에 휴식(0 시간)이 있는 경우 할당에서 시간 항목을 가져올 수 없습니다.
- 시간 항목을 만들 때 시작을 **msdyn_date** 와 동일하게 설정합니다.
- 시간 항목에 대한 대량 편집을 다시 활성화합니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.

- 요구 사항 없이 당일 예약 상태를 업데이트하려고 하면 null-ref 예외가 발생합니다.
- **조정 보기** 로드 중 오류가 발생합니다.


**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- **프로젝트 일정** 에서 **수동** 에서 **자동** 으로 변경하면 자동 저장이 완료되지 않습니다.
- 경비 비용은 **프로젝트 추적 그리드** 의 차이로 계산해서는 안 됩니다.
- 로드 중 **추정 태그** 열의 일관되지 않은 동작과 **시간 위상** 유형 변경을 비교합니다.
- 프로젝트의 실제 비용은 **실제** 의 총액을 반영하지 않을 수 있습니다.
- **요약** 탭의 **예상 완료 날짜** 가 **WBS 일정** 과 일치하지 않습니다.
- 내어쓰기의 **실제 시간 업데이트** 가 제대로 작동하지 않습니다.
- 루트 **BU** 외부의 프로젝트 관리자가 프로젝트를 만들 수 없습니다.
- **경비 추정** 의 작업 또는 범주 변경이 지속되지 않습니다.
- **계약 사본** 이 송장 일정 및 실행 상태를 복사합니다.
- **실적 새로 고침** 단추가 요약 작업을 잘못 계산합니다.
- Microsoft Project 추가 기능: 팀 구성원이 빈 리소스 단위를 가진 경우 null 참조 오류를 수정합니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]