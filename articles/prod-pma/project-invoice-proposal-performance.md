---
title: 프로젝트 송장 제안서 성능
description: 이 문서에서는 프로젝트 송장 제안의 성능 향상에 대한 정보를 제공합니다.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927198"
---
# <a name="project-invoice-proposal-performance"></a>프로젝트 송장 제안서 성능

[!include [banner](../includes/banner.md)]

새 송장 제안을 생성할 때 프로젝트 및 하위 프로젝트 수가 증가함에 따라 성능 문제가 발생할 수 있습니다. 성능을 향상시키기 위해 게시된 프로젝트 트랜잭션에 대한 새 송장 제안을 생성하는 데 필요한 시간을 줄이는 기능을 사용할 수 있습니다.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>프로젝트 송장 제안 성능 향상 활성화
프로젝트 송장 제안 성능 향상 기능을 사용하려면 다음 단계를 완료하십시오.

1.  **기능 관리** > **모두** 로 이동합니다. 기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.
2.  **지금 사용** 을 선택합니다.
3.  브라우저를 새로 고친 다음 새 송장 제안을 만듭니다.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>프로젝트 송장 제안 성능 향상 끄기
프로젝트 송장 제안 성능 향상을 끄려면 다음 단계를 완료하십시오.

1.  **기능 관리** > **모두** 로 이동합니다. 기능 목록에서 **프로젝트 송장 제안 성능 향상** 을 찾습니다.
2.  **사용 안 함** 을 선택합니다.
3.  브라우저를 새로 고칩니다.

> [!NOTE]
> 청구 규칙이 활성화된 경우 송장 제안 성능을 적용할 수 없습니다.
> 
> 송장 제안을 생성하기 위한 배치 프로세스 동안 하위 작업의 수는 입력한 내용에 관계없이 송장 가능한 트랜잭션이 있는 계약 수를 기반으로 작업을 최대 수로 분할합니다. 예를 들어 **3** 을 입력하면 일괄 송장 제안 생성을 위한 하위 작업의 수에 대해 송장 가능한 트랜잭션이 있는 두 개의 계약만 있고 두 개의 하위 작업만 생성됩니다.
