---
title: 예약 및 할당 비교
description: 이 항목은 리소스 예약과 리소스 할당 간의 차이점에 대한 정보를 제공합니다.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841180"
---
# <a name="bookings-vs-assignments"></a>예약 및 할당 비교

_**적용 대상 :** 리소스/비 재고 기반 시나리오를 위한 Project Operations, Lite 배포 - 견적 송장 처리_

예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다. 확정 예약은 리소스의 능력을 소비합니다. 예약은 팀의 조직 개념을 나타내므로 다양한 프로젝트에서 리소스가 사용되는 방식을 이해할 수 있습니다. Dynamics 365 Project Operations는 예약을 프로젝트 수준 개념으로 간주합니다. 

예약과 달리 할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 약정하는 것입니다. 리소스는 이름이 지정되거나 일반이 될 수 있습니다.  리소스 요구 사항이 프로젝트 작업 할당에서 파생되면 Project Operations는 리소스 할당의 작업량 등고선을 사용하여 리소스 요구 사항 세부 정보의 등고선을 만듭니다. 그러나 리소스 할당에 대한 참조는 유지되지 않습니다. 리소스 요구 사항에서 파생된 예약에 대한 업데이트는 리소스 할당을 업데이트하지 않습니다.

일반적으로 리소스 예약 합계는 하나 이상의 작업에 대한 리소스 할당 합계와 같습니다. 그러나 Project Operations는 이 계약을 강제하지 않습니다. **조정** 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.


