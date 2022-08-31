---
title: 2022년 7월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능
description: 이 문서에서는 재고/생산 기반 시나리오에 대한 Microsoft Dynamics 365 Project Operations의 2022년 7월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: ramagadu
ms.date: 8/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b1dc72f164202835a994935e479bca1ab23b7682
ms.sourcegitcommit: 6be13fc3d7e61a8f95ed200f418314135c7e5c2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305924"
---
# <a name="whats-new-or-changed-in-project-operations-july-2022-for-stockedproduction-based-scenarios"></a>2022년 7월 리소스/생산 기반 시나리오에 대한 Project Operations의 새로운 기능 또는 변경된 기능

_**적용 대상:** 리소스/생산 기반 시나리오에 대한 Project Operations_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dynamics 365 Finance 환경 버전 10.0.28의 프로젝트 관리 및 회계

## <a name="quality-updates"></a>품질 업데이트

이 업데이트에 포함된 버그 수정에 대한 정보는 Microsoft Dynamics LCS(Lifecycle Services)에 로그인하여 [KB 문서](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)를 보십시오.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>향후 릴리스에서 기본적으로 켜져 있는 기능

다음 표에는 버전 10.0.29에서 기본적으로 켜져 있는 기능이 나열되어 있습니다. 자동으로 켜진 대부분의 기능은 [기능 관리](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)에서 끌 수 있습니다. 앞으로는 자동으로 켜진 일부 기능이 기능 관리에서 제거되어 필수가 될 수 있습니다. 이 변경 사항은 고객이 현재 기능을 사용하도록 하여 추가된 현재 기능을 기반으로 개선 사항을 구축할 수 있도록 합니다. 기능은 필수라고 판단되지 않는 한 1년 이내에 자동으로 활성화되지 않습니다.

| 기능 이름 | 활성화 날짜 | 기능을 추가한 날짜 | 기능 상태 | 모듈 |
| --- | --- | --- |--- |--- |
| 자금 조달 규칙 할당 변경에 따른 시간 트랜잭션 조정 가능 | 2022년 9월 16일 | 2020년 10월 7일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트 구매 주문 선불 송장 취소 기능 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 자원 기반/비 재고 시나리오에 대해 Project Operations를 사용할 때 송장 제안 라인 삭제 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 게시된 프로젝트 트랜잭션에 대한 회계 조정 | 2022년 9월 16일 | 2020년 5월 10일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트에 대한 기본 회계 설정 활성화 | 2022년 9월 16일 | 2020년 2월 19일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트에 대해 여러 계약 내용 활성화 | 2022년 9월 16일 | 2020년 6월 29일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 현재 승인 상태가 편집을 허용하지 않는 경우 프로젝트 시간 분개장을 읽기 전용으로 설정 | 2022년 9월 16일 | 2021년 10월 6일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 구매 라인이 업데이트되고 구매 주문 변경 관리 매개 변수가 켜져 있을 때 구매 라인에서 판매 라인 동기화 활성화 | 2022년 9월 16일 | 2020년 10월 7일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| Dynamics 365 Customer Engagement에서 Project Operations 활성화 | 2022년 9월 16일 | 2020년 6월 29일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |
| 프로젝트 트랜잭션 취소 수정 기능 | 2022년 9월 16일 | 2020년 7월 13일 | 기본적으로 켜짐 | 프로젝트 관리 및 회계 |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>향후 릴리스에서 필수가 되는 기능

다음 표에는 버전 10.0.29 이후에 필수가 되는 기능이 나열되어 있습니다.

| 기능 이름 | 활성화 날짜 | 기능을 추가한 날짜 | 기능 상태 | 모듈 |
| --- | --- | --- | --- | --- |
| 환율을 반올림하지 않고 자금 출처의 약정 가치를 계산합니다. | 2022년 9월 16일 | 2020년 6월 14일 | 필수 | 프로젝트 관리 및 회계 |
| 원래 거래와 동일한 원장 계정으로 프로젝트 조정 전기 활성화 | 2022년 9월 16일 | 2020년 6월 14일 | 필수 | 프로젝트 관리 및 회계 |
| 프로젝트 계약 약정 금액 세부 정보 | 2022년 9월 16일 | 2019년 8월 31일 | 필수 | 프로젝트 관리 및 회계 |
| 프로젝트 송장 제안 생성 중 리소스별 정렬 활성화 | 2022년 9월 16일 | 2019년 8월 31일 | 필수 | 프로젝트 관리 및 회계 |
