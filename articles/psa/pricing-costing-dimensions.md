---
title: 가격 및 원가 차원 홈 페이지
description: 이 항목은 가격 차원에 대한 개요를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d17939777a6670bafc41b372adc922f8bdcc0411f3fdb399e7c9ab01eca87dd0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998469"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>가격 및 원가 차원 홈 페이지

[!include [banner](../includes/psa-now-project-operations.md)]

프로젝트 기반 조직에서 인건비 가격 및 비용을 설정하는 데 사용되는 차원은 다음 속성의 영향을 받습니다.

- 자신의 경험, 역할 또는 지리와 유사한 일을 하는 사람들
- 복잡성 또는 시간과 유사하게 수행할 작업

작업의 이러한 속성과 작업을 수행하는 데 필요한 사람의 일반적인 특성을 고려할 때 Project Service Automation에서 사용할 수 있는 두 가지 유형의 가격 책정 차원 값이 있습니다. 

- **옵션 집합** - 값 집합에 대해 고정된 열거형인 특성입니다.
- **엔터티 기반 값** - 유한하지만 시간이 지남에 따라 변경될 수 있는 다양한 값 집합을 가질 수 있는 특성입니다.

## <a name="pricing-dimensions"></a>가격 책정 차원

PSA는 기본 가격 차원 집합으로 배송됩니다. 이러한 것을 **Project Service** > **파라미터** 로 이동하여 볼 수 있습니다. 파라미터 레코드에서 **금액 기반 가격 책정 차원** 탭에서 역할, **msdyn_resourcecategory** 및 리소싱 조직 단위, **msdyn_organizationalunit** 의 필드 **매출액에 해당** 및 **원가에 해당** 이 **예** 로 설정되어 있는지 확인하십시오. 이렇게 하면 각 역할 및 조직 단위 조합에 대한 가격과 원가를 설정할 수 있습니다.

!["매출액에 해당"이 강조 표시된 Project Service 파라미터의 스크린샷.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> PSA 버전 3 이전에 역할 및 조직 단위의 즉시 사용 필드가 가격 차원으로 사용된 경우 관찰 가능한 변경 사항이 없습니다. 평소와 같이 Project Service를 계속 사용할 수 있습니다. 

추가 속성을 사용하는 리소스에 대한 가격 또는 원가가 필요한 경우 맞춤화된 필드, 엔터티 및 차원을 만들 수 있습니다. 자세한 내용은 다음 항목을 참조하지만 아래 나열된 순서대로 절차를 완료해야 합니다:

- [맞춤 필드 및 엔터티 만들기](create-custom-fields-entities.md)
- [가격 설정 및 처리 엔터티에 맞춤 필드 추가](field-references.md)
- [가격 책정 차원의 사용자 지정 필드 설정](set-up-pricing-dimensions.md)
- [새 가격 책정 차원을 포함하도록 플러그인 속성 업데이트](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>인적 자원 시간 가격 책정
조직이 인적 자원 시간을 어떻게 책정하는지는 종종 조직의 수익성에 직접적인 영향을 미치는 중요한 전략적 고려 사항입니다. 귀하의 조직이 인적 자원 시간을 위한 청구서 및 원가 요율을 설정하는 방법을 파악할 준비가 되면 재무팀 및 실무 책임자들과 협력하십시오.

가격 책정에 대한 다른 고려 사항으로는 현재 가격 책정 차원이 아니지만 조직의 가격 책정 차원으로 적용되는 필드 또는 엔터티를 다시 사용할지 여부가 있습니다. **처리 카테고리**(**msdyn_transactioncategory**) 및 **예약 가능한 리소스**(**bookableresource**) 같은 필드는 후보 차원의 예입니다. 

가격 책정 차원이 표여야 하는지 옵션 집합이어야 하는지도 고려합니다. 10 또는 12를 초과하는 차원값의 변경을 예측하고 이러한 값에 추가 속성이 필요한 경우 옵션 집합보다는 엔터티를 만듭니다. 값 추가 또는 제거와 같은 옵션 집합을 유지하려면 관리자 또는 개발자가 요구되지만 표에 새 행을 추가하는 것은 대부분의 비즈니스 사용자가 할 수 있습니다.

다음 예는 리소스가 속한 역할 및 리소스 조직 단위를 기반으로 설정된 청구 요율을 보여줍니다. 원가 요율은 일반적으로 직원의 급여대와 그들이 속한 조직 단위에 근거합니다. 이 예에서는 청구서 요율 및 원가 요율 표가 다음과 같습니다.

**샘플 청구서 요율**

| 역할        | 조직 단위    |단위      |가격      |통화  |
| ------------|-------------|----------|----------:|----------|
| 개발자   | Contoso US  |시간 | 200|USD     |
| 개발자   | Contoso India |시간|   112|USD     |


**샘플 원가 요율**

| 급여대     | 조직 단위    |단위      |가격      |통화  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |시간 | 145|USD     |
| My company_Band2 | Contoso India |시간|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]