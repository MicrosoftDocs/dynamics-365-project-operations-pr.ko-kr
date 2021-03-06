---
title: 프로젝트 상태 이해
description: 이 항목은 Dynamics 365 Project Operations에서 프로젝트에 할당된 상태에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965684"
---
# <a name="understand-project-status"></a>프로젝트 상태 이해

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_


 **프로젝트 엔터티** 페이지의 **상태** 섹션은 비용과 노력에 따라 프로젝트 상태에 대한 요약을 제공합니다.


## <a name="status-summary-fields"></a>상태 요약 필드

-  **전체 프로젝트 상태** 필드는 프로젝트의 전체 상태를 표시하는 편집 가능한 필드입니다. 이 필드는 녹색, 노란색 및 빨간색과 같은 색상 코딩을 사용하여 위험 증가를 나타냅니다. 
-  **주석** 필드를 사용하면 프로젝트 관리자가 상태에 대한 특정 주석을 입력할 수 있습니다. 
-  **상태 업데이트 날짜** 필드는 편집할 수 없습니다. 이 필드의 값은 상태가 마지막으로 업데이트된 시기를 나타내는 타임 스탬프입니다.
-  **일정 성능** 및 **비용 성능** 필드는 추적 그리드부터 설정됩니다.  **작업량 추적** 보기에서 루트 노드의 일정 및 비용 차이가 양수인 경우 이러한 필드를  **선행**으로 업데이트됩니다. 루트 노드의 일정 및 비용 차이가 음수인 경우 이러한 필드는  **후행**으로 설정됩니다.
