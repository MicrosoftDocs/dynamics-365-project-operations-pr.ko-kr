---
title: Finance and Operations에 전기를 위해 Project Service Automation에서 프로젝트 통합 저널로 프로젝트 실제 데이터를 직접 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Finance and Operations로 직접 프로젝트 실제를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988119"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Finance and Operations에 전기를 위해 Project Service Automation에서 프로젝트 통합 저널로 프로젝트 실제 데이터를 직접 동기화

[!include[banner](../includes/banner.md)]

이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 실제를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.

템플릿은 Project Service Automation의 트랜잭션을 Finance의 준비 테이블로 동기화합니다. 동기화가 완료되면 준비 테이블의 데이터를 통합 저널로 **반드시** 가져와야 합니다.

> [!NOTE]
> - 프로젝트 실제 통합은 버전 8.0.1부터 사용할 수 있습니다.
> - KB 4132657 및 KB 4132660를 설치한 후 Enterprise Edition 7.3.0을 사용하는 경우 템플릿을 사용하여 프로젝트 작업, 경비 트랜잭션 범주, 시간 추정, 경비 추정 및 실제를 통합하고 기능 잠금을 구성할 수 있습니다. 회계 분포를 재설정해야 하는 경우 KB 4131710도 설치하는 것이 좋습니다.
> - 버전 7.3.0을 사용 중이고 Project Service Automation에서 수수료 거래를 가져오는 경우 프로젝트 송장에 해당 수수료를 포함하려면 KB 4345320를 설치해야 합니다.
> - Project Service Automation에서 시간 또는 경비 트랜잭션에 대한 판매세 금액을 입력하는 경우 Project Service Automation 업데이트 7을 설치해야 합니다. 그렇지 않으면 실제 세금이 관련 시간 또는 실제 경비에 연결되지 않고 Finance에 동기화되지 않습니다. 자세한 내용은 지원 부서에 문의하십시오.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation에서 Finance까지의 데이터 흐름

Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 실제에 대한 데이터 흐름을 사용할 수 있습니다.

다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.

