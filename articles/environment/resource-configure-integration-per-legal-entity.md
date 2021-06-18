---
title: 법인별 프로젝트 Project Operations 통합 구성
description: 이 항목은 Project Operations에서 법인에 의한 통합 설정에 대한 정보를 제공합니다.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000084"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>법인별 프로젝트 Project Operations 통합 구성 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 토픽은 법인 당 Dynamics 365 Project Operations 구성에 필요한 단계를 안내합니다.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dynamics 365 Finance에서 기능 키 활성화

필수 기능을 사용하려면 다음 단계를 완료하십시오.

1. Dynamics 365 Finance에서 **기능 관리** 작업 영역으로 이동합니다.
2. **기능 목록** 에서 다음 기능을 찾아 활성화합니다.
  
    - **프로젝트에 대해 여러 계약 내용 활성화**
    - **Dynamics 365 Customer Engagement에서 Project Operations 활성화**

> [!NOTE]
> **기능 키** 가 표시되지 않으면 Finance 버전이 최소 버전 요구 사항(모든 품질 업데이트가 적용된 응용 프로그램 버전 10.0.13 이상)을 충족하는지 확인합니다. **업데이트 확인** 을 선택하여 기능 목록을 새로 고칩니다.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>법인에 대한 Project Operations 배포 시나리오 정의

법인 수준의 Dynamics 365 Customer Engagement에서 Project Operations를 활성화할 수 있습니다. 리소스/비 재고 기반 시나리오의 경우 Dynamics 365 Customer Engagement에서 Project Operations를 사용하여 하나의 법인이 있을 수 있습니다. 동일한 환경에서 재고/생산 주문 시나리오에 대해 Project Operations를 사용하는 다른 법인이 있을 수 있습니다.

1. Dynamics 365 Finance에서 **프로젝트 관리 및 회계** > **설정** > **전역 프로젝트 관리 및 회계 매개 변수** 로 이동합니다.
2. 사용 가능한 법인 목록에서 Dynamics 365 Customer Engagement 기능의 여러 계약 내용 및 Project Operations가 활성화되는 엔터티를 선택합니다. 재고/생산 주문 시나리오에 대해 Project Operations를 사용할 법인은 선택하지 않은 상태로 둡니다.

> [!NOTE]
> 법인은 기존 프로젝트가 없는 경우에만 선택할 수 있습니다.

## <a name="configure-project-management-and-accounting-parameters"></a>프로젝트 관리 및 회계 매개 변수 구성

Dynamics 365 Customer Engagement에서 Project Operations를 사용하는 각 법인은 기본 매개 변수 집합이 필요합니다. 이러한 매개 변수는 **프로젝트 관리 및 회계 매개 변수** 페이지의 **Project Operations** 탭에 구성됩니다. 매개 변수는 다음과 같습니다.

  - **결제 유형 기본값**: Project Operations는 라인 속성 Finance에 매핑되어야 하는 고정된 청구 유형 기본값 세트를 사용합니다. 각 청구 유형 **지정하지 않음**, **청구 가능**, **청구 불가능**, **무료** 및 **사용할 수 없음** 에 대한 레코드를 만듭니다.
  - **프로젝트 범주 기본값**: 각 트랜잭션 유형에 사용할 기본 프로젝트 범주를 선택합니다. 이러한 기본값은 **Project Operations 통합 분개장** 및 실제 프로젝트에 대해 트랜잭션 범주가 지정되지 않은 추정에 사용됩니다.
  - **예측**: 시간 및 비용 추정에 사용할 예측 모델을 선택합니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]