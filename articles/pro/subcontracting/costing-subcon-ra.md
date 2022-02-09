---
title: 하도급 계약 리소스 할당 비용 추정
description: 이 토픽에서는 Microsoft Dynamics 365 Project Operations가 하도급 계약 리소스 할당의 비용 추정치를 계산하는 방법에 대해 설명합니다.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903471"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>하도급 계약 리소스 할당 비용 추정

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

하도급 계약 프로젝트 팀 구성원의 작업 할당은 관련 팀 구성원 레코드의 하도급 계약에 첨부된 **구매** 가격표를 사용하여 비용이 계산됩니다. 이는 프로젝트의 계약 단위에 첨부된 **비용** 가격표를 사용하여 직원 리소스의 작업 배정 비용을 계산하는 직원 리소스 배정 비용을 계산하는 방법과 다릅니다. 

하도급 계약된 일반 프로젝트 팀 구성원의 경우 하도급 계약에 첨부된 구매 가격표의 역할 기반 가격 설정을 사용하여 할당 비용이 계산됩니다. 구매 가격은 각 리소스에 대해 구체적으로 설정할 수도 있습니다. 이러한 리소스별 가격은 명명된 프로젝트 팀 구성원의 원가 계산 작업 할당이 계약 근로자인 경우 우선 순위가 부여됩니다. 

역할별 구매 가격 대 리소스별 사용 우선 순위는 **매개변수 > 금액 기반 가격 책정 차원** 의 가격 책정 차원 우선 순위 설정에 따라 결정됩니다.

하청업체의 구매 가격에 대한 차원 설정을 기반으로 가격을 동적으로 도출하는 이 기능은 정규직 직원에 대한 비용 및 청구 요금이 도출되는 방식과 유사합니다. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>하청업체 리소스의 비용 추정치를 얻기 위한 작업 할당 생성

하청업체에 대한 작업 할당은 두 가지 방법으로 생성할 수 있습니다. 
- **작업** 탭 사용.
- **팀** 탭 사용.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>작업 탭을 사용하여 리소스 할당 생성
특정 작업에 대한 **작업** 탭에서 **리소스** 목록을 사용하여 명명된 리소스 또는 일반 리소스에 대한 작업 할당을 만들 수 있습니다. 작업의 **할당된 리소스** 드롭다운에서 명명된 리소스를 선택하고 이 리소스가 계약직 근로자인 경우 명명된 리소스가 작업에 지정되고 작업자 유형이 **계약 작업자** 로 설정되고 **유효성** 이 **잘못됨** 으로 설정된 상태에서 해당 프로젝트 팀 구성원 레코드가 생성됩니다. 다음 단계로 프로젝트 팀 구성원 레코드를 열고 하도급 계약 및 하도급 계약 내용을 선택해야 합니다. 이렇게 하면 하도급 계약 및 하도급 계약 내용에 대한 참조를 갖도록 작업 할당이 업데이트되고 팀 구성원 상태도 **유효** 로 업데이트됩니다.

작업의 **할당된 리소스** 드롭다운에서 일반 팀 구성원을 생성하도록 선택하면 **일반 팀 구성원 생성** 대화 상자에서 하도급 계약 및 하도급 계약 내용을 선택할 수 있습니다. 일반 리소스가 작업에 할당되고 해당 프로젝트 팀 구성원 레코드가 생성되면 작업자 유형이 **계약 작업자** 로 설정되고 **유효성** 이 **유효** 로 설정되어 프로젝트 팀 구성원 레코드가 생성되는 것을 알 수 있습니다.

### <a name="creating-project-team-members-using-the-team-tab"></a>팀 탭을 사용하여 프로젝트 팀 구성원 만들기
프로젝트의 팀 탭을 사용하여 일반 또는 명명된 팀 구성원을 생성할 수 있습니다. 팀 구성원을 생성할 때 하도급 계약 및 하도급 계약 내용을 선택할 수 있습니다. 팀 구성원이 생성된 후 작업에 **할당된 리소스** 드롭다운을 사용하여 작업에 팀 구성원을 할당해야 합니다. 

## <a name="updating-estimates"></a>견적 업데이트
프로젝트 팀 구성원을 작업에 할당한 후에는 프로젝트의 **추정** 탭으로 이동하고 **가격 업데이트** 를 선택하여 하청업체 리소스 할당의 비용율이 하청업체에 첨부된 구매 가격표를 기반으로 업데이트되도록 해야 합니다. Microsoft Dynamics 365 Project Operations에서 할당되지 않은 작업에 대해서는 추정이 생성되지 않습니다. 결과적으로 프로젝트에 대한 다양한 작업의 가격을 책정하고 비용을 책정하기 위해 작업 할당을 생성해야 합니다. 

> [참고!] **작업자 유형** 이 **계약 작업자** 이지만 하도급 계약 참조가 없는 **프로젝트 팀 구성원** 은 프로젝트 팀 구성원 표에서 **유효하지 않음** 으로 플래그가 지정됩니다. 이 상태의 프로젝트 팀 구성원이 있는 경우 프로젝트 팀 구성원 레코드를 열고 재무 비용 추정이 **추정** 탭의 하청업체 비용을 정확하게 반영하도록 하도급 계약 및 하도급 계약 내용 필드를 수동으로 업데이트합니다. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]