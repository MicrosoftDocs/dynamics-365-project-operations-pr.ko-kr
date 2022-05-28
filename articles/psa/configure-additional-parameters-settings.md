---
title: 추가 파라미터 설정 구성
description: 추가 파라미터를 구성하는 방법(Project Service)
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 0ceaa3af630df132339895a8497e49daf2e102c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592332"
---
# <a name="configure-additional-parameter-settings-project-service"></a>추가 파라미터 구성(Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

이전 토픽에서 항목을 구성하고 나면 프로젝트에 사용할 추가 프로젝트 파라미터를 설정해야 합니다. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 처음 설치하면 파라미터 설정을 만들어 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]가 작동하기 위해 필요한 모든 레코드를 먼저 만들어야 합니다. 이제 다시 앞으로 돌아가 해당 설정에 대한 추가 필드를 구성해야 합니다.  
  
 다음과 같은 설정을 구성해야 합니다.  
  
-   조직 구성 단위  
  
-   송장 빈도  
  
-   근무 시간 템플릿  
  
-   가격표  
 
이 단계에서 원하는 리소스 할당 유형 또한 표시할 수 있습니다.  
  
- **중앙**. 리소스 관리자만 프로젝트에 리소스를 할당할 수 있습니다.  
  
- **혼합**. 자원 관리자, 프로젝트 관리자 및 거래처 관리자가 프로젝트에 리소스를 할당할 수 있습니다.  
  
 
프로젝트 파라미터를 설정하려면  
  
1. **Project Service > 파라미터** 로 이동합니다.  
  
2. (처음 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]를 설치할 때 만든) 구성하려는 파라미터 설정을 클릭하거나 **새로 만들기** 를 클릭하여 새로 만듭니다.  
  
3. **일반** 영역에서 프로젝트 파라미터에 대한 모든 옵션을 설정합니다.  
  
4. **가격표 영역** 에서 **+** 를 클릭하여 가격표를 추가하고, **프로젝트 파라미터 가격표** 드롭다운 목록에서 가격표를 선택한 다음 **저장** 을 클릭합니다.  
  
5. 화면 오른쪽 아래 모서리에서 **저장** 단추를 클릭합니다.  

> [!NOTE]
> 올바르게 작동하려면 Project Service에 대해 프로젝트 매개 변수 레코드를 유지해야 합니다. 이 레코드는 삭제하면 안 됩니다.

### <a name="see-also"></a>참고 항목  
 [리소스 설정](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
