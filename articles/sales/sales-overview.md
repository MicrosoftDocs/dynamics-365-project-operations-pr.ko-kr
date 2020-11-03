---
title: 영업 프로세스 개요
description: 이 주제는 기본 영업 프로세스에 대한 정보를 제공합니다.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: c70760748c5faa87f6738ab7e2ab593e2df49e41
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080251"
---
# <a name="sales-processes-overview"></a>영업 프로세스 개요

프로젝트 기반 조직에서 사용되는 영업 프로세스는 제품 기반 조직에서 사용되는 영업 프로세스와 다릅니다. 이러한 차이는 프로젝트 기반 조직의 영업 주기가 더 길고 각 거래에 대한 견적을 분석하고 만드는 사용자 지정된 추정 기술이 필요하기 때문에 발생합니다. Dynamics 365 Project Operations는 영업 프로세스에 사용되는 다음과 같은 몇 가지 기능을 사용합니다.

- 잠재 고객 레코드는 영업 프로세스를 추적하는 데 사용됩니다.
- 적격 잠재 고객은 기회로 추적됩니다.
- 영업 기회에 대한 모든 관련 아티팩트에 액세스할 수 있습니다. 이러한 아티팩트에는 영업 팀, 이해 관계자, 가능성, 등급, 영업 스테이지 및 비즈니스 프로세스가 포함됩니다.
- 영업 기회에 대해 여러 견적이 만들어집니다.
- 견적은 영업 주문을 만들기 위해 **성공으로 종료** 상태로 제공됩니다. Project Operations에서 영업 주문은 사용자 지정되며 프로젝트 계약이라고 합니다.

## <a name="estimate-a-sale"></a>영업 예상
판매 가치는 이전에 전달된 프로젝트와 프로젝트의 복잡성을 기반으로 추정할 수 있습니다. 이전 프로젝트에 대한 확장이 포함된 프로젝트 또는 공급업체의 전문 지식이 높고 잘 알려진 작업 템플릿이 사용되는 프로젝트의 경우 더 간단한 예상 프로세스를 사용할 수 있습니다. 더 복잡한 프로젝트는 일반적으로 구매 프로세스가 더 깁니다. 따라서 영업 예상 프로세스에는 더 많은 단계가 있습니다. 프로세스 초기에 영업 팀은 거래처 관리자와 주제별 전문가(SME)의 입력을 사용하여 견적되는 각 개별 작업 구성 요소에 대한 높은 수준의 견적을 작성합니다. 이러한 작업 구성 요소는 견적 라인으로 표시됩니다. 

견적의 높은 수준의 예상을 작성할 수 있습니다. 결국 이 높은 수준의 예상은 표준화된 프로젝트 템플릿을 사용하여 만든 프로젝트 계획을 기반으로 하는 보다 자세한 예상으로 대체됩니다. 이러한 템플릿을 사용하면 견적 및 해당 구성 요소(견적 라인)에서 일정을 작성하고 금액 값을 결정하는 데 도움이 됩니다. 

프로젝트에 대해 여러 견적을 만들고 단일 영업 기회 레코드로 그룹화할 수 있습니다. 결국 이러한 견적 중 하나가 **성공으로 종료** 로 표시되고, 프로젝트 계약 또는 SOW(작업 명세서)가 만들어집니다. 프로젝트 계약은 배달을 위해 고객이 수락한 각 구성 요소(계약 내용)에 대한 계약 값을 보유합니다. SOW는 일반적으로 Microsoft Word 문서로 만들어집니다. 프로젝트 납품 과정에서 고객에게 전송되는 모든 송장은 프로젝트 계약 또는 SOW를 참조합니다.

하나의 영업 기회 레코드에서 대체 견적을 만들거나 견적이 성공할 때 프로젝트 계약이 생성되도록 시스템을 설정할 수도 있습니다. 이 경우 SOW를 나타내는 Word 문서를 프로젝트 계약 레코드에 첨부할 수 있습니다.

