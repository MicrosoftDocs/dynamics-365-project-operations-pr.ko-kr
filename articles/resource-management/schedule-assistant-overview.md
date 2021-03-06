---
title: 일정 도우미 보기
description: 이 항목은 일정 도우미를 사용하여 리소스를 예약하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908332"
---
# <a name="schedule-assistant-overview"></a>일정 도우미 보기

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

일정 도우미는 프로젝트 관리자가 정의한 요구 사항에 따라 리소스를 예약하는 데 사용됩니다. 일정 도우미는 리소스 요구 사항에 제공된 매개 변수를 사용하여 리소스를 찾습니다. 일정 도우미는 필요한 시간 창이나 기술과 같은 관련 요구 사항과 일치하는 리소스를 추천합니다.

적절한 리소스가 식별되면 리소스 또는 프로젝트 관리자가 리소스를 작업에 예약할 수 있습니다.

## <a name="prerequisites"></a>필수 구성 요소

일정 도우미는 Universal Resource Scheduling 솔루션의 일부입니다. 이 솔루션은 Dynamics 365 Project Operations, Dynamics 365 Field Service, Dynamics 365 Customer Service에 포함되어 설치됩니다.

## <a name="matching-requirements-and-resources"></a>일치하는 요구 사항 및 리소스

생성된 리소스 요구 사항은 다음과 같은 세부 정보를 기반으로 합니다.

-   특징
-   역할
-   사업부
-   리소스 선호 설정
-   작업량 윤곽
-   표준 시간대

일정 도우미는 이러한 세부 정보를 사용하여 리소스를 필터링합니다.

## <a name="launch-the-schedule-assistant"></a>일정 도우미 시작

일정 도우미를 시작하는 방법에는 두 가지가 있습니다. 하이브리드 모드를 사용하는 경우 팀 구성원 표에서 충족되지 않은 리소스 요구 사항이 있는 팀 구성원을 선택한 다음 **예약**을 선택합니다. 중앙 모드를 사용하는 경우 리소스 관리자가 리소스를 찾아 선택합니다.

## <a name="schedule-assistant-filters"></a>일정 도우미 필터

일정 도우미가 실행된 후 리소스 요구 사항의 세부 정보가 왼쪽 창에 필터링된 값으로 표시됩니다. 리소스 관리자 또는 프로젝트 관리자는 일정 요구 사항을 충족하도록 필터를 조정하여 결과를 미세 조정할 수 있습니다.

필터 창에는 다음과 같은 작업 관련 옵션이 표시됩니다.

-   작업 시작 및 종료
-   특징
-   역할
-   조직 구성 단위
-   리소싱 회사
-   리소스 유형
-   선호 리소스
