---
title: Project Service Automation 업데이트 릴리스 26, V3의 새로운 기능 또는 변경된 기능
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643271"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation 업데이트 릴리스 26, V3
================================================

Dynamics 365용 Project Service Automation 응용 프로그램의 최신 업데이트를 발표하게 되어 기쁘게 생각합니다. 이 릴리스에는 품질, 성능 및 유용성에 대한 몇 가지 중요한 개선 사항이 포함되어 있습니다. 이 릴리스는 Dynamics 365 9.x와 호환됩니다. 이 릴리스로 업데이트하려면 Dynamics 365 온라인용 관리 센터를 방문한 다음 솔루션 페이지로 이동하여 업데이트를 설치하십시오. 자세한 내용은 [선호 솔루션의 설치, 업데이트 또는 제거](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)를 참조하세요.

이 항목에는 Project Service Automation 업데이트 릴리스 26, V3에서 새로 추가되거나 변경된 기능 및 수정 사항이 나열되어 있습니다. 이 버전의 빌드 번호는 V3.10.44.59이며 일반적으로 2020년 12월 자체 업데이트를 통해 제공됩니다.

<a name="update-release-26"></a>업데이트 릴리스 26
-----------------

### <a name="bug-fixes"></a>버그 수정

**시간 및 경비**

다음과 같은 문제가 해결되었습니다.

-   사용자는 승인/제출된 시간 항목에서 작업을 변경할 수 있습니다.

-   시간 입력을 저장할 때 "개체 참조가 설정되지 않음" 오류가 발생합니다.

-   리소스 할당에서 시간 항목을 가져 오면 DateTime 값으로 잘못된 시간 항목이 생성됩니다.

-   Project Service Automation 및 Field Service 앱이 모두 설치되면 Field Service 앱의 시간 항목에 대한 **새로 만들기** 단추가 명령 모음에 두 번 표시됩니다.

-   **허용 단위** 및 **단위 그룹** 셀 업데이트가 이제 **경비 추정** 그리드에서 작동합니다.

-   **업데이트 시간 항목 편집** 양식에는 **타임라인** 이 포함됩니다.

-   비 프로젝트 시간 항목에 대한 시간 승인은 프로젝트 승인자 역할을 검색할 때 시스템을 차단합니다.

**리소스 관리**

다음과 같은 문제가 해결되었습니다.

-   **PostProjectCreate** 플러그인에 생성하기 전에 기본 요구 사항을 확인하는 유효성 검사가 추가되었습니다.

-   **프로젝트 팀 구성원** 빨리 만들기 양식은 양식에서 필드가 제거되는 경우 널 참조 예외가 발생합니다.

-   1년 동안 12시간에 대한 요구 사항 생성은 실패합니다.

-   리소스 요구 사항 생성 중 오류 메시지 null 참조 예외가 개선되었습니다.

**프로젝트 관리**

다음과 같은 문제가 해결되었습니다.

-   **PreProjectUpdate** 플러그인에서 생성된 null 참조 예외를 해결하기 위해 유효성 검사가 향상되었습니다.

-   Microsoft Project 데스크톱 추가 기능에서 게시한 프로젝트는 할당되지 않은 할당을 삭제합니다.

-   **PreValidateProjectTaskUpdate** 플러그인에서 Null 참조 예외로 인해 작업의 프로젝트 참조가 유효하지 않은 경우 새 유효성 검사를 추가했습니다.

-   팀 구성원 그리드는 팀 구성원 레코드에 고유한 할당을 표시하지 않습니다.

-   **PreProjectTaskDelete** 플러그인에서 Null 참조 예외로 인한 새 유효성 검사 및 오류 메시지를 추가했습니다.

**Sales**

다음과 같은 문제가 해결되었습니다.

-   견적 또는 계약에서 프로젝트 기반 라인을 선택할 때 **제안** 단추는 기존 제품과 연관된 제품 기반 라인을 선택할 때만 표시되어야합니다.

-   **Create_Product** 권한을 **Create_ProjectContract** 권한에서 분할합니다.

-   송장 라인을 삭제하면 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 에서 Null 참조 실패가 발생합니다.
