---
title: Project Service Automation 업데이트 릴리스 32, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 32, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994869"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Project Service Automation 업데이트 릴리스 32, V3의 새로운 기능 또는 변경된 기능

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation 앱에 대한 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인 솔루션 페이지의 관리 센터를 방문하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 32에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.53.108이며 일반적으로 2021년 6월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-32"></a>업데이트 릴리스 32

### <a name="bug-fixes"></a>버그 수정

#### <a name="general"></a>일반

- 주요 업그레이드가 실패하면 공유 엔터티에 계속 액세스할 수 있도록 기본 응용 프로그램 진입점만 차단해야 합니다.

#### <a name="time-and-expense"></a>시간 및 경비

다음과 같은 문제가 해결되었습니다.

- **TimeEntriesImportFromResourceAssignment** 는 리소스 할당 등고선 슬라이스의 시작 및 종료 시간을 유지하지 않습니다.
- **시간 항목** 에서 **항목 열기** 를 선택하면 다른 양식을 선택하지 못할 수 있습니다.
- 시간 항목에 할당을 가져오는 동안 클라이언트 코드 쿼리는 쿼리에 실패하는 긴 URL을 생성할 수 있습니다.
- **시간 항목** 그리드에서 값이 셀에서 삭제된 후 포커스가 그리드에 남아 있지 않습니다.
- 최신 승인의 경우 **승인 처리 중** 보기에서 **거부** 버튼이 제거되었습니다.
- 시간 항목 대량 승인의 안정성과 성능은 교착 상태 및 **시간 항목** 엔터티와 관련된 사용자 지정을 적절하게 처리하지 못하는 경우 영향을 받습니다.

#### <a name="project-planning"></a>프로젝트 계획

- **계약 단위** 필드에 null 값이 있는 프로젝트를 업데이트하면 null 참조 예외가 생성됩니다.
- **프로젝트 합계 새로 고침** 이 프로젝트의 남은 비용과 남은 매출을 잘못 계산합니다.
- 중복 가격 계산은 리소스 할당 윤곽의 업데이트와 관련된 성능에 영향을 줍니다.

#### <a name="resource-management"></a>리소스 관리

다음 문제가 해결되었습니다.

- 예약 가능한 리소스의 달력 용량이 1보다 크면 Project Service Automation에서 용량을 0(영)으로 잘못 인식합니다. 따라서 일정 보기에서 무한 루프가 발생합니다.

#### <a name="sales"></a>판매

다음과 같은 문제가 해결되었습니다.

- 사용자 지정 트랜잭션 유형이 있는 분개장 항목이 생성되면 다음과 같은 null 참조 예외가 발생합니다.*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- 견적을 복사하기 전에 비활성화된 역할 및 범주는 새로 복사된 견적의 청구 가능한 역할 및 범주에 추가하면 안됩니다.
- 증빙 날짜 및 회계 날짜가 초안 송장에 직접 생성된 송장 라인 세부 정보에 제공된 시작 날짜와 일치하지 않습니다.
- 견적을 복사하기 전에 역할 및 범주 비활성화와 관련된 시나리오에서 Null 참조 예외가 생성됩니다.
- **프로젝트** 페이지의 **가격 업데이트** 작업이 비용 견적 및 재료 견적을 업데이트하지 않습니다.
