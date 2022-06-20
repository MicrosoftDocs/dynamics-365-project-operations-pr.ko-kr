---
title: Project Operations 배포 - 라이트
description: 이 문서에서는 Project Operations 라이트 배포를 설치하는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930326"
---
# <a name="deploy-project-operations---lite"></a>Project Operations 배포 - 라이트

_**적용 대상:** 라이트 배포 - 견적 송장 거래_



Project Operations는 여러 배포 모델을 지원합니다. 최상의 배포 모델을 결정하려면 [배포 유형](determine-deployment-type.md)을 참조하십시오.


> [!IMPORTANT]
> 이 배포, 라이트 배포 – 견적 송장 처리 결과 **Project Operations의 Dataverse 전용 배포** 가 됩니다.

- [Project Operations를 새 Dataverse 환경에 설치](#new)
- [기존 Dataverse 환경에 설치](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations를 새 Dataverse 환경에 설치

1. Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](/power-platform/admin/global-service-administrators-can-administer-without-license)는 새로운 Dataverse 환경을 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에 생성합니다. **이 환경에 대한 데이터베이스 생성** 및 **Dynamics 365 앱** 이 활성화되었는지 확인합니다. 자세한 내용은 [Power Platform 관리 센터에서 환경 만들기 및 관리](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)를 참조하십시오.
2. Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 선택합니다.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations를 기존 Dataverse 환경에 설치
1. [리소스/비재고 기반 시나리오를 위한 Project Operations](project-operations-integrated-deployment-overview.md)를 설치하므로 환경이 [이중 쓰기](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)로 구성되지 않았는지 확인합니다.
2. Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](/power-platform/admin/global-service-administrators-can-administer-without-license)는 Project Operations를 설치하려는 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에서 환경을 찾습니다.
3. Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 설치합니다. 자세한 내용은 [Dynamics 365 앱 관리](/power-platform/admin/manage-apps)를 참조하십시오.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
