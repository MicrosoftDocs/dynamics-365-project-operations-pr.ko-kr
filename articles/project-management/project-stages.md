---
title: 프로젝트 스테이지
description: 이 항목은 Microsoft Dynamics Project Operations에서 사용할 수 있는 프로젝트 스테이지에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286796"
---
# <a name="project-stages"></a>프로젝트 스테이지

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

프로젝트 단계는 프로젝트가 진행됨에 따라 프로젝트의 상태를 반영하도록 설계되었습니다. 사용자 지정을 사용하여 비즈니스 프로세스 흐름, Power Automate 또는 플러그인 확장으로 단계를 자동으로 업데이트할 수 있습니다.

다음 단계는 기본 비즈니스 프로세스 흐름에 정의되어 있습니다:

- 최신
- 견적
- 계획
- 배송
- 완료됨
- 종료 

## <a name="new"></a>최신

프로젝트 생성 시 프로젝트 단계는 **신규** 로 설정됩니다. 템플릿에서 프로젝트를 만든 경우 스케줄, 추산 및 팀 데이터가 있을 수 있습니다. 그렇지 않으면 그것은 프로젝트의 개요일 뿐이며 나머지 구성 요소를 입력해야 합니다.

## <a name="quote"></a>견적

프로젝트를 견적과 연계하거나 견적에서 프로젝트를 만들 경우, 프로젝트 단계는 **견적** 으로 설정되며 예상 시작 및 종료 날짜도 업데이트됩니다. 프로젝트가 **견적** 단계에 있는 동안 **프로젝트 엔터티** 페이지의 **판매** 탭은 견적 내역을 표시합니다.

## <a name="plan"></a>계획

프로젝트와 연계된 견적을 따서 프로젝트가 **계약** 단계로 이동한 경우, 프로젝트 단계는 **계획** 으로 업데이트됩니다. 프로젝트가 **계획** 단계에 있는 동안 **프로젝트 엔터티** 페이지는 계약 내역을 표시합니다.

## <a name="deliver"></a>인도

프로젝트 계획이 완료되어 귀하가 프로젝트를 시작할 준비가 되면 프로젝트 관리자는 프로젝트 단계를 **인도** 로 업데이트하여 프로젝트가 시작되었음을 표시해야 합니다.

## <a name="complete"></a>완료 

프로젝트를 위한 작업이 완료되면 프로젝트 관리자는 그 단계를 **완료** 로 업데이트할 수 있습니다. 프로젝트 단계를 **완료** 로 업데이트함으로써 프로젝트 관리자는 작업이 100% 완료되었지만 프로젝트가 미결로 유지되어 미결 시간 또는 경비 항목을 기록할 수 있음을 나타냅니다.

## <a name="close"></a>닫기

모든 처리가 기록되면 프로젝트 관리자는 그 단계를 **종결** 로 업데이트할 수 있습니다. 그 시점에서는 처리를 기록할 수 없으며 프로젝트는 읽기 전용으로 설정됩니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]