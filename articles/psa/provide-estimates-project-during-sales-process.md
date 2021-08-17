---
title: 영업 프로세스 중에 프로젝트에 대한 작업 추정 제공
description: 영업 프로세스 중에 프로젝트에 대한 추정을 제공하는 방법(Project Service)
author: ruhercul
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
ms.openlocfilehash: acb1e5f598e3e057be78a70bc4f5c66c510053a08f4efb0a1595cf4853171662
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002474"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>영업 프로세스 중에 프로젝트에 대한 작업 추정 제공(Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

영업 과정 중에 견적 내용으로 처음부터 영업 예상을 산출할 수 있습니다. [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]의 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 기능은 작업 분할 구조에서 프로젝트에 대한 추정에 기여하는 작업 항목 분할 및 관련 특성 연결을 통해 영업 예상 결과를 보다 과학적이고 확실하게 제공합니다.  
  
 영업에 성공하면, 프로젝트의 성공적인 완료에 필요한 대로 변경하여 관련 작업 분할 구조를 프로젝트 계획에 사용할 수 있습니다.  
  
## <a name="link-a-project-to-a-quote-line"></a>프로젝트를 견적 내용에 연결  
 프로젝트 기반 견적 내용을 만들 때, 견적 내용에서 새 프로젝트를 만들 수 있습니다. 그런 다음, 미리 구성된 표준 프로젝트 계획 및 조직에서 일반적으로 사용되는 경비 추정 또는 과거 프로젝트에서 산출한 프로젝트 계획 및 추정 사본인 프로젝트 템플릿을 사용할 수 있습니다. 프로젝트를 만들 때, 프로젝트 템플릿을 선택하여 프로젝트 계획, 추정, 역할 요구 사항을 변경하는 기준을 사용할 수 있습니다. 견적에서 프로젝트를 만들면 프로젝트가 견적 내용에 자동으로 연결됩니다.  
  
## <a name="project-estimate-components"></a>프로젝트 추정 구성 요소  
 프로젝트의 작업 분할 구조는 작업을 업무 단위로 나누고, 업무의 계층 구조를 관리하며, 각 업무 완료에 필요한 예상 작업량을 할당하는 방법을 제공합니다. 또한 업무에 역할을 연결하여 업무 및 일정 완료에 필요한 리소스 유형 추정을 표시할 수 있습니다.  
  
 작업 분할 구조를 사용하면 작업량을 정하고 예상 일정을 짜는 데 도움이 됩니다. 기본적으로 프로젝트는 앞서 정의한 기본 가격표를 사용합니다. 가격표에 정의된 비용 및 영업 가격은 프로젝트 작업 분할에 대한 예상 비용을 정하는 데 도움이 됩니다.  
  
 프로젝트가 견적에 연결되고 견적의 가격표가 기본과 다를 경우, 견적의 가격표가 재무 추정에 사용됩니다.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>프로젝트에서 견적으로 추정 가져오기  
 프로젝트에서 프로젝트 추정을 확보하면 이것을 견적 내용으로 가져올 수 있습니다.  
  
-   **견적 내용 상세** 에서 **추정에서 가져오기** 를 클릭합니다. 

-   거래 유형, 역할 또는 작업 분할 구조 노드 수준별로 요약된 프로젝트 추정을 선택할 수 있습니다.  
  
### <a name="see-also"></a>참고 항목  
 [프로젝트 관리자 가이드](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]