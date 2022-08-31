---
title: 종료된 프로젝트에 대한 입력을 방지하기 위해 프로젝트 상태 동기화
description: 이 문서에서는 프로젝트 상태를 동기화하여 비활성 또는 닫힌 프로젝트에 대한 항목을 방지하는 방법을 설명합니다.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348042"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>종료된 프로젝트에 대한 입력을 방지하기 위해 프로젝트 상태 동기화

_**적용 대상:** 리소스/비 재고 기반 시나리오에 대한 Project Operations_

## <a name="scenario"></a>시나리오

Contoso는 리소스/비재고 시나리오용 Microsoft Dynamics 365 Project Operations을 사용 중입니다. 정상적인 비즈니스 활동의 일부로 프로젝트가 완료되거나 보류될 수 있습니다. 비용이나 송장이 생성되지 않도록 프로젝트를 비활성화할 수 있습니다.

## <a name="solution"></a>해결 방법

### <a name="prerequisites"></a>전제 조건

-   Microsoft Dynamics 365 Finance 10.0.29 이상이 설치되어 있어야 합니다.
-   프로젝트 V2(msdyn\_projects)용 이중 쓰기 맵 1.0.0.3은 아래 설명된 대로 설치하거나 수동으로 구성해야 합니다.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Project Operations 통합 프로젝트 V2 이중 쓰기 맵의 업데이트된 버전 만들기

Project Operations 프로젝트 V2 이중 쓰기 맵을 업데이트하려면:

1. **데이터 관리** 작업 영역으로 이동하여 **이중 쓰기** 를 선택합니다.
2. **이중 쓰기** 타일을 선택합니다.
3. **테이블 맵** 열에서 **프로젝트 V2 (msdyn\_projects)** 를 찾아 선택하고 중지를 선택합니다.
4. 맵 이름을 선택하여 맵을 연 후 **[없음]** 을 선택합니다.
5. 열 선택 대화 상자에서 **statecode \[Project Status\]** 를 선택한 다음 확인을 선택합니다. 필터 값에 **상태** 를 입력하여 목록을 좁힐 수 있습니다.
6.  **맵 유형** 열에서 **변환 추가 또는 편집** 을 선택하여 변환을 편집합니다.
7.  **변환 유형** 에서 **ValueMap** 을 선택합니다.
8.  **값 매핑** 를 선택한 다음 **키** 및 **값** 을 추가합니다.

   Key       | 값 
   ----------|-------
   InProcess | 12     
   완료됨 | 6     

![이중 쓰기 매핑을 보여주는 스크린샷](media/projectstage-dw-mapping.png)

9. **저장** 을 선택합니다.
10. **이중 쓰 > 프로젝트 V2(msdyn_projects)** 페이지 상단에서 **다른 이름으로 저장** 을 선택합니다.
11. **판매자** 필드의 **테이블 추가** 에서 **CDS 기본 판매자** 를 선택합니다.
12. **버전** 필드를 1.0.0.3으로 설정합니다.
13. **설명** 을 입력한 다음 **저장** 을 선택합니다.
14. **이중 쓰기 > 프로젝트 V2(msdyn_projects)** 페이지 상단에서 **실행** 을 선택하여 맵을 시작한 다음 실행 전에 확인 메시지가 표시되면 **예** 를 선택합니다. 

### <a name="close-a-newly-completed-project"></a>새로 완료된 프로젝트 닫기

Dynamics 365 Finance는 **프로젝트 단계** 필드를 사용하여 **프로세스 중** 또는 **완료** 프로젝트를 구분합니다. **완료** 프로젝트는 비용을 발생시키거나 고객에게 청구할 수 없습니다.

1. 비활성화할 프로젝트를 엽니다.
2. 리본 메뉴에서 **비활성화** 를 선택합니다.

> [!NOTE]
> 재무 컨텍스트에서 둘 다 동일하게 작동하므로 프로젝트를 비활성화하거나 닫을 수 있습니다.

3. 재무에서 **모든 프로젝트 목록** 페이지를 엽니다.
4. 비활성화된 프로젝트가 목록에 표시되지 않는지 확인합니다.
5. 목록 위의 **프로젝트 표시** 필터에서 값을 **활성** 에서 **모두** 로 변경합니다.
6. 이제 비활성화된 프로젝트가 표시됩니다.

재무에서 이 프로젝트에 대한 시간이나 비용을 기록하려고 하면 프로젝트가 선택되지 않아야 합니다. 비용에 프로젝트 번호를 수동으로 입력하면 "프로젝트 단계가 완료되어 프로젝트에 녹음/녹화를 허용하지 않습니다"와 같은 메시지가 표시됩니다. 송장 발행 및 기타 청구 기능은 닫힌 프로젝트의 컨텍스트에 있으므로 비활성화해야 합니다.

