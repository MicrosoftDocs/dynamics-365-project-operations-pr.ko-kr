---
title: 프로젝트 템플릿 만들기
description: 프로젝트 템플릿을 만드는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080065"
---
# <a name="create-a-project-template-project-service"></a>프로젝트 템플릿 만들기(Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

프로젝트 템플릿을 사용하면 회사가 정기적으로 비슷한 종류의 프로젝트에 입찰 중일 때 시간을 절약할 수 있습니다. 프로젝트 템플릿은 표준 역할 집합 및 프로젝트의 유형에 대한 예상 시간을 제공합니다. 거래처 관리자와 프로젝트 관리자는 프로젝트 템플릿을 사용하여 프로젝트를 만들거나 템플릿을 복사하여 고유 템플릿을 만들 수 있습니다.  
  
## <a name="components-of-project-template"></a>프로젝트 템플릿의 구성 요소
 프로젝트 템플릿은 세 개의 구성 요소로 이루어집니다.  
  
- **작업 분할 구조** : 프로젝트 서식 파일의 작업 분할 구조는 프로젝트와 동일한 요소 집합을 가집니다. Gantt에서 작업 계층 구조를 만들고, 작업과 역할을 연결하고, 일정 특성을 정의하고, 모든 데이터의 종속성 및 보기를 설정할 수 있습니다. 프로젝트 템플릿의 작업 분할 구조는 각 작업에 대한 작업 모드도 지원합니다. 작업 일정을 만들 때 프로젝트 템플릿과 프로젝트는 차이점이 없습니다.  
  
- **프로젝트 추정** : 템플릿에서 프로젝트 예상은 프로젝트에서와 동일한 방식으로 작동합니다. 단, 비용 및 판매 가격의 기본 가격표는 항상 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 파라미터에서 정의된 기본 비용 및 판매 가격표입니다. 나머지 기능은 프로젝트에서와 같습니다.  
  
- **프로젝트 팀 구성** : 프로젝트 템플릿에 대한 프로젝트 팀을 구성하는 경우 템플릿의 명명된 리소스를 예약할 수 없습니다. 작업 분할 구조에서 **프로젝트 팀 생성** 을 사용하여 일반 리소스의 집합을 생성할 수 있습니다. 일반 리소스에 대해 필요한 기술 및 숙련도를 지정할 수도 있습니다. 프로젝트 템플릿에서 예약 가능한 자원으로 일반 자원을 대체할 수 없습니다.  
  
## <a name="create-a-project-from-a-template"></a>템플릿에서 프로젝트 만들기  
 다음과 같은 방법으로 템플릿에서 프로젝트를 만들 수 있습니다.  
  
-   견적에서 프로젝트를 만들 때 프로젝트 빨리 만들기 양식에서 프로젝트 템플릿을 선택할 수 있습니다.  
  
-   **새 프로젝트** 를 클릭하여 프로젝트를 만들 때, 레코드를 저장하기 전에 프로젝트 양식을 표시합니다. 여기에서 **템플릿 선택** 필드를 클릭하여 조직에 미리 정의된 프로젝트 템플릿의 목록에서 선택할 수 있습니다.  
  
-   **프로젝트 템플릿** 페이지의 **템플릿에서 프로젝트 만들기** 를 클릭하여 템플릿에서 프로젝트를 만듭니다.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>프로젝트에 템플릿의 구성 요소 복사  
 템플릿의 구성 요소를 프로젝트로 복사할 때 알아야 할 몇 가지 있습니다.  
  
 **작업 분할 구조 복사** : 프로젝트 템플릿에서 작업 분할 구조를 복사할 때, 프로젝트에 템플릿이 아닌 다른 프로젝트 달력이 있는 경우 프로젝트 달력의 작업 시간이 작업 일정에 적용됩니다. 일정이 지원 프로젝트 달력에 조정됩니다. 마찬가지로, 작업 분할 구조에서 첫 번째 작업 계층 구조는 프로젝트의 시작 날짜를 가지며, 작업 계층 구조의 나머지 일정은 템플릿의 작업 분할 구조에 지정된 기간 및 종속성에 따라 업데이트됩니다.  
  
 **프로젝트 예상 복사** : 프로젝트 예상 라인을 복사할 때, 가격표는 비용 가격표에 대한 프로젝트 및 판매 가격표에 대한 고객의 소유 단위에 따라 업데이트됩니다. 단가 및 판매 가격은 판매 엔터티에 연결된 프로젝트의 해당 가격표에서 결정됩니다.  
  
 **프로젝트 팀 복사** : 템플릿에서 프로젝트로 팀 프로젝트를 복사할 때 일반 자원은 템플릿에 정의된 기술 및 숙련도와 함께 복사됩니다. 일반 자원 배정은 프로젝트 템플릿에서와 같이 관리됩니다.  
  
### <a name="see-also"></a>참고 항목  
 [프로젝트 관리자 가이드](../psa/project-manager-guide.md)
