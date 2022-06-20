---
title: 2022년 2월의 새로운 기능 - Project Operations 라이트 배포
description: 이 문서에서는 Project Operations Lite 배포의 2022년 2월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922828"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>2022년 2월의 새로운 기능 - Project Operations 라이트 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.28.0.120의 Project Operations

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스부터 단일 프로젝트에 최대 300명의 팀 구성원을 추가할 수 있습니다. 이전에는 팀원 수 제한이 150명이었습니다. 자세한 내용은 [프로젝트 제한](../../project-management/create-wbs.md#project-limitations)을 참조하십시오.

## <a name="quality-updates"></a>품질 업데이트

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2497369 | 재료 수정은 **보정** 매개 변수의 날짜 값을 따라야 합니다. |
| 청구 및 가격 책정 | 2498697 | **시간 입력 회수** 에 대한 보안 구성을 개선했습니다. |
| 청구 및 가격 책정 | 2517455 | **송장 라인 트랜잭션 새로 고침** 작업은 동일한 송장에 대해 작업이 동시에 여러 번 실행되도록 허용해서는 안 됩니다. |
| 청구 및 가격 책정 | 2517465 | **송장 라인 상세내역 비활성화** 작업은 지원되지 않기 때문에 작업이 차단되었습니다. |
| 청구 및 가격 책정 | 2556660 | 프로젝트 매개변수 레코드에 첨부된 가격표에서 수행되는 날짜 유효성 검사를 수정했습니다. |
| 영업 기회 관리 | 2369202 | 유효 날짜가 겹치는 가격표를 동일한 프로젝트 계약에 첨부할 수 있는지 확인하는 비즈니스 로직을 수정했습니다. |
| 영업 기회 관리 | 2385965 | **저장 후 닫기** 를 선택할 때 **프로젝트 계약** 페이지의 **고객** 탭에서 동작을 수정했습니다. |
