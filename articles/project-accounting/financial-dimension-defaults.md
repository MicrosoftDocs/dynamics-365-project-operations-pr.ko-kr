---
title: 재무 차원 기본값
description: 이 항목은 재무 차원 기본값을 설정하는 방법에 대한 정보를 제공합니다.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922946"
---
# <a name="financial-dimension-defaults"></a>재무 차원 기본값

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations는 Dynamics 365 Finance의 [재무 차원](/dynamics365/finance/general-ledger/financial-dimensions) 프레임 워크를 사용하여 프로젝트 보조 원장 및 총계정 원장 트랜잭션에 대한 추가 통찰력을 제공합니다.

기본 재무 차원은 고객, 프로젝트 자금 출처, 중요 시점, 프로젝트 계약 내용 또는 프로젝트에서 설정할 수 있습니다.

## <a name="define-default-financial-dimensions-for-a-customer"></a>고객에 대한 기본 재무 차원 정의

고객 차원 기본값은 Finance에 지정됩니다. 차원 기본값을 설정하려면 다음 단계를 완료하십시오.

1. **수취 계정** > **고객** > **모든 고객** 으로 이동합니다.
2. **고객** 페이지의 **재무 차원** 탭에서 특정 고객에 대한 재무 차원 값을 설정합니다.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>프로젝트 계약에 대한 기본 재무 차원 정의

프로젝트 계약은 Common Data Service(CDS)에서 생성되고 유지됩니다. 프로젝트 계약에 대한 회계 특성은 Finance의 **프로젝트 관리 및 회계** 모듈에서 설정됩니다.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>프로젝트 자금 출처에 대한 재무 차원 설정

1. **프로젝트 관리 및 회계** > **프로젝트** > **프로젝트 계약** 으로 이동합니다.
2. 업데이트할 레코드를 선택하고 **프로젝트 계약** 탭에서 **기본 회계 표시** 를 선택합니다.
3. **관련 정보** 를 확장하고 **자금 출처** 탭을 선택합니다.
4. 재무 차원 기본값을 설정합니다. 재무 차원의 기본값은 고객 계정에서 설정됩니다.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>프로젝트 계약 내용에 대한 재무 차원 설정

1. **프로젝트 관리 및 회계** > **프로젝트** > **프로젝트 계약** 으로 이동합니다.
2. 업데이트할 레코드를 선택하고 **프로젝트 계약** 탭에서 **기본 회계 표시** 를 선택합니다.
3. **관련 정보** 를 확장하고 **계약 내용** 탭을 선택합니다.
4. 재무 차원 기본값을 설정합니다. 재무 차원 기본값이 적용 가능하며 고정 가격(중요 시점) 계약 내용에서만 사용할 수 있습니다.

이러한 기본값은 관련 프로젝트 미적용 거래 및 송장 라인에 사용됩니다.

## <a name="define-default-financial-dimensions-for-projects"></a>프로젝트에 대한 기본 재무 차원 정의

프로젝트는 CDS에서 생성되고 유지됩니다. 프로젝트에 대한 회계 특성은 Finance의 **프로젝트 관리 및 회계** 모듈에서 설정됩니다.

1. **프로젝트 관리 및 회계** > **프로젝트** > **모든 프로젝트** 로 이동합니다.
2. 업데이트할 레코드를 선택하고 **프로젝트** 탭에서 **기본 회계 표시** 를 선택합니다.
3. **관련 정보** 를 확장하고 **설정** 탭을 선택합니다.
4. 재무 차원 기본값을 설정합니다. 재무 차원의 기본값은 고객 계정에서 설정됩니다. 프로젝트가 여러 프로젝트 계약 고객이 있는 계약 내용과 연결된 경우 기본 고객이 재무 차원의 기본값에 사용됩니다.

프로젝트 기본 재무 차원은 **Project Operations 통합 분개장** 및 관련 프로젝트 송장 라인에서 시간, 경비 및 요금 트랜잭션에 대한 분개장 항목 기본값을 설정하는 데 사용됩니다.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>프로젝트 시간 항목에 재무 차원 적용
프로젝트 시간 항목에 재무 차원을 적용하려면 기본 차원 값이 다음 순서를 기반으로 합니다.

1. 리소스
2. Project
3. 자금 출처

예를 들어 기본 차원이 리소스에 지정된 경우 프로젝트에 지정된 기본값 위에 적용됩니다. 마찬가지로 기본 프로젝트 차원은 자금 조달 소스에 지정된 기본값 위에 적용됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
