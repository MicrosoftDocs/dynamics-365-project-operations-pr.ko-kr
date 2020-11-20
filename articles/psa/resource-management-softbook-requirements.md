---
title: 요건 가예약
description: 이 항목은 요건을 가예약하는 방법에 대한 정보를 제공합니다.
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124106"
---
# <a name="soft-book-requirements"></a>요건 가예약

리소스 요건은 확정 예약할 수 있습니다. 확정 예약은 리소스의 능력을 소비하는 제안을 만듭니다. 그런 다음 제안서가 승인을 위해 요청자에게 다시 발송됩니다. 가예약은 프로젝트 팀에 리소스를 임시로 추가하고 스케줄 게시판에 다른 상태를 가지지만 리소스의 능력을 소비하지는 않습니다. 스케줄 보드에서 리소스를 가예약하려면 **예약 상태** 필드를 **가예약** 으로 설정합니다.

![예약 상태가 가예약으로 설정됨](media/Resource-Management-image77.png)

**명명된 팀원** 보기에 **팀** 탭이 있으면 거기에 리소스가 나타납니다. 가예약된 시간은 **가예약된 시간** 열에 보고됩니다.

![명명된 팀원 보기에서 가예약된 시간](media/Resource-Management-image78.png)

가예약된 팀원은 과업에 할당할 수 있습니다.

![과업에 할당된 가예약된 팀원](media/Resource-Management-image79.png)

**조정** 탭은 확정 예약만 고려하므로 **조정** 탭에는 리소스를 가예약하기 위한 예약이 표시되지 않습니다.

![조정 탭에서 예약하지 않고 가예약된 리소스](media/Resource-Management-image80.png)

> [!NOTE]
> 일반 팀원으로부터 생성된 요건에서 리소스를 가예약할 수 없습니다.

스케줄 게시판에서 리소스에 대한 가예약에는 다른 색이 사용됩니다.

![스케줄 게시판에서 가예약](media/Resource-Management-image81.png)

가예약을 확정 예약으로 전환하려면 스케줄 게시판에서 가예약을 마우스 오른쪽 버튼으로 클릭한 다음 **상태 변경** \> **확정 예약** \> **확정** 을 선택합니다.

![예약 상태를 확정으로 변경](media/Resource-Management-image82.png)

예약이 변경되고 스케줄 게시판에서 상태가 변경됩니다. 예약 상태가 이제 **확정** 이기 때문에 리소스가 예약됨으로 표시되고 능력 및 가용성이 조정됩니다.

동일한 방법을 사용하여 스케줄 게시판에서 확정 예약 또는 가예약을 취소할 수 있습니다.

가예약된 리소스를 프로젝트의 **팀** 탭에서 확정 예약으로 전환하려면 리소스를 선택한 다음 **확인** 을 선택합니다.

![확인 명령](media/Resource-Management-image83.png)
