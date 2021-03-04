---
title: Project Service Automation에서 Finance and Operations로 직접 프로젝트 추정치 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 시간 견적 및 프로젝트 경비 추정치를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080180"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Project Service Automation에서 Finance and Operations로 직접 프로젝트 추정치 동기화

[!include[banner](../includes/banner.md)]

이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 시간 견적 및 프로젝트 경비 추정치를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.

> [!NOTE]
> - 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.
> - 실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation에서 Finance까지의 데이터 흐름

Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 시간 추정 및 프로젝트 경비 추정에 대한 데이터 흐름을 사용할 수 있습니다.

다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.

[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>프로젝트 시간 추청치

### <a name="template-and-tasks"></a>템플릿 및 작업

사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 시간 추정치를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지)
- **프로젝트에서 작업의 이름:**

    - 트랜잭션 관계
    - 경비 추정

### <a name="entity-set"></a>엔터티 집합

| Project Service Automation | 재무                                       |
|----------------------------|-----------------------------------------------|
| 프로젝트 작업              | 프로젝트 시간 추정을 위한 통합 엔터티 |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 시간 추정치는 Project Service Automation에서 관리되며 프로젝트 시간 예측으로 Finance에 동기화됩니다.

### <a name="prerequisites"></a>필수 구성 요소

프로젝트 시간 추정치를 동기화하기 전에 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.

### <a name="power-query"></a>파워 쿼리

프로젝트 시간 예상 템플릿에서 Microsoft Excel용 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.

- 통합이 새 시간 예측을 생성할 때 사용할 기본 예측 모델 ID를 설정합니다.
- 시간 예측으로의 통합에 실패할 작업에서 리소스 별 레코드를 필터링합니다.
- 빈 트랜잭션 범주 행을 필터링합니다. 이 작업을 완료하지 못하면 시간 예측이 잘못될 수 있습니다.

#### <a name="set-the-default-forecast-model-id"></a>기본 예측 모델 ID 설정

템플릿에서 기본 예측 모델 ID를 업데이트하려면 **매핑** 화살표를 클릭하여 매핑을 엽니다. 그런 다음 **고급 쿼리 및 필터링** 링크를 선택합니다.

- 기본 프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 **적용 단계** 목록에서 **삽입된 조건** 을 선택합니다. **함수** 항목에서 **O\_forecast** 를 통합과 함께 사용해야 하는 예측 모델 ID의 이름으로 바꿉니다. 기본 템플릿에는 데모 데이터의 예측 모델 ID가 있습니다.
- 새 템플릿을 만드는 경우 이 열을 추가해야 합니다. 파워 쿼리에서 **조건 열 추가** 를 클릭하고 새 열의 이름(예: **ModelID** )을 입력합니다. 열에 대한 조건을 입력합니다. 여기서 프로젝트 작업이 null이 아닌 경우 \<enter the forecast model ID\>, 그렇지 않으면 null입니다.

#### <a name="filter-out-resource-specific-records"></a>리소스별 레코드 필터링

프로젝트 시간 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 리소스별 레코드를 제거하는 기본 필터가 있습니다. 고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다. **False** 인 레코드만 포함되도록 **msdyn\_islinetask** 열에서 필터링할 **고급 쿼리 및 필터링** 링크를 선택합니다.

#### <a name="filter-out-empty-transaction-category-rows"></a>빈 트랜잭션 범주 행을 필터링합니다.

트랜잭션 범주가 비어있는 행을 제거하려면 필터를 추가해야 합니다. 이 작업은 기본 템플릿을 사용하는지 또는 고유한 템플릿을 생성하는지에 관계없이 필요합니다. 이 필터는 Finance의 시간 예측이 잘못될 수 있는 모든 요약 행을 Project Service Automation에서 제거합니다. **고급 쿼리 및 필터링** 링크를 선택하여 **msdyn\_transactioncategory\_value** 열에서 null 레코드를 필터링합니다.

### <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![데이터 통합의 템플릿 작업 매핑](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>프로젝트 경비 추정치

