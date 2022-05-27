---
title: Project Operations의 공급업체 및 구매 가격표 관리
description: 이 항목에서는 하도급을 위한 공급업체 데이터와 구매 가격표를 만들고 유지 관리하는 데 도움이 되는 정보를 제공합니다.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576738"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Project Operations의 공급업체 및 구매 가격표 관리

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

## <a name="vendors-in-project-operations"></a>Project Operations 공급업체

Microsoft Dynamics 365 Project Operations에서 공급업체 계정의 관계 유형은 **공급업체** 또는 **공급자** 입니다. 이러한 관계 유형 중 하나가 하청 계약의 공급업체로 포함된 계정 레코드만 선택할 수 있습니다.

하나 이상의 구매 가격표를 공급업체 레코드와 연결할 수 있습니다. 그러나 공급업체 레코드와 연결된 각 구매 가격표에는 고유한 날짜 유효성이 있어야 합니다. Project Operations는 구매 가격표에 대한 중복 날짜 유효성을 지원하지 않습니다.

기본적으로 공급업체 레코드의 다음 필드와 개념은 공급업체에 대해 생성된 모든 하도급 계약에 사용됩니다.

- 지불 조건
- 청구지 연락처
- 주 연락처

    > [!NOTE]
    > 기본적으로 공급업체의 기본 연락처는 하도급 계약의 공급업체 거래처 관리자로 사용됩니다.

- 통화
- 현재 구매 가격표

## <a name="purchase-price-lists-in-project-operations"></a>Project Operations의 구매 가격표

**컨텍스트** 필드가 **구매** 로 설정된 가격표는 구매 가격표로 간주됩니다. 구매 가격표는 시간, 경비 및 자재에 대한 구매율 카탈로그를 나타내도록 정의할 수 있습니다. 구매 가격표는 Project Operations의 비용 및 판매 가격표와 유사합니다. 다음 개념은 원가 및 판매 가격표에 적용되는 것과 동일한 방식으로 구매 가격표에 적용됩니다.

- **날짜 유효성** – 구매 가격표에는 날짜 유효성이 있습니다. 날짜 유효성은 각 가격표의 시작 날짜 및 종료 날짜 필드로 표시됩니다. 시작 날짜와 종료 날짜 사이의 시간이 날짜 유효 기간입니다.
- **통화** – 가격표 헤더의 통화는 카탈로그의 인건비, 경비 범주 및 제품에 대해 구매 가격이 표시되는 통화로 사용됩니다.
- **기본 시간 단위** – 기본 시간 단위는 구매에 대한 노동 가격을 나타냅니다. 가격표의 시간 단위 필드는 기본값을 제공하는 데만 사용됩니다. 해당 값은 개별 역할 가격 행에서 변경할 수 있습니다.

구매 가격표는 프로젝트 가격표라고 하는 연관으로 공급업체 레코드에 첨부될 수 있습니다. 이 가격표는 하도급 계약 라인에 기본 가격을 입력하는 데 사용됩니다. 기본적으로 여러 구매 가격표가 공급업체 레코드에 첨부된 경우 가장 최신 가격표가 공급업체에 대해 생성된 하도급 계약에 사용됩니다. **컨텍스트** 필드가 **구매** 로 설정된 가격표만 공급업체 레코드에 첨부할 수 있습니다.

### <a name="subcontract-specific-purchase-price-lists"></a>하도급 계약별 구매 가격표

구매 가격표는 프로젝트 가격표라고 하는 연관으로 하도급 계약에 첨부될 수도 있습니다. 이 가격표는 하도급 계약 라인에 기본 가격을 입력하는 데 사용됩니다. 기본적으로 여러 구매 가격표가 하도급 계약에 첨부된 경우 각 목록에 고유한 날짜 유효성이 있어야 합니다. Project Operations는 날짜 유효성이 중복되는 구매 가격표를 지원하지 않습니다. **컨텍스트** 필드가 **구매** 로 설정된 가격표만 하도급 계약에 첨부할 수 있습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
