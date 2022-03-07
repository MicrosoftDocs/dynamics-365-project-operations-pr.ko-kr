---
title: 미리 보기 구독 신청 - 라이트
description: 이 항목은 Project Operations 라이트 배포 - 견적 송장 거래를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5ba43ba9f917da068415fb62067ab73433b701139ee07014b6bd8c02612008ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991539"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>미리 보기 구독 신청 - 라이트 

이 항목에서는 평가판을 구독하고 Dynamics 365 Project Operations 라이트 배포를 배포하는 방법에 대해 설명합니다.

> [!NOTE]
> 이 프로세스는 Project Operations의 향후 릴리스에서 변경됩니다.

## <a name="prerequisites"></a>필수 조건
- 미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다. 첫 번째 제안 사용 중에 테넌트를 만들 수 있습니다.

> [!IMPORTANT]
> 조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다. 이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.
> 
> 평가판은 테넌트에서 일회용입니다. 평가판은 한 번만 실행할 수 있습니다. 평가판을 위해 새 테넌트를 만드는 것이 좋습니다.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations 평가판 

시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.

1. [Project Operations 평가판](https://aka.ms/try-po)으로 이동하여 첫 번째 제안 코드인 **Dynamics 365 Project Operations** 를 사용합니다.
2. 주문을 확인합니다.

  확인 제안이 성공적으로 사용되었음을 확인할 수 있습니다.

## <a name="assign-licenses"></a>라이선스 할당

> [!IMPORTANT]
> 다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.


1. [Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.
2. **활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.
3. **Dynamics 365 Project Operations** 라이선스가 선택되었는지 확인합니다. 
4. **변경 내용 저장** 을 선택합니다.

## <a name="create-a-new-dataverse-environment"></a>새 Dataverse 환경 만들기

1. 항목 [Dataverse 배포 모델](lite-deployment.md)의 지침에 따라 새 Project Operations Dataverse 배포 환경을 프로비전합니다. 환경 유형을 선택할 때 **평가판(구독 기반)** 을 사용해야 합니다.

  ![새 환경.](./media/19CreateEnvironment.png)

2. **Dynamics 365 앱 사용** 설정을 선택하고 **이러한 앱 자동 배포** 를 비워둡니다.  
3. **저장** 을 선택하여 환경을 만듭니다.

  ![데이터베이스 추가.](./media/20CreateEnvironment1.png)

4. 환경이 생성된 후 **Microsoft Dynamics 365 Project Operations** 솔루션을 설치합니다. 

![솔루션 설치.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS 구성 설치 및 데모 데이터 설정

항목 [데모 설정 및 구성 데이터 적용](lite-apply-demo-setup-config-data.md)의 지침에 따라 CDS 구성을 설치하고 데모 데이터를 설정합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
