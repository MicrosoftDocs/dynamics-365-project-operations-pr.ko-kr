---
title: 공급업체 재방문 주기 설정
description: 이 항목에서는 공급업체 보존을 설정하는 방법을 설명합니다.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594606"
---
# <a name="set-up-vendor-retention"></a>공급업체 재방문 주기 설정

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

이 항목에서는 공급업체 보존을 설정하는 방법에 대한 정보를 제공합니다.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>총계정원장에서 공급업체 유지 계정 설정

1. Dynamics 365 Finance에서 **총계정 원장** > **게시 설정** > **자동 거래 계정** 으로 이동합니다.
2. 새 라인을 추가합니다.
3. **게시 유형** 필드에서 **공급업체 유지** 를 선택합니다.
4. 공급업체 유지 전기에 대한 기본 계정을 선택합니다.

## <a name="create-vendor-retention-terms"></a>공급업체 유지 기간 생성

**공급업체 유지 기간** 페이지를 사용하여 공급업체 지불에 대한 보존 기간을 설정하고 유지합니다. 유지할 공급업체 지불의 백분율과 해제할 이전에 유지된 금액의 백분율을 입력합니다. 계약이 지정된 완료 상태에 도달할 때까지 금액이 공급업체 송장에 자동으로 유지됩니다. 공급업체에 대해 보존 기간을 설정한 후에는 공급업체가 작업하는 모든 프로젝트에 적용할 수 있습니다.

1. Finance에서 **프로젝트 관리 및 회계** > **설정** > **보유** > **공급업체 지불 유지 기간** 으로 이동합니다.
2. **새로 만들기** 를 선택하여 새 공급업체 유지 기간을 추가합니다. 새 용어에 대한 **규칙 ID** 필드의 값이 자동으로 입력됩니다. 
3. **설명** 필드에 새 용어의 설명 이름을 입력합니다.
4. **용어** 탭에서 **라인 추가** 를 선택하여 공급업체 보존 기간을 입력합니다.
5. **배송된 단위 비율** 필드에 규칙 완료율을 입력합니다. 금액은 프로젝트 완료 단계가 입력한 백분율과 같아질 때까지 공급업체 송장에 자동으로 유지됩니다. 예를 들어 50.00을 입력하면 프로젝트가 50% 완료될 때까지 금액이 유지됩니다.
6. **유지 비율** 필드에 보유할 공급업체 송장 금액의 백분율을 입력합니다. 예를 들어 이 필드에 10.00을 입력하면 프로젝트가 **배송된 단위 비율** 필드에서 선택한 완료 비율에 도달할 때까지 공급업체 송장 금액의 10%가 유지됩니다.
7. **해제 비율** 필드에 선택한 프로젝트 완료 레벨에서 해제할 이전에 보유된 금액의 백분율을 입력합니다.

> [!NOTE]
> 다른 수준의 프로젝트 완료에 대해 둘 이상의 마일스톤이 있는 경우 모든 보관 규칙에 대해 별도의 공급업체 보관 기간 라인을 입력합니다. 각 라인은 프로젝트 완료의 지정된 레벨에 대해 다른 유지 비율과 해제 비율을 지정할 수 있습니다.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>프로젝트에 대한 공급업체 계약 설정

프로젝트에 적용되는 공급업체 보존 조건을 설정합니다. 공급업체 유지 기간은 공급업체에 대해 생성한 구매 주문에도 표시됩니다.

1. Finance에서 **프로젝트 관리 및 회계** > **프로젝트** > **모든 프로젝트** 로 이동합니다. 
2. 프로젝트를 선택하고 작업 창에서 **프로젝트 그룹** > **공급업체 계약** 을 선택합니다.
3. **공급업체 계약** 페이지에서 새 줄을 추가합니다.
4. **계정 코드 필드** 필드에서 다음 옵션 중 하나를 선택합니다.
   - **테이블**: 공급업체 유지 조건은 단일 공급업체에 적용됩니다.
   - **그룹**: 공급업체 유지 조건은 공급업체 그룹의 모든 공급 업체에 적용됩니다.
   - **모두**: 공급업체 유지 조건은 모든 공급업체에 적용됩니다.
5. **공급업체/공급업체 그룹** 필드에서 공급업체 유지 조건이 적용되는 공급업체 또는 공급업체 그룹을 선택합니다. **모두** 를 선택한 경우 이전 단계에서는 이 필드를 사용할 수 없습니다.
6. **공급업체 유지 기간** 필드에서 이 공급업체에 적용할 보존 조건의 규칙 ID를 선택합니다.
