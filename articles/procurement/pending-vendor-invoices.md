---
title: 보류 중인 공급업체 송장을 사용하여 재고가 없는 자재 또는 조달 범주 구매
description: 이 항목에서는 보류 중인 공급업체 송장을 기록하는 방법을 설명합니다.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612665"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>보류 중인 공급업체 송장을 사용하여 재고가 없는 자재 또는 조달 범주 구매

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

회사에서 프로젝트에 대해 재고가 없는 자재 또는 조달 범주를 조달할 때 프로젝트에 대해 비용을 즉시 기록할 수 있습니다. 

예를 들어 Contoso Robotics US는 장비 갱신 프로젝트를 수행하고 있으며 소프트웨어 라이선스가 필요합니다. 이러한 라이선스는 타사 공급업체에서 조달합니다.  Dynamics 365 Finance를 사용하여 미지급금 사무원은 보류 중인 공급업체 송장 문서를 기록하고 라이선스 비용을 장비 갱신 프로젝트에 직접 반영합니다. 

> [!IMPORTANT]
> 이 항목에 설명된 기능을 사용하기 전에 필요한 구성을 검토하고 적용하십시오. 자세한 내용은 [비재고 자재 및 보류 중인 공급업체 송장 활성화](configure-materials-nonstocked.md) 및 [프로젝트 구매 주문 및 보류 중인 공급업체 송장에 조달 범주 사용](configure-procurement-categories.md)을 참조하십시오.

## <a name="post-a-project-related-pending-vendor-invoice"></a>프로젝트 관련 보류 중인 공급업체 송장 전기 

보류 중인 공급업체 송장은 **보류 중인 공급업체 송장** 페이지 (**지급 계정** > **송장** > **보류 중인 공급업체 송장**)에 기록할 수 있습니다. 프로젝트 관련 보류 중인 공급업체 송장을 전기하려면 다음 단계를 완료하십시오.

1. **지급 계정** > **송장** 으로 이동하고 **새로 만들기** 를 선택합니다. 
1. **송장 계정** 필드에서 공급업체를 선택한 다음 **번호** 필드에 공급업체 송장 ID를 입력합니다.
1. 공급업체 송장에 라인을 추가한 다음 **항목 번호** 필드에서 공급업체로부터 구매한 비재고 품목을 선택합니다. 또는 **조달 범주** 필드에서 공급업체로부터 구매한 조달 범주를 선택합니다.   
1. 구매한 수량을 추가합니다. 시스템은 비재고 품목 가격 구성을 기반으로 단가를 채웁니다. 
1. 라인에서 총액 및 기타 필수 세부 사항을 확인하십시오.
1. 라인 세부 정보에서 **프로젝트** 탭에서 이 항목이 기록될 프로젝트의 ID를 선택합니다.
1. 선택 사항: 활동 번호를 선택하고 프로젝트 범주 및 라인 속성을 업데이트합니다.
1. 보류 중인 공급업체 송장을 전기합니다. 송장이 전기되면 시스템은 다음 정보를 기록합니다.
    
    - 공급업체 잔액.
    - 판매세 금액.
    - 프로젝트에 대한 비용은 조달 통합 계정에 기록됩니다.
    - Dataverse의 프로젝트 실제 비용 트랜잭션.  이 트랜잭션은 [Project Operations 통합 저널](../project-accounting/project-operations-integration-journal.md)을 사용하여 추가 처리됩니다. 이 분개장을 전기하면 금액이 조달 통합 계정에서 프로젝트 원가 계정으로 이동합니다. 
    - 시간 및 자재 청구 방법을 사용하여 프로젝트 고객에게 청구되는 구매입니다. 또한 Dataverse에서 구매에 대해 청구되지 않은 판매 트랜잭션이 생성됩니다. Dataverse의 제품 가격표는 판매 가격 및 미청구 판매 거래 금액에 사용됩니다.
