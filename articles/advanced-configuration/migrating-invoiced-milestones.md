---
title: 전환 시 완전히 청구된 청구 마일스톤 마이그레이션
description: 이 항목에서는 개시 날짜 이전에 열린 프로젝트 계약에 대해 고객에게 청구된 고정 가격 청구 마일스톤을 마이그레이션하는 방법을 설명합니다.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576278"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>전환 시 완전히 청구된 청구 마일스톤 마이그레이션

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

## <a name="scenario"></a>시나리오

Contoso가 리소스/비재고 시나리오용 Microsoft Dynamics 365 Project Operations로 전환 중입니다. 전환 활동의 일부로 구현 팀은 이전 시스템에서 공개 프로젝트 계약을 마이그레이션해야 합니다. 일부 프로젝트 계약에는 고정 가격 청구 방법을 사용하고 이미 최종 고객에게 부분적으로 송장이 발행된 계약 내용이 포함됩니다. 구현 팀은 수익 인식을 위해 총 계약 금액에 포함되어야 하므로 이러한 청구 마일스톤을 **전기된 고객 송장** 으로 마이그레이션해야 합니다. 그러나 외상매출금 및 총계정원장의 고객 잔액은 영향을 받지 않아야 합니다.

## <a name="solution"></a>해결 방법

### <a name="prerequisites"></a>전제 조건

- Dynamics 365 Finance 10.0.24 이상이 설치되어 있어야 합니다.
- 마이그레이션 단계가 완료될 환경은 유지 관리 모드에 있어야 합니다. 마일스톤을 마이그레이션하는 동안 다른 활동을 수행하면 안 됩니다.
- 마이그레이션 단계는 여기에 설명된 대로 정확히 따라야 하며 전환 활동에만 사용할 수 있습니다. Microsoft는 이 기능의 다른 사용을 지원하지 않습니다.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operations 통합 계약 내용 마일스톤 이중 쓰기 맵의 전환 버전 생성 

1. **Project Operations 통합 계약 내용 마일스톤** 엔터티에 대한 대상 매핑이 최신 상태인지 확인합니다. 

    1. Finance에서 **데이터 관리** \> **데이터 엔터티** 로 이동하고 **Project Operations 통합 계약 내용 마일스톤** 엔터티를 선택합니다. 
    2. **대상 매핑 수정** 을 선택합니다. 
    3. **대상에 스테이징 매핑** 페이지에서 **매핑 생성** 을 선택한 다음 매핑 생성을 확인합니다.

2. **Project Operations 통합 계약 내용 마일스톤**(**msdyn\_contractlinescheduleofvalues**) 이중 쓰기 맵을 중지하고 새로 고칩니다. 

    1. **데이터 관리** \> **이중 쓰기** 로 이동하고 맵을 선택하고 세부 정보를 엽니다. 
    2. **중지** 를 선택하고 시스템이 맵을 중지할 때까지 기다립니다. 
    3. **테이블 새로 고침** 을 선택합니다.

3. 트랜잭션 상태에 대한 매핑을 추가합니다.

    1. **매핑 추가** 를 선택합니다.
    2. 새로운 라인의 **금융 및 운영 앱** 열에서 **TRANSSTATUS \[TRANSSTATUS\]** 필드를 선택합니다.
    3. **Microsoft Dataverse** 열에서 **msdyn\_invoicestatus \[Invoice status\]** 를 선택합니다.
    4. **맵 유형** 열에서 오른쪽 화살표(**\>**)를 선택합니다.
    5. 표시되는 대화 상자의 **동기화 방향** 필드에서 **Dataverse 금융 및 운영 앱** 을 선택합니다.
    6. **변환 추가** 를 선택합니다.
    7. **변환 유형** 필드에서 **ValueMap** 을 선택합니다.
    8. **값 매핑 추가** 를 선택합니다.
    9. 왼쪽 필드에 **4** 를 입력합니다. 오른쪽 필드에 **192350001** 을 입력합니다. 
    10. **저장** 을 선택한 다음 대화 상자를 닫습니다.

4. **다른 이름으로 저장** 을 선택하여 이중 쓰기 맵의 버전을 저장합니다. 
5. **테이블 추가** 창의 **판매자** 필드에서 **기본 판매자** 를 선택합니다.
6. **버전** 필드에 버전을 입력합니다.
7. **설명** 필드에 이 전환 버전의 맵에 대한 메모를 입력합니다. 
8. **저장** 을 선택합니다.
9. 맵을 시작합니다.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>송장 발부 마일스톤을 Dataverse 환경으로 마이그레이션합니다.

1. Project Operations Dataverse 환경에서 송장 상태가 **송장 발부 준비 완료** 인 마일스톤을 만듭니다. 이 시점에서 송장 발부되지 않은 마일스톤은 마이그레이션하지 마십시오.

    > [!NOTE]
    > 청구 마일스톤을 마이그레이션하기 전에 프로젝트 계약 내용과 관련된 재무 차원이 예상대로 설정되었는지 확인하십시오. 마이그레이션이 완료된 후에는 재무 차원을 편집할 수 없습니다.

2. 모든 마일스톤이 마이그레이션된 후 다음 이중 쓰기 맵을 중지합니다.

    - Project Operations 통합 계약 내용 이정표(msdyn\_contractlinescheduleofvalues)
    - Project Operations 통합 실제(msdyn\_actuals)
    - 프로젝트 송장 제안서 V2(송장)

    맵을 중지하려면 다음 단계를 수행합니다.

    1. Finance에서 **데이터 관리** \> **이중 쓰기** 로 이동하고 맵을 선택하고 세부 정보를 엽니다.
    2. **중지** 를 선택하고 시스템이 맵을 중지할 때까지 기다립니다.

3. Project Operations Dataverse 환경에서 청구 마일스톤에 대한 견적 송장을 만들고 확인합니다. 

    1. 사이트맵에서 프로젝트 계약으로 이동하여 계약을 선택한 후 **송장 생성** 을 선택합니다.
    2. 송장이 생성되면 사이트 맵의 **송장** 메뉴에서 송장을 열고 **확인** 을 선택합니다.

    이 단계에서는 Dataverse 환경에서 필요한 레코드를 생성합니다. 그러나 이전에 나열된 이중 쓰기 맵이 중지되었으므로 재무 및 미수금에는 영향을 미치지 않습니다.

4. 모든 견적 송장이 확인되면 모든 이중 쓰기 맵을 초기 상태로 되돌립니다.

    1. **Project Operations 통합 계약 내용 마일스톤**(**msdyn\_contractlinescheduleofvalues**) 이중 쓰기 맵의 버전을 원본으로 업데이트합니다. 
    2. 맵 목록에서 이중 쓰기 맵을 선택하고 **테이블 맵 버전** 을 선택한 다음 테이블 맵의 원본 버전을 선택합니다.
    3. **저장** 을 선택합니다.
    4. 다음 이중 쓰기 맵을 다시 시작합니다.

        - Project Operations 통합 계약 내용 이정표(msdyn\_contractlinescheduleofvalues)
        - Project Operations 통합 실제(msdyn\_actuals)
        - 프로젝트 송장 제안서 V2(송장)

이제 마일스톤이 마이그레이션되었으며 시스템은 전환 활동의 다음 단계를 위한 준비가 되었습니다.
