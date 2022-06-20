---
title: 배포 유형 결정
description: 이 문서에서는 회사에 대한 올바른 배포 유형의 프로젝트 작업을 결정하는 데 도움이 되는 정보를 제공합니다.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912202"
---
# <a name="determine-your-deployment-type"></a>배포 유형 결정

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

> [!IMPORTANT]
> 라이선스를 구입한 후 여기에서 시작하여 [안내 설치 흐름](https://aka.ms/provisionprojectoperations)을 사용하여 Dynamics 365 Project Operations의 최적의 배포 모델을 결정하십시오.
> 안내식 설치 흐름을 완료한 후 올바른 관리 포털로 이동하여 설치를 완료합니다. 설치를 완료하려면 배포 세부 정보를 참조하십시오.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation을 사용하는 Dynamics의 기존 고객
Project Operations에는 Project Service Automation과 함께 제공되는 기능이 포함됩니다. 2021년 릴리스 웨이브 1에서 이러한 고객을 위한 업그레이드 경로가 릴리스됩니다.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>프로젝트 관리 및 회계를 사용하는 Dynamics 365 Finance의 기존 고객 

프로젝트 관리 및 회계 기능을 사용하는 기존 Finance 고객은 그대로 계속 사용할 수 있습니다. [리소스/생산 주문 시나리오에 대한 Project Operations](#pma)를 참조하십시오.


## <a name="deployment-regions"></a>배포 지역
Project Operations 배포를 지원하는 지역을 확인하려면 [Dynamics 365 및 Power Platform의 지리적 가용성 보고서](https://dynamics.microsoft.com/en-us/geographic-availability/)를 참조하십시오. **보고서 보기** 를 선택하고 **Dynamics 365 > 운영 앱 > Dynamics 365 Project Operations** 를 확장하고 지원되는 지역을 봅니다.

## <a name="deployment-types"></a>배포 유형
Project Operations는 요구 사항에 맞는 여러 배포 옵션을 지원합니다. 신규 또는 기존 Dynamics 365 고객에 관계 없이 Project Operations는 귀사의 요구를 지원할 수 있습니다.

[배포 설문지](https://aka.ms/provisionprojectoperations)는 올바른 배포를 결정하는 데 도움이 됩니다. 결과는 다음 배포 유형 중 하나로 안내합니다.

- [라이트 배포 - 견적 송장 거래](#lite)
- [리소스/비 재고 시나리오에 대한 Project Operations](#integrated)
- [리소스/생산 주문 시나리오에 대한 Project Operations](#pma)

Project Operations는 법인 수준 구성을 통해 동일한 환경에서 재고/생산 주문 시나리오와 비재고/리소스 기반 시나리오를 지원합니다. 예를 들어 Contoso는 미국 제조 시설(법인 = Contoso Manufacturing United States)에서 재고/생산 주문 기능을 사용할 수 있습니다. Contoso는 영국의 Contoso Robotics Arms 서비스 시설(법인 = Contoso Robotics United Kingdom)에서 비 재고/리소스 기반 기능을 사용할 수 있습니다.

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>라이트 배포 - 견적 송장 거래

라이트 배포에는 다음 기능이 포함됩니다.

- Dynamics 365 Sales 애플리케이션 경험을 확장하는 프로젝트의 영업 프로세스
- 웹용 Microsoft Project를 사용한 프로젝트 계획
- 다차원 가격 책정
- 통합 리소스 관리
- 시간 추적
- 기본 경비
- 프로젝트 관리자의 검토 및 편집을 위한 견적 송장 

#### <a name="deployment-steps"></a>배포 단계
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](lite-preview-subscription-sign-up.md) 및 [새로운 환경 제공](lite-deployment.md)을 참조하십시오. 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>리소스/비 재고 시나리오에 대한 Project Operations
리소스/비재고 시나리오에 대한 Project Operations에는 다음 기능이 포함됩니다.
 
- Dynamics 365 Sales 애플리케이션을 확장하는 프로젝트의 영업 프로세스
- 웹용 Microsoft Project를 사용한 프로젝트 계획
- 다차원 가격 책정
- 통합 리소스 관리
- 시간 추적
- 기본 경비
- 전체 경비
- OCR 영수증
- 견적 및 고객 대면 송장 발행 
- 프로젝트의 수익 인식

#### <a name="deployment-steps"></a>배포 단계
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](resource-sign-up-preview-subscription.md) 및 [새로운 환경 제공](resource-provision-new-environment.md)을 참조하십시오. 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>리소스/생산 주문 시나리오에 대한 Project Operations

- WBS를 사용한 프로젝트 계획
- 리소스 관리
- 시간 추적
- 전체 경비
- OCR 영수증
- 전체 송장 발행
- 수익 인식
- 생산 주문
- 재고가 있는 재고 자재 지원

#### <a name="deployment-steps"></a>배포 단계
[배포 설문지](https://aka.ms/provisionprojectoperations)를 사용하여 Project Operations의 최상의 배포 모델을 결정합니다.

이 배포의 경우 [미리 보기 구독 신청](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) 및 [새로운 환경 제공](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json)을 참조하십시오. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]