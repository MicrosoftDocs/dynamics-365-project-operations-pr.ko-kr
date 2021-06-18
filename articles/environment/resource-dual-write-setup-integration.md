---
title: Project Operations 설정 및 구성 데이터 통합
description: 이 항목은 Project Operations 이중 쓰기 맵 설정 및 구성에 대한 정보를 제공합니다.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001074"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations 설정 및 구성 데이터 통합

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 설정 및 구성 엔터티를 위한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.

## <a name="project-contracts-contract-lines-and-projects"></a>프로젝트 계약, 계약 내용 및 프로젝트

프로젝트 계약, 계약 내용 및 프로젝트는 Dataverse에서 생성되고 추가 회계를 위해 Finance and Operations 앱에 동기화됩니다. 이러한 엔터티의 레코드는 Dataverse에서만 만들고 삭제할 수 있습니다. 그러나 판매세 그룹 기본값 및 재무 차원과 같은 회계 속성은 Finance and Operations 앱에서 이러한 레코드에 추가할 수 있습니다.

  ![프로젝트 계약 통합 개념](./media/1ProjectContract.jpg)

판매 활동 잠재 고객, 영업 기회 및 견적은 Dataverse에서 추적되며 이 활동과 관련된 다운스트림 계정이 없기 때문에 Finance and Operations 앱과 동기화하지 않습니다.

Dataverse의 프로젝트 계약 기능은 **프로젝트 계약 헤더 (salesorders)** 테이블 맵을 사용하여 Finance and Operations 앱에 프로젝트 계약 레코드를 생성합니다. Dataverse에 프로젝트 계약을 저장하면 프로젝트 계약 고객 엔터티 레코드도 생성됩니다. 이 레코드는 **프로젝트 자금 출처(msdyn\_projectcontractssplitbillingrules)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다. 이 맵은 또한 프로젝트 계약 고객 추가, 업데이트 및 삭제를 동기화합니다. 프로젝트 계약 고객 간의 분할 청구 비율은 Dataverse에서만 마스터되며 Finance and Operations 앱과 동기화되지 않습니다.

Dataverse에서 프로젝트 계약이 생성되면 프로젝트 회계사는 **프로젝트 관리 및 회계** > **프로젝트 계약** > **설정** > **기본 계정 표시** 로 이동하여 Finance and Operations 앱에서 이 프로젝트 계약의 회계 속성을 업데이트할 수 있습니다. 회계사는 Dataverse에서 관련 프로젝트 계약 기록을 여는 Finance and Operations 앱에서 프로젝트 계약 ID를 선택하여 요청된 납품 날짜 및 계약 금액과 같은 운영 프로젝트 계약 속성을 검토할 수 있습니다.

프로젝트 엔터티는 **프로젝트 V2(msdyn\_projects)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다. 프로젝트 회계사는 다음을 수행할 수 있습니다.

  - **프로젝트 관리 및 회계** > **모든 프로젝트** 로 이동하여 Finance and Operations앱에서 프로젝트를 검토합니다. 
  - **프로젝트 관리 및 회계** > **모든 프로젝트** > **설정** > **기본 계정 표시** 로 이동하여 Finance and Operations 앱에서 프로젝트의 회계 속성을 업데이트합니다.  
  - Dataverse에서 관련 프로젝트 레코드를 여는 Finance and Operations앱에서 프로젝트 ID를 선택하여 예상 시작 및 종료 날짜와 같은 운영 프로젝트 속성을 검토합니다.

프로젝트는 **프로젝트 계약 내용** 엔터티를 통해 프로젝트 계약과 연결됩니다.

Dataverse의 프로젝트 계약 내용은 **프로젝트 계약 내용(salesorderdetails)** 테이블 맵을 사용하여 Finance and Operations 앱에서 프로젝트 계약 청구 규칙을 생성합니다. 청구 방법은 Finance and Operations 앱에서 프로젝트 계약 청구 규칙 유형을 정의합니다.

  - 시간 및 재료 청구 방법이 있는 프로젝트 계약 내용은 시간 및 재료 유형의 청구 규칙을 생성합니다.
  - 고정 가격 청구 방법 계약 내용은 중요 시점 청구 규칙을 생성합니다.

