---
title: Project Service Automation 업데이트 릴리스 16, V3의 새로운 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 16, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753272"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation V3, 업데이트 릴리스 16
Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다.

이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)를 참조하세요. 이 항목에는 PSA V3, 업데이트 릴리스 16에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.6.34이며 2020년 1월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-16"></a>업데이트 릴리스 16

### <a name="bug-fixes"></a>버그 수정

-   시간 및 경비

    -   해결: 승인을 위해 삭제된 시간 및 경비 항목을 제출하려는 사용자는 이제 관련 오류 메시지를 받습니다.

-   프로젝트 관리

    -   해결: 템플릿에서 팀 구성원에 대해 정의된 리포지토리 단위는 템플릿이 새 프로젝트에 적용되는 것을 존중합니다.

    -   해결: 레코드 소유권 재할당 처리 기능이 개선되었습니다.

    -   해결: 복사가 진행 중인 프로젝트는 모든 복사 작업이 완료될 때까지 복사할 수 없습니다.

-   리소스 관리

    -   해결: 예약 확장이 이제 짧은 지속 시간을 올바르게 처리하고 더 이상 확장 예약에 대해 0시간을 만들지 않습니다.

    -   해결: 이제 프로젝트 시간대가 +5:30 GMT이고 사용자의 시간이 다를 때 조정 보기가 렌더링됩니다.

-   Sales

    -   해결: 계약 라인에 매핑된 프로젝트가 제거되고 새 프로젝트가 매핑될 때 계약 라인에 정의된 대금 청구 및 가격 규칙에 따라 새 프로젝트의 실제 레코드가 재평가되지 않았습니다. 이 릴리스에서 수정되었습니다. 새로 매핑된 프로젝트의 가격 및 실제 레코드는 계약 라인의 가격 및 청구 규칙에 따라 올바르게 되돌려지고 다시 작성됩니다. 매핑되지 않은 프로젝트의 실제 레코드도 결과적으로 다시 평가되고 다시 만들어집니다.

    -   해결: null 값이 유지되지 않도록 추가 유효성 검사가 견적 라인의 **금액** 필드에 추가되었습니다.

    -   해결: 프로젝트에서 실제가 업데이트되면 사용자가 실제를 다시 동기화할 수 있도록 프로젝트 기본 양식에 새로 고침 단추가 추가되었습니다.

    -   해결: 사용자가 2.X에서 3.X로 업그레이드할 때 프로젝트 이름에 NULL 값을 가진 프로젝트가 허용됩니다.

