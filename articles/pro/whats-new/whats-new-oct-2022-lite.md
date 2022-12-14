---
title: 2022년 10월의 새로운 기능 - Project Operations Lite 배포
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations Lite 배포의 2022년 10월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806642"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>2022년 10월의 새로운 기능 - Project Operations Lite 배포

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.57.0.176의 Project Operations

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

| 기능 영역 | 기능 이름 | 자세한 정보 |
| --- | --- | --- |
| 프로젝트 계획 및 추적 | **Project Operations 외부 스케줄링**<br>외부 예약 모드를 사용하면 고객은 기본적으로 Project for the Web에서 적용되는 현재 제한 없이 기본 Dataverse API를 사용하여 WBS(작업 분할 구조)와 관련된 엔터티를 만들고 업데이트하고 삭제할 수 있습니다. | [외부 일정](/dynamics365/project-operations/project-management/external-scheduling) |
| 배포 및 구성 | <p>**고객이 배포 유형을 선택하도록 허용**<br>Project Operations의 PDU(제품 기반 업데이트)는 이중 쓰기 코어 및 오케스트레이션 솔루션이 환경에 설치된 경우 Project Operations 이중 쓰기 솔루션을 자동으로 설치하는 데 사용됩니다.</p><p>이 기능은 프로젝트 매개 변수에 새로운 **솔루션 업그레이드 동작** 매개 변수를 도입합니다. 이 매개 변수가 **Lite 전용** 으로 설정되면 환경에 이중 쓰기 코어 및 오케스트레이션 솔루션이 설치되어 있어도 PUD는 더 이상 Project Operations 이중 쓰기 솔루션을 자동으로 설치하지 않습니다. 이 동작은 이중 쓰기 솔루션을 사용하여 판매 주문을 금융 및 운영 앱에 통합할 계획이지만 Lite 모드(즉, 금융 및 운영 앱에 통합하지 않음)에서 Project Operations를 사용하려는 고객에게 도움이 됩니다.</p> | |

## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2316317 | 시스템에서 청구 거래가 없는 송장을 생성할 수 있습니다. |
| 청구 및 가격 책정 | 2737300 | 양식에 액세스하기 전에 고객 필드 가용성을 확인하세요. |
| 청구 및 가격 책정 | 2744948 | 청구 방법에 대한 null 검사를 추가합니다. |
| 청구 및 가격 책정 | 2763515 | 송장의 판매 계약이 누락된 경우 Null 참조 오류 핸들입니다. |
| 청구 및 가격 책정 | 2844301 | 오류로 인해 일괄 송장 생성에 실패했습니다. |
| 청구 및 가격 책정 | 2845869 | 조직 서비스의 잘못된 저장. |
| 청구 및 가격 책정 | 2853729 | 청구 유형이 수정되면 역할 및 가격 세부 정보가 업데이트됩니다. |
| 청구 및 가격 책정 | 2940350 | 실제 가격이 책정되면 활성 가격 목록만 자동으로 입력되어야 합니다. |
| 배포 및 구성 | 3001206 | msdyn\_replaylogheader 엔터티가 고객 조직의 업그레이드를 막고 있습니다. |
| 영업 기회 관리 | 2755582 | 분할 청구 규칙 도우미에서 Null 참조 예외 처리. |
| 영업 기회 관리 | 2761477 | 분할 청구를 사용하는 경우 마일스톤(헤더)을 삭제하면 고아 마일스톤이 남습니다. |
| 영업 기회 관리 | 2767595 | 기본 양식에서 재료 사용 레코드를 열면 레코드에 대한 예약 가능한 리소스가 현재 로그인한 사용자로 변경됩니다. |
| 프로젝트 계획 및 추적 | 2790384 | Pending OperationSet 시간 제한이 너무 짧습니다. |
| 리소스 관리 | 2751560 | 자원 요구 사항에서 선호하는 조직 단위가 일치하지 않습니다. |
| 하도급 계약 | 2907231 | 공급업체 인보이스의 처리 단계를 진행할 수 없습니다. |
| 시간 및 경비 | 2867363 | 레코드가 승인 대기 중인 경우 승인을 위한 부재/휴가 보기에서 벗어나지 않습니다. |
| 시간 및 경비 | 2894405 | TESA: 사용하지 않는 POC 디렉토리로 인해 규정 준수 문제가 발생합니다. |