## <a name="configure-the-sales-process"></a>영업 프로세스 구성
비즈니스 프로세스 흐름을 사용하여 영업 프로세스를 구성할 수 있습니다. 이러한 흐름은 영업 프로세스 단계를 통해 거래를 진행할 수 있도록 안내된 시각적 인터페이스를 제공합니다.

예를 들어 회사의 영업 프로세스에 다음 6단계의 단계가 있을 수 있습니다.

1. 우량으로 선별
2. 추정
3. 내부 검토
4. 계약
5. 배송
6. 종료
 
조직에서는 서로 다른 엔터티를 사용하여 발전하는 것과 동일한 거래를 나타낼 수 있습니다. 영업 프로세스 초기에 거래는 영업 기회 엔터티로 표시됩니다. 시간이 지남에 따라 자세한 내용이 나오면 상위 수준 견적을 사용하여 하나 이상의 견적을 만들 수 있습니다. 이러한 견적 중 하나가 내부 및 고객 이해 관계자에 의해 검토되는 경우 견적 엔터티는 거래를 나타냅니다. 고객이 견적을 수락하면 프로젝트 계약 또는 SOW가 거래를 나타냅니다. 이 동작을 지원하기 위해 BPF는 프로세스의 각 단계가 다른 데이터베이스 테이블에 연결되도록 구조화됩니다.

영업 프로세스의 **우량으로 선별 스테이지** 는 영업 기회 엔터티에 의해 뒷받침될 수 있습니다. **예상** 및 **내부 검토** 스테이지는 견적 엔터티에 의해 뒷받침될 수 있습니다. **계약** , **배달** 및 **닫기** 스테이지는 프로젝트 계약 엔터티에 의해 뒷받침될 수 있습니다.

스테이지를 통해 거래를 이동하면 프로세스를 안내하고 안내하는 적절한 엔터티 레코드를 만들라는 메시지가 표시됩니다. 스테이지는 조건부일 수 있습니다. 예를 들어 견적에서 사용자 지정 가격표를 사용하는 경우에만 견적에 대한 내부 검토가 필요한 경우 비즈니스 프로세스의 적절한 스테이지에서 해당 조건을 구성할 수 있습니다. 그러면 **내부 검토** 스테이지는 사용자 지정 가격표를 사용하는 견적에 대해서만 표시됩니다. 다른 모든 거래 및 견적의 경우, **예상** 스테이지가 **계약** 스테이지 다음에 옵니다.

> [!NOTE]
> Project Operations에는 영업 기회, 견적, 주문 및 송장 엔터티 레코드에 대한 특정 페이지가 있습니다. 이러한 엔터티에 대한 프로젝트 정보 페이지를 사용하여 이러한 레코드를 만들어야 합니다. 그렇지 않으면 **프로젝트 정보** 페이지에서 레코드를 열 수 없습니다. **프로젝트 정보** 페이지에서 에서 레코드를 열려면 레코드를 삭제하고 **프로젝트 정보** 페이지를 사용하여 다시 만들어야 합니다. 이러한 각 엔터티 유형에 대한 비즈니스 논리가 레코드의 **유형** 필드가 올바르게 설정되고 모든 필수 개념이 올바르게 초기화되었는지 확인합니다.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>영업 주기에서 견적 및 프로젝트 계획에 대한 수정 정보 추적
Project Operations에서는 견적에 대한 수정을 추적할 수 없습니다. 대신 기존 견적을 **실패로 종료** 로 표시한 다음 새 견적을 만들어야 합니다. 견적을 복사하거나 프로젝트 기반 견적을 복제할 수 있습니다.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>견적 및 프로젝트 계약의 주석 및 승인 추적
레코드 담벼락과 게시물을 사용하여 견적 및 프로젝트 계약의 검토 및 승인을 관리할 수 있습니다. 조직에서 사용자 지정 워크플로 및 플러그인을 만들어 검토 및 승인 작업 항목의 알림을 할당, 리디렉션, 에스컬레이션 및 관리할 수 있습니다.