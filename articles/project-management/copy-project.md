---
title: 프로젝트 복사
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트 복사에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908341"
---
# <a name="copy-a-project"></a>프로젝트 복사

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations를 사용하면 **프로젝트**에서 **프로젝트 복사** 작업을 사용하여 새 프로젝트를 빠르게 빌드할 수 있습니다. 프로젝트를 복사하려면 프로젝트를 선택한 다음 **복사**를 선택합니다. 작업이 복사됩니다.

- 프로젝트 속성
- 작업 분할 구조
- 프로젝트 팀 구성원
- 프로젝트 추정
- 프로젝트 경비 추정치

## <a name="project-properties"></a>프로젝트 속성

프로젝트가 복사되면 다음 필드의 값이 복사됩니다.

- Name
- 설명
- 고객
- 일정 템플릿
- 통화
- 계약 단위
- 프로젝트 관리자
- 상태
- 전체 프로젝트 상태
- 메모
- 추정
- 예상 시작 날짜
- 완료 날짜
- 작업량(시간)
- 예상 노동 비용
- 예상 경비 비용

## <a name="work-breakdown-structure"></a>작업 분할 구조

프로젝트를 복사하면 전체 리소스 로드 작업 분할 구조가 복사됩니다. 명명된 리소스가 일반 리소스로 대체됩니다. 명명된 리소스의 작업 시간이 일반 리소스와 동일하지 않은 경우 일정이 다시 계산되고 작업 기간이 변경될 수 있습니다.

## <a name="project-team-members"></a>프로젝트 팀 구성원

원본 프로젝트에서 프로젝트 팀을 복사하면 일반 리소스가 복사됩니다. 일반 리소스 배정은 원본 프로젝트에서와 같이 관리됩니다. 명명된 리소스는 일반 팀 구성원으로 변환됩니다.

## <a name="estimates"></a>추정

프로젝트가 복사되면 리소스 및 경비 추정 라인이 모두 원본 프로젝트에서 복사됩니다.