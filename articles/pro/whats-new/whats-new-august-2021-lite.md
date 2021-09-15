---
title: 2021년 8월의 새로운 기능 - Project Operations 라이트 배포
description: 이 항목은 Project Operations 라이트 배포의 2021년 8월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323514"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>2021년 8월의 새로운 기능 - Project Operations 라이트 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 항목은 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

  - Dataverse 환경 버전 4.13.0.152의 Project Operations

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- **승인 집합**: 승인은 그룹 시간, 경비 또는 자재 사용 승인 요청을 더 작은 작업 하위 집합으로 함께 설정합니다. 이 그룹화를 통해 프로젝트별로 특정 순서로 승인을 처리하고 재시도 및 순서를 지정할 수 있습니다. 요청을 그룹화하면 대량 승인에 대한 승인 처리의 안정성과 추적 가능성이 향상됩니다. 자세한 내용은 [승인 집합](../../approvals/approval-sets.md)을 참조하십시오.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-on-dataverse"></a>Dataverse의 Project Operations

| **기능 영역** | **참조 번호** | **품질 업데이트** |
| --- | --- | --- |
| 청구 및 가격 책정 | 2295625 | 마일스톤 이름은 송장 일정에서 송장 라인 상세내역으로 복사해야 합니다. |
| 청구 및 가격 책정 | 2316323 | 리소스 기반 시나리오에 대한 Project Operations의 견적 송장에서 할인을 편집할 수 없어야 합니다. |
|  영업 기회 관리 | 2338619 | **영업 기회** 및 **견적** 비즈니스 규칙은 페이지에서만 호출해야 합니다. |
| 리소스 관리 | 2316523 | 역할이 연결된 리소스 요구 사항에서 **요청 보내기** 를 사용하면 오류가 표시되지 않습니다. |
| 리소스 관리 | 2326885 | 프로젝트를 통해 리소스 요구 사항을 생성하면 오류가 표시되지 않습니다. |
| 시간 및 경비 | 2335584 | 시간 항목에서 더 이상 사용되지 않는 작업 흐름입니다. |
| 시간 및 경비 | 2336884 | **주 복사** 시간 입력 버튼은 현재 사용자뿐만 아니라 다른 사용자에게도 작동해야 합니다. |
