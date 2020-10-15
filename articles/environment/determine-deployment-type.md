---
title: 배포 유형
description: 이 항목에서는 회사에 적합한 Project Operations 배포 유형을 결정하는 데 도움이 되는 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948958"
---
# <a name="deployment-types"></a>배포 유형

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

> [!IMPORTANT]
> 라이선스를 구매한 후 여기에서 시작하여 [안내식 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적 배포 모델을 결정합니다.
> 안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다. 설치를 완료하려면 아래 배포 세부 정보를 참조하십시오.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객
Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다. 향후 이러한 고객을 위한 업그레이드 경로가 릴리스될 예정입니다.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객 

프로젝트 관리 및 회계 기능을 사용하는 기존 재무 고객은 그대로 계속 사용할 수 있습니다. [리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.

Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다. 신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.

[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다. 결과는 다음 배포 유형 중 하나로 안내합니다.

- [라이트 배포 - 견적 송장 거래](#lite)
- [리소스/비 재고 시나리오에 대한 Project Operations](#integrated)
- [리소스/생산 주문 시나리오에 대한 Project Operations](#pma)

Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다. 예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)의 재고/생산 주문 기능과 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비재고/리소스 기반 기능을 활용할 수 있습니다.

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>라이트 배포 - 견적 송장 거래
라이트 배포에는 다음 기능이 포함됩니다.

- 웹용 Microsoft Project를 사용한 프로젝트 계획
- 다차원 가격 책정
- 통합 리소스 관리
- 시간 추적
- 기본 경비
- 송장 제안

### <a name="deployment-steps"></a>배포 단계:
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오. 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>리소스/비 재고 시나리오에 대한 Project Operations
리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.
  
- 웹용 Microsoft Project를 사용한 프로젝트 계획
- 다차원 가격 책정
- 통합 리소스 관리
- 시간 추적
- 기본 경비
- 전체 경비
- OCR 영수증
- 전체 송장 발행
- 수익 인식

### <a name="deployment-steps"></a>배포 단계:
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오. 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>리소스/생산 주문 시나리오에 대한 Project Operations

- WBS를 사용한 프로젝트 계획
- 리소스 관리
- 시간 추적
- 전체 경비
- OCR 영수증
- 전체 송장 발행
- 수익 인식
- 생산 주문
- 재료 지원

### <a name="deployment-steps"></a>배포 단계:
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) 및 [새로운 환경 제공](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)을 참조하십시오. 



