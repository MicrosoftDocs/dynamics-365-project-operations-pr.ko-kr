---
title: Finance and Operations 및 Project Service Automation 간에 프로젝트 비용 범주 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Finance 및 Dynamics 365 Project Service Automation 간에 프로젝트 경비 범주를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999859"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations 및 Project Service Automation 간에 프로젝트 비용 범주 동기화

[!include[banner](../includes/banner.md)]

이 항목에서는 Dynamics 365 Finance 및 Dynamics 365 Project Service Automation 간에 프로젝트 경비 범주를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.

> [!NOTE]
> - 프로젝트 작업 통합, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 기능 잠금은 버전 8.0에서 사용할 수 있습니다.
> - 실제 통합은 버전 8.0.1 이상에서 사용할 수 있습니다.
> - KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다. 회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Project Service Automation 및 Finance를 위한 데이터 흐름

Project Service Automation 및 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Finance와 Project Service Automation 간에 프로젝트 경비 트랜잭션 범주에 대한 데이터 흐름을 사용할 수 있습니다.

프로젝트 경비 범주가 Finance에서 마스터되는 경우 통합 흐름은 먼저 Finance에서 Project Service Automation으로 진행됩니다. 그런 다음 Project Service Automation에서 Finance 로의 동기화를 통해 프로젝트 경비 범주의 통합 ID가 업데이트됩니다.

프로젝트 경비 범주가 Project Service Automation에서 마스터되는 경우 통합 흐름은 먼저 Project Service Automation에서 Finance로 진행됩니다. 프로젝트 범주는 Project Service Automation에서 동기화하기 전에 Finance에 이미 구성되어 있어야 합니다. 그런 다음 Finance에서 Project Service Automation으로 다시 동기화한 다음 Project Service Automation에서 Finance로 다시 동기화합니다. 이러한 방식으로 범주가 연결되고 중복이 생성되지 않도록 보장할 수 있습니다.

> [!NOTE]
> 일반적으로 프로젝트 경비 범주는 Finance에서 마스터됩니다. 그러나 그렇지 않거나 Project Service Automation에서 경비 범주가 이미 생성된 경우 먼저 프로젝트 경비 트랜잭션 범주(PSA에서 Fin 및 Ops로) 템플릿을 사용하여 동기화해야 합니다. 그런 다음 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿을 사용하여 동기화합니다. 그런 다음 Project Service Automation에서 Finance로 동기화를 한 번 더 실행해야 합니다.
>
> Project Service Automation에서 먼저 동기화하는 경우 동기화를 실행하기 전에 Finance에서 다음 요구 사항을 충족해야 합니다.
>
> - Project Service Automation에서 설정된 프로젝트 범주와 일치하는 공유 범주가 있어야 하며 **프로젝트** 와 **경비** 두 범주 모두에 대해 활성화되어야 합니다.
> - 통합해야 하는 각 Finance 법인에 대해 다음 프로젝트 범주가 존재해야 합니다.
>
>     - **프로젝트 범주** 가 존재합니다. 
>     - **경비에 사용** 이 활성화됩니다.
>     - **저널에서 활성화** 가 활성화됩니다.
>     - **트랜잭션 유형** 이 **경비** 로 설정됩니다.

다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.

[![Project Service Automation과 Finance 통합을 위한 데이터 흐름](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Finance에서 Project Service Automation으로의 프로젝트 경비 범주 동기화

### <a name="template-and-task"></a>템플릿 및 작업

템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.

다음 템플릿 및 기본 작업은 Finance에서 Project Service Automation으로 프로젝트 경비 범주를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로)
- **프로젝트의 작업 이름:** 범주를 PSA에 동기화

### <a name="entity-set"></a>엔터티 집합

| 재무                           | Project Service Automation |
|-----------------------------------|----------------------------|
| 범주를 위한 통합 엔터티 | 트랜잭션 범주     |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 경비 범주는 Finance에서 관리되며 트랜잭션 범주로 Project Service Automation에 동기화됩니다.

### <a name="power-query"></a>파워 쿼리

Project Service Automation에 동기화할 때 Microsoft Excel용 파워 쿼리를 사용하여 트랜잭션 범주에 대한 청구 유형을 설정해야 합니다. 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿은 기본 열 및 매핑을 제공합니다. 고유한 템플릿을 만드는 경우 파워 쿼리에서 이 조건부 열을 추가해야 합니다. 다음 단계를 수행합니다.

1. 화살표를 클릭하여 프로젝트 경비 트랜잭션 범주(Fin 및 Ops에서 PSA로) 템플릿에서 프로젝트 경비 범주 작업의 매핑을 엽니다.
2. **고급 쿼리 및 필터링** 링크를 클릭하여 파워 쿼리를 엽니다.
2. **조건부 열 추가** 를 선택합니다.
3. 새 열의 이름(**BillingType**)을 입력합니다.
4. 다음 조건을 입력합니다. **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. 열에서 **확인** 을 클릭합니다.
6. 매핑 페이지에서 이 새 열을 매핑해야 합니다.

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Finance에서 Project Service Automation으로 동기화될 필드 정보를 보여줍니다.

[![프로젝트 경비와 Project Service Automation 템플릿 매핑](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Project Service Automation에서 Finance로의 프로젝트 경비 범주 동기화

### <a name="template-and-task"></a>템플릿 및 작업

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 경비 범주를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 경비 트랜잭션 범주(PSA에서 Fin 및 Ops로)
- **프로젝트의 작업 이름:** 범주를 Fin Ops에 동기화

### <a name="entity-set"></a>엔터티 집합

| Project Service Automation | 재무                           |
|----------------------------|-----------------------------------|
| 트랜잭션 범주     | 범주를 위한 통합 엔터티 |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 경비 범주는 Finance에서 관리되며 트랜잭션 범주로 Project Service Automation에 동기화됩니다. Project Service Automation의 통합 ID를 사용하여 Finance로의 동기화가 다시 Finance에서 프로젝트 범주를 업데이트합니다.

### <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다.

> [!NOTE]
> 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![Project Service Automation과 Finance 템플릿 매핑](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]