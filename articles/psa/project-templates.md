---
title: 프로젝트 템플릿
description: 이 항목은 빠른 프로젝트 설정을 위해 프로젝트 템플릿을 사용하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: aff6fc5bb855fe1e9007933fdc1a88eb020da0ad
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586030"
---
# <a name="project-templates"></a>프로젝트 템플릿 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

프로젝트 템플릿은 프로젝트를 빠르고 쉽게 시작하는 데 도움이 되는 사전 정의된 틀입니다. 사전 정의된 템플릿을 사용하여 한 번의 클릭으로 새 프로젝트를 만들 수 있습니다. 프로젝트의 경우 프로젝트 템플릿의 필수 구성 조건을 정의해야 합니다. 각 프로젝트 템플릿에 대한 프로젝트 스케줄을 정의해야 하며 템플릿의 구성 요소에 유용한 데이터가 있도록 조직에서 역할 및 가격 목록을 사전 정의해야 합니다.

프로젝트 템플릿은 스케줄, 프로젝트 추산 및 프로젝트 팀원의 세 가지 구성 요소로 구성됩니다.

## <a name="schedule"></a>일정

프로젝트 템플릿의 스케줄은 프로젝트의 스케줄과 동일한 요소 집합을 갖습니다. 귀하는 과업 계층 구조를 만들고, 역할을 과업과 연계하고, 스케줄 속성을 정의하고, 종속성을 설정할 수 있습니다. 프로젝트 템플릿의 스케줄은 각 과업에 대한 과업 모드도 지원합니다. 따라서 그것은 스케줄링 엔진을 지원합니다. 프로젝트 캘린더를 프로젝트와 연계해야 합니다. 작업 스케줄을 만들 때 프로젝트 템플릿과 프로젝트 사이에 차이는 없습니다.

## <a name="project-estimates"></a>프로젝트 추산

프로젝트 템플릿에서 프로젝트 추산은 프로젝트에서 프로젝트 추산과 동일한 방식으로 작동합니다. 그러나 원가 및 판매 가격은 이 파라미터들에 정의된 기본 원가 및 판매 가격 목록에서 가져온 값입니다.

## <a name="creating-a-project-from-a-template"></a>템플릿에서 프로젝트 만들기
 
프로젝트 템플릿에서 프로젝트를 만드는 방법에는 여러 가지가 있습니다:

- 견적에서 프로젝트를 만들 때, **빠른 생성: 프로젝트** 대화 상자에서 프로젝트 템플릿을 선택할 수 있습니다.

> ![빠른 생성: 프로젝트 대화 상자.](media/project-11.png)

- **새 프로젝트** 를 선택하여 프로젝트를 만들 때, **프로젝트** 페이지가 나타나면 레코드를 저장합니다. **템플릿 선택** 필드에서 조직에서 사전 정의된 프로젝트 템플릿 중 하나를 선택합니다.
- **템플릿 엔터티** 페이지에서 **템플릿에서 프로젝트 만들기** 를 사용합니다.

## <a name="copying-components-of-template-to-project"></a>프로젝트에 템플릿의 구성 요소 복사

프로젝트 템플릿의 구성 요소를 프로젝트에 복사하면 프로젝트의 설정에 따라 몇 가지 재정의가 발생할 수 있습니다.

### <a name="copying-the-schedule"></a>스케줄 복사

프로젝트 템플릿에서 스케줄을 복사할 때, 프로젝트에 템플릿이 아닌 다른 프로젝트 캘린더가 있는 경우, 프로젝트 캘린더의 작업 시간 수가 작업 스케줄에 적용됩니다. 이런 식으로 스케줄이 지원 프로젝트 캘린더에 일치하도록 조정됩니다. 마찬가지로, 스케줄의 첫 번째 과업이 프로젝트의 시작 날짜를 취하며, 나머지 계층의 스케줄은 템플릿에 지정된 기간 및 종속성에 근거하여 업데이트됩니다. 

### <a name="copying-project-estimates"></a>프로젝트 추산 복사 

프로젝트 추산 행을 복사하면 가격표가 업데이트됩니다. 원가표의 경우 이러한 업데이트는 프로젝트의 소유 단위에 근거합니다. 판매 가격표의 경우 고객에 근거합니다. 판매 엔터티와 연계된 프로젝트의 경우, 단가 및 판매 가격은 해당 가격표에 근거하여 결정됩니다.

### <a name="copying-a-project-team"></a>프로젝트 팀 복사

프로젝트 템플릿에서 프로젝트 팀을 어떤 프로젝트에 복사할 때, 일반 리소스가 템플릿에 정의된 기능 및 숙련도와 함께 복사됩니다. 일반 리소스 배정은 프로젝트 템플릿에서와 같이 관리됩니다. 명명된 리소스는 프로젝트 템플릿에서 지원되지 않습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
