---
title: Project Service Automation 업데이트 릴리스 36, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation 업데이트 릴리스 36, V3에서 사용 가능한 기능 및 수정 사항을 나열합니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586674"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Project Service Automation 업데이트 릴리스 36, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 36, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.57.152이며 2021년 10월에 자체 업데이트를 통해 일반적으로 제공됩니다.

## <a name="update-release-36"></a>업데이트 릴리스 36

### <a name="bug-fixes"></a>버그 수정

다음과 같은 문제가 해결되었습니다.

**일반**
- **기본 작업 시간 템플릿** 필드 이름이 **프로젝트 매개변수** 페이지에서 잘못 번역되었습니다.
- 비동기 플러그인은 **SharedVariableService** 와 관련된 예외를 올바르게 처리하지 않습니다.

**시간 및 경비**
- 분개장 항목이 누락되었거나 사용자에게 분개 라인을 읽을 수 있는 올바른 권한이 없는 경우 프로젝트 승인이 취소될 때 잘못된 오류가 발생합니다.
- 경비 또는 시간 항목에 둘 이상의 연결된 프로젝트 승인이 있는 경우 사용자는 승인을 취소할 수 없습니다.
- **부재** 및 **휴가** 는 **시간 입력** 빠른 만들기 페이지의 조회에서 중국어의 경우 잘못 번역되었습니다.

**리소스 관리**
- 보기 모드가 **일**, **주** 또는 **월** 로 설정되어 있을 때 **일정 도우미** 에서 사용자가 리소스를 검색할 수 없습니다.
- 일반 리소스에는 빈 직위 이름이 잘못 허용됩니다. 
- 분실로 계약을 종료해도 향후 예약은 취소되지 않습니다.

**판매**
- 제품의 양이 많은 환경에서는 **재료 견적** 그리드의 성능이 저하됩니다.
- 템플릿에서 프로젝트를 생성할 때 프로젝트 통화는 기본적으로 해당 프로젝트 관리자의 계약 단위로 설정되지 않습니다.
- 실제 금액이 프로젝트 기한에 반영된 금액과 항상 일치하지 않거나 특정 회수 시나리오에서 금액이 음수가 됩니다.
- 프로젝트 템플릿에서 생성된 프로젝트를 계약 내용에 연관시킬 때 오류가 발생합니다.
- 사용자는 **인보이스 준비** 및 **송장 생성됨** 이정표가 있는 계약 내용을 삭제할 수 있습니다. 이것은 허용되어서는 안됩니다.
- 프로젝트에서 견적을 가져올 때 견적 라인에 대해 작업 기반 청구가 활성화된 경우 견적 라인 세부사항 청구 가능성이 잘못 설정됩니다.
- 고정 가격 청구 마일스톤을 추가하면 페이지를 새로 고칠 때까지 마일스톤이 마일스톤 하위 표에 반영되지 않습니다.
- null인 견적 이름으로 프로젝트 계약을 생성하면 null 참조 예외가 생성됩니다.
- 프로젝트 통화가 리소스의 통화와 다른 수동 모드 작업은 잘못된 가격 견적을 초래합니다.
- 사용자는 수정 송장으로 성공적으로 수정된 거래를 회수할 수 없습니다.
- 비활성화된 거래 범주는 **비용 견적** 그리드에 나타납니다.



