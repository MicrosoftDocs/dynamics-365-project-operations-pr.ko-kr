---
title: 비 재고 재료 및 보류 중인 공급업체 송장 구성
description: 이 항목은 비 재고 재료 및 보류 중인 공급업체 송장을 활성화하는 방법을 설명합니다.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880663"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>비 재고 재료 및 보류 중인 공급업체 송장 구성

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

## <a name="minimum-version-requirement"></a>최소 버전 요구 사항

Dynamics 365 Project Operations 비 재고/리소스 기반 시나리오를 위한 비 재고 재료 및 보류 중인 공급업체 송장을 사용하려면 다음 버전이 필요합니다.

Dynamics 365 Dataverse 솔루션:

- Project Operations – 4.9.0.221 이상
- 이중 쓰기 애플리케이션 오케스트레이션 솔루션 - 2.2.2.23 이상

Dynamics 365 Finance:
- 10.0.18(10.0.793.52) 이상. Finance 환경이 최신 상태이고 모든 품질 업데이트가 최소 버전 요구 사항을 충족하도록 적용되었는지 확인합니다.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>비 재고 재료 및 공급업체 송장 통합을 위한 이중 쓰기 맵 실행

이 섹션에서는 비 재고 재료 및 공급업체 송장에 필요한 특정 맵에 대한 정보를 제공합니다. [새로운 환경 제공](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) 항목에 나열된 전제 조건 맵이 사용자 환경에서 실행 중인지 확인하십시오.

1. Lifecycle Services(LCS)로 이동하고 LCS 프로젝트로 이동한 다음 **환경 세부 정보** 페이지로 이동합니다.
2. **Common Data Service 환경 정보** 섹션에서 **앱용 CDS 링크** 를 선택합니다. 링크를 선택하면 매핑의 엔터티 목록으로 리디렉션됩니다.
3. 다음 맵이 실행 중인지 확인하십시오. 실행 중이 아니면 시작하고 모든 관련 테이블 맵을 포함해야 합니다.

    - CDS는 고유한 제품(제품)을 출시했습니다.
    - 공급업체 v2(msdyn_vendors)
    - 재료 견적을 위한 Project Operations 테이블(msdyn_estimatelines)
    - Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn_projectvendorinvoices)
    - Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn_projectvendorinvoicelines)
    - Project Operations 통합 실제(msdyn_actuals). 맵 버전 1.0.0.14 이상을 실행하고 있는지 확인하십시오. **이중 쓰기** 페이지의 **버전** 열에서 맵의 활성 버전을 볼 수 있습니다. **테이블 맵 버전** 을 선택한 다음 선택한 버전을 저장하여 새 버전의 맵을 활성화할 수 있습니다.

표준 데모 데이터를 사용하는 경우 초기 동기화를 통해 다음 엔터티 맵을 중지했다가 다시 시작해야 할 수도 있습니다.
  - 지불 날짜 CDS V2(msdyn_paymentdays)
  - 지불 일정(msdyn_paymentschedules)
  - 지불 조건(msdyn_paymentterms)
  - 공급업체 그룹(msdyn_vendorgroups)
  - 단위(uom)

> [!NOTE]
> 공급업체 그룹 및 장치에 대한 초기 동기화가 기존 데모 데이터 집합의 일부 레코드에 대해 실패할 수 있습니다. 실패는 Project Operations에서 데모 데이터를 사용하는 것을 방해하지 않으므로 무시할 수 있습니다.

## <a name="configure-prerequisites-in-dataverse"></a>Dataverse에서 필수 구성 요소 구성

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>공급업체 엔터티를 기반으로 계정을 생성하는 워크플로 활성화

이중 쓰기 오케스트레이션 솔루션은 [공급업체 마스터 통합](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping)을 제공합니다. 이 기능의 전제 조건으로 공급업체 데이터는 **계정** 엔터티에서 만들어야 합니다. 템플릿 워크플로 프로세스를 활성화하여 [공급업체 설계 간 전환](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type)에 설명된 **계정** 표에 공급업체를 만듭니다.

### <a name="set-products-to-be-created-as-active"></a>생성할 제품을 활성으로 설정

비 재고 재료는 Finance에서 **릴리스된 제품** 으로 구성해야 합니다. 이중 쓰기 오케스트레이션 솔루션은 즉시 사용 가능한 [Dataverse 제품 카탈로그에 릴리스된 제품 통합](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping)을 제공합니다. 기본적으로 Finance의 제품은 초안 상태의 Dataverse에 동기화됩니다. 재료 사용 문서 또는 보류 중인 공급업체 송장에서 직접 사용할 수 있도록 제품을 활성 상태로 동기화하려면 **시스템** > **관리** > **시스템 관리** > **시스템 설정** 으로 이동한 다음 **영업** 탭에서 **활성 상태의 제품 만들기** 를 **예** 로 설정합니다.

## <a name="configure-prerequisites-in-finance"></a>Finance에서 필수 구성 요소 구성

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>보류 중인 공급업체 송장에 대한 기능 키 활성화

보류 중인 공급업체 송장 라인에 프로젝트 상세 내역을 추가하는 기능을 활성화하려면 다음 단계를 완료하십시오.

