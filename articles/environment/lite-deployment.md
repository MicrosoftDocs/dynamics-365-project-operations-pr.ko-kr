---
title: Project Operations Lite 배포
description: 이 문서에서는 Project Operations 라이트 배포를 설치하는 방법에 대한 정보를 제공합니다.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810987"
---
# <a name="deploy-project-operations-lite"></a>Project Operations Lite 배포

_**적용 대상:** 라이트 배포 - 견적 송장 거래_



Project Operations는 여러 배포 모델을 지원합니다. 최상의 배포 모델을 결정하려면 [배포 유형](determine-deployment-type.md)을 참조하십시오.


> [!IMPORTANT]
> 이 배포, 라이트 배포 – 견적 송장 처리 결과 **Project Operations의 Dataverse 전용 배포** 가 됩니다.

- [Project Operations를 새 Dataverse 환경에 설치](#new)
- [기존 Dataverse 환경에 설치](#existing)
- [이중 쓰기 구성 요소가 있는 기존 Dataverse 환경에 설치](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Lite를 새 Dataverse 환경에 설치

1. Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](/power-platform/admin/global-service-administrators-can-administer-without-license)는 새로운 Dataverse 환경을 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에 생성합니다. **이 환경에 대한 데이터베이스 생성** 및 **Dynamics 365 앱** 이 활성화되었는지 확인합니다. 자세한 내용은 [Power Platform 관리 센터에서 환경 만들기 및 관리](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)를 참조하십시오.
1. Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 선택합니다.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Lite를 기존 Dataverse 환경에 설치 
1. Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](/power-platform/admin/global-service-administrators-can-administer-without-license)는 Project Operations를 설치하려는 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에서 환경을 찾습니다.
1. Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 설치합니다. 자세한 내용은 [Dynamics 365 앱 관리](/power-platform/admin/manage-apps)를 참조하십시오.

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>이중 쓰기 솔루션이 이미 존재하는 기존 Dataverse 환경에 Project Operations Lite 설치

Lite 배포 모드에서 Project Operations를 계속 실행하려면 다음 단계를 따라야 합니다.

1. Project Operations 라이선스가 있는 [전역 또는 Power Platform 관리자](/power-platform/admin/global-service-administrators-can-administer-without-license)는 Project Operations를 설치하려는 [PowerPlatform 관리 센터](https://admin.powerplatform.com)에서 환경을 찾습니다.
1. Dynamics 365 앱의 배포 목록에서 **Microsoft Dynamics 365 Project Operations** 를 설치합니다. 자세한 내용은 [Dynamics 365 앱 관리](/power-platform/admin/manage-apps)를 참조하십시오.
1. 환경에 금융 및 운영 앱 통합에 도움이 되는 이중 쓰기 구성 요소가 설치되어 있으므로 Project Operations 설치는 Project 관련 데이터를 금융 및 운영 앱에 통합하는 데 필요한 기능 및 확장도 설치합니다. Lite 배포에서 Project Operations를 실행하려고 하므로 이러한 통합 구성 요소는 Lite 배포 시나리오에 대한 제한 및 오버헤드를 생성하므로 제거해야 합니다. 솔루션 **Dynamics 365 Project Operations 이중 쓰기** 및 **Dynamics 365 Project Operations 이중 쓰기 엔터티 맵** 을 수동으로 제거하여 이러한 구성 요소를 제거합니다.
1. **Project Operations -> 설정 -> 매개 변수** 로 이동합니다. **프로젝트 매개 변수** 세부사항 페이지를 열고 **솔루션 업그레이드 동작** 필드를 **Lite 전용** 으로 설정합니다. 이렇게 하면 Project Operations의 후속 업그레이드가 통합 구성 요소를 Project Operations로 다시 가져오지 않습니다.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
