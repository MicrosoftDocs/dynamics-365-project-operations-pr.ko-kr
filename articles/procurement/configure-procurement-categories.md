---
title: 프로젝트 구매 주문 및 보류 중인 공급업체 송장과 함께 조달 범주 사용
description: 이 항목에서는 프로젝트 구매 주문 및 보류 중인 공급업체 송장과 함께 사용할 수 있는 조달 범주를 구성하는 방법을 설명합니다.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613291"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>프로젝트 구매 주문 및 보류 중인 공급업체 송장과 함께 조달 범주 사용

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

구매 전문가는 프로젝트 구매 주문 및 보류 중인 공급업체 송장에 사용할 수 있는 항목 및 서비스의 카탈로그를 만들고 유지 관리할 수 있습니다. [조달 카탈로그](/dynamics365/supply-chain/procurement/procurement-catalogs)는 출시된 제품 카탈로그를 구성하고 사용할 필요 없이 구매를 분류할 수 있는 쉬운 방법을 제공합니다. 각 조달 범주는 시간, 경비 또는 품목 트랜잭션에 대한 프로젝트 범주에 매핑될 수 있습니다. 조달 범주를 사용하는 보류 중인 공급업체 송장이 전기된 후 시스템은 시간, 경비 또는 자재 프로젝트 실제 값, 프로젝트 트랜잭션 및 보조원장 입력을 생성합니다.

## <a name="minimum-version-requirements"></a>최소 버전 요구 사항

Microsoft Dynamics 365 Project Operations 비재고/리소스 기반 시나리오에 대한 프로젝트 구매 주문과 함께 조달 범주를 사용하려면 다음 버전이 필요합니다.

- Project Operations Dataverse 솔루션 버전 4.41.0.45 이상
- Finance and Operations 환경 버전 10.0.26 이상

## <a name="run-dual-write-maps-for-procurement-category-support"></a>조달 범주 지원을 위한 이중 쓰기 맵 실행

**Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티 msdyn\_projectvendorinvoicelines** 에 대한 매핑이 버전 1.0.0.4 이상을 사용하는지 확인합니다.

## <a name="enable-the-feature-key-for-procurement-categories"></a>조달 범주에 대한 기능 키 활성화

프로젝트 구매 주문과 함께 조달 범주를 사용하는 기능을 활성화하려면 다음 단계를 따르십시오.

1. Dynamics 365 Finance에서 **기능 관리** 작업 영역을 엽니다.
1. 기능 목록에서 **리소스 기반/비재고 시나리오에 대한 Project Operations의 조달 범주 사용** 기능을 찾은 다음 **활성화** 를 선택합니다.

> [!IMPORTANT]
> 전제 조건으로 **리소스 기반/비재고 시나리오에 대해 Project Operations에서 보류 중인 공급업체 송장 활성화** 기능도 활성화해야 합니다.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>조달 범주 계층 구조에서 프로젝트 범주 매핑

프로젝트 범주를 **조달 범주** 계층 구조의 조달 범주에 매핑하려면 다음 단계를 따르십시오.

1. **조달 및 소싱 \> 조달 범주** 로 이동합니다.
1. **범주 계층 구조 편집** 을 선택합니다.
1. 원하는 범주 계층 구조 노드를 선택한 다음 **프로젝트 범주 할당** 탭의 **시간**, 경비 또는 **품목 프로젝트** 범주(즉, **기본 시간** 또는 **기본 경비** 범주)와 노드를 연결합니다.
1. **저장** 을 선택합니다.
1. 창을 닫습니다.

> [!NOTE]
> 조달 범주를 프로젝트 범주에 매핑하는 것은 선택 사항입니다. 조달 범주가 매핑되지 않은 경우 시스템은 **프로젝트 관리 및 회계 매개 변수** 페이지의 **Dynamics 365 Customer engagement의 Project Operations** 탭에 있는 **프로젝트 범주 기본값** 섹션의 **항목** 필드에 설정된 값을 사용합니다.
