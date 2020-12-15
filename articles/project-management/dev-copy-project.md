---
title: 프로젝트 복사로 프로젝트 템플릿 개발
description: 이 항목은 프로젝트 복사 사용자 지정 작업을 사용하여 프로젝트 템플릿을 만드는 방법에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642416"
---
# <a name="develop-project-templates-with-copy-project"></a>프로젝트 복사로 프로젝트 템플릿 개발

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations는 프로젝트를 복사하고 할당을 역할을 나타내는 일반 리소스로 되돌리는 기능을 지원합니다. 고객은 이 기능을 사용하여 기본 프로젝트 템플릿을 만들 수 있습니다.

**프로젝트 복사** 를 선택하면 대상 프로젝트의 상태가 업데이트됩니다. **상태 설명** 을 사용하여 복사 작업이 완료되는 시기를 결정합니다. 또한 **프로젝트 복사** 를 선택하면 대상 프로젝트 엔터티에서 대상 날짜가 감지되지 않는 경우 프로젝트의 시작 날짜를 현재 시작 날짜로 업데이트합니다.

## <a name="copy-project-custom-action"></a>프로젝트 사용자 지정 작업 복사 

### <a name="name"></a>Name 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>입력 매개 변수
3개의 입력 매개 변수가 있습니다.

| 매개 변수          | 종류   | 값                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** 또는 **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 엔터티 참조 | 원본 프로젝트 |
| 대상             | 엔터티 참조 | 대상 프로젝트 |


- **{"clearTeamsAndAssignments": true}** : 웹용 프로젝트의 기본 동작이며 모든 할당 및 팀 구성원을 제거합니다.
- **{"removeNamedResources": true}** Project Operations의 기본 동작이며 할당을 일반 리소스로 되돌립니다.

작업에 대한 자세한 내용은 [웹 API 작업 사용](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)을 참조하십시오.

## <a name="specify-fields-to-copy"></a>복사할 필드 지정 
작업이 호출되면 **프로젝트 복사** 는 프로젝트 보기 **프로젝트 열 복사** 를 조회하여 프로젝트를 복사할 때 복사할 필드를 결정합니다.
