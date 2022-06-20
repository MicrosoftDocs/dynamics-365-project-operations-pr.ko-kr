---
title: 프로젝트 계약 관리
description: 이 문서에서는 프로젝트 기반 계약 보기에 대한 정보를 제공합니다.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: acf1331068ccd1cbbf6a63f85c1bc424889f67e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917262"
---
# <a name="manage-project-contracts"></a>프로젝트 계약 관리

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

Dynamics 365 Project Operations의 프로젝트 계약은 프로젝트의 약정 및 청구 세부 정보에 대해 계약상 합의된 내용을 캡처하고 관리합니다. Project Operations의 프로젝트 계약 구조는 다음 구성 요소를 사용하여 프로젝트 기반 작업에 맞게 조정됩니다.

- 프로젝트 송장에서 상위 수준 구성 요소로 표시될 작업의 개별 구성 요소를 식별하는 계약 내용입니다.
- 각 상위 수준 구성 요소 또는 계약 내용에 대한 작업을 식별하고 추정하는 계약 내용 세부 정보입니다. 추정에는 계약 내용에 연결된 작업에 대한 일정 및 재정적 측면이 포함됩니다.
- 계약 모델 및 청구 가능 구성 요소는 각 계약 내용 및 전체 계약에 대한 청구 약정을 보유하는 각 계약 내용에 대해 설정됩니다.

## <a name="view-all-project-based-contracts"></a>모든 프로젝트 기반 계약 보기

모든 프로젝트 계약 목록은 **견적** 목록 페이지에서 볼 수 있습니다. 

1. **영업** > **연락처** 로 이동합니다. 시스템의 모든 프로젝트 계약 목록이 표시됩니다. 
2. **보기 전환기**(보기 이름 옆의 드롭다운 화살표)를 선택하여 다른 필터링된 보기를 선택합니다. 사용자 지정 필터 기준을 사용하여 고유한 보기를 만들 수 있습니다.

이 목록 페이지 또는 세부 사항 페이지에서 계약을 작성하거나 삭제할 수 있습니다.

> [!NOTE]
> 연관된 프로젝트, 작업, 견적, 분개장 및/또는 실제가 있는 계약은 삭제할 수 없습니다. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
