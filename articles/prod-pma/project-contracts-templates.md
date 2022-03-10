---
title: Project Service Automation에서 Finance로 직접 프로젝트 계약 및 프로젝트 동기화
description: 이 항목에서는 Microsoft Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 계약 및 프로젝트를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.
author: Yowelle
ms.date: 12/17/2020
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: acb87be977cc009f89ceac5b01c9028d6741b552a441ef49e024b6b078a188d4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001079"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Project Service Automation에서 Finance로 직접 프로젝트 계약 및 프로젝트 동기화 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

이 항목에서는 Dynamics 365 Project Service Automation에서 Dynamics 365 Finance로 직접 프로젝트 계약 및 프로젝트를 동기화하는 데 사용되는 템플릿 및 기본 작업을 설명합니다.

> [!NOTE] 
> Enterprise 버전 7.3.0을 사용하는 경우 KB 4074835를 설치해야 합니다.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation에서 Finance까지의 데이터 흐름

> [!NOTE]
> Project Service Automation to Finance 통합 솔루션을 사용하려면 먼저 Dynamics 365 데이터 통합 기능에 익숙해야 합니다.

Project Service Automation에서 Finance 통합 솔루션은 데이터 통합 기능을 사용하여 Project Service Automation 및 Finance 인스턴스간에 데이터를 동기화합니다. 데이터 통합 기능과 함께 사용할 수 있는 통합 템플릿을 사용하면 Project Service Automation에서 Finance로 프로젝트 계약, 프로젝트, 프로젝트 계약 내용 및 프로젝트 계약 내용 중요 시점에 대한 데이터 흐름을 사용할 수 있습니다.

다음 그림은 Project Service Automation과 Finance 간에 데이터가 동기화되는 방식을 보여줍니다.

