---
title: 고급 조직 구성 단위
description: 이 항목은 Dynamics 365 Project Service Automation의 조직 구성 단위에 대한 정보를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 80208be7be56d0b09354c45cd2afd96958daf985
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589434"
---
# <a name="about-organizational-units"></a>조직 구성 단위 정보 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, 조직 구성 단위는 비용 요금이 있는 청구 가능한 리소스를 사용하는 전문 서비스 회사의 고유한 그룹 또는 부서입니다.

다양한 실무 영역이나 비즈니스 라인에서 기술 리소스를 사용하는 전문 서비스 회사의 경우 한 실무 영역이나 비즈니스 라인에서 역할을 채우는 비용은 다른 실무 영역이나 비즈니스 라인에서 역할을 채우는 비용과 다를 수 있습니다. 개념 조직 구성 단위는 이러한 역할에 대해 고유한 비용 구조를 가지는 회사의 부서에서 청구 가능한 역할 집합을 그룹화하는 방법을 제공하여 이 시나리오에서 도움이 됩니다.

## <a name="key-attributes-and-associations-of-organizational-units"></a>주요 속성 및 조직 구성 단위의 연결

PSA에서 PSA의 조직 구성 단위에는 특정 통화 및 특정 비용 가격표가 있습니다.

조직 구성 단위의 통화는 비용을 추적하는 데 사용되는 기본 통화입니다.

하나 이상의 비용 가격표는 각 조직 구성 단위에 연결할 수 있습니다. PSA는 조직 구성 단위에 연결할 수 있는 가격표에 다음과 같은 제한을 둡니다.

- 가격표는 조직 구성 단위의 통화여야 합니다.
- 가격표는 비용 가격표여야 합니다.

또한 리소스 엔터티의 조직 구성 단위에 대한 특성이 있습니다. 각 리소스는 한 조직 구성 단위에만 할당될 수 있습니다.

## <a name="roles-of-organizational-units"></a>조직 구성 단위의 역할

조직 구성 단위는 PSA에서 두 가지 역할을 합니다.

- **계약 단위** - 판매에 성공하고 고객에게 작업 및 서비스 제공을 관리하는 책임이 있는 회사 그룹 또는 부서를 대표하는 조직 구성 단위입니다. 계약 단위는 **영업 기회**, **견적**, **프로젝트 계약** 및 **프로젝트** 페이지의 헤더 섹션에 있는 **계약 단위** 필드로 식별됩니다.
- **리소스 단위** - 리소스가 속하거나 할당된 조직 구성 단위입니다. 이 조직 구성 단위는 SOW(작업 명세서) 및 계약 단위가 소유한 프로젝트에 대한 일부 역할에 대한 리소스를 제공할 수 있습니다.

