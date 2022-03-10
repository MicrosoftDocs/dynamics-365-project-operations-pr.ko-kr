---
title: 프로젝트에 리소스 예약
description: 프로젝트에 대한 리소스 일정을 예약하는 방법(Project Service)
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 7beb1f86795a909a1266b2a2c97421e1f04ef3c4cf2f9b49413cd1382b0f2011
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998154"
---
# <a name="schedule-resources-for-a-project-project-service"></a>프로젝트에 대한 리소스 일정 예약(Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

리소스 사용 가능 여부를 확인하여 예약된 리소스 상태를 전부 보거나, 보기를 기술, 팀, 위치 및 기타 옵션으로 필터링할 수 있습니다.  
  
일정 게시판에는 리소스 및 사용 가능 여부에 대한 목록이 표시됩니다. **시간**, **일**, **주**, 또는 **월** 로 사용 가능성을 표시하도록 보기 모드를 선택합니다.  
  
일정 게시판을 사용하기 전에 설정하는 것이 중요합니다. 자세한 내용은 [일정 보드 구성(Field Service 또는 Project Service Automation)](/dynamics365/field-service/configure-schedule-board)을 참조하십시오.
  
이전 버전을 사용 중인 경우 리소스 사용 가능 시간에 대해 [리소스 사용 가능한 시간 보기](../psa/view-resource-availability.md)를 참조하십시오.  

> [!IMPORTANT]
>  일정 게시판 예약 기능, 지역 코드 입력, 위치 서비스를 사용하려면 지도를 사용하도록 설정해야 합니다.  
> 
> 1. 메인 메뉴에서 **리소스 예약** > **관리** 를 선택합니다.  
> 2. **예약 파라미터** 를 클릭합니다.  
> 3. 레코드를 열고 **Resource Scheduling Optimization** 섹션으로 아래로 스크롤합니다.  
> 4. **지도에 연결** 필드에서 **예** 를 선택합니다.  
> 5. 약관에 동의하고 레코드를 저장합니다.  
> 6. 메인 메뉴에서 **Project Service** > **일정 게시판** 을 선택합니다. 여기에서 예약 요구 사항을 수동으로 예약하는 방법이 여러 가지가 있습니다. 사용자에게 맞는 방법을 선택하세요.
  
## <a name="find-available-resources"></a>사용 가능한 리소스 찾기

1.  **예약 요구 사항** 목록에서 예약되지 않은 예약을 마우스 오른쪽 단추로 클릭하고 다음 중 하나를 선택합니다.  
  
- **사용 가능성 찾기 - 현재 리소스** 를 선택하여 일정 게시판의 목록에서 사용 가능한 리소스를 찾습니다.  
- **사용 가능성 찾기 - 모든 리소스** 를 선택하여 시스템의 리소스 목록에서 사용 가능한 리소스를 찾습니다.  
   > [!NOTE]
   >  이렇게 하면 필터링을 통해 선택한 예약 요구 사항에 대한 옵션이 표시됩니다.  
  
2. 일정 게시판에서 타임 슬롯 중 사용 가능한 슬롯을 마우스 오른쪽 단추로 클릭하고 **여기에서 예약** 을 선택합니다. 또는 예약 요구 사항을 사용 가능한 시간 슬롯에 끌어 놓습니다.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>일별 보기를 사용하여 리소스를 예약하고 예약이 덜 된 리소스 찾기
  
1.  일정 게시판에서 **보기 모드** 를 선택하고 **일** 을 선택합니다.  
  
    리소스가 하루에 몇 시간 예약됐는지 그리고 여유 있는 날짜를 나타내는 표 보기가 표시됩니다.  
  
2.  예약을 원하는 리소스를 누른 다음 **예약** 을 선택합니다.  
  
3.  **리소스 예약(만들기)** 대화 상자에서 리소스를 예약하고자 하는 프로젝트와 예약 방법, 시작 및 종료 시각을 선택합니다.  
  
4.  완료되면 **예약** 을 선택합니다.  
  
## <a name="view-to-the-schedule-board"></a>일정 게시판 보기
  
1.  하단의 목록에서 예약되지 않은 예약 요구 사항을 선택합니다.  
  
2.  예약 보드의 사용 가능한 리소스/시간 슬롯으로 예약 요구 사항을 끌어 놓습니다.  
  
3.  완료되면 **예약** 을 선택합니다.  
  
### <a name="additional-resources"></a>추가 리소스  
 [리소스 관리자 가이드](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]