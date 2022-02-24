---
title: 보안 모델
description: 이 토픽은 Dynamics 365 Project Operations의 보안 모델에 대한 정보를 제공합니다.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642911"
---
# <a name="security-model"></a>보안 모델

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations는 Microsoft Office 그룹과 협업하는 역할 기반 비즈니스 보안 모델을 허용하는 고유한 보안 모델을 포함합니다. 


## <a name="security-roles"></a>보안 역할
Project Operations 프런트 엔드 기능에는 다음 역할이 포함됩니다.

| 역할                          | 설명                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| 연습 관리자              | 프로젝트 간 보고를 지원합니다.                                                                                                            | 사업부              |
| 프로젝트 승인자              | 프로젝트에 대한 시간 및 경비를 승인합니다.                                                                                                                              | 사업부 |
| 프로젝트 청구 관리자 | 송장 제안을 생성합니다.                                                                                                                                                 | 사업부 |
| 프로젝트 관리자               | 프로젝트 계획을 작성하고 자원을 요청합니다.                                                                                                                              | 사업부 |
| 프로젝트 리소스              | 시간을 예약 및 보고할 수 있는 팀 구성원.                                                                                                          | 사업부|
| 리소스 관리자              | 리소스 요청 및 예약 이행과 같은 모든 리소스 관리 기능은 하이브리드 프로젝트 관리자 + 리소스 관리자 구성 및 단일 및 중앙 집중식 리소스 관리자 역할을 지원하도록 분리됩니다. | 사업부 |


웹용 Microsoft Project에는 다음 역할이 포함됩니다.

| 역할           | 설명                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| 프로젝트 사용자   | 자신의 프로젝트를 만들고 공유된 프로젝트를 볼 수 있는 Project의 공동 작업 사용자입니다. | User   |
| 프로젝트 시스템 | 애플리케이션 컨텍스트에 사용되는 역할입니다. 고객은 이 시스템 역할을 사용해서는 안됩니다.                                    | 전역 |

## <a name="security-enforcement"></a>보안 적용
프로젝트 수준에서 수행되는 작업은 로그인한 사용자의 컨텍스트에서 수행됩니다. 즉, 프로젝트를 생성, 열기 또는 삭제하려면 사용자가 CDS에서 액세스할 수 있어야 합니다. CDS에서의 액세스는 플랫폼에 포함된 모든 가능한 메커니즘을 통해 부여될 수 있습니다. 예를 들어, 더 큰 범위의 사용자가 프로젝트에 액세스할 수 있거나 사용자에게 액세스 권한을 부여하는 명시적인 프로젝트 공유 작업이 수행된 경우입니다.

Project Operations에서 프로젝트를 만들 때 이것을 고려하는 것이 중요합니다.

## <a name="modern-group-collaboration-with-project-operations"></a>Project Operations와의 현대적인 그룹 공동 작업
웹용 프로젝트 및 Project Operations는 공동 작업을 위한 최신 그룹을 지원합니다. 그룹을 통해 프로젝트에 추가된 사용자는 프로젝트 계획을 편집할 수 있습니다.

웹용 프로젝트는 할당 시 사용자를 그룹에 자동으로 추가합니다.

그룹은 프로젝트의 권한을 허용하고 협업 아티팩트를 지원하여 공동으로 작업할 수 있습니다. 다음 다이어그램은 그룹 할당 프로세스 중에 발생하는 이벤트 및 상태 변경을 보여줍니다.

Project Operations는 암시적 작업을 통해 그룹을 생성하지 않으며 그룹을 누르는 명시적 작업을 통해서만 생성합니다.

**그룹 관리** 대화 상자의 그룹 구성원 검색은 환경 보안 그룹의 일부로 설정된 사용자로 제한됩니다. 자세한 내용은 [환경에 대한 사용자 액세스 제어: 보안 그룹 및 라이선스](https://docs.microsoft.com/power-platform/admin/control-user-access)를 참조하십시오.

![그룹 모드](./media/groupsmode.png)

1. 프로젝트는 생성된 사용자가 생성하고 소유합니다.
2. 프로젝트 담당자가 팀으로 업데이트됩니다.
3. 담당자 팀은 지정되거나 생성된 Office 그룹에 매핑됩니다.
4. 프로젝트의 원래 담당자가 Office 그룹에 추가됩니다.

## <a name="deployment-recommendation"></a>배포 권장 사항
Office 그룹 공동 작업 모델이 발전함에 따라 시간이 지나면서 보다 세부적인 제어를 제공하는 기능이 추가될 것입니다. 현재 Project Operations를 배포하는 고객은 기존 Microsoft Dynamics 365 보안 모델에 집중하는 것이 좋습니다.

자세한 내용은 [Common Data Service의 보안](https://docs.microsoft.com/power-platform/admin/wp-security)을 참조하십시오.

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations 및 Microsoft Dynamics 365 Finance 보안
Project Operations에는 다음 역할이 포함됩니다.

- 프로젝트 관리자
- 프로젝트 회계사

Finance의 보안에 대한 자세한 내용은 [역할 기반 보안](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)을 참조하십시오.


