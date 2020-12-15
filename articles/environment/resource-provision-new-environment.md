---
title: 새 환경 프로비전
description: 이 항목은 새 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642987"
---
# <a name="provision-a-new-environment"></a>새 환경 프로비전

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

이 토픽은 리소스/비 재고 기반 시나리오를 위한 새 Dynamics 365 Project Operations 환경을 프로비전하는 방법에 대한 정보를 제공합니다.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>LCS 프로젝트에서 Project Operations 자동화 프로비전 활성화

다음 단계를 사용하여 LCS 프로젝트에 대한 Project Operations 자동화 프로비전 흐름을 활성화합니다.

1. [LCS](https://lcs.dynamics.com/v2)로 이동하고 **미리 보기 기능 관리** 타일을 선택합니다.
2. **미리 보기 기능** 목록에서 **Project Operations 기능** 을 선택하고 **미리 보기 기능 활성화됨** 을 선택하여 Project Operations를 활성화합니다.

> [!NOTE]
> 이 단계는 LCS 프로젝트당 한 번만 수행됩니다.

## <a name="provision-a-project-operations-environment"></a>Project Operations 환경 프로비전

1. 새로운 Dynamics 365 Finance [데모 환경](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 또는 [샌드박스/프로덕션 환경](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)을 엽니다. 
2. **환경 프로비전** 마법사를 안내합니다. 

> [!IMPORTANT]
> 선택한 응용 프로그램 버전이 10.0.13 이상인지 확인하십시오.

3. Project Operations를 프로비전하려면 **고급 설정** 에서 **Common Data Service** 를 선택합니다. 
4. **예** 를 선택하여 **Common Data Service 설정** 을 활성화한 다음 필수 필드에 정보를 입력합니다.

  - Name
  - 영역
  - 언어
  - 통화
 
5. **Common Data Service 템플릿** 필드에서 **Project Operations** 를 선택합니다. 

6. 배포할 환경 유형을 선택합니다. 구독 기반 평가판을 사용하면 30일 동안 CDS 환경을 배포할 수 있습니다. 

![배포 설정](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> **수락** 을 선택하여 서비스 약관에 동의한 다음 **완료** 를 선택하여 배포 설정으로 돌아갑니다.

![배포 동의](./media/2DeploymentConsent.png)

7. 마법사의 나머지 필수 필드를 완료하고 배포를 확인합니다. 환경 프로비전 시간은 환경 유형에 따라 다릅니다. 프로비전에는 최대 6시간이 소요될 수 있습니다.

  배포가 성공적으로 완료되면 환경이 **배포됨** 으로 표시됩니다.

8. 환경이 성공적으로 배포되었는지 확인하려면 **로그인** 을 선택하고 확인을 위해 환경에 로그온합니다.

![ 환경 세부 정보](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance 데모 데이터 적용(선택 단계)

[이 문서](resource-apply-finance-demo-data.md)에 설명된 대로 Project Operations Finance 데모 데이터를 10.0.13 서비스 릴리스 클라우드 호스팅 환경에 적용합니다.

## <a name="apply-updates-to-the-finance-environment"></a>Finance 환경에 업데이트 적용

Project Operations에는 애플리케이션 버전이 **10.0.13(10.0.569.20009)** 이상인 Finance 환경이 필요합니다.

이 버전을 받으려면 Finance 환경에 품질 업데이트를 적용해야 할 수 있습니다.

1. LCS의 **환경 세부 정보** 페이지에서 **사용 가능한 업데이트** 섹션에서 **업데이트 보기** 를 선택합니다.

![보기 업데이트](./media/5ViewUpdates.png)

2. **바이너리 업데이트** 페이지에서 **패키지 저장** 을 선택합니다.

![패키지 저장](./media/6SavePackage.png)

3. **모두 선택** 을 클릭한 다음 **패키지 저장** 을 선택합니다.

![업데이트 검토 및 저장](./media/7ReviewAndSaveUpdates.png)

4. 패키지의 이름과 설명을 입력한 다음 **저장** 을 선택합니다. 인터넷 연결에 따라 이 과정은 다소 시간이 걸릴 수 있습니다.

![자산 라이브러리에 패키지 업로드](./media/8UploadPackageToAssetsLibrary.png)

5. 패키지를 저장한 후 **완료** 를 선택하고 이 패키지를 LCS 프로젝트의 자산 라이브러리에 저장합니다.

패키지를 저장하고 유효성을 검사하는 데 15분 정도 걸릴 수 있습니다.

6. 업데이트를 적용하려면 LCS의 **환경 세부 정보** 페이지에서 **유지** > **업데이트 적용** 으로 이동합니다.

![환경 유지](./media/9MaintainEnvironment.png)

7. 업데이트 목록에서 생성한 패키지를 선택하고 **적용** 을 선택합니다.

![업데이트 적용](./media/10ApplyUpdates.png)

환경 서비스는 다소 시간이 걸립니다. 완료되면 환경이 배포된 상태로 돌아갑니다.

![배포된 환경](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>이중 쓰기 연결 설정 

1. LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.
2. **Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다.
3. 링크가 완료된 후 **CDS for Apps에 대한 링크** 를 다시 선택합니다. Finance에서 이중 쓰기로 리디렉션됩니다.

![CDS에 대한 링크](./media/12LinktoCDS.png)

4. **솔루션 적용** 을 선택하여 통합에 매핑될 엔터티에 액세스합니다.

![솔루션 적용](./media/13ApplySolutions.png)

5. 두 솔루션 **Dynamics 365 Finance and Operations 이중 쓰기 엔터티 맵** 과 **Dynamics 365 Project Operations 이중 쓰기 엔터티 맵** 을 모두 선택한 다음 **적용** 을 선택합니다.

![솔루션 확인](./media/14ConfirmSolutions.png)

솔루션이 적용된 후 이중 쓰기 엔터티가 환경에 적용됩니다.

![솔루션 적용](./media/15ApplyingSolutions.png)

엔터티가 적용된 후 사용 가능한 모든 매핑이 환경에 나열됩니다.

![이중 쓰기 맵](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>업데이트 후 데이터 엔터티 새로 고침

1. Finance에서 **데이터 관리** 작업 영역으로 이동합니다.

![데이터 관리 작업 공간](./media/16DataManagement.png)

2. **프레임워크 매개 변수** 타일을 선택합니다.

![프레임워크 매개 변수](./media/17FrameworkParameters.png)

3. **엔터티 설정** 페이지에서 **엔터티 목록 새로 고침** 을 선택합니다.

![엔터티 목록 새로 고침](./media/18RefreshEntityList.png)

새로 고침에는 약 20분이 소요됩니다. 완료되면 알림이 표시됩니다.

![새로 고침 확인](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Project Operations 이중 쓰기 맵 실행

1. LCS 프로젝트에서 **환경 세부 정보** 페이지로 이동합니다.
2. **Common Data Service 환경 정보** 에서 **CDS for Apps에 대한 링크** 를 선택합니다. 링크를 선택하면 매핑의 엔터티 목록으로 리디렉션됩니다.
3. 다음 표에 설명된 대로 맵을 시작합니다. 나열된 순서를 따르십시오.

| **엔터티 맵** | **엔터티 새로 고침** | **초기 동기화** | **초기 동기화용 마스터** | **필수 구성 요소 실행** | **필수 구성 요소 초기 동기화** |
| --- | --- | --- | --- | --- | --- |
| **모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories)** | 없음 | 있음 | Common Data Service | 없음 | 해당 없음 |
| **법인(cdm\_companies)** | 없음 | 있음 | Finance and Operations 앱 | 없음 | 해당 없음 |
| **원장(msdyn_ledgers)** | 없음 | 있음 | Finance and Operations 앱 | 있음 | 예, Finance and Operations 앱 |
| **Project Operations 통합 실제(msdyn\_actuals)** | 없음 | 없음 | 해당 없음 | 예 | 없음 |
| **프로젝트 계약 내용(salesorderdetails)** | 없음 | 없음 | 해당 없음 | 없음 | 없음 |
| **프로젝트 트랜잭션 관계를 위한 통합 엔터티(msdyn\_transactionconnections)** | 없음 | 없음 | 해당 없음 | 없음 | 해당 없음 |
| **Project Operations 통합 계약 내용 중요 시점(msdyn\_contractlinesscheduleofvalues)** | 없음 | 없음 | 해당 없음 | 없음 | 해당 없음 |
| **경비 추정용 Project Operations 통합 엔터티(msdyn\_estimateslines)** | 없음 | 없음 | 해당 없음 | 없음 | 해당 없음 |
| **Project Operations 통합 프로젝트 경비 범주 내보내기 엔터티(msdyn\_expensecategories)** | 없음 | 없음 | 해당 없음 | 없음 | 해당 없음 |
| **Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn\_expenses)** | 예 | 없음 | 해당 없음 | 없음 | 해당 없음 |
| **시간 추정용 Project Operations 통합 엔터티(msdyn\_resourceassignments)** | 예 | 없음 | 해당 없음 | 없음 | 해당 없음 |


4. 엔터티를 새로 고치려면 맵 이름을 선택한 다음 **엔터티 새로 고침** 을 선택합니다. 


![맵 새로 고침](./media/20RefreshMapping.png)

5. 새로 고침이 완료된 후 맵을 실행합니다. 다음 맵을 활성화하기 전에 테이블의 맵이 **실행 중** 상태인지 확인합니다. 많은 수의 필수 구성 요소가 있는 맵을 실행하는 데 시간이 걸릴 수 있습니다.

필수 구성 요소가 있는 맵을 실행하려면 **관련 엔터티 맵 표시** 토글을 활성화합니다. 테이블에 **필수 구성 요소 초기 동기화** 가 **아니요** 로 나타나는 경우 실행하기 전에 모든 필수 구성 요소 맵에서 **초기 동기화** 플래그가 **끄기** 인지 확인합니다.

![맵 실행](./media/21RunMap.png)

6. 모든 프로젝트 관련 맵이 실행 중 상태인지 확인합니다.

![모든 맵 실행 중](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Project Operations용 CDS 에 구성 데이터 적용(선택 사항)

Finance 환경에 데모 데이터를 적용한 경우 [Project Operations에 대해 Common Data Service에서 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md)을 참조하여 CDS 환경에 데모 데이터를 적용합니다.


이제 Project Operations 환경이 프로비전 및 구성되었습니다. 
