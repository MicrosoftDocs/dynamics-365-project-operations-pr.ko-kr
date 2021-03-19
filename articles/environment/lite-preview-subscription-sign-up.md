---
title: 미리 보기 구독 신청 - 라이트
description: 이 항목은 Project Operations 라이트 배포 - 견적 송장 거래를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290052"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>미리 보기 구독 신청 - 라이트 

이 항목은 미리 보기 파트너 제안을 구독하고 Dynamics 365 Project Operations 라이트 배포 - 견적 송장 처리를 배포하는 방법을 설명합니다.

> [!NOTE]
> 이 프로세스는 Project Operations의 향후 릴리스에서 변경됩니다.

## <a name="prerequisites"></a>필수 구성 요소

- 미리 보기에 참여하도록 초대하는 이메일을 받게 됩니다. [Project Operations 웹 사이트](https://dynamics.microsoft.com/en-us/project-operations/overview/)에서 미리 보기를 요청할 수 있습니다.
- 미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.
- 모든 이용 약관을 검토하십시오.

## <a name="subscribe"></a>구독

[미리 보기 요청](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) 승인을 받으면 이메일로 Microsoft로부터 두 가지 제안을 받게 됩니다. 이러한 제안을 통해 Project Operations 미리 보기를 배포할 수 있습니다.

- Dynamics 365 Project Operations (CRM) - 평가판 미리 보기
- Office 365 Project Operations - 평가판 미리 보기

> [!IMPORTANT]
> 조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다. 이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - 평가판 미리 보기 

시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.

1. 브라우저 URL에 붙여 넣어 첫 번째 제안 코드 **Dynamics 365 Project Operations(CRM) - 평가판 미리보기** 를 사용합니다.

![초대 제안](./media/16RedeemFirstOfferNew.png)

2. 주문을 확인합니다.
![주문 확인](./media/17ConfirmOrderNew.png)

확인 제안이 성공적으로 회수되었음을 확인하는 메시지가 표시됩니다.

![확인](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - 평가판 미리 보기

첫 번째 제안 코드와 동일한 단계를 반복합니다. 첫 번째 제안 코드에 사용된 것과 동일한 사용자 계정을 사용하여 두 번째 제안 코드를 추가해야 합니다.

## <a name="assign-licenses"></a>라이선스 할당

> [!IMPORTANT]
> 다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.


1. [Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.

![관리 센터 홈 페이지](./media/14AdminPortal.png)

2. **활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.

![라이선스 할당](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations(CRM) 미리 보기** 및 **Office 365Project Operations - 미리 보기** 라이센스가 선택되었는지 확인합니다. 
4. **변경 내용 저장** 을 선택합니다.

## <a name="create-a-new-cds-environment"></a>새 CDS 환경 만들기

1. 항목 [CDS 배포 모델](lite-deployment.md)의 지침에 따라 새 Project Operations CDS 배포 환경을 프로비전합니다. 환경 유형을 선택할 때 **평가판(구독 기반)** 을 사용해야 합니다.
![새 환경](./media/19CreateEnvironment.png)

2. **Dynamics 365 앱 사용** 설정을 선택하고 **이러한 앱 자동 배포** 를 비워둡니다.  
3. **저장** 을 선택하여 환경을 만듭니다.

![데이터베이스 추가](./media/20CreateEnvironment1.png)

4. 환경이 생성된 후 **Microsoft Dynamics 365 Project Operations** 솔루션을 설치합니다. 

![솔루션 설치](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS 구성 설치 및 데모 데이터 설정

항목 [데모 설정 및 구성 데이터 적용](lite-apply-demo-setup-config-data.md)의 지침에 따라 CDS 구성을 설치하고 데모 데이터를 설정합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]