1. Finance에서 **기능 관리** 작업 영역으로 이동합니다.
2. 기능 목록에서 **리소스 기반/비 재고 시나리오를 위해 Project Operations에서 보류 중인 공급업체 송장 활성화** 기능을 찾아 **활성화** 를 선택합니다.

### <a name="define-category-groups-and-project-categories-for-items"></a>항목에 대한 범주 그룹 및 프로젝트 범주 정의

**항목** 트랜잭션 유형에 대해 하나 이상의 범주 그룹 및 이 그룹을 사용하는 하나 이상의 프로젝트 범주를 구성합니다. 자세한 내용은 [프로젝트 범주 구성](../project-accounting/configure-project-categories.md#category-groups)을 참조하십시오.

프로젝트 원가 및 수익 프로필을 검토하고 품목 트랜잭션에 대한 원장 전기 설정을 구성합니다. 자세한 내용은 [청구 가능 프로젝트에 대한 회계 구성](../project-accounting/configure-accounting-billable-projects.md)을 참조하십시오.

### <a name="set-up-a-write-in-product"></a>직접 입력 제품 설정

Project Operations에서 릴리스된 제품 카탈로그에 구성된 카탈로그 제품 및 직접 입력 제품에 대한 재료 견적 및 사용량을 기록할 수 있습니다. 직접 입력 제품을 사용하려면 이 목적을 위해 Finance에서 구성된 단일 릴리스 제품이 필요합니다. 다음 단계를 완료하여 직접 입력 제품을 구성합니다. 리소스/비 재고 시나리오에 대해 Project Operations를 사용하는 각 법인에서 이 단계를 반복합니다.

1. Finance에서 **제품 정보 관리** > **제품** > **릴리스된 제품** 으로 이동하고 **새로 만들기** 를 선택합니다.
2. **제품 유형** 필드에서 **항목** 을 선택하고 **제품 하위 유형** 필드에서 **제품** 을 선택합니다.
3. 제품 번호(WRITEIN)와 제품 이름(직접 입력 제품)을 입력합니다.
4. 항목 모델 그룹을 선택합니다. 선택한 항목 모델 그룹에 **재고 정책 재고 제품** 필드가 **False** 로 설정되어 있는지 확인하십시오.
5. **항목 그룹**, **스토리지 차원 그룹** 및 **차원 그룹 추적** 필드에서 값을 선택합니다. **사이트** 에만 **저장소 크기** 를 사용하고 추적 크기를 설정하지 마십시오.
6. **재고 단위**, **구매 단위** 및 **판매 단위** 필드에서 값을 선택한 다음 변경 사항을 저장합니다.
7. **계획** 탭에서 기본 주문 설정을 지정하고 **재고** 탭에서 기본 사이트 및 창고를 설정합니다.
8. **프로젝트 관리 회계** > **설정** > **프로젝트 관리 및 회계 매개 변수** 로 이동하고 **Dynamics 365 Dataverse의 Project Operations** 를 엽니다. 
9. **재료** 탭의 **직접 입력 제품** 필드에서 생성한 제품을 선택합니다.
10. Dataverse 환경의 사이트 맵에서 **제품** 엔터티를 열고 직접 입력 제품 레코드를 찾습니다. 
11. 레코드 세부 정보를 열고 제품 상태를 **사용 중지됨** 으로 설정합니다. 이 제품 상태는 재료 견적 및 사용 문서에서 실수로 이 레코드를 직접 사용하는 것을 방지합니다.

### <a name="set-up-a-procurement-integration-account"></a>조달 통합 계정 설정

조달 통합 계정은 프로젝트에 귀속된 라인이 있는 보류 중인 공급업체 송장을 전기할 때 임시 계정으로 사용됩니다.

시스템에서 보류 중인 공급업체 송장을 전기할 때 이 계정이 프로젝트 원가 금액에 사용됩니다. 공급업체 송장 세부 정보는 Dataverse에서 처리되고 해당 프로젝트 실제가 생성됩니다. 실제 프로젝트의 정보는 Project Operations 통합 분개장에 추가됩니다. 통합 분개장을 전기하면 금액이 조달 통합 계정에서 반제되고 프로젝트 비용에 기록됩니다.

1. 조달 통합 계정을 설정하려면 **프로젝트 관리 회계** > **설정** > **프로젝트 관리 및 회계 매개 변수** 로 이동하고 **Dynamics 365 Dataverse의 Project Operations** 를 엽니다. 
2. **재료** 탭을 선택하고 **조달 통합 계정** 필드에서 값을 선택합니다.

#### <a name="set-up-project-category-defaults-for-an-item"></a>항목에 대한 프로젝트 범주 기본값 설정

1. Finance에서 **프로젝트 관리 회계** > **설정** > **프로젝트 관리 및 회계 매개 변수** 로 이동하고 **Dynamics 365 Dataverse의 Project Operations** 를 엽니다. 
2. **프로젝트 범주 기본값** 탭의 **항목** 필드에서 값을 선택합니다. 이 프로젝트 범주는 프로젝트 범주가 프로젝트 실제 레코드에 설정되지 않은 경우 재료 트랜잭션에 사용됩니다.
