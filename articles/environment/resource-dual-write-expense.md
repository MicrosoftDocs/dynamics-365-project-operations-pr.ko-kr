---
title: 경비 관리 통합
description: 이 항목에서는 이중 쓰기를 사용하여 Project Operations에서 경비 보고서 통합에 대한 정보를 제공합니다.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986589"
---
# <a name="expense-management-integration"></a>경비 관리 통합

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목에서는 이중 쓰기를 사용하여 Project Operations [전체 경비 배포](../expense/expense-overview.md)에서 경비 보고서 통합에 대한 정보를 제공합니다.

## <a name="expense-categories"></a>경비 범주

전체 경비 배포에서 경비 범주는 Finance and Operations 앱에서 생성 및 유지됩니다. 새 경비 범주를 생성하려면 다음 단계를 완료하십시오.

1. Microsoft Dataverse에서 **트랜잭션** 범주를 생성합니다. 이중 쓰기 통합은 이 트랜잭션 범주를 Finance and Operations 앱과 동기화합니다. 자세한 내용은 [프로젝트 범주 구성](/dynamics365/project-operations/project-accounting/configure-project-categories) 및 [Project Operations 설정 및 구성 데이터 통합](resource-dual-write-setup-integration.md)을 참조하십시오. 이 통합의 결과로 시스템은 Finance and Operations 앱에 4개의 공유 범주 레코드를 생성합니다.
2. Finance에서 **경비 관리** > **설정** > **공유 범주** 로 이동하고 **경비** 트랜잭션 클래스를 사용하여 공유 범주를 선택합니다. **경비에 사용할 수 있음** 매개 변수를 **True** 로 설정하고 사용할 경비 유형을 정의합니다.
3. 이 공유 범주 레코드를 사용하여 **경비 관리** > **설정** > **경비 범주** 로 이동하고 **새로 만들기** 를 선택하여 새 경비 범주를 만듭니다. 레코드가 저장되면 이중 쓰기는 테이블 맵, **Project Operations 통합 프로젝트 경비 범주 내보내기 엔터티(msdyn\_expensecategories)** 를 사용하여 이 레코드를 Dataverse에 동기화합니다.

  ![경비 범주 통합.](./media/DW6ExpenseCategories.png)

Finance and Operations 앱의 경비 범주는 회사 또는 법인별로 다릅니다. Dataverse에는 별도의 해당 법인별 레코드가 있습니다. 프로젝트 관리자가 경비를 추정할 때 작업 중인 프로젝트를 소유한 회사가 아닌 다른 회사가 소유한 프로젝트에 대해 생성된 경비 범주를 선택할 수 없습니다. 

## <a name="expense-reports"></a>경비 보고서

경비 보고서는 Finance and Operations 앱에서 생성되고 승인됩니다. 자세한 내용은 [Dynamics 365 Project Operations 에서 경비 보고서 작성 및 처리](/learn/modules/create-process-expense-reports/)를 참조하십시오. 프로젝트 관리자가 경비 보고서를 승인하면 총계정 원장에 전기됩니다. Project Operations에서 프로젝트 관련 경비 보고서 라인은 특별 전기 규칙을 사용하여 전기됩니다.

  - 프로젝트 관련 원가(불 공제 세금 포함)는 총계정 원장의 프로젝트 원가 계정에 즉시 전기되지 않고 대신 비용 통합 계정에 전기됩니다. 이 계정은 **프로젝트 관리 및 회계** > **설정** > **프로젝트 관리 및 회계 매개변수**, **Dynamics 365 Customer engagement의 Project Operations** 탭에서 구성됩니다.
  - 이중 쓰기는 **Project Operations 통합 프로젝트 경비 내보내기 엔터티(msdyn\_expenses)** 테이블 맵을 사용하여 Dataverse에 동기화됩니다.
  - 세금 보조 원장, 공급 업체 보조 원장 및 기타 재무 전기는 경비 보고서 전기시 해당되는 대로 기록됩니다.

  ![경비 보고서 통합.](./media/DW6ExpenseReports.png)

Dataverse의 **경비** 항목에 레코드가 기록되면 시스템은 레코드의 자동화된 승인 프로세스를 트리거합니다. 필요한 경우 **고급 설정** > **시스템** > **시스템 작업** 으로 이동하여 Dataverse에서 자동 승인 프로세스 상태를 검토할 수 있습니다. 승인이 완료되면 **실제** 엔터티에 경비 트랜잭션 클래스 레코드가 생성됩니다.

그런 다음 경비 관련 실제 값은 이중 쓰기 테이블 맵 **Project Operations 통합 실제(msdyn\_actuals)** 를 사용하여 처리됩니다. 자세한 내용은 [프로젝트 추정 및 실제](resource-dual-write-estimates-actuals.md)를 참조하십시오.

주기적 프로세스인 **준비에서 가져오기** 는 Project Operations 통합 분개장에 경비 보고서 관련 분개장 항목을 생성합니다. 오프셋 계정의 기본값은 경비 통합 계정입니다. 전기 통합 분개장은 경비 트랜잭션에 대한 계정 잔액을 지우고 비용 금액을 프로젝트 원가 계정으로 이동합니다. 시스템은 또한 다운스트림 송장 발행 및 수익 인식 목적으로 프로젝트 보조 원장 트랜잭션을 생성합니다.
