---
title: 가격 책정 차원 개요
description: 이 항목은 Dynamics 365 Project Operations에서 가격 책정 차원에 대한 정보를 제공합니다.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898224"
---
# <a name="pricing-dimensions-overview"></a>가격 책정 차원 개요

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

인적 자원에서 가격 및 원가를 설정하는 데 사용되는 차원은 두 가지 카테고리로 나뉩니다:

- 사람
- 계획된 작업

따라서 사용할 수 있는 가격 차원 값에는 두 가지 타입이 있습니다:

- **옵션 집합**: 값 집합에 대해 고정된 열거형인 차원입니다.
- **엔터티 기반 값**: 다양한 값 집합일 수 있는 차원입니다.

## <a name="pricing-dimensions"></a>가격 책정 차원

Dynamics 365 Project Operations는 기본 가격 책정 차원 집합과 함께 제공됩니다. **프로젝트 작업** > **매개 변수**로 이동하여 이러한 가격 책정 차원을 볼 수 있습니다. 파라미터 레코드에서 **금액 기반 가격 책정 차원** 탭에서 역할, **msdyn_resourcecategory** 및 리소싱 조직 단위, **msdyn_organizationalunit**의 필드 **매출액에 해당** 및 **원가에 해당**이 **예**로 설정되어 있는지 확인하십시오. 이러한 필드를 활성화하면 각 역할 및 조직 단위 조합에 대한 가격과 원가를 설정할 수 있습니다.

추가 속성을 사용하는 리소스에 대한 가격 또는 원가가 필요한 경우 맞춤화된 필드, 엔터티 및 차원을 만들 수 있습니다.

## <a name="pricing-human-resource-time"></a>인적 자원 시간 가격 책정
조직이 인적 자원 시간을 어떻게 책정하는지는 종종 조직의 수익성에 직접적인 영향을 미치는 중요한 전략적 고려 사항입니다. 귀하의 조직이 인적 자원 시간을 위한 청구서 및 원가 요율을 설정하는 방법을 파악할 준비가 되면 재무팀 및 실무 책임자들과 협력하십시오.

가격 책정에 대한 다른 고려 사항으로는 현재 가격 책정 차원이 아니지만 조직의 가격 책정 차원으로 적용되는 필드 또는 엔터티를 다시 사용할지 여부가 있습니다. **처리 카테고리**(**msdyn_transactioncategory**) 및 **예약 가능한 리소스**(**bookableresource**) 같은 필드는 후보 차원의 예입니다. 

가격 책정 차원이 표여야 하는지 옵션 집합이어야 하는지도 고려합니다. 10 또는 12를 초과하는 차원값의 변경을 예측하고 이러한 값에 추가 속성이 필요한 경우 옵션 집합보다는 엔터티를 만들 수 있습니다. 값 추가 또는 제거와 같은 옵션 집합을 유지하려면 관리자 또는 개발자가 요구되지만 표에 새 행을 추가하는 것은 대부분의 사용자가 할 수 있습니다.

다음 예는 리소스가 속한 역할 및 리소스 조직 단위를 기반으로 설정된 청구 요율을 보여줍니다. 원가 요율은 일반적으로 직원의 급여대와 그들이 속한 조직 단위에 근거합니다. 이 예에서는 청구서 요율 및 원가 요율 표가 다음과 같습니다.

**샘플 청구서 요율**

| 역할        | 조직 단위    |단위      |가격      |통화  |
| ------------|-------------|----------|----------:|----------|
| 개발자   | Contoso US  |Hour | 200|USD     |
| 개발자   | Contoso India |Hour|   112|USD     |


**샘플 원가 요율**

| 급여대     | 조직 단위    |단위      |가격      |통화  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hour | 145|USD     |
| My company_Band2 | Contoso India |Hour|   67|USD     |
