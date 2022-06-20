---
title: 2021년 12월의 새로운 기능 - Project Operations Lite 배포
description: 이 문서에서는 Project Operations Lite 배포의 2021년 12월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914088"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>2021년 12월의 새로운 기능 - Project Operations Lite 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.27.0.195, 4.27.0.242, 4.27.0.244의 Project Operations


## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

### <a name="subcontract-management"></a>하도급 계약 관리 

- [프로젝트 팀원 하도급 계약](../subcontracting/subcontracting-project-team-members.md): 프로젝트 관리자는 인력 충원 및 견적에 영향을 미치기 위해 하도급 계약 및 하도급 계약 내용이 있는 명명된 또는 일반 팀 구성원을 생성할 수 있습니다.
- [프로젝트 팀 구성원을 위한 하도급 계약 옵션](../subcontracting/subcon-options.md): 명명된 또는 일반 프로젝트 팀 구성원에 대한 인력 배치를 선택할 때 프로젝트 관리자는 기존 하도급 계약을 검토하거나 한 명 이상의 프로젝트 팀 구성원에 대한 새 하도급 계약을 작성할 수 있습니다. 
- [하도급 계약 리소스 배정 비용 추정](../subcontracting/costing-subcon-ra.md): 프로젝트 비용 추정은 하도급 계약 리소스 할당을 고려하고 하도급 계약과 관련된 구매 가격표를 사용하여 비용을 책정합니다. 
- [계약 작업자 및 하도급 계약 용량을 표시하도록 일정 게시판 구성](../subcontracting/configure-sb-subcon.md): 이제 Project Operations의 일정 게시판이 직원과 함께 예약 가능한 리소스 및 하도급 계약 용량의 계약 작업자 유형을 검색하고 제안하도록 구성할 수 있습니다. 이 구성은 특정 프로젝트 요구 사항에 대한 인력 배치 컨텍스트 내에서 리소스를 검색하거나 프로젝트 요구 사항 컨텍스트 외부에서 검색할 때 적용할 수 있습니다.
- [계약 작업자 및 하도급 계약 능력이 있는 프로젝트 인력 배치](../subcontracting/staffing-cw.md): 이제 일정 게시판 경험을 활용하여 프로젝트에 계약 작업자를 예약할 수 있습니다.
- [하도급 계약 구성 요소에 대한 프로젝트의 시간, 경비 및 자재 사용량 기록](../subcontracting/recording-subcon-actuals.md): 계약 작업자는 시간과 경비를 기록할 수 있고, 프로젝트 팀 구성원은 프로젝트에서 하도급 계약을 통해 구매한 자재의 사용량을 기록할 수도 있습니다. 이렇게 하면 구매한 용량 또는 자재를 사용하는 프로젝트에 대한 정확한 비용이 기록됩니다.
- [하도급 계약의 상태 전환](../subcontracting/subcon-states.md): 하도급 계약은 판매자와의 협상 완료를 확인하기 위해 확인하고, 납품 완료를 위해 마감을 하거나, 납품이 완료되기 전에 판매자와 계약이 종료되는 것을 취소하기 위해 계약을 체결할 수 있습니다.

### <a name="task-planning"></a>작업 계획
- 시스템 관리자를 위한 개선된 문제 해결. 사용자가 프로젝트를 열 수 없는 경우 관리자는 [프로젝트 일정 로그](../../project-management/schedule-api-logs.md)에서 Project for the Web에서 생성된 라이선스와 관련 없는 오류를 검토할 수 있습니다.
- [Microsoft Project for the Web에서 작업 검사 목록 사용](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for the Web에서 검사 목록을 작업에 추가하여 특정 항목을 추적할 수 있습니다.

## <a name="quality-updates"></a>품질 업데이트

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 계획 및 추적 | 2392596 | 일정 API는 이제 **남은 작업량**, **완료된 작엽량** 및 **완료율** 필드에 대한 업데이트를 허용합니다. |
| 계획 및 추적 | 2478497 | 일정 API **활동 번호** 및 **작업 ID** 필드는 시스템에서 자동 번호 지정을 사용하여 채우기 때문에 입력 시 비어 있을 수 있습니다.|
| 시간 및 경비 | 2468135 | 승인 재시도 횟수가 5회에서 3회로 줄었습니다. |
| 시간 및 경비 | 2468188 | **Annotation** 엔터티의 **notetext** 속성에서 로그 텍스트가 최대 길이를 초과하는 문제를 수정했습니다. |
