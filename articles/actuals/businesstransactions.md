---
title: Project Operations의 비즈니스 거래
description: 이 항목에서는 Microsoft Dynamics 365 Project Operations의 비즈니스 트랜잭션 개념에 대한 개요를 제공합니다.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582212"
---
# <a name="business-transactions-in-project-operations"></a>Project Operations의 비즈니스 거래

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Microsoft Dynamics 365 Project Operations에서 *업무 처리* 는 어떤 엔터티로도 표현되지 않는 추상적 개념입니다. 그러나 엔터티의 일부 공통 필드와 프로세스는 업무 처리의 개념을 사용하도록 설계되었습니다. 다음 엔터티들이 이 추상적 개념 사용합니다:

- 견적 행 내역
- 계약 행 내역
- 추산 행
- 분개장 행
- 실제

이러한 엔터티 중 견적 행 내역, 계약 행 내역 및 추산 행 내역은 프로젝트 라이프사이클의 *추산 단계* 에 매핑됩니다. 분개장 행 및 실제값 엔터티는 프로젝트 라이프사이클의 *집행 단계* 에 매핑됩니다.

Project Operations는 이러한 5개 엔터티 모두의 레코드를 비즈니스 트랜잭션으로 취급합니다. 유일한 차이점은 추정 단계에 매핑된 엔터티의 레코드(견적 라인 세부 정보, 계약 내용 세부 정보 및 견적 라인)는 *재무 예측* 으로 간주되는 반면 실행 단계에 매핑되는 엔터티의 레코드(분개장 항목 및 실제 값)는 이미 발생한 *재무적 사실* 로 간주됩니다.

상세한 설명은 [추산](../project-management/estimating-projects-overview.md) 및 [실제값](actuals-overview.md)을 참조하십시오.

## <a name="concepts-that-are-unique-to-business-transactions"></a>업무 처리에 독특한 개념

다음 개념은 업무 처리의 개념에 고유합니다:

- 처리 타입
- 처리 등급
- 처리 기원
- 처리 연결

### <a name="transaction-type"></a>처리 타입

처리 타입은 프로젝트에 미치는 재무적 영향의 타이밍과 상황을 나타냅니다. Project Operations에서 지원되는 다음 값이 있는 옵션 집합에 의해 정의됩니다.

- 비용
- 프로젝트 계약
- 미청구된 매출액
- 청구된 매출액
- 조직간 매출액
- 리소스 단위 비용

### <a name="transaction-class"></a>처리 등급

처리 등급은 프로젝트에서 발생하는 다양한 타입의 비용을 나타냅니다. Project Operations에서 지원되는 다음 값이 있는 옵션 집합에 의해 정의됩니다.

- 시간
- 경비
- 재료
- 티켓
- 이정표
- 세금

> [!NOTE]
> **이정표** 는 일반적으로 Project Operations에서 고정 가격 청구를 위한 비즈니스 논리에 의해 사용됩니다.

### <a name="transaction-origin"></a>거래 확보 경로

트랜잭션 출처는 보고 및 추적성을 돕기 위해 각 비즈니스 트랜잭션의 출처를 저장하는 엔터티입니다. 프로젝트 실행이 시작되면 각 비즈니스 트랜잭션은 또 다른 비즈니스 트랜잭션을 생성하고 차례로 다른 비즈니스 트랜잭션을 생성하는 식입니다.

### <a name="transaction-connection"></a>처리 연결

처리 연결은 비용과 관련 매출액 실제값 같은 두 개의 유사한 업무 처리 사이의 관계 또는 청구서 확인 또는 청구서 수정과 같은 청구 활동에 의해 트리거되는 처리 반전을 저장하는 엔터티입니다.

처리 기원 및 처리 연결 엔터티를 함께 사용하면 업무 처리와 특정 업무 처리의 생성을 야기하는 조치 사이의 관계를 추적하는 데 도움이 됩니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
