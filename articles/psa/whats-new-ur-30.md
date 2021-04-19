---
title: Project Service Automation 업데이트 릴리스 30, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 30, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852871"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Project Service Automation 업데이트 릴리스 30, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 30에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.51.61이며 일반적으로 2021년 4월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-30"></a>업데이트 릴리스 30

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- **역할** 필드가 제거된 경우 **빨리 만들기** 페이지에서 시간 항목을 만들고 저장할 때 오류가 발생합니다.
- 시간 입력 필터가 잘못된 필터 연산자를 적용합니다.
- 복사된 작업표는 시간 입력 제어에서 **주 복사** 선택시 자동으로 표시되지 않습니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.

- 예약을 연장할 때 하드 예약에 지정된 예약 상태가 올바르지 않습니다. 예약 연장은 예약 설정 메타데이터에서 **커밋** 으로 정의된 예약 상태를 따릅니다.
- 유효한 예약 상태가 지정되지 않은 경우 오류 메시지가 올바르게 현지화되지 않은 것입니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- 프로젝트는 하나의 통화로 만들 수 없으며 관련 작업을 다른 통화로 포함할 수 없습니다.

**판매**

다음과 같은 문제가 해결되었습니다.

- 가격표를 복사하면 가격이 업데이트되지 않습니다.
- 원가 세부 정보에 원산지 값이 있으면 견적을 성공으로 마감할 수 없습니다.
- **프로젝트 작업** 엔터티에서 **추정 비용** 이름이 **계획 비용(기본)** 으로 변경되었습니다.
- 송장이 생성되거나 삭제될 때 null 참조 예외가 생성됩니다.
