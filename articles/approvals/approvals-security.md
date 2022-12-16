---
title: 보안 및 승인
description: 이 문서에서는 Microsoft Dynamics 365 Project Operations에서 승인 작업을 위한 보안 설정에 대한 정보를 제공합니다.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841932"
---
# <a name="security-and-approvals"></a>보안 및 승인

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Microsoft Dynamics 365 Project Operations에서는 두 가지 보안 역할을 사용하여 시간, 경비 및 자재 항목을 승인할 수 있습니다.

- 프로젝트 승인자
- 프로젝트 승인자 관리자

## <a name="project-approver"></a>프로젝트 승인자

프로젝트 시간, 경비 및 자재 항목을 승인하려면 **프로젝트 승인자r** 보안 역할이 있어야 합니다. 또한 **프로젝트** 와 같은 관련 관련 엔터티에 대한 액세스 권한이 있어야 합니다. 해당 액세스 권한은 **프로젝트 관리자** 역할이 있는 사람이 할당할 수 있습니다. 또한 프로젝트의 팀 구성원이어야 하며 승인자로 표시되어야 합니다.

프로젝트가 아닌 항목을 승인하려면 제출자의 관리자여야 합니다.

## <a name="project-approver-admin"></a>프로젝트 승인자 관리자

> [!NOTE]
> 프로젝트 승인자 관리 기능을 사용하려면 먼저 [승인 세트](approval-sets.md) 기능을 활성화해야 합니다.

**프로젝트 승인자 관리자** 보안 역할를 사용하면 사용자가 정책을 우회하고 모든 프로젝트에서 항목을 승인할 수 있습니다. 이 역할을 할당하면 팀 구성원 자격이 필요하고 승인자로 표시되는 유효성 검사 논리가 무시됩니다. 할당된 보안 역할을 통해 **프로젝트** 와 같은 관련 테이블에 대한 액세스 권한이 있어야 합니다.

SYSTEM 사용자 컨텍스트는 프로젝트 승인자 관리자 보안 역할와 동일한 방식으로 유효성 검사를 우회합니다.
