---
title: 프로젝트 견적 만들기
description: 프로젝트 견적을 만드는 방법(Project Service)
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5a28bafed6fa76e21e3edb890da04f105b2b2a3c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133151"
---
# <a name="create-a-project-quote-project-service"></a>프로젝트 견적 만들기(Project Service )

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

견적 만들기는 영업 기회 만들기와 비슷합니다. 영업 기회는 내부 참조용이지만, 견적은 잠재적인 고객에게 보내는 것입니다. 각 영업 기회에 대해 여러 견적을 만들 수 있습니다. 프로젝트의 **제안** 단계에서 잠재적인 고객에게 보낼 견적을 만듭니다.  
  
1. 영업 기회에서 견적을 만들려면, **Project Service > 영업 기회** 로 이동한 후 견적을 만들려는 영업 기회를 클릭합니다.  
  
2. 진행률 표시줄 오른쪽의 **다음 단계** 를 클릭한 후 기존 견적을 선택하거나 **만들기** 를 클릭하여 새 견적을 만듭니다.  
  
3. **요약** 영역에서 필요에 따라 정보를 변경합니다.  
  
4. **저장** 을 클릭하여 견적을 만들면 계속 편집할 수 있습니다.  
  
5. 견적에 제품을 추가하려면 **견적 내용** 영역의 **제품 기반 내용** 아래에 있는 **새로 만들기** 를 클릭합니다. **제품 이름** 아래 항목을 선택한 다음 수량, 영업 가격 및 견적 총액을 지정합니다.  
  
6. 견적에 프로젝트 예상을 추가하려면 **견적 내용** 영역의 **제품 기반 내용** 아래에 있는 **+** 를 클릭합니다. 가능한 경우 이름, 예산 총액 및 프로젝트를 입력합니다. 작업 분할 구조로 프로젝트를 만들어 예상을 생성해야 할 경우 [프로젝트 만들기](../psa/create-project.md)를 참조하십시오.  
  
7. 편집을 마쳤으면, 화면 우측 하단의 **저장** 단추를 클릭합니다.  
  
8. 견적을 고객에게 보낼 준비가 되면, **더 보기**(...)를 클릭하고 **보고서 실행** 을 클릭한 다음 **견적** 을 클릭합니다. [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] 문서로 보고서를 저장하고 필요한 경우 편집한 다음 견적을 고객에게 보냅니다.  
  
9. 고객이 견적을 수락하면 **견적** 화면 상단의 **성공으로 닫기** 를 클릭합니다. 고객이 일부 항목에 대한 변경을 원할 경우, 전체 프로세스를 다시 수행하여 새 견적을 만듭니다. 고객이 지금 서비스를 사용하지 않기로 결정할 경우, **견적** 화면 상단의 **실패로 닫기** 를 클릭합니다.  
  
   성공으로 견적을 닫을 경우, 프로젝트가 **계약** 단계로 이동하며, 이 프로젝트에 대한 계약을 만들 **프로젝트 계약** 화면이 나타납니다.  
  
### <a name="see-also"></a>참고 항목  
 [거래처 관리자 가이드](../psa/account-manager-guide.md)
