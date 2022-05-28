---
title: Project Service Automation 통합 매개 변수
description: 이 항목에서는 Microsoft Dynamics 365 for Project Service Automation을 Microsoft Dynamics 365 Finance와 통합할 때 기본 데이터가 입력되는 방식을 구성하는 방법에 대해 설명합니다.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 70dcf44c0948bfb8f17c51e052b6c76e029d35fd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683684"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 통합 매개 변수

[!include[banner](../includes/banner.md)]

**Project Service Automation 통합 매개 변수** 페이지에서 Dynamics 365 Project Service Automation을 Dynamics 365 Finance와 통합할 때 기본 데이터가 입력되는 방식을 구성할 수 있습니다. Project Service Automation에서 Finance로 프로젝트를 성공적으로 동기화하려면 다음 필드를 설정해야 합니다.

**Project Service Automation 통합 매개 변수** 페이지를 열려면 **프로젝트 관리 및 회계** \> **설정** \> **Dynamics 365 for Project Service Automation 통합 매개 변수** 로 이동합니다. 

> [!NOTE]
> - 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.
> - 실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.


| 탭                    | 필드                | 설명 |
|------------------------|----------------------|-------------|
| 일반                | 기본 프로젝트 유형 | 기본 프로젝트 유형을 선택합니다. 프로젝트가 Project Service Automation에서 동기화될 때 통합 템플릿에 기본값을 제공하지 않은 경우 이 값이 사용됩니다. 동기화하는 동안 새 프로젝트의 **프로젝트 유형** 필드는 이 값으로 설정됩니다. 그러나 프로젝트 계약 내용이 Project Service Automation에서 동기화될 때 값이 업데이트될 수 있습니다. |
|                        | 시간 범주        | 기본 시간 범주를 선택합니다. 이 값은 시간 추정치가 Project Service Automation에서 동기화될 때 사용됩니다. 시간 추정치와 실제 시간이 Project Service Automation에서 동기화되면 Finance에서 새 프로젝트 예상 시간의 **범주** 필드가 이 값으로 설정됩니다. |
|                        | 요금 범주         | 기본 요금 범주를 선택합니다. 이 값은 실제 요금이 Project Service Automation에서 동기화될 때 사용됩니다. 실제 요금이 Project Service Automation에서 동기화되면 Finance에서 새 요금 트랜잭션의 **범주** 필드가 이 값으로 설정됩니다. |
| 프로젝트 그룹 기본값 | 프로젝트 형식         | **새로 만들기** 를 클릭하여 기본 프로젝트 그룹을 설정할 프로젝트 유형을 선택할 수 있는 행을 추가합니다. 특정 프로젝트 유형은 구성에서 한 번만 선택할 수 있습니다. |
|                        | 프로젝트 그룹        | 선택한 프로젝트 유형에 대한 기본 프로젝트 그룹을 선택합니다. 새 프로젝트가 Project Service Automation에서 동기화되면 통합 템플릿에 기본값을 제공하지 않은 경우 **프로젝트 그룹** 필드는 프로젝트 유형의 기본값으로 설정됩니다. |
| 청구 유형 기본값  | 청구 유형         | **새로 만들기** 를 클릭하여 기본 라인 속성을 설정할 청구 유형을 선택할 수 있는 행을 추가합니다. 특정 청구 유형은 구성에서 한 번만 선택할 수 있습니다. |
|                        | 라인 속성        | 선택한 청구 유형에 대한 기본 라인 속성을 선택합니다. 새 시간 추정치, 새 경비 추정치 또는 새 실제가 Project Service Automation에서 동기화되면 **라인 속성** 필드는 청구 유형의 기본값으로 설정됩니다. |
| 기능 잠금  | 해당 없음       | Project Service Automation에서 시작된 프로젝트 및 계약에 대해 Finance에서 비활성화할 기능을 선택합니다. 예를 들어 계약 및 프로젝트를 편집하고, 작업 분할 구조를 만들고, Finance에서 작업 표를 입력하는 기능을 끌 수 있습니다. 회계 관련 필드는 매개 변수 설정에서 사용할 수 없는 경우에도 계속 활성화됩니다. 기본적으로 모든 기능이 활성화됩니다. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]