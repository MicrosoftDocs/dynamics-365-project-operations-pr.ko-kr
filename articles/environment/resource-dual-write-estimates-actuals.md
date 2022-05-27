---
title: 프로젝트 추정 및 실제 통합
description: 이 항목은 프로젝트 추정 및 실제를 위한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577198"
---
# <a name="project-estimates-and-actuals-integration"></a>프로젝트 추정 및 실제 통합

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목은 프로젝트 추정 및 실제를 위한 Project Operations 이중 쓰기 통합에 대한 정보를 제공합니다.

## <a name="project-estimates"></a>프로젝트 추정

프로젝트 노동, 비용 및 자재 견적은 Microsoft Dataverse에서 생성 및 유지 관리되며 회계 목적으로 금융 및 운영 앱과 동기화됩니다. 금융 및 운영 앱에서는 생성, 업데이트 및 삭제 작업이 지원되지 않습니다.

추정을 작성하려면 프로젝트에 대한 유효한 회계 구성이 필요합니다. 계약 내용과 연관된 프로젝트에는 프로젝트 원가 및 수익 프로필 규칙에 정의된 유효한 프로젝트 원가 및 수익 프로필이 있어야 합니다. 자세한 내용은 [청구 가능 프로젝트에 대한 회계 구성](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules)을 참조하십시오.

## <a name="labor-estimates"></a>인건비 추정

인건비 추정은 프로젝트 작업에 일반 또는 명명된 리소스를 할당하는 프로젝트 관리자 또는 자원 관리자가 만듭니다. 리소스 할당 기록은 Dataverse의 **프로젝트 세부 정보** 페이지에 있는 **리소스 할당** 탭에서 검토할 수 있습니다. Dataverse의 리소스 할당 레코드는 **시간 추정을 위한 Project Operations 통합 엔터티(msdyn\_resourceassignments)** 를 사용하여 금융 및 운영 앱에서 시간 예측 레코드를 생성합니다.

   ![인건비 추정 통합.](./Media/DW4LaborEstimates.png)

이중 쓰기는 리소스 할당 레코드를 준비 테이블(**ProjCDSEstimateHoursImport**)과 동기화한 다음 비즈니스 로직을 사용하여 시간 예측 레코드(**ProjForecastEmpl**)를 만들고 업데이트합니다.

프로젝트 회계사는 **프로젝트 관리 및 회계** > **모든 프로젝트** > **계획** > **시간 예측** 으로 이동하여 금융 및 운영 앱에서 생성된 예측 시간 레코드를 검토합니다.

## <a name="expense-estimates"></a>경비 추정

경비 추정은 프로젝트 관리자가 Dataverse의 **프로젝트 세부 정보** 페이지에 있는 **경비 추정** 탭에서 생성합니다 . 경비 추정 기록은 Dataverse의 **추정 라인** 엔터티에 저장됩니다. 이러한 추정 레코드에는 트랜잭션 클래스 **경비** 가 있으며 **경비 추정을 위한 Project Operations 통합 엔터티(msdyn\_estimatelines)** 를 사용하여 금융 및 운영 앱의 비용 예측 레코드와 동기화됩니다.

   ![경비 추정 통합.](./Media/DW4ExpenseEstimates.png)

이중 쓰기는 경비 추정 레코드를 준비 테이블(**ProjCDSEstimateExpenseImport**)과 동기화한 다음 비즈니스 로직을 사용하여 경비 예측 레코드(**ProjForecastCost**)를 만들고 업데이트합니다. 견적 라인은 판매 견적 및 비용 견적 레코드를 별도로 저장합니다. 금융 및 운영 앱의 비즈니스 논리는 준비 테이블의 이 세부 정보를 사용하여 단일 비용 예측 레코드를 채웁니다.

프로젝트 회계사는 **프로젝트 관리 및 회계** > **모든 프로젝트** > **계획** > **경비 예측** 으로 이동하여 금융 및 운영 앱에서 경비 예측 레코드를 검토할 수 있습니다.

## <a name="material-estimates"></a>재료 추정

재료 추정은 프로젝트 관리자가 Dataverse의 **프로젝트 세부 정보** 페이지에 있는 **재료 추정** 탭에서 생성합니다 . 재료 추정 기록은 Dataverse의 **추정 라인** 엔터티에 저장됩니다. 이러한 추정 레코드에는 트랜잭션 클래스 **자재** 가 있으며 **자재 추정을 위한 Project Operations 통합 엔터티(msdyn\_estimatelines)** 를 사용하여 금융 및 운영 앱의 항목 예측 레코드와 동기화됩니다.

   ![재료 추정 통합.](./Media/DW4MaterialEstimates.png)