[![Project Service Automation과 Finance 통합을 위한 데이터 흐름.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>템플릿 및 작업

사용 가능한 템플릿에 액세스하려면 Microsoft Power Apps 관리 센터에서 **프로젝트** 를 선택한 다음 오른쪽 상단에서 **새 프로젝트** 를 선택하여 공개 템플릿을 선택합니다.

다음 템플릿 및 기본 작업은 Project Service Automation에서 Finance로 프로젝트 계약 및 프로젝트를 동기화하는 데 사용됩니다.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Dynamics 365 Project Service Automation v2.x와 통합
- **데이터 통합의 템플릿 이름:** 프로젝트 및 계약(Project Service Automation에서 Finance로)
- **프로젝트에서 작업의 이름:**

    - 프로젝트 계약 Project Service Automation에서 Finance로
    - 프로젝트 Project Service Automation에서 Finance로
    - 프로젝트 계약 내용 Project Service Automation에서 Finance로
    - 프로젝트 계약 내용 중요 시점 Project Service Automation에서 Finance로
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Dynamics 365 Project Service Automation v3.x와 통합
프로젝트 계약 내용 중요 시점 템플릿에 영향을 미치는 Project Service Automation의 스키마 변경이 있으며 Project Service Automation v3.x를 Dynamics 365과 통합하려면 v2 버전의 템플릿을 사용해야 합니다.

- **데이터 통합의 템플릿 이름:** 프로젝트 및 계약(Project Service Automation 3.x에서 Finance로) - v2
- **프로젝트에서 작업의 이름:**

    - 프로젝트 계약 Project Service Automation에서 Finance로
    - 프로젝트 Project Service Automation에서 Finance로
    - 프로젝트 계약 내용 Project Service Automation에서 Finance로
    - 프로젝트 계약 내용 중요 시점 Project Service Automation에서 Finance로

프로젝트 계약 및 프로젝트의 동기화가 발생하기 전에 계정을 동기화해야 합니다.

## <a name="entity-set"></a>엔터티 집합

| Project Service Automation       | 재무                                                |
|----------------------------------|--------------------------------------------------------|
| 주문                           | 프로젝트 계약을 위한 통합 엔터티                |
| 프로젝트                         | 프로젝트를 위한 통합 엔터티                         |
| 주문 라인                      | 프로젝트 계약 내용을 위한 통합 엔터티           |
| 프로젝트 계약 내용 중요 시점 | 프로젝트 계약 내용 중요 시점을 위한 통합 엔터티 |

## <a name="entity-flow"></a>엔터티 흐름

프로젝트 계약은 Project Service Automation에서 관리되며 프로젝트 계약으로 Finance에 동기화됩니다. 통합 템플릿의 일부로 Finance에서 프로젝트 계약에 대한 통합 소스를 설정할 수 있습니다.

시간과 재료 및 고정 가격 프로젝트는 Project Service Automation에서 관리되고 프로젝트로서 Finance에 동기화됩니다. 템플릿 통합의 일부로 Finance에서 프로젝트의 통합 소스를 설정할 수 있습니다. 현재 시간과 재료 및 고정 가격 프로젝트만 지원됩니다.


프로젝트 계약 내용은 Project Service Automation에서 관리되며 프로젝트 계약 청구 규칙으로 Finance에 동기화됩니다. 청구 방법이 기본 프로젝트 유형과 다른 경우 동기화는 계약 항목 프로젝트 및 프로젝트 그룹에 대한 프로젝트 유형을 업데이트합니다.

프로젝트 계약 내용 중요 시점은 Project Service Automation에서 관리되며 프로젝트 계약 청구 규칙 중요 시점으로 Finance에 동기화됩니다.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation에서 Finance 통합 솔루션

**프로젝트 계약 ID** 필드는 **프로젝트 계약** 페이지에서 사용할 수 있습니다. 이 필드는 통합을 지원하기 위해 자연스럽고 고유한 키로 만들어졌습니다.

새 프로젝트 계약이 생성될 때 **프로젝트 계약 ID** 값이 아직 존재하지 않으면 숫자 시퀀스를 사용하여 자동으로 생성됩니다. 값은 **ORD** 와 증가하는 숫자 시퀀스 및 6자 접미사가 이어집니다. 예를 들어 다음과 같습니다. **ORD-01022-Z4M9Q0**.

**프로젝트 번호** 필드는 **프로젝트** 페이지에서 사용할 수 있습니다. 이 필드는 통합을 지원하기 위해 자연스럽고 고유한 키로 만들어졌습니다.

새 프로젝트가 생성될 때 **프로젝트 번호** 값이 아직 존재하지 않으면 숫자 시퀀스를 사용하여 자동으로 생성됩니다. 값은 **PRJ** 와 증가하는 숫자 시퀀스 및 6자 접미사가 이어집니다. 예를 들어 다음과 같습니다. **PRJ-01049-CCNID0**.

Project Service Automation과 Finance 통합 솔루션이 적용되면 업그레이드 스크립트가 Project Service Automation에서 기존 프로젝트 계약의 **프로젝트 계약 ID** 필드 및 기존 프로젝트의 **프로젝트 번호** 필드를 설정합니다.

## <a name="prerequisites-and-mapping-setup"></a>필수 조건 및 매핑 설정

- 프로젝트 계약 및 프로젝트의 동기화가 발생하기 전에 계정을 동기화해야 합니다.
- 연결 세트에서 **msdyn\_organizationalunits** 에 대한 통합 키 필드 매핑을 **msdyn\_name \[Name\]** 에 추가합니다. 먼저 연결 세트에 프로젝트를 추가해야 할 수 있습니다. 자세한 내용은 [앱용 Common Data Service에 데이터 통합](/powerapps/administrator/data-integrator)을 참조하십시오.
- 연결 세트에서 **msdyn\_projects** 에 대한 통합 키 필드 매핑을 **msdynce\_projectnumber \[Project Number\]** 에 추가합니다. 먼저 연결 세트에 프로젝트를 추가해야 할 수 있습니다. 자세한 내용은 [앱용 Common Data Service에 데이터 통합](/powerapps/administrator/data-integrator)을 참조하십시오.
- 프로젝트 계약 및 프로젝트의 **SourceDataID** 는 다른 값으로 업데이트하거나 매핑에서 제거할 수 있습니다. 기본 템플릿 값은 **Project Service Automation** 입니다.
- **PaymentTerms** 매핑은 Finance의 유효한 지불 조건을 반영하도록 업데이트해야 합니다. 프로젝트 작업에서 매핑을 제거할 수도 있습니다. 기본값 맵에는 데모 데이터에 대한 기본값이 있습니다. 다음 표에는 Project Service Automation의 값이 나와 있습니다.

    | 값 | 설명   |
    |-------|---------------|
    | 1     | 30일        |
    | 2     | 2% 10일, 30일 |
    | 3     | 45일        |
    | 4     | 60일        |

## <a name="power-query"></a>파워 쿼리

다음 조건이 충족되는 경우 Excel용 Microsoft 파워 쿼리를 사용하여 데이터를 필터링합니다.

- Dynamics 365 Sales에 판매 주문이 있습니다.
- Project Service Automation에 여러 조직 단위가 있으며 이러한 조직 단위는 Finance의 여러 법인에 매핑됩니다.

파워 쿼리를 사용해야 하는 경우 다음 지침을 따르십시오.

- 프로젝트 및 계약(PSA에서 Fin 및 Ops까지) 템플릿에는 **작업 항목(msdyn\_ordertype = 192350001)** 유형의 판매 주문만 포함하는 기본 필터가 있습니다. 이 필터는 Finance에서 판매 주문에 대해 프로젝트 계약이 생성되지 않도록 보장합니다. 고유한 템플릿을 만드는 경우 이 필터를 추가해야 합니다.
- 통합 연결 집합의 법인에 동기화되어야 하는 계약 조직만 포함하는 파워 쿼리 필터를 만듭니다. 예를 들어 계약 조직 단위가 Contoso US인 프로젝트 계약은 USSI 법인에 동기화되어야 하지만 계약 조직 단위가 Contoso Global인 프로젝트 계약은 USMF 법인과 동기화되어야 합니다. 이 필터를 작업 매핑에 추가하지 않으면 모든 프로젝트 계약이 계약 조직 단위에 관계없이 연결 집합에 대해 정의된 법인에 동기화됩니다.

## <a name="template-mapping-in-data-integration"></a>데이터 통합의 템플릿 매핑

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** 및 **AddressZipCode** 필드는 프로젝트 계약의 기본 매핑에 포함되지 않습니다. 프로젝트 계약에 대해 이 데이터를 동기화해야 하는 경우 매핑을 추가할 수 있습니다.
>
> **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** 및 **ProjectType** 필드는 프로젝트의 기본 매핑에 포함되지 않습니다. 프로젝트에 대해 이 데이터를 동기화해야 하는 경우 매핑을 추가할 수 있습니다.

다음 그림은 데이터 통합에서 템플릿 작업 매핑의 예를 보여줍니다. 매핑은 Project Service Automation에서 Finance로 동기화될 필드 정보를 보여줍니다.

[![프로젝트 계약 템플릿 매핑.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![프로젝트 템플릿 매핑.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![프로젝트 계약 내용 템플릿 매핑.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![프로젝트 계약 내용 중요 시점 템플릿 매핑.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>프로젝트 및 계약(PSA 3.x에서 Dynamics로) - v2 템플릿의 프로젝트 계약 내용 중요 시점 매핑:

[![두 템플릿 버전이 있는 프로젝트 계약 내용 중요 시점 매핑.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]