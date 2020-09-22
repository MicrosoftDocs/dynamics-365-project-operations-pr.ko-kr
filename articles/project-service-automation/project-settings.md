---
title: 프로젝트 설정
description: 이 항목은 프로젝트 관리 설정에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753251"
---
# <a name="project-settings"></a>프로젝트 설정

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

다음 설정을 사용하여 프로젝트 계획 기능에 액세스합니다.

## <a name="work-template"></a>작업 템플릿

프로젝트 스케줄을 생성하려면 일당 작업 시간 수와 휴무를 정의하는 프로젝트 캘린더 템플릿을 생성합니다. 프로젝트 캘린더 템플릿을 생성하려면 프로젝트를 위한 **Calendar 캘린더 템플릿** 필드와 작업 템플릿을 연계합니다. 다음 단계에 따라 작업 템플릿을 만드십시오.

1. PSA의 왼쪽 탐색 창에서 **리소스**를 클릭합니다. 
2. **리소스** 목록 페이지에서 사용자 레코드를 연 다음 **작업 시간 수 표시**를 선택합니다.

  > [!NOTE]
  > 브라우저 페이지에서 팝업을 허용해야 합니다. 이렇게 하면 리소스에 대해 설정된 작업 시간 수를 볼 수 있습니다.
  
3. **월별 보기** 탭에서 **설정**을 클릭합니다. 세 가지 옵션의 목록이 나타납니다: 

  - 새 주별 스케줄
  - 하루 작업 스케줄
  - 휴가

> ![옵션 설정](media/project-13.png)

4. **새 주별 스케줄**을 선택한 다음 이 리소스 스케줄에 대한 옵션을 설정합니다. 되풀이되는 주간 일정, 일일 시간 파라미터, 휴무 등을 설정할 수 있습니다.
5. 날짜 범위를 설정하고 **저장**을 선택한 다음 **닫기**를 클릭합니다. 
6. **리소스** 목록 페이지로 돌아가서 작업 시간을 설정한 리소스를 선택합니다. 
7. **캘린더를 설정**을 선택하여 작업 템플릿을 설정합니다. 
8. **작업 템플릿** 대화 상자에서 작업 템플릿의 명칭을 입력한 다음 **적용**을 선택합니다. 

이제 작업 템플릿을 프로젝트 스케줄 템플릿과 연계할 수 있습니다.

## <a name="resource-roles"></a>리소스 역할

*리소스 역할*이라는 용어는 사람이 프로젝트에서 특정 작업 집합을 수행해야 하는 기능, 역량 및 자격증 집합을 나타냅니다. PSA를 사용하면 리소스가 연계된 역할에 근거한 리소스의 시간 비용을 추산하여 청구할 수 있습니다. 모든 조직은 **Project Service** 메뉴에서 왼쪽 탐색을 사용하여 이러한 역할을 설정해야 합니다.

모든 조직은 **활성 리소스 카테고리** 페이지에서 이러한 역할을 설정해야 합니다. 이 페이지를 열려면 왼쪽 탐색 창에서 **리소스 역할**을 선택합니다.

## <a name="price-lists"></a>가격표

가격표에서 조직에서의 리소스 역할, 경비 카테고리, 제품 및 기타 요소를 위한 원가와 판매 가격을 설정할 수 있습니다. 프로젝트를 위해 인도해야 하는 작업의 재무 추산을 설정하기 전에 증빙 원가와 판매 가격표를 생성해야 합니다. 파라미터 섹션에서 조직에서 만든 모든 프로젝트에 적용되는 기본 원가 및 판매 가격표도 설정해야 합니다. **활성 프로젝트 파라미터** 페이지에서 기본 원가 및 판매 가격표를 설정해야 합니다.
