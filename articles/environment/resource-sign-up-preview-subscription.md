---
title: 리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록
description: 이 항목은 리소스/비 재고 기반 시나리오에 대한 Project Operations를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276851"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

이 항목은 미리 보기/파트너 제안을 구독하고 리소스/비 재고 시나리오를 위한 Project Operations 환경을 배포하는 방법을 설명합니다.

## <a name="prerequisites"></a>필수 구성 요소

- 미리 보기에 참여하도록 초대하는 이메일을 받게 됩니다. [Project Operations 웹 사이트](https://dynamics.microsoft.com/en-us/project-operations/overview/)에서 미리 보기를 요청할 수 있습니다.
- 미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다.
- Finance 환경을 배포하려면 환경별로 요금이 청구되는 유효한 Azure 구독이 필요합니다. 조직의 기존 구독을 사용하거나 [Azure 평가판](https://azure.microsoft.com/en-us/free/)을 사용하여 시작할 수 있습니다. CDS 환경은 제한된 30일 동안 무료로 제공됩니다.

## <a name="subscribe"></a>구독

[미리 보기 요청](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)이 승인되면 이메일로 Microsoft로부터 세 가지 제안을 받게 됩니다. 이러한 제안을 통해 Project Operations 미리 보기를 배포할 수 있습니다.

- Dynamics 365 Project Operations (CRM) - 평가판 미리 보기
- Office 365 Project Operations - 평가판 미리 보기
- Dynamics 365 Finance - 평가판 미리 보기

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 평가판 미리 보기

환영 이메일의 마지막 제안에 대해 동일한 단계를 반복하십시오.

## <a name="assign-licenses"></a>라이선스 할당

> [!IMPORTANT]
> 다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.

1. [Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.

![관리 센터 홈 페이지](./media/14AdminPortal.png)

2. **활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.

![라이선스 할당](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations(CRM) 미리 보기** 및 **Office 365 Project Operations - 미리보기** 라이선스가 선택되었는지 확인하고 **변경 사항 저장** 을 선택합니다.

> [!NOTE]
> Finance 평가판 제안은 사용자에게 할당할 필요가 없습니다.

## <a name="start-a-new-project-in-lcs"></a>LCS에서 새 프로젝트 시작

항목 [LCS에서 새 프로젝트 시작](create-lcs-project.md)에 설명된 대로 새 LCS 프로젝트를 만듭니다.

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS 프로젝트에 Azure 구독 추가

이 작업을 완료하려면 항목 [LCS 프로젝트에 Azure 구독 추가](resource-add-azure-subscription-lcs-project.md)의 단계를 따릅니다.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>리소스/비 재고 시나리오를 위한 Project Operations과 함께 Finance 데모 환경 배포

항목 [새로운 환경 프로비전](resource-provision-new-environment.md)의 안내를 따라 배포를 완료합니다. 미리 보기를 위한 [데모 환경](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 배포 유형을 사용합니다. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS 설정 및 구성 데이터 설치

항목 [Common Data Service에서 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md)에 설명된 대로 CDS 설정 및 구성 데이터를 설치합니다.
Finance 데모 환경이 배포되고 FO의 데모 데이터가 준비된 후에만 이 단계를 완료합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]