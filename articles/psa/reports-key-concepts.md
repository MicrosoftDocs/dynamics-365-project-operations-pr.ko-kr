---
title: 주요 개념
description: 이 문서에서는 Project Service Automation에서 리소스 관리를 위한 주요 개념에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 41b13000ca17ec3a5d86fdb17885f09692d6f0c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921724"
---
# <a name="key-concepts"></a>주요 개념

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

다음 표는 Dynamics 365 Project Service Automation 앱에서 사용되는 주요 개념을 정의합니다.

| 개념                    | 정의 |
|----------------------------|------------|
| 프로젝트 팀원        | 프로젝트 팀의 일원으로서 프로젝트 팀원은 예약이 있는 명명된 리소스, 예약이 없는 명명된 리소스 또는 일반 리소스일 수 있습니다. 일반 리소스는 예약을 갖지 않으며 프로젝트에 로컬이고 프로젝트 전체에 걸친 능력 제약 조건은 없습니다. |
| 프로젝트 일반 리소스   | 팀을 형성하고 명명된 리소스를 알 필요 없이 프로젝트 계획에 충원할 수 있는 리소스 자리 표시자입니다. 프로젝트 캘린더는 일반 리소스의 캘린더로 사용됩니다. 일반 리소스를 프로젝트 팀에 추가하고 과업에 할당할 수 있습니다. |
| 예약된 시간 수               | 프로젝트 작업이 완료되도록 보장하기 위해 프로젝트에 대해 리소스 시간을 확정 예약합니다. 예약된 시간 수는 리소스의 전체 능력에서 소비됩니다. 예약은 일반 리소스가 아니라 명명된 리소스에만 해당합니다. |
| 할당된 시간 수             | 리소스 시간 수는 프로젝트 스케줄의 과업에 할당됩니다. 할당은 명명된 리소스 또는 일반 리소스에 대해 수행될 수 있습니다. 할당은 예약과 무관할 수 있습니다. |
| 요구되는 시간 수             | 요구되지만 명명된 리소스에 의해 아직 충족되지 않은 능력입니다. 요구되는 시간 수는 리소스 요건을 생성한 일반 팀원에만 관련이 있습니다. |
| 수요                     | 현재 및 들어오는 작업부하입니다. Project Service Automation에서 수요는 리소스 요건 또는 리소스 요청으로 표시됩니다. |
| 리소스 요구 사항       | 요구되는 리소스를 위해 요구되는 시간 수, 시작 및 종료 날짜, 기능, 지역 및 기타 가격 책정 차원을 포착하는 데 사용되는 엔터티입니다. 리소스 요건은 프로젝트 팀원에서 생성되거나 개별적으로 만들어집니다. |
| 리소스 요청           | 리소스 관리자가 수행해야 하는 리소스 요건을 수행하기 위해 "봉투"로 사용되는 엔터티입니다. |
| 리소스 기본 역할      | 활용도 계산을 위해 리소스가 그룹화되는 역할입니다. 리소스는 역할에 요구되는 기능을 가지고 있고 해당 역할에 대한 목표 활용도를 충족하는 것으로 간주됩니다. |
| 리소스 조직 단위 | 리소스가 배정된 조직 단위입니다. |
| 등고선                    | 과업, 요건 또는 할당 시간 수가 일일 분포로 세분화됩니다. 예컨대 5일, 40시간 과업은 5일에 걸친 하루 8시간으로 윤곽을 만들 수 있습니다. |
| 조정 보기        | 각 프로젝트 팀원의 예약 및 할당을 표시하는 보기입니다. 이 보기를 통해 프로젝트 관리자는 예약과 할당 사이의 불일치를 확인하고 불일치가 발생할 경우 시정 조치를 취할 수 있습니다. |
| 근무 시간                 | 리소스 능력과 작업 및 비작업 시간을 식별하는 데 사용되는 엔터티입니다. 이 엔터티를 리소스 캘린더라고도 합니다. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
