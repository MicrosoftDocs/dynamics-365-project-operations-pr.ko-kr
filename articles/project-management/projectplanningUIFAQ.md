---
title: 작업 그리드에서 작업 문제 해결
description: 이 토픽은 작업 그리드에서 작업할 때 필요한 문제 해결 정보를 제공합니다.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: ee80363cf6f9a65a91be43a84434d37f02511f26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596426"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>작업 그리드에서 작업 문제 해결 


_**적용 대상:** 리소스/비재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 발행 처리, Project for the Web_

Dynamics 365 Project Operations에서 활용하는 작업 그리드는 Microsoft Dataverse 내의 호스팅된 iframe입니다. 이 사용의 결과로 인증 및 권한 부여가 올바르게 작동하도록 하려면 특정 요구 사항을 충족해야 합니다. 이 항목에서는 작업 분할 구조(WBS)에서 그리드를 렌더링하거나 작업을 관리하는 기능에 영향을 미칠 수 있는 일반적인 문제를 간략하게 설명합니다.

일반적인 문제는 다음과 같습니다.

- 작업 그리드의 **작업** 탭이 비어 있습니다.
- 프로젝트를 열 때 프로젝트가 로드되지 않고 사용자 인터페이스(UI)가 스피너에서 멈춥니다.
- **Project for the Web** 에 대한 권한 관리.
- 작업을 생성, 업데이트 또는 삭제할 때 변경 사항이 저장되지 않습니다.

## <a name="issue-the-task-tab-is-empty"></a>문제: 작업 탭이 비어 있음

### <a name="mitigation-1-enable-cookies"></a>완화 1: 쿠키 활성화

Project Operations에서는 작업 분할 구조를 렌더링하기 위해 타사 쿠키를 활성화해야 합니다. 타사 쿠키가 활성화되지 않은 경우 작업이 표시되는 대신 **프로젝트** 페이지에서 **작업** 탭을 선택하면 빈 페이지가 표시됩니다.

Microsoft Edge 또는 Google Chrome 브라우저의 경우 다음 절차는 타사 쿠키를 사용하도록 브라우저 설정을 업데이트하는 방법을 설명합니다.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Edge 브라우저를 엽니다.
2. 오른쪽 상단에서 **줄임표**(...)를 선택한 다음 **설정** 을 선택합니다.
3. **쿠키 및 사이트 권한** 아래에서 **쿠키 및 사이트 데이터** 를 선택합니다.
4. **타사 쿠키 차단** 을 끕니다.
5. 브라우저를 새로 고칩니다. 

#### <a name="google-chrome"></a>Google Chrome

1. Chrome 브라우저를 엽니다.
2. 오른쪽 상단에서 세 개의 수직 점을 선택한 다음 **설정** 을 선택합니다.
3. **개인 정보 및 보안** 아래에서 **쿠키 및 기타 사이트 데이터** 를 선택합니다.
4. **모든 쿠키 허용** 을 선택합니다.
5. 브라우저를 새로 고칩니다. 

> [!NOTE]
> 타사 쿠키를 차단하면 해당 사이트가 예외 목록에서 허용되더라도 다른 사이트의 모든 쿠키 및 사이트 데이터가 차단됩니다.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>완화 2: PEX 끝점이 올바르게 구성되었는지 확인

Project Operations를 위해서는 프로젝트 매개 변수가 PEX 끝점을 참조해야 합니다. 이 끝점은 작업 분할 구조를 렌더링하는 데 사용되는 서비스와 통신하는 데 필요합니다. 매개 변수가 활성화되지 않은 경우 "프로젝트 매개 변수가 유효하지 않습니다."라는 오류 메시지가 표시됩니다. PEX 끝점을 업데이트하려면 다음 단계를 완료하십시오.

1. **PEX 끝점** 필드를 **프로젝트 매개 변수** 페이지에 추가합니다.
2. 사용 중인 제품 유형을 식별합니다. 이 값은 PEX 끝점이 설정될 때 사용됩니다. 검색 시 제품 유형이 이미 PEX 끝점에 정의되어 있습니다. 이 값을 유지합니다.
3. 다음 값으로 필드를 업데이트합니다: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. 다음 표는 제품 유형에 따라 사용해야 하는 유형 매개변수를 제공합니다.

      | **제품 유형**                     | **유형 매개 변수** |
      |--------------------------------------|--------------------|
      | 기본 조직의 Project for the Web   | 유형=0             |
      | CDS 명명 조직의 Project for the Web | 유형=1             |
      | Project Operations                   | 유형=2             |

4. **프로젝트 매개 변수** 페이지에서 필드를 제거합니다.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>완화 3: project.microsoft.com에 로그인
Microsoft Edge 브라우저에서 새 탭을 열고 project.microsoft.com으로 이동한 다음 Project Operations에 액세스하는 데 사용하는 사용자 역할을 사용하여 로그인합니다.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>문제: 프로젝트가 로드되지 않고 UI가 스피너에서 멈춤

