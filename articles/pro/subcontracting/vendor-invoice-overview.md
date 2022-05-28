---
title: 공급업체 송장 발행 - 개념 및 생성
description: 이 항목에서는 공급업체 청구서의 개념, 사용 시나리오 및 Microsoft Dynamics 365 Project Operations에서 공급업체 청구서를 만드는 방법을 설명합니다.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580556"
---
# <a name="vendor-invoicing---concept-and-creation"></a>공급업체 송장 발행 - 개념 및 생성

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Microsoft Dynamics 365 Project Operations의 공급업체 송장 발행은 공급업체의 프로젝트에 대한 서비스 및/또는 자재 제공 비용을 기록하는 데 사용할 수 있습니다.

서비스 및/또는 재료가 공급업체에 하도급될 때 하도급 계약은 해당 공급업체와의 계약을 나타냅니다. 공급업체가 서비스를 제공하거나 자재를 받아 프로젝트 작업에 사용할 때 비용이 프로젝트에 기록됩니다. 정기적으로 공급업체는 확인되고 프로젝트에 기록된 비용과 일치하는 송장을 보냅니다. 확인 프로세스가 완료되면 공급업체 송장이 확인되고 지불을 위해 릴리스됩니다.

## <a name="scenarios-for-use"></a>사용 시나리오

Project Operations의 공급업체 송장은 두 가지 별개의 시나리오를 지원하는 데 사용할 수 있습니다.

### <a name="customers-use-the-full-subcontracting-experiences"></a>고객은 전체 하도급 계약 환경을 사용합니다.

공급업체 송장 환경은 하도급 계약 구성 요소를 참조하는 시간 항목, 자재 사용량 및 비용 항목을 확인하고 공급업체 송장 라인과 일치시키는 방법을 제공합니다. 이 프로세스는 공급업체 송장 라인의 정확성을 확인하는 데 사용할 수 있습니다. 검증 프로세스가 완료되고 공급업체 송장이 확인되면 애플리케이션은 승인된 시간, 비용 및 자재 사용 로그에 의해 기록된 실제 비용을 취소하고 공급업체 송장 라인을 사용하여 새로운 실제 비용을 생성합니다.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>고객은 전체 하도급 계약 환경을 사용하지 않지만 Project Operations에서 프로젝트 비용에 대한 통합 보기를 원합니다.

타사 시스템에서 하도급 계약 프로세스를 추적하는 경우 하도급 계약을 참조하지 않는 공급업체 송장을 생성하여 해당 타사 시스템의 비용을 Project Operations에 기록할 수 있습니다. 이러한 방식으로 프로젝트 관리자는 주어진 프로젝트의 모든 비용에 대한 단일 통합 보기를 가질 수 있습니다.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Project Operations에서 공급업체 송장 생성

공급업체 송장은 두 가지 방법으로 생성할 수 있습니다.

- 공급업체 송장 목록 페이지 또는 단일 공급업체 송장에 대한 세부 정보 페이지에서
- 하도급 계약 목록 페이지 또는 단일 하도급 계약에 대한 세부 정보 페이지에서

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>공급업체 송장 목록 페이지 또는 세부 정보 페이지에서 생성

1. **구매** \> **공급업체 송장** 으로 이동합니다.
2. 공급업체 송장 목록 페이지 또는 단일 공급업체 송장에 대한 세부 정보 페이지에서 **새로 만들기** 를 선택하여 새 공급업체 송장을 생성합니다.

이러한 방식으로 생성된 공급업체 송장은 하도급 계약도 참조할 수 있습니다.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>하도급 계약 목록 페이지 또는 세부 정보 페이지에서 생성

1. **구매** \> **하도급 계약** 으로 이동합니다.
2. 하나 이상의 하도급 계약을 선택합니다.
3. 하도급 계약 목록 페이지 또는 단일 하도급에 대한 세부 정보 페이지에서 **공급업체 송장 생성** 을 선택하여 새 공급업체 송장을 생성합니다.

선택한 각 하도급 계약에 대해 **초안** 상태의 새 공급업체 송장이 생성됩니다.

이 방법으로 생성하는 공급업체 송장은 항상 공급업체 송장 헤더의 하도급 계약을 참조합니다. 시간 및 자재 청구 방법이 있는 하도급 계약의 각 라인으로 인해 공급업체 송장에 라인이 생성됩니다. 고정 가격 청구 방법이 있는 하도급 계약의 각 라인은 **송장 준비 완료** 상태인 모든 하도급 계약 라인 마일스톤에 대해 공급업체 청구서에 라인이 생성되도록 합니다.

다음 필드 및 관련 레코드가 하도급 계약에서 공급업체 송장의 헤더로 복사됩니다.

- 공급업체.
- 관련 가격 목록은 가격 목록으로 공급업체 송장에 복사됩니다.
- 통화.
- 계약 단위.
- 지불 조건.

시간 및 자재 하도급 계약 내용의 경우 다음 필드 및 관련 레코드가 하도급 계약 내용에서 공급업체 송장 라인으로 복사됩니다.

- 하도급 계약 및 하도급 계약 내용 참조
- 거래 등급
- 역할
- 처리 카테고리
- 제품 필드
- Project
- 작업
- 예약 가능한 리소스

고정 가격 하도급 계약 내용의 경우 하도급 계약 내용 및 하도급 계약 내용 마일스톤에서 공급업체 송장 라인으로 다음 필드가 복사됩니다.

- 하도급 계약 및 하도급 계약 내용 참조.
- 트랜잭션 클래스. 기본적으로 값은 **마일스톤** 이 됩니다.
- 마일스톤 이름 및 금액은 관련 하도급 계약 내용 마일스톤에서 복사됩니다.
- 사용자는 공급업체 송장 라인에서 프로젝트와 작업을 선택할 수 있습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
