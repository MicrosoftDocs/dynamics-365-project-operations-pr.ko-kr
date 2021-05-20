---
title: 공급업체 송장 통합
description: 이 항목은 Project Operations의 공급업체 송장 통합에 대한 정보를 제공합니다.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955790"
---
# <a name="vendor-invoice-integration"></a>공급업체 송장 통합

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Dynamics 365 Project Operations의 프로젝트 관련 조달은 **지급 계정** > **송장** > **보류 중인 공급업체 송장** 으로 이동하고 보류 중인 공급업체 송장 문서를 사용하여 기록할 수 있습니다. 자세한 내용은 [보류 중인 공급업체 송장을 사용하여 비 재고 재료 구매](../procurement/pending-vendor-invoices.md)를 참조하십시오.

> [!IMPORTANT]
> 이 항목에 설명된 기능을 사용하기 전에 필요한 구성을 검토하고 적용하십시오. 자세한 내용은 [비 재고 재료 및 보류 중인 공급업체 송장 활성화](../procurement/configure-materials-nonstocked.md)를 참조하십시오.

Project Operations에서 프로젝트 관련 공급업체 송장은 특별 전기 규칙을 사용하여 전기됩니다.

- 프로젝트 관련 비용(불 공제 세금 포함)은 총계정 원장의 프로젝트 비용 계정에 즉시 전기되지 않습니다. 대신 비용이 **조달 통합 계정** 에 전기됩니다. 이 계정은 **프로젝트 관리 및 회계** > **설정** > **프로젝트 관리 및 회계 매개변수**, **Dynamics 365 Customer engagement의 Project Operations** 탭에서 구성됩니다.
- 이중 쓰기는 다음 테이블 맵을 사용하여 공급업체 송장 세부 정보를 Microsoft Dataverse에 동기화합니다.

     - **Project Operations 통합 프로젝트 공급업체 송장 내보내기 엔터티(msdyn_projectvendorinvoices)**: 이 테이블 맵은 공급업체 송장 헤더 정보를 동기화합니다. 프로젝트 ID가 포함된 라인이 하나 이상 있는 공급업체 송장만 Dataverse에 동기화됩니다.
     - **Project Operations 통합 프로젝트 공급업체 송장 라인 내보내기 엔터티(msdyn_projectvendorinvoicelines)**: 이 테이블 맵은 공급업체 송장 라인 정보를 동기화합니다. 프로젝트 ID가 포함된 라인만 Dataverse에 동기화됩니다.

     > [!NOTE]
     > Dataverse의 공급업체 송장 세부 정보는 편집할 수 없습니다.

세금 보조 원장, 공급업체 보조 원장 및 기타 재무 전기는 공급업체 송장이 전기될 때 Dynamics 365 Finance에 해당하는 대로 기록됩니다.

![공급업체 송장 통합](media/DW7VendorInvoice.png)

Dataverse의 **공급업체 송장** 엔터티에 레코드가 기록되면 레코드의 자동 승인 프로세스가 시작됩니다. 필요한 경우 **고급 설정** > **시스템** > **시스템 작업** 으로 이동하여 Dataverse에서 자동 승인 프로세스 상태를 검토할 수 있습니다. 승인이 완료된 후 시스템은 **실제** 엔터티에 재료 트랜잭션 클래스 레코드를 생성합니다.

그런 다음 재료 관련 실제 값은 이중 쓰기 테이블 맵 **Project Operations 통합 실제(msdyn_actuals)** 를 사용하여 처리됩니다. 자세한 내용은 [프로젝트 추정 및 실제](resource-dual-write-estimates-actuals.md)를 참조하십시오.

주기적 프로세스인 **준비에서 가져오기** 는 공급업체 송장 관련 Project Operations 통합 분개장을 생성합니다. 오프셋 계정의 기본값은 조달 통합 계정입니다. 통합 분개장이 전기되면 공급업체 송장 트랜잭션에 대한 계정 잔액이 반제되고 라인 금액이 프로젝트 원가 계정으로 이동됩니다. 프로젝트 보조 원장 트랜잭션은 다운스트림 송장 발행 및 수익 인식 목적으로도 생성됩니다.
