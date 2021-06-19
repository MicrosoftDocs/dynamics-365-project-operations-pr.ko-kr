---
title: 프로젝트 상태 추적
description: 프로젝트 상태를 추적하는 방법(Project Service)
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014394"
---
# <a name="track-a-projects-status-project-service"></a>프로젝트 상태 추적(Project Service) 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]를 사용하여 클라이언트의 프로젝트 진행 상황을 추적할 수 있습니다.  

업무 진행 시, 프로젝트 단계가 업무 스테이지를 반영하여 업데이트됩니다.  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **새로 만들기**    | 프로젝트 생성 시, 스테이지는 **새로 만들기** 로 설정됩니다. 템플릿에서 프로젝트를 만드는 경우, 이 스테이지에서는 프로젝트에 일정, 추정 및 팀 데이터가 있을 수 있습니다. 그렇지 않을 경우, 프로젝트 개요가 되며 나머지 프로젝트 구성 요소를 직접 입력해야 합니다. |
|  **견적**   |      프로젝트를 견적에 연결하거나 견적에서 프로젝트를 만들 경우, 프로젝트 스테이지가 **견적** 으로 설정되며 예상 시작 및 종료 날짜도 업데이트됩니다. 프로젝트 진행 단계가 견적 스테이지일 경우, 견적 세부 항목이 **프로젝트** 페에지의 **영업** 탭에 표시됩니다.      |
|   **계획**   |                                     프로젝트와 연결된 견적에 대한 판매 승인을 받고 업무 진행 상황이 계약서 스테이지인 경우, 프로젝트 스테이지가 **계획** 으로 업데이트됩니다. 계약서 세부 항목은 **프로젝트** 페이지의 **영업** 탭에 표시됩니다.                                      |
| **완료됨** |                    프로젝트 작업이 완료되면, 스테이지를 **완료됨** 으로 전환할 수 있습니다. 프로젝트 스테이지가 완료됨으로 설정되면, 작업이 100% 완료된 것으로 인식되지만 보류 시간 동안 또는 경비 기입이 기록될 때까지 프로젝트가 열려있는 상태로 유지됩니다.                     |
|  **닫기**   |           모든 트랜젝션이 프로젝트에 기록되고 더 이상 기록할 것이 없을 것으로 예상될 경우, 직접 스테이지를 **종료** 로 설정할 수 있습니다. 프로젝트가 **종료** 로 설정되면, 프로젝트에 대한 추가 트랜잭션을 기록할 수 없고 프로젝트는 일기 전용 상태가 됩니다.           |

## <a name="to-track-a-projects-status"></a>프로젝트 상태 추적 방법  

1.  **Project Service > 프로젝트** 로 이동합니다.  

2.  작업을 원하는 프로젝트를 클릭합니다.  

3.  화면 상단 표시줄에서 프로젝트 이름 옆의 아래로 향하는 화살표를 선택한 다음 **프로젝트 추적** 을 클릭합니다.  

4.  작업 목록 위 드롭다운 목록에서 **작업량 추적** 또는 **비용 추적** 을 선택합니다.  

5.  편집할 업무를 두 번 클릭합니다. 또한, Gantt 차트의 막대를 움직이거나 크기를 조정하여 시간과 작업 진행 상황을 변경할 수 있습니다.  

### <a name="see-also"></a>참고 항목  
 [프로젝트 관리자 가이드](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]