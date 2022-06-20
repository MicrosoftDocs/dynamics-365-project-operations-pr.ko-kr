---
title: 2021년 11월의 새로운 기능 - Project Operations Lite 배포
description: 이 문서에서는 Project Operations Lite 배포의 2021년 11월 릴리스에서 사용할 수 있는 품질 업데이트에 대한 정보를 제공합니다.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913812"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>2021년 11월의 새로운 기능 - Project Operations Lite 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 문서는 다음 구성 요소 및 Microsoft Dynamics 365 Project Operations 버전에 적용됩니다.

- Dataverse 환경 버전 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155의 Project Operations
  
## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

이 릴리스에는 다음과 같은 기능이 포함되어 있습니다.

- 프로젝트 일정 API(응용 프로그래밍 인터페이스)는 이제 프로젝트 버킷 생성 및 삭제 기능을 지원합니다.

## <a name="quality-updates"></a>품질 업데이트

### <a name="project-operations-in-dataverse"></a>Dataverse의 Project Operations

| 기능 영역 | 참조 번호 | 품질 업데이트 |
| --- | --- | --- |
| 청구 및 가격 책정 | 2358236 | 송장 수정은 영(0) 가격 라인이 있는 수정을 허용해야 합니다. |
| 리소스 관리 | 2410072 | 프로젝트 관리자로 작업에 할당된 리소스 설정을 허용합니다. |
| 청구 및 가격 책정 | 2430234 | 비용 성과 계산 문제를 해결합니다. |
| 시간 및 경비 | 2436978 | 시간을 hh:mm 형식으로 입력할 수 있습니다. |
| 청구 및 가격 책정 | 2448623 | 가격표가 조직 구성 단위와 연결된 후 업데이트되도록 허용합니다. |
| 시간 및 경비 | 2460396 | 셀을 지워서 시간 항목을 삭제할 수 있습니다. |
| 청구 및 가격 책정 | 2467386 | 작업이 낙찰된 견적과 연결된 경우에도 작업이 있는 프로젝트를 삭제할 수 있습니다. |
| 시간 및 경비 | 2461744 | **내 승인 실패** 보기에는 **제출됨** 스테이지의 프로젝트 승인만 포함됩니다. |
| 시간 및 경비 | 2464082 | 대상 상태가 일치하면 프로젝트 승인에서 승인 집합으로의 링크를 제거합니다. |
| 시간 및 경비 | 2468108 | 일정 작업은 승인 집합에 대한 **처리 중** 상태를 설정해서는 안 됩니다. |
| 시간 및 경비 | 2471503 | 7일이 지난 승인 집합을 삭제합니다. |
| 청구 및 가격 책정 | 2480687 | 견적 라인 이정표가 생성될 때 견적 라인 참조를 제거하면 안 됩니다. |
