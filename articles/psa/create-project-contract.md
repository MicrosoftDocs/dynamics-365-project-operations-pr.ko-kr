---
title: 프로젝트 계약 만들기
description: 프로젝트 계약을 만드는 방법(Project Service)
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
ms.openlocfilehash: 7a626da271a4c4e1751870323b56ce54743bb891
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080066"
---
# <a name="create-a-project-contract-project-service"></a>프로젝트 계약서 만들기(Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

프로젝트에 대한 견적이 완성되면 계약서를 만들어 고객과 공식 확인해야 합니다. 각 견적에 대해 여러 계약서를 만들 수 있습니다. 프로젝트의 **계약** 단계에서 계약서를 만듭니다.  
  
1. 이전 단계의 **프로젝트 계약** 화면에서 **요약** 영역의 필요한 정보를 변경합니다.  
  
2. 계약 대상 제품을 추가하려면 **계약 내용** 영역의 **제품 기반 내용** 아래에 있는 **새로 만들기** 를 클릭합니다. **제품 이름** 아래 항목을 선택한 다음 수량, 영업 가격 및 계약 총액을 지정합니다.  
  
3. 계약서에 프로젝트 기반 내용을 추가하려면 **계약 내용** 영역의 **프로젝트 기반 내용** 아래에 있는 **+** 를 클릭합니다. 가능한 경우 이름, 예산 총액 및 프로젝트를 입력합니다. 작업 분할 구조로 프로젝트를 만들어 예상을 생성해야 할 경우 [프로젝트 만들기](../psa/create-project.md)를 참조하십시오.  
  
4. 편집을 마쳤으면, 화면 우측 하단의 **저장** 단추를 클릭합니다.  
  
5. 계약서를 고객에게 보낼 준비가 되면 **더 보기** (...)를 클릭하고 **보고서 실행** 을 클릭한 다음 **주문** 을 클릭합니다. [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)] 문서로 보고서를 저장하고 필요한 경우 편집한 다음 계약서를 고객에게 보냅니다.  
  
6. 고객이 계약 내용을 승인할 경우, **프로젝트 계약** 화면 상단의 **승인** 을 클릭합니다. 고객이 항목 변경을 원할 경우 새 계약서를 만듭니다. 고객이 지금 서비스를 사용하지 않기로 결정할 경우, **프로젝트 계약** 화면 상단의 **실패로 종료** 를 클릭합니다.  
  
### <a name="see-also"></a>참고 항목  
 [거래처 관리자 가이드](../psa/account-manager-guide.md)