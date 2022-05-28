---
title: Project Operations 이중 쓰기 통합
description: 이 항목은 Project Operations 이중 쓰기 통합에 대한 개요를 제공합니다.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582764"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations 이중 쓰기 통합 개요

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Project Operations는 [이중 쓰기 기능](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)을 사용하여 Microsoft Dataverse 및 Dynamics 365 Finance에서 데이터를 동기화합니다.

다음 그림은 Dataverse와 Finance 간의 통합의 일부로 데이터가 동기화되는 방식을 보여줍니다.

![Project Operations 데이터 흐름 개요.](./media/ProjectOperationsFlows.jpg)

Dataverse의 Project Operations는 최신 사용자 인터페이스(UI)와 Power Platform 기능을 사용하여 코드가 없는 간편한/낮은 코드 확장성을 제공합니다. 프로젝트 관리자, 리소스 관리자, 프로젝트 팀 구성원 및 기타 프론트 오피스 페르소나는 Dataverse에서 Project Operations에서 활동을 수행합니다.

Finance의 Project Operations는 프로젝트 회계 및 수익 인식 지원을 제공합니다. Project Operations는 판매세 계산, 환율, 재무 차원 보고 등을 위해 Finance의 재무 프레임워크에 연결됩니다. 프로젝트 회계사 경험은 대부분 Finance를 기반으로 합니다.

Project Operations는 다음 구성 요소 통합으로 구성됩니다.


- [Project Operations 설정 및 구성 데이터 통합](resource-dual-write-setup-integration.md) 
- [프로젝트 추정 및 실제](resource-dual-write-estimates-actuals.md)
- [프로젝트 송장](resource-dual-write-project-invoice.md)
- [경비 관리](resource-dual-write-expense.md)
- [공급업체 송장](resource-dual-write-vendor-invoice.md)
