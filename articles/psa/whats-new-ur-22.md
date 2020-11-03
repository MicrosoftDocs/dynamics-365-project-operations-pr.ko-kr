---
title: Project Service Automation 업데이트 릴리스 22, V3의 새로운 기능 또는 변경된 기능
description: 이 항목에는 Project Service Automation 업데이트 릴리스 22, V3에서 사용할 수 있는 기능 및 수정 사항이 나열되어 있습니다.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080000"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation 업데이트 릴리스 22, V3

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation V3, 업데이트 릴리스 22에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V 3.10.33.48이며 일반적으로 2020년 6월 자체 업데이트를 통해 제공됩니다.

## <a name="update-release-22"></a>업데이트 릴리스 22

### <a name="bug-fixes"></a>버그 수정



**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

- **시간 항목** 은 가져온 후 시간 항목 일정에 자동으로 추가되지 않습니다.
- **시간 항목** 그리드 날짜 선택기는 사용자의 지역 설정을 인식하지 못합니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.

- 수동 모드에서는 **리소스 요구 사항** 을 생성할 때 **리소스 할당** 윤곽의 변경 사항이 인식되지 않습니다.
- **리소스 요청** 은 사용자 지정 요청 상태를 지원하지 않습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

- EstimateGridControl을 두 번 클릭하면 네덜란드어 형식 숫자를 올바르게 구문 분석할 수 없습니다.
- Microsoft Project 데스크톱 클라이언트 추가 기능을 사용하여 할당을 변경하면 할당된 시간이 올바르게 업데이트되지 않습니다.
- 계약 통화가 고객 통화와 다르고 조직이 통화 기호 대신 통화 코드를 표시하도록 구성된 경우 프로젝트 추적 및 견적 그리드에 잘못된 판매 통화 코드가 표시됩니다.
- 작업 시간 일정이 하루 24시간이면 팀원의 종료 날짜가 1일 추가됩니다.
- 프로젝트 일정에서 트랜잭션 범주를 작업에 추가해도 자동 저장이 트리거되지 않습니다.
- 프로젝트 템플릿에 팀 구성원을 추가할 때 다음 오류가 표시됩니다. "리소스 요구 사항을 프로젝트 템플릿과 연결할 수 없습니다." 
- 리본 규칙 스크립트 "msdyn.Approval.CanApproveOrReject"가 시간 초과 오류를 표시합니다.

**Sales**

다음과 같은 문제가 해결되었습니다.

- '새 견적 프로젝트 가격 목록' 양식/엔터티의 가격 목록 조회에서 비용 가격 목록을 선택한 경우 유효성 검사 오류 메시지가 표시되지 않습니다.
- 견적에 첨부된 BPF가 최종 단계에 있는 경우 견적을 성공으로 마감해도 생성된 계약으로 이동하지 않습니다.
- **미청구 판매** 를 반전하면 시간 항목이 리콜될 때 원래 비용에 연결됩니다.
- **확인** 버튼을 선택한 후 송장이 새로 고쳐지지 않는 한 인보이스 상태가 **확인됨** 으로 변경되지 않습니다.