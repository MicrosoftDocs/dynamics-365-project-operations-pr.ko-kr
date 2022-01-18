---
title: Project Operations 업데이트
description: 이 토픽은 Dynamics 365 Project Operations의 출시된 버전에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5e37bc90a74e6bc9f1bf3d3820a34c3f4c3496d
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942847"
---
# <a name="project-operations-updates"></a>Project Operations 업데이트

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 처리 및 재고/생산 기반 시나리오를 위한 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations 구성 요소

Dynamics 365 Project Operations는 두 가지 구성 요소로 구성됩니다.

- Dataverse 환경의 Project Operations는 영업 기회에서 견적 송장까지 다양한 기능을 다룹니다. Dataverse는 Project Operations의 라이트 배포 및 리소스/비 재고 시나리오 배포에 사용됩니다.
- Dynamics 365 Finance 환경의 프로젝트 관리 및 회계에는 경비 관리 기능, 프로젝트 회계 및 수익 인식이 포함됩니다. Finance and Operations 앱 환경은 리소스/비 재고 기반 시나리오를 위한 Project Operations 및 재고/생산 기반 시나리오를 위한 Project Operations에 사용됩니다.

## <a name="project-operations-release-notes"></a>Project Operations 릴리스 정보
- [리소스/비 재고](whats-new-dec-2021-resource-based.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.
- [라이트 배포](../pro/whats-new/whats-new-dec-2021-lite.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.
- [리소스/생산](../prod-pma/whats-new/whats-new-oct-2021-stocked.md) 시나리오에 대한 Project Operations 최신 릴리스 정보.

## <a name="project-operations-latest-version"></a>Project Operations 최신 버전

| Dataverse 환경의 Project Operations | Finance and Operations 앱 환경의 프로젝트 관리 및 회계 | 
| --- | --- |
| 4.27.0.242 | 10.0.23 |

Project Operations 리소스/재고가 없는 시나리오의 경우 Dual Write Orchestration 버전 2.3.1.15 이상을 사용하는 것이 좋습니다.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Dataverse 환경에서 Project Operations를 위한 릴리스 일정

Dataverse 환경의 Project Operations에 대한 업데이트는 매월 제공됩니다. 

| 스테이션 | 지역 | 현재 버전 번호 | 라이트 배포를 위한 자동 업데이트 | 리소스/비 재고 배포를 위한 자동 업데이트 | 다음 버전 번호 | 일반적으로 사용 가능한 다음 버전 |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| 스테이션 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 최초 릴리스         |  4.27.0.242     | 완료*          | 완료*           | TBD                 | 2022년 1월 14일    |
| 스테이션 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 남아메리카         |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 14일    |
|   &nbsp;  | 캐나다                |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 14일    |
|   &nbsp;  | 인도                 |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 14일    |
|   &nbsp;  | 프랑스                |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 14일    |
|   &nbsp;  | 남아프리카 공화국          |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 14일    |
| 스테이션 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 일본                 |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 21일    |
|   &nbsp;  | 아시아 태평양          |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 21일    |
|   &nbsp;  | 영국         |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 21일    |
|   &nbsp;  | 오세아니아               |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 21일    |
|   &nbsp;  | 아랍에미리트연합국  |  4.27.0.242     | 완료됨           | 2022년 1월 7일    | TBD                 | 2022년 1월 21일    |
| 스테이션 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 유럽                |  4.26.0.155     | 완료됨           | 2022년 1월 7일    | 4.27.0.242          | 2022년 1월 10일    |
| 스테이션 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 북아메리카         |  4.26.0.155     | 2022년 1월 7일   | 2022년 1월 14일    | 4.27.0.242          | 2022년 1월 17일    |

>[!Note]
> - 완료* - 버전 4.27.0.195로 자동 업데이트가 완료되었습니다.


## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Finance and Operations 앱 환경의 프로젝트 관리 및 회계에 대한 릴리스 일정

프로젝트 관리 및 회계에 대한 업데이트는 1년에 8번 릴리스됩니다.

|지원되는 버전| 사용 가능성 미리 보기(PEAP) | 일반적으로 사용 가능(자체 업데이트) | 자동 업데이트 일정(LCS 업데이트 설정을 통해) 생산 시작 날짜 |   서비스 종료   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.23     |      2021년 10월 15일       |        2021년 12월 10일          |                          2021년 12월 31일                           | 2022년 3월 18일     |
|     10.0.22     |      2021년 9월 3일      |        2021년 10월 22일           |                          2021년 11월 5일                            | 2022년 1월 14일   |


릴리스 예정일은 변경될 수 있습니다. 자세한 내용은 [서비스 업데이트 가용성](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json)을 참조하십시오.

|대상 버전 | 사용 가능성 미리 보기(PEAP) | 일반적으로 사용 가능(자체 업데이트) | 자동 업데이트 일정(LCS 업데이트 설정을 통해) 생산 시작 날짜 |   서비스 종료   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.24     |      2021년 12월 3일       |        2022년 1월 14일           |                          2020년 2월 4일                            | 2022년 4월 15일     |
|     10.0.25     |      2022년 1월 31일       |        2022년 3월 18일             |                          2022년 4월 1일                               | 2022년 6월 10일      |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
