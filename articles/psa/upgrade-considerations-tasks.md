---
title: 작업 세분화 구조를 위한 업그레이드 고려 사항
description: 이 항목은 작업 세분화 구조를 Project Service Automation 2.x에서 3.x로 업그레이드하는 방법을 설명합니다.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149551"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>작업 세분화 구조를 위한 업그레이드 고려 사항

[!include [banner](../includes/psa-now-project-operations.md)]

이 항목은 작업 세분화 구조를 Project Service Automation 2.x에서 3.x로 업그레이드하는 방법을 설명합니다. 이 항목은 Project Service Automation(PSA)에서 성공적인 업그레이드를 위해 요구되는 건전한 프로젝트의 상태를 정의합니다. 업그레이드를 실패하게 만드는 일반적인 차단 조건에 대한 정보도 있습니다. 프로젝트 스케줄 내에서 프로젝트 과업 및 그 기능을 정의하는 데 대한 자세한 설명은 [프로젝트 스케줄](project-creating.md)을 참조하십시오.

## <a name="key-entities"></a>주요 엔터티
리소스가 이미 로드된 정확한 작업 세분화 구조의 경우 다음 엔터티가 요구됩니다:

- [프로젝트](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [프로젝트 팀](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [프로젝트 작업](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [리소스 할당](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [프로젝트 작업 종속성](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [예약 가능한 리소스](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

리소스가 로드한 작업 세분화 구조를 정의하려면 다음 단계를 완료해야 합니다:

1. 새 프로젝트 만들기. 새 프로젝트를 만드는 방법에 대한 자세한 설명은 [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)를 참조하십시오.
2. 하나 이상의 과업을 만듭니다. 과업을 만드는 방법에 대한 자세한 설명은 [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)를 참조하십시오.
3. 과업 종속성을 정의합니다. 자세한 내용은 [프로젝트 작업 종속성](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)을 참조하세요.
4. 프로젝트에 프로젝트 팀원을 배정합니다. 자세한 설명은 [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)을 참조하십시오.
5. 과업에 프로젝트 팀원을 배정합니다. 자세한 설명은 [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)를 참조하십시오.

## <a name="project-team-relationships"></a>프로젝트 팀 관계

성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:
- 모든 프로젝트 팀원이 예약 가능한 리소스와 연계되어야 합니다.
- 모든 프로젝트 팀원이 같은 프로젝트와 연계되어야 합니다. 

## <a name="project-task-relationships"></a>프로젝트 과업 관계
성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:

- 관련 과업은 동일한 프로젝트와 연계되어야 합니다.
- 모든 행 과업에는 상위 과업이 있어야 합니다.
- 모든 과업에는 상위 프로젝트가 있어야 합니다.

### <a name="valid-conditions"></a>유효한 조건

- 모든 과업 기간은 1시간보다 크거나 같아야 하며(>=) 1,800,000분(1,250일)보다 작아야 합니다.*
- 모든 과업은 시작 날짜가 2000/01/01 이후여야 합니다.*
- 모든 과업은 현재 날짜로부터 17년 이내의 시작 날짜가 있어야 합니다.*
- 모든 과업은 시작 날짜가 완료 날짜보다 일찍 또는 같아야 합니다.
- 분류에 대한 모든 처리 타입(경비, 자재, 세금 및 시간)에는 **기본 단위** 및 **단위 그룹** 에 대한 값이 있어야 합니다.
- 문자가 있는 날짜 형식은 피해야 합니다.

### <a name="potential-mitigation-steps"></a>잠재적인 완화 단계
- 상세하게 찾기를 사용하여 프로젝트 ID가없는 프로젝트 작업을 식별하십시오.
- 예약된 기간이 1,800,000보다 큰 프로젝트 작업을 식별하려면 상세하게 찾기를 사용하십시오.
- 데이터를 변경하기 전에 데이터를 불량 상태로 만드는 엔터티와 관련된 사용자 지정 내용을 조사해야 합니다. 이러한 사용자 지정은 데이터 관련 업데이트를 진행하기 전에 해결해야 합니다.
- 연결된 프로젝트가 없는 것으로 식별된 작업이 필요하지 않거나 올바른 상위 프로젝트와 연관되어야 하는 경우 해당 작업을 삭제하십시오.
- 기간이 1,250일을 초과하는 작업의 경우 가능하다면 전체 기간을 나타내는 여러 작업을 추가하는 것이 좋습니다.

> [!NOTE]
> 별표(\*)로 표시된 항목에는 고객 관계 관리(CRM) 시스템이 7,320번의 되풀이 확장만 지원함으로 인한 한도가 있습니다. 이 한도 밑으로 유지해야 합니다.

## <a name="resource-assignment-relationships"></a>리소스 할당 관계
성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:

- 작업 분할 구조의 모든 리소스 할당은 동일한 프로젝트에 관련되어야 합니다.
- 작업 분할 구조의 모든 리소스 할당은 동일한 프로젝트의 프로젝트 팀원들과 연계되어야 합니다.

### <a name="potential-mitigation-steps"></a>잠재적인 완화 단계
- 위에서 설명한 조건을 벗어나는 모든 작업을 식별하십시오.  
- 더 이상 유효하지 않은 리소스 할당은 삭제해야 합니다.

## <a name="project-task-dependency-relationships"></a>프로젝트 과업 종속성 관계
성공적인 업그레이드를 위해서는 다음 관계를 올바르게 유지해야 합니다:

- 모든 프로젝트 과업 종속성은 동일한 프로젝트에 관련되어야 합니다.
- 과업은 두 번 이상 참조된 동일한 종속성을 가질 수 없습니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]