---
title: 프로젝트 일정 정의
description: 이 항목은 프로젝트 캘린더를 사용하여 프로젝트 일정을 추적하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080226"
---
# <a name="define-project-calendars"></a>프로젝트 일정 정의

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

프로젝트 스케줄을 생성하려면 일당 작업 시간 수와 휴무를 정의하는 프로젝트 캘린더 템플릿을 생성합니다. 프로젝트 캘린더 템플릿을 생성하려면 프로젝트를 위한 **Calendar 캘린더 템플릿** 필드와 작업 템플릿을 연계합니다. 다음 단계에 따라 작업 템플릿을 만드십시오.

1. 왼쪽 탐색 창에서 **리소스** 를 선택합니다. 
2. **리소스** 목록 페이지에서 사용자 레코드를 연 다음 **작업 시간 수 표시** 를 선택합니다.

  > [!NOTE]
  > 브라우저 페이지에서 팝업을 허용해야 합니다. 이렇게 하면 리소스에 대해 설정된 작업 시간 수를 볼 수 있습니다.
  
3. **월별 보기** 탭에서 **설정** 을 선택합니다. 세 가지 옵션의 목록이 나타납니다: 

  - 새 주별 일정
  - 하루 작업 일정
  - 휴가

4. **새 주별 스케줄** 을 선택한 다음 이 리소스 스케줄에 대한 옵션을 설정합니다. 되풀이되는 주간 일정, 일일 시간 파라미터, 휴무 등을 설정할 수 있습니다.
5. 날짜 범위를 설정하고 **저장** 을 선택한 다음 **닫기** 를 선택합니다. 
6. **리소스** 목록 페이지로 돌아가서 작업 시간을 설정한 리소스를 선택합니다. 
7. **캘린더를 설정** 을 선택하여 작업 템플릿을 설정합니다. 
8. **작업 템플릿** 대화 상자에서 작업 템플릿의 명칭을 입력한 다음 **적용** 을 선택합니다. 

이제 작업 템플릿을 프로젝트 스케줄 템플릿과 연계할 수 있습니다.
