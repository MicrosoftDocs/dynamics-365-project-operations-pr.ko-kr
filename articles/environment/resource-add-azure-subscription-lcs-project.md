---
title: LCS 프로젝트에 Azure 구독 추가
description: 이 항목은 Azure 구독을 LCS 프로젝트에 연결하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e4502c1dec3bfeed083186b2d053549fefc9339609946c8da919b46e0e56cc79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986679"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS 프로젝트에 Azure 구독 추가

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

클라우드 호스팅 환경은 기존 Azure 구독을 사용하여 배포해야 합니다. 이 항목은 기존 Azure 구독을 LCS 프로젝트에 연결하는 방법을 설명합니다. 

## <a name="grant-admin-consent"></a>관리자 동의 부여

1. LCS 프로젝트의 **환경** 섹션에서 **Microsoft Azure 설정** 을 선택합니다.

![Microsoft Azure 설정.](./media/1MicrosoftAzureSettings.png)

2. **Azure 커넥터** 탭의 **프로젝트 설정** 페이지에서 **승인** 을 선택합니다. 이를 통해 이 프로젝트에 환경을 배포할 수 있습니다.

![Azure 커넥터.](./media/2AzureConnectors.png)

3. **승인** 을 다시 선택하여 관리자 동의를 제공합니다.

![관리자 동의 부여.](./media/3GrantAdminConsent.png)

4. 권한 요청을 수락합니다.

![권한 요청 수락.](./media/4AcceptPermissionRequest.png)

이제 인증이 완료되었습니다. 

![승인 성공.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Azure 구독에 대한 Dynamics 배포 서비스 액세스 제공

1. [Microsoft Azure 청구](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)로 이동하여 구독을 선택합니다. Dynamics Deployment Services는 환경을 배포할 수 있으려면 이 구독에 액세스해야 합니다.

![Azure 구독 정보.](./media/6AzureSubscription.png)

2. 탐색 창에서 **액세스 제어(IAM)** 를 선택한 다음 **역할 할당 추가** 를 선택합니다.
3. 오른쪽의 슬라이더에서 **Contributor 역할** 을 클릭하고 제공된 목록에서 **Dynamics 배포 서비스** 를 선택합니다. 
4. **저장** 을 선택합니다.

![구독 액세스.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>LCS 프로젝트에 구독 커넥터 추가

1. LCS 프로젝트의 **Microsoft Azure 설정** 페이지에서 **추가** 를 선택하여 새 커넥터를 추가합니다.
2. Azure 구독 ID를 입력합니다. Azure 구독 ID는 [Azure 포털](https://ms.portal.azure.com/)의 **설정** 아래 화면 왼쪽 하단에 있습니다.
3. **Azure Resource Manager를 사용하도록 구성** 필드에서 **예** 를 선택합니다.
4. Azure의 구독 AAD 테넌트 도메인이 사용 중인 도메인 소유 Azure 구독과 일치하는지 확인하고 **다음** 을 선택합니다.
5. **Microsoft Azure 설정** 화면에서 **다음** 을 선택하여 확인합니다. 이 화면에 오류가 표시되면 이 항목의 [Azure 구독에 대한 Dynamics 배포 서비스 액세스 제공](#provide) 섹션으로 돌아가서 모든 단계를 완료했는지 확인하십시오.
6. 컴퓨터의 로컬 폴더에 Azure 관리 인증서를 다운로드합니다. 구독을 선택하고 **설정** > **관리 인증서** 로 이동하여 Azure 구독 관리자에게 인증서를 Azure 관리 포털에 업로드하도록 요청합니다. 이 인증서를 사용하면 LCS가 사용자를 대신하여 Azure와 통신할 수 있습니다. 사용자에게 구독에 대한 액세스 권한이 있는 경우 이 단계를 건너뛸 수 있습니다.
7. **다음** 을 선택합니다.
8. 배포할 Azure 지역을 선택하고 이 시스템을 사용하려는 위치와 가까운 데이터 센터를 선택합니다.
9.  **연결** 을 선택합니다.

Azure 구독을 성공적으로 연결했습니다. 이제 Dynamics 365 Finance 클라우드 호스팅 환경을 배포할 수 있습니다.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
