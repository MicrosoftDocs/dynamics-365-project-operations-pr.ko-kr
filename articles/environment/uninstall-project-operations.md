---
title: Dynamics 365 Project Operations 제거
description: 이 문서에서는 Dynamics 365 Project Operations를 제거하는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911972"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dynamics 365 Project Operations 제거 

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

Dynamics 365 Project Operations를 제거하려면 관리자 역할을 할당 받아야 합니다.

1. **설정** > **솔루션** 으로 이동합니다.

    ![페이지 설정.](./media/uninstall-proj-ops-solutions.png)
  
2. 다음 표에 나열된 정확한 순서로 솔루션을 제거합니다. 

    | 단계 | 솔루션 이름                                    | 노트                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 2 | ProjectOperations_Anchor                           | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 5 | ProjectService                                     | 추가 메모가 없습니다.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | 추가 메모가 없습니다.                                                                         |
    | 7 | ProjectServiceCore                                 | 추가 메모가 없습니다.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 9 | FieldServiceCommon                                 | 이중 쓰기에 필요(Dynamics 365 Finance 또는 Dynamics 365 Supply Chain Management 포함).   |
    | 10 | msdyn_AssetCommon                                  | 이중 쓰기에 필요(Dynamics 365 Finance 또는 Dynamics 365 Supply Chain Management 포함).   |
    | 11 | msdyn_TESA_Anchor                                  | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 13 | msdyn_TESA                                         | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 14 | ResourceSchedulingControls                         | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Dynamics 365 Field Service에 필요합니다.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 19 | Dynamics365Notes                                   | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 21 | DualWriteCore                                      | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 23 | Dynamics365AssetManagement                         | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 25 | Dynamics365FinanceExtended                         | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 26 | HCMCommon                                          | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 28 | 파티                                              | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 29 | Dynamics365Company                                 | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 30 | CurrencyExchangeRates                              | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
    | 31 | AssetCommon                                        | 찾을 수 없는 경우 이 솔루션을 건너뜁니다.                                                            |
