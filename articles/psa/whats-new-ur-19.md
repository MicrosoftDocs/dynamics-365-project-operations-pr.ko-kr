---
title: Project Service Automation 업데이트 릴리스 19, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 19, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126850"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation 업데이트 릴리스 19, V3

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 PSA V3, 업데이트 릴리스 19에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.30.41이며 일반적으로 2020년 5월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-19"></a>업데이트 릴리스 19

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다. 

- 시간 항목 가져 오기에서 파생된 오류가 올바르게 표시되지 않습니다.
- 시간 입력 그리드는 **날짜만** 필드 동작을 지원하지 않습니다.
- 프로젝트 리소스가 프로젝트 비용을 만들 수 없습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다. 

-  최하위 작업은 완료(EAC) 계산 중에 잘못된 노력 추정치를 유발합니다.

**Sales**

다음과 같은 문제가 해결되었습니다. 

- **다시 계산** 작업은 비용 계약 내용 세부 사항 또는 견적 라인 세부 사항과 함께 작동하지 않습니다.
- **가격 업데이트** 에 비용 추정치가 누락되었습니다.
-  고객이 **프로젝트 계약** 페이지에서 사용자 지정 계약 상태 설명을 선택할 수 없습니다.
- 고객은 견적에서 사용자 정의 가격표를 작성할 때 성능 저하를 경험합니다.
- 고객이 **견적 라인 세부 사항** 및 **계약 내용 세부 사항** 페이지에서 **단위** 기본값의 불일치를 경험합니다.
- 청구 불가능한 거래 범주 항목을 청구 가능 계약 내용에 추가하면 거래 범주의 **청구 불가능한** 청구 유형이 적용되지 않습니다.
- 고객은 이전에 생성된 계약에서 새로 추가된 역할 및 범주를 사용할 수 없습니다.
- 고객이 PreValidateProjectTeamMemberUpdate.cs의 불필요한 검색에서 성능 저하를 경험합니다.
- **리소스 범주** 목록에서 청구 불가능으로 설정된 역할은 프로젝트의 계약 내용에서 **청구 가능한 역할** 탭에 **청구 불가능** 으로 추가되어야 합니다.
- **GetBookableResourceIdFromUser** 는 기본 ID 대신 예약 가능한 리소스의 모든 열을 검색하기 때문에 프로젝트를 만들 때 고객이 성능 저하를 경험할 수 있습니다.
- **TransactionType** 엔터티에 사용자가 트랜잭션 유형에 유효하지 않은 **단위** 및 **단위 그룹** 을 입력하지 못하도록 사전 유효성 검사 업데이트 플러그인이 누락되었습니다.
- 시간 항목 가져오기에 **제거** 단계가 작동하지 않습니다.
