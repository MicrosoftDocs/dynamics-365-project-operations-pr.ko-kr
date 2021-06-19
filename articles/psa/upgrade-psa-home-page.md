---
title: 홈 페이지 업그레이드
description: 이 항목은 Dynamics 365 Project Service Automation에서 새 기능 및 변경된 기능에 대한 중요한 정보와 최신 버전으로 업그레이드하는 프로세스를 확인할 수 있는 위치를 보여줍니다.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012369"
---
# <a name="upgrade-home-page"></a>홈 페이지 업그레이드

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>PSA 버전 2.x 또는 1.x에서 버전 3.x로 업그레이드

### <a name="new-instances"></a>새 인스턴스

2019년 5월 17일 현재 새 인스턴스 프로비저닝 중에 Project Service Automation이 선택되면 버전 3.x가 기본적으로 설치됩니다.

### <a name="existing-instances"></a>기존 인스턴스

이전에는 PSA 버전 2.x의 인스턴스를 가지고 있고 PSA의 통합 클라이언트 인터페이스 기반(UCI) 버전인 버전 3.x로 업그레이드해야 하는 고객은 Microsoft 지원팀에 연락하여 인스턴스의 세부 정보를 제공해야 했습니다. 그러면 지원팀이 버전 3.x로 업그레이드하기 위한 인스턴스를 활성화할 수 있었습니다. 2020년 3월 1일부터 PSA 버전 2.x 인스턴스가 있고 버전 3.x로 업그레이드해야 하는 고객은 Microsoft 지원팀에 문의하지 않고도 관리 포털에서 직접 인스턴스를 업그레이드할 수 있습니다.  

> [!NOTE]
> PSA 버전 3.x에는 중요한 변경 사항이 포함되어 있습니다. 향상된 사용자 환경을 제공하기 위해 통합 인터페이스 프레임워크를 기반으로 구축되었습니다. 재설계된 이 앱은 일관되고 균일한 사용자 인터페이스(UI)를 제공하며, 어떤 화면 크기 또는 기기에서도 최적의 보기를 위한 반응형 디자인 원칙을 따릅니다. 애플리케이션 전체에 다른 변경 사항이 있습니다. 변경된 영역 중 일부는 가격 책정, 예약 및 리소스, 시간, 경비 및 결재를 포함합니다.

업그레이드 프로세스를 시작하기 전에 다음 과업을 완료하는 것이 좋습니다:

- 식별된 인스턴스에 Dynamics 365 Field Service 및 Project Service Automation이 설치되어 있는지 확인합니다. 두 솔루션이 모두 설치된 경우, 인스턴스의 정기적인 사용을 다시 시작하기 전에 둘 다 업그레이드하도록 계획해야 합니다.
- 다음 항목을 주의 깊게 검토하십시오. 버전들 사이의 변경 사항에 대한 인식과 이해는 업그레이드 프로세스에 도움이 됩니다. 이러한 항목들은 PSA의 주요 변경 사항에 대한 정보와 버전 3.x로의 업그레이드 계획에 대한 고려 사항 및 권장 사항을 제공합니다.

    - [Project Service Automation 버전 3의 새로운 내용 또는 변경 내용](whats-new-changed-v3.md)
    - [업그레이드 고려 사항 - Project Service Automation 버전 2.x 또는 1.x에서 버전 3](upgrade-v3.md)

- 생산 인스턴스를 업그레이드하기 전에 샌드박스 인스턴스를 업그레이드하여 구현의 변경 사항을 평가하십시오.

앞에서 언급한 항목을 검토하고 PSA 버전 3.x 또는 UCI 기반 버전으로 업그레이드할 준비가 된 후 관리 센터에서 업그레이드를 사용할 수 있도록 Microsoft 지원팀에 요청을 제출하십시오. 요청에서 인스턴스의 세부 정보를 제공합니다.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>새로 만든 인스턴스에서 PSA의 이전 버전(PSA 버전 2.x)

2019년 5월 17일부로 모든 새 인스턴스에 UCI가 기본 클라이언트로 사용됩니다. 이러한 변경에 따라 PSA 버전 3.x 및 Field Service 버전 8.x는 UCI 클라이언트에서 작동하도록 설계되었기 때문에 기본적으로 프로비전됩니다.

2020년 3월 1일부터 Dynamics PSA 고객은 더 이상 이전 버전의 PSA(예: PSA 버전 2.x 이하)로 새 환경을 만들 수 없습니다. 새로운 환경에서는 PSA 버전 3.x만 제공됩니다.

> [!NOTE]
> 이전 버전의 Field Service 및 PSA 애플리케이션을 사용할 때 최상의 경험을 위해서는 **시스템 설정** 페이지로 이동하여, **새 통합 인터페이스만 사용(권장)** 필드를 위해 **아니요** 를 선택하십시오. 이러한 버전은 UCI에서 올바르게 로드되도록 설계되지 않았기 때문입니다. UCI를 끄면 이전 웹 클라이언트를 사용하여 이러한 버전의 Field Service 및 PSA를 열고 실행할 수 있습니다. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]