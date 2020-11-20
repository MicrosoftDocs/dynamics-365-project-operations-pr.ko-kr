---
title: 승인을 위한 개발자 노트
description: 이 항목은 승인 작업에 대한 추가 개발자 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483956"
---
# <a name="developer-notes-for-approvals"></a>승인을 위한 개발자 노트

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations에는 승인 단계를 통해 올바른 레코드 전환을 보장하는 유효성 검사 논리가 포함되어 있습니다. 올바른 레코드 전환은 다음을 보장합니다. 

  - 모든 지원 행은 분개장 및 실제와 같은 관련 테이블에 생성됩니다.
  - 승인자는 진행하기 전에 프로젝트에서 **프로젝트 승인자** 로 표시됩니다.
