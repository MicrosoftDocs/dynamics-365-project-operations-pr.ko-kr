---
title: 프로젝트 구매 주문을 사용하여 프로젝트에 대한 비 재고 재료 주문
description: 이 문서에서는 프로젝트 구매 주문을 사용하여 프로젝트에 대한 비 재고 재료를 주문하는 방법에 대해 설명합니다.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929820"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>프로젝트 구매 주문을 사용하여 프로젝트에 대한 조달 범주 또는 재고가 없는 자재 주문

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

조직의 조달 부서에서는 [구매 주문](/dynamics365/supply-chain/procurement/purchase-order-overview)을 사용하여 상품 및 서비스 주문을 추적할 수 있습니다. 조달 범주 또는 재고가 없는 자재에 대한 구매 주문은 프로젝트에 기인할 수 있습니다. 이러한 구매 주문을 송장 발행하면 프로젝트에 대한 비용이 기록됩니다.

## <a name="prerequisites"></a>필수 조건
프로젝트 구매 주문 기능을 활성화하려면 다음 단계를 완료하십시오.

1. Dynamics 365 Finance에서 **기능 관리** 작업 영역으로 이동합니다.
2. 기능 목록에서 기능을 찾아 선택하고, **리소스 기반/비재고 시나리오에 대한 Project Operations에서 프로젝트 구매 주문을 활성화** 합니다.
3. **사용** 을 선택합니다.
4. [비 재고 재료 및 보류 중인 공급업체 송장 구성](configure-materials-nonstocked.md)에 설명된 대로 비 재고 재료 및 보류 중인 공급업체 송장을 구성합니다.
5. [프로젝트 구매 주문 및 보류 중인 공급업체 송장에 조달 범주 사용](configure-procurement-categories.md)에 설명된 대로 조달 범주를 구성합니다.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>프로젝트 구매 주문 목록에서 프로젝트 구매 주문 생성

1. Finance에서 **프로젝트 관리 및 회계** > **프로젝트** > **모든 프로젝트** 로 이동하고 프로젝트를 선택합니다.
2. 작업 창의 **관리** 탭에 있는 **새** 그룹에서 **항목 작업** > **구매 주문** 을 선택합니다.
3. **구매 주문 생성** 페이지에서 구매 주문을 하려는 공급업체를 선택하고 적절하게 기타 정보를 입력한 다음 **확인** 을 선택합니다.
4. **구매 주문** 페이지의 **구매 주문 라인** 그리드에서 **라인 추가** 를 선택합니다.
5. 품목 번호 또는 조달 범주, 수량, 단위, 단가 및 기타 정보를 적절하게 입력합니다.

    > [!NOTE]
    > 조달 범주, 재고가 없는 품목 및 서비스만 프로젝트 구매 주문에 사용할 수 있습니다. 재고 품목은 지원되지 않습니다.

6. 계속해서 필요에 따라 항목 또는 조달 범주를 추가하고 구매 주문을 확인합니다.

    상품 및 서비스 영수증은 제품 영수증을 작성하여 게시하여 기록할 수 있습니다.

    > [!NOTE]
    > 제품 영수증은 Microsoft Dataverse에서 프로젝트 실제에 기록되지 않으며 프로젝트 보조원장에 영향을 미치지 않습니다.

    공급업체가 구매 주문에 대한 항목 및 서비스에 대한 송장을 보낸 후 조달 부서는 작업 창에서 **송장** > **생성** > **송장** 으로 이동하여 구매 주문에 대한 송장을 생성할 수 있습니다. 보류 중인 공급업체 송장에 대한 자세한 내용은 [보류 중인 공급업체 송장을 사용하여 비 재고 재료 구매](pending-vendor-invoices.md)를 참조하십시오.
