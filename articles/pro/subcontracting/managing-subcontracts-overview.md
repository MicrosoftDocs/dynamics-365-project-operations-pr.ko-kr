---
title: Project Operations에서 하도급 관리
description: 이 항목에서는 Microsoft Dynamics 365 Project Operations의 종단 간 하도급 관리 프로세스에 대한 개요를 제공합니다.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994239"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations에서 하도급 관리

[!include [banner](../../includes/dataverse-preview.md)]

_**적용 대상:** 라이트 배포 - 견적 송장 거래_

Microsoft Dynamics 365 Project Operations의 하도급 계약은 다음 비즈니스 프로세스 흐름를 지원합니다.

![하도급 계약 프로세스 흐름](../media/SubcontractingProcessFlow.png)

다음은 하도급 계약 프로세스에 대한 단계별 설명입니다.

1. 프로젝트 관리자는 공급업체와 하도급 계약을 생성합니다. 기본적으로 공급업체 레코드에 첨부된 가격표가 하도급 계약에 사용됩니다. 공급업체 거래처의 관계 유형은 **공급업체** 또는 **공급자** 입니다.
2. 프로젝트 관리자는 모든 구매를 하도급 계약의 항목으로 항목화할 수 있습니다. 하도급 계약 라인은 시간, 경비 또는 제품에 대한 것일 수 있습니다. 각 하도급 계약 라인에서 선택한 트랜잭션 클래스에 따라 해당 라인이 결정됩니다.
3. 공급업체 거래처 관리자와 프로젝트 관리자는 하도급 계약을 반복할 수 있습니다. 가격 책정은 하도급 계약에 첨부된 구매 가격표에서 조정할 수 있습니다.
4. 프로세스의 이 시점 또는 이후에 하도급 계약 라인이 시간을 위한 것이라면 공급업체 거래처 관리자는 연락처를 각 하도급 계약 라인과 연결합니다. 이 연결은 하도급 계약을 수행하는 프로젝트 관리자에게 정보를 제공합니다. 연락처가 하도급 계약 라인과 연결되어 있을 때 예약 가능한 리소스가 아직 없는 경우 시스템은 연락처로부터 예약 가능한 리소스를 자동으로 생성합니다.
5. 각 하도급 계약 라인의 청구 방법은 **고정 가격** 또는 **시간과 재료** 가 될 수 있습니다. 고정 가격 하도급 계약 라인의 경우 중요 시점 기반 송장 일정을 설정할 수 있습니다.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
