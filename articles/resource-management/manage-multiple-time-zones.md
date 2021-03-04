---
title: 표준 시간대 관리
description: 프로젝트가 생성될 때 시간대는 적용된 근무 시간 템플릿에 정의된 시간대를 기반으로 합니다.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119831"
---
# <a name="manage-time-zones"></a>표준 시간대 관리

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


## <a name="projects"></a>프로젝트

프로젝트가 생성될 때 시간대는 적용된 근무 시간 템플릿에 정의된 시간대를 기반으로 합니다. **프로젝트** 에서 날짜는 항상 **작업** 탭을 제외하고 각 탭에 로그인한 사용자의 표준 시간대를 기준으로 합니다. 작업 분할 구조를 볼 때 날짜는 항상 프로젝트의 시간대로 표시됩니다.

## <a name="tasks"></a>작업

작업이 생성되면 시작 시간, 종료 시간 및 시간/일은 프로젝트의 작업 시간에 의해 제어됩니다. 예를 들어 시간대가 -8 PST이고 근무 시간이 월요일 ~ 금요일 오전 9시 ~ 오후 5시인 프로젝트로 작업이 생성된 경우 할당없이 생성된 모든 작업은 시작 시간과 프로젝트 일정의 종료 시간을 준수합니다.

## <a name="manage-resources-with-time-zones"></a>표준 시간대로 리소스 관리

**예약 연장** 사용시 정확하고 예측 가능한 결과를 위해 충족해야 하는 두 가지 주요 전제 조건이 있습니다.  

- 사용자는 시스템의 **개인화 설정** 에 정의된 표준 시간대와 일치하도록 장치의 시간대를 구성해야 합니다.
 
  ![Windows 10의 시간대 설정](media/reconcile-assignments-03.png)

  ![개인 맞춤 설정의 시간대 설정](media/reconcile-assignments-04.png)
 
- 예약 가능한 리소스에는 요청된 확장을 정의하는 데 사용되는 배분과 겹치는 최소 1분의 작업 시간이 있어야 합니다. 예를 들어 근무 시간이 오전 9시에서 오후 7시 사이인 다음 리소스가 있습니다. 

  ![리소스 배분 비교](media/reconcile-assignments-05.png)

아래 표는 다음을 보여줍니다.

- 프로젝트 일정 템플릿
- 리소스 A :이 리소스는 일정이 같고 프로젝트와 동일한 시간대에 있습니다. 예약 시작 시간은 오전 9시입니다.
- 리소스 B: 이 리소스는 프로젝트와 다른 표준 시간대에 있으며 해당 표준 시간대의 오전 7시에 시작됩니다. 그러나 예약은 할당 배분의 가장 빠른 시작 시간이므로 오전 9시에 시작됩니다.
- 리소스 C 및 D: 리소스는 둘 모두 프로젝트와 서로 다른 표준 시간대에 있으며 예약은 사용 가능한 시작 시간보다 일찍 시작되지 않습니다.

|엔터티  |달력  |
|-|-|
|프로젝트 일정 템플릿   | ![프로젝트 일정](media/reconcile-assignments-06.png) |
|리소스 A  | ![리소스 A 일정](media/reconcile-assignments-06.png) |
|리소스 B  |  ![리소스 B 일정](media/reconcile-assignments-07.png) |
|리소스 C  |  ![리소스 C 일정](media/reconcile-assignments-08.png) |
|리소스 D  | ![리소스 D 일정](media/reconcile-assignments-09.png)  |
 
**조정** 보기로 이동할 때 리소스 할당 및 연관된 예약 부족이 표시됩니다.

![확장 전 조정 보기](media/reconcile-assignments-10.png)

각 리소스에 대해 예약 연장 기능이 사용된 후 각 리소스의 작업 시간이 부족의 윤곽과 겹치기 때문에 각 리소스에 대한 예약이 성공적으로 확장됩니다.

![예약 확장 후 조정 보기](media/reconcile-assignments-11.png) 

예약 세부 정보를 자세히 살펴보면 예약 시작 시간에 차이가 있음을 알 수 있습니다. 예약은 할당 윤곽의 시작 시간 이전에 시작되지 않고 리소스의 사용 가능한 시작 시간 이전에 시작되지 않습니다.

![일정 게시판에서 리소스의 새로운 예약](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]