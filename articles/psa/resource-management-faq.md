---
title: 리소스 관리 FAQ
description: 이 항목은 리소스 관리에 대해 자주 묻는 질문에 대한 답변을 제공합니다.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144376"
---
# <a name="resource-management-faq"></a>리소스 관리 FAQ

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>팀원과 리소스 요건 사이의 차이는 무엇입니까?

프로젝트 팀원은 과업에 할당, 예약 또는 초과 예약되거나 결재자로 설정될 수 있습니다. 리소스 요건은 수요의 초안으로 프로젝트 팀원 없이도 존재할 수 있습니다. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>제안된 시간과 가예약된 시간 사이의 차이는 무엇입니까?

제안된 시간과 가예약된 시간은 가시성이 다릅니다. 제안된 시간은 리소스 요청을 사용하여 요청을 시작한 리소스 관리자와 프로젝트 관리자에게만 표시됩니다. 가예약된 시간은 스케줄 보드에 액세스할 수 있는 모든 사용자가 볼 수 있습니다.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>팀의 리소스에 대한 가예약된 시간을 어떻게 확인할 수 있습니까?

리소스 요건 예약 시, 가예약을 할 수 있습니다. 프로젝트 팀에서 가예약된 리소스는 가예약된 시간이 있는 팀웜으로 표시됩니다. 또한 스케줄 게시판에도 표시됩니다.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>예약한 리소스(일반 또는 명명된)에 대해 요구되는 시간과 시작 날짜 및 종료 날짜를 변경하려면 어떻게 해야 합니까?

리소스를 예약한 후 요구되는 변경을 하려면 **예약 정비** 를 선택하십시오.

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation은 어떤 리소스 타입을 지원합니까?

**사용자** 및 **연락처** 가 Dynamics 365 Project Service Automation에서 지원되는 유일한 리소스 타입입니다. 다른 타입의 리소스(예: **장비** 및 **그룹**)를 만들 수 있지만 종단 간 사용 사례는 지원되지 않습니다.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>할당과 예약 사이의 차이는 무엇입니까?

할당은 프로젝트 스케줄의 프로젝트 과업에 리소스를 할당하는 것입니다. 리소스는 실제 또는 일반 리소스일 수 있습니다. 예약은 프로젝트에 리소스를 확정 또는 가배정하는 것입니다. 확정 예약은 리소스의 능력을 소비합니다. 이상적으로는, 실제 리소스의 경우 예약과 할당이 다르지 않기 때문에 일치해야 합니다. 그러나 PSA는 이 일치를 강제하지 않습니다. 조정 보기에는 리소스의 예약 및 할당이 일치하지 않는 프로젝트 관리자가 표시됩니다.


[!INCLUDE[footer-include](../includes/footer-banner.md)]