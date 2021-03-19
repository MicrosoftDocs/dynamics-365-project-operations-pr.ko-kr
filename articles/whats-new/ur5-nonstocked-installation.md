---
title: Finance 환경에서 Project Operations 업데이트
description: 이 항목은 Dynamics 365 Finance 환경에서 Project Operations를 업데이트하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291987"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Finance 환경에서 Project Operations 업데이트

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_


이 항목은 Dynamics 365 Finance  환경에서 Dynamics 365 Project Operations를 업데이트하는 방법에 대한 정보를 제공합니다. Project Operations를 업데이트 5(UR5)로 업데이트하는 데 필요한 세 가지 절차가 있습니다.

- [미리보기 프로젝트로 패키지 가져오기](#import)
- [업데이트 적용](#apply)
- [Dataverse 환경 업데이트](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>LCS 프로젝트로 패키지 가져오기

1. [Lifecycle Services(LCS)](https://lcs.dynamics.com/)에 프로젝트 담당자 또는 환경 관리자로 로그인합니다.
2. 프로젝트 목록에서 LCS 프로젝트를 선택합니다.
3. **프로젝트** 페이지의 **환경** 그룹에서 업데이트할 환경을 엽니다.
4. 환경이 실행되고 있는지 확인합니다. 시작되지 않은 경우 환경을 시작합니다.
5. **새 릴리스** 섹션의 **사용 가능한 업데이트** 아래에서 10.0.15에 대한 **업데이트보기** 를 선택합니다.

![업데이트 보기 단추](media/view-update.png)

6. **바이너리 업데이트** 페이지에서 **패키지 저장** 을 선택합니다.
7. **업데이트 검토 및 저장** 페이지에서 **패키지 저장** 을 선택합니다.
8. **자산 라이브러리에 패키지 저장** 창이 열리면 패키지 이름을 입력하고 **패키지 저장** 을 선택합니다.
9. LCS가 패키지 저장을 마치면 **완료** 단추가 활성화됩니다. **완료** 를 선택합니다. LCS가 패키지를 확인합니다. 확인에는 몇 분 또는 최대 1시간이 소요될 수 있습니다.


## <a name="apply-the-package-update"></a><a name="apply"></a>패키지 업데이트 적용

1. LCS의 **환경 세부 정보** 페이지에서 **유지 보수** > **업데이트 적용** 을 선택합니다.
2. 목록에서 이전에 저장한 패키지를 선택한 다음 **적용** 을 선택합니다.
3. **예** 를 선택하여 패키지를 배포할지 확인합니다.

![패키지 배포 확인 대화 상자](media/confirm-package-deployment.png)

4. **예** 를 선택하여 응용 프로그램을 업데이트할지 확인합니다.

![응용 프로그램 업데이트 확인 대화 상자](media/confirm-application-update.png)

배포 및 응용 프로그램 업데이트가 시작됩니다. 

**환경 세부 정보** 페이지의 오른쪽 상단에서 환경 상태가 **서비스 중** 으로 업데이트됩니다. 약 2시간 후에 업데이트가 완료됩니다. 응용 프로그램 릴리스 정보가 **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** 로 업데이트되고 환경 상태가 **배포됨** 으로 업데이트됩니다.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Dataverse 환경 업데이트

1. [Power Platform 관리 센터](https://admin.powerplatform.com/)에 로그인합니다.
2. 목록에서 Project Operations를 설치하는 데 사용한 환경을 찾아서 엽니다.
3. **환경** 페이지에서 **리소스** > **Dynamics 365 앱** 을 선택합니다.
4. 목록에서 **Microsoft Dynamics 365 Project Operations** 를 찾아 **상태** 열에서 **업데이트 사용 가능** 을 선택합니다.
5. **서비스 약관에 동의함** 확인란을 선택한 다음 **업데이트** 를 선택합니다. 최신 버전의 솔루션이 설치됩니다.

설치가 완료되면 버전 4.5.0.134가 설치됩니다.

## <a name="configure-new-features"></a>새 기능 구성

### <a name="enable-dual-write-mapping"></a>이중 쓰기 매핑 활성화

Finance 및 Dataverse 환경에 대한 업데이트를 완료한 후 필요한 이중 쓰기 매핑을 활성화할 수 있습니다. 다음 절차를 완료하여 이중 쓰기 매핑을 활성화합니다.

- [Customer Engagement 환경에서 보안 설정 업데이트](#security)
- [데이터 엔터티 새로 고침](#refresh)
- [이중 쓰기 매핑 업데이트 및 실행](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Dataverse 환경에서 보안 설정 업데이트

UR5 업데이트의 일부로 엔티티의 보안 권한에 대한 다음 업데이트가 필요합니다.

1. Dataverse 환경에서 **설정** 으로 이동하고 **시스템** 그룹에서 **보안** 을 선택합니다.

![Dataverse 환경 설정](media/Picture21.png)

2. **보안 역할** 을 선택합니다.
3. 역할 목록에서 **이중 쓰기 앱 사용자** 를 선택하고 **사용자 지정 엔터티** 탭을 선택합니다. 
4. 역할에 다음에 대한 **읽기** 및 **다른 레코드에 추가** 권한이 있는지 확인합니다.

      - **통화 환율 유형**
      - **계정 차트** 
      - **회계 달력** 
      - **원장**

5. 보안 역할이 업데이트되면 **설정** > **보안** > **팀** 으로 이동합니다. **이중 쓰기 앱 사용자** 역할이 팀에 적용되었는지 확인합니다. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>업데이트에서 데이터 엔터티 새로 고침

1. Finance 환경에서 **데이터 관리** 작업 영역을 열고 **프레임워크 매개 변수** 페이지를 엽니다.
2. **엔터티 설정** 탭에서 **엔터티 목록 새로 고침** 을 선택합니다.
3. **닫기** 를 선택하여 엔터티 새로 고침을 확인합니다.

 > [!NOTE]
 > 이 프로세스는 완료하는 데 약 20분 정도 걸립니다. 새로 고침이 완료되면 알림을 받게 됩니다.

### <a name="update-dual-write-mappings"></a><a name="run"></a>이중 쓰기 매핑 업데이트

1. **데이터 관리** 작업 영역에서 **이중 쓰기** 를 선택합니다.
2. **솔루션 적용** 을 선택하고 목록에서 두 솔루션을 모두 선택한 다음 **적용** 을 선택합니다.
3. **이중 쓰기** 페이지에서 다음 테이블 맵을 선택한 다음 **중지** 를 선택합니다.

    - **Project Operations 통합 실제(msdyn_actuals)**
    - **Project Operations 통합 프로젝트 경비 범주(msdyn_expensecategories)**
    - **Project Operations 통합 실제 프로젝트 경비 내보내기 엔터티(msdyn_expenses)**

4. **테이블 맵 버전** 페이지에서 새 버전의 맵을 세 항목 각각에 적용합니다.
5. **이중 쓰기** 페이지에서 실행을 선택하여 맵을 다시 시작합니다.
6. 맵 목록에서 모든 필수 구성 요소가 있는 **원장(msdyn_ledgers)** 을 선택하고 **초기 동기화** 확인란을 선택합니다. 
7. **초기 동기화를 위한 마스터** 필드에서 **Finance and Operations 앱** 을 선택한 다음 **실행** 을 선택합니다.
 
 ![원장 맵 동기화](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]