인증을 위해 작업 그리드를 로드하려면 팝업을 활성화해야 합니다. 팝업이 활성화되어 있지 않으면 로딩 스피너에서 화면이 멈춥니다. 다음 그래픽은 주소 표시줄에 차단된 팝업 레이블이 있는 URL을 보여줍니다. 이로 인해 스피너가 페이지를 로드하려고 할 때 멈추게 됩니다. 

   ![멈춘 스피너와 팝업 블록.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>완화 1: 팝업 활성화

프로젝트가 스피너에서 멈추면 팝업이 활성화되지 않을 수 있습니다.

#### <a name="microsoft-edge"></a>Microsoft Edge

Edge 브라우저에서 팝업을 활성화하는 방법에는 두 가지가 있습니다.

1. Edge 브라우저에서 브라우저 오른쪽 상단의 알림을 선택합니다.
2. **항상 특정 Dataverse 환경에서 팝업 및 리디렉션 허용** 을 선택합니다.
 
     ![팝업이 차단된 창입니다.](media/enablepopups.png)

또는 다음 단계를 완료할 수 있습니다.

1. Edge 브라우저를 엽니다.
2. 오른쪽 상단 모서리에서 **줄임표**(...)를 선택한 다음 **설정** > **사이트 권한** > **팝업 및 리디렉션** 을 선택합니다.
3. 장치에서 팝업을 차단하려면 **팝업 및 리디렉션** 을 끄고 팝업을 허용하려면 켭니다.
4. 팝업을 활성화한 후 브라우저를 새로 고칩니다. 

#### <a name="google-chrome"></a>Google Chrome
1. Chrome 브라우저를 엽니다.
2. 팝업이 차단된 페이지로 이동합니다.
3. 주소 표시줄에서 **팝업 차단됨** 을 선택합니다.
4. 보려는 팝업의 링크를 선택합니다.
5. 팝업을 활성화한 후 브라우저를 새로 고칩니다. 

> [!NOTE]
> 사이트에 대한 팝업을 항상 보려면 **[사이트]에서 팝업 및 리디렉션 항상 허용** 을 선택한 다음 **완료** 를 선택합니다.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>문제 3: Project for the Web에 대한 권한 관리

Project Operations는 외부 일정 서비스에 의존합니다. 이 서비스를 사용하려면 사용자에게 WBS와 관련된 엔터티를 읽고 쓸 수 있는 여러 역할이 할당되어 있어야 합니다. 이러한 엔터티에는 프로젝트 작업, 리소스 할당 및 작업 종속성이 포함됩니다. 사용자가 **작업** 탭으로 이동할 때 WBS를 렌더링할 수 없는 경우 **Project Operations** 를 위한 **프로젝트** 가 활성화되지 않았기 때문일 수 있습니다. 사용자는 보안 역할 오류 또는 액세스 거부와 관련된 오류를 수신할 수 있습니다.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>완화 1: 애플리케이션 사용자 및 최종 사용자 보안 역할의 유효성 검사

1. **설정** > **보안** > **사용자** > **응용 프로그램 사용자** 로 이동합니다.  

   ![응용 프로그램 판독기.](media/applicationuser.jpg)
   
2. 애플리케이션 사용자 레코드를 두 번 클릭하여 다음을 확인합니다.

     - 사용자는 프로젝트에 액세스합니다. 사용자에세 **프로젝트 관리자** 보안 역할이 있는지 확인하여 이를 수행할 수 있습니다.
     - Microsoft Project 응용 프로그램 사용자가 존재하고 올바르게 구성되었습니다.
 
3. 이 사용자가 없으면 새 사용자 레코드를 만듭니다. 
4. **새 사용자** 를 선택하고 입력 양식을 **응용 프로그램 사용자** 로 변경한 다음 **응용 프로그램 ID** 를 추가합니다.

   ![응용 프로그램 사용자 세부 정보.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>문제 4: 작업을 생성, 업데이트 또는 삭제할 때 변경 사항이 저장되지 않습니다

WBS에 대해 하나 이상의 업데이트를 수행하면 변경 사항이 실패하고 저장되지 않습니다. "최근 변경 사항을 저장할 수 없습니다"라는 메시지와 함께 일정 표에 오류가 발생합니다.

### <a name="mitigation-1-validate-the-license-assignment"></a>완화 1: 라이선스 할당 유효성 검사

1. 사용자에게 올바른 라이선스가 할당되었으며 라이선스의 서비스 계획 세부 정보에서 서비스가 활성화되었는지 확인합니다.  
2. 사용자가 **project.microsoft.com** 을 열 수 있는지 확인합니다.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>완화 2: 프로젝트 응용 프로그램 사용자의 유효성 검사 구성
1. 프로젝트 응용 프로그램 사용자가 만들어졌는지 확인합니다.
2. 사용자에게 다음 보안 역할을 적용합니다.
  
  - Dataverse 사용자 또는 기본 사용자
  - Project Operations 시스템
  - 프로젝트 시스템
  - Project Operations 이중 쓰기 시스템. 이 역할은 Project Operations의 리소스/비 재고 기반 배포 시나리오에 필요합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