프로젝트 계약 내용은 **프로젝트 관리 및 회계** > **프로젝트 계약** > **설정** > **기본 회계 표시** 로 이동하고 **계약 내용** 탭에서 세부 사항을 검토하여 Finance and Operations 앱에서 프로젝트 회계사가 검토할 수 있습니다. 회계사는 이 탭에서 고정 가격 청구 방법 계약 내용에 대한 기본 재무 차원을 설정할 수도 있습니다.

## <a name="billing-milestones"></a>청구 이정표

고정 가격 청구 방법을 사용하는 프로젝트 계약 라인은 청구 이정표를 통해 청구됩니다. 청구 이정표는 **Project Operations 통합 계약 내용 이정표(msdyn\_contractlinescheduleofvalues)** 테이블 맵을 사용하여 Finance and Operations 앱의 프로젝트 계정 트랜잭션에 동기화됩니다.

  ![청구 이정표 통합](./media/2Milestones.jpg)

회계사는 계정 내 거래를 검토하고 **프로젝트 관리 및 회계** > **프로젝트 계약** > **유지** > **계정 트랜잭션** 또는 **프로젝트 관리 및 회계** > **모든 프로젝트** > **유지** > **계정 트랜잭션** 으로 이동하여 해당 트랜잭션에 대한 회계 속성을 조정할 수 있습니다.

주어진 프로젝트 계약 내용에 대한 청구 이정표를 처음 생성하면 시스템은 이 계약 내용과 연관된 프로젝트에 대한 고정 가격 수익 추정 프로젝트를 자동으로 생성합니다. 고정 가격 수익 추정 프로젝트는 **프로젝트 관리 및 회계** > **고정 가격 수익 추정 프로젝트** 로 이동하여 검토할 수 있습니다.

### <a name="project-tasks"></a>프로젝트 작업

프로젝트 작업은 참조 목적으로만 **프로젝트 작업(msdyn\_projecttasks)** 테이블 맵을 통해 Finance and Operations 앱에 동기화됩니다. Finance and Operations 앱에서는 작업 생성, 업데이트 및 삭제가 지원되지 않습니다.

  ![프로젝트 작업 통합](./media/3Tasks.jpg)

## <a name="project-resources"></a>프로젝트 리소스

**프로젝트 리소스 역할** 엔터티는 참조 목적으로만 **모든 회사에 대한 프로젝트 리소스 역할(bookableresourcecategories)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다. Dataverse의 리소스 역할은 회사별로 다르기 때문에 시스템은 이중 쓰기 통합 범위에 포함된 모든 법인에 대해 자동으로 Finance and Operations 앱에 각 회사별 리소스 역할 레코드를 생성합니다.

![리소스 역할 통합](./media/5Resources.jpg)

Project Operations의 프로젝트 리소스는 Dataverse에서 유지되며 Finance and Operations 앱과 동기화되지 않습니다.

### <a name="transaction-categories"></a>트랜잭션 범주

트랜잭션 범주는 Dataverse에서 유지되며 **프로젝트 트랜잭션 범주(msdyn\_transactioncategories)** 테이블 맵을 사용하여 Finance and Operations 앱에 동기화됩니다. 트랜잭션 범주 레코드가 동기화된 후 시스템은 4개의 공유 범주 레코드를 자동으로 생성합니다. 각 레코드는 Finance and Operations 앱의 트랜잭션 유형에 해당하며 이를 트랜잭션 범주 레코드에 연결합니다.

![트랜잭션 범주 통합](./media/4TransactionCategories.jpg)

견적 및 실제에 대해 트랜잭션 범주를 사용하려면 프로젝트 회계사 또는 시스템 관리자가 모든 법인에서 해당 프로젝트 범주를 만들어야합니다. 자세한 내용은 [프로젝트 범주 구성](../project-accounting/configure-project-categories.md)을 참조하십시오.
