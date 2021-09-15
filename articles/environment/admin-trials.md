---
title: Project Operations 평가판 등록
description: 이 주제는 Dynamics 365 Project Operations 평가판을 배포하는 방법에 대한 정보를 제공합니다.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418465"
---
# <a name="sign-up-for-project-operations-trials"></a>Project Operations 평가판 등록 

_**적용 대상:** 리소스/비 재고 기반 시나리오를 위한 Project Operations, 라이트 배포 - 견적 송장 처리 및 재고/생산 기반 시나리오를 위한 Project Operations_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

이 항목에서는 프리뷰 파트너 제안을 구독하고 Dynamics 365 Project Operations 환경을 배포하는 방법을 설명합니다.

새로운 Project Operations 평가판을 사용하면 최상의 배포 접근 방식을 권장하는 설문지를 작성하여 지원되는 세 가지 배포 시나리오 중 하나를 자동으로 배포할 수 있습니다. 이 항목은 다음 방법에 대한 정보를 제공합니다.

- 평가판 사용.
- 프로비저닝을 시작.
- 이중 쓰기 구성.
- Project Operations에 대해 자세히 알아보기. 

다음 표에는 새로운 평가판 제안에 대한 세부 정보가 나와 있습니다.

| **제안 항목**               | **세부 정보**                                  |
|------------------------------|----------------------------------------------|
| 제안 유형                   | 이 제안 유형은 관리자 잠재 고객이므로 사용하려면 테넌트 관리자가 필요합니다. |
| 제안 사용                    | 테넌트당 1회                          |
| 제안 기간               | 30일                             |
| 테넌트당 사용       | 6                                            |
| 사용자 수              | 25                                           |
| 확장명                    | 연장 1회, 30일               |
| 평가판 환경 수 | 3                                            |


## <a name="admin-trial-details"></a>관리자 평가판 세부정보
다음 표에는 평가판 세부 정보와 각 배포 유형에 적용되는 방법이 나와 있습니다.

| **상품**                      | **라이트**                                     | **비 재고 재료** | **재고 재료** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| 제공된 설정 데이터           | 예                                          | 예                       | 예(USSI)            |
| 처리 데이터            | 아니요                                           | 아니요                        | 아니요                    |
| 프로비저닝 시간(분)  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>필수 조건
Dynamics 365 Project Operations의 평가판을 배포하기 위해 다음과 같은 조건이 필요합니다.

- [Dynamics 365 Project Operations - 평가판 프리뷰](https://www.aka.ms/try-po)를 등록합니다.
- 미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.

> [!IMPORTANT]
> 조직의 한 사람인 테넌트 관리자만 이 작업을 수행하면 됩니다. 이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - 평가판 프리뷰 

시작하기 전에 Project Operations 프리뷰를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인합니다.

1. 브라우저 URL에 붙여 넣어 첫 번째 제안 코드 **Dynamics 365 Project Operations - 평가판 프리뷰** 를 사용합니다.

    ![초대 제안](./media/16RedeemFirstOfferNew.png)

2. 주문을 확인합니다.

    ![주문 확인](./media/17ConfirmOrderNew.png)

  확인 제안이 성공적으로 사용되었음을 확인할 수 있습니다.

   ![확인](./media/18OrderConfirmationNew.png)

  [Power Platform 관리 센터](https://admin.powerplatform.microsoft.com/projectoperationstrial)로 리디렉션됩니다.

## <a name="questionnaire-and-provisioning"></a>설문지 및 프로비저닝

1.  [Power Platform 관리 센터](https://admin.powerplatform.com/projectoperationstrial)로 이동하고 설문지를 작성합니다.  
2.  권장 배포 유형을 검토하고 **설정 시작** 을 선택하여 프로비저닝을 시작합니다.
3.  이용 약관을 검토하고 **시작** 을 선택합니다.

   프로비저닝이 시작되면 Power Platform 관리 센터의 환경 목록으로 리디렉션됩니다. 프로비저닝이 진행되는 동안 환경 상태는 **인스턴스 준비 중** 입니다.
 
  프로비저닝이 완료된 후 환경 상태는 **준비됨** 입니다.
 
4.  프로비저닝이 완료되면 해당하는 Microsoft Dataverse URL 및 Finance and Operations 앱 URL을 선택하여 배포를 확인합니다.

## <a name="demo-data-installation"></a>데모 데이터 설치

다음 링크를 사용하여 재고가 없는 재료 및 라이트 배포 시나리오에 대한 데모 데이터 패키지에 액세스합니다. 
- [비 재고 재료 데모 데이터](resource-apply-pro-setup-config-data.md)
- [라이트 데모 데이터](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>이중 쓰기 구성
비 재고 재료 배포의 경우에만 이중 쓰기 매핑을 구성합니다. 자세한 내용은 [Project Operations 이중 쓰기 맵 버전](resource-dual-write-maps.md)을 참조하십시오.

## <a name="assign-licenses"></a>라이선스 할당

다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.

1. [Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.

   ![관리 센터 홈 페이지](./media/14AdminPortal.png)

2. **활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.

   ![라이선스 할당](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations 프리뷰** 라이선스가 선택되었는지 확인하고 **변경 사항 저장** 을 선택합니다.

## <a name="additional-resources"></a>추가 리소스

다음 리소스는 Project Operations 여정을 시작할 때 유용한 지침을 제공합니다.

- [비디오 시리즈 - Project Operations 개요, 심층 분석 및 로드맵 제공](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [배포 유형 결정](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>자주 묻는 질문

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>내 Finance and Operations 앱 환경에 ALM 또는 ELM이 필요하면 어떻게 합니까?

- 전체 환경 수명 주기 관리 기능이 필요한 파트너는 [파트너 샌드박스 라이선스 요청](https://experience.dynamics.com/requestlicense)을 참조하여 새 파트너 제안을 검토합니다. 
- 내부 사용권에 대한 자세한 정보를 원하는 파트너는 [내부 사용권 클라우드 및 소프트웨어 혜택(microsoft.com)](https://partner.microsoft.com/membership/internal-use-software)을 참조하십시오.

### <a name="can-i-extend-my-trial-beyond-30-days"></a>평가판을 30일 이상 연장할 수 있습니까?
평가판을 연장하려면 다음 단계를 완료하십시오.

1. **Microsoft 365 관리 센터** 에서 **대금 청구** > **제품** 으로 이동합니다.
2. **Dynamics 365 Project Operations (CE) - 평가판 프리뷰** 를 선택합니다.
3. **만료 날짜** 아래에서 **날짜 연장** 을 선택합니다.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>라이트 배포에서 리소스/비재고 기반 시나리오 배포로 업그레이드할 수 있습니까?
현재, 라이트에서 비재고 기반 배포로 환경을 업그레이드하는 것은 지원되지 않습니다.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Finance 환경에서 LCS(Lifecycle Services)에 액세스할 수 있습니까?  
아니요 이러한 평가판의 경우 배포는 Power Platform 관리 센터를 통해 처리됩니다. Finance 환경에 대한 액세스가 제한됩니다.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>기존 환경에 평가판을 설치할 수 있습니까?
기존 환경이 있는 경우 Power Platform 관리 센터에서 기존 판매 Dataverse 환경에 라이트 배포를 설치할 수 있습니다.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
