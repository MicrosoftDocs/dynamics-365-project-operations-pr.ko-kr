---
title: Project Service Automation 업데이트 릴리스 13, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에서는 Project Service Automation 업데이트 릴리스 13, V3의 새로운 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080012"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation 업데이트 릴리스 13, V3
Dynamics 365 Project Service Automation(PSA) 애플리케이션의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 13에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.3.18이며 다음 일정으로 일반적으로 제공됩니다.

- **일반 가용성(자체 업데이트):** 2019년 11월
- **자동 업데이트:** 2019년 12월


## <a name="update-release-13"></a>업데이트 릴리스 13 

### <a name="bug-fixes"></a>버그 수정

- 시간 및 경비

     - 수정: 비용 목적으로 검색할 때 **비용 승인** 페이지의 검색 기능이 작동하지 않습니다.

- 리소스 관리

     - 수정: 조정의 숫자가 올바르게 정렬되도록 업데이트되었습니다.
     - 수정: 명명된 리소스를 **일정** 탭을 통해 작업에 할당할 수 없습니다.

- 프로젝트 관리

     - 수정: 팀 구성원을 할당할 때 **TransactionType** 에 **단위** 및 **기본 그룹** 에 대한 설정 정보가 누락된 경우 Null 참조 예외.

- Sales

     - 수정: 역할 가격 레코드가 작성되면 중복 거래 유형 레코드가 오류를 반환합니다.
     - 수정: **새 영업 기회** , **견적** , **주문 라인** , **제품 추가** 에 대한 추가 버튼이 영업 기회, 견적, 주문 제품에 대한 명령과 프로젝트 기반 라인 하위 표에 표시됩니다.


