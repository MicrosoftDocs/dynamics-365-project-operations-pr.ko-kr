---
title: 프로젝트 업데이트
description: 이 항목은 Project Operations의 프로젝트 업데이트에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286391"
---
# <a name="update-a-project"></a>프로젝트 업데이트

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

다음은 프로젝트가 생성된 후 업데이트될 수 있는 필드와 업데이트의 적용 가능한 의미에 대한 요약입니다.

## <a name="project-detail-fields"></a>프로젝트 세부 사항 필드

- **이름**: 프로젝트의 제목입니다.
- **설명**: 프로젝트의 개요입니다.
- **고객**: 프로젝트를 전달할 회사입니다.
- **일정 템플릿**: 프로젝트의 작업 시간입니다. 필드가 변경되면 전체 일정이 다시 계산됩니다.
- **통화**: 프로젝트의 통화입니다. 이 필드의 기본값은 계약 단위에 정의된 통화를 기반으로 합니다. 계약 단위가 업데이트되면 필드도 업데이트됩니다.
- **계약 단위**: 판매에 성공하고 고객에게 작업 및 서비스 제공을 관리하는 책임이 있는 회사 그룹 또는 부서를 대표하는 조직 구성 단위입니다. 
- **프로젝트 관리자**: 시간 항목 및 경비를 검토하고 승인할 권한이 있는 프로젝트 팀 구성원입니다.

## <a name="estimate-fields"></a>추정 필드

- **예상 시작 날짜**: 프로젝트가 시작되는 날짜입니다. 이 필드가 업데이트되면 프로젝트의 모든 작업이 새 시작 날짜에 비례하여 이동합니다.
- **종료 날짜**: 프로젝트 종료 예정 날짜입니다.
- **작업량**: 프로젝트의 예상 작업량입니다. 프로젝트에 작업이 추가되면 이 필드는 더 이상 편집할 수 없습니다.
- **예상 노동 비용**: 프로젝트의 예상 노동 비용입니다. 프로젝트에 노동 비용이 추가되면 이 필드는 더 이상 편집할 수 없습니다.
- **예상 경비**: 프로젝트의 예상 경비입니다. 프로젝트에 경비가 추가되면 이 필드는 더 이상 편집할 수 없습니다.

## <a name="project-actual-fields"></a>프로젝트 실제 필드
- **실제 시작**: 프로젝트가 시작된 날짜입니다.
- **실제 종료**: 프로젝트가 완료되면 업데이트됩니다.

## <a name="project-status-fields"></a>프로젝트 상태 필드

- **전체 프로젝트 상태**: 프로젝트 관리자가 제공한 전체 프로젝트 상태입니다.
- **댓글**: 프로젝트 관리자가 제공한 프로젝트의 현재 상태에 대한 댓글입니다.



[!INCLUDE[footer-include](../includes/footer-banner.md)]