> ![계약 단위 및 리소스 조달 단위.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>조직 구성 단위 FAQ

다음은 조직 구성 단위에 대한 몇 가지 질문입니다.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>PSA의 조직 구성 단위 엔터티는 Dynamics 365에 이미 있는 조직 구성 엔터티와 어떻게 관련이 있습니까?

Microsoft Dynamics 365의 조직 구성 엔터티는 전체 Dynamics 365 인스턴스의 이름을 나타냅니다. 이 이름은 일반적으로 글로벌 기업의 이름입니다.

조직 구성 단위 엔터티는 글로벌 엔터프라이즈의 그룹 또는 부서를 나타냅니다. 이 그룹 또는 부서에는 해당 역할에 대한 역할 집합과 비용 가격표가 있으며 이러한 역할 및 가격표는 엔터프라이즈의 다른 그룹 또는 부서의 역할 및 가격표와 다릅니다.

PSA가 설치되면 조직에 따라 기본 조직 구성 단위가 만들어집니다. 모든 기존 리소스는 기본 조직 구성 단위에 할당됩니다. 새 Active Directory 사용자 또는 리소스를 Dynamics 365로 가져오는 경우, 사용자 가져오기 프로세스는 이를 PSA의 기본 조직 구성 단위에 할당합니다.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>조직 구성 단위 엔터티는 비즈니스 단위 엔터티와 어떻게 다릅니까?

Dynamics 365에서 비즈니스 단위 엔터티는 보안 구성입니다. 비즈니스 단위와 사용자를 연결하면 사용자가 액세스할 수 있는 엔터티 및 엔터티 레코드가 결정됩니다. 또한 사용자가 해당 엔터티 레코드에 대해 가지고 있는 권한(생성, 읽기, 쓰기, 삭제, 추가, 다음에 추가, 할당 또는 공유)을 결정합니다.

조직 구성 단위 엔터티는 할당된 직원에 대해 고유한 비용 비율이 있는 회사 그룹 또는 부서를 나타냅니다. 조직 구성 단위와 리소스의 연결은 프로젝트 참여에 대한 리소스 비용을 결정합니다.

Dynamics 365를 구현할 때 사업부의 계층 구조에 대한 보안 권한 부여와 사업부에 사용자를 할당하는 데 최적화합니다. 일반적으로 동일한 레코드 집합에 액세스해야 하는 모든 사용자를 동일한 사업부에 할당합니다. 조직 구성 단위는 보안 권한 부여 또는 액세스에 영향을 주지 않습니다.

#### <a name="example-of-organizational-units-and-business-units"></a>조직 구성 단위 및 사업부의 예

Contoso, Ltd.는 번창하는 Microsoft 기술 방법을 가지고 있습니다. 인과 해원은 모두 C\# 개발자이지만, 해원은 미국에 있는 반면 인은 인도에 있습니다. 대부분의 프로젝트 계약에는 Contoso India 및 Contoso US의 리소스가 필요하며 인과 해원은 이 방법 영역의 프로젝트에 동일한 수준의 보안 액세스가 필요합니다. 그러나 Contoso India의 개발자 비용은 Contoso US의 개발자 비용과 크게 다릅니다.

다음은 Dynamics 365 및 PSA를 사용하여 이 시나리오를 디자인하는 최적의 방법입니다.

1. Microsoft 기술 방법을 사업부로 만들고 인과 해원을 연결합니다. 이러한 방식으로 두 직원이 해당 방법 영역의 모든 프로젝트에 동일한 수준의 보안 액세스를 갖도록 보장할 수 있습니다. 둘 다 진행 상황을 확인하고 시간, 비용 및 작업 업데이트를 보고할 수 있습니다. 
2. 프로젝트 비용이 올바르게 반영되도록 두 개의 조직 구성 단위를 만듭니다. 
3. 해원을 Contoso US과 연결하고 인을 Contoso India와 연결합니다.
4. 두 조직 구성 단위에 적절한 비용 가격표을 할당합니다. 이러한 방식으로 인과 해원 프로젝트에 기록된 비용이 Contoso US와 Contoso India 간의 비용 차이를 정확하게 반영하도록 보장합니다.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>조직 구성 단위가 Dynamics 365의 판매 영역과 관련이 있습니까?

영업권역과 조직 구성 단위 간에는 연결 또는 관계가 없습니다. 영업권역은 일반적으로 판매가 발생하는 지리적 영역입니다. 영업 가격표는 각 영업권역에 연결할 수 있습니다.

조직 구성 단위는 회사의 내부 그룹 또는 부서로, 다른 부서 또는 외부 고객에게 판매하는 일련의 역할에 대한 비용을 추적합니다.

#### <a name="example-of-organizational-units-and-sales-territories"></a>조직 구성 단위 및 영업권역의 예

Contoso, Ltd.는 Contoso US 및 Contoso India 두 개의 개발 센터를 가지고 있습니다. 자원 비용은 이 두 개발 센터 간에 크게 다릅니다.

Contoso는 라틴 아메리카, 북아메리카, 아시아 태평양, 서유럽 및 중동과 같은 많은 국제 시장에서 IT 서비스를 판매하고 있습니다. 동일한 프로젝트 역할에 대한 청구 요금은 이러한 시장마다 크게 다를 수 있습니다.

Contoso US 및 Contoso India는 조직 구성 단위로 설정해야 하며, 각 조직 구성 단위에는 자체 비용 가격표가 있어야 합니다. 아시아 태평양, 라틴 아메리카, 북아메리카, 서유럽 및 중동은 판매 지역으로 설정되어야 하며, 각 영업권역에는 자체 영업 가격표가 있어야 합니다.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>가격표와 조직 구성 단위의 연관성에 제한이 있는 이유는 무엇입니까? 

영업 가격은 일반적으로 서비스가 판매되는 지리적 영역 또는 시장에 고유합니다. 회사의 내부 부서에는 일반적으로 동일한 유형의 서비스에 대한 자체 가격표가 없습니다. 그러나 내부 부서는 고용하는 사람들의 기술과 그들이 운영하는 지역의 노동 조건에 따라 판매 된 상품 (COGS)의 다른 비용을 가지고 있습니다. 조직 구성 단위는 회사의 내부 부서로 모델링되므로 비용 가격표만 가질 수 있습니다.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>영업 가격표를 조직 구성 단위로 연결할 수 없는 이유는 무엇입니까?

PSA에서 영업 가격표는 고객 및 판매 지역과 연결할 수 있습니다. 영업 기회, 견적, 프로젝트 계약 및 프로젝트와 같은 트랜잭션 엔터티는 고객 계정 또는 영업권역에 연결된 영업 가격표를 사용하여 프로젝트 참여에 대한 청구서 비율 및 잠재적 수익을 결정합니다.

비용 가격표는 조직 구성 단위와 연결됩니다. 영업 기회, 견적, 프로젝트 계약 및 프로젝트와 같은 트랜잭션 엔터티는 계약 단위에 연결된 영업 가격표를 사용하여 프로젝트 계약에 대한 비용을 결정합니다.

### <a name="are-organizational-units-hierarchical-in-psa"></a>조직 구성 단위가 PSA에서 계층적입니까?

번호 PSA의 현재 릴리스에서 조직 구성 단위는 계층적이지 않습니다. 즉, 다음을 수행할 수 없습니다.

- 계층 구조를 통과하는 기본 비용 가격에 대한 패턴을 구성합니다. 
- 조직 구성 단위 계층 구조의 여러 수준에서 롤업된 수익 또는 비용을 보고합니다.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>우리는 비용 센터, 부서 및 청구 사무실의 복잡하고 다단계 계층 구조를 갖춘 대규모 다국적 기업입니다. 이 버전의 Project Service 앱에서 조직 구성 단위 개념을 최대한 활용하려면 어떻게 해야 할까요?

비용 센터, 부서, 청구 사무실 등의 복잡한 계층 구조가 있는 경우 해당 계층의 리프 노드를 고유한 조직 구성 단위로 설정합니다.
다음 예제에서는 일반적인 계층 구조를 보여 줍니다.

**Contoso India**

  - SAP 방법 

    - 기술 컨설턴트 
    - 기능 컨설턴트 
    
  - Microsoft 기술 방법 

    - 기술 컨설턴트
    - 기능 컨설턴트 
    
**Contoso US**

 - SAP 방법 

    - 기술 컨설턴트 
    - 기능 컨설턴트 
    
 - Microsoft 기술 방법 

    - 기술 컨설턴트 
    - 기능 컨설턴트 
 
계층 구조가 비슷하면 다음과 같이 플랫 목록으로 설정해야 합니다.
- Contoso India - SAP 방법 - 기술 컨설턴트 
- Contoso India - SAP 방법 - 기능 컨설턴트       
- Contoso India - Microsoft 기술 방법 기능 컨설턴트 
- Contoso India - Microsoft 기술 방법 기능 컨설턴트 
- Contoso US - SAP 방법 - 기술 컨설턴트  
- Contoso US - SAP 방법 - 기능 컨설턴트  
- Contoso US - Microsoft 기술 방법 - 기술 컨설턴트 
- Contoso US - Microsoft 기술 방법 - 기능 컨설턴트

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>우리는 하나의 부서로 운영되는 작은 전문 서비스 회사입니다. PSA의 현재 버전에서 조직 구성 단위 개념을 가장 잘 사용할 수 있는 방법은 무엇입니까?

회사에서 하나의 비용 가격표가 있는 하나의 단위로 운영되는 경우, 조직 구성 단위를 설정할 필요가 없습니다. PSA 설치 중에, Dynamics 365는 조직과 이름이 같은 하나의 기본 조직 구성 단위를 만듭니다. 기본적으로 모든 사용자는 이 조직 구성 단위에 할당됩니다. 시스템에서 조직 단위를 선택해야 할 때마다, 기본적으로 이 조직 구성 단위가 선택됩니다.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>견적 또는 프로젝트 계약 내용에서 프로젝트를 만들 때 기본 계약 단위는 견적 또는 프로젝트 계약에서 비롯됩니다. 견적 또는 프로젝트 계약과 같은 판매 엔터티 보다 먼저 프로젝트를 만든 경우 기본 계약 단위는 무엇입니까?

프로젝트를 자체적으로 만들 때 프로젝트의 기본 계약 단위는 프로젝트를 만드는 사용자를 기반으로 합니다. 해당 사용자는 기본 프로젝트 관리자이기도 합니다. 프로젝트가 견적 또는 프로젝트 계약과 같은 판매 엔터티에 매핑되는 경우 프로젝트의 계약 단위는 대신 영업 엔터티를 기반으로 합니다. 이 경우 계약 단위가 변경된 경우 비용 견적 변경을 계산하는 데 비용 가격표가 사용되므로 프로젝트 예상 값이 다시 계산될 수 있습니다. 영업 가격표는 견적의 프로젝트 가격표와 동기화되도록 변경될 판매 예상 값을 계산하는 데 사용됩니다.

프로젝트의 **계약 단위** 및 **통화** 필드는 프로젝트가 매핑되는 판매 엔터티(견적 또는 프로젝트 계약)의 값과 동기화되어야 하기 때문에 편집을 위해 잠깁니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
