---
title: 리소스 관리 모드 개요
description: 이 항목은 Dynamics 365 Project Operations에서 리소스 관리 기능에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118526"
---
# <a name="resource-management-modes-overview"></a>리소스 관리 모드 개요

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


Dynamics 365 Project Operations는 전체 예약 흐름을 실행하기 위해 두 가지 모드를 지원합니다. 관리 모드는 프로젝트 매개 변수로 정의되며 비즈니스 변경이 필요한 경우 수정할 수 있습니다.    

## <a name="central-mode"></a>중앙 모드
프로젝트에 대한 리소스 할당을 중앙 집중화하는 조직의 경우 중앙 모드는 프로젝트 관리자가 프로젝트 수준에서 리소스 요구 사항을 정의할 수 있도록 하는 방법을 제공합니다. 리소스 요구 사항의 이행은 리소스 관리자에게 위임됩니다. 프로젝트 관리자는 리소스 관리자가 제안한 리소스를 수락하거나 거부할 수 있습니다.

![중앙 모드](./media/resource-management-central.png)

중앙 모드로 리소스를 관리하려면 다음을 참조하십시오.

- [작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [리소스 요건에서 명명된 리소스 예약](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [리소스 요청 제출](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [리소스 요청 이행](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [리소스 요청에서 제안된 프로젝트 리소스를 수락 또는 거부](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>하이브리드 모델
리소스 할당에 유연성이 필요한 조직의 경우 하이브리드 모드를 사용하면 프로젝트 관리자와 리소스 관리자 모두 리소스를 예약할 수 있습니다.

![하이브리드 모드](./media/resource-management-hybrid.png)

지원되는 중앙 모드 프로세스 외에도 다음 항목을 참조하여 하이브리드 모드에서 지원되는 다른 모든 예약 흐름을 관리합니다.

프로젝트에 리소스를 직접 예약
- [프로젝트 팀에 지정된 예약 가능한 리소스 예약 및 작업 배정](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

리소스 요구 사항에서 리소스 예약:
- [작업에 일반 예약 가능한 리소스 할당 및 리소스 요건 생성](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [리소스 요건에서 명명된 리소스 예약](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]