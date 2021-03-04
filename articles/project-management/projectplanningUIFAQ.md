---
title: 작업 그리드에서 작업 문제 해결
description: 이 토픽은 작업 그리드에서 작업할 때 필요한 문제 해결 정보를 제공합니다.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031545"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>작업 그리드에서 작업 문제 해결 

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

이 토픽은 비용 관리 작업 중에 발생할 수 있는 문제를 해결하는 방법을 설명합니다.

## <a name="enable-cookies"></a>쿠키 활성화

Project Operations에서는 작업 분할 구조를 렌더링하기 위해 타사 쿠키를 활성화해야 합니다. 타사 쿠키가 활성화되지 않은 경우 작업이 표시되는 대신 **프로젝트** 페이지에서 **작업** 탭을 선택하면 빈 페이지가 표시됩니다.

![타사 쿠키가 활성화되지 않은 경우 빈 탭](media/blankschedule.png)


### <a name="workaround"></a>해결 방법
Microsoft Edge 또는 Google Chrome 브라우저의 경우 다음 절차는 타사 쿠키를 사용하도록 브라우저 설정을 업데이트하는 방법을 설명합니다.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Edge 브라우저를 엽니다.
2. 오른쪽 상단에서 **줄임표**(...)를 선택한 다음 **설정** 을 선택합니다.
3. **쿠키 및 사이트 권한** 아래에서 **쿠키 및 사이트 데이터** 를 선택합니다.
4. **타사 쿠키 차단** 을 끕니다.

#### <a name="google-chrome"></a>Google Chrome

1. Chrome 브라우저를 엽니다.
2. 오른쪽 상단에서 세 개의 수직 점을 선택한 다음 **설정** 을 선택합니다.
3. **개인 정보 및 보안** 아래에서 **쿠키 및 기타 사이트 데이터** 를 선택합니다.
4. **모든 쿠키 허용** 을 선택합니다.

> [!IMPORTANT]
> 타사 쿠키를 차단하면 해당 사이트가 예외 목록에서 허용되더라도 다른 사이트의 모든 쿠키 및 사이트 데이터가 차단됩니다.

## <a name="pex-endpoint"></a>PEX 끝점

Project Operations를 위해서는 프로젝트 매개 변수가 PEX 끝점을 참조해야 합니다. 이 끝점은 작업 분할 구조를 렌더링하는 데 사용되는 서비스와 통신하는 데 필요합니다. 매개 변수가 활성화되지 않은 경우 "프로젝트 매개 변수가 유효하지 않습니다."라는 오류 메시지가 표시됩니다. 

### <a name="workaround"></a>해결 방법
 ![프로젝트 매개 변수의 PEX 끝점 필드](media/projectparameter.png)

1. **PEX 끝점** 필드를 **프로젝트 매개 변수** 페이지에 추가합니다.
2. 다음 값으로 필드를 업데이트합니다: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. **프로젝트 매개 변수** 페이지에서 필드를 제거합니다.

## <a name="privileges-for-project-for-the-web"></a>웹에 대한 프로젝트 권한

Project Operations는 외부 일정 서비스에 의존합니다. 이 서비스를 사용하려면 사용자에게 작업 분할 구조와 관련된 엔터티를 읽고 쓰기 위해 할당된 여러 역할이 있어야 합니다. 이러한 엔터티에는 프로젝트 작업, 리소스 할당 및 작업 종속성이 포함됩니다. **작업** 탭으로 이동할 때 사용자가 작업 분할 구조를 렌더링할 수 없는 경우 Project Operations를 위한 프로젝트가 활성화되지 않았기 때문일 수 있습니다. 사용자는 보안 역할 오류 또는 액세스 거부와 관련된 오류를 수신할 수 있습니다.


## <a name="workaround"></a>해결 방법

1. **설정 > 보안 > 사용자 > 응용 프로그램 사용자** 로 이동합니다.  

   ![응용 프로그램 판독기](media/applicationuser.jpg)
   
2. 응용 프로그램 사용자 레코드를 두 번 클릭하여 다음을 확인합니다.

 - 사용자는 프로젝트에 액세스합니다. 이 확인은 일반적으로 사용자가 **프로젝트 관리자** 보안 역할이 있는지 확인하면 됩니다.
 - Microsoft Project 응용 프로그램 사용자가 존재하고 올바르게 구성되었습니다.
 
3. 이 사용자가 없으면 새 사용자 레코드를 만들 수 있습니다. **새 사용자** 를 선택합니다. 입력 양식을 **응용 프로그램 사용자** 로 변경한 다음 **응용 프로그램 ID** 를 추가합니다.

   ![응용 프로그램 사용자 세부 정보](media/applicationuserdetails.jpg)

4. 사용자에게 올바른 라이선스가 할당되었으며 라이선스의 서비스 계획 세부 정보에서 서비스가 활성화되었는지 확인합니다.
5. 사용자가 project.microsoft.com을 열 수 있는지 확인합니다.
6. 시스템이 올바른 프로젝트 끝점을 가리키고 있는지 프로젝트 매개 변수를 통해 확인합니다.
7. 프로젝트 응용 프로그램 사용자가 만들어졌는지 확인합니다.
8. 사용자에게 다음 보안 역할을 적용합니다.

  - Dataverse 사용자
  - Project Operations 시스템
  - 프로젝트 시스템

## <a name="error-when-updating-the-work-breakdown-structure"></a>작업 분할 구조를 업데이트할 때 오류 발생

작업 분할 구조를 하나 이상 업데이트하면 변경 사항이 결국 실패하고 저장되지 않습니다. 일정표에서 "최근 변경 사항을 저장할 수 없습니다."라는 오류가 발생합니다.

### <a name="workaround"></a>해결 방법

1. 사용자에게 올바른 라이선스가 할당되었으며 라이선스의 서비스 계획 세부 정보에서 서비스가 활성화되었는지 확인합니다.
2. 사용자가 project.microsoft.com을 열 수 있는지 확인합니다.
3. 시스템이 올바른 프로젝트 끝점을 가리키고 있는지 확인합니다.
4. 프로젝트 응용 프로그램 사용자가 만들어졌는지 확인합니다.
5. 사용자에게 다음 보안 역할을 적용합니다.
  
  - Dataverse사용자 또는 기본 사용자
  - Project Operations 시스템
  - 프로젝트 시스템
  - Project Operations 이중 쓰기 시스템(이 역할은 Project Operations의 리소스/비 재고 기반 시나리오를 배포하는 경우 필요합니다.)
