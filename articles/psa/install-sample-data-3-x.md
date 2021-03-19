---
title: 샘플 데이터 설치
description: 이 항목은 Project Service Automation에서 샘플 데이터를 설치하는 방법에 대한 정보를 제공합니다.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 377e50fc5772c4dc146ccee098bf2806bbc8c6b7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275096"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Project Service 응용 프로그램에 대한 샘플 데이터 설치

[!include [banner](../includes/psa-now-project-operations.md)]

귀하만의 데모 환경을 구축하는 데 도움이 되도록 Microsoft는 귀하 앱의 기능을 보여주는 다운로드 가능한 샘플 데이터 패키지를 제공합니다. 두 가지 유형의 샘플 데이터 패키지:
- 참조/설정 데이터
- 데모 데이터(참조/설정 및 작업 주문과 프로젝트 같은 트랜잭션 데이터)

샘플 **참조** 데이터 패키지는 세 개의 별도 패키지로 다운로드할 수 있으므로 Project Service에 대해서만 또는 Field Service에 대해서만 데이터를 설치하거나 두 응용 프로그램에 대한 샘플 데이터를 한 번에 모두 설치할 수 있습니다.

샘플 설정/참조 데이터 패키지:

- [**V902PSMasterData** - Project Service 버전 3.x 전용](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service 버전 8.x 전용](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x 및 Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

최신 **데모** 데이터 패키지:

 - [**FPSDemoData** - Field Service 8.x 및 Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   설치 지침은 섹션을 만들고 구성하는 사용자가 약간씩 다르지만 나머지는 이전 [**블로그 게시물**](https://aka.ms/fpsdemodatablog)에서와 동일합니다. 이 패키지는 감소된 데모 데이터 세트를 제공하며 설치하는 데 약 3시간이 걸립니다.

이 샘플 데이터 패키지는 영어로만 제공됩니다.

> [!IMPORTANT]
> **샘플 데이터 설치를 해제하는 방법은 없습니다.** 이러한 패키지는 데모, 평가, 교육 또는 테스트 시스템에서만 사용해야 합니다. 또한 개별 패키지를 설치한 다음 다른 개별 패키지를 설치하는 것은 지원되지 않습니다. (즉 **FSMasterData** 뒤에 **PSMasterData** 를 설치할 수 없습니다 또는 그 반대의 경우도 마찬가지입니다.) 나중에 두 응용 프로그램에 대한 샘플 데이터가 필요한 경우 **v902FPSMasterData** 패키지를 설치해야 합니다.

샘플 데이터 패키지를 설치하는 경우 설치 프로세스는 다음 작업을 수행합니다.

- Project Service, Field Service 또는 두 응용 프로그램 모두(해당되는 경우)를 사용하기 위한 기본 파라미터를 만들거나 설정합니다.

- 예약 가능한 리소스, 응용 프로그램별 역할, 판매 및 비용 가격표, 조직 구성 단위, 영업 프로세스 레코드 및 기타 엔터티와 같은 응용 프로그램의 샘플 데이터를 가져와 주요 기능을 보여줍니다.  

**데모 데이터** 패키지를 사용하면 작업 주문 및 프로젝트와 같은 위의 트랜잭션 데이터를 얻을 수 있습니다.

샘플 데이터를 사용하여 데모를 수행할 수 있는 기능에 대해 궁금하십니까? [기술 정보](#technical-notes)의 Fabrikam Robotics 가상 시나리오를 참조하십시오.

이러한 샘플 데이터 패키지를 설치하는 방법에 대한 질문이 있는 경우 [fpsdemodata@microsoft.com에서 전자 메일을 보내주십시오](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>요구 사항

설치 프로토콜은 대상 인스턴스(org)에 대해 다음을 가정합니다.

- 기본 언어는 영어이고 기본 통화는 미국 달러(USD, $)입니다.

- 조직에는 아직 Project Service 또는 Field Service 데이터가 없거나, 새 조직에 제공되는 기본 데이터만 있습니다.

- 올바른 버전의 비즈니스 응용 프로그램이 이미 설치되어 있습니다.
       
    - **FPSDemoData 또는 v902FPSMasterData의 경우:** 조직에는 Field Service 버전 8.x 및 Project Service 버전 3.x가 설치되어 있습니다.

    - **v902PSMasterData의 경우:** 조직에 Project Service 버전 3.x가 설치되어 있습니다.

    - **v902FSMasterData의 경우:** 조직에 Field Service 버전 8.x가 설치되어 있습니다.

> [!NOTE]
> 이미 데이터가 있는 기존 Project Service 및 Field Service 평가판 또는 데모 환경 위에 샘플 데이터를 설치해야 하는 경우(권장하지 않음) 설치 관리자가 수행하는 안전 사전 검사를 일시 중단해야 합니다. 자세한 내용은 아래의 기술 정보를 참조하십시오.

## <a name="prepare-for-installation"></a>설치 준비

최신 버전의 Windows(Windows 10 선호)를 사용하여 컴퓨터에서 설치 관리자를 실행해야 합니다.

컴퓨터를 네트워크에 연결된 상태로 유지하고 설치를 **설정/참조 데이터** 에 대해 최대 **1시간** 동안 실행하도록 계획해야 합니다. (일반적으로 설치는 두 응용 프로그램에 대한 샘플 데이터를 포함하는 **FPSMasterData** 에 대해 약 30분이 소요됩니다.) **FPSDemoData** 의 경우 설치 시 약 **3시간** 이 소요됩니다.

컴퓨터에 화면 보호기 기능이 꺼져 있어야 합니다. 그렇지 않으면 세션을 활성 상태로 유지하지 않는 한 화면 보호기가 작동할 때 설치에 대한 세션 자격 증명이 손실될 수 있습니다.

> [!div class="mx-imgBorder"]
> ![화면 보호기가 꺼져 있는 화면 보호기 설정의 스크린샷](media/sample-data-1.png)

## <a name="download-and-unpack"></a>다운로드 및 압축 풀기

Project Service 및 Field Service 샘플 데이터 설치 관리자는 자동 압축 풀기 실행 파일로 배포됩니다. 파일 이름은 샘플 데이터 패키지에 따라 다를 수 있지만 그렇지 않은 경우에는 설치하는 패키지에 관계 없이 단계는 동일합니다.

패키지를 다운로드한 후, .exe 파일을 실행한 다음 약관에 동의하여 압축된 zip 파일의 압축을 풉니다. 그런 다음 해당 파일을 실행하여 컴퓨터의 폴더에 압축을 풉니다.

운영 체제 및 보안 설정에 따라 zip 파일의 압축을 푼 후 다음 단계를 수행해야 할 수 있습니다.

1. **v902FPSMasterData** / **PackageDeployer_FPSDemoData** 폴더에서 **FPSDemoData.dll** 파일을 찾아 마우스 오른쪽 단추로 클릭합니다.

2. **차단 해제** 를 선택합니다.

3. **적용** 을 선택합니다.

4. **확인** 을 선택합니다.


## <a name="create-or-configure-users"></a>사용자 만들기 또는 구성

**FPSDemoData** 패키지는 6명의 사용자를 필요로 하지만 **FPSMasterData** 패키지는 한 명의 사용자가 필요합니다. 샘플 데이터 패키지에 대한 올바른 내용을 참조하십시오.

## <a name="create-or-configure-users---setupreference-data-packages"></a>사용자 - 설정/참조 데이터 패키지 만들기 또는 구성

**FPSMasterData** 패키지는 여기에 설명된 설정을 사용하여 Spencer Low라는 이름의 한 사용자로 설치하도록 설계되었습니다. 패키지를 올바르게 설치하려면 들어오는 샘플 데이터 구성과 일치하도록 귀하의 환경에서 사용자를 만들거나 임시로 이름을 바꾸어야 합니다.

사용자를 만들거나 구성하려면 **설정** > **보안** > **사용자** 로 이동하여 다음을 수행합니다.

1. UserFullname="Spencer Low"를 사용자 이름 "spencerl"(**소문자**)로 설정하여 프로젝트 관리자 및 업무 관리자 역할로 설정합니다.

2. **Spencer Low** 사용자를 선택한 다음 **역할 관리** 를 선택합니다. **시스템 관리자** 역할을 찾아 선택한 다음 **확인** 을 선택하여 전체 관리자 권한을 Spencer Low에 부여합니다. 이 단계는 올바른 사용자 소유권을 사용하여 샘플 레코드를 만들고 보기를 올바르게 채울 수 있도록 하는 데 필요합니다.

3. 다운로드한 패키지에서 기본 사용자 컨텍스트의 전자 메일 주소를 사용하여 데이터 매핑 파일을 업데이트해야 합니다. 이 작업을 수행하려면 **PkgFolder** 를 연 다음 메모장(또는 Visual Studio 또는 다른 xml 편집기)에서 **ImportUserMapFile.xml** 파일을 찾아서 엽니다. **DefaultUserToMapTo=** 필드를 Spencer Low 사용자의 전자 메일 주소로 설정합니다.

4. 사용자 이름 **spencerl** 로 Spencer Low를 사용하지 않는 경우, 추가 파일을 업데이트해야 합니다. **DemoDataPreImportConfig.xml** 파일을 연 다음 **userstocreateandconfigure** 태그를 찾습니다. **\<login\>** 태그를 Spencer Low 사용자의 사용자 이름으로 업데이트합니다. 자세한 내용은 [기술 정보](#technical-notes)를 참조하십시오.

## <a name="create-or-configure-users---demo-data-package"></a>사용자 - 데모 데이터 패키지 만들기 또는 구성

데모 데이터 패키지에는 여섯 명의 사용자가 필요합니다. 패키지를 올바르게 설치하려면 다음을 수행합니다.

 1. **설정** > **보안** > **사용자** 로 이동하여 들어오는 샘플 데이터 구성과 일치하도록 기존 사용자를 만들거나 임시로 이름을 바꿉니다.
 
    이러한 역할은 가상 사용자 기반 데모에만 필요합니다.  
    - 사용자 전체 이름 = "David So" Field Service 기술자   
    - 사용자 전체 이름 = "Jamie Reding" Customer Service 및 Field Service 디스패처   
    - 사용자 전체 이름 = "Molly Clark" 계정 관리자   
    - 사용자 전체 이름 = "Spencer Low" 연습 및 프로젝트 관리자  
    - 사용자 전체 이름 = "Veronica Quek" 팀 구성원   
    - 사용자 전체 이름 = "William Contoso"
  
2. 데모 데이터 가져오기의 목적을 위해 관리자 역할 위에 여섯 명의 사용자를 할당하여 샘플 레코드를 올바르게 가져올 수 있도록 합니다. 

3. **PkgFolder** 를 열고 **ImportUserMapFile.xml** 을 찾아서 엽니다. 시스템에 있는 해당 사용자의 전자 메일 주소에 대한 **새=** 필드를 업데이트합니다.

   > [!div class="mx-imgBorder"]
   > ![UserMapFile의 스크린 샷](media/sample-data-7.png)

4. "Spencer Low" 전체 이름 사용자가 **"spencerl"** 과 다른 사용자 ID를 가지고 있다면 추가 파일을 업데이트해야 합니다. **DemoDataPreImportConfig.xml** 파일을 연 다음 **userstocreateandconfigure** 태그를 찾습니다. **\<login\>** 태그를 loginid(대/소문자 구분)로 업데이트합니다. 

5. 첫 번째 사용자의 일정(**userstocreateandconfigure** 태그에 있음)은 데모 데이터를 가져올 수 있는 모든 예약 가능한 리소스에 대한 근무 시간을 채우는 데 사용됩니다. **설정** > **보안** > **사용자** 로 이동하여 "Spencer Low" 사용자를 찾고 "근무 시간" 옵션을 엽니다. 기존 근무 시간을 편집하여 **되풀이되는 주별 일정의 시작 날짜부터 종료 날짜까지 모두** 선택합니다. **근무 시간이 월요일부터 금요일까지 오전 8시 ~ 오후 5시까지 설정되고 시간대가 태평양 표준시(미국 및 캐나다)로 설정되었는지** 확인합니다. 이는 프로젝트 및 일정 게시판이 예상대로 표시되는지 확인하는 데 필요합니다.

**권장 사항**: 샘플 데이터를 설치하는 동안 문제가 발생하여 시작 지점으로 되돌려야 하는 경우에 대비해 지금 조직의 백업을 만드는 것이 좋습니다. 자세한 내용은 [인스턴스 백업 및 복원](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances)을 참조하십시오.

## <a name="run-the-package-deployer"></a>Package Deployer를 실행합니다.

1. **v902FPSMasterData** 또는 **PackageDeployer_FPSDemoData** 폴더에서 **PackageDeployer.exe** 를 찾아 실행합니다.

2. 사용 약관에 동의합니다.

3. 다음 창에서:

   a. 배포 유형 **Office 365** 을 선택합니다.

   b. "사용자 만들기 또는 구성"(사용자 이름이 "spencerl"인 "Spencer Low")에 구성된 시스템 관리자 사용자의 사용자 및 암호를 사용합니다.

   c. **사용 가능한 조직 목록 표시** 가 선택되어 있는지 확인합니다.

      > [!div class="mx-imgBorder"]
      > !["가용 조직 목록 표시"가 선택된 Package Deployer 창의 스크린샷](media/sample-data-2.png)

4. 샘플 데이터를 설치하려는 조직을 선택합니다.

5. **데모 데이터 설정** 대화 상자가 표시될 때까지 **다음** 을 선택합니다.

   > [!div class="mx-imgBorder"]
   > ![데모 데이터 설치 관리자 상태 창의 스크린샷](media/sample-data-3.png)

6. 계속하기 전에 샘플 데이터를 설치하는 데 최대 1시간이 걸릴 수 있습니다(일반적으로 10분 이내). 설치 과정에서 컴퓨터가 네트워크에 연결되어 있고 세션이 활성 상태를 유지하는지 확인해야 합니다.   

7. 준비가 되면 **다음** 을 클릭하여 샘플 데이터 설치 프로세스를 시작합니다. 샘플 데이터가 로드된 후 **마침** 을 클릭합니다.

## <a name="verify-the-sample-data-installation"></a>샘플 데이터 설치 확인

정확성 검사의 경우 Fabrikam Robotics 가상 시나리오에 나열된 엔터티의 레코드 및 유형 수가 예상대로 나타나는지 확인합니다.

샘플 데이터가 완전히 로드된 후에는 Spencer Low 사용자로 로그인하고 다음을 확인합니다.

- Project Service 응용 프로그램이 설치된 경우 **Project Service** > **설정** > **가격표** 로 이동합니다. 데이터 집합에 각 국가/지역에 대한 적절한 통화로 청구서 요금 및 비용 비율이 존재하는지 확인합니다.

- Project Service 응용 프로그램이 설치된 경우 **Universal Resource Scheduling** > **설정** > **조직 구성 단위** 로 이동합니다. 적절한 통화가 포함된 원가 목록이 각 조직 단위(도시 항목 제외)와 연결되어 있는지 확인합니다. 누락된 경우 올바른 원가 목록을 찾아 연결합니다.

- Field Service 응용 프로그램이 설치된 경우 **Project Service** > **설정** > **가격표** 로 이동합니다. 청구서 요금 및 비용 비율이 존재하는지 확인합니다. **Field Service** > **설정** > **가격표** 로 이동하여 데이터 집합에 각 국가/지역에 대한 적절한 통화로 청구서 요금 및 비용 비율이 있는지 확인합니다.

  > [!div class="mx-imgBorder"]
  > ![활성 가격표의 스크린샷](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![활성 조직 단위의 스크린샷](media/sample-data-5.png)

## <a name="technical-notes"></a>기술 정보

이 데이터의 설치에 대한 자세한 기술 정보는 아래를 참조하십시오.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>기존 데이터 위에 샘플 데이터 설치(권장하지 않음)

이미 데이터가 있는 기존 Field Service 또는 Project Service 평가판 또는 데모 환경 위에 샘플 데이터를 설치해야 하는 경우 설치 관리자가 수행하는 안전 사전 검사를 일시 중단해야 합니다.

이렇게 하려면 **PkgFolder** 폴더로 이동하여 메모장(또는 다른 xml 편집기)을 사용하여 **DemoDataPreImportConfig.xml** 파일을 찾아 엽니다.

다음 값을 찾은 다음 true에서 false로 설정을 변경합니다.

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

이 변경으로 인해 설치 관리자는 다음을 포함한 몇 가지 중요한 안전 검사를 우회합니다.

- 활성 **조직 구성 단위** 레코드가 둘 이상 있는지 확인한 다음 **Fabrikam US** 로 이름을 변경합니다.

- 활성 **작업 템플릿** 레코드가 두 개 이상 있는지 확인합니다.

- 활성 **프로젝트 파라미터** 레코드가 둘 이상 있는지 확인한 다음 해당 항목을 **파라미터** 로 이름을 변경합니다.

### <a name="configuration-components"></a>구성 구성 요소

이 사전 가져오기 구성 파일에는 여러 가지 다른 구성 구성 요소가 있습니다. 기술 사용자의 경우 다음이 포함됩니다.

- **\<RequiredSolutions\>** 는 필수 구성 요소 솔루션 설치 및 해당 버전 번호를 지정합니다.

- **\<InstallSampleData\>** 는 앱을 위한 기본 샘플 데이터를 설치할지 여부를 통제합니다.

    - false - 이 기본 제공 데이터(이동식)의 설치를 건너뜁니다.

    - true - FS 및 PSA 샘플 데이터의 설치와 동시에 기본 제공 데이터를 설치합니다.

- **\<PreImportDataCollection\>** 은 플랫 파일 데이터 맵 및 기본 샘플 데이터 설치 전에 가져올 관련 레코드를 지정합니다.

- **\<EntitiesToEnableScheduling\>** 은 Microsoft Dynamics Scheduling(즉, Universal Resource Scheduling)에서 예약할 수 있는 엔터티를 지정합니다.

- **\<UsersToCreateAndConfigure\>** 는 샘플 데이터 가져오기가 실행되기 전에(아직 존재하지 않는 경우) 만들어질 예약 가능한 리소스를 지정합니다. 소스 시스템 샘플 데이터 예약 가능 리소스가 각 리소스의 FullName 및 로그인에 있는 대상 시스템 예약 가능 리소스 레코드와 일치합니다. 따라서 이러한 이름을 사용하여 먼저 샘플 데이터를 대상 시스템으로 가져온 다음 예약 가능한 리소스의 이름을 활성화된 사용자 레코드와 함께 원하는 이름으로 바꾼 다음 최종 대상 시스템으로 가져오기 위해 데이터를 다시 내보내지 않는 한 이 사전 구성 파일의 이름을 변경할 수 없습니다(그에 따라 **ImportUserMapFile.xml** 이전 및 새 항목에 업데이트).

- **\<PluginsToDisable\>** 은 샘플 데이터 가져오기 중에 비활성화해야 하는 매우 불연속 라인 항목 플러그 인을 지정한 다음 나중에 다시 활성화합니다.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics 가상 시나리오

Field Service 및 Project Service 샘플 참조 데이터 패키지는 약 4000 레코드 및 약 40가지 다른 엔터티와 함께 **Fabrikam Manufacturing Master Data (v3.0.0.0) 솔루션** 을 설치합니다. Field Service 또는 Project Service에 대한 별도의 샘플 데이터 패키지에는 해당 응용 프로그램에 대한 **v902FPSMasterData** 샘플 데이터의 하위 집합이 포함되어 있습니다. **데모 데이터** 패키지는 148 엔터티에서 약 22,000 레코드를 가진 **Fabrikam 제조 데모 데이터(v3.0.0.7) 솔루션** 을 설치합니다.

가상의 회사인 Fabrikam Robotics는 전자 장치 조립 라인 로봇 제조업체로, 설치 계획, 구현 및 지속적인 유지 관리 서비스를 포함하여 제품 품질, 혁신 및 확실한 고객 서비스로 잘 알려져 있습니다. Fabrikam은 미국에 본사를 두고(Fabrikam US) 프랑스, 인도, 영국 및 스위스에서 프로젝트 기반 서비스 작업을 수행합니다.

Field Service 작업은 미국 중심부, 주로 시애틀 지역에서 이루어집니다. 이 회사는 사물 인터넷(IoT) 연결을 활용하여 고객 자산 성과를 모니터링하고 더욱 적극적인 현장 서비스를 제공하는 데 주력하고 있습니다.

샘플 데이터에 대한 높은 수준의 개요는 다음과 같습니다.

- 일반적인 샘플 데이터 요소(두 응용 프로그램 모두에 포함됨)

    - 1명의 사용자

    - 71개의 거래처

    - 137개의 연락처

    - 다양한 거래 유형 및 범주

    - 1개 제품 가격표가 있는 50개 제품

    - 14개의 원가/가격표

    - 3개 레벨(등급 값)이 있는 2개 등급 모델에서 31개 특성(리소스 기술)

- Project Service

    - 8개 조직 구성 단위

    - 6개 역할별 사용률 수준

    - 2.8k+ 역할 가격 사양

- Field Service

    - 4개 권역

    - 5개 작업 주문 유형

    - 22개 고객 자산

    - 관련 리소스 특성(9), 서비스(13) 및 서비스 작업(13)의 범위를 가진 9개 문제 유형
   
**데모 데이터** 패키지는 약 179개 작업 주문, 12개 프로젝트 및 관련 트랜잭션 데이터를 설치합니다. 

### <a name="change-the-work-hours-for-sample-resources"></a>샘플 리소스의 작업 시간 변경

기본적으로 예약 가능한 모든 리소스에는 24 근무 시간 달력이 있습니다.

샘플 예약 가능한 리소스의 작업 시간을 변경해야 하는 경우 **Universal Resource Scheduling** > **예약** > **리소스** 로 이동합니다.

사용자(예: Spencer Low)를 선택하고 여러 사용자에게 적용하려는 시간으로 Spencer의 근무 시간을 변경합니다. **Universal Resource Scheduling** > **설정** > **작업 시간 템플릿** 으로 이동하여 **기본 작업 템플릿** 레코드를 편집합니다. **템플릿 리소스** 필드에서 다른 리소스에 적용하려는 근무 시간이 있는 사용자를 선택합니다. **Universal Resource Scheduling** > **일정** > **리소스** > **예약 가능한 활성 리소스** 로 이동합니다. 변경할 리소스를 선택한 다음 **일정 설정** 을 선택합니다. **작업 템플릿** 드롭다운 목록에서 **기본 작업 시간** 템플릿 또는 올바른 템플릿 리소스가 있는 다른 템플릿을 선택합니다. 일정 게시판으로 이동하면 리소스가 작업 시간을 업데이트한 것을 확인할 수 있습니다.

> [!div class="mx-imgBorder"]
> ![예약 가능한 활성 리소스의 스크린샷](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]