이중 쓰기는 재료 추정 레코드를 준비 테이블(**ProjForecastSalesImpor**)과 동기화한 다음 비즈니스 로직을 사용하여 항목 예측 레코드(**ForecastSales**)를 만들고 업데이트합니다. 견적 라인은 판매 견적 및 비용 견적 레코드를 별도로 저장합니다. 금융 및 운영 앱의 비즈니스 논리는 준비 테이블의 이 세부 정보를 사용하여 단일 품목 예측 레코드를 채웁니다.

프로젝트 회계사는 **프로젝트 관리 및 회계** > **모든 프로젝트** > **계획** > **품목 예측** 으로 이동하여 금융 및 운영 앱에서 품목 예측 레코드를 검토할 수 있습니다.

## <a name="project-actuals"></a>프로젝트 실제

프로젝트 실제는 Dataverse에서 시간, 경비, 재료 및 청구 활동을 기반으로 생성됩니다. 수량, 원가, 판매 가격 및 프로젝트를 포함한 이러한 트랜잭션의 모든 운영 속성이 이 Dataverse 엔터티에 캡처됩니다. 자세한 내용은 [실제](../actuals/actuals-overview.md)를 참조하십시오. 실제 레코드는 다운스트림 회계를 위해 이중 쓰기 테이블 맵 **Project Operations 통합 실제 값(msdyn\_actuals)** 을 사용하여 금융 및 운영 앱에 동기화됩니다.

   ![실제 통합.](./Media/DW4Actuals.png)

**Project Operations 통합 실제** 테이블 맵은 속성 **동기화 건너뛰기(내부 전용)** 를 **False** 로 설정된 Dataverse에 있는 **실제** 엔터티의 모든 레코드를 동기화합니다. 이 속성 값은 Dataverse에서 레코드가 생성될 때 자동으로 설정됩니다. 이 속성이 **True** 로 설정된 예:

  - 내부 거래 트랜잭션에 대한 프로젝트 원가 실제. 자세한 내용은 [내부 거래 트랜잭션 생성](../project-accounting/create-intercompany-transactions.md)을 참조하십시오. 이러한 레코드는 회사 간 공급업체 송장이 게시될 때 시스템이 금융 및 운영 앱에서 실제 프로젝트 비용을 다시 생성하기 때문에 건너뜁니다.
  - 견적 송장이 확인될 때 생성된 청구되지 않은 음수 판매 기록. 금융 및 운영 앱의 프로젝트 보조원장은 송장 발행 시 미청구 판매 레코드를 취소하지 않고 상태를 완전 송장 발행으로 변경하기 때문에 이러한 레코드는 건너뜁니다.

이중 쓰기 테이블 맵은 실제 레코드를 준비 테이블 **ProjCDSActualsImport** 에 동기화합니다. 이러한 레코드는 Project Operations 통합 분개장 라인 및 프로젝트 송장 제안 라인을 생성할 때 주기적인 프로세스 **준비 테이블에서 가져 오기** 에 의해 처리됩니다. 자세한 내용은 [Project Operations의 통합 분개장](../project-accounting/project-operations-integration-journal.md)을 참조하십시오.

Dataverse는 **트랜잭션 연결** 엔터티의 프로젝트 실제 트랜잭션 간의 링크도 캡처합니다. 자세한 내용은 [실제를 원본 레코드에 연결](../actuals/linkingactuals.md)을 참조하십시오. 실제 트랜잭션 간의 링크는 이중 쓰기 테이블 맵인 **프로젝트 트랜잭션 관계에 대한 통합 엔터티(msdyn\_transactionconnections)** 를 사용하여 금융 및 운영 앱과도 동기화됩니다. 이러한 레코드는 Project Operations 통합 분개장 라인 및 프로젝트 송장 제안 라인을 생성할 때 주기적인 프로세스 **준비 테이블에서 가져 오기** 에 의해 사용됩니다.

Project Operations 통합 분개장 및 프로젝트 송장 제안을 전기하면 준비 테이블 **ProjCDSActualsImport** 의 각 레코드에서 업데이트가 트리거됩니다. 시스템은 실제 트랜잭션에 대해 다음 회계 속성을 캡처하고 기록합니다.

- 회계 통화 금액
- 환율
- 바우처 번호
- 판매세 금액

**Project Operations 통합 실제** 테이블 맵은 이 정보로 Dataverse의 각 실제 레코드를 업데이트합니다.
