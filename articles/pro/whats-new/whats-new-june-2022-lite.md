---
title: 2022년 6월의 새로운 기능 - Project Operations 라이트 배포
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations Lite 배포의 2022년 6월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959442"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>2022년 6월의 새로운 기능 - Project Operations 라이트 배포

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.43.0.77의 Project Operations

## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 하도급 계약 | 2708885 | 사용자가 예약 가능한 리소스가 채워지지 않은 예약 가능한 리소스 예약 헤더 레코드를 생성할 때 나타나는 오류 메시지를 수정했습니다. |
| 프로젝트 계획 및 추적 | 2629441 | 프로젝트 작업이 업데이트될 때 무한 루프를 방지하는 데 도움이 되도록 워크플로 트리거 논리를 수정했습니다. |
| 시간 및 경비 | 2641209 | 할당/예약에서 시간 입력 가져오기는 예약 가능한 리소스 참조를 유지해야 합니다. |
| 프로젝트 계획 및 추적 | 2651148 | 프로젝트 문서 헤더는 보호되어야 합니다.|
| 프로젝트 계획 및 추적 | 2653145 | 이름에 유효하지 않은 문자가 포함된 프로젝트 레코드를 생성할 수 없도록 하는 유효성 검사가 추가되었습니다. |
| 시간 및 경비 | 2654710 | **승인** 페이지에서 필터링을 수정했습니다. |
| 청구 및 가격 책정 | 2667805 | 미청구 판매 실적을 뒷받침하지 않는 경우 청구 판매 실적이 생성되지 않도록 하는 유효성 검사가 추가되었습니다. |
| 청구 및 가격 책정 | 2668378 | 논리적 이름과 필드 이름이 채워지지 않는 한 사용자 정의 가격 차원이 추가되는 것을 방지하는 데 도움이 되는 유효성 검사가 추가되었습니다. |
| 시간 및 경비 | 2700428 | 승인 세트 중 하나가 시스템 작업에 걸린 경우에도 프로젝트에 대한 다른 승인 세트를 처리할 수 있도록 승인 논리를 개선했습니다. |
