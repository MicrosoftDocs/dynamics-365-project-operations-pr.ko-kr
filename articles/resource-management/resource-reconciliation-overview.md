---
title: 리소스 조정 개요
description: 이 항목은 프로젝트에 대한 리소스 예약 및 할당이 정렬되었는지 확인하는 방법에 대한 정보를 제공합니다.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897459"
---
# <a name="resource-reconciliation-overview"></a>리소스 조정 개요

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

팀 구성원의 경우 예약 및 할당이 느슨하게 결합됩니다. 즉, 리소스는 할당을 가질 수 있지만 예약은 없을 수도 있고, 예약을 할 수 있지만 할당은 없을 수 있습니다. 예약과 할당은 정렬되는 것이 좋습니다. 그래야 리소스가 작업 할당을 수행할 수 있는 생산 능력이 이행됩니다. 그러나 예약은 가용성을 기반으로 할 수 있으며 프로젝트가 계속됨에 따라 작업 타이밍이 변경될 수 있습니다. 따라서 예약과 할당의 느슨한 결합은 유연성을 제공합니다.

**프로젝트** 양식의 **조정** 탭을 사용하면 프로젝트 관리자가 프로젝트 팀을 위한 팀원 예약과 배정을 조정할 수 있습니다.

**조정** 탭은 각 팀 구성원에 대해 개별 작업 할당의 수준으로 내려가는 예약 및 할당도 표시합니다. 시간에는 셀에 수 개월~수 일의 기간을 나타내는 시간이 표시됩니다.

탭에는 **총** 열과 함께 프로젝트의 전체 순합계도 표시됩니다.

각 리소스에 대해 탭은 팀 구성원의 예약과 해당 팀원의 과업 할당 롤업 사이의 차이를 계산합니다. 이상적으로는 이 차이가 0(제로)이어야 합니다. 즉, 리소스의 예약과 작업 할당 사이에 차이가 없어야 합니다. 차이점은 두 가지 조건에 주의를 끌기 위한 색상과 그늘입니다.

- **예약 부족** – 리소스에 예약보다 많은 작업이 있을 때 예약 부족이 발생합니다. 이 능력은 예약되지 않았므로 프로젝트 관리자는 부족을 충당하기 위해 리소스 예약을 연장하여 이 조건을 수정할 수 있습니다.
- **초과 예약** – 리소스가 프로젝트에 예약되었지만 과업에 할당되지 않은 경우 초과 예약이 발생합니다. 작업 할당이 발생하기 전에 리소스가 프로젝트에 예약된 경우 이 조건을 사용할 수 있습니다. 그러나 다른 경우에는 작업에 이 리소스를 할당할 계획이 없습니다. 이러한 경우 프로젝트 관리자는 다른 프로젝트에 능력을 사용할 수 있도록 리소스의 예약을 취소하는 것을 고려해야 합니다.

경우에 따라 일 수준(예: 월 수준)보다 높은 수준에서 시간을 볼 때 리소스에 대한 순 차이(예: 예약 = 할당)가 표시될 수 있습니다. 그러나 주 수준의 시간을 살펴보면 첫 주에 0시간의 할당과 40시간의 예약을 볼 수 있지만, 두 번째 주에 40시간의 할당과 0시간의 예약이 있는 것을 볼 수 있습니다. 전반적으로, 예약 및 할당은 조정되지만 1주일에서 다음 주까지 다릅니다.

더 높은 시간 수준을 볼 때 **조정** 탭의 셀은 낮은 수준에 차이가 있음을 알리는 표시등이 표시됩니다. 셀을 두 번 클릭하여 확대하고 차이를 볼 수 있습니다. 그런 다음 마우스 오른쪽 단추로 클릭하여 축소할 수 있습니다. 리소스를 선택한 다음 그리드 도구 모음에서 **다음 차이** 컨트롤을 사용하여 해당 리소스에 대한 예약과 할당 간의 다음 차이로 이동하여 확인할 수 있습니다. 그런 다음 **이전 차이** 컨트롤을 사용하여 다시 돌아갈 수 있습니다. **설정**에서 차이 표시기 및 탐색 동작을 해제할 수도 있습니다.


리소스에 대한 작업 할당이 있지만 예약이 없는 경우, **조정** 탭의 **프로젝트** 페이지에서 예약 부족을 선택한 다음 **예약 연장**을 선택합니다. **예약 연장** 대화 상자가 나타나고 리소스 부족을 해결하는 데 필요한 예약을 표시합니다. 또한 모든 프로젝트 또는 기타 예약 가능한 엔터티에서 리소스의 기존 예약을 표시합니다. 리소스의 가용성에 관계없이 리소스에 대한 예약을 만들려면 **확인**을 선택하면 초과 예약이 발생할 수 있습니다.

그런 다음 프로젝트 관리자 또는 리소스 관리자는 일정 게시판을 사용해서 리소스가 생산 능력을 초과해서 예약된 모든 상황을 관리할 수 있습니다.

