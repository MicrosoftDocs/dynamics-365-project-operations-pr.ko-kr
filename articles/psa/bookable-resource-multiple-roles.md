---
title: 예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다.
description: 이 항목에서는 프로젝트에서 여러 역할을 수행하는 리소스의 가격 책정 및 비용을 지원하기 위해 가격 책정 차원을 사용하는 방법에 대한 정보를 제공합니다.
author: rumant
ms.custom:
- dyn365-projectservice
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f8b84de740a3d610e49acea8fa13885b977b440c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590722"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>예약 가능한 리소스가 프로젝트에서 여러 역할을 수행할 때 프로젝트 판매 및 비용을 추정합니다. 

[!include [banner](../includes/psa-now-project-operations.md)]

프로젝트 기반 회사는 종종 프로젝트에서 여러 역할을 수행하기 위해 하나의 리소스가 필요합니다. 이러한 각 역할은 가격이 책정되고 비용이 다르게 책정될 수 있습니다. 즉, 프로젝트에서 동일한 리소스의 시간이 각 역할의 청구서 및 비용 요율에 따라 다른 재무 추정치를 얻을 수 있음을 의미합니다. Project Service Automation을 사용하면 명명된 리소스에 대한 팀 구성원 레코드의 값을 설정할 수 있으며 팀 구성원이 할당된 각 작업에 대해 다른 재정의가 허용됩니다.

다음 예에서는 이 값의 단순 재정의를 통해 리소스가 비용 및 청구 요율이 다른 프로젝트에서 여러 역할을 가질 수 있는 방법을 설명합니다.

## <a name="create-tasks"></a>작업 만들기
각각 40시간 동안 두 개의 프로젝트 작업(작업 A 및 작업 B)을 만듭니다. 작업 B의 선행 작업으로 작업 A를 선택합니다.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>일반 프로젝트 팀 구성원에 대한 역할 및 조직 단위 설정

1. **일정** 페이지에서 작업 A의 **작업** 행을 선택합니다. 
2. **리소스** 필드의 드롭다운 목록에서 **만들기** 를 선택합니다.
3. **팀 구성원 빨리 만들기** 페이지에서 이 작업을 수행할 수 있는 일반 팀 구성원의 속성을 지정합니다.
4. 적절한 역할 및 조직 구성 단위를 선택한 다음 **저장 후 닫기** 를 선택합니다. 일반 팀 구성원이 생성되고 이 작업에 할당됩니다. 

작업 B에 대해 이러한 단계를 반복하고 작업 B에 대해 생성된 일반 팀 구성원의 역할 및 조직 단위가 작업 A와 다른지 확인합니다. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>프로젝트 작업에 대한 역할 및 조직 구성 단위 설정

1. 작업 A를 생성한 후 작업을 선택한 다음 **작업 편집** 을 선택합니다.
2. **작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 필드에 이 작업을 수행할 리소스에 필요한 값을 추가합니다. 

  > [!NOTE]
  > Project Service Automation 데모 데이터를 사용하여 이 시나리오를 완료하는 경우 **컨설팅 리드** 역할 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.

3. 작업 B를 선택한 다음, **작업 편집** 을 선택합니다.
4. **작업 세부 정보** 페이지에서 **역할** 및 **조직 구성 단위** 필드에 이 작업을 수행할 리소스에 필요한 값을 추가합니다. **역할** 과 **조직 구성 단위** 필드의 값이 작업 A의 값과 작업 B의 값이 다른지 확인합니다. 

  > [!NOTE]
  > Project Service Automation 데모 데이터를 사용하여 이 시나리오를 완료하는 경우 **네트워크 기술자** 역할 및 **Fabrikam US** 를 조직 구성 단위로 선택합니다.

5. 저장 후 **작업 세부 정보** 페이지를 닫습니다. 

## <a name="team-member-and-estimates-behavior"></a>팀 구성원 및 추정 행동 

1. **작업 세부 정보** 페이지의 **팀 구성원** 에서 두 개의 일반 팀 구성원을 선택한 다음 **요구 사항 생성** 을 선택합니다. 
2. **컨설팅 리드** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다. 일정 게시판이 열리고 해당 요구 사항에 대한 리소스가 예약됩니다.
3. **네트워크 기술자** 에 대한 팀 구성원 행을 선택한 다음 **예약** 을 선택합니다. 일정 게시판이 열리고 해당 요구 사항에 대한 동일한 리소스가 예약됩니다.

### <a name="team-member-grid"></a>팀 구성원 그리드 
**팀 구성원** 그리드에서 두 개의 일반 팀 구성원 레코드가 삭제되고 하나의 리소스로 대체되었음을 확인합니다. **역할** 및 **조직 구성 단위** 에 대한 기본 값 집합을 보여주는 해당 리소스에 대한 값 집합이 하나 있습니다.
해당 팀 구성원 레코드의 행을 확장하면 두 작업 모두에 대해 팀 구성원 레코드에서 고유한 할당을 볼 수 있습니다. 각 할당 행에는 **역할** 및 **조직 구성 단위** 에 대한 작업별 값이 있습니다. 

### <a name="estimates-grid"></a>추정 그리드 
**추정** 그리드로 이동할 때 동일한 리소스에 대한 두 할당의 가격이 다르게 책정됨을 알 수 있습니다.
작업 A의 리소스 할당은 **컨설팅 리드** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다. 작업 B의 동일한 리소스 할당은 **네트워크 기술자** 의 **역할** 속성 값을 사용하여 가격이 책정됩니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
