---
title: 리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록
description: 이 문서에서는 리소스/비재고 기반 시나리오에 대해 Project Operations를 구독하고 배포하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842024"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>리소스/비 재고 시나리오에 대한 Project Operations 미리 보기 구독에 등록

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_



이 문서에서는 평가판을 구독하고 리소스/비재고 기반 시나리오를 위해 Project Operations 환경을 배포하는 방법을 설명합니다.

## <a name="prerequisites"></a>필수 조건
- 미리 보기를 배포하는 사용자는 Azure 테넌트 전역 관리자 권한이 있어야 합니다. 첫 번째 제안 사용 중에 테넌트를 만들 수 있습니다. 
- Finance 환경을 배포하려면 환경별로 요금이 청구되는 유효한 Azure 구독이 필요합니다. 조직의 기존 구독을 사용하거나 [Azure 평가판](https://azure.microsoft.com/free/)을 사용하여 시작할 수 있습니다. CDS 환경은 제한된 30일 동안 무료로 제공됩니다.

> [!IMPORTANT]
> 조직의 테넌트 관리자인 한 사람만이 작업을 수행하면 됩니다. 이 릴리스의 구독자가 아닌 경우 조직이 등록되고 사용자 자격 증명을 받을 때까지 기다리십시오.
> 
> 평가판은 테넌트에서 일회용입니다. 평가판은 한 번만 실행할 수 있습니다. 평가판을 위해 새 테넌트를 만드는 것이 좋습니다.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations(CE) - 평가판 미리 보기 

시작하기 전에 프로젝트 작업 미리 보기를 원하는 테넌트의 사용자 작업 계정으로 브라우저에 로그인했는지 확인합니다.

1. 첫 번째 제안 코드 **Dynamics 365 Project Operations** 여기[ Project Operations 평가판](https://aka.ms/try-po)을 사용합니다.
2. 주문을 확인합니다.

  확인 제안이 성공적으로 회수되었음을 확인하는 메시지가 표시됩니다.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 미리 보기 평가판

[Dynamics 365 for Finance 미리 보기 평가판](https://aka.ms/trypoche)으로 이동하고 제안의 이전 섹션의 단계를 반복하고 클라우드 호스팅 환경에 가입합니다.  

## <a name="assign-licenses"></a>라이선스 할당

> [!IMPORTANT]
> 다음 단계를 완료하려면 조직의 Microsoft 365 포털에서 관리 액세스 권한이 필요합니다.

1. [Microsoft 365 관리 센터](https://portal.office.com/)로 이동하여 사용자에게 라이선스를 할당합니다.

2. **활성 사용자** 페이지에서 라이선스를 할당할 사용자를 선택합니다.

3. **Dynamics 365 Project Operations** 라이선스가 선택되었는지 확인하고 **변경 사항 저장** 을 선택합니다.

> [!NOTE]
> Finance 평가판 제안은 사용자에게 할당할 필요가 없습니다.

## <a name="start-a-new-project-in-lcs"></a>LCS에서 새 프로젝트 시작

[LCS에서 새 프로젝트 시작](create-lcs-project.md) 문서에 설명된 대로 새 LCS 프로젝트를 만듭니다.

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS 프로젝트에 Azure 구독 추가

이 작업을 완료하려면 [LCS 프로젝트에 Azure 구독 추가](resource-add-azure-subscription-lcs-project.md) 문서의 단계를 따르십시오.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>리소스/비 재고 시나리오를 위한 Project Operations과 함께 Finance 데모 환경 배포

[새 환경 프로비저닝](resource-provision-new-environment.md) 문서의 지침에 따라 배포를 완료합니다. 미리 보기를 위한 [데모 환경](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) 배포 유형을 사용합니다. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS 설정 및 구성 데이터 설치

[Common Data Service의 구성 데이터 설정 및 적용](resource-apply-pro-setup-config-data.md) 문서에 설명된 대로 CDS 설정 및 구성 데이터를 설치합니다.
Finance 데모 환경이 배포되고 데모 데이터가 준비된 후에만 이 단계를 완료하십시오.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
