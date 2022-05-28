---
title: 2022년 3월의 새로운 기능 - Project Operations 라이트 배포
description: 이 항목에서는 Project Operations Lite 배포의 2022년 3월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583758"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>2022년 3월의 새로운 기능 - Project Operations 라이트 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 항목은 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.30.0.99의 Project Operations

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

- 하도급 계약: 공급업체 송장 생성 및 일치 경험

## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 시간 및 경비 | 2388011 | 일괄 승인 중에 시간 입력 제출자에게 거부 의견을 표시합니다. |
| 프로젝트 계획 및 추적 | 2495294 | **작업 세부 정보** 페이지에서는 프로젝트 세부 정보를 편집할 수 없어야 합니다. |
| 청구 및 가격 책정 | 2499605 | 견적 마일스톤에서 생성된 계약 마일스톤이 읽기 전용으로 잘못 표시됩니다. |
| 프로젝트 계획 및 추적 | 2506050 | 저장할 변경 사항이 없으면 작업 집합이 1시간 동안 보류 상태로 유지됩니다. 그런 다음 집합은 **실패** 로 잘못 표시되지만 즉시 완료되어야 합니다. |
| 청구 및 가격 책정 | 2507401 | 잘못된 캐싱으로 인해 기본 계약 단위가 프로젝트에 잘못 입력됩니다. |
| 청구 및 가격 책정 | 2541660 | 이중 쓰기의 **판매 주문 생성 유효성 검사** 는 프로젝트 기반 주문에만 사용해야 합니다. |
| 청구 및 가격 책정 | 2552745 | 분할 청구 규칙을 설정한 고객 간에 세금이 분할되지 않습니다. |
| 청구 및 가격 책정 | 2558859 | 가격 책정 차원을 설정할 때 오류 메시지가 개선되었습니다. |
| 청구 및 가격 책정 | 2558933 | **msdyn\_project** 가 가격 차원으로 추가되면 **프로젝트 견적에서 가져오기** 가 실패합니다. |
| 청구 및 가격 책정 | 2559101 | 프로젝트 매개 변수 삭제가 차단되지 않고 문제가 발생합니다. |
| 영업 기회 관리 | 2570390 | 이중 쓰기 플러그인은 견적, 주문 및 영업 기회에 대한 계정 유형이 정확하지 않은 경우에도 **고객** 이 되도록 강제합니다. |
| 청구 및 가격 책정 | 2586097 | 분할 청구 비용 실제 값은 프로젝트가 프로젝트 계약 내용에서 제거될 때 취소되지 않습니다. |
| 청구 및 가격 책정 | 2589619 | 직접 입력 자재에 대한 세금은 청구되지 않은 실제 판매액과 송장으로 전달됩니다. |
| 영업 기회 관리 | 2594015 | **Net60** 지불 조건이 있는 고객의 경우 견적을 낙찰로 마감할 수 없습니다. |
| 프로젝트 계획 및 추적 | 2595841 | Project for the Web에서 사용자는 새 리소스 요청을 만들 때 누락된 **msdyn\_actualstart** 에 대한 오류 메시지를 받습니다. |
| 시간 및 경비 | 2602511 | 시간 항목에 대한 **거부한 사람** 필드에 기명 사용자 대신 **시스템** 이 거부자로 표시됩니다. |
| 시간 및 경비 | 2602528 | 프로젝트 승인자는 승인자로 나열되지 않은 프로젝트의 시간을 승인할 수 있습니다. |
| 청구 및 가격 책정 | 2608550 | 수정 송장은 원본에 변경 사항이 없어도 확정할 수 있습니다. |

## <a name="removed-and-deprecated-features"></a>제거되었고 사용되지 않는 기능

[Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](../../whats-new/removed-depreciated-features-project.md) 항목에서는 Dynamics 365 Project Operations의 제거되었거나 더 이상 사용되지 않는 기능을 설명합니다.

- 제거된 기능은 더 이상 제품에서 사용할 수 없습니다.
- 더 이상 사용되지 않는 기능은 현재 개발 중이 아니며 향후 업데이트에서 제거될 수 있습니다.

사용 중단 발표는 제품에서 기능이 제거되기 12개월 전에 [Project Operations에서 제거되거나 더 이상 사용되지 않는 기능](../../whats-new/removed-depreciated-features-project.md) 항목에 표시됩니다.