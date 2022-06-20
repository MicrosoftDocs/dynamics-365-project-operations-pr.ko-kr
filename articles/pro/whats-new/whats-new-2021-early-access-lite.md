---
title: 새로운 기능 2021 웨이브 2 조기 액세스 - Project Operations 라이트 배포
description: 이 문서에서는 Project Operations Lite 배포의 2021년 웨이브 2 조기 액세스 릴리스에서 사용할 수 있는 기능에 대한 정보를 제공합니다.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924116"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>새로운 기능 2021 웨이브 2 조기 액세스 - Project Operations 라이트 배포

_적용 대상: 라이트 배포 - 견적 송장 거래_

이 문서는 다음 Dynamics 365 Project Operations 구성 요소 및 버전에 적용됩니다.

  - Dataverse 환경 버전 4.23.0.4의 Project Operations

릴리스는 환경이 [조기 액세스를 선택](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates)한 경우에만 적용됩니다.

## <a name="features-included-in-this-release"></a>이 릴리스에 포함된 기능

[하도급 계약 관리](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - 이 기능은 프로젝트 작업의 모든 측면에 대한 더 나은 가시성과 제어를 제공합니다. 하도급 계약 관리 프리뷰에는 다음 기능이 포함됩니다.

  - 프로젝트 관리자는 공급업체와 하도급 계약을 생성할 수 있습니다. 기본적으로 공급업체 레코드에 첨부된 가격표가 하도급 계약에 사용됩니다. 공급업체 거래처의 관계 유형은 **공급업체** 또는 **공급자** 입니다.
  - 프로젝트 관리자는 모든 구매를 하도급 계약의 항목으로 항목화할 수 있습니다. 하도급 계약 라인은 시간, 경비 또는 제품에 대한 것일 수 있습니다. 하도급 계약 라인의 트랜잭션 클래스에 따라 해당 라인이 결정됩니다.
  - 공급업체 거래처 관리자와 프로젝트 관리자는 하도급 계약을 반복할 수 있습니다. 가격 책정은 하도급 계약에 첨부된 구매 가격표에서 조정할 수 있습니다.
  - 프로세스 중에 하도급 계약 내용이 시간을 위한 것이라면 공급업체 계정 관리자는 공급업체 연락처를 각 하도급 계약 내용과 연결할 수 있습니다. 이 연결은 하도급 계약을 수행하는 프로젝트 관리자에게 정보를 제공합니다. 공급업체 연락처가 하도급 계약 라인과 연결되어 있을 때 예약 가능한 리소스가 아직 없는 경우 시스템은 연락처로부터 예약 가능한 리소스를 자동으로 생성합니다.
  - 각 하도급 계약 라인의 청구 방법은 고정 가격 또는 시간과 재료가 될 수 있습니다. 고정 가격 하도급 계약 라인의 경우 중요 시점 기반 송장 일정이 설정됩니다.
