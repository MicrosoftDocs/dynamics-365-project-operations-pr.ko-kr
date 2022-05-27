---
title: 승인을 위한 개발자 노트
description: 이 항목은 승인 작업에 대한 추가 개발자 정보를 제공합니다.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579728"
---
# <a name="developer-notes-for-approvals"></a>승인을 위한 개발자 노트

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations에는 승인 단계를 통해 올바른 레코드 전환을 보장하는 유효성 검사 논리가 포함되어 있습니다. 올바른 레코드 전환은 다음을 보장합니다. 

  - 모든 지원 행은 분개장 및 실제와 같은 관련 테이블에 생성됩니다.
  - 승인자는 진행하기 전에 프로젝트에서 **프로젝트 승인자** 로 표시됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]