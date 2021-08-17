---
title: Project Service Automation 업데이트 릴리스 17, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 17, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: ba2bc9da1c6e7e2e2628980878f9201b1c732cc03f791f5259bbbd0ee279b31b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006614"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation 업데이트 릴리스 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.  이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 PSA V3, 업데이트 릴리스 17에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.6.34이며 2020년 3월에 자체 업데이트를 통해 일반적으로 제공됩니다.


## <a name="update-release-17"></a>업데이트 릴리스 17

### <a name="bug-fixes"></a>버그 수정

**일반**

- 해결: Team Member 라이선스를 시행하도록 Project Service Automation를 업데이트합니다(프로젝트 리소스 허브에는 팀 구성원 서비스 계획 메타데이터 3.x가 포함됨).
 
**시간 및 경비**

- 해결: 경비 견적을 0이 아닌 가격에서 0으로 변경할 수 없습니다. 변경은 무시됩니다.

**프로젝트 관리**

- 해결: 팀 구성원의 직위 이름에 null 값 검사가 추가되었습니다.
- 해결: **msdyn_resourceassignment** 엔터티의 **msdyn_userresourceid** 필드는 더 이상 사용되지 않습니다.
- 해결: 2.x에서 3.x로 업그레이드하면 작업 할당에서 빈 작업량 등고선을 처리합니다.

**Sales**

- 해결: **Invoice.PreValidateInvoiceUpdate** 는 이제 레코드 소유자를 올바르게 재할당하는 시나리오를 처리합니다.
- 해결: 트랜잭션 클래스가 **시간** 이면 **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** 및 **ContractLineDetails** 를 포함하여 모든 엔터티에 대해 **UnitGroup** 을 편집할 수 없습니다.. 그러나 **단위** 는 **JournalLine** 과 **InvoiceLineDetails** 의 경우에만 편집할 수 없습니다 .




[!INCLUDE[footer-include](../includes/footer-banner.md)]