[![Project Service Automation과 Finance and Operations 통합을 위한 데이터 흐름.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation의 프로젝트 실제

### <a name="template-and-tasks"></a>템플릿 및 작업

사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 실제를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 실제(PSA에서 Fin 및 Ops까지)
- **프로젝트에서 작업의 이름:**

    - 실제
    - TransactionConnections

### <a name="entity-set"></a>엔터티 집합

| Project Service Automation | 재무                                   |
|----------------------------|----------------------------------------------------------|
| 실제                    | 프로젝트 실제를 위한 통합 엔터티                   |
| 거래 연결    | 프로젝트 트랜잭션 관계를 위한 통합 엔터티 |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 실제는 Project Service Automation에서 관리되며 Finance에서 프로젝트 통합 저널과 동기화됩니다. 회계는 기본 재무 차원 및 전기 설정을 기반으로 적용됩니다.

### <a name="prerequisites"></a>필수 구성 요소

실제 동기화가 발생하기 전에 Project Service Automation 통합 매개 변수를 구성하고 프로젝트, 프로젝트 작업 및 프로젝트 경비 트랜잭션 범주를 동기화해야 합니다.

### <a name="power-query"></a>파워 쿼리

프로젝트 실제 템플릿에서 Microsoft Excel용 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.

- Project Service Automation의 트랜잭션 유형을 Finance의 올바른 트랜잭션 유형으로 변환합니다. 이 변환은 프로젝트 실제(PSA에서 Fin 및 Ops로) 템플릿에 이미 정의되어 있습니다.
- Project Service Automation의 청구 유형을 Finance의 올바른 청구 유형으로 변환합니다. 이 변환은 프로젝트 실제(PSA에서 Fin 및 Ops로) 템플릿에 이미 정의되어 있습니다. 그런 다음 청구 유형은 **Project Service Automation 통합 매개 변수** 페이지의 구성에 따라 라인 속성에 매핑됩니다.
- 이 템플릿과 동기화해야 하는 특정 리소스 조직 단위로 필터링합니다.
- 회사 간 시간 또는 회사 간 비용 실제가 Finance에 동기화되는 경우 계약 조직 단위를 Finance의 올바른 법인으로 변환해야 합니다. 프로젝트 실제(PSA에서 Fin 및 Ops으로) 템플릿에서 조건부 열은 데모 데이터를 기반으로 정의됩니다. 마지막으로 삽입된 조건부 열을 올바른 법인으로 업데이트해야 합니다. 그렇지 않으면 통합 오류가 발생하거나 잘못된 실제 트랜잭션을 Finance로 가져올 수 있습니다.
- 회사 간 시간 또는 회사 간 경비 실제가 Finance에 동기화되지 않는 경우 템플릿에서 마지막으로 삽입된 조건부 열을 삭제해야 합니다. 그렇지 않으면 통합 오류가 발생하거나 잘못된 실제 트랜잭션을 Finance로 가져올 수 있습니다.

#### <a name="contract-organizational-unit"></a>연락처 조직 구성 단위
템플릿에서 삽입된 조건부 열을 업데이트하려면 **매핑** 화살표를 클릭하여 매핑을 엽니다. **고급 쿼리 및 필터링** 링크를 선택하여 파워 쿼리를 엽니다.

- 기본 프로젝트 실제(PSA에서 Fin 및 Ops까지) 템플릿을 사용하는 경우 파워 쿼리의 **적용 단계** 섹션에서 마지막 **삽입된 조건** 을 선택합니다. **함수** 항목에서 **USSI** 를 통합과 함께 사용해야 하는 법인의 이름으로 바꿉니다. 필요에 따라 추가 조건을 **함수** 항목에 추가하고 **USMF** 의 **else** 조건을 올바른 법인으로 업데이트합니다.
- 새 템플릿을 만드는 경우 회사 간 시간 및 경비를 지원하기 위해 열을 추가해야 합니다. **조건 열 추가** 를 선택하고 열의 이름(예: **LegalEntity**)을 입력합니다. 열에 대한 조건을 입력합니다. 여기서 **msdyn\_contractorganizationalunitid.msdyn\_name** 이 \<organizational unit\>인 경우 \<enter the legal entity\>, 그렇지 않으면 null입니다.

### <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![템플릿 매핑 - 실제.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![템플릿 매핑 - 트랜잭션 연결.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation에서 통합한 후 준비 테이블에서 가져오기

Project Service Automation에서 Finance로 실제 데이터를 동기화한 후 준비 테이블에서 가져오기 주기적 프로세스를 실행해야 합니다. 이 프로세스는 준비 테이블에서 Project Service Automation 통합 저널로 프로젝트 트랜잭션을 가져오며 여기에서 회계가 적용되고 가져온 트랜잭션을 전기할 수 있습니다. 이 프로세스를 배치 모드로 실행하는 것이 좋습니다. 반복 배치로 실행되도록 선택적으로 설정할 수 있습니다.

## <a name="update-actuals-from-finance"></a>Finance에서 실제 업데이트

### <a name="template-and-tasks"></a>템플릿 및 작업

다음 템플릿 및 기본 작업은 Finance에서 Project Service Automation으로 전기된 프로젝트 트랜잭션에 대한 바우처 번호 및 판매세를 동기화하는 데 사용됩니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 실제 업데이트(Fin Ops에서 PSA로)
- **프로젝트에서 작업의 이름:**

    - 실제 
    - TransactionConnections

### <a name="entity-set"></a>엔터티 집합

| 재무                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| 프로젝트 실제를 위한 통합 엔터티                   | 실제                    |
| 프로젝트 트랜잭션 관계를 위한 통합 엔터티 | 거래 연결    |

### <a name="entity-flow"></a>엔터티 흐름

프로젝트 실제는 Project Service Automation에서 관리되며 Finance에서 프로젝트 통합 저널과 동기화됩니다. 실제 값이 Finance에 전기된 후 Finance의 바우처 번호로 Project Service Automation에서 업데이트됩니다. Finance에 판매세가 추가된 경우 Project Service Automation에서 새 실제 세금이 생성됩니다.

### <a name="power-query"></a>파워 쿼리

프로젝트 실제 업데이트 템플릿에서 파워 쿼리를 사용하여 다음 작업을 완료해야 합니다.

- Finance의 트랜잭션 유형을 Project Service Automation의 올바른 트랜잭션 유형으로 변환합니다. 이 변환은 프로젝트 실제 업데이트(Ops에서 PSA로) 템플릿에 이미 정의되어 있습니다.
- Finance의 청구 유형을 Project Service Automation의 올바른 청구 유형으로 변환합니다. 이 변환은 프로젝트 실제 업데이트(Ops에서 PSA로) 템플릿에 이미 정의되어 있습니다.

### <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Finance에서 Project Service Automation으로 동기화될 필드 정보를 보여줍니다.

[![템플릿 매핑 - 실제 업데이트.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![템플릿 매핑 - 트랜잭션 업데이트.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]