### <a name="template-and-tasks"></a>템플릿 및 작업

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 경비 추정치를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지)
- **프로젝트에서 작업의 이름:**

    - 트랜잭션 관계 
    - 경비 추정

### <a name="entity-set"></a>엔터티 집합

| Project Service Automation | 재무                                                  |
|----------------------------|----------------------------------------------------------|
| 거래 연결    | 프로젝트 트랜잭션 관계를 위한 통합 엔터티 |
| 추정 라인             | 프로젝트 경비 추정을 위한 통합 엔터티         |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 경비 추정치는 Project Service Automation에서 관리되며 프로젝트 경비 예측으로 Finance에 동기화됩니다.

### <a name="prerequisites"></a>필수 구성 요소

프로젝트 경비 추정치를 동기화하기 전에 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.

### <a name="power-query"></a>파워 쿼리

프로젝트 경비 추정치 템플릿에서 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.

- 경비 추정 라인 레코드만 포함하도록 필터링합니다.
- 통합이 새 시간 예측을 생성할 때 사용할 기본 예측 모델 ID를 설정합니다.
- 청구 유형을 변환합니다.
- 트랜잭션 유형을 변환합니다.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>경비 추정 라인만 포함하도록 필터링합니다.

프로젝트 경비 추정(PSA에서 Fin 및 Ops까지) 템플릿에는 통합에 경비 라인만 포함하는 기본 필터가 있습니다. 고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다. **트랜잭션 관계** 작업을 선택한 다음 **매핑** 화살표를 클릭하여 매핑을 엽니다. **고급 쿼리 및 필터링** 링크를 선택합니다. **msdyn\_estimateline** 만 포함하도록 **msdyn\_transactiontype1** 열을 필터링합니다.

#### <a name="set-the-default-forecast-model-id"></a>기본 예측 모델 ID 설정

템플릿에서 기본 예측 모델 ID를 업데이트하려면 **경비 추정** 작업을 선택한 다음 **매핑** 화살표를 클릭하여 매핑을 엽니다. **고급 쿼리 및 필터링** 링크를 선택합니다.

- 기본 프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 파워 쿼리의 **적용 단계** 섹션에서 첫 번째 **삽입된 조건** 을 선택합니다. **함수** 항목에서 **O\_forecast** 를 통합과 함께 사용해야 하는 예측 모델 ID의 이름으로 바꿉니다. 기본 템플릿에는 데모 데이터의 예측 모델 ID가 있습니다.
- 새 템플릿을 만드는 경우 이 열을 추가해야 합니다. 파워 쿼리에서 **조건 열 추가** 를 클릭하고 새 열의 이름(예: **ModelID** )을 입력합니다. 열에 대한 조건을 입력합니다. 여기서 추정 라인 ID가 null이 아닌 경우 \<enter the forecast model ID\>, 그렇지 않으면 null입니다.

#### <a name="transform-the-billing-types"></a>청구 유형을 변환합니다

프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 통합 중에 Project Service Automation에서 받은 청구 유형을 변환하는 데 사용되는 조건부 열이 포함되어 있습니다. 고유한 템플릿을 만드는 경우 이 조건부 열을 추가해야 합니다. **고급 쿼리 및 필터링** 링크를 선택한 다음 **조건부 열 추가** 를 선택합니다. 새 열의 이름( **BillingType** )을 입력합니다. 그런 후에, 다음 조건을 입력합니다.

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>트랜잭션 유형을 변환합니다

프로젝트 경비 추정치(PSA에서 Fin 및 Ops까지) 템플릿에는 통합 중에 Project Service Automation에서 받은 트랜잭션 유형을 변환하는 데 사용되는 조건부 열이 포함되어 있습니다. 고유한 템플릿을 만드는 경우 이 조건부 열을 추가해야 합니다. **고급 쿼리 및 필터링** 링크를 선택한 다음 **조건부 열 추가** 를 선택합니다. 새 열의 이름( **TransactionType** )을 입력합니다. 그런 후에, 다음 조건을 입력합니다.

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![경비 추정 트랜잭션의 템플릿 매핑](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![경비 추정의 템플릿 매핑](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]